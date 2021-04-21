---
description: Crie uma solicitação de privacidade no Livefyre.
title: Criar uma solicitação de privacidade
exl-id: 117e1edb-becd-45f2-bfe5-12fb19ad01e0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Criar uma solicitação de privacidade{#create-a-privacy-request}

Crie uma solicitação de privacidade no Livefyre.

Exclua todos os dados de um usuário, gere um relatório de todos os dados de um usuário e faça alterações de opt-in ou opt-out usando esse processo.

Para pesquisar e localizar um usuário e gerar um relatório de seu conteúdo:

1. Vá para **[!UICONTROL Settings > Privacy]** e clique em **[!UICONTROL Create Request]**.

   ![](assets/privacypage1.png)

1. Preencha as informações na janela **[!UICONTROL Submit Request]**:

   * **[!UICONTROL Reference Id]**. Insira um identificador para usar em referência futura. Por exemplo, você pode adicionar texto, um número de tíquete, um URL, um endereço de email ou outra sequência de até 255 caracteres
   * **[!UICONTROL Type]**

      * **Acesso**. Coleta todos os dados disponíveis associados à conta. Os detalhes confidenciais, por exemplo, senhas ou credenciais sociais, serão ofuscados ou omitidos.

      * **Excluir**. Cria ou ofusca todos os dados associados à conta. **Se você escolher essa opção e clicar em Enviar, não será possível reverter ou cancelar essa ação,  *nem recuperar os dados excluídos.*** Se a conta pertencer a um usuário do Livefyre Studio, alguns dados serão preservados para manter a integridade de seus registros comerciais.

         >[!IMPORTANT]
         >
         >A exclusão de dados de uma conta excluirá ou destruirá permanentemente os dados associados à conta. Não é possível reverter essa ação nem recuperar dados depois de excluí-la.

      * **Recusar**. Impede que o Livefyre colete dados ou conteúdo de uma conta social passivamente por meio de fluxos ou pesquisa social. O opt-in e o opt-out não se aplicam a usuários registrados
      * **Opt-in**. Repermite que o Livefyre colete dados ou conteúdo passivamente de uma conta social que anteriormente optou por não participar do Streams ou da Pesquisa social. O opt-in e o opt-out não se aplicam a usuários registrados

      ![](assets/privacypage2.png)

   * **[!UICONTROL Identifier Type]** e **[!UICONTROL Identifier]**

      * **[!UICONTROL User Account]**

         * Identifica uma conta de um usuário registrado pela ID da conta de usuário gerada pelo seu sistema de gerenciamento de usuários ou pelo identificador do usuário Studio do Livefyre. Você também pode localizar a ID da conta de usuário em Detalhes do usuário no **Livefyre** **Configurações do usuário** ou nos detalhes do conteúdo na **Biblioteca de ativos** ou **Conteúdo do aplicativo**

         * Valores permitidos: Sequência alfanumérica de até 255 caracteres. Um endereço de email não é uma entrada válida
      * **[!UICONTROL Facebook User]**

         * Identifica uma conta por uma ID numérica fornecida pelo Facebook. O solicitante deve fornecer essa informação. Você pode encontrar instruções sobre como localizar a ID numérica do Facebook [aqui](https://www.facebook.com/help/1397933243846983?helpref=faq_content)
         * Valores permitidos: 6-16 caracteres numéricos
      * **[!UICONTROL Instagram User]**

         * Identifica a conta por uma ID numérica fornecida pelo Instagram. O solicitante deve fornecer essa informação. Você pode encontrar instruções sobre como localizar a Instagram ID numérica em uma conta do Instagram pesquisando online
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL Twitter User]**

         * Identifica uma conta por uma ID numérica fornecida pelo Twitter. A pessoa que solicita a alteração de privacidade deve fornecer isso. Você pode encontrar instruções sobre como localizar a Twitter ID numérica para uma conta do Twitter pesquisando online
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL YouTube User]**

         * Identifica uma conta por uma ID numérica fornecida pelo YouTube. A pessoa que solicita a alteração de privacidade deve fornecer isso. Você pode encontrar instruções sobre como localizar a YouTube ID numérica em uma conta YouTube [aqui](https://support.google.com/youtube/answer/3250431?hl=en)
         * Valores permitidos: 5-16 caracteres numéricos
      * **[!UICONTROL Generic Author]**

         * Identifica uma conta por uma ID de autor do Livefyre (JID). Use essa opção para conteúdo proveniente de RSS, Tumblr ou URLs. Para localizar essa ID, pesquise o conteúdo atribuído ao autor em **Conteúdo do aplicativo** ou **Biblioteca de ativos** e selecione um item. A ID está disponível em **Conteúdo do Aplicativo** em **Informações** ou na **Biblioteca de Ativos** em **Autor** na seção **Detalhes**

         * Valores permitidos: Sequência alfanumérica de até 255 caracteres

         ![](assets/privacypage3.png)








1. Clique em **[!UICONTROL Finish]**.

   ![](assets/privacypage4.png)

1. (Somente para solicitações de exclusão) Confirme se deseja excluir todas as informações do usuário.

   >[!IMPORTANT]
   >
   >A exclusão de dados de uma conta excluirá ou destruirá permanentemente os dados associados à conta. Não é possível reverter essa ação nem recuperar dados depois de excluí-la.
