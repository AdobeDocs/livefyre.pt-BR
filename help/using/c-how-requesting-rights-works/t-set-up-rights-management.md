---
description: Defina as configurações para solicitar direitos para postagens do Instagram e do Twitter.
seo-description: Defina as configurações para solicitar direitos para postagens do Instagram e do Twitter.
seo-title: Configurar o Gerenciamento de direitos
solution: Experience Manager
title: Configurar o Gerenciamento de direitos
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Configurar o Gerenciamento de direitos{#set-up-rights-management}

Defina as configurações para solicitar direitos para postagens do Instagram e do Twitter.

Antes de definir as Configurações de solicitação de direitos, você deve configurar uma ou mais contas sociais para o Instagram ou Twitter. Para obter mais informações sobre como configurar uma conta social, consulte [Adicionar uma conta social](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Você pode configurar o gerenciamento de direitos somente no nível de rede. Não é possível configurar o gerenciamento de direitos específico do site.

1. No Livefyre Studio, navegue **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]** até.

   >[!NOTE]
   >
   >Você precisará de permissões de nível de rede do Moderador ou Administrador para configurar Contas de gerenciamento de direitos.

1. Selecione **[!UICONTROL +Add New Account]** se você não tem contas de Gerenciamento de direitos definidas.
1. Clique **[!UICONTROL Create New Setting]** na rede social que deseja usar para o Rights Management.

   >[!NOTE]
   >
   >Para contas do Instagram, é necessário ter uma conta comercial do Instagram para solicitar direitos com automação parcial. Para obter mais informações sobre os diferentes tipos de contas do Instagram e como usá-las, consulte [Sobre contas](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)do Instagram.

1. Preencha os campos exibidos. Todos os campos são obrigatórios.

   * **[!UICONTROL Display name:]** Digite um nome para exibição para identificar a conta do Twitter ou do Instagram a ser usada na sua conta de Solicitação de direitos. Esse nome é apenas interno.
   * ****[!UICONTROL Enabled:]Definido como padrão por padrão. Habilita o gerenciamento de direitos para a conta.
   * **[!UICONTROL Approval hashtag:]** A hashtag que o proprietário do conteúdo usará para indicar que eles aceitam usar seu conteúdo.
   * **[!UICONTROL Terms and conditions:]** Um link para os Termos e condições da sua rede para a reutilização do conteúdo. Este campo diferencia maiúsculas e minúsculas.
   * **[!UICONTROL Network and sites:]** A rede ou o site para o qual esta conta pode solicitar direitos de reutilização de conteúdo. Para tornar essa conta disponível em toda a rede, selecione o primeiro item na lista ou limite para sites específicos usando a tecla Command/CTRL.
   * **[!UICONTROL Default message:]** Uma mensagem a ser exibida com sua Solicitação de direitos. Você pode substituir esta mensagem ao solicitar direitos.

      * O Livefyre apresenta uma das mensagens padrão a moderadores quando um moderador emite uma solicitação para um autor de conteúdo. Os moderadores podem gerar outra mensagem padrão ou editar a mensagem antes de enviar. As mensagens devem incluir o Twitter ou o identificador do Instagram ({identificador}), a hashtag de aprovação ({granttag}) e um link para seus Termos e condições ({termslink}).

         **[!UICONTROL Note:]** {identificador}, {granttag} e {termslink} fazem distinção entre letras maiúsculas e minúsculas.

         **[!UICONTROL Note:]** Para evitar uso malicioso, o Twitter vincula quaisquer urls incluídos com [formatação t. co](https://t.co/) . Para evitar que sua mensagem padrão exceda 140 caracteres, o Livefyre recomenda não incluir urls na mensagem padrão.

      * Práticas recomendadas para a gravação de mensagens de solicitação de direitos:

         * Crie várias mensagens padrão para que não se pareça como um robô. Salve cada mensagem padrão antes de criar a sua próxima mensagem padrão.
         * Incentive seus moderadores a personalizarem esta observação antes de enviar, para impedir que as solicitações da rede sejam marcadas como Spam.

1. Clique em **[!UICONTROL Save Settings]** para adicionar sua conta de Solicitação de direitos.
Envie uma solicitação de direitos a partir da Biblioteca de ativos. Consulte [Enviar uma solicitação](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) de direitos para obter mais informações sobre como enviar uma solicitação de direitos da Biblioteca de ativos.