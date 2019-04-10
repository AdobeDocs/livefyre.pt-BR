---
description: null
seo-description: null
seo-title: Usar o Livefyre com o Adobe Analytics e o Gerenciador dinâmico de tags
  (DTM) lk xavvn vefyre com o Adobe Analytics e o Gerenciador dinâmico de tags (DTM)
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Usar o Livefyre com o Adobe Analytics e o Gerenciador dinâmico de tags (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Configure o Adobe Analytics e o Gerenciador dinâmico de tags (DTM) para coletar dados para aplicativos do Livefyre.

## Etapa 1: Configurar eventos no Adobe Analytics {#section_iks_kgd_4cb}

Mapeie eventos do Livefyre para um ou mais Eventos de sucesso personalizados no Gerenciador de conjunto de relatórios do Adobe Analytics.

Para obter mais informações sobre o Gerenciador de conjunto de relatórios, consulte [Gerenciador](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)do conjunto de relatórios.

1. Faça logon no Adobe Analytics como um usuário do administrador.
1. Abra o Gerenciador de conjunto de relatórios de administração do Adobe Analytics.
1. Crie um novo conjunto de relatórios ou escolha uma existente.
1. Edite o conjunto de relatórios clicando no conjunto de relatórios para modificar e navegue **[!UICONTROL Edit Settings > Conversion > Success Events]**até.
1. Mapeie os eventos do Livefyre para um ou mais Eventos de sucesso personalizados.

## Etapa 2: Configurar variáveis de conversão

Mapeie variáveis de conversão do Livefyre (evars) para variáveis de conversão no Gerenciador de conjunto de relatórios de administração do Adobe Analytics. As variáveis de conversão atuam como uma função de classificação para determinar como você planeja identificar os dados coletados dos eventos do Livefyre.

1. No Gerenciador de report suite, clique **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**em.
1. Escolha as variáveis de conversão personalizadas (evars) para usá-las e mapeá-las nas variáveis de conversão do Livefyre. Para mapear uma variável de conversão do Livefyre para uma variável de conversão personalizada:
* Ativar a variável de conversão
* Nomear a variável de conversão
* Fornecer um tipo à variável de conversão
1. Salve as variáveis de conversão personalizadas.

## Etapa 3: Usar o DTM para adicionar o conjunto de relatórios com eventos do Livefyre {#section_t15_2hd_4cb}

Adicione o Adobe Analytics ao DTM para que o Analytics funcione. Para fazer isso, crie uma nova propriedade e ferramenta e adicione o novo conjunto de relatórios com eventos do Livefyre para a propriedade. Para obter mais informações sobre o DTM, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Você não precisa executar essa etapa se já tiver uma propriedade ou uma ferramenta configurada para o conjunto de relatórios configurado com eventos do Livefyre.

1. No DTM, crie ou edite uma propriedade existente.
1. Crie ou edite uma ferramenta existente do Adobe Analytics.
1. Se uma ferramenta Adobe Analytics existente não existir, clique no **[!UICONTROL Add a Tool]** botão.
Defina os seguintes parâmetros para a ferramenta:
* Defina **[!UICONTROL Tool Type]** como **[!UICONTROL Adobe Analytics]**.
* Ativar **[!UICONTROL Automatic Configuration]**.
* Ativar **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Adicione ou confirme o nome do conjunto de relatórios com eventos do Livefyre para o **[!UICONTROL Report Suites]** campo.

## Etapa 4: Configurar uma regra de carregamento de página para configurar o manuseio do Analytics {#section_jfj_j3d_4cb}

Configure uma Regra de carregamento de página para obter todos os dados. A Regra de carregamento de página permite colocar javascript personalizado na regra que registra o evento quando a página é carregada.

>[!NOTE]
>
>Não use Regras baseadas em eventos nem Regras de chamada direta.

1. No DTM, selecione **[!UICONTROL Rules]** tab.
1. Clique **[!UICONTROL Page Load Rules]**em.
1. Clique no **[!UICONTROL Create New Rule]** botão.
1. Abra **[!UICONTROL Conditions]** a seção clicando no **[!UICONTROL Plus]** botão.
1. Acione a regra. Escolha **[!UICONTROL DOM Ready]** ou **[!UICONTROL Onload]** acione tipos se desejar atrasar ou implementar a regra de forma assíncrona.
1. (Opcional) Adicione outros parâmetros para limitar as páginas que exibem Aplicativos do Livefyre. Para obter mais informações sobre opções adicionais de configuração, consulte [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Em **[!UICONTROL Javascript/ Third Party Tags]**, clique na **[!UICONTROL Non-sequential]** guia e, em seguida, clique **[!UICONTROL Add New Script]**em.
1. Selecione **[!UICONTROL Sequential HTML]** como o tipo de script.
1. Adicione o seguinte script no editor de códigos e clique **[!UICONTROL Save Code]**em.
O script a seguir chama a `livefyre_analytics` regra de chamada direta após carregar o Javascript do Livefyre. O exemplo de script a seguir verifica a cada 400 ms para ver se `livefyre.analytics` está na página. Depois que a página é carregada, o livefyre. analytics envia informações de rastreamento.

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

1. Clique **[!UICONTROL Save Code]**em.
1. Clique **[!UICONTROL Save Rule]**em.

## Etapa 5: Criar uma regra de chamada direta para criar a configuração de mapeamento do Adobe Analytics para o Livefyre {#section_gvp_b1g_pdb}

Há outras maneiras de implementar o Livefyre com o DTM usando eventos personalizados, campos de interface do usuário do Adobe Analytics no DTM e elementos de dados. Este documento usa Javascript personalizado para obter o mesmo efeito.

1. No DTM, selecione a **guia Regras** e clique em Regras de chamada **direta**.
1. Clique no botão **Criar nova regra** .
1. Dê um nome à nova regra **do Livefyre Analytics**.
1. Expanda a **área de** configuração das condições.
1. No campo **String** , digite `livefyre_analytics`.
1. Expanda a seção Tag de Javascript/terceiros e clique no botão **Adicionar novo script** .
1. Insira **a configuração do Livefyre Analytics** na caixa **de entrada Nome** da tag.
1. Selecione **Javascript não sequencial**.
1. Insira o seguinte código de configuração do Livefyre no editor de códigos e clique no botão **Salvar código** .

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

* Adiciona um manipulador de análise para todos os eventos de análise do Livefyre. Para cada evento, ele define os dados em um objeto global e, em seguida, envia o evento.

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

var s =_ satellite. gettoolsbytype`('sc')[0]`. getS ();
var evarmap = {appid: ' Evar 81 ',
apptype: ' Evar 82 '};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {flagcancel: ' event 82 ',\
Flagclick: ' event 82 ',\
Flagdiscord: ' event 82 ',\
Flagofensiva: ' event 82 ',\
Flagofftopic: ' event 82 ',\
Flagspam: ' event 82 ',\
Curtir: ' event 82 ',
Load: ' event 81 ',\
Requestmore: ' event 82 ',\
Sharebuttonclick: ' event 82 ',\
Sharefacebook: ' event 82 ',\
Shareonpostclick: ' event 82 ',\
Sharetwitter: ' event 82 ',\
Shareurl: ' event 82 ',\
Sortstream: ' event 82 ',\
Twitterlikeclick: ' event 82 ',
twitterreplyclick: ' event 82 ',\
Twitterretweetclick: ' event 82 ',\
Twitteruserfollow: ' event 82 '};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log (' Track: ', data. type, event);

if (! event) {console.
warn (data. type,' não está mapeado para um evento em AA ');\
return;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = [' events '];\
switch (event) {case'event
82 ': s. evar 83 = data. type;\
vars. push (' evar 83 ');\
break;
padrão:}

[' generator ',' evars ']. foreach (function (type) {\
var obj = datatype[];
for (var d in obj) {if
(obj. hasownproperty (d) & & evarmapd[]) {\
s [evarmapd[]] = objd[];\
vars. push (evarmapd[]);}}});

s. linktrackvars = vars. join (',');\
s. linktrackevents = event;\
s. events = event;

console. log (' linktrackvars: ', s. linktrackvars);\
console. log (' linktrackevents: ', s. linktrackevents);\
console. log (' events: ', s. events);

s. tl ();}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Adiciona um manipulador de análise para todos os eventos de análise do Livefyre. Para cada evento, ele define os dados em um objeto global e, em seguida, envia o evento.

*/function
addanalyticshandler () {Livefyre.
analytics. addhandler (função (events) {(events) || []). Foreach (function (data) {console.
log (' Event handled: ', data. type);
Tracklivefyreevent (data);});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

