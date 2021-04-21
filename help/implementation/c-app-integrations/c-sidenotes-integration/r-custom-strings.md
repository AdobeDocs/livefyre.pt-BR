---
title: Registra Cadeias de Caracteres Personalizadas
description: Registra Cadeias de Caracteres Personalizadas
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 11%

---

# Indica strings personalizadas{#sidenotes-custom-strings}

As cadeias de caracteres personalizadas são aplicadas por meio de um objeto inserido no construtor Sidenotes e substituem as cadeias de caracteres padrão usadas pelo aplicativo. Eles podem ser usados para personalizar qualquer parte do idioma de acordo com seu estilo ou especificações de idioma. As sequências de caracteres se mesclarão automaticamente com os padrões.

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
| appName | Observações |
| commentModeratorTag | Mod |
| commentPendingTag | Pendente |
| commentReadMoreLink | Ler mais |
| commentReplyLink | Veja {número} respostas |
| commentReplyLinkSing | Ver resposta |
| commentVoteCount | votações |
| commentVoteCountSing | voto |
| editorPlaceholder | O que você acha? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Publicar |
| editorPosting | Postando… |
| editorReplyBtn | Postar resposta |
| editorReplyTitle | Resposta de gravação |
| editorTitle | Nota de escrita |
| emptyImageBlockTxt | O que você acha? |
| emptyTextBlockTxt | + |
| errorConnection | Ah-oh. Você não parece ter uma boa conexão. |
| errorDuplicate | Gostamos da sua nota também, mas você não pode publicá-la duas vezes. |
| errorGeneral | Ocorreu um erro. Tente novamente. |
| errorServer | Algo deu errado com nosso servidor. Tente isso de novo? |
| facebookShareCaption | SideNotes em &quot;{title}&quot; |
| menuAuthSignedInMsg | Você deve estar conectado a {action} |
| menuAuthSignInBtn | Entrar |
| menuBackBtn | Voltar |
| menuConfirmAccept | Sim, {action} |
| menuConfirmCancel | Cancelar |
| menuConfirmTitle | Você tem certeza? |
| menuEtcOptionApprove | Aprovar |
| menuEtcOptionDelete | Excluir |
| menuEtcOptionEdit | Editar   |
| menuEtcOptionFlag | Segnalato |
| menuEtcOptionShare | Compartilhar |
| menuEtcPostedAt | Publicado em {date} |
| menuEtcTitle | Mais |
| menuFlagOptionDisagree | Discordo |
| menuFlagOptionOffensive | Ofensiva |
| menuFlagOptionOffTopic | Tópico desativado |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Sinalizar como... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Ajuda |
| menuInfoLivefyreLink | Visite Livefyre.com |
| menuRepliesExibirResposta | Responder à Conversa |
| menuRepliesViewTitle | Detalhes |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copiar Permalink |
| menuShareOptionLinkComplete | Copiado |
| menuShareOptionLinkFailed | Falha na cópia |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Compartilhar |
| notificationApproved | Aprovado |
| notificationDeleted | Excluído |
| notificationFlagged | Sinalizado |
| permalinkBackBtn | Todos |
| permalinkTitle | Permalink |
| questionExplication | Agora é possível ler e escrever comentários diretamente em frases, parágrafos, imagens e aspas.<br><br>Realce o texto e clique no ícone &quot;fycon-write&quot; ou clique no ícone &quot;fycon-action-view&quot; no final de cada parágrafo. |
| questionMockText | O &quot;conhecimento familiar&quot; não é bem conhecido, só pelo fato de ser &quot;familiar&quot;. |
| questionTitle | O que é um Sidenote? |
| queuedCommentsPlural | {número} Novas Observações |
| queuedCommentsSingular | 1 Novo Sidenote |
| queuedRepliesPlural | {número} Novas Respostas |
| queuedRepliesSingular | 1 Nova Resposta |
| replyBtn | Responder |
| signInToPost | Fazer logon para escrever uma nota |
| sliderCommentTally | of |
| sliderInviteRead | Lido |
| sliderInviteWrite | Gravar |
| sliderWriteText | O que você acha? Toque para gravar |
| threadColapseBtn | Recolher |
| threadExpandBtnPlural | Expandir {número} Respostas |
| threadExpandBtnSingular | Expandir 1 resposta |
| threadReplyBtn | Responder à Conversa |
