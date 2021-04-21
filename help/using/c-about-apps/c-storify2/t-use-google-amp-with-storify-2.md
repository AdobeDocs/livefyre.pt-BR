---
description: Use as APIs do Livefyre para adicionar a funcionalidade do Google AMP à sua página do Storify 2, a fim de manter o conteúdo interativo e compatível com SEO.
title: Usar o Google AMP com o Storify 2
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Usar o Google AMP com o Storify 2{#use-google-amp-with-storify}

Use as APIs do Livefyre para adicionar a funcionalidade do Google AMP à sua página do Storify 2, a fim de manter o conteúdo interativo e compatível com SEO.

Para usar o Google AMP com o Storify 2, você deve criar uma página para seu aplicativo do Storify 2 com marcação do Google AMP.

A versão AMP das solicitações do aplicativo é atualizada a partir da página original (use o parâmetro **pollInterval** na API **amp-live-list** para definir o intervalo para solicitações de atualização). Para garantir que os visitantes da sua página de AMP obtenham o conteúdo mais atualizado rapidamente, mantenha um TTL de baixo cache nas páginas de AMP do Storify 2.

Os ativos que não são de imagem (por exemplo, vídeos) incluídos como publicações em um aplicativo Storify 2 devem usar HTTPS, conforme especificado pela especificação da AMP. Os URLs AMP que usam a Rede de entrega de conteúdo (CDN) do Google Cloud usam HTTPS.

Para usar o Google AMP com o Storify 2:

1. Crie um modelo validado pela AMP no site.
1. Use uma ou mais das seguintes APIs do Google AMP para personalizar a página do Google AMP:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframe para personalizar a exibição do Storify 2
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list para personalizar o intervalo de tempo de atualizações
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) shareter para adicionar um botão de compartilhamento social
1. Inclua o conteúdo da seguinte página AMP do Storify 2 no CSS da página do Storify 2 na tag `<style amp-custom>` : [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Inclua o conteúdo da seguinte API de marcação AMP do Storify 2 no modelo do Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` onde {{APP_ID}} é a ID do aplicativo para o aplicativo Storify 2 no Livefyre Studio.
   1. O único parâmetro de consulta é **pollInterval**, que é o intervalo no qual o aplicativo verificará se há atualizações (definidas em milissegundos).
   1. O URL inclui conteúdo das publicações mais recentes (incluindo Tweets, vídeos, etc.)
   1. A página do editor precisa obter conteúdo desse URL com a frequência com que você deseja que a página do Google AMP seja atualizada.
