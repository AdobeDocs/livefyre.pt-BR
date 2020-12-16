---
description: Os Conjuntos de Tradução permitem que você especifique um idioma alternativo para Aplicativos.
seo-description: Os Conjuntos de Tradução permitem que você especifique um idioma alternativo para Aplicativos.
seo-title: Conjuntos de Tradução
solution: Experience Manager
title: Conjuntos de Tradução
uuid: 8ba66a61-5520-482a-bc0b-e4f6b57f1744
translation-type: tm+mt
source-git-commit: 366b7248c2f3b6994fa10419599e66fa1c8e5e48
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 7%

---


# Conjuntos de Tradução {#translation-sets}

Os Conjuntos de Tradução permitem que você especifique um idioma alternativo para Aplicativos.

<!-- 
c_translation_sets.dita
-->

Use as configurações de tradução para localizar aplicativos em vários idiomas ou para especificar texto alternativo para vários aplicativos de um local no Studio. Por exemplo, você pode garantir que todos os sites em espanhol usem o idioma espanhol para todos os campos do aplicativo. Você também pode modificar o texto para que todos os campos correspondam à voz e ao toque do site ou da rede.

É possível especificar configurações de tradução para todos os aplicativos, exceto o Storify 2. Para obter mais informações sobre quais campos você pode localizar, consulte [Localizar strings](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Comentários, Blog ao vivo e Bate-papo compartilham o mesmo conjunto de strings em um conjunto de traduções.

Especifique um conjunto de traduções para uma rede, site, aplicativo ou usando uma API.

Os conjuntos de tradução em níveis diferentes substituem-se uns aos outros seguindo este padrão:

* O conjunto de traduções da API substitui todos os conjuntos de traduções em qualquer nível (aplicativo, rede e site)
* O conjunto de tradução do aplicativo substitui os conjuntos de tradução no nível da rede e no nível do site.
* Os conjuntos de tradução no nível do site substituem os conjuntos de tradução no nível da rede.

## Revisar sequências de texto {#c-review-text-strings}

Personalização das strings de texto para revisões do Livefyre.

Esta página lista e descreve as sequências de caracteres disponíveis para personalização em aplicativos de revisão. As strings listadas aqui são além e substituem as strings padrão para os aplicativos principais do Livefyre, listadas em Personalizações de string. Onde os duplicados são listados, as strings listadas nessas tabelas são o padrão para aplicativos de revisões.

* Implementação
* Interface de análise/classificação
* Informações de fluxo
* Informações do autor/conteúdo
* Ações do usuário
* Funções de publicação
* Erros

## Implementação {#section-vsy-1k4-xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das strings que você deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

Exemplo:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Interface de análise/classificação {#section_iyv_zj4_xz}

Strings disponíveis para a interface do usuário Revisar e Classificar.

| Elemento | Chave | Texto padrão |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Botões |  |  |
|  | editReviewBtn | Editar revisão |
|  | reviewBtn | Revisão de gravação |
|  | reviewClosed | Revisões Fechadas |
|  | showReviewBtn | Mostrar revisão |
|  | follow | Estou interessado |
|  | shareText | Acabei de escrever uma resenha. Confira! |
| Dicas de ferramentas de classificação |  |  |
|  | ratingValues | Uma matriz. Padrão = [‘Pobre’, ‘Pobre’, ‘Justo’, ‘Justo’, ‘Média’, ‘Média’, ‘Boa’, ‘Excelente’, ‘Excelente’]; |
|  |  | Observação: os valores na matriz devem ser duplicados para atribuir a metade esquerda e direita de cada estrela o mesmo nome. |
| Subpartes de classificação |  |  |
|  | ratingSubpartPlaceholder | Uma matriz. Padrão = [] |
|  | ratingSubpartTitle | Uma matriz. Padrão = [] |
|  | reviewStreamTitle | Em branco por padrão. Título da seção de resumo da revisão. |
| Misc |  |  |
|  | averageRating | Classificação média de usuário |
|  | breakHeader | Detalhamento da classificação |
|  | útil | %s de %s encontrado útil |
|  | útilPlural | %s de %s encontrado útil |
|  | outOf | / |
|  | ratingType | estrela |

## Informações de fluxo {#section_wmv_yj4_xz}

Strings disponíveis para informações e exibição do fluxo de conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Classificação* |  |  |
|  | sortBy | *Em branco por padrão.* |
|  | sortHighestRated | [Classificação mais alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Classificação mais baixa](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Mais úteis](https://d.pr/i/huTd) |
| *Stream misc.* |  |  |
|  | showMore | Mostrar mais |
| *Transmissão em alta velocidade* |  |  |
|  | newComment | Nova revisão |
|  | newComments | Novas revisões |
| *Contagem de ouvinte* |  |  |
|  | listenerCount | pessoa ouvindo |
|  | listenerCountPlural | pessoas ouvindo |
| *Contagens de comentários* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Contagem de notificador de comentários* |  |  |
|  | commentNotifier | Nova revisão |
|  | commentNotifierPlural | Novas revisões |

## Informações do autor/conteúdo {#section_osx_xj4_xz}

As strings estão disponíveis para informações de autor e conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Detalhamento de segmentos* |  |  |
|  | reviewContentNotFoundMsg | [Esta revisão não está mais visível](https://d.pr/i/svXs) |
|  | backToComments | Voltar para revisões |

## Ações do usuário {#section_tlx_wj4_xz}

Strings disponíveis para ações do usuário: marcar, compartilhar e marcar o conteúdo existente como útil.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Rodapé do comentário* |  |  |
|  | wasReviewHelpful | [Útil?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Útil? |
|  | ownwasReviewHelpful | [Achou útil.](https://d.pr/i/Q0mA) |
|  | reviewwasHelpful | [Sim](https://d.pr/i/Q0mA) |
|  | útilDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewwasNotHelpful | [Não](https://d.pr/i/Q0mA) |
| *Votação modal* |  |  |
|  | voteTitle | Esta revisão foi útil? |
|  | voteDownvote | Não |
|  | voteReplyTitle | Esta resposta foi útil? |
|  | voteTitle | Este comentário foi útil? |
|  | voteUpvote | Sim |
| *Sinalizar modal* |  |  |
|  | flagTitle | Sinalizar a revisão de %s |
|  | flagSuccessMsg | A revisão foi sinalizada. |
| *Sinalizar móvel* |  |  |
|  | flagConfirmationMessage | Sinalizar a revisão de %s como %s? |
| *Menção modal* |  |  |
|  | referenceDefaultText | Eu mencionei você em uma revisão do Livefyre! |
| *Compartilhar modal* |  |  |
|  | shareTitle | Revisão de compartilhamento |

## Funções de publicação {#section_yl1_wj4_xz}

Strings disponíveis para usuários que postam revisões.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Gravar revisão... |
|  | postEditButton | Editar   |
|  | postEditCancelButton | Cancelar |
|  | postAsButton | Publicar revisão como... |
|  | postButton | Revisão posterior |
|  | postReplyAsButton | Publicar como... |
|  | postReplyButton | Publicar |
|  | shareButton | Compartilhar |
|  | titlePlaceholder | Título… |

## Erros {#section_jbc_vj4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Erros |  |  |
|  | errorAlreadyPosted | Você só pode postar uma revisão. |
|  | errorAuthError | Você não está autorizado a postar uma revisão nesta conversa |
|  | errorCommentsNotAllowed | As revisões não podem ser publicadas no momento |
|  | errorDislikeOwnComment | Você não pode descurtir sua própria revisão |
|  | errorDuplicate | Por mais que você tenha gostado da sua revisão, não é permitido postá-la duas vezes. |
|  | errorEditDuplicate | Você deve alterar o corpo da revisão ao editá-la. |
|  | errorEditNotAllowed | Você não tem permissão para editar revisões nesta conversa. |
|  | errorEditTimeExceeded | Seu período de edição de revisão expirou. |
|  | errorEmpty | Parece que você está tentando postar uma revisão vazia. |
|  | errorEmptyTitle | Parece que você está tentando publicar um título vazio |
|  | errorFieldRating | classificação por estrelas |
|  | errorFieldReview | revisão |
|  | errorFieldTitle | title |
|  | errorMaxChars | Sua análise é muito longa. Edite e tente novamente. |
|  | errorMissingFields | Insira um |
|  | errorRatingEmpty | Não é possível enviar uma classificação vazia |
|  | errorRatingNotSet | Todas as classificações devem ser definidas |
|  | errorRatingNotValid | A classificação deve ser um objeto |
|  | errorShowMore | Erro ao carregar mais revisões. |
|  | errorTitleMaxChars | Desculpe, seu título é muito longo. Edite e tente novamente. |
|  | errorVoteOwnComment | Não pode votar na sua própria revisão |

## Indica strings de texto {#c_sidenotes_text_strings}

Personalização das strings de texto para Livefyre Sidenotes

<!-- 

c_sidenotes_text_strings.dita

 -->

Esta página lista e descreve todas as sequências de caracteres disponíveis para personalização em aplicativos Sidenotes. Para obter informações sobre strings disponíveis para os principais aplicativos Livefyre, consulte Personalizações de string.

* Implementação
* Auth
* Informações de fluxo
* Informações do autor/conteúdo
* Ações do usuário
* Funções de publicação
* Interface do moderador
* Erros

## Implementação {#section_wp2_ql4_xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das strings que você deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

Exemplo:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Autenticação {#section_pqf_3l4_xz}

Strings disponíveis para o processo de autenticação e nos menus de usuário autenticados.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Strings de menu de autenticação* |  |  |
|  | menuAuthSignInBtn | Entrar |
|  | menuAuthSignedInMsg | Você deve estar conectado a {action} |
|  | menuUserEditProfile | Editar perfil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Sair |
|  | menuUserBackBtn | Todos |

## Informações de fluxo {#section_wpy_gl4_xz}

Strings disponíveis para informações e exibição do fluxo de conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Opções do menu Informações* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Ajuda |
|  | menuInfoLivefyreLink | Visite Livefyre.com |

## Informações do autor/conteúdo {#section_dhb_gl4_xz}

As strings estão disponíveis para informações de autor e conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentCurrentTag | Pendente |
|  | commentReadMoreLink | Ler mais |
|  | commentReplyLink | Consulte {número} respostas |
|  | commentReplyLinkSing | Consulte resposta |
|  | commentVoteCount | votação |
|  | commentVoteCountSing | voto |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Uma matriz. Padrão = *[ &quot;Janeiro&quot;, &quot;fevereiro&quot;, &quot;março&quot;, &quot;abril&quot;, &quot;maio&quot;, &quot;junho&quot;, &quot;julho&quot;, &quot;agosto&quot;, &quot;setembro&quot;, &quot;outubro&quot;, &quot;novembro&quot;, &quot;dezembro&quot; ] |
|  | questionExplication | Agora você pode ler e escrever comentários diretamente em frases, parágrafos, imagens e citações. <br>Realce o texto e clique no ícone ou no ícone no final de cada parágrafo. |
|  | questionMockText | O que é &quot;conhecido familiar&quot; não é propriamente conhecido, apenas pelo fato de ser &quot;familiar&quot;. |
|  | questionTitle | O que é um Sidenote? |

## Ações do usuário {#section_qxd_fl4_xz}

Strings disponíveis para ações do usuário: marcar, compartilhar e curtir o conteúdo existente.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Opções do menu Responder* |  |  |
|  | menuRespostasExibirTítulo | Detalhes |
|  | menuRespostasExibirResponder | Responder à conversa |
| *Opções do menu Compartilhar* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuCompartilharTítulo | Compartilhar |
| *Opções do menu Sinalizar* |  |  |
|  | menuFlagOptionDisagree | Discordar |
|  | menuFlagOptionOffensive | Ofensivo |
|  | menuFlagOptionOffTopic | Tópico desativado |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Sinalizar como... |
|  | facebookShareCaption | Notas de identidade em &quot;{title}&quot; |
| *Opções do usuário móvel* |  |  |
|  | sliderCommentTally | of |
|  | sliderInviteRead | Lido |
|  | sliderInviteWrite | Gravar |
|  | sliderLoading | Carregando… |
|  | sliderWriteText | O que você acha? Toque em para escrever. |

## Funções de publicação {#section_xzf_2l4_xz}

Strings disponíveis para usuários que postam conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | editorEditBtn | Salvar |
|  | editorEditPosting | Salvando... |
|  | editorEditReplyTitle | Editar resposta |
|  | editorEditarTítulo | Editar Sidenote |
|  | editorPlaceholder | O que você acha? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Publicar |
|  | editorPostagem | Postando… |
|  | editorReplyBtn | Postar resposta |
|  | editorReplyTitle | Gravar resposta |
|  | editorTitle | Gravar nota secundária |
|  | emptyImageBlockTxt | O que você acha? |
|  | emptyTextBlockTxt | + |
|  | replyBtn | Responder |
|  | threadReplyBtn | Responder à conversa |
| *Excluir opções do menu* |  |  |
|  | menuConfirmAccept | Sim, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | Você tem certeza? |
| *Opções do menu Etc* |  |  |
|  | menuEtcOptionAprovar | Aprovar |
|  | menuEtcOptionDelete | Excluir |
|  | menuEtcOptionEdit | Editar   |
|  | menuEtcOptionFlag | Segnalato |
|  | menuEtcOptionShare | Compartilhar |
|  | menuEtcPostedAt | Publicado em {date} |
|  | menuEtcTitle | Mais |

## Interface do moderador {#section_o5f_dl4_xz}

Strings disponíveis para a interface de moderador autenticada pelo usuário.

| Elemento | Chave | Texto padrão |
|---|---|---|
| *Mensagens de confirmação do menu Mais* |  |  |
|  | notificationAprovado | Aprovado |
|  | notificationDeleted | Excluído |
|  | notificationFlagged | Sinalizado |

## Erros {#section_gtk_cl4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | errorConnection | Oh-oh. Você não parece ter uma boa conexão. |
|  | errorDuplicate | Também gostamos da sua nota, mas não é possível publicá-la duas vezes. |
|  | errorGeneral | Ocorreu um erro. Tente novamente. |
|  | errorServer | Algo deu errado com nosso servidor. Tenta de novo? |
