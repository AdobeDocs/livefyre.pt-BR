---
title: Personalizações da faixa de filtros
description: Personalizações da faixa de filtros
exl-id: 2765699f-7adc-4b17-acfb-ef594ff65e89
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Personalizações da faixa de arquivos{#filmstrip-customizations}

Todos os Apps usam as opções **[!UICONTROL Style]** e **[!UICONTROL Config]** no **[!UICONTROL App Designer]**. Consulte Personalização de aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos em **[!UICONTROL App Designer.]**

Você pode personalizar a Tira de filme usando as seguintes opções adicionais no Designer de aplicativos:

* **[!UICONTROL Content fit]**. Escolha **[!UICONTROL crop]** para recortar o conteúdo para preencher o cartão ou **[!UICONTROL Aspect Ratio]** para exibir uma imagem inteira no cartão, seja ele preenche ou não o cartão inteiro.
* **[!UICONTROL Tile Size]**. Insira o tamanho dos blocos em pixels.
* **[!UICONTROL Show Notifications]**. Escolha se deseja exibir uma notificação para o novo conteúdo conforme ele é transmitido para o aplicativo Filmstrip.
* **[!UICONTROL Require rights]**. Ative essa opção para exibir somente o conteúdo com um status de solicitação de direitos de &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Ative essa opção para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos forem concedidos para um conteúdo.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão de chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne o botão para ligado para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne o botão para ligado para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de chamada para ação apareça para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão chamar para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se o botão de chamada para ação deve ser exibido em um bloco Filme em vez de exibir o botão de chamada para ação somente quando o visitante do site clicar em um cartão e abrir o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal chamar para ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão de chamada para ação no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão de chamada para ação no modal de conteúdo. O texto padrão é &quot;Compre agora:&quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o  **[!UICONTROL Photo]** e o  **[!UICONTROL Product name]** com o botão de chamada para ação.

      >[!NOTE]
      >
      >Os botões Foto e Nome do produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne o botão para ligado para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referências do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produto. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto for exibido no aplicativo, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

Consulte [Opções de Fita de Arquivo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) para obter mais informações sobre como personalizar uma Fita de Arquivo usando Livefyre.js.
