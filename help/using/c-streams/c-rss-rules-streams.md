---
description: Você pode criar regras de fluxo que extraem conteúdo de feeds RSS.
seo-description: Você pode criar regras de fluxo que extraem conteúdo de feeds RSS.
seo-title: Regras RSS
solution: Experience Manager
title: Regras RSS
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regras RSS{#rss-rules}

Você pode criar regras de fluxo que extraem conteúdo de feeds RSS.

Os fluxos RSS são atualizados a cada 5 minutos, procurando por conteúdo que ainda não existe no Livefyre dos primeiros 50 itens no feed. Livefyre ignora tudo depois dos 50 primeiros itens no feed.

Para criar Regras RSS para extrair conteúdo de feeds RSS para o aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL URL]** do RSS Feed.
* **[!UICONTROL Include recent items.]** Se estiver definido como:

   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 50 itens de conteúdo em seu feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 50 itens de conteúdo no feed ao stream com uma data de publicação que é a mesma que a data de criação da regra de fluxo ou posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Retire informações do link do item ou do XML.

**Regras RSS**

O Livefyre analisa os feeds RSS com base nas seguintes especificações RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS de mídia](https://en.wikipedia.org/wiki/Media_RSS)
* [Feed Atom](https://validator.w3.org/feed/docs/atom.html)

O Livefyre não lê feeds que não aderem a essas especificações e seu conteúdo não será inserido em seu stream. Use o Serviço de validação de feed WC3 para verificar a sintaxe do feed RSS e garantir que ele seja válido.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte Opções de regra de [fluxo para todas as regras](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de fluxo.
