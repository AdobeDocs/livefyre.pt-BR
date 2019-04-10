---
description: Você pode criar regras de fluxo que puxam conteúdo do Tumblr.
seo-description: Você pode criar regras de fluxo que puxam conteúdo do Tumblr.
seo-title: Regras do Tumblr
solution: Experience Manager
title: Regras do Tumblr
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Regras do Tumblr{#tumblr-rules}

Você pode criar regras de fluxo que puxam conteúdo do Tumblr.

Crie regras do Tumblr com base em um blog do Tumblr e filtrado por tag. Os fluxos tumblr são atualizados a cada 5 minutos, procurando conteúdo que ainda não existe no Livefyre dos primeiros 20 itens no feed. O Livefyre ignora tudo o que passou dos primeiros 20 itens no feed.

Para criar Regras do Tumblr para extrair o conteúdo do Tumblr no aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Blog]**

   * Digite o **[!UICONTROL Blog Name]** blog do Tumblr. Insira o URL (*staff.tumblr.com*) ou o nome do blog (*pessoal*).

   * Inclua até uma **[!UICONTROL Tag]** para filtrar os resultados por publicações que incluem uma determinada tag.

* **[!UICONTROL Include recent items.]** Se isso for definido como:

   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 20 itens de conteúdo do feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 20 itens de conteúdo no feed ao stream com uma data de publicação que é igual à data de criação da regra de fluxo ou posterior.

Para opções adicionais de regras de Fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
