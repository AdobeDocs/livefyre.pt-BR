---
description: Personalização das cadeias de texto para as revisões do Livefyre.
title: Rever cadeias de texto
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# Rever cadeias de texto{#review-text-strings}

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

## Revisar / Interface de Classificação {#section_iyv_zj4_xz}

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
| Subpartes de classificação | ratingSubpartPlaceholder | Uma matriz. Padrão = `[]` |
|  | ratingSubparttitles | Uma matriz. Padrão = `[]` |
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
| Classificação | sortBy | Por padrão, em branco. |
|  | sortHighestRated | Classificação mais alta |
|  | sortLowestRated | Classificação mais baixa |
|  | sortManyHelpful | Mais úteis |
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
| Quebra de linha | resenhasContentNotFoundMsg | Esta revisão não está mais visível |
|  | backToComments | Voltar para Revisões |

## Ações do usuário {#section_tlx_wj4_xz}

Cadeias de caracteres disponíveis para ações do usuário: marcar, compartilhar e marcar o conteúdo existente como útil.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Rodapé do comentário | wasReviewHelpful | Útil? |
|  | wasReviewHelpfulMobile | Útil? |
|  | ownIsReviewHelpful | Considerado útil. |
|  | reviewwasHelpful | Sim |
|  | útilDivider | &amp;vert; |
|  | reviewIsNotHelpful | Não |
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
