---
description: Use as APIs do Livefyre para adicionar a funcionalidade do Google AMP à sua página do Storify 2 para manter o conteúdo interativo e compatível com SEO.
seo-description: Use as APIs do Livefyre para adicionar a funcionalidade do Google AMP à sua página do Storify 2 para manter o conteúdo interativo e compatível com SEO.
seo-title: Usar o Google AMP com o Storify 2
solution: Experience Manager
title: Usar o Google AMP com o Storify 2
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Usar o Google AMP com o Storify 2{#use-google-amp-with-storify}

Use as APIs do Livefyre para adicionar a funcionalidade do Google AMP à sua página do Storify 2 para manter o conteúdo interativo e compatível com SEO.

Para usar o Google AMP com o Storify 2, você deve criar uma página para seu aplicativo do Storify 2 com marcação do Google AMP.

A versão AMP das solicitações do aplicativo é atualizada da página original (use o parâmetro **pollInterval** na API **amp-live-list** para definir o intervalo das solicitações de atualização). Para garantir que os visitantes em sua página AMP obtenham o conteúdo mais atualizado rapidamente, mantenha um TTL de baixo cache nas páginas AMP do Storify 2.

Os ativos que não são de imagem (por exemplo, vídeos) incluídos como postagens em um aplicativo Storify 2 devem usar HTTPS conforme especificado na especificação AMP. Os URLs AMP que usam a Rede de entrega de conteúdo (CDN) do Google Cloud usam HTTPS.

Para usar o Google AMP com o Storify 2:

1. Crie um modelo validado pela AMP em seu site.
1. Use uma ou mais das seguintes APIs do Google AMP para personalizar sua página do Google AMP:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) para personalizar a exibição do Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) para personalizar o intervalo de tempo para atualizações
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) para adicionar um botão de compartilhamento em redes sociais
1. Inclua o conteúdo da seguinte página AMP do Storify 2 no CSS para a sua página do Storify 2 no <style amp-custom> tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Inclua o conteúdo da seguinte API de marcação AMP do Storify 2 no modelo do Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` onde {{APP_ID}} é a ID do aplicativo para o aplicativo Storify 2 no Livefyre Studio.
   1. O único parâmetro de consulta é **pollInterval**, que é o intervalo no qual o aplicativo verificará se há atualizações (definidas em milissegundos).
   1. O URL inclui conteúdo das postagens mais recentes (incluindo Tweets, vídeos etc.)
   1. A página do editor precisa obter conteúdo desse URL com a frequência desejada para que a página do Google AMP seja atualizada.
