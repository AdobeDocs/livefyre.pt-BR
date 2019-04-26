---
description: Personalização das strings de texto para Livefyre Sidenotes
seo-description: Personalização das strings de texto para Livefyre Sidenotes
seo-title: Vincular strings de texto
solution: Experience Manager
title: Vincular strings de texto
uuid: a 3735237-e 55 d -4 bc 0-b 88 d -8 a 323980 ee 09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Vincular strings de texto{#sidenotes-text-strings}

Personalização das strings de texto para Livefyre Sidenotes

Esta página lista e descreve todas as strings disponíveis para personalização em aplicativos de Sidenotes. Para obter informações sobre strings disponíveis para os aplicativos principais do Livefyre, consulte Personalizações de string.

Erros de
autor de implementação de
autenticação/informações
de conteúdo do usuário das informações
de publicação do moderador

## Implementação {#section_wp2_ql4_xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das sequências de caracteres que deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

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

Strings disponíveis para o processo de Autenticação e a partir dos menus de usuário autenticados.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Strings de menu de autenticação | Menuauthsigninbtn | Entrar |
|  | Menuauthsignedinmsg | Você deve estar conectado à {action} |
|  | Menuusereditprofile | Editar perfil |
|  | Menuuseradmin | Admin Console |
|  | Menuuserlogout | Sair |
|  | Menuuserbackbtn | Todos |

## Informações de fluxo {#section_wpy_gl4_xz}

Strings disponíveis para informações de fluxo de conteúdo e exibição.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Opções do menu Informações | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Ajuda |
|  | Menuinfolivefyrevink | Visite Livefyre.com |

## Informações do autor/conteúdo {#section_dhb_gl4_xz}

As classificações disponíveis para o autor e informações de conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | Commentmoderatortag | Mod |
|  | Commentpendingtag | Pendente |
|  | Commentreadmorelink | Ler mais |
|  | Commentreplylink | Consulte {número} respostas |
|  | Commentreplylinksing | Consulte a resposta |
|  | Commentvotecount | votos |
|  | Commentvotecountsing | vote |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | Uma matriz. Padrão =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | Questionexplanation | Agora você pode ler e escrever comentários diretamente em frases, parágrafos, imagens e aspas.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Realce o texto</span> e clique no <span class="&rdquo;fycon-write&rdquo;"></span> ícone ou clique no <span class="&rdquo;fycon-action-view&rdquo;"></span> ícone ao final de cada parágrafo. |
|  | Questionmocktext | O que é conhecido como "familiar" não é conhecido corretamente, apenas pelo motivo pelo qual é "familiar". |
|  | Questiontitle | O que é um sidenote? |

## Ações do usuário {#section_qxd_fl4_xz}

Strings disponíveis para ações do usuário: sinalizar, compartilhar e curtir conteúdo existente.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Opções de menu de resposta | Menurepliesviewtitle | Detalhes |
|  | Menurepliesviewresponse | Responder à conversa |
| Opções de menu Compartilhar | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Compartilhar |
| Opções de menu Sinalizar | Menuflagoptiondisagree | Discordar |
|  | Menuflagoptionoffensive | Ofensiva |
|  | Menuflagoptionofftopic | Tópico desligado |
|  | Menuflagoptionspam | Spam |
|  | Menuflagtitle | Sinalizar como… |
|  | Facebookshouteraption | Tarefas em «{title}» |
| Opções de usuário móvel | Slidercommenttally | de |
|  | Sliderinviteread | Leitura |
|  | Sliderinvitewrite | Gravar |
|  | Sliderloading | Carregando… |
|  | Sliderwritetext | O que você acha? Toque em para gravar. |

## Funções de postagem {#section_xzf_2l4_xz}

Strings disponíveis para usuários que postam conteúdo.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | Editoreditbtn | Salvar |
|  | Editoreditposting | Salvando… |
|  | Editoreditreplytitle | Editar resposta |
|  | Editoredittitle | Editar sidenote |
|  | Editorplaceholder | O que você acha? |
|  | Editorpostbtn | Sidenote de postagem |
|  | Editorpostbtnmobile | Postagem |
|  | Editorpostpostar | Postando… |
|  | Editorreplybtn | Resposta posterior |
|  | Editorreplytitle | Escrever resposta |
|  | Editortitle | Escrever sidenote |
|  | Emptyimageblocktxt | O que você acha? |
|  | Emptytextblocktxt | + |
|  | Replybtn | Responder |
|  | Threadreplybtn | Responder à conversa |
| Excluir opções de menu | Menuconfirmaccept | Sim, {action} |
|  | Menuconfirmcancel | Cancelar |
|  | Menuconfirmtitle | Tem certeza? |
| Opções de menu | Menuetcoptionapprove | Aprovar |
|  | Menuetcoptiondelete | Excluir |
|  | Menuetcoptionedit | Editar |
|  | Menuetcoptionflag | Sinalizar |
|  | Menuetcoptionshare | Compartilhar |
|  | Menuetcpostedat | Publicado em {data} |
|  | Menuetctitle | Mais |

## Interface do moderador {#section_o5f_dl4_xz}

Strings disponíveis para a interface do moderador autenticada pelo usuário.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Mensagens de confirmação no menu Mais | Notificationapproved | Aprovado |
|  | Notificationdeleted | Excluído |
|  | Notificationflagged | Sinalizado |

## Erros {#section_gtk_cl4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | Errorconnection | Uh-oh. Você não tem uma boa conexão. |
|  | Errorduplicate | Também queremos sua observação, mas não é possível postá-la duas vezes. |
|  | Errorgeneral | Ocorreu um erro. Tente novamente. |
|  | Errorserver | Algo deu errado com nosso servidor. Experimente novamente? |

