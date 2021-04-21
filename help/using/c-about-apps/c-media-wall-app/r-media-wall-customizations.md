---
description: Altere as opções de tamanho, largura e interação do aplicativo Media Wall.
title: Personalizações do mural de mídia
exl-id: bc34d8da-9e14-4226-b38d-128889bc31cc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Personalizações do mural de mídia{#media-wall-customizations}

Altere as opções de tamanho, largura e interação do aplicativo Media Wall.



Mural de mídia transmite imagens ao vivo e outros conteúdos em um mural social em tempo real, visualizando todas as atividades ao redor de um evento.

Se estiver ativado, os usuários podem publicar texto, imagens ou vídeo diretamente neste aplicativo. Os tipos de arquivos suportados incluem:

* Imagem: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP4, MPEG, WebM
* Áudio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define o número inicial de itens de conteúdo exibidos.

* **[!UICONTROL Load content with animation.]** Ative essa opção para carregar o Mural de mídia em uma página com animação. Desative esta opção para carregar o Mural de mídia em uma página sem animação.
* **[!UICONTROL Number of columns.]** Defina o número de colunas para o Mural de mídia. O número de colunas permanece o mesmo, independentemente do tamanho da janela ou do navegador. Se você selecionar Automático, o número de colunas se ajusta para exibir um número otimizado de colunas para o tamanho da tela.
* **[!UICONTROL Fit content to width]**. Quando essa opção está desativada, o conteúdo é cortado em um quadrado. Alterne essa opção para ligada para exibir uma imagem inteira no cartão, seja ele preenche ou não o cartão inteiro.
* **[!UICONTROL Include content modal]**

   Permite que os usuários cliquem em uma foto no fluxo para abri-la em uma janela pop-up sobreposta.

* **[!UICONTROL Require rights]**. Ative essa opção para exibir somente o conteúdo com um status de solicitação de direitos de &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Ative essa opção para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos forem concedidos para um conteúdo.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Selecione se você permitirá que os usuários postem texto, foto ou vídeo com o botão de upload.
   * **[!UICONTROL Require Media]**. Alterne para para um para exigir que os usuários façam upload somente de conteúdo de foto ou vídeo usando o botão Fazer upload .
   * Você pode editar o texto padrão dos seguintes campos do Botão de upload:

      * **[!UICONTROL Upload Button Text]**. Texto para o botão Upload. O texto padrão é &quot;O que você acha?&quot;
      * **[!UICONTROL Comment Modal Title]**. O título usado pelos visitantes do site modal para publicar o conteúdo. O texto padrão é &quot;Poste seu comentário&quot;.
      * **[!UICONTROL Comment Modal Button]**. O texto do botão que os visitantes do site clicam para publicar conteúdo. O texto padrão é &quot;Poste seu comentário&quot;.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Call-to-action com um catálogo de produtos para direcionar usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne o botão para ligado para exibir o botão Chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para ligado para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de ação Chamar para o conteúdo apareça.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamar para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Call-to-action no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Call-to-action no modal de conteúdo. O texto padrão é &quot;Compre agora:&quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir a foto e o nome do produto com o botão Call-to-action .

      >[!NOTE]
      >
      >Os botões Foto e Nome do produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne o botão para ligado para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referências do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produto. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto for exibido no aplicativo, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

Você pode personalizar o Mural de mídia usando:

* **[!UICONTROL Style]** e  **[!UICONTROL Config]** opções para todos os aplicativos no  **[!UICONTROL App Designer]**. Consulte Personalização de aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte [Integração de mural de mídia](/help/implementation/c-app-integrations/c-media-wall-integration.md) para obter mais informações sobre como personalizar um mural de mídia usando as Ferramentas de integração.
