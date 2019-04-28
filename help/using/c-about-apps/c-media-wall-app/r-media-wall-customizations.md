---
description: Altere as opções de tamanho, largura e interação do aplicativo de Firewall.
seo-description: Altere as opções de tamanho, largura e interação do aplicativo de Firewall.
seo-title: Personalizações de parede de mídia
solution: Experience Manager
title: Personalizações de parede de mídia
uuid: 79 aasu 92-3937-4 bb 4-a 1 a 6-b 090 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Personalizações de parede de mídia{#media-wall-customizations}

Altere as opções de tamanho, largura e interação do aplicativo de Firewall.



Os caminhos de mídia são imagens ativas e outros conteúdos em um mural social em tempo real, visualizando todas as atividades em torno de um evento.

Se ativado, os usuários podem publicar texto, imagens ou vídeo diretamente neste aplicativo. Os tipos de arquivos suportados incluem:

* Imagem: JPEG, GIF, PNG
* Vídeo: Quicktime/MOV, MP 4, MPEG, webm
* Áudio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Define o número inicial de itens de conteúdo exibidos.

* **[!UICONTROL Load content with animation.]** Ative esta opção para carregar o mural de mídia em uma página com animação. Desative essa opção para carregar o mural de mídia em uma página sem animação.
* **[!UICONTROL Number of columns.]** Defina o número de colunas para o mural de mídia. O número de colunas continua a mesma, independentemente do tamanho da janela ou do navegador. Se você selecionar Automático, o número de colunas ajustará para exibir um número otimizado de colunas para o tamanho da tela.
* **[!UICONTROL Fit content to width]**. Quando essa opção estiver desativada, o conteúdo será cortado para um quadrado. Alterne essa opção para exibir uma imagem inteira no cartão, se ela preenche ou não o cartão inteiro.
* **[!UICONTROL Include content modal]**

   Permite que os usuários clicem em uma foto no stream para abri-la em uma janela pop-up sobreposta.

* **[!UICONTROL Require rights]**. Habilite essa opção para exibir somente o conteúdo com status de solicitação de direitos de &quot;Concedido&quot;.
* **[!UICONTROL Hide social branding when rights granted]** Alterne isso para remover o logotipo da rede de mídia social de origem (Twitter ou Instagram) quando os direitos são concedidos para um conteúdo.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Selecione se permitirá que os usuários postem texto, foto ou vídeo com o botão carregar.
   * **[!UICONTROL Require Media]**. Alternar para para exigir que os usuários carreguem apenas conteúdos de fotos ou vídeos usando o botão Carregar.
   * É possível editar o texto padrão para os seguintes campos de Botões de upload:

      * **[!UICONTROL Upload Button Text]**. Texto para o botão Carregar. O texto padrão é &quot;O que está pensando?&quot;
      * **[!UICONTROL Comment Modal Title]**. O título para os visitantes modal do site usam para postar conteúdo. O texto padrão é &quot;Postar seu comentário&quot;.
      * **[!UICONTROL Comment Modal Button]**. O texto dos visitantes do site do botão clica para publicar conteúdo. O texto padrão é &quot;Postar seu comentário&quot;.

* **[!UICONTROL Call-to-action button]** Você pode usar o botão Chamar a ação com um catálogo de produtos para direcionar os usuários para um produto ou para seu site para obter mais ações.

   * **[!UICONTROL Call-to-action button]** Alterne a alternância para para exibir o botão Chamar a ação.
   * **[!UICONTROL Require rights to display products]** Alterne a alternância para para exigir que o proprietário do conteúdo tenha concedido direitos para o conteúdo antes de um botão Chamar-a-ação aparecer para o conteúdo.

      >[!NOTE]
      >
      >O conteúdo é exibido mesmo se os direitos não forem concedidos para o conteúdo, mas o botão Chamar a ação não será exibido com o conteúdo, a menos que os direitos do conteúdo sejam concedidos.

   * **[!UICONTROL Call-to-action header text]** As palavras a serem exibidas no cabeçalho acima do botão Chamar-para-ação no modal de conteúdo. A letra padrão é &quot;Loja desses produtos: &quot;.
   * **[!UICONTROL Call-to-action button text]** As palavras a serem exibidas no botão Chamada de ação no modal de conteúdo. O texto padrão é &quot;Comprar agora: &quot;.
   * **[!UICONTROL Product display options]** Escolha se deseja exibir a foto e o nome do produto com o botão Chamar-to-action.

      >[!NOTE]
      >
      >Os botões de Nome de foto e de produto destacam azul quando estão ativados.

   * **[!UICONTROL Product URL referral tracking]** Alterne a alternância para para rastrear as referências deste aplicativo para a página do produto associada.
   * **[!UICONTROL Referral tracking key-value pairs]** Adicione parâmetros para especificar ainda mais o rastreamento de referência do conteúdo do aplicativo para a página do produto associada.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Selecione esta opção para criar um aplicativo para várias páginas de produtos. Filtre o UGC específico do produto para cada página de produto. Você pode selecionar uma ou mais pastas para associar coleções específicas ao aplicativo.
   * **[!UICONTROL Select Product folders]**. Selecione as pastas de produto de nível superior a serem usadas para filtrar o UGC. Use CTRL/Command + clique para selecionar mais de uma pasta. O Livefyre usa a pasta para determinar quais produtos nessa pasta serão exibidos no aplicativo em várias páginas.
   * **[!UICONTROL Show related content]**. Alterne isso para exibir conteúdo publicado no aplicativo, mas marcado com uma ID de produto diferente. Depois que o conteúdo específico do produto para o aplicativo é exibido, o Livefyre exibe o conteúdo de outros produtos e conteúdo não associados a um produto. O Livefyre prioriza o conteúdo com a mesma ID de produto primeiro, em seguida, o conteúdo publicado no Aplicativo com outras IDs de produto, em seguida, o conteúdo publicado no Aplicativo sem IDs de produto.

Você pode personalizar o Media Wall usando:

* **[!UICONTROL Style]** e **[!UICONTROL Config]** opções para todos os aplicativos no **[!UICONTROL App Designer]**. Consulte Personalizar aplicativos para obter detalhes sobre o padrão **[!UICONTROL Style]** e **[!UICONTROL Config]** as opções para todos os aplicativos no **[!UICONTROL App Designer]**.

* Ferramentas de integração. Consulte [Integração de mural de mídia](/help/implementation/c-app-integrations/c-media-wall-integration.md) para saber como personalizar um mural de mídia usando Ferramentas de integração.

