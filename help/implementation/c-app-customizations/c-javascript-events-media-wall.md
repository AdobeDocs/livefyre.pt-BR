---
description: Use eventos Javascript para acompanhar eventos que ocorrem em um mural
  de mídia e enviá-los para a ferramenta de análise de sua escolha.
seo-description: Use eventos Javascript para acompanhar eventos que ocorrem em um
  mural de mídia e enviá-los para a ferramenta de análise de sua escolha.
seo-title: Eventos Javascript para o Media Wall
solution: Experience Manager
title: Eventos Javascript para o Media Wall
uuid: 8 afc 0529-4640-476 a-b 207-91 b 2 c 70101 f 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eventos Javascript para o Media Wall{#javascript-events-for-media-wall}

Use eventos Javascript para acompanhar eventos que ocorrem em um mural de mídia e enviá-los para a ferramenta de análise de sua escolha.

O Livefyre fornece eventos javascript para rastrear a atividade do usuário em seus Aplicativos do Livefyre. Por exemplo, você pode querer atualizar a página quando os usuários curtirem ou compartilhar conteúdo no Twitter ou Facebook, ou quando novo conteúdo é publicado.

Este é um exemplo de como receber os eventos. Substitua `console.log` por seu código para mapear e enviar o evento à integração do Analytics (Gerenciamento dinâmico de tags, JS do Adobe Analytics, Google Analytics etc.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista de eventos de Dynamic Wall suportados:

## Eventos de mural de mídia

| Evento | Definição |
|---|---|
| `Init` | Quando um mural de mídia é incluído em uma página. |
| `Load` | Quando o Media Wall foi carregado em uma página independentemente da posição. |
| `PostButtonClick` | Quando um usuário clica em um botão Carregar em um mural de mídia. |
| `RequestMore` | Quando o usuário carrega mais conteúdo em um Media Wall. |
| `TwitterReplyClick` | Quando um usuário clica no botão Responder do Twitter a partir do Media Wall. |
| `TwitterRetweetClick` | Quando um usuário clica no botão Retweet do Twitter a partir do Media Wall. |
| `TwitterLikeClick` | Quando um usuário clica no botão Curtir/Favorito do Twitter a partir do Media Wall. |
| `ModalView` | Quando o usuário clica em para exibir o conteúdo do Media Wall em uma janela modal maior. |
| `Like` | Quando um usuário clica no botão Curtir do Mural de mídia. |
| `ShareButtonClick` | Sempre que um usuário clica no botão Compartilhar em um cartão de Wall Wall. |
| `ShareURL` | Quando a área de texto Compartilhar com URL é selecionada/copiada do mural de mídia. |
| `ShareFacebook` | Quando Compartilhar no Facebook é clicado no Media Wall. |
| `ShareTwitter` | Quando Compartilhar no Twitter é clicado no Media Wall. |
