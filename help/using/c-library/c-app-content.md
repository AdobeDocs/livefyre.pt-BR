---
description: Gerenciamento de conteúdo em sua rede Livefyre.
seo-description: Gerenciamento de conteúdo em sua rede Livefyre.
seo-title: Guia Conteúdo do aplicativo
solution: Experience Manager
title: Guia Conteúdo do aplicativo
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Guia Conteúdo do aplicativo{#app-content-tab}

Gerenciamento de conteúdo em sua rede Livefyre.

A guia Conteúdo do aplicativo na Biblioteca permite que você pesquise e modere o conteúdo publicado em seus aplicativos. A **[!UICONTROL App Content]** guia ativa vários filtros de pesquisa com pesquisa curinga, para permitir que você defina os parâmetros de pesquisa de forma mais rápida e fácil.

Use a guia Conteúdo do aplicativo para:

* Procurar conteúdo
* Exibir histórico de conteúdo
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

Use o **[!UICONTROL Quick Filters]** menu suspenso para restringir o conteúdo retornado ao **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]** ou **[!UICONTROL Pending]****[!UICONTROL Rights Requests]** status. Em seguida, selecione uma **[!UICONTROL Filter by]** opção e use as caixas de seleção ou os campos de entrada disponíveis para restringir sua pesquisa.

Use o menu suspenso para classificar o conteúdo na lista por **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]** ou **[!UICONTROL Most flags]** **[!UICONTROL Most liked]**.

## Filtrar por opções {#section_aqn_xqm_zz}

Use a **[!UICONTROL Filter by]** barra para filtrar pelas seguintes opções:

* **Estado** Permite filtrar pelo estado de moderação atual do conteúdo:*** [!UICONTROL All Content]*, **[!UICONTROL Approved]**, **[!UICONTROL Pending]** ou **[!UICONTROL Bozo]**.

* **Origem** Permite filtrar pela origem do conteúdo. Selecione **[!UICONTROL Livefyre]** para listar o conteúdo gerado pelo usuário publicado diretamente no fluxo. Selecione **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** ou **[!UICONTROL RSS]** para incluir o conteúdo extraído para seus aplicativos dessas fontes.

* **Sinalizadores** A seleção de Sinalizadores permite filtrar por **[!UICONTROL User Flags]** (Spam, Fora do tópico, Ofensivo ou Discordo), **[!UICONTROL System Flags]** aplicado pelo SAFE (Profanidade, Spam ou Magicamente Moderado) ou **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Data/hora** Permite que você se ajuste quando o conteúdo foi originalmente **[!UICONTROL Created]** (ou colocado no aplicativo por meio do SocialSync ou de um Stream) ou por último **[!UICONTROL Modified]** (editado, sinalizado ou o estado alterado).

* **Autor** Permite filtrar pelo **[!UICONTROL IP]** endereço do autor, **[!UICONTROL Display Name]** (localizado no painel Usuários ou acima do conteúdo publicado pelo autor) ou **[!UICONTROL User ID]**(encontrado no painel Usuários).

* **Contém** Permite filtrar os 90 dias mais recentes de conteúdo por **[!UICONTROL Keyword]** ou **[!UICONTROL Content Tag]**. Marque a caixa de **[!UICONTROL Media]** seleção para retornar somente o conteúdo que contém Mídia. (Para pesquisar por todo o conteúdo, role para baixo por todo o conteúdo da lista e clique em **[!UICONTROL Search full data]**.)

   **** Observação: Não há suporte para várias pesquisas de palavras-chave e marcas de conteúdo. Se várias palavras-chave ou tags forem inseridas, a última palavra será usada para a pesquisa.

   Ao pesquisar por tag de conteúdo, as tags sugeridas serão preenchidas automaticamente à medida que você digita no campo de pesquisa. Os resultados da pesquisa retornarão todo o conteúdo que já recebeu a tag . (Use esse campo para procurar conteúdo em destaque ou clique no **[!UICONTROL Featured]** rótulo de qualquer conteúdo em destaque no Studio.)

   **** Observação: Use um sinal de menos (-) antes de um nome de tag para procurar conteúdo que não inclua essa tag. Por exemplo: Procure "-Miley" para procurar por todo o conteúdo que não inclui a tag "Miley".

* **Aplicativo** Permite filtrar por **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** ou ID **pai**. A filtragem por ID pai retorna todo o conteúdo que é uma resposta à ID de conteúdo de entrada. (Filtre por várias tags digitando tags separadas por vírgula.)

* **Direitos** Permite filtrar pelo status Solicitações de direitos:** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** ou **[!UICONTROL Expired]**.

## Conteúdo Bozo {#section_afl_vqm_zz}

Em Aplicativos, **[!UICONTROL Bozo]** o conteúdo é exibido somente para o autor do conteúdo. Isso permite que o usuário acredite que seu conteúdo foi aprovado, enquanto o oculta de todos os outros usuários e moderadores.

>[!NOTE]
>
>O conteúdo social originário do SocialSync ou do Streams **[!UICONTROL cannot]** deve ser definido como Bozo.

