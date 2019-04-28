---
description: 'null'
seo-description: 'null'
seo-title: Vincular strings personalizadas
title: Vincular strings personalizadas
uuid: 73745273-d 3 fb -4569-8910-d 149 fb 37 a 7 b 4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Vincular strings personalizadas{#sidenotes-custom-strings}

As strings personalizadas são aplicadas por meio de um objeto inserido no construtor de Sidenotes e substituem as strings padrão usadas pelo aplicativo. Eles podem ser usados para personalizar qualquer parte do idioma para se ajustar às especificações de estilo ou idioma. As sequências de caracteres serão mescladas automaticamente com padrões.

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
| Appname | Auxiliares |
| Commentmoderatortag | Mod |
| Commentpendingtag | Pendente |
| Commentreadmorelink | Ler mais |
| Commentreplylink | Consulte {número} respostas |
| Commentreplylinksing | Consulte a resposta |
| Commentvotecount | votos |
| Commentvotecountsing | vote |
| Editorplaceholder | O que você acha? |
| Editorpostbtn | Sidenote de postagem |
| Editorpostbtnmobile | Postagem |
| Editorpostpostar | Postando… |
| Editorreplybtn | Resposta posterior |
| Editorreplytitle | Escrever resposta |
| Editortitle | Gravar nota |
| Emptyimageblocktxt | O que você acha? |
| Emptytextblocktxt | + |
| Errorconnection | Uh-oh. Você não tem uma boa conexão. |
| Errorduplicate | Também queremos sua observação, mas não é possível postá-la duas vezes. |
| Errorgeneral | Ocorreu um erro. Tente novamente. |
| Errorserver | Algo deu errado com nosso servidor. Experimente novamente? |
| Facebookshouteraption | Sidenotes em «{title}» |
| Menuauthsignedinmsg | Você deve estar conectado à {action} |
| Menuauthsigninbtn | Entrar |
| Menubackbtn | Voltar |
| Menuconfirmaccept | Sim, {action} |
| Menuconfirmcancel | Cancelar |
| Menuconfirmtitle | Tem certeza? |
| Menuetcoptionapprove | Aprovar |
| Menuetcoptiondelete | Excluir |
| Menuetcoptionedit | Editar |
| Menuetcoptionflag | Sinalizar |
| Menuetcoptionshare | Compartilhar |
| Menuetcpostedat | Publicado em {data} |
| Menuetctitle | Mais |
| Menuflagoptiondisagree | Discordar |
| Menuflagoptionoffensive | Ofensiva |
| Menuflagoptionofftopic | Tópico desligado |
| Menuflagoptionspam | Spam |
| Menuflagtitle | Sinalizar como… |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | Ajuda |
| Menuinfolivefyrevink | Visite Livefyre.com |
| Menurepliesviewresponse | Responder à conversa |
| Menurepliesviewtitle | Detalhes |
| Menushareoptionfacebook | Facebook |
| Menushareoptionlink | Copiar permalink |
| Menushareoptionlinkcomplete | Copiado |
| Menushareoptionlinkfailed | Falha na cópia |
| Menushareoptiontwitter | Twitter |
| Menusharetitle | Compartilhar |
| Notificationapproved | Aprovado |
| Notificationdeleted | Excluído |
| Notificationflagged | Sinalizado |
| Permalinkbackbtn | Todos |
| Permalinktitle | Permalink |
| Questionexplanation | Agora você pode ler e escrever comentários diretamente em frases, parágrafos, imagens e aspas.<br><br>Realce o texto e clique no ícone &quot;fycon-write&quot; ou clique no ícone &quot;fycon-action-view&quot; ao final de cada parágrafo. |
| Questionmocktext | O que é conhecido como &quot;familiar&quot; não é conhecido corretamente, apenas pelo motivo pelo qual é &quot;familiar&quot;. |
| Questiontitle | O que é um sidenote? |
| Queuedcommentsplural | {número} Novas seções |
| Queuedcommentssingular | 1 Novo sidenote |
| Queuedrepliesplural | {número} Novas respostas |
| Queuedrepliessingular | 1 Nova resposta |
| Replybtn | Responder |
| Signintopost | Fazer logon para gravar um sidenote |
| Slidercommenttally | de |
| Sliderinviteread | Leitura |
| Sliderinvitewrite | Gravar |
| Sliderwritetext | O que você acha? Toque para gravar |
| Threadcollapsebtn | Recolher |
| Threadexpandbtnplural | Expandir {número} Respostas |
| Threadexpandbtnous | Expandir 1 Resposta |
| Threadreplybtn | Responder à conversa |
