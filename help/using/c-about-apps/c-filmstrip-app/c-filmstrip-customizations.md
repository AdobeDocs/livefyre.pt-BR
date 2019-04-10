---
description: null
seo-description: null
seo-title: Personalizações de película fotográfica
solution: Experience Manager
title: Personalizações de película fotográfica
uuid: 99 f 8 b 697-4 aa 3-4813-bcac-d 0 e 0 bdee 252 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personalizações de película fotográfica{#filmstrip-customizations}

Todos os **[!UICONTROL Style]** aplicativos usam **[!UICONTROL Config]** e opções no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre o padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** as opções para todos os aplicativos na **[!UICONTROL App Designer.]**

Você pode personalizar Película fotográfica usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Content fit]**. Opte **[!UICONTROL crop]** por cortar o conteúdo para preencher o cartão ou **[!UICONTROL Aspect Ratio]** para exibir uma imagem inteira no cartão, se ela preenche o cartão inteiro ou não.
* **[!UICONTROL Tile Size]**. Digite o tamanho dos blocos em pixels.
* **[!UICONTROL Show Notifications]**. Escolha se deseja exibir uma notificação para novo conteúdo à medida que ele flui para o aplicativo Película fotográfica.
* **[!UICONTROL Require rights]**. Habilite essa opção para exibir somente o conteúdo com status de solicitação de direitos de "Concedido".
* **[!UICONTROL Hide social branding when rights granted]** Alterne isso para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos são concedidos para um conteúdo.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão de chamada de ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para obter mais ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes de um botão de chamada para ação aparecer para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão de chamada de ação não será exibido com o conteúdo, a menos que os direitos do conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se o botão de chamada de ação deve ser exibido em um bloco Película fotográfica, em vez de exibir o botão de chamada de ação somente quando o visitante do site clica em um cartão e abre o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal de chamada de ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão de chamada para ação no modal de conteúdo. O texto padrão é "Loja desses produtos: ".
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão de chamada de ação no modal de conteúdo. O texto padrão é "Comprar agora: ".
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** botão **[!UICONTROL Product name]** de chamada e de chamada.

      >[!NOTE]
      >
      >Os botões de Nome de foto e de produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para para rastrear as referências deste aplicativo para a página do produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referência do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto para o aplicativo é exibido, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, em seguida, o conteúdo publicado no Aplicativo com outras IDs de produto, em seguida, o conteúdo publicado no Aplicativo sem IDs de produto.

Consulte [Opções de película fotográfica](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) para saber como personalizar uma Película fotográfica usando o Livefyre. js.