Você pode fazer o conteúdo do Bozo pelos seguintes motivos:

* O conteúdo identificado como Spam pelo SAFE é automaticamente definido para o estado Bozo.
* Todo o conteúdo de Usuários proibidos é automaticamente definido como Bozo.
* O conteúdo pode ser marcado como Bozo do Studio.
* Os moderadores podem fazer zoom diretamente no stream.

## Exibir histórico de conteúdo {#section_ayz_tqm_zz}

O painel de conteúdo permite que você analise o histórico de todo o conteúdo listado, incluindo pré-moderação, filtragem de spam, data de publicação e quaisquer sinalizadores de usuário ou observações atribuídas ao item.

Use as guias na parte inferior do painel de conteúdo para exibir seu histórico.

* **[!UICONTROL More Info:]** lista todas as atividades neste conteúdo, incluindo envio, edição, verificação de spam, alteração de estado e observações. A ID de conteúdo do Livefyre e o endereço IP do usuário também são exibidos nesta seção.
* **[!UICONTROL Replies:]** lista um máximo de 6 respostas. Clique em **[!UICONTROL Show all replies]** para exibir todas as respostas à publicação.

* **[!UICONTROL Flags & Reports:]** lista todos os sinalizadores de usuário, com o avatar do usuário que sinalizou o conteúdo e quaisquer Relatórios (observações que foram adicionadas pelo usuário ao sinalizar o conteúdo).
* **[!UICONTROL Add a note:]** permite que você adicione uma nota, visível para outros Administradores ou Moderadores.
* **[!UICONTROL Request Rights:]** abre a **[!UICONTROL New Rights Request]** caixa de diálogo, a partir da qual uma Solicitação de direitos pode ser emitida.

* **[!UICONTROL Save as Asset:]**abre a **[!UICONTROL Advanced Options]** caixa de diálogo, que permite salvar o item selecionado na sua Biblioteca de ativos, Publicá-lo em um aplicativo ou solicitar direitos de reutilização do autor.

![](assets/PublishedMoreInfo-1024x462.png)

## Adicionar uma tag ao conteúdo {#section_xb4_mxr_rdb}

A marcação de conteúdo permite que você categorize e organize o conteúdo para fácil recuperação e personalização de estilo, ou marque o conteúdo como em destaque.

Para adicionar Tags, basta clicar no ícone de adição ( **[!UICONTROL +]**) em conteúdo. Insira uma nova tag ou selecione em uma lista de tags existentes.

![](assets/PublishedAddTag-1024x338.png)

## Procurando por imagens em todos os ativos {#section_zxf_hsf_wcb}

Depois de adicionar o conteúdo à biblioteca, é possível pesquisar o conteúdo por tags inteligentes.

Na Biblioteca, em Todos os ativos, você pode pesquisar imagens existentes clicando em **[!UICONTROL Show Filters]** e, em seguida:

* Inserir texto para pesquisa no campo de pesquisa
* Classificação por relevância
* Inserir texto no **[!UICONTROL Tags]** campo para pesquisar por Tags inteligentes. O algoritmo de classificação de Tags inteligentes filtra o conteúdo usando uma pontuação de confiança de tag inteligente, a novidade do conteúdo e o número de estrelas que um usuário deu ao conteúdo.

## Conteúdo em destaque {#section_emb_kqm_zz}

Selecione a **[!UICONTROL Featured]** tag padrão para marcar o conteúdo como em destaque e destaque-a como importante para seus usuários. Depois de marcados, use opções de estilização personalizadas para personalizar o Conteúdo em destaque em seus aplicativos.

## Para Recurso ou Cancelar Recurso de Conteúdo {#section_ojx_3qm_zz}

* No Studio, clique no **[!UICONTROL +]** sinal ao lado de um conteúdo, selecione a **[!UICONTROL Featured]** tag na lista suspensa e clique **[!UICONTROL Enter]** para Funcionar o conteúdo. A tag será salva e exibida ao lado do conteúdo.

* Para desativar o recurso, clique **[!UICONTROL x]** na **[!UICONTROL Featured]** tag exibida no conteúdo.

* Em um aplicativo de Comentários, Blog ao vivo ou Revisões, passe o mouse sobre o conteúdo que deseja incluir e clique em **[!UICONTROL Feature]**. Para cancelar o recurso, passe o mouse sobre o conteúdo e clique em **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>Devido a restrições de espaço, o conteúdo de bate-papo pode ser apresentado apenas ou não usando o Studio e pode não ser apresentado dentro do próprio aplicativo.

## Editar conteúdo em destaque {#section_pyw_hqm_zz}

As ações mais regulares no conteúdo podem ser realizadas no conteúdo em destaque, com exceção dos seguintes:

* O conteúdo em destaque não pode ser sinalizado.
* Os usuários não podem editar seu conteúdo depois que ele for apresentado em destaque, embora ainda possam excluí-lo se desejarem. Os moderadores podem editar o conteúdo em destaque.

