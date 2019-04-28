---
description: 'null'
seo-description: 'null'
seo-title: Eventos do Livefyre Analytics
solution: Experience Manager
title: Eventos do Livefyre Analytics
uuid: 4 eb 5 a 196-ca 33-40 f 8-a 96 d-ed 46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventos do Livefyre Analytics {#livefyre-analytics-events}

## Definição do objeto de evento {#section_dh1_yhn_pdb}

O código a seguir define os campos no objeto de evento que são recebidos pelo manipulador de análises em uma página.

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

## Eventos e evars do Livefyre Analytics {#section_u3k_tft_mcb}

Os seguintes eventos do Livefyre são mapeados para eventos personalizados a serem usados em relatórios usando o Gerenciador de conjunto de relatórios. Para obter mais informações sobre Conjuntos de relatórios no Adobe Analytics, consulte [Gerenciador](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)de conjunto de relatórios. Para saber mais sobre como usar eventos do Livefyre com o Gerenciador de report suite, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos do Livefyre Analytics

| Evento | Descrição |
|---|---|
| Init | Quando uma página que inclui pelo menos um aplicativo Livefyre é carregada |
| Carregar | Sempre que um aplicativo foi carregado em uma página independentemente da exibição do usuário |
| Exibir | Quando um aplicativo entrou no visor pela primeira vez. |
| Postagem | Sempre que um usuário posta um comentário ou um pedaço de conteúdo, incluindo ex: postagem de nível superior, respostas, revisões, uploads de mural de mídia |
| Postado | Quando uma publicação é bem-sucedida. |
| Twitter_ Response | Sempre que um usuário respondeu no Twitter |
| Twitter_ Like | Onde o conteúdo foi compartilhado para: Retweet |
| Livefyre_ Like | Sempre que o recurso de livefyre como o recurso é usado em um aplicativo |
| Livefyre_ Unlike | Quando um usuário desgosta de um livefyre, |
| Shareonpost | Sempre que um usuário posta o conteúdo e usa o compartilhamento no recurso de publicação |
| Sharebuttonclick | Sempre que um usuário clica no botão Compartilhar em um comentário |
| Sharetwitter | Quando Compartilhar no Twitter é clicado |
| Sharefacebook | Quando Compartilhar no Facebook é clicado |
| Shareurl | Quando a área de texto Compartilhar com URL é selecionada/copiada. |
| Expandreplies | Quando um usuário clica no link + ou Expandir para exibir todas as respostas em uma postagem de nível superior |
| Collapsereplies | Quando um usuário clica no link - ou Contrair para exibir todas as respostas em uma postagem de nível superior |
| Flagclick | Sempre que um usuário abrir o Sinalizador modal |
| Flagspam | Quando um usuário sinaliza o conteúdo como spam |
| Flagdiscordisagree | Quando um usuário sinaliza o conteúdo como discordar |
| Flagofensiva | Quando um usuário sinaliza o conteúdo como ofensivo |
| Flagofftopic | Quando um usuário sinaliza o conteúdo como fora do tópico |
| Flagcancel | Quando um usuário clica em X ou &quot;cancelar&quot; ao enviar um sinalizador |
| Followcollection | Sempre que uma conversa for seguida (&quot;Estou interessado&quot; em Revisões) |
| Unfollowcollection | Quando uma conversa não é seguida |
| Requestmore | Sempre que um usuário carregou mais conteúdo em um aplicativo (precisa ser para velocidade alta também) |
| Modalview | Sempre que um usuário clica em para exibir o conteúdo em um modal |
| Twitterretweetclick | Onde o conteúdo foi compartilhado para: Retweet |
| Postbuttonclick | Quando um usuário clica na publicação (&quot;Whats em sua mente?&quot;&quot;) botão |
| Logon | Sempre que um usuário conectou-se |
| Logout | Sempre que um usuário desconectou |

A seguir está uma lista de variáveis de conversão (evars) fornecidas pelo Livefyre.

## Variáveis de conversão - evars

| Evento | Descrição |
|--- |--- |
| ID da rede | ID de rede/nome no Livefyre |
| ID do aplicativo | O URN do aplicativo |
| ID de contexto | ID de conteúdo no Livefyre |
| Tipo de aplicativo | Tipo de aplicativo Livefyre. Opções: <br><ul><li>Blog ao vivo  </li><li> Cartão de recursos</li><li>Carrossel</li><li>Bate-papo </li><li>Comentários</li><li>Película fotográfica</li><li>Mapa</li><li>Mosaico</li><li>Media Wall</li><li>Tendência</li><li>Botão Upload</li></ul> |
| Tipo de conteúdo | Instagram, Twitter, Facebook, livefyre, youtube etc. |

## Mais informações {#section_b3d_4yl_pdb}

Para obter mais informações sobre os tópicos discutidos nesta página, consulte:

* [Report Suite managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Regras](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)