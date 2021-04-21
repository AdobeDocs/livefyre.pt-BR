---
description: Modere conteúdo em uma única interface inteligente.
title: Moderar conteúdo usando ModQ
exl-id: 694b1f45-2b24-4e80-99a1-788e2cecc8a4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1454'
ht-degree: 0%

---

# Moderar conteúdo usando ModQ{#moderate-content-using-modq}

Modere conteúdo em uma única interface inteligente.

O ModQ cria uma fila em tempo real de todo o conteúdo do site ou da rede que corresponde às regras de pré-moderação definidas, permitindo que os moderadores se concentrem somente no conteúdo que requer a atenção deles.

Após definir as configurações do ModQ, o novo conteúdo que entra no fluxo ou o conteúdo existente sinalizado por seus usuários serão adicionados à fila. As alterações nas regras não removerão o conteúdo do ModQ, mas adicionarão novo conteúdo à fila de acordo com suas novas configurações.

O ModQ permite:

* Modere no contexto, visualize threads inteiros e Aprove, Lixeira ou Bozo em partes individuais do conteúdo ou em threads completos em um clique.
* Aumente a velocidade e a eficiência do seu fluxo de trabalho.
* Responda ao conteúdo, aumentando seu envolvimento com sua comunidade.
* Permitir que vários moderadores trabalhem pelo conteúdo, sem duplicar o trabalho uns dos outros.

O conteúdo do Livefyre é listado no ModQ por até 6 semanas, e o conteúdo dos fluxos pré-moderados que não foi abordado é listado no ModQ por 90 dias.

>[!NOTE]
>
>Um único conteúdo pode ser listado várias vezes se corresponder a várias regras para inclusão no ModQ. Por exemplo, se um conteúdo acionar uma regra de sinalizador de usuário para Ofensivo e, posteriormente, acionar outra regra para Perfil, ele será listado duas vezes no ModQ.

O conteúdo que não é exibido no ModQ inclui:

* Conteúdo enviado para a lixeira.
* Conteúdo aprovado por um moderador.
* Conteúdo publicado por um usuário proibido ou sinalizadores de usuário aplicados por um usuário proibido.

## Navegando no ModQ {#section_uv4_db2_yy}

O ModQ é dividido em dois painéis com guias:

* **[!UICONTROL Items]** lista todo o conteúdo nativo do Livefyre e do SocialSync relacionado à moderação. Esta guia inclui qualquer conteúdo de Pesquisa social ou Fluxo que tenha sido sinalizado ou editado após a moderação.
* **[!UICONTROL Streams Premoderation]** lista todo o conteúdo que entra em seus aplicativos por meio de fluxos com o recurso Premoderate ativado. (Para obter mais informações, consulte Criação de fluxos.)

Ambas as guias oferecem muitos dos mesmos filtros e ferramentas de moderação.

* **[!UICONTROL Item Count]** O número de itens restantes na fila é exibido no canto superior esquerdo do ModQ.
* **[!UICONTROL Filter]** Clique em  **[!UICONTROL Filter]** para definir parâmetros pelos quais o conteúdo será listado no painel.
* **[!UICONTROL History]** Clique no  **[!UICONTROL History]** botão na parte superior direita da tela para abrir uma lista de conteúdos moderados recentemente, permitindo que você revise seu trabalho ou altere uma ação de moderação recente. Clique no botão novamente para retornar ao conteúdo em fila. Somente suas 100 ações mais recentes serão exibidas. **** O histórico não listará as ações executadas por outro moderador.

* **[!UICONTROL User Pane]** Clique nos botões expandir ou recolher na parte superior direita da página para abrir ou fechar o painel Usuário.

## Como entender o conteúdo do ModQ {#section_oxm_kgz_y1b}

Cada conteúdo listado exibe informações de visualização, incluindo o site em que foi postado e seu autor. Selecionar um item exibirá todo o conteúdo, incluindo qualquer mídia.

>[!NOTE]
>
>O conteúdo nativo do Livefyre exibirá mais informações do que o conteúdo adicionado ao seu aplicativo por meio de fluxos ou outras fontes de mídia social.

As seguintes informações são exibidas ao selecionar um item:

