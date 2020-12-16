---
description: Crie uma solicitação de privacidade no Livefyre.
seo-description: Crie uma solicitação de privacidade no Livefyre.
seo-title: Criar uma solicitação de privacidade
title: Criar uma solicitação de privacidade
uuid: 9fdbd564-0cea-4e4f-bdea-d5b8744fe63a
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---


# Criar uma solicitação de privacidade{#create-a-privacy-request}

Crie uma solicitação de privacidade no Livefyre.

Exclua todos os dados de um usuário, gere um relatório de todos os dados de um usuário e faça alterações de aceitação ou recusa usando esse processo.

Para pesquisar e localizar um usuário e gerar um relatório de seu conteúdo:

1. Vá para **[!UICONTROL Settings > Privacy]** e clique em **[!UICONTROL Create Request]**.

   ![](assets/privacypage1.png)

1. Preencha as informações na janela **[!UICONTROL Submit Request]**:

   * **[!UICONTROL Reference Id]**. Insira um identificador para usar para referência futura. Por exemplo, você pode adicionar texto, um número de tíquete, um URL, um endereço de email ou outra sequência de até 255 caracteres
   * **[!UICONTROL Type]**

      * **Acesso**. Coleta todos os dados disponíveis associados à conta. Detalhes confidenciais, por exemplo, senhas ou credenciais sociais, serão ofuscados ou omitidos.

      * **Excluir**. Célula ou ofusca todos os dados associados à conta. **Se você escolher essa opção e clicar em Enviar, não será possível reverter ou cancelar essa ação  *nem recuperar os dados excluídos.*** Se a conta pertencer a um usuário do Livefyre Studio, alguns dados serão preservados para manter a integridade de seus registros comerciais.

         >[!IMPORTANT]
         >
         >A exclusão de dados de uma conta excluirá ou destruirá permanentemente os dados associados à conta. Não é possível reverter esta ação nem recuperar dados depois de excluí-la.

      * **Recusar**. Impede o Livefyre de coletar passivamente dados ou conteúdo de uma conta social por meio do Streams ou do Social Search. A aceitação e a não participação não se aplicam a usuários registrados
      * **Aceitar**. Reativa o Livefyre para coletar passivamente dados ou conteúdo de uma conta social que anteriormente não era incluída no Streams ou na Pesquisa Social. A aceitação e a não participação não se aplicam a usuários registrados

      ![](assets/privacypage2.png)

   * **[!UICONTROL Identifier Type]** e **[!UICONTROL Identifier]**

      * **[!UICONTROL User Account]**

         * Identifica uma conta de um usuário registrado pela ID da conta de usuário gerada pelo seu Sistema de gerenciamento de usuários ou pelo identificador de usuário do Studio do Livefyre. Você também pode localizar a ID da conta de usuário em Detalhes do usuário em **Livefyre** **Configurações do usuário** ou nos detalhes do conteúdo na **Biblioteca de ativos** ou **Conteúdo do aplicativo**

         * Valores permitidos: Sequência alfanumérica de até 255 caracteres. Um endereço de email não é uma entrada válida
      * **[!UICONTROL Facebook User]**

         * Identifica uma conta por uma ID numérica fornecida pelo Facebook. O requerente deve fornecer esta informação. Você pode encontrar instruções sobre como localizar a ID numérica do Facebook [aqui](https://www.facebook.com/help/1397933243846983?helpref=faq_content)
         * Valores permitidos: 6-16 caracteres numéricos
      * **[!UICONTROL Instagram User]**

         * Identifica a conta por uma ID numérica fornecida pelo Instagram. O requerente deve fornecer esta informação. Você pode encontrar instruções sobre como localizar a ID numérica do Instagram em uma conta do Instagram pesquisando online
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL Twitter User]**

         * Identifica uma conta por uma ID numérica fornecida pelo Twitter. A pessoa que solicita a alteração da privacidade deve fornecer isso. Você pode encontrar instruções sobre como localizar a ID numérica do Twitter para uma conta do Twitter pesquisando online
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL YouTube User]**

         * Identifica uma conta por uma ID numérica fornecida pelo YouTube. A pessoa que solicita a alteração da privacidade deve fornecer isso. Você pode encontrar instruções sobre como localizar a ID numérica do YouTube em uma conta do YouTube [aqui](https://support.google.com/youtube/answer/3250431?hl=en)
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL Generic Author]**

         * Identifica uma conta por uma ID de autor do Livefyre (JID). Use essa opção para conteúdo originado por RSS, Tumblr ou URLs. Para localizar essa ID, procure o conteúdo atribuído ao autor em **Conteúdo do aplicativo** ou **Biblioteca de ativos** e selecione um item. A ID está disponível em **Conteúdo do Aplicativo** em **Informações** ou na **Biblioteca de Ativos** em **Autor** na seção **Detalhes**

         * Valores permitidos: Sequência alfanumérica de até 255 caracteres

         ![](assets/privacypage3.png)








1. Clique em **[!UICONTROL Finish]**.

   ![](assets/privacypage4.png)

1. (Somente para solicitações de exclusão) Confirme se deseja excluir todas as informações do usuário.

   >[!IMPORTANT]
   >
   >A exclusão de dados de uma conta excluirá ou destruirá permanentemente os dados associados à conta. Não é possível reverter esta ação nem recuperar dados depois de excluí-la.

