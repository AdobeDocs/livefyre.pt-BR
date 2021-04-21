---
title: Eventos do Livefyre Analytics
description: Eventos do Livefyre Analytics
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Eventos do Livefyre Analytics

## Definição de objeto de evento {#section_dh1_yhn_pdb}

O código a seguir define os campos no objeto de evento que são recebidos pelo manipulador de análise em uma página.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Eventos e eVars do Livefyre Analytics {#section_u3k_tft_mcb}

Os seguintes eventos do Livefyre a serem mapeados para eventos personalizados a serem usados em relatórios usando o Gerenciador de conjunto de relatórios. Para obter mais informações sobre Conjuntos de relatórios no Adobe Analytics, consulte [Gerenciador do Conjunto de relatórios](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Para obter mais informações sobre como usar eventos do Livefyre com o Gerenciador de conjunto de relatórios, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos do Livefyre Analytics

| Evento | Descrição |
|---|---|
| Inicializar | Quando uma página que inclui pelo menos um aplicativo Livefyre é carregada |
| Load | Sempre que um aplicativo era carregado em uma página, independentemente da exibição do usuário |
| Exibir | Quando um aplicativo entrou no visor pela primeira vez. |
| Publicar | Sempre que um usuário postar um comentário ou um conteúdo, incluindo por exemplo: publicação de nível superior, respostas, revisões, uploads de mural de mídia |
| Postado | Quando uma publicação foi bem-sucedida. |
| Twitter_Reply | Sempre que um usuário responde no Twitter |
| Twitter_Like | Onde o conteúdo foi compartilhado: Retweet |
| Livefyre_Like | Sempre que o recurso curtir do livefyre for usado em um aplicativo |
| Livefyre_Unlike | Sempre que um usuário descurar um arquivo ao vivo como |
| ShareOnPost | Sempre que um usuário publica conteúdo e usa o recurso compartilhar na publicação |
| ShareButtonClick | Sempre que um usuário clicar no botão Compartilhar em um comentário |
| ShareTwitter | Ao clicar em Compartilhar na Twitter |
| ShareFacebook | Ao clicar em Compartilhar na Facebook |
| ShareURL | Quando a área de texto Compartilhar no URL é selecionada/copiada. |
| ExpandirRespostas | Quando um usuário clica no link + ou Expandir para exibir todas as respostas em uma publicação de nível superior |
| RecolherRespostas | Quando um usuário clica no link - ou Recolher para exibir todas as respostas em uma publicação de nível superior |
| FlagClick | Sempre que um usuário abrir o modal Sinalizar |
| FlagSpam | Quando um usuário sinaliza conteúdo como spam |
| FlagDisagree | Quando um usuário sinaliza o conteúdo como discordante |
| SinalizadorOfensivo | Quando um usuário sinaliza o conteúdo como ofensivo |
| FlagOffTopic | Quando um usuário sinaliza o conteúdo como tópico fora |
| FlagCancel | Sempre que um usuário clicar em X ou &quot;cancelar&quot; ao enviar um sinalizador |
| FollowCollection | Sempre que uma conversa é seguida (&quot;Estou interessado&quot; em Revisões) |
| UnfollowCollection | Quando uma conversa não é seguida |
| RequestMore | Sempre que um usuário carregou mais conteúdo em um aplicativo (precisa ser para alta velocidade também) |
| ModalView | Sempre que um usuário clicar para exibir o conteúdo em uma modal |
| TwitterRetweetClick | Onde o conteúdo foi compartilhado: Retweet |
| PostButtonClick | Quando um usuário clica na publicação (&quot;O que você acha?&quot;) botão |
| Logon | Sempre que um usuário fizer logon |
| Logout | Sempre que um usuário desconectou |

Veja a seguir uma lista de variáveis de conversão (eVars) fornecida pelo Livefyre.

## Variáveis de conversão - eVars

| Evento | Descrição |
|--- |--- |
| ID de rede | ID/nome de rede no Livefyre |
| ID do aplicativo | O URN do aplicativo |
| ID de contexto | ID de conteúdo no Livefyre |
| Tipo de aplicativo | Tipo de aplicativo Livefyre. Opções: <br><ul><li>Blog ao vivo  </li><li> Placa de recurso</li><li>Carrossel</li><li>Bate-papo </li><li>Comentários</li><li>Tira</li><li>Mapa</li><li>Mosaico</li><li>Mural de mídia</li><li>Tendência</li><li>Botão Upload</li></ul> |
| Tipo de conteúdo | Instagram, Twitter, Facebook, LiveFile, YouTube etc |

## Mais informações {#section_b3d_4yl_pdb}

Para obter mais informações sobre os tópicos discutidos nesta página, consulte:

* [Gerenciador ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[do conjunto de relatóriosDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Regras](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
