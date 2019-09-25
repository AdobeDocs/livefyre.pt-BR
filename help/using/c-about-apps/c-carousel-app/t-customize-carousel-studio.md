---
description: Altere o tamanho, a largura e as opções de interação do aplicativo Carrossel.
seo-description: Altere o tamanho, a largura e as opções de interação do aplicativo Carrossel.
seo-title: Personalizar um carrossel usando o Studio
solution: Experience Manager
title: Personalizar um carrossel usando o Studio
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizar um carrossel usando o Studio{#customize-a-carousel-using-studio}

Altere o tamanho, a largura e as opções de interação do aplicativo Carrossel.

Todos os aplicativos usam **[!UICONTROL Style]** e **[!UICONTROL Config]** opções no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

Você pode personalizar um carrossel usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Max Number of Items]**

   Define o número de itens a serem exibidos no carrossel. O padrão é 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Somente para telas de computador

   * Se o conteúdo for maior que 600 pixels, será exibido na horizontal
   * Se o conteúdo for menor que 600 pixels, será exibido verticalmente
   * **Vertical.** Para telas de computador ou dispositivos móveis. Em dispositivos móveis, a placa encolhe para se ajustar ao tamanho da tela.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para ligado para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para on para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de chamada para ação seja exibido para o conteúdo.
   >[!NOTE]
   >
   >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão de chamada para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se deseja exibir o botão de chamada para ação em um bloco em vez de exibir o botão de chamada para ação somente quando o visitante do site clicar em um cartão e abrir o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal de chamada para ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamada para ação no modal de conteúdo. O texto padrão é "Compre estes produtos:".
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Chamada para ação no modal de conteúdo. O texto padrão é "Comprar agora:".
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** e o **[!UICONTROL Product name]** com o botão Chamada para ação.
   >[!NOTE]
   >
   >Os botões Foto e Nome do produto realçam azul quando ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para on para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar o rastreamento de referência do conteúdo do aplicativo para a página de produto associada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione essa opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produtos de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Após a exibição do conteúdo específico do produto para o aplicativo, o Livefyre exibe o conteúdo de outros produtos e o conteúdo não associado a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.
