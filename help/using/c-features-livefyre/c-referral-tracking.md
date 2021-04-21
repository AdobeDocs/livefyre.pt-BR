---
description: Rastreie cliques de volta para sua página a partir do tráfego de referência.
title: Rastreamento de referência
exl-id: 44cc221c-1603-4e6e-ae4a-1b993f7dc446
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---

# Rastreamento de referência{#referral-tracking}

Rastreie cliques de volta para sua página a partir do tráfego de referência.

O Livefyre anexa uma variável de referência ao URL quando um comentário é publicado ou compartilhado em uma rede social, e para permalinks incluídos nos emails do Livefyre. Use essa variável para rastrear o tráfego de referência dos aplicativos Livefyre para suas propriedades sociais ou de propriedade.

Os aplicativos Livefyre permitem rastrear fluxos de dados resultantes do tráfego de referência, permitindo analisar o tráfego do site.

## Rastreamento do tráfego de referência do Livefyre {#section_nsy_qp4_xz}

O tráfego de referência do Livefyre nas redes sociais e emails pode ser rastreado ao inspecionar os parâmetros da string de consulta nos URLs das suas páginas e implementar o código na página para rastrear isso por meio do provedor de análises. Livefyre anexa um link de referência ao URL quando um comentário é publicado ou compartilhado em uma rede social, e para permalinks incluídos em emails do Livefyre.

## Exemplo de implementação {#section_xvs_x44_xz}

Se o tráfego foi de uma notificação fornecida pelo StreamHub, haverá um parâmetro de sequência de consulta hubRefSrc com um valor de email, facebook, twitter, linkedin ou permalink. O nome do parâmetro hubRefSrc pode ser configurado no nível da rede pela equipe de delivery Livefyre.

Para integrar com uma plataforma de análise, sua página deve procurar o hubRefSrc durante o carregamento e registrar o tráfego se ele estiver presente.

Por exemplo:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```



Aplicativos que usam este recurso:

* [Bate-papo](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Observações](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
