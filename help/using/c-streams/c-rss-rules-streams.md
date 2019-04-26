---
description: Você pode criar regras de fluxo que puxam conteúdo de feeds RSS.
seo-description: Você pode criar regras de fluxo que puxam conteúdo de feeds RSS.
seo-title: Regras RSS
solution: Experience Manager
title: Regras RSS
uuid: 3 c 9 e 2069-bb 85-41 dc -8 b 35-6237642 a 538 a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regras RSS{#rss-rules}

Você pode criar regras de fluxo que puxam conteúdo de feeds RSS.

Os fluxos RSS atualizam a cada 5 minutos, procurando conteúdo que ainda não existe no Livefyre dos primeiros 50 itens no feed. O Livefyre ignora tudo o que passou dos primeiros 50 itens no feed.

Para criar regras RSS para extrair conteúdo de feeds RSS para o aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL URL]** do Feed RSS.
* **[!UICONTROL Include recent items.]** Se isso for definido como:

   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 50 itens de conteúdo do feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 50 itens de conteúdo no feed ao stream com uma data de publicação que é igual à data de criação da regra de fluxo ou posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Extraia informações do link do item ou do XML.

**Regras RSS**

O Livefyre analisa os feeds RSS com base nas seguintes especificações RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS de mídia](https://en.wikipedia.org/wiki/Media_RSS)
* [Feed atom](https://validator.w3.org/feed/docs/atom.html)

O Livefyre não lê os feeds que não seguem essas especificações, e seu conteúdo não será inserido no seu fluxo. Use o Serviço de validação do feed WC 3 para verificar a sintaxe do feed RSS e garantir que seja válido.

Para opções adicionais de regras de Fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
