---
description: Disponibilizar o conteúdo da comunidade para rastreadores de mecanismo
  de pesquisa.
seo-description: Disponibilizar o conteúdo da comunidade para rastreadores de mecanismo
  de pesquisa.
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137 e 4382-4 e 7 b -4124-9 d 35-1 d 872 a 497 bc 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap HTML

Disponibilizar o conteúdo da comunidade para rastreadores de mecanismo de pesquisa.

Para obter uma lista completa de endpoints disponíveis, consulte a seção Referência [da API](https://api.livefyre.com/docs) do Livefyre.

Os aplicativos do Livefyre exigem que você execute o javascript na sua página para exibir conteúdo de suas Coleções. Como a maioria dos rastreadores do mecanismo de pesquisa não consegue executar o javascript, eles não conseguem visualizar o conteúdo que suas publicações da comunidade. Use a API de bootstrap HTML para adicionar fragmentos pesquisáveis desse conteúdo à resposta HTTP inicial da sua página, permitindo que seu conteúdo e palavras-chave melhorem a otimização do mecanismo de pesquisa.

>[!NOTE]
>
>Esta API está disponível apenas para os tipos de Comentários e Coleção de blog live.

## Integração

A API HTML de Bootstrap do Livefyre retornará um fragmento HTML do conteúdo do usuário, que pode ser incluído na resposta HTTP da página. Essa resposta será legível pelos rastreadores do mecanismo de pesquisa sem executar qualquer javascript. Quando a página estiver ativa no navegador de um usuário, o fragmento HTML será substituído pelo widget completo e interativo, e o usuário será capaz de publicar conteúdo.

Para implementar a API de HTML de bootstrap:

1. Faça um servidor para a solicitação API do servidor para o ponto de extremidade Bootstrap HTML documentado abaixo.

   >[!NOTE]
   >
   >Se você estiver tentando pegar o HTML Bootstrap para uma conversa que ainda não existe (ou seja, se ainda não incorporar o aplicativo ou criar a coleção), você receberá um 200, mas com conteúdo semelhante a: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se o retorno não incluir conteúdo com «404» nele, salve-o em uma sequência de caracteres. Você pode colocar essa resposta em cache para uso posterior para evitar solicitar a API de bootstrap HTML em cada pageload.
1. Insira a sequência de caracteres de bootstrap HTML na página da Web onde você gostaria que o conteúdo fosse exibido.
1. Forneça sua página da Web para o navegador (ou rastreador do mecanismo de pesquisa).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parâmetros

* **Networkname** Seu Livefyre forneceu nome da rede. Por exemplo: ** em `labs.fyre.co`.
* **Siteid** A ID do site da coleção.
* **b 64 articleid** A ID do artigo da coleção usando a codificação base 64 url.

## Exemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Resposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
