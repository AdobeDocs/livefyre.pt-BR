---
description: Gerenciamento de conteúdo na rede Livefyre.
title: Guia Conteúdo do aplicativo
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
source-git-commit: 600c9712366f5de303de27cf39045beccd4145eb
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Guia Conteúdo do aplicativo{#app-content-tab}

Gerenciamento de conteúdo na rede Livefyre.

A guia Conteúdo do aplicativo na Biblioteca permite pesquisar e moderar o conteúdo publicado nos aplicativos. O **[!UICONTROL App Content]** A guia ativa vários filtros de pesquisa com pesquisa por curinga, para permitir que você defina os parâmetros de pesquisa de forma mais rápida e fácil.

Use a guia Conteúdo do aplicativo para:

* Pesquisar conteúdo
* Visualizar histórico de conteúdo
* Conteúdo moderado
* Adicionar uma tag
* Conteúdo do recurso
* Associar conteúdo a produtos do catálogo de produtos

Para obter mais informações sobre como moderar o conteúdo usando a guia Conteúdo do aplicativo , consulte [Moderar conteúdo usando a guia Conteúdo do aplicativo](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Pesquisa curinga {#section_jvr_ntm_zz}

Os campos de pesquisa Livefyre oferecem suporte a curingas, que permitem adicionar um asterisco ( * ) às palavras (ou fragmentos de palavra) para capturar correspondências parciais.

Por exemplo:

* bola retorna somente bola
* ball* retorna bola e balão
* *bola retorna bola e futebol
* * ball* retorna bola e desliga e nevou

## Pesquisar conteúdo {#section_fw1_mtm_zz}

O painel Conteúdo do aplicativo permite restringir sua pesquisa usando várias opções diferentes de filtragem de conteúdo.

![](assets/PublishedState-1024x367.png)

Use o **[!UICONTROL Quick Filters]** menu suspenso para restringir o conteúdo retornado ao **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]** ou **[!UICONTROL Rights Requests]** status. Em seguida, selecione um **[!UICONTROL Filter by]** e use as caixas de seleção ou os campos de entrada disponíveis para limitar sua pesquisa.

Use o menu suspenso para classificar o conteúdo da lista por **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** ou **[!UICONTROL Most liked]**.

## Filtrar por opções {#section_aqn_xqm_zz}

Use o **[!UICONTROL Filter by]** barra para filtrar pelas seguintes opções:

* **Estado** Permite filtrar pelo estado de moderação atual do conteúdo:** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]** ou **[!UICONTROL Bozo]**.

* **Origem** Permite que você filtre pela fonte do conteúdo. Selecionar **[!UICONTROL Livefyre]** para listar o conteúdo gerado pelo usuário publicado diretamente no fluxo. Selecionar **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]** ou **[!UICONTROL RSS]** para incluir o conteúdo extraído de suas fontes para seus aplicativos.

* **Sinalizadores** Selecionar Sinalizadores permite filtrar por **[!UICONTROL User Flags]** (Spam, fora do tópico, ofensivo ou discordante), **[!UICONTROL System Flags]** aplicado por SAFE (Profanity, Spam ou Magically Moderated) ou **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Data/Hora** Permite filtrar por quando o conteúdo foi originalmente **[!UICONTROL Created]** (ou extraído para o aplicativo por meio do SocialSync ou de um Stream) ou por último **[!UICONTROL Modified]** (editado, sinalizado ou o estado alterado).

* **Autor** Permite que você filtre pelo **[!UICONTROL IP]** endereço, **[!UICONTROL Display Name]** (encontrado no painel Usuários ou acima do conteúdo publicado pelo autor), ou **[!UICONTROL User ID]**(localizado no painel Usuários).

* **Contém** Permite filtrar os 90 dias mais recentes de conteúdo por **[!UICONTROL Keyword]** ou **[!UICONTROL Content Tag]**. Selecione o **[!UICONTROL Media]** caixa de seleção para retornar somente o conteúdo que contém Mídia. (Para pesquisar todo o conteúdo, role para baixo até o final do conteúdo da lista e clique em **[!UICONTROL Search full data]**.)

   **Observação:** Não há suporte para várias pesquisas de palavra-chave e tag de conteúdo. Se várias palavras-chave ou tags forem inseridas, a última palavra será usada para a pesquisa.

   Ao pesquisar por Tag de conteúdo, as tags sugeridas serão preenchidas automaticamente à medida que você digita no campo de pesquisa. Os resultados da pesquisa retornarão todo o conteúdo que já recebeu a tag . (Use este campo para procurar conteúdo em destaque ou clique no link **[!UICONTROL Featured]** em qualquer conteúdo em destaque no Studio.)

   **Observação:** Use um sinal de menos (-) antes de um nome de tag para procurar conteúdo que não inclua essa tag. Por exemplo: Procure por &quot;-Miley&quot; para procurar todo o conteúdo que não inclui a tag &quot;Miley&quot;.

* **Aplicativo** Permite que você filtre por **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]** ou **ID principal**. A filtragem por ID pai retorna todo o conteúdo que é uma resposta à ID de conteúdo de entrada. (Filtre por várias tags inserindo tags separadas por vírgula.)

* **Direitos** Permite filtrar por status de Solicitações de Direitos:** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]** ou **[!UICONTROL Expired]**.

