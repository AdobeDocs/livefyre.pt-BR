---
description: Rastreie os cliques de volta à sua página do tráfego de referência.
seo-description: Rastreie os cliques de volta à sua página do tráfego de referência.
seo-title: Rastreamento de referência
solution: Experience Manager
title: Rastreamento de referência
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Rastreamento de referência{#referral-tracking}

Rastreie os cliques de volta à sua página do tráfego de referência.

Livefyre anexa uma variável de referência ao URL quando um comentário é publicado ou compartilhado em uma rede social e para permalinks incluídos nos emails do Livefyre. Use essa variável para rastrear o tráfego de referência dos aplicativos Livefyre para suas propriedades sociais ou de propriedade.

Os aplicativos Livefyre permitem rastrear fluxos de dados resultantes do tráfego de referência, permitindo que você analise o tráfego do site.

## Rastrear o tráfego de referência do Livefyre {#section_nsy_qp4_xz}

O tráfego de referência do Livefyre de redes sociais e e-mails pode ser rastreado inspecionando os parâmetros da sequência de caracteres do query nos URLs de suas páginas e implementando o código na sua página para rastrear isso por meio do seu provedor de análises. Livefyre anexa um link de referência ao URL quando um comentário é publicado ou compartilhado em uma rede social e para permalinks incluídos nos emails do Livefyre.

## Exemplo de implementação {#section_xvs_x44_xz}

Se o tráfego for de uma notificação fornecida pelo StreamHub, haverá um parâmetro de string de query hubRefSrc com um valor de email, facebook, Twitter, link ou permalink. O nome do parâmetro hubRefSrc pode ser configurado no nível da rede pela equipe do delivery Livefyre.

Para se integrar a uma plataforma de análise, sua página deve procurar o hubRefSrc na carga e registrar o tráfego se ele estiver presente.

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
* [Sidenotes](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