* **[!UICONTROL Time in Queue:]** lista o tempo em que o conteúdo foi adicionado ao ModQ.
* **[!UICONTROL App name:]** o aplicativo no qual o conteúdo é exibido. Links para o site com o aplicativo.
* **[!UICONTROL Content Body:]** miniatura de texto e mídia, se disponível.
* **[!UICONTROL Status:]** o estado atual do conteúdo (Pendente, Lixeira, etc.).
* **[!UICONTROL Author information:]** o nome e nome de usuário do autor.
* **[!UICONTROL Timestamp:]** o carimbo de data e hora relativo de quando o conteúdo foi criado. Efetua o Permalinks ao conteúdo da página de Conteúdo do Aplicativo do Studio.
* **[!UICONTROL Flag Type:]** Ofensivo, Discordo, Spam e etc.

   * Sinalizadores SAFE: Spam e em massa.
   * Sinalizador aplicado pela sua Lista de Persistência de Rede e Site: Profanação.
   * Sinalizadores aplicados pelo SAFE: Discurso do ódio, PII (Informações de identificação pessoal), Insulto e Profanação.
   * Sinalizadores de usuário: Spam, fora do tópico, ofensivo e discordante.

* **[!UICONTROL Flag origin:]** a origem do sinalizador listado. Pode ser SAFE, nome de usuário ou Livefyre.
* **[!UICONTROL More info:]** lista detalhes do conteúdo, incluindo o número de opções Curtir, Sinalizadores de usuário, Respostas e quaisquer tags aplicadas ao conteúdo. Clicar no Site abre a página de nível superior do site em que o conteúdo está localizado. Clicar no carimbo de data e hora abre uma visualização segmentada do conteúdo no contexto da página.

## Opções de filtro no ModQ {#section_r2c_qc2_yy}

Clique em **[!UICONTROL Filter]** no canto superior esquerdo da janela do ModQ para abrir um painel com opções de filtro disponíveis para o conteúdo listado. À medida que você seleciona opções, o ModQ será atualizado automaticamente para listar somente o conteúdo filtrado. Clique em **[!UICONTROL Clear filters]** para limpar todas as opções selecionadas e recarregue a lista completa de itens.

Diferentes opções de filtro estão disponíveis para as guias **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]** .

As seguintes opções estão disponíveis para o ModQ em **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Use o campo Pesquisar aplicativos para filtrar os resultados por aplicativo. Vários aplicativos podem ser selecionados.
* **[!UICONTROL System Flags]**. Filtre o conteúdo por regras como Spam, Profanidade, SAFE e Premoderation.

   * Selecionar **[!UICONTROL Spam]** listará todo o conteúdo marcado como Spam pelo SAFE.
   * Selecionar **[!UICONTROL Profanity]** listará todos os perfis de conteúdo marcados pela sua Lista de Perfil de Rede ou de Site.
   * Selecionar **[!UICONTROL SAFE]** listará todo o conteúdo que entra no ModQ como resultado das Regras SAFE.
   * Selecionar **[!UICONTROL Premoderation]** listará todo o conteúdo marcado para Premoderação por suas Configurações de rede, fluxo ou aplicativo.

* **[!UICONTROL User Flags]** Filtre o conteúdo por sinalizadores de usuário. As opções incluem Ofensivo, Spam, Off-topic e Discordo.
* **[!UICONTROL Rights Requests.]** Exiba somente o conteúdo com direitos concedidos clicando na caixa de seleção .
* **[!UICONTROL Entered the queue.]** Filtre o conteúdo pelo período durante o qual o conteúdo foi enviado para o ModQ. O horário em que o conteúdo foi enviado para o ModQ não é necessariamente o horário em que o conteúdo foi publicado no aplicativo.

As seguintes opções estão disponíveis para o ModQ em **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre o conteúdo pela fonte social da qual o conteúdo se originou. Por exemplo, as opções de fontes sociais incluem Twitter, Instagram, Facebook e RSS.

A seguinte opção está disponível para o ModQ em **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre o conteúdo de acordo com a recomendação fornecida pela Recomendação de moderação automatizada.

As imagens a seguir mostram a aparência da Moderação do Recommendations no ModQ:  ![](assets/mod_reco1.png)

A recomendação de moderação é fornecida para o conteúdo quando ele é configurado em **[!UICONTROL Network Settings > Moderation]** e **[!UICONTROL Network Settings > ModQ]**.

## Ações que podem ser usadas no ModQ {#section_h4g_wrn_z1b}

