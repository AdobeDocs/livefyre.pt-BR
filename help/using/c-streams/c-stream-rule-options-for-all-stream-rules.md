---
description: Essas opções se aplicam a quaisquer regras de fluxo de todas as redes sociais ou métodos de publicação.
seo-description: Essas opções se aplicam a quaisquer regras de fluxo de todas as redes sociais ou métodos de publicação.
seo-title: Opções de regras de fluxo para todas as regras de fluxo
solution: Experience Manager
title: Opções de regras de fluxo para todas as regras de fluxo
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# Opções de regras de fluxo para todas as regras de fluxo{#stream-rule-options-for-all-stream-rules}

Essas opções se aplicam a quaisquer regras de fluxo de todas as redes sociais ou métodos de publicação.

Pesquisar recursos para campos de texto e palavra-chave:

* Quando você digita palavras-chave, o Livefyre usa automaticamente o operador Booliano **OU** quando se trata de palavras individuais. Por exemplo, para pesquisar por publicações com a palavra *bolo* ou *fórmula*, digite *bolo* e insira a *fórmula* no **[!UICONTROL keyword]** campo.

* Você pode pesquisar por frases exatas ao redor do texto exato da frase entre aspas. Por exemplo, para pesquisar a receita *exata do* bolo de frases, digite *"receita do bolo"* no **[!UICONTROL keyword]** campo.

* É possível combinar as pesquisas Booleanas e de frases exatas em uma regra de fluxo. Por exemplo, você pode procurar por *bolo*, *receita* e *"receita de bolo"* inserindo cada frase uma de cada vez.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selecione uma das seguintes opções:

   * **[!UICONTROL All Content.]** Permitir qualquer conteúdo.
   * **[!UICONTROL Media Required.]** Permitir somente conteúdo com imagens e vídeos. (Para conteúdo do Instagram e do Facebook, você pode especificar **[!UICONTROL Photos]** ou **[!UICONTROL Videos]** apenas).

* **[!UICONTROL Language]**. Escolha o idioma no qual pesquisar. O inglês é o idioma padrão.
* **[!UICONTROL Smart Tags]**. Escolha as tags a serem usadas para identificar o conteúdo. Livefyre usa a tecnologia de visão computacional para identificar fotos e vídeos com tags inteligentes específicas para tornar essa pesquisa mais precisa. Use o **[!UICONTROL ANY]** modificador para filtrar o conteúdo no fluxo usando qualquer tag ou **[!UICONTROL ALL]** modificador para filtrar o conteúdo no fluxo que usa todas as tags. Use o **[!UICONTROL Image contains none of these smart tags]** campo para inserir tags para fotos que contenham conteúdo não desejado no fluxo. Essa opção não funciona para conteúdo de texto.

* **[!UICONTROL Products]**. Adicione tags de produto para corresponder à regra de fluxo com produtos do catálogo de produtos.
* **[!UICONTROL Premoderate]**. Selecione uma das seguintes opções:

   * **[!UICONTROL On]**. Preparar todo o conteúdo da regra de entrada. Você pode exibir conteúdo pré-moderado na seção Streams do ModQ. **[!UICONTROL On]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Off]**. Não pré-moderar nenhum conteúdo de regra recebido. **[!UICONTROL Off]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Inherited (Off)]**. Use as configurações pré-moderadas do site (em **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selecione uma das seguintes opções:
   * **[!UICONTROL Apply SAFE Rules]**. Aplique todas as regras SAFE a este fluxo.
   * **[!UICONTROL Apply SAFE Rules for:]** Selecione uma ou mais opções para aplicar as Regras SAFE para esta regra de fluxo.
   * **[!UICONTROL Disable SAFE Rules]**. Não aplique quaisquer Regras SAFE a este fluxo.

Para obter opções de regras de fluxo específicas a uma rede social ou tipo de conteúdo, consulte a seguinte documentação para o respectivo tipo de rede social ou conteúdo:

* [Páginas do Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Email](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
