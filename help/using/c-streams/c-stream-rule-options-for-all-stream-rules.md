---
description: Essas opções se aplicam a todas as regras de fluxo de todas as redes sociais ou métodos de publicação.
title: Opções de regra de fluxo para todas as regras de fluxo
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---

# Opções de Regra de Fluxo para Todas as Regras de Fluxo{#stream-rule-options-for-all-stream-rules}

Essas opções se aplicam a todas as regras de fluxo de todas as redes sociais ou métodos de publicação.

Pesquisar recursos para campos de texto e palavra-chave:

* Quando você insere palavras-chave, o Livefyre usa automaticamente o operador booleano **OU** quando para palavras individuais. Por exemplo, para procurar por postagens com a palavra *bolo* ou *receita*, digite *bolo* e digite *receita* no campo **[!UICONTROL keyword]**.

* Você pode pesquisar por frases exatas ao redor do texto da frase exata entre aspas. Por exemplo, para procurar a frase exata *receita do bolo*, digite *&quot;receita do bolo&quot;* no campo **[!UICONTROL keyword]**.

* É possível combinar as pesquisas de Booleano e de frase exata em uma regra de fluxo. Por exemplo, você pode procurar por *bolo*, *receita* e *&quot;receita do bolo&quot;* inserindo cada frase uma de cada vez.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selecione uma das opções a seguir:

   * **[!UICONTROL All Content.]** Permitir qualquer conteúdo.
   * **[!UICONTROL Media Required.]** Permitir somente conteúdo com imagens e vídeos. (Para conteúdo Instagram e Facebook, você pode especificar somente **[!UICONTROL Photos]** ou **[!UICONTROL Videos]**).

* **[!UICONTROL Language]**. Escolha o idioma para pesquisar. Inglês é o idioma padrão.
* **[!UICONTROL Smart Tags]**. Escolha as tags a serem usadas para identificar o conteúdo. Livefyre usa tecnologia de visão computacional para identificar fotos e vídeos com tags inteligentes específicas para tornar essa pesquisa mais precisa. Use o modificador **[!UICONTROL ANY]** para filtrar o conteúdo no fluxo usando qualquer tag ou o modificador **[!UICONTROL ALL]** para filtrar o conteúdo no fluxo que usa todas as tags. Use o campo **[!UICONTROL Image contains none of these smart tags]** para inserir tags para fotos que contenham conteúdo que você não deseja no stream. Essa opção não funciona para conteúdo de texto.

* **[!UICONTROL Products]**. Adicione tags de produto para corresponder a regra de fluxo com produtos do catálogo de produtos.
* **[!UICONTROL Premoderate]**. Selecione uma das opções a seguir:

   * **[!UICONTROL On]**. Remova todo o conteúdo da regra de entrada. Você pode exibir conteúdo pré-moderado na seção Streams do ModQ. **[!UICONTROL On]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Off]**. Não pré-modere nenhum conteúdo de regra de entrada. **[!UICONTROL Off]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Inherited (Off)]**. Use as configurações pré-moderadas do site (em **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selecione uma das opções a seguir:
   * **[!UICONTROL Apply SAFE Rules]**. Aplique todas as regras SAFE a este fluxo.
   * **[!UICONTROL Apply SAFE Rules for:]** Selecione uma ou mais das opções para aplicar Regras SAFE para esta regra de fluxo.
   * **[!UICONTROL Disable SAFE Rules]**. Não aplique quaisquer Regras SAFE a este fluxo.

Para obter as opções de Regra de fluxo específicas a uma rede social ou tipo de conteúdo, consulte a seguinte documentação para os respectivos tipos de rede social ou conteúdo:

* [Páginas do Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Email](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
