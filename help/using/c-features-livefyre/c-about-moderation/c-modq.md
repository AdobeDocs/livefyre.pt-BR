---
description: Modere o conteúdo de uma interface única e inteligente.
seo-description: Modere o conteúdo de uma interface única e inteligente.
seo-title: Moderar conteúdo usando o ModQ
title: Moderar conteúdo usando o ModQ
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# Moderar conteúdo usando ModQ{#moderate-content-using-modq}

Modere o conteúdo de uma interface única e inteligente.

O ModQ cria uma fila em tempo real de todo o conteúdo do site ou da rede que corresponde às regras de pré-moderação definidas, permitindo que os moderadores se concentrem somente no conteúdo que requer atenção.

Depois de definir as configurações do ModQ, o novo conteúdo que entrar no fluxo ou o conteúdo existente sinalizado pelos usuários será adicionado à sua fila. As alterações nas regras não removerão o conteúdo do ModQ, mas adicionarão novo conteúdo à fila de acordo com as novas configurações.

O ModQ permite:

* Modere no contexto, visualização em threads inteiros e Aprovar, Lixeira ou Ocultar partes individuais de conteúdo ou threads completos em um clique.
* Aumente a velocidade e a eficiência do fluxo de trabalho.
* Responda ao conteúdo, aumentando seu envolvimento com sua comunidade.
* Permita que vários moderadores trabalhem pelo conteúdo, sem duplicar o trabalho de cada um.

O conteúdo do Livefyre é listado no ModQ por até 6 semanas, e o conteúdo de streams pré-moderados que não foi abordado é listado no ModQ por 90 dias.

>[!NOTE]
>
>Um único conteúdo pode ser listado várias vezes se corresponder a várias regras para inclusão no ModQ. Por exemplo, se um conteúdo acionar uma regra de sinalizador de usuário para Offensive e, posteriormente, acionar outra regra para o Profane, ela será listada duas vezes no ModQ.

O conteúdo que não é exibido no ModQ inclui:

* Conteúdo com lixeira.
* Conteúdo aprovado por um moderador.
* Conteúdo publicado por um usuário banido ou sinalizadores de usuário aplicados por um usuário banido.

## Navegação no ModQ {#section_uv4_db2_yy}

O ModQ é dividido em dois painéis com guias:

* **[!UICONTROL Items]** lista todo o conteúdo do Livefyre-native e do SocialSync programado para moderação. Essa guia inclui qualquer pesquisa social ou conteúdo de fluxo que tenha sido sinalizado ou editado após a moderação.
* **[!UICONTROL Streams Premoderation]** lista todo o conteúdo que entra em seus aplicativos do Streams com o Premoderate ativado. (Para obter mais informações, consulte Criação de fluxos.)

Ambas as guias oferta muitos dos mesmos filtros e ferramentas de moderação.

* **[!UICONTROL Item Count]** O número de itens restantes na fila é exibido no canto superior esquerdo do ModQ.
* **[!UICONTROL Filter]** Clique  **[!UICONTROL Filter]** para definir os parâmetros pelos quais o conteúdo será listado no painel.
* **[!UICONTROL History]** Clique no  **[!UICONTROL History]** botão na parte superior direita da tela para abrir uma lista de conteúdo moderado recentemente, permitindo que você reveja seu trabalho ou altere uma ação de moderação recente. Clique novamente no botão para retornar ao seu conteúdo na fila. Somente suas 100 ações mais recentes serão exibidas. **A** história não vai lista ações tomadas por outro moderador.

* **[!UICONTROL User Pane]** Clique nos botões expandir ou recolher na parte superior direita da página para abrir ou fechar o painel Usuário.

## Como entender o conteúdo do ModQ {#section_oxm_kgz_y1b}

Cada conteúdo listado exibe informações de pré-visualização, incluindo o site onde foi publicado e seu autor. Selecionar um item exibirá todo o conteúdo, incluindo qualquer mídia.

>[!NOTE]
>
>O conteúdo nativo do Livefyre exibirá mais informações do que o conteúdo adicionado ao seu aplicativo por meio do Streams ou de outras fontes de mídia social.

As seguintes informações são exibidas quando você seleciona um item:

