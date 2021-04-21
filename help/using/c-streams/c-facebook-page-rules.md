---
description: Você pode criar regras de fluxo que obtêm conteúdo das páginas do Facebook.
title: Regras da página do facebook
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Regras de página do facebook{#facebook-page-rules}

Você pode criar regras de fluxo que obtêm conteúdo das páginas do Facebook.

Você pode usar as Regras de página do Facebook para fazer stream de conteúdo publicado publicamente a partir de Páginas do Facebook. O conteúdo será extraído para o aplicativo ou pasta na mesma frequência do SocialSync, que muda com base na página do Facebook e nos padrões de tráfego de postagem. Os links nas páginas do Facebook também são suportados e serão exibidos no fluxo.

Para criar Regras de página do Facebook para extrair conteúdo das páginas do Facebook para seu aplicativo ou Pasta, você pode filtrar por:

* **[!UICONTROL Facebook Page]**

   * Insira o **[!UICONTROL Name]** para a Página. Insira somente o texto à direita para o URL. **Por exemplo:** Para adicionar conteúdo de  `https://facebook.com/KellysSuperFunFanPage`, digite  ** KellysSuperFunFanPage no  **[!UICONTROL Name]** campo.

   * Ative **[!UICONTROL Include Facebook Comments for each post]** se desejar incluir comentários do usuário em Publicações da página.
   * Ative **[!UICONTROL Only Show Author Posts]** se desejar excluir publicações de outros usuários.

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>O Livefyre é restrito ao conteúdo recebido do Facebook e, portanto, não pode garantir que todas as publicações em uma página do Facebook sejam incluídas no seu fluxo.

>[!NOTE]
>
>Se o Facebook SocialSync e uma Regra de página do Facebook estiverem ativados para uma Página específica do Facebook e os comentários do usuário estiverem ativados para a Regra de página do Facebook, a Regra de fluxo substituirá o SocialSync. O conteúdo será transmitido para o aplicativo com base somente na regra de preparação de página do Facebook, e não usando o SocialSync.

Os tipos de conteúdo compatíveis com o Facebook Page Curate incluem:

* Proprietário ou administrador da página

   * Status
   * Fotos
   * Vídeos como links

* Usuário padrão do Facebook

   * Status
   * Fotos
   * Vídeos como links

* Terceiros

   * Status
