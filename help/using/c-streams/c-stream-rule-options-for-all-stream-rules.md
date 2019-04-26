---
description: Essas opções se aplicam a qualquer regra de fluxo de todas as redes sociais
  ou métodos de postagem.
seo-description: Essas opções se aplicam a qualquer regra de fluxo de todas as redes
  sociais ou métodos de postagem.
seo-title: Opções de regras de fluxo para todas as regras de fluxo
solution: Experience Manager
title: Opções de regras de fluxo para todas as regras de fluxo
uuid: 4072 ee 83-31 e 7-4 de 6-918 c -134 b 8 b 8032 e 1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# Opções de regras de fluxo para todas as regras de fluxo{#stream-rule-options-for-all-stream-rules}

Essas opções se aplicam a qualquer regra de fluxo de todas as redes sociais ou métodos de postagem.

Recursos de pesquisa para campos de texto e palavra-chave:

* Quando você insere palavras-chave, o Livefyre usa automaticamente o operador Booleano **OU** quando para palavras individuais. Por exemplo, para pesquisar postagens com *o botão* ou *a fórmula de palavra*, insira *o bolo*e insira *a fórmula* no **[!UICONTROL keyword]** campo.

* Você pode pesquisar frases exatas ao redor do texto da frase exata entre aspas. Por exemplo, para pesquisar a fórmula exata *do bolo de frase*, digite *"recipe de bola"* no **[!UICONTROL keyword]** campo.

* É possível combinar a pesquisa Booleana e as pesquisas exatas em uma regra de fluxo. Por exemplo, você pode pesquisar *o bolo*, *a fórmula*e *a "receita do bolo"* inserindo cada frase uma de cada vez.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Selecione um dos seguintes:

   * **[!UICONTROL All Content.]** Permitir qualquer conteúdo.
   * **[!UICONTROL Media Required.]** Permitir apenas conteúdos com imagens e vídeos. (Para o conteúdo do Instagram e do Facebook, você pode especificar **[!UICONTROL Photos]** apenas **[!UICONTROL Videos]** ).

* **[!UICONTROL Language]**. Escolha o idioma a ser pesquisado. Inglês é o idioma padrão.
* **[!UICONTROL Smart Tags]**. Escolha as tags a serem usadas para identificar o conteúdo. O Livefyre usa tecnologia de visão do computador para identificar fotos e vídeos com tags inteligentes específicas para tornar essa pesquisa mais precisa. Use o **[!UICONTROL ANY]** modificador para filtrar o conteúdo no stream usando qualquer tag ou **[!UICONTROL ALL]** modificador para filtrar o conteúdo no stream que usa todas as tags. Use **[!UICONTROL Image contains none of these smart tags]** o campo para inserir tags para fotos contendo conteúdo que você não deseja no stream. Essa opção não funciona para conteúdo de texto.

* **[!UICONTROL Products]**. Adicione tags de produto para corresponder à regra de fluxo com produtos do catálogo de produtos.
* **[!UICONTROL Premoderate]**. Selecione um dos seguintes:

   * **[!UICONTROL On]**. Pré-moderar todo o conteúdo da regra de entrada. É possível exibir conteúdo pré-moderado da seção Fluxos de modq. **[!UICONTROL On]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Off]**. Não pré-modere qualquer conteúdo de regra de entrada. **[!UICONTROL Off]** substitui as configurações em Configurações do aplicativo.
   * **[!UICONTROL Inherited (Off)]**. Use as configurações de pré-moderação do site (em **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Selecione um dos seguintes:
   * **[!UICONTROL Apply SAFE Rules]**. Aplique todas as regras de segurança a este fluxo.
   * **[!UICONTROL Apply SAFE Rules for:]** Selecione uma ou mais opções para aplicar Regras de segurança para esta regra de fluxo.
   * **[!UICONTROL Disable SAFE Rules]**. Não aplique regras de segurança a esse fluxo.

Para opções de regras de fluxo específicas a uma rede social ou tipo de conteúdo, consulte a documentação a seguir para a respectiva rede social ou tipo de conteúdo:

* [Páginas do Facebook](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [Email](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [Youtube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
