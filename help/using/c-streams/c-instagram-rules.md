---
description: Você pode criar regras de fluxo que extraem conteúdo do Instagram.
seo-description: Você pode criar regras de fluxo que extraem conteúdo do Instagram.
seo-title: Regras do Instagram
title: Regras do Instagram
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Regras do Instagram{#instagram-rules}

Você pode criar regras de fluxo que extraem conteúdo do Instagram.

>[!NOTE]
>
>Antes de criar um fluxo do Instagram, você deve adicionar pelo menos uma conta comercial do Instagram à seção **[!UICONTROL Social Accounts]** em **[!UICONTROL Network Settings]**. Para obter mais informações sobre como configurar uma conta do Instagram, consulte [Sobre as contas do Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Crie regras do Instagram com base em @menções ou hashtag.

>[!NOTE]
>
>Todas as regras do Instagram exigem pelo menos uma hashtag. Adicionar palavras-chave e um nome de usuário para sua regra retornará conteúdo que inclui ambas as entradas.

Para criar regras do Instagram para extrair conteúdo dos feeds do Instagram para seu aplicativo ou pasta, filtre por:

* **[!UICONTROL Words]**

   * Insira **[!UICONTROL hashtags]** para ser incluído ou excluído do fluxo do Instagram. A especificação de valores para os campos **[!UICONTROL Contains]** e **[!UICONTROL Does not contain]** retornará imagens que contêm a primeira e não a segunda.

   * Por exemplo, inserir **[!UICONTROL Contains]** palavras-chave Giants, Posey e **[!UICONTROL Does not contain]** palavras-chave Dodger retornará todas as publicações que incluem a palavra Giants ou Posey e não incluirá a palavra Dodger.

      >[!NOTE]
      >
      >As Regras do Instagram retornarão postagens que incluem a hashtag listada nos comentários do autor, que podem não aparecer no stream.

* **[!UICONTROL Mentions]**

   * Digite **[!UICONTROL @mentions]** para entrar no fluxo ou exclua do fluxo.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >É necessário ter uma conta comercial do Instagram configurada no Livefyre para usar a pesquisa Autor em uma regra do Instagram Stream. Para obter mais informações sobre como configurar contas de negócios do Instagram no Livefyre, consulte [Sobre as contas do Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Digite **[!UICONTROL @usernames]** para entrar no fluxo. A conta associada ao **@username** deve ser uma conta de negócios do Instagram.

   * Insira **@usernames** para excluir do fluxo.

* **[!UICONTROL Additional Filters]**

   * Selecione se deseja incluir **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** ou **[!UICONTROL Photos Only]** no seu fluxo.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
