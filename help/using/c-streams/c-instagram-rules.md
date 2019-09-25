---
description: Você pode criar regras de fluxo que extraem conteúdo do Instagram.
seo-description: Você pode criar regras de fluxo que extraem conteúdo do Instagram.
seo-title: Regras do Instagram
title: Regras do Instagram
uuid: 98108db-5710-4331-891b-7e1bb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regras do Instagram{#instagram-rules}

Você pode criar regras de fluxo que extraem conteúdo do Instagram.

>[!NOTE]
>
>Antes de criar um fluxo do Instagram, você deve adicionar pelo menos uma conta comercial do Instagram à **[!UICONTROL Social Accounts]** seção em **[!UICONTROL Network Settings]**. Para obter mais informações sobre como configurar uma conta do Instagram, consulte [Sobre contas](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)do Instagram.

Crie regras do Instagram com base em @menções ou hashtag.

>[!NOTE]
>
>Todas as regras do Instagram exigem pelo menos uma hashtag. Adicionar palavras-chave e um nome de usuário para sua regra retornará conteúdo que inclui ambas as entradas.

Para criar regras do Instagram para extrair conteúdo dos feeds do Instagram para seu aplicativo ou pasta, filtre por:

* **[!UICONTROL Words]**

   * Digite **[!UICONTROL hashtags]** para ser incluído ou excluído do seu fluxo do Instagram. A especificação de valores para os campos **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]** retornará imagens que contêm o primeiro e não o segundo.

   * Por exemplo, inserir **[!UICONTROL Contains]** palavras-chave Giants, Posey e **[!UICONTROL Does not contain]** a palavra-chave Dodger retornará todas as publicações que incluem a palavra Giants ou Posey e não incluirão a palavra Dodger.

      >[!NOTE]
      >
      >As Regras do Instagram retornarão postagens que incluem a hashtag listada nos comentários do autor, que podem não aparecer no stream.

* **[!UICONTROL Mentions]**

   * Insira **[!UICONTROL @mentions]** para extrair no fluxo ou exclua do fluxo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >É necessário ter uma conta comercial do Instagram configurada no Livefyre para usar a pesquisa Autor em uma regra do Instagram Stream. Para obter mais informações sobre como configurar contas comerciais do Instagram no Livefyre, consulte [Sobre contas](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)do Instagram.

   * Digite **[!UICONTROL @usernames]** para entrar no fluxo. A conta associada ao **@username** deve ser uma conta comercial do Instagram.

   * Digite o **@usernames** a ser excluído do fluxo.

* **[!UICONTROL Additional Filters]**

   * Selecione se deseja incluir **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** no seu fluxo.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte Opções de regra de [fluxo para todas as regras](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de fluxo.
