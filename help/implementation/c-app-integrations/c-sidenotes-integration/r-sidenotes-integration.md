---
description: Integre um aplicativo de Sidenotes seguindo um processo semelhante a
  Aplicativos principais.
seo-description: Integre um aplicativo de Sidenotes seguindo um processo semelhante
  a Aplicativos principais.
seo-title: Integração de sidenotes
solution: Experience Manager
title: Integração de sidenotes
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Integração de sidenotes{#sidenotes-integration}

Integre um aplicativo de Sidenotes seguindo um processo semelhante a Aplicativos principais.

Como regra geral, se a integração do aplicativo principal estiver concluída, o código escrito para gerar o `collectionMeta` objeto poderá ser reutilizado para auxiliar.

Você também pode reutilizar `auth` seus representantes existentes fornecendo um `auth` delegado criado `fyre.conv` com a opção Auxiliar no `authDelegate` campo (opcional).

>[!NOTE]
>
>Os auxiliares permitem que você inclua `network`, `siteId`e `articleId` em um único objeto, em vez de passá-los separadamente em outras partes do construtor.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Conforme observado na `collectionMeta` seção Construção, `collectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON pega o seguinte formato antes de ser codificado em JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Para obter mais informações, consulte o `collectionMeta` token.

## Configuração móvel

As sidenotes foram otimizadas para uso em dispositivos móveis. Para obter melhores resultados com versões móveis de seu aplicativo Livefyre, defina a opção dimensionável do usuário para não. Por exemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
