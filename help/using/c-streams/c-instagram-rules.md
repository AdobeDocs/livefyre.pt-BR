---
description: Você pode criar Regras de fluxo que obtêm conteúdo do Instagram.
title: Regras do instagram
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Regras do instagram{#instagram-rules}

Você pode criar Regras de fluxo que obtêm conteúdo do Instagram.

>[!NOTE]
>
>Antes de criar um fluxo do Instagram, você deve adicionar pelo menos uma conta comercial do Instagram à seção **[!UICONTROL Social Accounts]** em **[!UICONTROL Network Settings]**. Para obter mais informações sobre como configurar uma conta Instagram, consulte [Sobre contas Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Crie Regras do Instagram com base em @menções ou hashtag.

>[!NOTE]
>
>Todas as regras do Instagram exigem pelo menos uma hashtag. Adicionar palavras-chave e um nome de usuário para sua regra retornará conteúdo que inclui ambas as entradas.

Para criar regras do Instagram para extrair conteúdo dos feeds do Instagram para seu aplicativo ou Pasta, filtre por:

* **[!UICONTROL Words]**

   * Insira **[!UICONTROL hashtags]** para ser incluído ou excluído do fluxo do Instagram. A especificação de valores para os campos **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]** retornará imagens que contêm o primeiro e não contêm o segundo.

   * Por exemplo, inserir **[!UICONTROL Contains]** palavras-chave Giants, Posey e **[!UICONTROL Does not contain]** palavra-chave Dodger retornará todas as postagens que incluem a palavra Giants ou Posey e não incluirá a palavra Dodger.

      >[!NOTE]
      >
      >As Regras do instagram retornarão postagens que incluem a hashtag listada nos comentários do autor, que podem não aparecer no stream.

* **[!UICONTROL Mentions]**

   * Insira **[!UICONTROL @mentions]** para entrar no fluxo ou exclua do fluxo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Você deve ter uma conta comercial do Instagram configurada no Livefyre para usar a pesquisa Autor em uma regra do Instagram Stream. Para obter mais informações sobre como configurar contas comerciais do Instagram no Livefyre, consulte [Sobre contas do Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Insira **[!UICONTROL @usernames]** para entrar no fluxo. A conta associada ao **@username** deve ser uma conta comercial do Instagram.

   * Insira o **@usernames** para excluir do fluxo.

* **[!UICONTROL Additional Filters]**

   * Selecione se deseja incluir **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** no seu fluxo.

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