* **[!UICONTROL Time in Queue:]** lista o tempo que o conteúdo foi adicionado ao ModQ.
* **[!UICONTROL App name:]** o aplicativo no qual o conteúdo é exibido. Links para o site com o aplicativo.
* **[!UICONTROL Content Body:]** miniatura de texto e mídia, se disponível.
* **[!UICONTROL Status:]** o estado atual do conteúdo (Pendente, Tracejado e etc.).
* **[!UICONTROL Author information:]** o nome do autor e o nome de usuário.
* **[!UICONTROL Timestamp:]** o carimbo de data e hora relativo de quando o conteúdo foi criado. Efetua o permalinks para o conteúdo da página Conteúdo do aplicativo do Studio.
* **[!UICONTROL Flag Type:]** Ofensivo, Discordo, Spam e etc.

   * Sinalizadores SAFE: Spam e em massa.
   * Sinalizador aplicado pela sua Lista de Profanação de Rede e Site: Profanidade.
   * Sinalizadores aplicados pela SAFE: Discurso de ódio, PII (Informações de identificação pessoal), insulto e profecia.
   * Sinalizadores do usuário: Spam, fora do tópico, Ofensivo e Discordo.

* **[!UICONTROL Flag origin:]** a origem do sinalizador listado. Pode ser SAFE, um nome de usuário ou Livefyre.
* **[!UICONTROL More info:]** Detalhes do lista para o conteúdo, incluindo o número de Curtir, Sinalizadores de usuário, Respostas e quaisquer tags aplicadas ao conteúdo. Clicar no Site abre a página de nível superior do site no qual o conteúdo está localizado. Clicar no carimbo de data e hora abre uma visualização segmentada do conteúdo no contexto da página.

## Opções de filtro no ModQ {#section_r2c_qc2_yy}

Clique em **[!UICONTROL Filter]** na parte superior esquerda da janela ModQ para abrir um painel com opções de filtro disponíveis para o conteúdo listado. À medida que você seleciona opções, o ModQ será atualizado automaticamente para lista somente do conteúdo filtrado. Clique em **[!UICONTROL Clear filters]** para apagar todas as opções selecionadas e recarregue a lista completa dos itens.

Diferentes opções de filtro estão disponíveis para as guias **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]**.

As seguintes opções estão disponíveis para o ModQ em **[!UICONTROL Items]** e **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Use o campo Pesquisar aplicativos para filtrar os resultados por aplicativo. Vários aplicativos podem ser selecionados.
* **[!UICONTROL System Flags]**. Filtre o conteúdo por regras como Spam, Profanity, SAFE e Premoderation.

   * Selecionar **[!UICONTROL Spam]** irá lista todo o conteúdo marcado como Spam pelo SAFE.
   * Selecionar **[!UICONTROL Profanity]** irá lista todo o conteúdo marcado como Profane pela sua Lista de Rede ou Profanidade do Site.
   * Selecionar **[!UICONTROL SAFE]** irá lista todo o conteúdo que entrar no ModQ como resultado das Regras SAFE.
   * Selecionar **[!UICONTROL Premoderation]** irá lista todo o conteúdo marcado para Premoderação pelas suas Configurações de rede, fluxo ou aplicativo.

* **[!UICONTROL User Flags]** Filtre o conteúdo por sinalizadores de usuário. As opções incluem Ofensivo, Spam, Off-tópico e Discordar.
* **[!UICONTROL Rights Requests.]** Exiba somente o conteúdo com direitos concedidos clicando na caixa de seleção.
* **[!UICONTROL Entered the queue.]** Filtre o conteúdo pelo período de tempo durante o qual o conteúdo foi enviado para o ModQ. O conteúdo de hora enviado para o ModQ não é necessariamente o momento em que o conteúdo foi publicado no aplicativo.

As seguintes opções estão disponíveis para o ModQ em **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre o conteúdo pela fonte social da qual o conteúdo se originou. Por exemplo, as opções de fontes sociais incluem Twitter, Instagram, Facebook e RSS.

A seguinte opção está disponível para o ModQ em **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre o conteúdo pela recomendação fornecida pela Recomendação de moderação automática.

As imagens a seguir mostram a aparência do Recommendations de moderação no ModQ:  ![](assets/mod_reco1.png)

A recomendação de moderação é fornecida para o conteúdo quando ele é configurado em **[!UICONTROL Network Settings > Moderation]** e **[!UICONTROL Network Settings > ModQ]**.

