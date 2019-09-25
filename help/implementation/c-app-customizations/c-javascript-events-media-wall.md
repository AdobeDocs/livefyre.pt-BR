---
description: Use eventos Javascript para acompanhar eventos que ocorrem em um Mídia e enviá-los para a ferramenta de análise de sua escolha.
seo-description: Use eventos Javascript para acompanhar eventos que ocorrem em um Mídia e enviá-los para a ferramenta de análise de sua escolha.
seo-title: Eventos Javascript para mural de mídia
solution: Experience Manager
title: Eventos Javascript para mural de mídia
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Eventos Javascript para mural de mídia{#javascript-events-for-media-wall}

Use eventos Javascript para acompanhar eventos que ocorrem em um Mídia e enviá-los para a ferramenta de análise de sua escolha.

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário nos aplicativos Livefyre. Por exemplo, você pode desejar atualizar a página quando os usuários curtirem ou compartilharem conteúdo no Twitter ou Facebook, ou quando novo conteúdo for publicado.

Este é um exemplo de como receber os eventos. Substitua `console.log` pelo código para mapear e enviar o evento para a integração do Analytics (Gerenciamento dinâmico de tags, JS do Adobe Analytics, Google Analytics etc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista de eventos suportados do Media Wall:

## Eventos de mural de mídia

| Evento | Definição |
|---|---|
| `Init` | Quando um mural de mídia é incluído em uma página. |
| `Load` | Quando o Media Wall era carregado em uma página independentemente da posição. |
| `PostButtonClick` | Quando um usuário clica em um botão Carregar em um mural de mídia. |
| `RequestMore` | Quando o usuário carrega mais conteúdo em um mural de mídia. |
| `TwitterReplyClick` | Quando um usuário clica no botão Resposta do Twitter no Media Wall. |
| `TwitterRetweetClick` | Quando um usuário clica no botão Retweet do Twitter no Media Wall. |
| `TwitterLikeClick` | Quando um usuário clica no botão Curtir/Favorito do Twitter no Media Wall. |
| `ModalView` | Quando o usuário clica para exibir o conteúdo do Media Wall em uma janela modal maior. |
| `Like` | Quando um usuário clica no botão Curtir no Media Wall. |
| `ShareButtonClick` | Sempre que um usuário clicar no botão Compartilhar em um cartão do Media Wall. |
| `ShareURL` | Quando a área de texto Compartilhar para URL é selecionada/copiada do Mídia. |
| `ShareFacebook` | Quando o botão Compartilhar no Facebook é clicado no Media Wall. |
| `ShareTwitter` | Quando a opção Compartilhar no Twitter é clicada no Media Wall. |
