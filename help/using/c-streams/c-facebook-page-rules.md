---
description: Você pode criar regras de fluxo que puxam conteúdo de Páginas do Facebook.
seo-description: Você pode criar regras de fluxo que puxam conteúdo de Páginas do
  Facebook.
seo-title: Regras de página do Facebook
solution: Experience Manager
title: Regras de página do Facebook
uuid: 2 be 63476-1 a 92-409 d-a 22 f-e 1 ec 66 b 6 dcc 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Regras de página do Facebook{#facebook-page-rules}

Você pode criar regras de fluxo que puxam conteúdo de Páginas do Facebook.

Você pode usar Regras de página do Facebook para transmitir conteúdo publicado publicamente das páginas do Facebook. O conteúdo será coletado no aplicativo ou pasta na mesma frequência do socialsync, que muda com base na página do Facebook e nos padrões de tráfego da postagem. Os links nas Páginas do Facebook também são suportados e serão exibidos no stream.

Para criar Regras de página do Facebook para extrair conteúdo das páginas do Facebook no aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Facebook Page]**

   * Insira a **[!UICONTROL Name]** página para a página. Digite somente o texto à direita para o URL. **Por exemplo:** Para adicionar conteúdo de `https://facebook.com/KellysSuperFunFanPage`, digite *kellyssuperfunfanpage* no **[!UICONTROL Name]** campo.

   * Ative **[!UICONTROL Include Facebook Comments for each post]** se deseja incluir comentários do usuário nas publicações da Página.
   * Ative **[!UICONTROL Only Show Author Posts]** se deseja excluir publicações de outros usuários.

Para opções adicionais de regras de Fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>O Livefyre está restrito ao conteúdo recebido do Facebook e, portanto, não é possível garantir que cada publicação em uma Página do Facebook será incluída em seu fluxo.

>[!NOTE]
>
>Se o socialsync do Facebook e uma Regra de página do Facebook estiverem ativados para uma Página do Facebook específica e os comentários do usuário forem ativados para a Regra de página do Facebook, a Regra de fluxo substituirá socialsync. O conteúdo será transmitido para o aplicativo com base na Regra de preparação de página do Facebook e não usando o socialsync.

Os tipos de conteúdo compatíveis com a Curadoria de página do Facebook incluem:

* Proprietário da página ou Administrador

   * Status
   * Fotos
   * Vídeos como links

* Usuário padrão do Facebook

   * Status
   * Fotos
   * Vídeos como links

* Terceiros

   * Status

