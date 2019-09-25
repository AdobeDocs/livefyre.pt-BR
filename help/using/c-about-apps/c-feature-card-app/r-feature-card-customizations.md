---
description: Altere o tamanho, a largura e as opções de interação do aplicativo Mapa.
seo-description: Altere o tamanho, a largura e as opções de interação do aplicativo Mapa.
seo-title: Personalizações da placa de recurso
solution: Experience Manager
title: Personalizações da placa de recurso
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Personalizações da placa de recurso{#feature-card-customizations}

Altere o tamanho, a largura e as opções de interação do aplicativo Mapa.

<!-- 
r_feature_card_customization.dita
 -->

Os aplicativos de placa de recurso incluem apenas personalizações padrão:*** [!UICONTROL Theme]*, cor da marca, família da fonte e tamanho da fonte.

Você pode personalizar Cartões de recurso usando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** opções para todos os aplicativos no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte Integrações de aplicativos para obter mais informações sobre como personalizar aplicativos usando as Ferramentas de integração.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamada para ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para ligado para exibir o botão Chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para on para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão Chamada para ação seja exibido para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamada para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamada para ação no modal de conteúdo. O texto padrão é "Compre estes produtos:".
   * **[!UICONTROL Call-to-action button text]** Personalize o texto no botão Chamada para ação. O texto padrão é "Compre agora".
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** e o **[!UICONTROL Product name]** com o botão Chamada para ação.
   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para on para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar o rastreamento de referência do conteúdo do aplicativo para a página de produto associada.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione essa opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produtos de nível superior a serem usadas para filtrar o UGC. Use `CTRL/Command + click` para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Após a exibição do conteúdo específico do produto para o aplicativo, o Livefyre exibe o conteúdo de outros produtos e o conteúdo não associado a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.

