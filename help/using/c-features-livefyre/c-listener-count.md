---
description: A contagem de ouvintes é um contador que acompanha o número de visitantes do site para um aplicativo em uma página e exibe esse número.
seo-description: A contagem de ouvintes é um contador que acompanha o número de visitantes do site para um aplicativo em uma página e exibe esse número.
seo-title: Contagem de Listener
solution: Experience Manager
title: Contagem de Listener
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Contagem de Listener{#listener-count}

A contagem de ouvintes é um contador que acompanha o número de visitantes do site para um aplicativo em uma página e exibe esse número.

Contagem de ouvintes é o número de visitantes do site que têm um navegador aberto na página em que um aplicativo é instanciado. Isso permite que você saiba quantos visitantes do site estão na página a qualquer momento, para que você possa acompanhá-los enquanto eles assistem streaming ou conteúdo ao vivo em tempo real.

A contagem de Listener de Livefyre funciona assim:

1. O site que contém seu aplicativo faz ping em um servidor Livefyre a cada 60 segundos.
1. O servidor Livefyre responde com o número de visitantes do site na página que exibe o aplicativo (definido como o número de visitantes do site com um navegador aberto para essa página).
1. O número de visitantes do site na página com o aplicativo é exibido no aplicativo.

Aplicativos que usam este recurso:

* [Bate-papo](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Avatares do Listener {#section_wcn_kxp_vz}

A contagem de ouvintes exibe no máximo 10 avatares e exibe avatares somente para as pessoas que clicaram **[!UICONTROL Follow]** na conversa.

>[!NOTE]
>
>Devido a restrições de espaço, a interface móvel exibe apenas o número de ouvintes e um pequeno ícone "pessoas".

A Contagem de ouvintes do Livefyre exibe o número de pessoas ativamente na página em um determinado momento, além do número de pessoas que seguem a conversa. Se alguém estiver na página e seguindo a conversa, esse usuário não será contado duas vezes. Por exemplo, se um usuário estiver em uma página e clicar **[!UICONTROL Follow]**, a contagem de ouvintes não aumentará; se esse usuário clicar **[!UICONTROL Unfollow]**, a contagem não diminuirá.

Aplicativos que usam este recurso:

* [Bate-papo](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

