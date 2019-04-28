---
description: Altere as opções de tamanho, largura e interação do aplicativo carrossel.
seo-description: Altere as opções de tamanho, largura e interação do aplicativo carrossel.
seo-title: Personalizar um carrossel usando o Studio
solution: Experience Manager
title: Personalizar um carrossel usando o Studio
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizar um carrossel usando o Studio{#customize-a-carousel-using-studio}

Altere as opções de tamanho, largura e interação do aplicativo carrossel.

Todos os **[!UICONTROL Style]** aplicativos usam **[!UICONTROL Config]** e opções no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre o padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** as opções para todos os aplicativos no **[!UICONTROL App Designer]**.

Você pode personalizar um carrossel usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Max Number of Items]**

   Define o número de itens a serem exibidos no carrossel. O padrão é 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Apenas para telas do computador

   * Se o conteúdo tiver mais de 600 pixels, é exibido horizontalmente
   * Se o conteúdo for menor que 600 pixels, é exibido verticalmente
   * **Vertical.** Para telas de computador ou dispositivos móveis. Em dispositivos móveis, o cartão diminui para ajustar o tamanho da tela.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamar a ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para obter mais ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes de um botão de chamada para ação aparecer para o conteúdo.
   >[!NOTE]
   >
   >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão de chamada de ação não será exibido com o conteúdo, a menos que os direitos do conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se deseja exibir o botão de chamada de ação em um bloco em vez de exibir o botão de chamada de ação somente quando o visitante do site clica em um cartão e abre o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal de chamada de ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamar-para-ação no modal de conteúdo. O texto padrão é &quot;Loja desses produtos: &quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Chamada de ação no modal de conteúdo. O texto padrão é &quot;Comprar agora: &quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** botão **[!UICONTROL Product name]** de ação de chamada e chamada.
   >[!NOTE]
   >
   >Os botões de Nome de foto e de produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para para rastrear as referências deste aplicativo para a página do produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referência do conteúdo do aplicativo para a página do produto associada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto para o aplicativo é exibido, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, em seguida, o conteúdo publicado no Aplicativo com outras IDs de produto, em seguida, o conteúdo publicado no Aplicativo sem IDs de produto.
