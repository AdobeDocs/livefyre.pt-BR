---
description: Integre um aplicativo Sidenotes seguindo um processo semelhante aos aplicativos principais.
seo-description: Integre um aplicativo Sidenotes seguindo um processo semelhante aos aplicativos principais.
seo-title: Integração com Sidenotes
solution: Experience Manager
title: Integração com Sidenotes
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---


# Integração Sidenotes{#sidenotes-integration}

Integre um aplicativo Sidenotes seguindo um processo semelhante aos aplicativos principais.

Como regra geral, se a integração do Aplicativo principal estiver concluída, o código gravado para gerar o objeto `collectionMeta` poderá ser reutilizado para Sidenotes.

Você também pode reutilizar seus representantes `auth` existentes fornecendo um representante `auth` criado com `fyre.conv` para Sidenotes no campo (opcional) `authDelegate`.

>[!NOTE]
>
>As notas de identificação permitem que você inclua `network`, `siteId` e `articleId` em um único objeto, em vez de passá-los separadamente em outras partes do construtor.

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

Conforme observado na seção Criação `collectionMeta`, `collectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Para obter mais informações, consulte o token `collectionMeta`.

## Configuração móvel

As notas de identificação foram otimizadas para uso em dispositivos móveis. Para obter melhores resultados com as versões móveis do aplicativo Livefyre, defina a opção dimensionável pelo usuário como não. Por exemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
