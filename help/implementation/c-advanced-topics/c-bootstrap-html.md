---
description: Disponibilize o conteúdo da comunidade para rastreadores de mecanismos de pesquisa.
seo-description: Disponibilize o conteúdo da comunidade para rastreadores de mecanismos de pesquisa.
seo-title: HTML de inicialização
solution: Experience Manager
title: HTML de inicialização
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# HTML de inicialização

Disponibilize o conteúdo da comunidade para rastreadores de mecanismos de pesquisa.

Para obter uma lista completa dos pontos de extremidade disponíveis, consulte a seção Referência [da](https://api.livefyre.com/docs) API Livefyre.

Os aplicativos Livefyre exigem que você execute o JavaScript na sua página para exibir o conteúdo de suas coleções. Como a maioria dos rastreadores de mecanismo de pesquisa não consegue executar o JavaScript, eles não conseguem ver o conteúdo publicado na sua comunidade. Use a API HTML do Bootstrap para adicionar fragmentos pesquisáveis desse conteúdo à resposta HTTP inicial da sua página, permitindo que o conteúdo e as palavras-chave melhorem a otimização do mecanismo de pesquisa.

>[!NOTE]
>
>Esta API está disponível somente para os tipos Comentários e Coleção de Blogs em tempo real.

## Integração

A API HTML Bootstrap do Livefyre retornará um fragmento HTML do conteúdo do usuário, que pode ser incluído na resposta HTTP da página. Essa resposta poderá ser lida por rastreadores de mecanismo de pesquisa sem executar qualquer JavaScript. Quando a página estiver ativa no navegador do usuário, o fragmento HTML será substituído pelo widget completo e interativo e o usuário poderá publicar o conteúdo.

Para implementar a API HTML do Bootstrap:

1. Faça uma solicitação de API do servidor para o ponto de extremidade HTML do Bootstrap documentado abaixo.

   >[!NOTE]
   >
   >Se você estiver tentando capturar o HTML do Bootstrap para uma conversa que ainda não existe (ou seja, se ainda não tiver incorporado o aplicativo ou criado a coleção), você receberá um 200, mas com conteúdo que se parece com: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Se o seu retorno não incluir conteúdo com "404" nele, salve-o em uma string. Você pode colocar essa resposta em cache para uso posterior para evitar solicitar a API HTML do Bootstrap em cada pagelload.
1. Insira a sequência de caracteres HTML do Bootstrap na sua página da Web onde deseja que o conteúdo seja exibido.
1. Servir sua página da Web para o navegador (ou o rastreador do mecanismo de pesquisa).

## Recurso

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parâmetros

* **networkName** Seu Livefyre forneceu o nome da rede. Por exemplo: *laboratórios* em `labs.fyre.co`.
* **siteId** A ID do site da coleção.
* **b64articleId** A ID do artigo da coleção usando a codificação base64url.

## Exemplo

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Resposta

```
https://gist.github.com/ec5c2457322faf9cf515 
```
