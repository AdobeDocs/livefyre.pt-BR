---
description: Você pode criar regras de fluxo que extraem conteúdo do Tumblr.
seo-description: Você pode criar regras de fluxo que extraem conteúdo do Tumblr.
seo-title: Regras do Tumblr
solution: Experience Manager
title: Regras do Tumblr
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Regras do Tumblr{#tumblr-rules}

Você pode criar regras de fluxo que extraem conteúdo do Tumblr.

Crie regras do Tumblr com base em um blog do Tumblr e filtrado por tag. Os fluxos do Tumblr são atualizados a cada 5 minutos, procurando por conteúdo que ainda não existe no Livefyre dos primeiros 20 itens no feed. Livefyre ignora tudo depois dos 20 primeiros itens no feed.

Para criar Regras do Tumblr para inserir conteúdo do Tumblr em seu aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Blog]**

   * Digite o **[!UICONTROL Blog Name]** para o blog do Tumblr. Insira o URL (*staff.tumblr.com*) ou o nome do blog (*staff*).

   * Inclua até um **[!UICONTROL Tag]** para filtrar os resultados por publicações que incluem uma determinada tag.

* **[!UICONTROL Include recent items.]** Se estiver definido como:

   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 20 itens de conteúdo em seu feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 20 itens de conteúdo no feed ao stream com uma data de publicação que é a mesma que a data de criação da regra de fluxo ou posterior.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
