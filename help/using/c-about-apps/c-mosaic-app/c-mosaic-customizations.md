---
description: Altere as opções de tamanho, largura e interação do aplicativo Mosaic.
seo-description: Altere as opções de tamanho, largura e interação do aplicativo Mosaic.
seo-title: Personalizações de mosaico
solution: Experience Manager
title: Personalizações de mosaico
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizações de mosaico{#mosaic-customizations}

Altere as opções de tamanho, largura e interação do aplicativo Mosaic.

Todos os **[!UICONTROL Style]** aplicativos usam **[!UICONTROL Config]** e opções no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre o padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** as opções para todos os aplicativos na **[!UICONTROL App Designer.]**

Você pode personalizar Mosaico usando as seguintes opções adicionais no App Designer:

* **[!UICONTROL Content interaction]**. Define o estilo com o qual novo conteúdo será carregado na página:

   * **[!UICONTROL Hover Fade]** para desaparecer para o outro lado de um cartão quando um visitante do site passa o cursor do mouse sobre o conteúdo.
   * **[!UICONTROL Hover Flip]** para virar para o outro lado de um cartão quando um visitante do site passa o cursor do mouse sobre o conteúdo.
   * **[!UICONTROL Click]** para exibir o outro lado de um cartão quando um visitante do site clica em seu mouse sobre o conteúdo.

* **[!UICONTROL Number of Tiles to Load]**. O número de blocos para carregar em um Mosaico. Isso pode afetar a exibição da saída. O mosaico não será exibido em uma grade a menos que você escolha o número correto de blocos para corresponder à largura do contêiner. Talvez seja necessário ajustá-los para que a grade seja exibida corretamente.
* **[!UICONTROL Hide social branding when rights granted]** Alterne isso para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos são concedidos para um conteúdo.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamar a ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para obter mais ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para para exibir o botão Chamar a ação.

   * **[!UICONTROL Require rights to display products]** Alterne a alternância para para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes de um botão Chamar-a-ação aparecer para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamar a ação não será exibido com o conteúdo, a menos que os direitos do conteúdo sejam concedidos.

   * **[!UICONTROL Show call-to-action in tile]**. Escolha se o botão de chamada de ação deve ser exibido em um bloco Película fotográfica, em vez de exibir o botão de chamada de ação somente quando o visitante do site clica em um cartão e abre o conteúdo em uma janela maior.
   * **[!UICONTROL Call-to-action indication text]** O texto a ser exibido para solicitar que o usuário clique no cartão para abrir o modal de chamada de ação.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamar-para-ação no modal de conteúdo. A letra padrão é &quot;Loja desses produtos: &quot;.

   * **[!UICONTROL Call-to-action button text]** Personalize o texto no botão Chamar a ação. O texto padrão é &quot;Comprar agora&quot;.

   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** botão **[!UICONTROL Product name]** de ação de chamada e chamada.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para para rastrear as referências deste aplicativo para a página do produto associada.

   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referência do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto para o aplicativo é exibido, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, em seguida, o conteúdo publicado no Aplicativo com outras IDs de produto, em seguida, o conteúdo publicado no Aplicativo sem IDs de produto.

Consulte [Opções](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) de mosaico para saber como personalizar um Mosaico usando o Livefyre. js.
