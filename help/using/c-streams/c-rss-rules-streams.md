---
description: Você pode criar regras de fluxo que extraem conteúdo de feeds RSS.
title: Regras RSS
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Regras RSS{#rss-rules}

Você pode criar regras de fluxo que extraem conteúdo de feeds RSS.

Os fluxos RSS são atualizados a cada 5 minutos, procurando por conteúdo que ainda não existe no Livefyre a partir dos primeiros 50 itens no feed. O Livefyre ignora tudo depois dos primeiros 50 itens no feed.

Para criar Regras de RSS para extrair conteúdo de feeds RSS para o aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL URL]** do RSS Feed.
* **[!UICONTROL Include recent items.]** Se estiver definido como:

   * **[!UICONTROL Enabled]**, Livefyre adiciona os primeiros 50 itens de conteúdo no seu feed ao fluxo, independentemente da data da publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 50 itens de conteúdo em seu feed ao fluxo com uma data de publicação que seja a mesma data de criação da regra de fluxo ou posterior.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Obter informações do link do item ou do XML.

**Regras RSS**

O Livefyre analisa os feeds RSS com base nas seguintes especificações RSS:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [RSS de mídia](https://en.wikipedia.org/wiki/Media_RSS)
* [Feed Atom](https://validator.w3.org/feed/docs/atom.html)

O Livefyre não lê feeds que não aderem a essas especificações e seu conteúdo não será extraído para o seu fluxo. Use o Serviço de validação de feed WC3 para verificar a sintaxe do feed RSS e garantir que ele seja válido.

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
