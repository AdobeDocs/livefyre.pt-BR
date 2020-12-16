---
description: Altere o tamanho, a largura e as opções de interação do aplicativo Mosaico.
seo-description: Altere o tamanho, a largura e as opções de interação do aplicativo Mosaico.
seo-title: Personalizações mosaicas
solution: Experience Manager
title: Personalizações mosaicas
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Personalizações do mosaico{#mosaic-customizations}

Altere o tamanho, a largura e as opções de interação do aplicativo Mosaico.

Todos os aplicativos usam as opções **[!UICONTROL Style]** e **[!UICONTROL Config]** em **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos em **[!UICONTROL App Designer.]**

Você pode personalizar o mosaico usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Content interaction]**. Define o estilo com o qual o novo conteúdo será carregado na página:

   * **[!UICONTROL Hover Fade]** para desaparecer para o outro lado de um cartão quando um visitante do site passa o mouse sobre o conteúdo.
   * **[!UICONTROL Hover Flip]** para virar para o outro lado de um cartão quando um visitante do site passa o mouse sobre o conteúdo.
   * **[!UICONTROL Click]** para exibir o outro lado de um cartão quando um visitante do site clicar no mouse sobre o conteúdo.

* **[!UICONTROL Number of Tiles to Load]**. O número de blocos a serem carregados em um mosaico. Isso pode afetar a exibição de saída. O mosaico não será exibido em uma grade, a menos que você escolha o número correto de blocos para corresponder à largura do container. Talvez seja necessário ajustá-los para que a grade seja exibida corretamente.
* **[!UICONTROL Hide social branding when rights granted]** Ative para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos forem concedidos para um conteúdo.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para ligado para exibir o botão Chamada para ação.

   * **[!UICONTROL Require rights to display products]** Alterne a alternância para on para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão Chamada para ação seja exibido para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamada para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se deseja exibir o botão de chamada para ação em um bloco Película fotográfica em vez de exibir o botão de chamada para ação somente quando o visitante do site clicar em um cartão e abrir o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal Chamada para ação.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamada para ação no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.

   * **[!UICONTROL Call-to-action button text]** Personalize o texto no botão Chamada para ação. O texto padrão é &quot;Compre agora&quot;.

   * **[!UICONTROL Product display options]** Escolha se deseja exibir o  **[!UICONTROL Photo]** e o  **[!UICONTROL Product name]** com o botão Chamada para ação.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para on para rastrear as referências deste aplicativo para a página de produto associada.

   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar o rastreamento de referência do conteúdo do aplicativo para a página de produto associada.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione essa opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produtos de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Após a exibição do conteúdo específico do produto para o aplicativo, o Livefyre exibe o conteúdo de outros produtos e o conteúdo não associado a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

Consulte [Opções de mosaico](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) para obter mais informações sobre como personalizar um mosaico usando Livefyre.js.
