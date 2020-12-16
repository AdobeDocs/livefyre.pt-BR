---
description: Gerenciamento de conteúdo em sua rede Livefyre.
seo-description: Gerenciamento de conteúdo em sua rede Livefyre.
seo-title: Guia Conteúdo do aplicativo
solution: Experience Manager
title: Guia Conteúdo do aplicativo
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---


# Guia Conteúdo do aplicativo{#app-content-tab}

Gerenciamento de conteúdo em sua rede Livefyre.

A guia Conteúdo do aplicativo na Biblioteca permite que você pesquise e modere o conteúdo publicado em seus aplicativos. A guia **[!UICONTROL App Content]** permite que vários filtros de pesquisa com pesquisa curinga, a fim de permitir que você defina seus parâmetros de pesquisa de forma mais rápida e fácil.

Use a guia Conteúdo do aplicativo para:

* Procurar conteúdo
* Histórico de conteúdo da visualização
* Moderar conteúdo
* Adicionar uma tag
* Conteúdo do recurso
* Associar conteúdo a produtos do catálogo de produtos

Para obter mais informações sobre como moderar o conteúdo usando a guia Conteúdo do aplicativo, consulte [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Pesquisa curinga {#section_jvr_ntm_zz}

Os campos de pesquisa Livefyre oferecem suporte a curingas, que permitem adicionar um asterisco ( * ) a palavras (ou fragmentos de palavras) para capturar correspondências parciais.

Por exemplo:

* bola retorna apenas bola
* ball* retorna bola e balão
* *bola retorna bola e futebol
* *ball* retorna bola, despejo e nevado

## Procurar conteúdo {#section_fw1_mtm_zz}

O painel Conteúdo do aplicativo permite restringir sua pesquisa usando várias opções diferentes de filtragem de conteúdo.

![](assets/PublishedState-1024x367.png)

Use o menu suspenso **[!UICONTROL Quick Filters]** para restringir o conteúdo retornado ao status **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** ou **[!UICONTROL Rights Requests]**. Em seguida, selecione uma opção **[!UICONTROL Filter by]** e use as caixas de seleção ou os campos de entrada disponíveis para restringir sua pesquisa.

Use o menu suspenso para classificar o conteúdo na lista por **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** ou **[!UICONTROL Most liked]**.

## Filtrar por opções {#section_aqn_xqm_zz}

Use a barra **[!UICONTROL Filter by]** para filtrar pelas seguintes opções:

* **** EstadoPermite filtrar pelo estado de moderação atual do conteúdo:***  [!UICONTROL All Content]**,  **[!UICONTROL Approved]**,  **[!UICONTROL Pending]** ou  **[!UICONTROL Bozo]**.

* **** FontePermite filtrar pela origem do conteúdo. Selecione **[!UICONTROL Livefyre]** para lista o conteúdo gerado pelo usuário publicado diretamente no fluxo. Selecione **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** ou **[!UICONTROL RSS]** para incluir o conteúdo extraído para seus aplicativos a partir dessas fontes.

* **** SinalizadoresA seleção de Sinalizadores permite filtrar por  **[!UICONTROL User Flags]** (Spam, Fora do tópico, Ofensivo ou Discordo),  **[!UICONTROL System Flags]** aplicado pelo SAFE (Profanidade, Spam ou Magicamente Moderado) ou  **[!UICONTROL Moderation Recommendations]**.  ![](assets/appcontentfilter.png)

* **Data/** HoraPermite que você se ajuste quando o conteúdo foi originalmente  **[!UICONTROL Created]** (ou colocado no aplicativo por meio do SocialSync ou de um Stream), ou por último  **[!UICONTROL Modified]** (editado, sinalizado ou o estado alterado).

* **** AutorPermite filtrar pelo  **[!UICONTROL IP]** endereço do autor,  **[!UICONTROL Display Name]** (localizado no painel Usuários ou acima do conteúdo publicado pelo autor) ou  **[!UICONTROL User ID]**(encontrado no painel Usuários).

* **** ContémPermite filtrar os 90 dias mais recentes de conteúdo por  **[!UICONTROL Keyword]** ou  **[!UICONTROL Content Tag]**. Marque a caixa de seleção **[!UICONTROL Media]** para retornar somente o conteúdo que contém Mídia. (Para pesquisar por todo o conteúdo, role para baixo por todo o conteúdo da lista e clique em **[!UICONTROL Search full data]**.)

   **Observação: não há suporte para pesquisa de** várias palavras-chave e marcas de conteúdo. Se várias palavras-chave ou tags forem inseridas, a última palavra será usada para a pesquisa.

   Ao pesquisar por tag de conteúdo, as tags sugeridas serão preenchidas automaticamente à medida que você digita no campo de pesquisa. Os resultados da pesquisa retornarão todo o conteúdo que já recebeu a tag . (Use esse campo para procurar conteúdo em destaque ou clique no rótulo **[!UICONTROL Featured]** em qualquer conteúdo em destaque no Studio.)

   **Observação:** use um sinal de menos (-) antes de um nome de tag para pesquisar por conteúdo que não inclua essa tag. Por exemplo: Procure &quot;-Miley&quot; para procurar por todo o conteúdo que não inclui a tag &quot;Miley&quot;.

* **** AppPermite que você filtre por  **[!UICONTROL Collection ID]**,  **[!UICONTROL App Tag]** ou ID  **pai**. A filtragem por ID pai retorna todo o conteúdo que é uma resposta à ID de conteúdo de entrada. (Filtre por várias tags digitando tags separadas por vírgula.)

* **** DireitosPermite filtrar por status de Solicitações de direitos:**  [!UICONTROL Requested]**,  **[!UICONTROL Granted]**,  **[!UICONTROL Replied]** ou  **[!UICONTROL Expired]**.

## Conteúdo Bozo {#section_afl_vqm_zz}

Em Aplicativos, o conteúdo **[!UICONTROL Bozo]** é exibido somente para o autor do conteúdo. Isso permite que o usuário acredite que seu conteúdo foi aprovado, enquanto o oculta de todos os outros usuários e moderadores.

>[!NOTE]
>
>O conteúdo social originário do SocialSync ou do Streams **[!UICONTROL cannot]** deve ser definido como Bozo.

Você pode fazer o conteúdo do Bozo pelos seguintes motivos:

* O conteúdo identificado como Spam pelo SAFE é automaticamente definido para o estado Bozo.
* Todo o conteúdo de Usuários proibidos é automaticamente definido como Bozo.
* O conteúdo pode ser marcado como Bozo do Studio.
* Os moderadores podem fazer zoom diretamente no stream.

## Histórico de conteúdo da visualização {#section_ayz_tqm_zz}

O painel de conteúdo permite que você analise o histórico de todo o conteúdo listado, incluindo pré-moderação, filtragem de spam, data de publicação e quaisquer sinalizadores de usuário ou observações atribuídas ao item.

Use as guias na parte inferior do painel de conteúdo para visualização de seu histórico.

* **[!UICONTROL More Info:]** lista toda a atividade neste conteúdo, incluindo envio, edição, verificação de spam, alteração de estado e observações. A ID de conteúdo do Livefyre e o endereço IP do usuário também são exibidos nesta seção.
* **[!UICONTROL Replies:]** lista no máximo 6 respostas. Clique em **[!UICONTROL Show all replies]** para exibir todas as respostas à publicação.

* **[!UICONTROL Flags & Reports:]** lista todos os sinalizadores de usuário, com o avatar do usuário que sinalizou o conteúdo e quaisquer Relatórios (observações que foram adicionadas pelo usuário ao sinalizar o conteúdo).
* **[!UICONTROL Add a note:]** permite que você adicione uma nota, visível para outros Administradores ou Moderadores.
* **[!UICONTROL Request Rights:]** abre a  **[!UICONTROL New Rights Request]** caixa de diálogo, a partir da qual uma Solicitação de direitos pode ser emitida.

* **[!UICONTROL Save as Asset:]**abre a caixa de diálogo **[!UICONTROL Advanced Options]**, que permite salvar o item selecionado na sua Biblioteca de ativos, Publicá-lo em um aplicativo ou solicitar direitos de reutilização do autor.

![](assets/PublishedMoreInfo-1024x462.png)

## Adicionar uma tag ao conteúdo {#section_xb4_mxr_rdb}

A marcação de conteúdo permite que você categorize e organize o conteúdo para fácil recuperação e personalização de estilo, ou marque o conteúdo como em destaque.

Para adicionar Tags, basta clicar no ícone de adição ( **[!UICONTROL +]**) em conteúdo. Insira uma nova tag ou selecione uma lista de tags existentes.

![](assets/PublishedAddTag-1024x338.png)

## Procurando por imagens em todos os ativos {#section_zxf_hsf_wcb}

Depois de adicionar o conteúdo à biblioteca, é possível pesquisar o conteúdo por tags inteligentes.

Na Biblioteca, em Todos os ativos, você pode pesquisar imagens existentes clicando em **[!UICONTROL Show Filters]** e, em seguida:

* Inserir texto para pesquisa no campo de pesquisa
* Classificação por relevância
* Inserir texto no campo **[!UICONTROL Tags]** para pesquisar por Tags inteligentes. O algoritmo de classificação de Tags inteligentes filtros o conteúdo usando uma pontuação de confiança de tag inteligente, a novidade do conteúdo e o número de estrelas que um usuário deu ao conteúdo.

## Conteúdo em destaque {#section_emb_kqm_zz}

Selecione a tag padrão **[!UICONTROL Featured]** para marcar o conteúdo como em destaque e destaque-a como importante para seus usuários. Depois de marcados, use opções de estilização personalizadas para personalizar o Conteúdo em destaque em seus aplicativos.

## Para Recurso ou Cancelamento de Recurso do Conteúdo {#section_ojx_3qm_zz}

* No Studio, clique no sinal **[!UICONTROL +]** ao lado de um conteúdo, selecione a tag **[!UICONTROL Featured]** na lista suspensa e clique em **[!UICONTROL Enter]** para Funcionar o conteúdo. A tag será salva e exibida ao lado do conteúdo.

* Para desativar o recurso, clique em **[!UICONTROL x]** na tag **[!UICONTROL Featured]** exibida no conteúdo.

* Em um aplicativo de Comentários, Blog ao vivo ou Revisões, passe o mouse sobre o conteúdo que deseja incluir e clique em **[!UICONTROL Feature]**. Para cancelar o recurso, passe o mouse sobre o conteúdo e clique em **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>Devido a restrições de espaço, o conteúdo de bate-papo pode ser apresentado apenas ou não usando o Studio e pode não ser apresentado dentro do próprio aplicativo.

## Editar conteúdo em destaque {#section_pyw_hqm_zz}

As ações mais regulares no conteúdo podem ser realizadas no conteúdo em destaque, com exceção dos seguintes:

* O conteúdo em destaque não pode ser sinalizado.
* Os usuários não podem editar seu conteúdo depois que ele for apresentado em destaque, embora ainda possam excluí-lo se desejarem. Os moderadores podem editar o conteúdo em destaque.

