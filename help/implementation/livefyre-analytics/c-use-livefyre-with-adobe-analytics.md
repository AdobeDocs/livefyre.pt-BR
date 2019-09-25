---
description: 'null'
seo-description: 'null'
seo-title: Use o Livefyre com o Adobe Analytics e o Dynamic Tag Manager (DTM) lk xavvn vefyre com o Adobe Analytics e o Dynamic Tag Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {appId: 'eVar81',appType: 'eVar82'};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap = {FlagCancel: 'event82',\
FlagClick: 'event82',\
SinalizarDiscordo: 'event82',\
FlagOffensive: 'event82',\
FlagOffTopic: 'event82',\
SinalizarSpam: 'event82',\
Curtir: 'event82',Load: 'event81',\
Solicitar mais: 'event82',\
ShareButtonClick: 'event82',\
ShareFacebook: 'event82',\
ShareOnPostClick: 'event82',\
ShareTwitter: 'event82',\
ShareURL: 'event82',\
SortStream: 'event82',\
TwitterLikeClick: 'event82',TwitterReplyClick: 'event82',\
TwitterRetweetClick: 'event82',\
TwitterUserSeguir: 'event82'};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLivefyreEvent(data) {\
var event =[eventMapdata.type];
console.log('Track:', data.type, event);

if (!event) {console.warn(data.type, 'não está mapeado para um evento em AA');\
regresso; }

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = ['events'];\
switch (event) {case 'event82': s.eVar83 = data.type;\
vars.push('eVar83');\
quebra;
padrão: }

['generator', 'evars'].forOnce(function (type) {\
var obj =[datatype];
for (var d in obj) {if (obj.hasOwnProperty(d) &amp;&amp;[evarMapd]) {\
s[[evarMapd]] =[objd];\
vars.push([evarMapd]);
}});

s.linkTrackVars = vars.join(',');\
s.linkTrackEvents = event;\
s.events = event;

console.log('linkTrackVars:', s.linkTrackVars);\
console.log('linkTrackEvents:', s.linkTrackEvents);\
console.log('events:', s.events);

s.tl();
}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Adiciona um manipulador de análises para todos os eventos de análise do Livefyre. Para cada evento, ele define os dados em um objeto global e despacha o evento.

*/function addAnalyticsHandler() {Livefyre.analytics.addHandler(function (events) {(events)|| []).forAt(function (data) {console.log('Event handling:', data.type);
trackLivefyreEvent(data);
});
}); }

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

