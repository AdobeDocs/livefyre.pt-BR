---
description: Altere as opções de tamanho, largura e interação do aplicativo Mapa.
seo-description: Altere as opções de tamanho, largura e interação do aplicativo Mapa.
seo-title: Personalizações de cartão de recursos
solution: Experience Manager
title: Personalizações de cartão de recursos
uuid: dd 43 c 076-027 f -42 c 8-be 2 e -7 d 863 d 4 e 3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Personalizações de cartão de recursos{#feature-card-customizations}

Altere as opções de tamanho, largura e interação do aplicativo Mapa.

<!-- 
r_feature_card_customization.dita
 -->

Os aplicativos de cartão de recurso incluem apenas personalizações padrão: ** [!UICONTROL Theme]**, cor da marca, família fonte e tamanho da fonte.

Você pode personalizar os Cartões de recursos usando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** opções para todos os aplicativos no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre o padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** as opções para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte Integrações do aplicativo para saber mais sobre como personalizar Aplicativos usando Ferramentas de integração.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamar a ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para obter mais ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para para exibir o botão Chamar a ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes de um botão Chamar-a-ação aparecer para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamar a ação não será exibido com o conteúdo, a menos que os direitos do conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamar-para-ação no modal de conteúdo. A letra padrão é "Loja desses produtos: ".
   * **[!UICONTROL Call-to-action button text]** Personalize o texto no botão Chamar a ação. O texto padrão é "Comprar agora".
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o **[!UICONTROL Photo]** botão **[!UICONTROL Product name]** de ação de chamada e chamada.
   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para para rastrear as referências deste aplicativo para a página do produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referência do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use `CTRL/Command + click` para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto para o aplicativo é exibido, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, em seguida, o conteúdo publicado no Aplicativo com outras IDs de produto, em seguida, o conteúdo publicado no Aplicativo sem IDs de produto.

