---
description: Personalização das strings de texto para Livefyre Sidenotes
seo-description: Personalização das strings de texto para Livefyre Sidenotes
seo-title: Separa strings de texto
solution: Experience Manager
title: Separa strings de texto
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 12%

---


# Separa strings de texto{#sidenotes-text-strings}

Personalização das strings de texto para Livefyre Sidenotes

Esta página lista e descreve todas as sequências de caracteres disponíveis para personalização em aplicativos Sidenotes. Para obter informações sobre strings disponíveis para os principais aplicativos Livefyre, consulte Personalizações de string.

Implementação
Auth
Informações de fluxo
Informações do autor/conteúdo
Ações do usuário
Funções de publicação
Interface do moderador
Erros

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
| Strings de menu de autenticação | menuAuthSignInBtn | Entrar |
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
|  | datetimeMonths | Uma matriz. Padrão =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplication | Agora você pode ler e escrever comentários diretamente em frases, parágrafos, imagens e citações.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Realce o texto </span> e clique no  <span class="&rdquo;fycon-write&rdquo;"></span> ícone ou no  <span class="&rdquo;fycon-action-view&rdquo;"></span> ícone no final de cada parágrafo. |
|  | questionMockText | O que é &quot;conhecido familiar&quot; não é propriamente conhecido, apenas pelo fato de ser &quot;familiar&quot;. |
|  | questionTitle | O que é um Sidenote? |

## Ações do usuário {#section_qxd_fl4_xz}

Strings disponíveis para ações do usuário: marcar, compartilhar e curtir o conteúdo existente.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Opções do menu Responder | menuRespostasExibirTítulo | Detalhes |
|  | menuRespostasExibirResponder | Responder à conversa |
| Opções do menu Compartilhar | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuCompartilharTítulo | Compartilhar |
| Opções do menu Sinalizar | menuFlagOptionDisagree | Discordar |
|  | menuFlagOptionOffensive | Ofensivo |
|  | menuFlagOptionOffTopic | Tópico desativado |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Sinalizar como... |
|  | facebookShareCaption | Notas de identidade em &quot;{title}&quot; |
| Opções do usuário móvel | sliderCommentTally | of |
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
| Excluir opções do menu | menuConfirmAccept | Sim, {action} |
|  | menuConfirmCancel | Cancelar |
|  | menuConfirmTitle | Você tem certeza? |
| Opções do menu Etc | menuEtcOptionAprovar | Aprovar |
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
| Mensagens de confirmação do menu Mais | notificationAprovado | Aprovado |
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

