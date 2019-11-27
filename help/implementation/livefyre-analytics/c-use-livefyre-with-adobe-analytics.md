---
description: 'null'
seo-description: 'null'
seo-title: Use o Livefyre com o Adobe Analytics e o Dynamic Tag Manager (DTM) lk xavvn vefyre com o Adobe Analytics e o Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 987482066f1ca3c021a5c9f0fc0109edff616c0a

---


# Use o Livefyre com o Adobe Analytics e o Gerenciador dinâmico de tags (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure o Adobe Analytics e o Gerenciador dinâmico de tags (DTM) para coletar dados dos aplicativos Livefyre.

## Etapa 1: Configurar eventos no Adobe Analytics {#section_iks_kgd_4cb}

Mapeie eventos do Livefyre para um ou mais Eventos de sucesso personalizados no Gerenciador de conjunto de relatórios do Adobe Analytics.

Para obter mais informações sobre o Gerenciador de conjuntos de relatórios, consulte Gerenciador [de conjuntos de](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)relatórios.

1. Faça logon no Adobe Analytics como um usuário administrador.
1. Abra o Gerenciador de conjunto de relatórios de administração do Adobe Analytics.
1. Crie um novo conjunto de relatórios ou escolha um existente.
1. Edite o conjunto de relatórios clicando no conjunto de relatórios para modificá-lo e, em seguida, navegue até **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mapeie os eventos do Livefyre para um ou mais Eventos de sucesso personalizados.

## Etapa 2: Configurar variáveis de conversão

Mapeie as variáveis de conversão do Livefyre (eVars) para variáveis de conversão no Adobe Analytics Admin Report Suite Manager. As variáveis de conversão funcionam como uma função de classificação para determinar como você planeja identificar os dados coletados dos eventos do Livefyre.

1. No Gerenciador de conjunto de relatórios, clique em **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Escolha as variáveis de conversão personalizadas (eVars) a serem usadas e mapeie-as para as variáveis de conversão do Livefyre. Para mapear uma variável de conversão do Livefyre para uma variável de conversão personalizada:
* Ativar a variável de conversão
* Nomeie a variável de conversão
* Fornecer um tipo para a variável de conversão
1. Salve as variáveis de conversão personalizadas.

## Etapa 3: Usar o DTM para adicionar seu conjunto de relatórios com eventos do Livefyre {#section_t15_2hd_4cb}

Adicione o Adobe Analytics ao DTM para fazer com que o Analytics funcione. Para fazer isso, crie uma nova propriedade e ferramenta e adicione o novo conjunto de relatórios com eventos do Livefyre à propriedade. Para obter mais informações sobre o DTM, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Não é necessário executar essa etapa se você já tiver uma propriedade ou ferramenta configurada para o conjunto de relatórios configurado com eventos do Livefyre.

1. No DTM, crie ou edite uma propriedade existente.
1. Crie ou edite uma ferramenta Adobe Analytics existente.
1. Se uma ferramenta Adobe Analytics existente não existir, clique no **[!UICONTROL Add a Tool]** botão.
Defina os seguintes parâmetros para a ferramenta:

   * Set **[!UICONTROL Tool Type]** to **[!UICONTROL Adobe Analytics]**.
   * Enable **[!UICONTROL Automatic Configuration]**.
   * Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Adicione ou confirme o nome do conjunto de relatórios com eventos Livefyre ao **[!UICONTROL Report Suites]** campo.

## Etapa 4: Configurar uma regra de carregamento de página para configurar o processamento do Analytics {#section_jfj_j3d_4cb}

Configure uma regra de carregamento de página para extrair todos os dados. A regra de carregamento de página permite que você coloque javascript personalizado na regra que registra o evento quando a página é carregada.

>[!NOTE]
>
>Não use Regras baseadas em eventos ou Regras de chamada direta.

1. No DTM, selecione a **[!UICONTROL Rules]** guia.
1. Clique em **[!UICONTROL Page Load Rules]**.
1. Clique no **[!UICONTROL Create New Rule]** botão.
1. Abra a **[!UICONTROL Conditions]** seção clicando no **[!UICONTROL Plus]** botão.
1. Acione a regra. Escolha os tipos **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** acionadores se desejar atrasar ou implementar a regra de forma assíncrona.
1. (Opcional) Adicione outros parâmetros para limitar as páginas que exibem os aplicativos Livefyre. Para obter mais informações sobre opções de configuração adicionais, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Em **[!UICONTROL Javascript/ Third Party Tags]**, clique na **[!UICONTROL Non-sequential]** guia e, em seguida, clique em **[!UICONTROL Add New Script]**.
1. Selecione **[!UICONTROL Sequential HTML]** o tipo de script.
1. Adicione o script a seguir ao editor de código e clique em **[!UICONTROL Save Code]**.

   O script a seguir chama a regra de chamada `livefyre_analytics` direta depois que o Livefyre JavaScript é carregado. O exemplo de script a seguir verifica a cada 400 ms para ver se `livefyre.analytics` está na página. Depois que a página é carregada, o livefyre.analytics envia informações de rastreamento.

   ```
   /** 
   * Poll for Livefyre.analytics object to exist since it gets loaded via the 
   * Livefyre.js JavaScript file. Depending on the timing, this could already 
   * exist or need a little time. 
   */ 
   function pollForAnalytics() {  
   if (Livefyre.analytics) { 
     _satellite.track('livefyre_analytics'); 
       return true; 
     } 
     setTimeout(pollForAnalytics, 400); 
   } 
   setTimeout(pollForAnalytics, 400);
   ```

