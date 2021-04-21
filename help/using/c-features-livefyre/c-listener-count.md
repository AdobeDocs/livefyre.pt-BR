---
description: A contagem do ouvinte é um contador que acompanha o número de visitantes do site de um aplicativo em uma página e exibe esse número.
title: Contagem de Listener
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Contagem de Listener{#listener-count}

A contagem do ouvinte é um contador que acompanha o número de visitantes do site de um aplicativo em uma página e exibe esse número.

Contagem do ouvinte é o número de visitantes do site que têm um navegador aberto na página em que um aplicativo é instanciado. Isso permite que você saiba quantos visitantes do site estão na página a qualquer momento, para que você possa acompanhá-los enquanto assistem a streaming ou conteúdo ao vivo em tempo real.

A contagem do Ouvinte da Livefyre funciona assim:

1. O site que contém seu aplicativo consulta um servidor Livefyre a cada 60 segundos.
1. O servidor Livefyre responde com o número de visitantes do site na página que exibe o aplicativo (definido como o número de visitantes do site com um navegador aberto para essa página).
1. O número de visitantes do site na página com o aplicativo é exibido no aplicativo.

Aplicativos que usam este recurso:

* [Bate-papo](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatares do Listener {#section_wcn_kxp_vz}

A contagem de ouvintes exibe um máximo de 10 avatares e exibe avatares somente para as pessoas que clicaram **[!UICONTROL Follow]** para a conversa.

>[!NOTE]
>
>Devido a restrições de espaço, a interface móvel exibe apenas o número de ouvintes e um pequeno ícone &quot;pessoas&quot;.

A Contagem de Ouvinte do Livefyre exibe o número de pessoas ativamente na página em um determinado momento, mais o número de pessoas após a conversa. Se alguém estiver na página e após a conversa, esse usuário não será contado duas vezes. Por exemplo, se um usuário estiver em uma página e clicar em **[!UICONTROL Follow]**, a contagem do ouvinte não aumentará; se esse usuário clicar em **[!UICONTROL Unfollow]**, a contagem não diminuirá.

Aplicativos que usam este recurso:

* [Bate-papo](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
