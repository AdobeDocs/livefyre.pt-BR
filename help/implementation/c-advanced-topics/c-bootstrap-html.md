---
description: Disponibilizar o conteúdo da comunidade para rastreadores de mecanismo de pesquisa.
title: HTML do Bootstrap
exl-id: 22ab4f2d-f433-4805-b0dd-16d4531e425d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# HTML do Bootstrap

Disponibilizar o conteúdo da comunidade para rastreadores de mecanismo de pesquisa.

Para obter uma lista completa de endpoints disponíveis, consulte a seção Livefyre [API Reference](https://api.livefyre.com/docs) .

Os aplicativos Livefyre exigem a execução do JavaScript na página para exibir o conteúdo das suas coleções. Como a maioria dos rastreadores de mecanismo de pesquisa não pode executar o JavaScript, eles não podem ver o conteúdo que sua comunidade publica. Use a API HTML do Bootstrap para adicionar fragmentos pesquisáveis desse conteúdo à resposta HTTP inicial da sua página, permitindo que seu conteúdo e palavras-chave melhorem a otimização do mecanismo de pesquisa.

>[!NOTE]
>
>Essa API está disponível somente para os tipos Comentários e Coleção de Blog ao Vivo.

## Integração

A API HTML do Bootstrap do Livefyre retornará um fragmento HTML do conteúdo do usuário, que pode ser incluído na resposta HTTP da página. Essa resposta poderá ser lida por rastreadores de mecanismo de pesquisa sem executar nenhum JavaScript. Quando a página estiver ativa no navegador do usuário, o fragmento HTML será substituído pelo widget completo e interativo e o usuário poderá publicar o conteúdo.

Para implementar a API HTML do Bootstrap:

1. Faça uma solicitação de API de servidor para servidor para o endpoint HTML do Bootstrap documentado abaixo.

   >[!NOTE]
   >
   >Se você estiver tentando capturar o HTML do Bootstrap para uma conversa que ainda não existe (ou seja, se ainda precisar incorporar o aplicativo ou criar a coleção), você receberá um 200, mas com conteúdo que se parece com: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se o retorno não incluir conteúdo com um &quot;404&quot;, salve-o em uma string. Você pode armazenar essa resposta em cache para uso posterior a fim de evitar solicitar a API HTML do Bootstrap em cada carregamento de página.
1. Insira a sequência de caracteres HTML do Bootstrap na página da Web, onde deseja que o conteúdo seja exibido.
1. Aplique sua página da Web ao navegador (ou crawler do mecanismo de pesquisa).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parâmetros

* **** networkNameSeu Livefyre forneceu o nome da rede. Por exemplo: *labs* em `labs.fyre.co`.
* **** siteIdA ID do site da coleção.
* **b64** articleIdA ID do artigo da Coleção usando a codificação base64url.

## Exemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Resposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
