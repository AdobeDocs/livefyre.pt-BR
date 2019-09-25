---
description: Nem todos os tweets que correspondem a uma regra são exibidos em um fluxo.
seo-description: Nem todos os tweets que correspondem a uma regra são exibidos em um fluxo.
seo-title: Limitação e frequência de tweets
solution: Experience Manager
title: Limitação e frequência de tweets
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Limitação e frequência de tweets{#throttling-and-frequency-of-tweets}

Nem todos os tweets que correspondem a uma regra são exibidos em um fluxo.

A limitação de regras do Twitter e as interrupções de feed do Twitter podem limitar o número de Tweets visíveis no fluxo.

>[!NOTE]
>
>Para garantir que tweets específicos sejam incluídos no seu fluxo, use a opção Fazer upload do ativo na página Todos os ativos.

* As regras do Twitter reduzem o conteúdo, puxando 1 Tweet por regra a cada 5 segundos. Isso permite que o conteúdo que aparece nos aplicativos Livefyre seja mais equilibrado e não fique sobrecarregado com tweets. Limitar os tweets recebidos dessa maneira também ajuda a impedir que o fluxo se torne inundado ou ilegível durante períodos de tráfego altos.

   >[!NOTE]
   >
   >Para garantir que o conteúdo de seus autores de alto valor apareça em seus aplicativos, mesmo em fluxos de alta velocidade, as Regras para autores específicos nunca são aceleradas.

* As interrupções de feed do Twitter podem ocorrer por vários motivos. Em alguns casos, o Twitter não envia tweets, portanto, o Livefyre não recebe notificação do novo conteúdo e não pode ser exibido. Interrupções de serviço de APIs do Twitter ou tráfego em hashtags/palavras-chave de alto volume também podem resultar em tweets perdidos.

