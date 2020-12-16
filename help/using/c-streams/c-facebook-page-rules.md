---
description: Você pode criar regras de fluxo que extraem conteúdo de Páginas do Facebook.
seo-description: Você pode criar regras de fluxo que extraem conteúdo de Páginas do Facebook.
seo-title: Regras de página do Facebook
solution: Experience Manager
title: Regras de página do Facebook
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Regras de página do Facebook{#facebook-page-rules}

Você pode criar regras de fluxo que extraem conteúdo de Páginas do Facebook.

Você pode usar as Regras de página do Facebook para transmitir o conteúdo publicado publicamente das Páginas do Facebook. O conteúdo será colocado no aplicativo ou na pasta com a mesma frequência do SocialSync, que muda com base na página do Facebook e nos padrões de tráfego de postagem. Links em Páginas do Facebook também são suportados e serão exibidos no stream.

Para criar Regras de página do Facebook para extrair conteúdo de páginas do Facebook para seu aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Facebook Page]**

   * Digite **[!UICONTROL Name]** como Página. Insira apenas o texto à direita para o URL. **Por exemplo:** Para adicionar conteúdo de  `https://facebook.com/KellysSuperFunFanPage`, digite  ** KellysSuperFunFanPagein no  **[!UICONTROL Name]** campo.

   * Ative **[!UICONTROL Include Facebook Comments for each post]** se desejar incluir comentários do usuário nas postagens da Página.
   * Ative **[!UICONTROL Only Show Author Posts]** se desejar excluir publicações de outros usuários.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>O Livefyre está restrito ao conteúdo recebido do Facebook e, portanto, não é capaz de garantir que cada postagem em uma página do Facebook seja incluída em seu fluxo.

>[!NOTE]
>
>Se o Facebook SocialSync e uma Regra de página do Facebook estiverem ativados para uma página específica do Facebook e os comentários do usuário estiverem ativados para a Regra de página do Facebook, a Regra de fluxo substituirá o SocialSync. O conteúdo será transmitido no aplicativo com base apenas na regra de preparação de página do Facebook e não no uso do SocialSync.

Os tipos de conteúdo suportados pelo Facebook Page Curate incluem:

* Proprietário ou Administrador da página

   * Status
   * Fotos
   * Vídeos como links

* Usuário padrão do Facebook

   * Status
   * Fotos
   * Vídeos como links

* Terceiros

   * Status

