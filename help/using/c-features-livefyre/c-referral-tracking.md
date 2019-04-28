---
description: Rastrear os cliques de volta para a página a partir do tráfego de referência.
seo-description: Rastrear os cliques de volta para a página a partir do tráfego de referência.
seo-title: Rastreamento de referências
solution: Experience Manager
title: Rastreamento de referências
uuid: 7 daf 615 d -0 c 07-49 d 1-adb 2-1 ac 67 ea 563 e 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Rastreamento de referências{#referral-tracking}

Rastrear os cliques de volta para a página a partir do tráfego de referência.

O Livefyre anexa uma variável de referência ao URL quando um comentário é postado ou compartilhado em uma rede social e para permalinks incluídos em emails do Livefyre. Use essa variável para rastrear o tráfego de referência de Aplicativos do Livefyre para suas propriedades sociais ou de propriedade.

Os aplicativos do Livefyre permitem rastrear fluxos de dados resultantes do tráfego de referências, permitindo analisar o tráfego do site.

## Rastreamento de tráfego de referência do Livefyre {#section_nsy_qp4_xz}

O tráfego de referência do Livefyre de redes sociais e emails pode ser rastreado inspecionando os parâmetros da string de consulta nos urls de suas páginas e implementando o código na página para rastrear isso por meio do seu provedor de análise. O Livefyre anexa um link de referência para o URL quando um comentário é postado ou compartilhado em uma rede social e para permalinks incluídos em emails do Livefyre.

## Exemplo de implementação {#section_xvs_x44_xz}

Se o tráfego tiver sido de uma notificação com streamhub, haverá um parâmetro de string de consulta hubrefsrc com um valor de email, facebook, twitter, linkedin ou permalink. O nome do parâmetro hubrefsrc pode ser configurado no nível de rede pela equipe de entrega do Livefyre.

Para integrar com uma plataforma de análise, sua página deve procurar o hubrefsrc na carga e gravar o tráfego se estiver presente.

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
* [Revisões](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Auxiliares](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

