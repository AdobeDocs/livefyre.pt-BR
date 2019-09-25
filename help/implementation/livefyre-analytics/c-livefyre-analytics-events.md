---
description: 'null'
seo-description: 'null'
seo-title: Eventos do Livefyre Analytics
solution: Experience Manager
title: Eventos do Livefyre Analytics
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventos do Livefyre Analytics {#livefyre-analytics-events}

## Definição de objeto de evento {#section_dh1_yhn_pdb}

O código a seguir define os campos no objeto de evento que são recebidos pelo manipulador do Analytics em uma página.

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

Os seguintes eventos do Livefyre para mapear para eventos personalizados a serem usados em relatórios usando o Gerenciador de conjunto de relatórios. Para obter mais informações sobre Report Suites no Adobe Analytics, consulte Gerenciador [](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)de report suite. Para obter mais informações sobre como usar eventos do Livefyre com o Gerenciador de conjunto de relatórios, consulte [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Eventos do Livefyre Analytics

| Evento | Descrição |
|---|---|
| Inicializar | Quando uma página que inclui pelo menos um aplicativo Livefyre é carregada |
| Load | Sempre que um aplicativo for carregado em uma página, independentemente da exibição do usuário |
| Exibir | Quando um aplicativo entrou no visor pela primeira vez. |
| Publicar | Sempre que um usuário postar um comentário ou um conteúdo, incluindo ex: publicação de nível superior, respostas, revisões, uploads de mural de mídia |
| Postado | Quando uma postagem foi bem-sucedida. |
| Twitter_Reply | Sempre que um usuário responde no Twitter |
| Twitter_Like | Onde o conteúdo foi compartilhado: Retweet |
| Livefyre_Like | Sempre que o recurso como livefyre for usado em um aplicativo |
| Livefyre_Unlike | Sempre que um usuário descurtir uma vida como uma |
| ShareOnPost | Sempre que um usuário postar conteúdo e usar o recurso Compartilhar no post |
| ShareButtonClick | Sempre que um usuário clicar no botão Compartilhar em um comentário |
| ShareTwitter | Ao clicar em Compartilhar no Twitter |
| ShareFacebook | Ao clicar em Compartilhar no Facebook |
| ShareURL | Quando a área de texto Compartilhar para URL é selecionada/copiada. |
| ExpandirRespostas | Quando um usuário clica no link + ou Expandir para exibir todas as respostas em uma publicação de nível superior |
| RecolherRespostas | Quando um usuário clica no link - ou Recolher para exibir todas as respostas em uma publicação de nível superior |
| FlagClick | Sempre que um usuário abrir o modo Sinalizar |
| SinalizarSpam | Quando um usuário sinaliza o conteúdo como spam |
| SinalizarDiscordar | Quando um usuário sinaliza o conteúdo como discordante |
| FlagOffensive | Quando um usuário sinaliza o conteúdo como ofensivo |
| FlagOffTopic | Quando um usuário sinaliza o conteúdo como tópico fora |
| SinalizarCancelar | Sempre que um usuário clicar em X ou "cancelar" ao enviar um sinalizador |
| followCollection | Sempre que uma conversa for seguida ("Estou interessado" em Revisões) |
| UnfollowCollection | Quando uma conversa não é seguida |
| RequestMore | Sempre que um usuário carregava mais conteúdo em um aplicativo (também precisa estar em alta velocidade) |
| ModalView | Sempre que um usuário clicar para exibir o conteúdo em um modal |
| TwitterRetweetClick | Onde o conteúdo foi compartilhado: Retweet |
| PostButtonClick | Quando um usuário clica na publicação ("O que você acha?") botão |
| Logon | Sempre que um usuário fizer logon |
| Logout | Sempre que um usuário desconectou |

A seguir está uma lista de variáveis de conversão (eVars) fornecida pelo Livefyre.

## Variáveis de conversão - eVars

| Evento | Descrição |
|--- |--- |
| ID de rede | ID/nome de rede no Livefyre |
| ID do aplicativo | A URN do aplicativo |
| ID de contexto | ID de conteúdo no Livefyre |
| Tipo de aplicativo | Tipo de aplicativo Livefyre. Opções: <br><ul><li>Blog ao vivo  </li><li> Placa de recurso</li><li>Carrossel</li><li>Bate-papo </li><li>Comentários</li><li>Película fotográfica</li><li>Mapa</li><li>Mosaico</li><li>Mídia</li><li>Tendência</li><li>Botão Upload</li></ul> |
| Tipo de conteúdo | Instagram, Twitter, Facebook, LiveFyre, YouTube etc |

## Mais informações {#section_b3d_4yl_pdb}

Para obter mais informações sobre os tópicos discutidos nesta página, consulte:

* [Report Suite](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[ManagerDTM](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Regras](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)