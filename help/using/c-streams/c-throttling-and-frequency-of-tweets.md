---
description: Nem todos os tweets que correspondem a uma regra são exibidos em um fluxo.
title: Limitação e frequência de tweets
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Limitação e frequência de tweets{#throttling-and-frequency-of-tweets}

Nem todos os tweets que correspondem a uma regra são exibidos em um fluxo.

O controle de regras do twitter e as interrupções do feed do Twitter podem limitar o número de Tweets visíveis no stream.

>[!NOTE]
>
>Para garantir que tweets específicos sejam incluídos em seu fluxo, use a opção Fazer upload de ativo na página Todos os ativos .

* As regras do twitter limitam o conteúdo, puxando 1 Tweet por regra a cada 5 segundos. Isso permite que o conteúdo que aparece nos aplicativos do Livefyre seja mais equilibrado e não se torne sobrecarregado por tweets. Limitar os Tweets recebidos dessa maneira também ajuda a impedir que o fluxo se torne inundado ou ilegível durante períodos de alto tráfego.

   >[!NOTE]
   >
   >Para garantir que o conteúdo de seus autores de alto valor apareça em seus aplicativos, mesmo em fluxos de alta velocidade, as Regras para autores específicos nunca serão diminuídas.

* As interrupções do feed do twitter podem ocorrer por vários motivos. Em alguns casos, o Twitter não envia tweets, portanto, o Livefyre não recebe notificação do novo conteúdo e ele não pode ser exibido. As interrupções do serviço das APIs da Twitter, ou o tráfego em hashtags/palavras-chave de alto volume, também podem resultar na perda de Tweets.