## Conteúdo do Bozo {#section_afl_vqm_zz}

Em Aplicativos, **[!UICONTROL Bozo]** o conteúdo é exibido somente para o autor do conteúdo. Isso permite que o usuário acredite que o conteúdo foi aprovado, enquanto o oculta de todos os outros usuários e moderadores.

>[!NOTE]
>
>Conteúdo social originário de SocialSync ou Fluxos **[!UICONTROL cannot]** ser definido como Bozo.

Você pode fazer o bozo do conteúdo pelos seguintes motivos:

* O conteúdo identificado como spam pelo SAFE é automaticamente definido para o estado Bozo.
* Todo o conteúdo de Usuários Banidos é automaticamente definido como Bozo.
* O conteúdo pode ser marcado como Bozo do Studio.
* Os moderadores podem fazer o bozo do conteúdo diretamente no stream.

## Visualizar histórico de conteúdo {#section_ayz_tqm_zz}

O painel de conteúdo permite revisar o histórico de todo o conteúdo listado, incluindo pré-moderação, filtragem de spam, data de publicação e quaisquer sinalizadores de usuário ou observações atribuídas ao item.

Use as guias na parte inferior do painel de conteúdo para visualizar seu histórico.

* **[!UICONTROL More Info:]** lista todas as atividades neste conteúdo, incluindo envio, edição, verificação de spam, alteração de estado e observações. A ID de conteúdo do Livefyre e o endereço IP do usuário também são exibidos nesta seção.
* **[!UICONTROL Replies:]** lista no máximo 6 respostas. Clique em **[!UICONTROL Show all replies]** para exibir todas as respostas à publicação.

* **[!UICONTROL Flags & Reports:]** lista todos os sinalizadores de usuário, com o avatar do usuário que sinalizou o conteúdo e quaisquer Relatórios (observações que foram adicionadas pelo usuário ao sinalizar o conteúdo).
* **[!UICONTROL Add a note:]** permite adicionar uma observação, visível para outros Administradores ou Moderadores.
* **[!UICONTROL Request Rights:]** abre o **[!UICONTROL New Rights Request]** , da qual uma Solicitação de direitos pode ser emitida.

* **[!UICONTROL Save as Asset:]**abre o **[!UICONTROL Advanced Options]** , que permite salvar o item selecionado em sua Biblioteca de ativos, Publicá-lo em um aplicativo ou solicitar direitos de reutilização de seu autor.

![](assets/PublishedMoreInfo-1024x462.png)

## Adicionar uma tag ao conteúdo {#section_xb4_mxr_rdb}

A marcação de conteúdo permite categorizar e organizar o conteúdo para fácil recuperação e personalização de estilos ou marcar o conteúdo como em destaque.

Para adicionar Tags, basta clicar no sinal de mais ( **[!UICONTROL +]**) em conteúdo. Insira uma nova tag ou selecione em uma lista de tags existentes.

![](assets/PublishedAddTag-1024x338.png)

## Pesquisar imagens em todos os ativos {#section_zxf_hsf_wcb}

Após adicionar o conteúdo à biblioteca, você pode pesquisar o conteúdo por tags inteligentes.

Na Biblioteca, em Todos os ativos, você pode pesquisar imagens existentes clicando em **[!UICONTROL Show Filters]** e depois:

* Inserir texto para pesquisa no campo de pesquisa
* Classificação por relevância
* Inserção de texto no **[!UICONTROL Tags]** para pesquisar por Tags inteligentes. O algoritmo de classificação de Tags inteligentes filtra o conteúdo usando uma pontuação de confiança de tag inteligente, a novidade do conteúdo e o número de estrelas que um usuário deu ao conteúdo.

## Conteúdo em destaque {#section_emb_kqm_zz}

Selecione o padrão **[!UICONTROL Featured]** para marcar o conteúdo como em destaque e destacá-lo como importante para os usuários. Depois de marcar, use as opções de estilo personalizadas para personalizar o Conteúdo em destaque nos aplicativos.

## Para Recurso ou Desrecurso de Conteúdo {#section_ojx_3qm_zz}

* No Studio, clique no botão **[!UICONTROL +]** ao lado de um conteúdo, selecione o **[!UICONTROL Featured]** na lista suspensa e clique em **[!UICONTROL Enter]** para Conteúdo em destaque. A tag será salva e exibida ao lado do conteúdo.

* Para cancelar o recurso, clique no botão **[!UICONTROL x]** no **[!UICONTROL Featured]** tag exibida no conteúdo.

* Em um Aplicativo Comentários, Blog em tempo real ou Revisões, passe o mouse sobre o conteúdo que deseja incluir e clique em **[!UICONTROL Feature]**. Para cancelar a funcionalidade, passe o mouse sobre o conteúdo e clique em **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>Devido a restrições de espaço, o conteúdo do Chat só pode ser apresentado ou não com o uso do Studio, e pode não ser apresentado dentro do próprio aplicativo.

## Edição de conteúdo em destaque {#section_pyw_hqm_zz}

As ações mais comuns em conteúdo podem ser executadas em Conteúdo em destaque, com exceção do seguinte:

* O conteúdo em destaque não pode ser sinalizado.
* Os usuários não poderão editar o conteúdo depois que ele for em destaque, embora ainda possam excluí-lo se desejarem. Os moderadores podem editar o conteúdo em destaque.
