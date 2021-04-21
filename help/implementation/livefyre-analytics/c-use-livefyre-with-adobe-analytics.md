---
description: Configure o Adobe Analytics e o Gerenciador dinâmico de tags (DTM) para coletar dados dos aplicativos do Livefyre.
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
translation-type: tm+mt
source-git-commit: 24d016fbb2771487f8105b2ca0bb0d03dd60cfc1
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 1%

---

# Use o Livefyre com Adobe Analytics e o Gerenciador dinâmico de tags (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure o Adobe Analytics e o Gerenciador dinâmico de tags (DTM) para coletar dados dos aplicativos do Livefyre.

## Etapa 1: Configurar eventos no Adobe Analytics {#section_iks_kgd_4cb}

Mapeie eventos do Livefyre para um ou mais Eventos bem-sucedidos personalizados no Gerenciador de conjunto de relatórios do Adobe Analytics.

Para obter mais informações sobre o Gerenciador de conjunto de relatórios, consulte [Gerenciador de conjunto de relatórios](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Faça logon no Adobe Analytics como um usuário administrador.
1. Abra o Gerenciador do Conjunto de relatórios do Administrador do Adobe Analytics.
1. Crie um novo Conjunto de relatórios ou escolha um existente.
1. Edite o conjunto de relatórios clicando em seu conjunto para modificar e navegue até **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mapeie os eventos do Livefyre a um ou mais Eventos bem-sucedidos personalizados.

## Etapa 2: Configurar variáveis de conversão

Mapeie variáveis de conversão do Livefyre (eVars) para variáveis de conversão no Gerenciador de conjunto de relatórios do Administrador do Adobe Analytics. As variáveis de conversão funcionam como uma função de classificação para determinar como você planeja identificar os dados coletados dos eventos do Livefyre.

1. No Gerenciador de conjunto de relatórios, clique em **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Escolha as variáveis de conversão personalizadas (eVars) a serem usadas e mapeie-as para as variáveis de conversão do Livefyre. Para mapear uma variável de conversão do Livefyre para uma variável de conversão personalizada:
* Ativar a variável de conversão
* Nomeie a variável de conversão
* Atribua à variável de conversão um tipo
1. Salve as variáveis de conversão personalizadas.

## Etapa 3: Use o DTM para adicionar seu conjunto de relatórios com eventos do Livefyre {#section_t15_2hd_4cb}

Adicione o Adobe Analytics ao DTM para fazer com que o Analytics funcione. Para fazer isso, crie uma nova propriedade e ferramenta e adicione o novo conjunto de relatórios com eventos Livefyre à propriedade. Para obter mais informações sobre o DTM, consulte [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).

Não é necessário executar essa etapa se já tiver uma propriedade ou ferramenta configurada para o conjunto de relatórios configurado com eventos do Livefyre.

1. No DTM, crie ou edite uma propriedade existente.
1. Crie ou edite uma ferramenta Adobe Analytics existente.
1. Se uma Ferramenta Adobe Analytics existente não existir, clique no botão **[!UICONTROL Add a Tool]**.
Defina os seguintes parâmetros para a ferramenta:

   * Defina **[!UICONTROL Tool Type]** para **[!UICONTROL Adobe Analytics]**.
   * Ativar **[!UICONTROL Automatic Configuration]**.
   * Ativar **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Adicione ou confirme o nome do conjunto de relatórios com eventos do Livefyre ao campo **[!UICONTROL Report Suites]**.

## Etapa 4: Configurar uma regra de carregamento de página para configurar o tratamento do Analytics {#section_jfj_j3d_4cb}

Configure uma regra de carregamento de página para extrair todos os dados. A regra de carregamento de página permite colocar um javascript personalizado na regra que registra o evento quando a página é carregada.

>[!NOTE]
>
>Não use Regras baseadas em eventos ou Regras de chamada direta.

1. No DTM, selecione a guia **[!UICONTROL Rules]** .
1. Clique em **[!UICONTROL Page Load Rules]**.
1. Clique no botão **[!UICONTROL Create New Rule]**.
1. Abra a seção **[!UICONTROL Conditions]** clicando no botão **[!UICONTROL Plus]**.
1. Acione a regra. Escolha os tipos de acionador **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** se desejar atrasar ou implementar a regra de forma assíncrona.
1. (Opcional) Adicione parâmetros adicionais para limitar as páginas que exibem os aplicativos do Livefyre. Para obter mais informações sobre opções de configuração adicionais, consulte [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. Em **[!UICONTROL Javascript/ Third Party Tags]**, clique na guia **[!UICONTROL Non-sequential]** e, em seguida, clique em **[!UICONTROL Add New Script]**.
1. Selecione **[!UICONTROL Sequential HTML]** como o tipo de script.
1. Adicione o script a seguir no editor de código e clique em **[!UICONTROL Save Code]**.

   O script a seguir chama a regra de chamada direta `livefyre_analytics` depois que o JavaScript do Livefyre é carregado. O exemplo de script a seguir verifica a cada 400 ms para ver se `livefyre.analytics` está na página. Depois que a página é carregada, o livefyre.analytics envia informações de rastreamento.

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

## Etapa 5: Crie uma regra de chamada direta para construir a configuração de mapeamento do Adobe Analytics para Livefyre {#section_gvp_b1g_pdb}

Há outras maneiras de implementar o Livefyre com DTM usando eventos personalizados, campos da interface do usuário do Adobe Analytics no DTM e elementos de dados. Este documento usa o Javascript personalizado para obter o mesmo efeito.

1. No DTM, selecione a guia **Rules** e clique em **Direct Call Rules**.
1. Clique no botão **Criar nova regra**.
1. Nomeie a nova regra **Livefyre Analytics**.
1. Expanda a área de configuração **conditions**.
1. No campo **String**, digite `livefyre_analytics`.
1. Expanda a seção Javascript / Tag de terceiros e clique no botão **Adicionar novo script**.
1. Insira **Livefyre Analytics Config** na caixa de entrada **Tag Name**.
1. Selecione **Javascript não sequencial**.
1. Insira o seguinte código de configuração do Livefyre no editor de código e clique no botão **Salvar código**.

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

   * Adiciona um manipulador de análise para todos os eventos de análise do Livefyre. Para cada evento, ele define os dados em um objeto global e, em seguida, despacha o evento.

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

1. Clique em **Salvar Regra**.

## Etapa 6: Aprovar alterações para Regra de Carregamento de Página {#section_pxc_11t_ycb}

1. Vá para a guia **[!UICONTROL Approvals]** .
1. Clique em **[!UICONTROL Approve]**.
1. Clique em **[!UICONTROL Yes, approve]** para confirmar a aprovação.
1. Ir para **[!UICONTROL Overview > Publish Queue]**.
1. Selecione a Regra a ser publicada.
1. Clique em **[!UICONTROL Publish Selected]**.
1. Clique em **[!UICONTROL Publish]** para confirmar que deseja publicar.

## Script {#section_xkb_vft_mcb}

O código de amostra a seguir mapeia as eVars específicas para eVars do Livefyre disponíveis. O nome da variável de conversão do Livefyre ( `eVar`) (por exemplo, `appId`) mapeia para o nome que você configurou no Gerenciador de conjunto de relatórios (por exemplo, `eVar81`). Altere os nomes `eVar` neste script para as variáveis de conversão personalizadas.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

O código de amostra a seguir mapeia os eventos específicos configurados no Gerenciador de conjunto de relatórios com eventos do Livefyre disponíveis. Neste exemplo, `event82` é configurado como qualquer evento de interação do usuário sem diferenciar qual tipo de evento de interação do usuário (por exemplo, curtir ou compartilhar conteúdo). Essa é uma maneira eficiente de registrar todas as informações de interação do usuário em um bloco. Também é possível mapear os eventos na interface do usuário do DTM Analytics com referência ao elemento de dados.

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

A amostra a seguir declara que, se não houver um evento nessa lista, não faça nada. Não é necessário modificar essa seção do código.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

O código a seguir diferencia os tipos de evento que `event82` registra. A variável de conversão, `eVar83` registra o tipo de interação do usuário e o script configura `eVar83` para separar os dados de interação do usuário por tipo. Assim, `eVar83` permite dividir os dados registrados em tipos específicos de interações do usuário.

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

A amostra de código a seguir adiciona um manipulador para ouvir todos os eventos que ocorrem. Ela usa a regra de carregamento de página ao carregar, aguarda a existência de eventos e configura o manipulador para todos os eventos do aplicativo e os rastreia. Não é necessário modificar esse código.

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

* [Gerenciador do Conjunto de relatórios](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [Regras](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
