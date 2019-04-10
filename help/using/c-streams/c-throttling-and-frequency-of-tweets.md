---
description: Nem todo tweet que corresponde a uma regra aparece em um fluxo.
seo-description: Nem todo tweet que corresponde a uma regra aparece em um fluxo.
seo-title: Limitação e frequência de tweets
solution: Experience Manager
title: Limitação e frequência de tweets
uuid: b 9 edfb 1 e-e 6 cf -4 a 48-8756-05 f 5 f 18 d 8799
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Limitação e frequência de tweets{#throttling-and-frequency-of-tweets}

Nem todo tweet que corresponde a uma regra aparece em um fluxo.

A limitação de regra do Twitter e as interrupções do feed do Twitter podem limitar o número de tweets visíveis no stream.

>[!NOTE]
>
>Para garantir que Tweets específicos sejam incluídos em seu fluxo, use a opção Carregar ativo na página Todos os ativos.

* O conteúdo das Regras do Twitter, puxando 1 tweet por regra a cada 5 segundos. Isso permite que o conteúdo apareça nos aplicativos do Livefyre seja mais equilibrado e não fique sobrecarregado com tweets. Limitar os tweets de entrada dessa forma também ajuda a impedir que o fluxo seja inundado ou ilegível durante períodos de tráfego altos.

   >[!NOTE]
   >
   >Para garantir que o conteúdo dos autores de alto valor apareça nos aplicativos, mesmo em fluxos de alta velocidade, as Regras para autores específicos nunca são encapsuladas.

* As interrupções do feed do Twitter podem ocorrer por vários motivos. Em alguns casos, o Twitter não envia tweets, portanto o Livefyre não recebe notificações do novo conteúdo e não pode ser exibido. Interrupções de serviço das apis do Twitter, ou tráfego em hashtags/palavras-chave de alto volume, também podem resultar em tweets perdidos.

