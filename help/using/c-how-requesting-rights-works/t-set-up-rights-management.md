---
description: Defina as configurações para solicitar direitos para publicações do Instagram e do Twitter.
seo-description: Defina as configurações para solicitar direitos para publicações do Instagram e do Twitter.
seo-title: Configurar Rights Management
solution: Experience Manager
title: Configurar Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# Configurar Rights Management{#set-up-rights-management}

Defina as configurações para solicitar direitos para publicações do Instagram e do Twitter.

Antes de definir Configurações de solicitação de direitos, você deve configurar uma ou mais contas sociais para o Instagram ou Twitter. Para obter mais informações sobre como configurar uma conta social, consulte [Adicionar uma conta do Social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Você pode configurar o gerenciamento de direitos somente no nível da Rede. Não é possível configurar o gerenciamento de direitos específico do site.

1. No Livefyre Studio, navegue até **[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Você precisará de permissões de nível de rede do Moderador ou Administrador para configurar as Contas de Rights Management.

1. Selecione **[!UICONTROL +Add New Account]** se você não tiver nenhuma conta Rights Management configurada.
1. Clique em **[!UICONTROL Create New Setting]** na rede social que deseja usar para o Rights Management.

   >[!NOTE]
   >
   >Para contas do Instagram, é necessário ter uma conta de negócios do Instagram para solicitar direitos com automação parcial. Para obter mais informações sobre os diferentes tipos de contas do Instagram e como usá-las, consulte [Sobre as Contas do Instagram](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Preencha os campos exibidos. Todos os campos são obrigatórios.

   * **[!UICONTROL Display name:]** Insira um nome para exibição para identificar a conta do Twitter ou Instagram a ser usada para sua conta de Solicitação de direitos. Este nome é apenas interno.
   * **[!UICONTROL Enabled:]**Definido como ativado por padrão. Ativa o gerenciamento de direitos para a conta.
   * **[!UICONTROL Approval hashtag:]** A hashtag que o proprietário do conteúdo usará para indicar que ele concorda em usar seu conteúdo.
   * **[!UICONTROL Terms and conditions:]** Um link para os Termos e condições de sua rede para a reutilização do conteúdo. Este campo diferencia maiúsculas de minúsculas.
   * **[!UICONTROL Network and sites:]** A rede ou site para o qual esta conta pode solicitar direitos de reutilização de conteúdo. Para disponibilizar essa conta em toda a rede, selecione o primeiro item na lista ou limite a sites específicos usando a chave Command/CTRL.
   * **[!UICONTROL Default message:]** Uma mensagem a ser exibida com sua Solicitação de direitos. Você pode substituir essa mensagem ao solicitar direitos.

      * O Livefyre apresenta uma das mensagens padrão aos moderadores quando um moderador emite uma solicitação para um autor de conteúdo. Os moderadores podem gerar outra mensagem padrão ou editar a mensagem antes de enviá-la. As mensagens devem incluir o identificador do Twitter ou Instagram do autor ({identificador}), sua hashtag de aprovação ({GrantTag}) e um link para seus Termos e Condições ({termsLink}).

         **[!UICONTROL Note:]** {identificador}, {GrantTag} e {termsLink} distinguem maiúsculas de minúsculas.

         **[!UICONTROL Note:]** Para evitar o uso mal-intencionado, o Twitter vincula quaisquer URLs incluídos com  [t.](https://t.co/) coformatting. Para impedir que sua mensagem padrão exceda 140 caracteres, Livefyre recomenda não incluir URLs na mensagem padrão.

      * Práticas recomendadas para gravar mensagens de solicitação de direitos:

         * Crie várias mensagens padrão para que você não pareça um robô. Salve cada mensagem padrão antes de criar sua próxima mensagem padrão.
         * Incentive os moderadores a personalizarem esta nota antes de enviarem, para evitar que as solicitações da rede sejam marcadas como Spam.

1. Clique em **[!UICONTROL Save Settings]** para adicionar sua conta de Solicitação de direitos.
Envie uma solicitação de direitos da Biblioteca de ativos. Consulte [Enviar uma solicitação de direitos](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) para obter mais informações sobre como enviar uma solicitação de direitos da Biblioteca de ativos.