Você pode decidir o que fazer com cada parte do conteúdo no ModQ.

Selecione uma das seguintes opções:

* O ícone **[!UICONTROL Checkbox]** para aprovar o conteúdo
* O ícone **[!UICONTROL Trash can]** para enviar o conteúdo para a lixeira
* **[!UICONTROL Request Rights]** para solicitar os direitos ao conteúdo do proprietário do conteúdo.

   >[!NOTE]
   >
   >Não é possível solicitar direitos no ModQ para conteúdo do Instagram. Você deve usar a Biblioteca ou o Conteúdo do aplicativo para enviar solicitações de direitos de conteúdo do Instagram.

* **[!UICONTROL Feature and Approve]** para aprovar o conteúdo e também incluir a parte de conteúdo.
* **[!UICONTROL Product Tag and Approve]** para adicionar um produto do catálogo de produtos ao conteúdo e depois aprová-lo.
* **[!UICONTROL Mark as Pending]** para marcar o conteúdo como pendente.

>[!NOTE]
>
>Depois de enviar um conteúdo para a lixeira, o conteúdo e todas as respostas ao conteúdo são removidos do ModQ permanentemente. Para colocar um conteúdo enviado para a lixeira em um aplicativo, consulte [Adicionar um item enviado para a lixeira de volta em um aplicativo](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Se o conteúdo já estiver no estado desejado, escolher Lixeira, Ozo ou Aprovar confirmará o estado e removerá o item da lista. A moderação de um conteúdo imediatamente o removerá de sua fila e o desativará em outras filas de moderadores.

>[!NOTE]
>
>O conteúdo de fluxo pode não ser Bozo’d. O conteúdo do Stream de Transmissão o removerá permanentemente do Stream e não poderá ser desfeito.

Depois que o conteúdo for moderado, ele será removido do ModQ do moderador e seu autor não poderá mais editá-lo no stream. Se um moderador rejeitar um item ou se um usuário excluir seu comentário, ele aparecerá esmaecido nas filas de outros moderadores em tempo real. Quando o conteúdo é esmaecido, o botão **[!UICONTROL Clear Moderated]** é exibido na página, permitindo que os moderadores o removam de suas listas e mantenham seu lugar na página independentemente de outra atividade do moderador.

## Uso da função Lixeira no ModQ {#section_tpx_qgz_y1b}

Use a seção de configurações para selecionar as opções disponíveis quando o conteúdo for marcado como Lixeira.

* ****[!UICONTROL Confirm Trash]**** Ative essa opção para exigir que os Moderadores confirmem a ação ao definir o conteúdo para Lixeira. Quando ativado, selecionar **[!UICONTROL Trash]** para conteúdo exibirá uma caixa de diálogo solicitando um **[!UICONTROL Reason for Moderation]** e oferecerá um campo no qual **[!UICONTROL Note]** poderá ser inserido.

   (Essa configuração está disponível **[!UICONTROL only]** no nível da rede e será aplicada para todos os sites em sua rede.)

* ****[!UICONTROL Hide Replies]**** Ative essa opção para enviar automaticamente respostas para a lixeira quando um comentário pai for enviado para a lixeira ou para o Bozo’d.

## Alterar o status do usuário no ModQ {#section_tmw_lg1_z1b}

Clique no botão **[!UICONTROL User actions]** do painel Resumo do usuário para Mudo, Banir ou Permitir o acesso do usuário à lista de permissões.

* **[!UICONTROL Mute:]** permite desativar a função Mudo de sinalizadores do usuário que sinalizou o conteúdo listado. Use esta opção para excluir os sinalizadores do usuário de seus filtros de pré-moderação. O conteúdo que eles sinalizarem não entrará no ModQ como resultado do sinalizador, e seus sinalizadores não serão incluídos nas Regras de sinalizador.
* **[!UICONTROL Ban:]** permite que você exclua o usuário listado de seu site ou rede. (Somente Administradores do Studio ou Gerentes de Usuário podem proibir em rede um usuário.)
* **[!UICONTROL Whitelist:]** permite que você inclua na lista de permissões o usuário listado do seu site ou rede. (Somente Administradores do Studio ou Gerentes de usuários podem colocar na lista de permissões de rede um usuário.)



Aplicativos que usam ModQ:

* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Observações](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
