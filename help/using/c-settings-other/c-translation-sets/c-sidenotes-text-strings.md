---
description: Personalização das cadeias de texto para Livefyre Sidenotes
title: Registra Cadeias de Caracteres de Texto
exl-id: 132a7c8d-10e1-419c-9d79-a40553e70785
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 13%

---

# Indica sequências de texto{#sidenotes-text-strings}

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
|  | datetimeMonths | Uma matriz. Padrão =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
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
