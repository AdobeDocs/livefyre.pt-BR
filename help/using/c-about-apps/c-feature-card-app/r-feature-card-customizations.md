---
description: Altere as opções de tamanho, largura e interação do aplicativo Mapa.
title: Personalizações da placa de recurso
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Personalizações da placa de recurso{#feature-card-customizations}

Altere as opções de tamanho, largura e interação do aplicativo Mapa.

<!-- 
r_feature_card_customization.dita
 -->

Os aplicativos de placa de recurso incluem apenas personalizações padrão:** [!UICONTROL Theme]**, cor da marca, família de fontes e tamanho da fonte.

Você pode personalizar Cartões de recursos usando:

* **[!UICONTROL Style]** e  **[!UICONTROL Config]** opções para todos os aplicativos no  **[!UICONTROL App Designer]**. Consulte Personalização de aplicativos para obter detalhes sobre as opções padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte Integrações de aplicativos para obter mais informações sobre como personalizar aplicativos usando as Ferramentas de integração.
* **[!UICONTROL Call-to-action button]** Você pode usar o botão Call-to-action com um catálogo de produtos para direcionar usuários para um produto ou para seu site para outras ações.

   * **[!UICONTROL Call-to-action button]** Alterne o botão para ligado para exibir o botão Chamada para ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para ligado para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes que um botão de ação Chamar para o conteúdo apareça.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamar para ação não será exibido com o conteúdo, a menos que os direitos para o conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Call-to-action no modal de conteúdo. O texto padrão é &quot;Compre estes produtos:&quot;.
   * **[!UICONTROL Call-to-action button text]** Personalize o texto no botão Call-to-action . O texto padrão é, &quot;Compre agora.&quot;
   * **[!UICONTROL Product display options]** Escolha se deseja exibir o  **[!UICONTROL Photo]** e o  **[!UICONTROL Product name]** com o botão Call-to-action .
   * **[!UICONTROL Product URL referral tracking]** Alterne o botão para ligado para rastrear as referências deste aplicativo para a página de produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referências do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produto. Filtre o UGC específico do produto no aplicativo para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use `CTRL/Command + click` para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir o conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto for exibido no aplicativo, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, depois o conteúdo publicado no aplicativo com outras IDs de produto e, em seguida, o conteúdo publicado no aplicativo sem IDs de produto.
