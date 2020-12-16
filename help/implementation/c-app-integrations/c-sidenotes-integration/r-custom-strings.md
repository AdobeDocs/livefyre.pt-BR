---
description: 'null'
seo-description: nulo
seo-title: Separa strings personalizadas
title: Separa strings personalizadas
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 12%

---


# Transfere strings personalizadas{#sidenotes-custom-strings}

As strings personalizadas são aplicadas por meio de um objeto inserido no construtor Sidenotes e substituem as strings padrão usadas pelo aplicativo. Eles podem ser usados para personalizar qualquer parte do idioma de acordo com suas especificações de estilo ou idioma. As sequências de caracteres se mesclarão automaticamente com os padrões.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Chave | Padrão |
|---|---|
| appName | Sidenotes |
| commentModeratorTag | Mod |
| commentCurrentTag | Pendente |
| commentReadMoreLink | Ler mais |
| commentReplyLink | Consulte {número} respostas |
| commentReplyLinkSing | Consulte resposta |
| commentVoteCount | votação |
| commentVoteCountSing | voto |
| editorPlaceholder | O que você acha? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Publicar |
| editorPostagem | Postando… |
| editorReplyBtn | Postar resposta |
| editorReplyTitle | Gravar resposta |
| editorTitle | Gravar nota |
| emptyImageBlockTxt | O que você acha? |
| emptyTextBlockTxt | + |
| errorConnection | Oh-oh. Você não parece ter uma boa conexão. |
| errorDuplicate | Também gostamos da sua nota, mas não é possível publicá-la duas vezes. |
| errorGeneral | Ocorreu um erro. Tente novamente. |
| errorServer | Algo deu errado com nosso servidor. Tenta de novo? |
| facebookShareCaption | SideNotes em &quot;{title}&quot; |
| menuAuthSignedInMsg | Você deve estar conectado a {action} |
| menuAuthSignInBtn | Entrar |
| menuBackBtn | Voltar |
| menuConfirmAccept | Sim, {action} |
| menuConfirmCancel | Cancelar |
| menuConfirmTitle | Você tem certeza? |
| menuEtcOptionAprovar | Aprovar |
| menuEtcOptionDelete | Excluir |
| menuEtcOptionEdit | Editar   |
| menuEtcOptionFlag | Segnalato |
| menuEtcOptionShare | Compartilhar |
| menuEtcPostedAt | Publicado em {date} |
| menuEtcTitle | Mais |
| menuFlagOptionDisagree | Discordar |
| menuFlagOptionOffensive | Ofensivo |
| menuFlagOptionOffTopic | Tópico desativado |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Sinalizar como... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Ajuda |
| menuInfoLivefyreLink | Visite Livefyre.com |
| menuRespostasExibirResponder | Responder à conversa |
| menuRespostasExibirTítulo | Detalhes |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copiar Permalink |
| menuShareOptionLinkComplete | Copiado |
| menuShareOptionLinkFailed | Falha na cópia |
| menuShareOptionTwitter | Twitter |
| menuCompartilharTítulo | Compartilhar |
| notificationAprovado | Aprovado |
| notificationDeleted | Excluído |
| notificationFlagged | Sinalizado |
| permalinkBackBtn | Todos |
| permalinkTitle | Permalink |
| questionExplication | Agora você pode ler e escrever comentários diretamente em frases, parágrafos, imagens e citações.<br><br>Realce o texto e clique no ícone &quot;fycon-write&quot; ou clique no ícone &quot;fycon-action-visualização&quot; no final de cada parágrafo. |
| questionMockText | O que é &quot;conhecido familiar&quot; não é propriamente conhecido, apenas pelo fato de ser &quot;familiar&quot;. |
| questionTitle | O que é um Sidenote? |
| queuedCommentsPlural | {número} Novos Sidenotes |
| queuedCommentsSingular | 1 Novo Sidenote |
| queuedRepliesPlural | {número} Novas Respostas |
| queuedRepliesSingular | 1 Nova resposta |
| replyBtn | Responder |
| signInToPost | Fazer logon para escrever uma nota de identidade |
| sliderCommentTally | of |
| sliderInviteRead | Lido |
| sliderInviteWrite | Gravar |
| sliderWriteText | O que você acha? Toque para gravar |
| threadCollapseBtn | Recolher |
| threadExpandBtnPlural | Expandir {number} Respostas |
| threadExpandBtnSingular | Expandir 1 resposta |
| threadReplyBtn | Responder à conversa |
