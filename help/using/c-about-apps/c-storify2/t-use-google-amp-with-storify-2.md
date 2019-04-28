---
description: Use apis do Livefyre para adicionar a funcionalidade do Google AMP à página do Storify 2 para manter o conteúdo interativo e compatível com a SEO.
seo-description: Use apis do Livefyre para adicionar a funcionalidade do Google AMP à página do Storify 2 para manter o conteúdo interativo e compatível com a SEO.
seo-title: Usar o Google AMP com o Storify 2
solution: Experience Manager
title: Usar o Google AMP com o Storify 2
uuid: 40 c 9 f 083-7284-43 ba-ae 27-53 b 1 ff 9 e 3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Usar o Google AMP com o Storify 2{#use-google-amp-with-storify}

Use apis do Livefyre para adicionar a funcionalidade do Google AMP à página do Storify 2 para manter o conteúdo interativo e compatível com a SEO.

Para usar o Google AMP com o Storify 2, você deve criar uma página para seu aplicativo Storify 2 com marcação do Google AMP.

A versão AMP do aplicativo solicita atualizações da página original (use o parâmetro **pollinterval** na API **de lista amp-live** para definir o intervalo para solicitações de atualização). Para garantir que os visitantes na sua página AMP tenham o conteúdo mais atualizado rapidamente, mantenha um TTL baixo em suas páginas do Storify 2 AMP.

Os ativos não de imagem (por exemplo, vídeos) incluídos como publicações em um aplicativo Storify 2 devem usar HTTPS como especificado pela especificação AMP. Os urls AMP que usam o Google Cloud Content Delivery Network (CDN) usam HTTPS.

Para usar o Google AMP com o Storify 2:

1. Crie um modelo validado pela AMP em seu site.
1. Use uma ou mais das seguintes apis do Google AMP para personalizar sua página do Google AMP:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) para personalizar a exibição do Storify 2
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) para personalizar o intervalo de tempo das atualizações
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) para adicionar um botão de compartilhamento em redes sociais
1. Inclua o conteúdo da seguinte página do Storify 2 AMP no CSS para a página do Storify 2 na <style amp-custom> tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Inclua o conteúdo da seguinte API de marcação do Storify 2 AMP em seu modelo do Google AMP: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` em que {{APP_ ID}} é a ID do aplicativo para o aplicativo Storify 2 no Livefyre Studio.
   1. O único parâmetro de consulta é **o pollinterval**, que é o intervalo no qual o aplicativo verifica atualizações (definido em milissegundos).
   1. O URL inclui conteúdo das postagens mais recentes (incluindo Tweets, vídeos etc.)
   1. A página do editor precisa obter o conteúdo dessa URL com o que você desejar que a página do Google AMP seja atualizada.
