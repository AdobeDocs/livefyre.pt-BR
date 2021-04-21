---
description: Use eventos Javascript para acompanhar eventos que ocorrem em um Mural de mídia e enviá-los para a ferramenta de análise de sua escolha.
title: Eventos Javascript para mural de mídia
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Eventos Javascript para Mural de Mídia{#javascript-events-for-media-wall}

Use eventos Javascript para acompanhar eventos que ocorrem em um Mural de mídia e enviá-los para a ferramenta de análise de sua escolha.

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário nos aplicativos do Livefyre. Por exemplo, você pode querer atualizar a página quando os usuários curtirem ou compartilharem conteúdo com o Twitter ou Facebook, ou quando um novo conteúdo for publicado.

Este é um exemplo de como receber os eventos. Substitua `console.log` por seu código para mapear e enviar o evento para sua integração do Analytics (Dynamic Tag Management, Adobe Analytics JS, Google Analytics, etc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista de eventos do Mural de mídia suportados:

## Eventos do mural de mídia

| Evento | Definição |
|---|---|
| `Init` | Quando um Mural de mídia é incluído em uma página. |
| `Load` | Quando o Mural de mídia foi carregado em uma página, independentemente da posição. |
| `PostButtonClick` | Quando um usuário clica em um botão Upload em um mural de mídia. |
| `RequestMore` | Quando o usuário carrega mais conteúdo em um Mural de mídia. |
| `TwitterReplyClick` | Quando um usuário clica no botão Resposta do Twitter no Mural de mídia. |
| `TwitterRetweetClick` | Quando um usuário clica no botão Retweet do Twitter no Mural de mídia. |
| `TwitterLikeClick` | Quando um usuário clica no botão Curtir/Favorito do Twitter no Mural de mídia. |
| `ModalView` | Quando o usuário clica para exibir o conteúdo do Mural de mídia em uma janela modal maior. |
| `Like` | Quando um usuário clica no botão Curtir no Mural de mídia. |
| `ShareButtonClick` | Sempre que um usuário clicar no botão Compartilhar em um cartão do Mural de mídia. |
| `ShareURL` | Quando a área de texto Compartilhar no URL é selecionada/copiada do Mural de mídia. |
| `ShareFacebook` | Quando Compartilhar na Facebook é clicado no Mural de mídia. |
| `ShareTwitter` | Quando Compartilhar na Twitter é clicado no Mural de mídia. |
