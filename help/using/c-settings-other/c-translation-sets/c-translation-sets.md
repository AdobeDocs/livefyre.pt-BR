---
description: Os Conjuntos de Tradução permitem especificar o idioma alternativo para os Aplicativos.
title: Conjuntos de tradução
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 7%

---

# Conjuntos de Tradução{#translation-sets}

Os Conjuntos de Tradução permitem especificar o idioma alternativo para os Aplicativos.

Use as configurações de tradução para localizar aplicativos em vários idiomas ou especificar texto alternativo para vários aplicativos de um local no Studio. Por exemplo, você pode garantir que todos os sites em espanhol usem o idioma espanhol em todos os campos do aplicativo. Você também pode modificar o texto para que todos os campos correspondam à voz e ao toque do site ou da rede.

É possível especificar configurações de tradução para todos os aplicativos, exceto Storify 2. Para obter mais informações sobre quais campos você pode localizar, consulte [Localizar sequências de caracteres](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Comentários, Blog ao vivo e Bate-papo compartilham o mesmo conjunto de strings em um conjunto de traduções.

Especifique um conjunto de tradução para uma rede, site, aplicativo ou usando uma API.

Os conjuntos de tradução em níveis diferentes se substituem após este padrão:

O conjunto de tradução da API substitui todos os conjuntos de tradução em qualquer nível (aplicativo, rede e site)
O conjunto de tradução do aplicativo substitui os conjuntos de tradução no nível da rede e no nível do site.
Os conjuntos de tradução no nível do site substituem os conjuntos de tradução no nível da rede.

## Revisar sequências de texto {#c_review_text_strings}

Personalização das cadeias de texto para as revisões do Livefyre.

Esta página lista e descreve as cadeias de caracteres disponíveis para personalização em aplicativos de revisão. As cadeias de caracteres listadas aqui são adicionais e substituições para as cadeias de caracteres padrão dos aplicativos principais do Livefyre, listadas em Personalizações de cadeia de caracteres. Quando duplicatas são listadas, as cadeias de caracteres listadas nessas tabelas são o padrão para aplicativos de Revisões.

Implementação
Revisar / Interface de Classificação
Informações de fluxo
Informações do autor/conteúdo
Ações do usuário
Funções de publicação
Erros

## Implementação {#section-vsy-1k4-xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das cadeias de caracteres que deseja substituir no objeto de configuração Javascript. Se um campo não for fornecido, o texto padrão será usado.

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

## Revisar / Rating Interface {#section_iyv_zj4_xz}

Cadeias de caracteres disponíveis para a interface de usuário de Revisão e Classificação .

| Elemento | Chave | Texto padrão |
|--- |--- |--- |
| Botões | editReviewBtn | Editar revisão |
|  | reviewBtn | Análise de escrita |
|  | resenhasClosed | Revisões Fechadas |
|  | showReviewBtn | Mostrar revisão |
|  | seguir | Estou interessado |
|  | shareText | Acabei de escrever uma revisão. Dê uma olhada! |
| Dicas de ferramentas de classificação | ratingValues | Uma matriz. Padrão = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Observação: Os valores na matriz devem ser duplicados para atribuir a metade esquerda e direita de cada estrela o mesmo nome. |
| Subpartes de classificação | ratingSubpartPlaceholder | Uma matriz. Padrão = [] |
|  | ratingSubparttitles | Uma matriz. Padrão = [] |
|  | reviewStreamTitle | Por padrão, em branco. Título da seção de resumo da revisão. |
| Misc | averageRating | Classificação média de usuário |
|  | breakHeader | Detalhamento da classificação |
|  | útil | %s de %s encontrado útil |
|  | útilPlural | %s de %s encontrado útil |
|  | outOf | / |
|  | ratingType | star |

## Informações de fluxo {#section_wmv_yj4_xz}

Strings disponíveis para informações e exibição do fluxo de conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Classificação | sortBy | *Por padrão, em branco.* |
|  | sortHighestRated | [Classificação mais alta](https://d.pr/i/huTd) |
|  | sortLowestRated | [Classificação mais baixa](https://d.pr/i/huTd) |
|  | sortManyHelpful | [Mais úteis](https://d.pr/i/huTd) |
| Erro de fluxo. | showMore | Mostrar mais |
| Transmitir alta velocidade | newComment | Nova revisão |
|  | newComments | Novas revisões |
| Contagens de ouvinte | listenerCount | escuta de pessoa |
|  | listenerCountPlural | pessoas ouvindo |
| Contagens de comentários | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Contagem do notificador do comentário | commentNotifier | Nova revisão |
|  | commentNotifierPlural | Novas revisões |

## Informações do autor/conteúdo {#section_osx_xj4_xz}

As sequências estão disponíveis para as informações de autor e conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Quebra de linha | resenhasContentNotFoundMsg | [Esta revisão não está mais visível](https://d.pr/i/svXs) |
|  | backToComments | Voltar para Revisões |

## Ações do usuário {#section_tlx_wj4_xz}

Cadeias de caracteres disponíveis para ações do usuário: marcar, compartilhar e marcar o conteúdo existente como útil.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Rodapé do comentário | wasReviewHelpful | [Útil?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Útil? |
|  | ownIsReviewHelpful | [Considerado útil.](https://d.pr/i/Q0mA) |
|  | reviewwasHelpful | [Sim](https://d.pr/i/Q0mA) |
|  | útilDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewIsNotHelpful | [Não](https://d.pr/i/Q0mA) |
| Modal de voto | voteTitle | Esta revisão foi útil? |
|  | votarDesfavor | Não |
|  | voteReplyTitle | Essa resposta foi útil? |
|  | voteTitle | Este comentário foi útil? |
|  | voteUpvote | Sim |
| Sinalizar modal | flagTitle | Sinalizar revisão de %s |
|  | flagSuccessMsg | A revisão foi sinalizada. |
| Sinalizar móvel | flagConfirmationMessage | Sinalizar a revisão de %s como %s? |
| Modal de menção | mentionDefaultText | Eu mencionei você em uma revisão do Livefyre! |
| Compartilhar modal | shareTitle | Análise de compartilhamento |

## Funções de publicação {#section_yl1_wj4_xz}

Cadeias de caracteres disponíveis para usuários que postaram revisões.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Editor | bodyPlaceholder | Gravar revisão... |
|  | postEditButton | Editar   |
|  | postEditCancelButton | Cancelar |
|  | postAsButton | Publicar revisão como... |
|  | postButton | Revisão da postagem |
|  | postReplyAsButton | Publicar como... |
|  | postReplyButton | Publicar |
|  | shareButton | Compartilhar |
|  | titlePlaceholder | Título… |

## Erros {#section_jbc_vj4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Erros | errorAlreadyPosted | Você só pode postar uma revisão. |
|  | errorAuthError | Você não está autorizado a postar uma revisão nesta conversa |
|  | errorCommentsNotAllowed | As revisões não podem ser publicadas no momento |
|  | errorDislikeOwnComment | Você não pode descurar sua própria revisão |
|  | errorDuplicate | Por mais que tenha gostado da sua revisão, você não tem permissão para publicá-la duas vezes. |
|  | errorEditDuplicate | Você deve alterar o corpo da revisão ao editá-la. |
|  | errorEditNotAllowed | Você não tem permissão para editar revisões nesta conversa. |
|  | errorEditTimeExceeded | Seu período de edição de revisão expirou. |
|  | errorEmpty | Parece que você está tentando postar uma revisão vazia. |
|  | errorEmptyTitle | Parece que você está tentando publicar um título vazio |
|  | errorFieldRating | avaliação de estrelas |
|  | errorFieldReview | revisão |
|  | errorFieldTitle | title |
|  | errorMaxChars | Sua revisão é muito longa. Edite e tente novamente. |
|  | errorMissingFields | Insira um |
|  | errorRatingEmpty | Não é possível enviar uma classificação vazia |
|  | errorRatingNotSet | Todas as classificações devem ser definidas |
|  | errorRatingNotValid | A classificação deve ser um objeto |
|  | errorShowMore | Erro ao carregar mais revisões. |
|  | errorTitleMaxChars | Seu título é muito longo. Edite e tente novamente. |
|  | errorVoteOwnComment | Não pode votar na sua própria revisão |

## Indica as sequências de texto {#c_sidenotes_text_strings}

Personalização das cadeias de texto para Livefyre Sidenotes

Esta página lista e descreve todas as strings disponíveis para personalização em aplicativos do Sidenotes. Para obter informações sobre cadeias de caracteres disponíveis para os aplicativos principais do Livefyre, consulte Personalizações de cadeias de caracteres .

Implementação
Auth
Informações de fluxo
Informações do autor/conteúdo
Ações do usuário
Funções de publicação
Interface do moderador
Erros

## Implementação {#section_wp2_ql4_xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das cadeias de caracteres que deseja substituir no objeto de configuração Javascript. Se um campo não for fornecido, o texto padrão será usado.

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

Strings disponíveis para o processo de autenticação e nos menus de usuário autenticado.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Cadeias de caracteres do menu de autenticação | menuAuthSignInBtn | Entrar |
|  | menuAuthSignedInMsg | Você deve estar conectado a {action} |
|  | menuUserEditProfile | Editar perfil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Sair |
|  | menuUserBackBtn | Todos |

## Informações de fluxo {#section_wpy_gl4_xz}

Strings disponíveis para informações e exibição do fluxo de conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Opções do menu Informações | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Ajuda |
|  | menuInfoLivefyreLink | Visite Livefyre.com |

## Informações do autor/conteúdo {#section_dhb_gl4_xz}

As sequências estão disponíveis para as informações de autor e conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | Pendente |
|  | commentReadMoreLink | Ler mais |
|  | commentReplyLink | Veja {número} respostas |
|  | commentReplyLinkSing | Ver resposta |
|  | commentVoteCount | votações |
|  | commentVoteCountSing | voto |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | Uma matriz. Padrão =[ &quot;Janeiro&quot;, &quot;fevereiro&quot;, &quot;março&quot;, &quot;abril&quot;, &quot;maio&quot;, &quot;junho&quot;, &quot;julho&quot;, &quot;agosto&quot;, &quot;setembro&quot;, &quot;outubro&quot;, &quot;novembro&quot;, &quot;dezembro&quot; ] |
|  | questionExplication | Agora é possível ler e escrever comentários diretamente em frases, parágrafos, imagens e aspas.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Realce o texto </span> e clique no  <span class="&rdquo;fycon-write&rdquo;"></span> ícone ou clique no  <span class="&rdquo;fycon-action-view&rdquo;"></span> ícone no final de cada parágrafo. |
|  | questionMockText | O &quot;conhecimento familiar&quot; não é bem conhecido, só pelo fato de ser &quot;familiar&quot;. |
|  | questionTitle | O que é um Sidenote? |

## Ações do usuário {#section_qxd_fl4_xz}

Cadeias de caracteres disponíveis para ações do usuário: marcar, compartilhar e curtir o conteúdo existente.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Opções do menu Responder | menuRepliesViewTitle | Detalhes |
|  | menuRepliesExibirResposta | Responder à Conversa |
| Opções do menu Compartilhar | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Compartilhar |
| Opções do menu Sinalizar | menuFlagOptionDisagree | Discordo |
|  | menuFlagOptionOffensive | Ofensiva |
|  | menuFlagOptionOffTopic | Tópico desativado |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Sinalizar como... |
|  | facebookShareCaption | Observações em &quot;{title}&quot; |
| Opções do usuário móvel | sliderCommentTally | of |
|  | sliderInviteRead | Lido |
|  | sliderInviteWrite | Gravar |
|  | sliderLoading | Carregando… |
|  | sliderWriteText | O que você acha? Toque em para gravar. |

## Funções de publicação {#section_xzf_2l4_xz}

Cadeias de caracteres disponíveis para usuários que postam conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | editorEditBtn | Salvar |
|  | editorEditPosting | Salvando... |
|  | editorEditReplyTitle | Editar resposta |
|  | editorEditTitle | Editar Sidenote |
|  | editorPlaceholder | O que você acha? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Publicar |
|  | editorPosting | Postando… |
|  | editorReplyBtn | Postar resposta |
|  | editorReplyTitle | Resposta de gravação |
|  | editorTitle | Escrever Sidenote |
|  | emptyImageBlockTxt | O que você acha? |
|  | emptyTextBlockTxt | + |
|  | replyBtn | Responder |
|  | threadReplyBtn | Responder à Conversa |
| Excluir opções do menu | menuConfirmAccept | Sim, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | Você tem certeza? |
| Opções do menu Etc | menuEtcOptionApprove | Aprovar |
|  | menuEtcOptionDelete | Excluir |
|  | menuEtcOptionEdit | Editar   |
|  | menuEtcOptionFlag | Segnalato |
|  | menuEtcOptionShare | Compartilhar |
|  | menuEtcPostedAt | Publicado em {date} |
|  | menuEtcTitle | Mais |

## Interface do moderador {#section_o5f_dl4_xz}

Cadeias de caracteres disponíveis na interface de moderador autenticada pelo usuário.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Mensagens de confirmação do menu Mais | notificationApproved | Aprovado |
|  | notificationDeleted | Excluído |
|  | notificationFlagged | Sinalizado |

## Erros {#section_gtk_cl4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | errorConnection | Ah-oh. Você não parece ter uma boa conexão. |
|  | errorDuplicate | Gostamos da sua nota também, mas você não pode publicá-la duas vezes. |
|  | errorGeneral | Ocorreu um erro. Tente novamente. |
|  | errorServer | Algo deu errado com nosso servidor. Tente isso de novo? |