1. Clique em **[!UICONTROL Save Code]**.
1. Clique em **[!UICONTROL Save Rule]**.

## Etapa 5: Criar uma regra de chamada direta para construir a configuração de mapeamento do Adobe Analytics para o Livefyre {#section_gvp_b1g_pdb}

Existem outras maneiras de implementar o Livefyre com o DTM usando eventos personalizados, campos de interface do usuário do Adobe Analytics no DTM e elementos de dados. Este documento usa o Javascript personalizado para realizar o mesmo efeito.

1. No DTM, selecione a guia **Regras** e clique em Regras **de chamada** direta.
1. Click on the **Create New Rule** button.
1. Nomeie a nova regra como **Livefyre Analytics**.
1. Expanda a área de configuração de **condições** .
1. No campo **String** , digite `livefyre_analytics`.
1. Expanda a seção Javascript / Tag de terceiros e clique no botão **Adicionar novo script** .
1. Digite **Livefyre Analytics Config** na caixa de entrada Nome **da** tag.
1. Selecione Javascript **** não sequencial.
1. Digite o seguinte código de configuração do Livefyre no editor de código e clique no botão **Salvar código** .

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
     } 
     ]
   
     /** 
   ```

   * Adiciona um manipulador de análises para todos os eventos de análise do Livefyre. Para cada evento, ele define os dados em um objeto global e despacha o evento.

   ```
   */ 
   function addAnalyticsHandler() {  
     Livefyre.analytics.addHandler(function (events) { 
       (events || []).forEach(function (data) {  
         console.log('Event handled:', data.type);  
         trackLivefyreEvent(data); 
       }); 
     }); 
   } 
   addAnalyticsHandler();  
   ```

1. Clique em **Salvar regra**.

## Etapa 6: Aprovar alterações para a regra de carregamento de página {#section_pxc_11t_ycb}

1. Vá para a **[!UICONTROL Approvals]** guia.
1. Clique em **[!UICONTROL Approve]**.
1. Clique **[!UICONTROL Yes, approve]** para confirmar sua aprovação.
1. Ir para **[!UICONTROL Overview > Publish Queue]**.
1. Selecione a regra a ser publicada.
1. Clique em **[!UICONTROL Publish Selected]**.
1. Clique **[!UICONTROL Publish]** para confirmar que deseja publicar.

## Script {#section_xkb_vft_mcb}

O código de amostra a seguir mapeia as eVars específicas para eVars do Livefyre disponíveis. O nome da variável de conversão ( `eVar`) do Livefyre (por exemplo, `appId`) mapeia para o nome que você configurou no Gerenciador de conjunto de relatórios (por exemplo, `eVar81`). Altere os `eVar` nomes neste script para as variáveis de conversão personalizadas.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

O código de amostra a seguir mapeia os eventos específicos que você configurou no Gerenciador de conjunto de relatórios com eventos Livefyre disponíveis. Neste exemplo, `event82` é configurado como qualquer evento de interação do usuário sem diferenciar o tipo de evento de interação do usuário (por exemplo, curtir ou compartilhar conteúdo). Essa é uma maneira eficiente de registrar todas as informações de interação do usuário em um bloco. Também é possível mapear os eventos na interface do usuário do DTM Analytics com referência ao elemento de dados.

```
var eventMap = { 
  FlagCancel: 'event82',  
  FlagClick: 'event82',  
  FlagDisagree: 'event82',  
  FlagOffensive: 'event82',  
  FlagOffTopic: 'event82',  
  FlagSpam: 'event82',  
  Like: 'event82', 
  Load: 'event81',  
  RequestMore: 'event82',  
  ShareButtonClick: 'event82',  
  ShareFacebook: 'event82',  
  ShareOnPostClick: 'event82',  
  ShareTwitter: 'event82',  
  ShareURL: 'event82',  
  SortStream: 'event82',  
  TwitterLikeClick: 'event82', 
  TwitterReplyClick: 'event82',  
  TwitterRetweetClick: 'event82',  
  TwitterUserFollow: 'event82' 
};
```

A amostra a seguir indica que, se não houver um evento nessa lista, não faça nada. Não é necessário modificar esta seção do código.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

O código a seguir diferencia os tipos de eventos que `event82` registram. A variável de conversão registra o tipo de interação do usuário e o script é configurado `eVar83` `eVar83` para separar os dados de interação do usuário por tipo. Assim, `eVar83` você pode dividir os dados gravados em tipos específicos de interações do usuário.

```
  var vars = ['events'];  
  switch (event) { 
    case 'event82': s.eVar83 = data.type;  
      vars.push('eVar83');  
      break; 
    default: 
  } 
   
  ['generator', 'evars'].forEach(function (type) {  
    var obj = data[type]; 
    for (var d in obj) { 
      if (obj.hasOwnProperty(d) && evarMap[d]) {  
        s[evarMap[d]] = obj[d];  
        vars.push(evarMap[d]); 
      } 
    } 
  }); 
   
  s.linkTrackVars = vars.join(',');  
  s.linkTrackEvents = event;  
  s.events = event; 
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

A amostra de código a seguir adiciona um manipulador para ouvir todos os eventos que ocorrem. Ele usa a regra de carregamento da página ao carregar, aguarda a existência de eventos e configura o manipulador para todos os eventos do aplicativo e os rastreia. Não é necessário modificar esse código.

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## Mais informações

Para obter mais informações sobre os tópicos discutidos nesta página, consulte:

* [Gerenciador do Conjunto de relatórios](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Regras](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