## Ações que você pode usar no ModQ {#section_h4g_wrn_z1b}

Você pode decidir o que fazer com cada parte do conteúdo no ModQ.

Selecione uma das seguintes opções:

* O ícone **[!UICONTROL Checkbox]** para aprovar o conteúdo
* O ícone **[!UICONTROL Trash can]** para enviar o conteúdo para o lixo
* **[!UICONTROL Request Rights]** para solicitar os direitos ao conteúdo do proprietário do conteúdo.

   >[!NOTE]
   >
   >Não é possível solicitar direitos no ModQ para conteúdo do Instagram. Você deve usar a Biblioteca ou o Conteúdo do aplicativo para enviar solicitações de direitos de conteúdo do Instagram.

* **[!UICONTROL Feature and Approve]** para aprovar o conteúdo e também incluir o conteúdo.
* **[!UICONTROL Product Tag and Approve]** para adicionar um produto do catálogo de produtos ao conteúdo e depois aprová-lo.
* **[!UICONTROL Mark as Pending]** para marcar o conteúdo como pendente.

>[!NOTE]
>
>Depois que você descarta um conteúdo, o conteúdo e todas as respostas ao conteúdo são removidos do ModQ permanentemente. Para colocar um conteúdo com lixeira em um aplicativo, consulte [Adicionar um item com lixeira de volta em um aplicativo](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Se o conteúdo já estiver no estado desejado, escolher Lixeira, Ocupação ou Aprovar confirmará o estado e removerá o item da lista. A moderação de um conteúdo o removerá imediatamente da sua fila e o desativará nas filas de outros moderadores.

>[!NOTE]
>
>O conteúdo de fluxo pode não ser Bozo. O conteúdo de Transmissão em sequência o removerá permanentemente do Fluxo e não poderá ser desfeito.

Depois que o conteúdo for moderado, ele será removido do ModQ do moderador e seu autor não poderá mais editá-lo no fluxo. Se um moderador rejeitar um item ou se um usuário excluir seu comentário, ele aparecerá esmaecido nas filas de outros moderadores em tempo real. Quando o conteúdo estiver acinzentado, o botão **[!UICONTROL Clear Moderated]** será exibido na página, permitindo que os moderadores o removam de suas listas e mantenham seu lugar na página independentemente de outra atividade do moderador.

## Uso da função de lixeira no ModQ {#section_tpx_qgz_y1b}

Use a seção de configurações para selecionar opções disponíveis quando o conteúdo estiver marcado como Tracejado.

* ****[!UICONTROL Confirm Trash]**** Ative essa opção para exigir que os Moderadores confirmem sua ação ao configurar o conteúdo como Lixeira. Quando ativada, selecionar **[!UICONTROL Trash]** para conteúdo exibirá uma caixa de diálogo solicitando **[!UICONTROL Reason for Moderation]** e oferta um campo no qual **[!UICONTROL Note]** poderá ser inserido.

   (Essa configuração está disponível **[!UICONTROL only]** no nível da rede e será aplicada para todos os sites em sua rede.)

* ****[!UICONTROL Hide Replies]**** Habilite essa opção para eliminar automaticamente as respostas quando um comentário pai for descartado ou se o Bozo for descartado.

## Alterar o status do usuário no ModQ {#section_tmw_lg1_z1b}

Clique no botão **[!UICONTROL User actions]** do painel Resumo do usuário para Silenciar, Banir ou Permitir listar o usuário.

* **[!UICONTROL Mute:]** permite silenciar sinalizadores do usuário que sinalizou o conteúdo listado. Use essa opção para excluir os sinalizadores do usuário dos filtros de pré-moderação. O conteúdo que eles sinalizam não entrará no ModQ como resultado do sinalizador, e seus sinalizadores não serão incluídos nas Regras de sinalizador.
* **[!UICONTROL Ban:]** permite que você proíba o usuário listado de seu site ou rede. (Somente os Administradores do Studio ou Gerentes de usuários podem proibir a rede de um usuário.)
* **[!UICONTROL Whitelist:]** permite que você permita a lista do usuário listado para seu site ou rede. (Somente os Administradores do Studio ou Gerentes de Usuário podem permitir a lista de usuários na rede.)



Aplicativos que usam o ModQ:

* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

