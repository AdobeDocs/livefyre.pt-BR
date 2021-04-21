---
description: Você pode criar regras de fluxo que extraem conteúdo do Tumblr.
title: Regras Tumblr
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Regras Tumblr{#tumblr-rules}

Você pode criar regras de fluxo que extraem conteúdo do Tumblr.

Crie regras do Tumblr com base em um blog do Tumblr e filtrado por tag. Os fluxos Tumblr são atualizados a cada 5 minutos, procurando por conteúdo que ainda não existe no Livefyre dos 20 primeiros itens no feed. O Livefyre ignora tudo depois dos 20 primeiros itens no feed.

Para criar Regras Tumblr para inserir conteúdo do Tumblr no seu aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Blog]**

   * Insira o **[!UICONTROL Blog Name]** para o blog do Tumblr. Insira o URL (*staff.tumblr.com*) ou o nome do blog (*staff*).

   * Inclua até um **[!UICONTROL Tag]** para filtrar os resultados por publicações, incluindo uma determinada tag.

* **[!UICONTROL Include recent items.]** Se estiver definido como:

   * **[!UICONTROL Enabled]**, Livefyre adiciona os primeiros 20 itens de conteúdo em seu feed ao fluxo, independentemente da data da publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 20 itens de conteúdo em seu feed ao fluxo com uma data de publicação que é a mesma data de criação da regra de fluxo ou posterior.

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
