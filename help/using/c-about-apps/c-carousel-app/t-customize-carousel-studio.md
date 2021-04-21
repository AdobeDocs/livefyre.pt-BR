---
description: Altere as opções de tamanho, largura e interação do aplicativo Carrossel.
title: Personalizar um carrossel usando o Studio
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Personalizar um carrossel usando o Studio{#customize-a-carousel-using-studio}

Altere as opções de tamanho, largura e interação do aplicativo Carrossel.

Todos os Apps usam as opções **[!UICONTROL Style]** e **[!UICONTROL Config]** no **[!UICONTROL App Designer]**. Consulte Personalização de aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

Você pode personalizar um carrossel usando as seguintes opções adicionais no Designer de aplicativos:

* **[!UICONTROL Max Number of Items]**

   Define o número de itens a serem exibidos no carrossel. O padrão é 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Apenas para telas de computador

   * Se o conteúdo for maior que 600 pixels, será exibido horizontalmente
   * Se o conteúdo for menor que 600 pixels, será exibido verticalmente
   * **Vertical.** Para telas de computador ou dispositivos móveis. Em dispositivos móveis, a placa encolhe para caber no tamanho da tela.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Call-to-action com um catálogo de produtos para direcionar usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne o botão para ligado para exibir o botão de chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne o botão para ligado para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de chamada para ação apareça para o conteúdo.

   >[!NOTE]
   >
   >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão chamar para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se o botão de chamada para ação deve ser exibido em um bloco, em vez de exibir o botão de chamada para ação somente quando o visitante do site clicar em um cartão e abrir o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal chamar para ação.
   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Call-to-action no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Call-to-action no modal de conteúdo. O texto padrão é &quot;Compre agora:&quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o  **[!UICONTROL Photo]** e o  **[!UICONTROL Product name]** com o botão Call-to-action .

   >[!NOTE]
   >
   >Os botões Foto e Nome do produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne o botão para ligado para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referências do conteúdo do aplicativo para a página do produto associada.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produto. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto for exibido no aplicativo, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.
