---
description: Integre um aplicativo de Observações seguindo um processo semelhante aos Aplicativos principais.
title: Integração de observações
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Integração do Sidenotes{#sidenotes-integration}

Integre um aplicativo de Observações seguindo um processo semelhante aos Aplicativos principais.

Como regra geral, se a integração do Aplicativo principal estiver concluída, o código gravado para gerar o objeto `collectionMeta` poderá ser reutilizado para observações.

Você também pode reutilizar seus delegados `auth` existentes fornecendo um delegado `auth` criado com `fyre.conv` para Observações no campo (opcional) `authDelegate`.

>[!NOTE]
>
>As observações permitem incluir `network`, `siteId` e `articleId` em um único objeto, em vez de passá-las separadamente em outras partes do construtor.

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

Conforme observado na seção Criação `collectionMeta` , `collectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT.

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

As observações foram otimizadas para uso em dispositivos móveis. Para obter melhores resultados com as versões móveis do seu aplicativo Livefyre, defina a opção escalável pelo usuário como não. Por exemplo:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
