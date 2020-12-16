---
description: 'null'
seo-description: nulo
seo-title: Personalizações de Película fotográfica
solution: Experience Manager
title: Personalizações de Película fotográfica
uuid: 99f8b697-4aa3-4813-bcac-d0e0bdee252d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---


# Personalizações de Película fotográfica{#filmstrip-customizations}

Todos os aplicativos usam as opções **[!UICONTROL Style]** e **[!UICONTROL Config]** em **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos em **[!UICONTROL App Designer.]**

Você pode personalizar Película fotográfica usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Content fit]**. Escolha **[!UICONTROL crop]** para recortar o conteúdo para preencher o cartão ou **[!UICONTROL Aspect Ratio]** para exibir uma imagem inteira no cartão, independentemente de preencher ou não o cartão inteiro.
* **[!UICONTROL Tile Size]**. Insira o tamanho dos blocos em pixels.
* **[!UICONTROL Show Notifications]**. Escolha se deseja exibir uma notificação para o novo conteúdo conforme ele é transmitido para o aplicativo Película fotográfica.
* **[!UICONTROL Require rights]**. Ative esta opção para exibir somente o conteúdo com um status de solicitação de direitos de &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Ative para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos forem concedidos para um conteúdo.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão de chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para ligado para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para on para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de chamada para ação seja exibido para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão de chamada para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se deseja exibir o botão de chamada para ação em um bloco Película fotográfica em vez de exibir o botão de chamada para ação somente quando o visitante do site clicar em um cartão e abrir o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal de chamada para ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão de chamada para ação no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão de chamada para ação no modal de conteúdo. O texto padrão é &quot;Comprar agora:&quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o  **[!UICONTROL Photo]** e o  **[!UICONTROL Product name]** com o botão de chamada para ação.

      >[!NOTE]
      >
      >Os botões Foto e Nome do produto realçam azul quando ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para on para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar o rastreamento de referência do conteúdo do aplicativo para a página de produto associada.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione essa opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select product folders]**. Selecione as pastas de produtos de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Após a exibição do conteúdo específico do produto para o aplicativo, o Livefyre exibe o conteúdo de outros produtos e o conteúdo não associado a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

Consulte [Opções de película fotográfica](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) para obter mais informações sobre como personalizar uma película fotográfica usando Livefyre.js.

