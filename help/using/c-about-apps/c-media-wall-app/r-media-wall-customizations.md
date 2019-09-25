---
description: Altere o tamanho, a largura e as opções de interação do aplicativo Media Wall.
seo-description: Altere o tamanho, a largura e as opções de interação do aplicativo Media Wall.
seo-title: Personalizações do mural de mídia
solution: Experience Manager
title: Personalizações do mural de mídia
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizações do mural de mídia{#media-wall-customizations}

Altere o tamanho, a largura e as opções de interação do aplicativo Media Wall.



Os Media Walls fazem stream de imagens ao vivo e outros conteúdos em um mural social em tempo real, visualizando todas as atividades em torno de um evento.

Se ativado, os usuários podem publicar texto, imagens ou vídeo diretamente neste aplicativo. Os tipos de arquivos suportados incluem:

* Imagem: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP4, MPEG, WebM
* Áudio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define o número inicial de itens de conteúdo exibidos.

* **[!UICONTROL Load content with animation.]** Ative essa opção para carregar o Mídia em uma página com animação. Desative essa opção para carregar o mural de mídia em uma página sem animação.
* **[!UICONTROL Number of columns.]** Defina o número de colunas para o mural de mídia. O número de colunas permanece o mesmo, independentemente do tamanho da janela ou do navegador. Se você selecionar Automático, o número de colunas se ajusta para exibir um número otimizado de colunas para o tamanho da tela.
* **[!UICONTROL Fit content to width]**. Quando essa opção está desativada, o conteúdo é cortado em um quadrado. Alterne essa opção para ativada para exibir uma imagem inteira no cartão, independentemente de ela preencher ou não o cartão inteiro.
* **[!UICONTROL Include content modal]**

   Permite que os usuários cliquem em uma foto no fluxo para abri-la em uma janela pop-up sobreposta.

* **[!UICONTROL Require rights]**. Ative esta opção para exibir somente o conteúdo com um status de solicitação de direitos de "Concedido".
* **[!UICONTROL Hide social branding when rights granted]** Ative para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos forem concedidos para um conteúdo.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Selecione se você permitirá que os usuários publiquem texto, foto ou vídeo com o botão de upload.
   * **[!UICONTROL Require Media]**. Alterne para on para exigir que os usuários carreguem somente conteúdo de foto ou vídeo usando o botão Carregar.
   * Você pode editar o texto padrão para os seguintes campos de Botão de upload:

      * **[!UICONTROL Upload Button Text]**. Texto para o botão Carregar. O texto padrão é "O que você acha?"
      * **[!UICONTROL Comment Modal Title]**. O título para os visitantes modais do site usam para publicar conteúdo. O texto padrão é "Publicar seu comentário".
      * **[!UICONTROL Comment Modal Button]**. O texto do botão que os visitantes do site clicam para publicar o conteúdo. O texto padrão é "Publicar seu comentário".

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para ligado para exibir o botão Chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para on para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão Chamada para ação seja exibido para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamada para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamada para ação no modal de conteúdo. O texto padrão é "Compre estes produtos:".
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Chamada para ação no modal de conteúdo. O texto padrão é "Comprar agora:".
   * **[!UICONTROL Product display options]** Escolha se deseja exibir a foto e o nome do produto com o botão Chamada para ação.

      >[!NOTE]
      >
      >Os botões Foto e Nome do produto realçam azul quando ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para on para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar o rastreamento de referência do conteúdo do aplicativo para a página de produto associada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selecione essa opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produtos de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Após a exibição do conteúdo específico do produto para o aplicativo, o Livefyre exibe o conteúdo de outros produtos e o conteúdo não associado a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

Você pode personalizar o Media Wall usando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** opções para todos os aplicativos no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte Integração [do mural](/help/implementation/c-app-integrations/c-media-wall-integration.md) de mídia para obter mais informações sobre como personalizar um mural de mídia usando as Ferramentas de integração.

