---
description: Modere o conteúdo de uma interface única e inteligente.
seo-description: Modere o conteúdo de uma interface única e inteligente.
seo-title: Moderar conteúdo usando modq
title: Moderar conteúdo usando modq
uuid: c 630 fb 85-7 bd 0-4 da 0-ac 7 e -080 e 970 fb 4 f 9
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Moderar conteúdo usando modq{#moderate-content-using-modq}

Modere o conteúdo de uma interface única e inteligente.

O modq cria uma fila em tempo real de todo o conteúdo do site ou rede que corresponde às regras de moderação que você definiu, permitindo que seus moderadores se concentrem somente no conteúdo que requer sua atenção.

Após definir as configurações modq, o novo conteúdo inserido no stream ou conteúdo existente sinalizado pelos usuários será adicionado à fila. As alterações nas regras não removerão o conteúdo da modq, mas adicionarão novo conteúdo à fila de acordo com suas novas configurações.

Modq permite:

* Modere no contexto, exiba segmentos inteiros e Aprove, Lixeira ou Bozo, ou seja partes individuais de conteúdo ou threads completos em um clique.
* Aumente a velocidade e eficiência do seu fluxo de trabalho.
* Responder o conteúdo, aumentando seu envolvimento com a comunidade.
* Permita que vários moderadores trabalhem por conteúdo, sem duplicar o trabalho de outras pessoas.

O conteúdo do Livefyre é listado em modq por até 6 semanas, e o conteúdo de streams pré-moderados que não foi abordado é listado em modq por 90 dias.

>[!NOTE]
>
>Um único conteúdo pode ser listado várias vezes se corresponder a várias regras para inclusão em modq. Por exemplo, se uma parte do conteúdo aciona uma regra de sinalizador de usuário para Ofensiva, depois aciona outra regra para Profane, ela será listada duas vezes em modq.

O conteúdo que não é exibido em modq inclui:

* Conteúdo com tendência.
* Conteúdo aprovado por um moderador.
* Conteúdo publicado por um usuário proibido ou sinalizadores de usuário aplicados por um usuário proibido.

## Navegar por modq {#section_uv4_db2_yy}

A modq é dividida em dois painéis com guias:

* **[!UICONTROL Items]** lista todo o conteúdo do Livefyre nativo e do socialsync para moderação. Esta guia inclui qualquer pesquisa social ou conteúdo de fluxo que tenha sido sinalizado ou editado após a moderação.
* **[!UICONTROL Streams Premoderation]** lista todo o conteúdo que insere seus aplicativos nos fluxos com o premoderado ativado. (Para obter mais informações, consulte Criar fluxos.)

Ambas as guias oferecem muitos dos mesmos filtros e ferramentas de moderação.

* **[!UICONTROL Item Count]** O número de itens restantes na fila é exibido no canto superior esquerdo do modq.
* **[!UICONTROL Filter]** Clique **[!UICONTROL Filter]** para definir os parâmetros pelos quais o conteúdo será listado no painel.
* **[!UICONTROL History]** Clique no **[!UICONTROL History]** botão na parte superior direita da tela para abrir uma lista do conteúdo moderado recentemente, permitindo que você revise seu trabalho ou altere uma ação recente de moderação. Clique novamente no botão para retornar ao conteúdo em fila. Somente suas 100 ações mais recentes serão exibidas. **O histórico** não lista as ações tomadas por outro moderador.

* **[!UICONTROL User Pane]** Clique nos botões Expandir ou Recolher na parte superior direita da página para abrir ou fechar o painel Usuário.

## Noções básicas sobre o conteúdo modq {#section_oxm_kgz_y1b}

Cada parte listada do conteúdo exibe informações de visualização, incluindo o site onde foi postado e seu autor. Selecionar um item exibirá todo o conteúdo incluindo qualquer mídia.

>[!NOTE]
>
>O conteúdo nativo do Livefyre exibirá mais informações que o conteúdo adicionado ao seu aplicativo por meio de fluxos ou outras fontes de redes sociais.

As seguintes informações são exibidas quando um item é selecionado:

* **[!UICONTROL Time in Queue:]** lista a quantidade de tempo que o conteúdo foi adicionado ao modq.
* **[!UICONTROL App name:]** o aplicativo em que o conteúdo aparece. Links para o site com o aplicativo.
* **[!UICONTROL Content Body:]** texto e miniatura de mídia, se disponível.
* **[!UICONTROL Status:]** o estado atual do conteúdo (Pendente, Trashed e etc.).
* **[!UICONTROL Author information:]** o nome e o nome de usuário do autor.
* **[!UICONTROL Timestamp:]** o carimbo de data e hora relativo de quando o conteúdo foi criado. Percorre o conteúdo na página Conteúdo do aplicativo do Studio.
* **[!UICONTROL Flag Type:]** Ofensiva, Discordar, Spam e etc.

   * Sinalizadores SAFE: Spam e em massa.
   * Sinalizador aplicado pela sua rede e lista de perfis do site: Profanity.
   * Sinalizadores aplicados por SAFE: Ódio, PII (Informações de identificação pessoal), Insultos e Profanity.
   * Sinalizadores do usuário: Spam, Desativado, Ofensivo e Discordar.

* **[!UICONTROL Flag origin:]** a fonte do sinalizador listado. Pode ser SAFE, um nome de usuário ou Livefyre.
* **[!UICONTROL More info:]** lista detalhes do conteúdo, incluindo o número de Curtir, Sinalizadores do usuário, Respostas e qualquer tag aplicada ao conteúdo. Clicar no site abre a página de nível superior do site no qual o conteúdo está localizado. Clicar no carimbo de data e hora abre uma exibição encadeada do conteúdo no contexto na página.

## Opções de filtro na modq {#section_r2c_qc2_yy}

Clique **[!UICONTROL Filter]** em na parte superior esquerda da janela modq para abrir um painel com opções de filtro disponíveis para conteúdo listado. À medida que você seleciona opções, a modq atualizará automaticamente para listar apenas seu conteúdo filtrado. Clique **[!UICONTROL Clear filters]** para limpar todas as opções selecionadas e recarregar a lista completa de itens.

Opções de filtro diferentes estão disponíveis para as **[!UICONTROL Items]** guias e **[!UICONTROL Streams Premoderation]** guias.

As seguintes opções estão disponíveis para a modq em **[!UICONTROL Items]** ambos os e **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**. Use o campo Pesquisar aplicativos para filtrar os resultados por Aplicativo. Vários aplicativos podem ser selecionados.
* **[!UICONTROL System Flags]**. Filtre o conteúdo por regras como Spam, Profanity, SAFE e Premoderação.

   * A seleção **[!UICONTROL Spam]** listará todo o conteúdo marcado como Spam por SAFE.
   * A seleção **[!UICONTROL Profanity]** listará todo o conteúdo marcado por Perfil por sua rede ou lista de perfis de site.
   * Selecionar **[!UICONTROL SAFE]** listará todo o conteúdo que inserirá modq como resultado de suas Regras SEGURAS.
   * A seleção **[!UICONTROL Premoderation]** listará todo o conteúdo marcado para a Pré-moderação por suas Configurações de rede, fluxo ou aplicativo.

* **[!UICONTROL User Flags]** Filtrar conteúdo por sinalizadores do usuário. As opções incluem Ofensivos, Spam, Desativado e Discordar.
* **[!UICONTROL Rights Requests.]** Exibe apenas o conteúdo com direitos concedidos clicando na caixa de seleção.
* **[!UICONTROL Entered the queue.]** Filtre o conteúdo pelo período de tempo em que o conteúdo foi enviado para modq. O conteúdo de tempo foi enviado para modq não é necessariamente o momento em que o conteúdo foi publicado no aplicativo.

As seguintes opções estão disponíveis para o modq em **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** Filtre o conteúdo pela fonte social a partir da qual o conteúdo se originou. Por exemplo, as opções de fontes sociais incluem Twitter, Instagram, Facebook e RSS.

A seguinte opção está disponível para o modq em **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**. Filtre o conteúdo pela recomendação fornecida pela Recomendação de moderação automatizada.

As imagens a seguir mostram a aparência das Recomendações de moderação em modq: ![](assets/mod_reco1.png)

A recomendação de moderação é fornecida para o conteúdo quando ela é configurada **[!UICONTROL Network Settings > Moderation]** e **[!UICONTROL Network Settings > ModQ]**.

## Ações que você pode usar em modq {#section_h4g_wrn_z1b}

Você pode decidir o que fazer com cada parte do conteúdo na modq.

Selecione uma das seguintes opções:

* O **[!UICONTROL Checkbox]** ícone para aprovar o conteúdo
* O **[!UICONTROL Trash can]** ícone para enviar o conteúdo para a lixeira
* **[!UICONTROL Request Rights]** para solicitar os direitos do conteúdo do proprietário do conteúdo.

   >[!NOTE]
   >
   >Não é possível solicitar direitos em modq para conteúdo do Instagram. Você deve usar a Biblioteca ou Conteúdo do aplicativo para enviar solicitações de direitos para o conteúdo do Instagram.

* **[!UICONTROL Feature and Approve]** para aprovar o conteúdo e também o conteúdo do conteúdo.
* **[!UICONTROL Product Tag and Approve]** para adicionar um produto do catálogo de produtos ao conteúdo e aprová-lo.
* **[!UICONTROL Mark as Pending]** para marcar o conteúdo como pendente.

>[!NOTE]
>
>Após a lixeira de um conteúdo, a parte do conteúdo e todas as respostas à parte do conteúdo são removidas de forma permanente. Para inserir um conteúdo com tendência em um aplicativo, consulte [Adicionar um item com tendência de volta em um aplicativo](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app).

Se o conteúdo já estiver no estado desejado, escolher Lixeira, Bozo ou Aprovar confirmará o estado e removerá o item da lista. A moderação de um conteúdo irá removê-la imediatamente da fila e desativá-la em relação às filas de outros moderadores.

>[!NOTE]
>
>O conteúdo de fluxo pode não ser Bozo. O conteúdo de fluxo de traço será removido do Stream permanentemente e não poderá ser desfeito.

Depois que o conteúdo for moderado, ele será removido da modq do moderador, e o autor não poderá mais editá-lo a partir do stream. Se um moderador desativar um item, ou se um usuário excluir seu comentário, ele aparecerá acinzentado nas filas de outros moderadores em tempo real. Quando o conteúdo ficou acinzentado, o **[!UICONTROL Clear Moderated]** botão é exibido na página, permitindo que os moderadores o removam das listas e mantenham seu local na página independentemente de outras atividades do moderador.

## Uso da função de lixeira em modq {#section_tpx_qgz_y1b}

Use a seção de configurações para selecionar opções disponíveis quando o conteúdo estiver marcado como Traço.

* ****[!UICONTROL Confirm Trash]**** Ative essa opção para exigir que os Moderadores confirme sua ação ao configurar o conteúdo para a Lixeira. Quando ativado, a seleção **[!UICONTROL Trash]** de conteúdo exibirá uma caixa de diálogo solicitando a um **[!UICONTROL Reason for Moderation]**e oferecendo um campo no qual a entrada **[!UICONTROL Note]** pode ser inserida.

   (Esta configuração está disponível **[!UICONTROL only]** no nível da rede e será aplicada a todos os sites na rede.)

* ****[!UICONTROL Hide Replies]**** Ative essa opção para fazer a lixeira automaticamente quando um comentário pai estiver travado ou o Bozo for d.

## Alterar status do usuário em modq {#section_tmw_lg1_z1b}

Clique no **[!UICONTROL User actions]** botão do painel Resumo do usuário para Silenciar, Proibir ou em Lista de permissões o usuário.

* **[!UICONTROL Mute:]** permite Silenciar sinalizadores do usuário que sinalizou o conteúdo listado. Use essa opção para excluir os sinalizadores do usuário dos filtros de moderação. O conteúdo que eles sinalizarão não inserirá modq como resultado do sinalizador, e seus sinalizadores não serão incluídos nas Regras de sinalização.
* **[!UICONTROL Ban:]** permite que você exclua o usuário listado do site ou rede. (Somente administradores do Studio ou Gerentes de usuário podem proibir a rede de um usuário.)
* **[!UICONTROL Whitelist:]** permite adicionar o usuário listado para o site ou rede. (Somente administradores do Studio ou Gerentes de usuário podem usar a lista de permissões de rede um usuário.)



Aplicativos que usam modq:

* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Revisões](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Auxiliares](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

