---
description: Personalizar as sequências de caracteres dos aplicativos do Livefyre.
seo-description: Personalizar as sequências de caracteres dos aplicativos do Livefyre.
seo-title: Localizar strings
solution: Experience Manager
title: Localizar strings
uuid: c 0 ab 352 d -5 d 3 a -45 d 7-bbd 0-aed 165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Localizar strings{#localize-strings}

Personalizar as sequências de caracteres dos aplicativos do Livefyre.

As strings de texto para a maioria dos elementos HTML em qualquer aplicativo do Livefyre podem ser personalizadas. Isso proporciona a flexibilidade de alterar o texto de elementos HTML renderizados, como o botão «Postar como», o texto «Contagem de comentários» ou o botão «Sign In», a qualquer string UTF -8 válida. Use este recurso para adicionar personalidade à implementação do fluxo ou localizar o idioma no aplicativo para a sua base de usuários.

* Comentários, bate-papo e blog Live

   * [Implementação](#c-localize-strings/section_im4_224_xz)
   * [Acesso à conta](#c-localize-strings/section_cm3_d24_xz)
   * [Informações de fluxo](#c-localize-strings/section_wx1_c24_xz)
   * [Classificação de fluxo](#c-localize-strings/section_ih2_124_xz)
   * [Informações do conteúdo](#c-localize-strings/section_llv_yd4_xz)
   * [Conteúdo em destaque](#c-localize-strings/section_gmw_vd4_xz)
   * [Editor de texto](#c-localize-strings/section_ky5_td4_xz)
   * [Opções de resposta](#c-localize-strings/section_zvt_qd4_xz)
   * [Notificador do comentário](#c-localize-strings/section_qqt_pd4_xz)
   * [Mensagens de erro](#c-localize-strings/section_omz_jxn_xz)

* [Formato e formato de data](#c-localize-strings/section_yz4_g5n_xz)
* [Media Wall](#c-localize-strings/section_vwt_d5n_xz)
* [Mapa](#c-localize-strings/section_fxv_c5n_xz)
* [Mosaico](#c-localize-strings/section_e2s_b5n_xz)
* [Carrossel](#c-localize-strings/section_l2z_hkn_xz)
* [Cartão de recursos](#c-localize-strings/section_mw2_hkn_xz)
* [Pesquisa](#c-localize-strings/section_pdg_fwh_xz)
* [Identidade do Livefyre](#c-localize-strings/section_zc3_xvh_xz)
* Mais:
   * [Revisar strings de texto](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Auxiliares](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## Implementação {#section_im4_224_xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das sequências de caracteres que deseja substituir para o objeto de configuração javascript. Se você não fornecer um campo, o texto padrão será usado.

Exemplo:

```
var customStrings = {     
   postAsButton: "New Post As Text",     
   postEditButton: "New Post Edit Text"  
};   
   convConfig["strings"] = customStrings; fyre.conv.load(     
   networkConfig,     
   [convConfig],     
   function(){}  
);
```

Esta página lista todas as strings de texto que podem ser personalizadas para os principais aplicativos do Livefyre.

## Acesso à conta {#section_cm3_d24_xz}

Strings disponíveis para o processo de Autenticação e a partir dos menus de usuário autenticados.

![](assets/strings_threadheader-150x40.png)

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | Displayname | % s |
|  | Editprofile | Editar perfil |
|  | Notificationsettings | Configurações de notificação |
|  | Siteadmin | Admin Console (links para o Studio) |
|  | Signout | Sair |

## Informações de fluxo {#section_wx1_c24_xz}

Strings disponíveis para informações de fluxo de conteúdo e exibição. Lista o número de pessoas que escutam, o número de postagens para o aplicativo e permite que os usuários façam logon ou acessem suas informações de conta.

| Chave | Texto padrão | Dados de fluxo |
|---|---|---|
|  | Commentcountlabelzero | % s comentário |
|  | Commentcountlabel | % s comentário |
|  | Commentcountlabelplural | % s comentários |
|  | Listenercount | pessoa que ouve |
|  | Listenercountplural | pessoas que escutam |
|  | Liveblogpostcountlabelzero | post |
|  | Liveblogpostcountlabel | post |
|  | Liveblogpostcountlabelplural | postagens |
| Opções de encadeamento | Threadbreakoutbutton | Mostrar thread inteiro |
|  | Togglecollapse | Alternar redução |
| Comentários de velocidade alta/em fila | atualizar | Atualizar |
|  | Newcomment | Novo comentário |
|  | Newcomments | Novos comentários |
|  | Newreply | nova resposta |
|  | Newreplies | novas respostas |

## Classificação de fluxo {#section_ih2_124_xz}

Permite que os usos classifiquem o conteúdo retornado por idade ou popularidade.

![](assets/strings_newestoldesttop-1-150x56.png)

| Chave | Texto padrão | Opções de cabeçalho |
|---|---|---|
|  | Sortnewest | Mais recente |
|  | Sortoldest | Mais antiga |
|  | Sorttopcomments | Principais comentários |
|  | Sorthotthreads | Hot Threads |
|  | Sortseparator |  |  |
|  | Streamsorting | Carregando |
|  | Topcommentscontentnotfoundmsg | Ainda não há suficientes opções curtir. |
|  | Hotthreadscontentnotfoundmsg | Ainda não há threads suficientes. |
|  | Streamrefreshmsg | Consulte Novidades. |
| Opções de rodapé | Archiveheadertitle | Do arquivo |
|  | Archiveshowmais | Mostrar mais |
|  | Showmais | Mostrar mais comentários |
|  | Showmoreliveblog | Mostrar mais publicações |

![](assets/strings_threadend-150x47.png)

## Informações do conteúdo {#section_llv_yd4_xz}

Lista as informações da publicação: nome de usuário, qualquer tag de usuário aplicada e tempo de postagem.

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| Chave | Texto padrão | Autor |
|---|---|---|
|  | moderador | moderador |
|  | Hovercardviewprofile | Exibir perfil completo |
| Informações da publicação | Timejustnow | now |
|  | Timeminutesago | minuto atrás |
|  | Timeminutesagoplural | minutos atrás |
|  | Timehoursago | hora atrás |
|  | Timehoursagoplural | horas atrás |
|  | Timedaysago | dia atrás |
|  | Timedaysagoplural | dias atrás |
|  | Likesplural | Curtidas |
|  | Likessingular | Curtir |
|  | Moderatoredittimestamp | Editado por um Moderador |
|  | Commenttombstone | Esse comentário foi excluído |
|  | Permalinknotfoundmsg | Esse comentário não está mais visível. |
|  | Quickprofiletooltip | Perfil rápido |

## Conteúdo em destaque {#section_gmw_vd4_xz}

Se ativado, o conteúdo em destaque é listado na parte superior do fluxo.

|  | Chave | Texto padrão |
|---|---|---|
| Rótulos em destaque |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | Featuredcommentstag | Destaque |
|  | Featuredcommentstitleplural | Comentários em destaque |

## Editor de texto {#section_ky5_td4_xz}

Por padrão, disponível na parte superior da página para todos os usuários.

![](assets/strings_texteditor-1-150x77.png)

|  | Chave | Texto padrão |
|---|---|---| 
| Botões do editor | follow | + Seguir |
|  | unfollow | - Deixar de seguir |
|  | Liveblogfollow | Seguir blog ao vivo |
|  | Liveblogunfollow | Desseguir o blog Live |
|  | Postbutton (disponível para usuários conectados.) | Comentário da postagem |
|  | Postasbutton (Disponível para usuários não autenticados.) | Comentar como… |
|  | Posteditbutton | Editar comentário |
|  | Posteditasbutton | Editar comentário como… |
|  | Posteditcancelbutton | Cancelar |
|  | Editordisabled | No momento, esta conversa está fechada para novos comentários. |
| Opções de bate-papo | Livechatpostbuttonlabel | Postagem |
|  | Livechatposteditbutton | Editar |
|  | Livechatwindowsinstruction | Pressione control + enter para postar |
|  | Livechatotherinstruction | Pressione command + enter para postar |

## Opções de resposta {#section_zvt_qd4_xz}

A menos que seja observado, disponível para todos os usuários conectados. Passe o mouse sobre um painel de conteúdo para acessar.

![](assets/strings_banusermodal-150x36.png)

| Chave | Texto padrão |  |
|---|---|---|
| Opções de resposta do usuário | Disponível para usuários finais. |  |
| Flagbutton | Sinalizar |
|  | Flagcommenttooltip | Sinalizar |
|  | Editboton (Disponível somente para autores e moderadores, se ativado.) | Editar |
|  | Deletebutton (Disponível somente para autores e moderadores, se ativado.) | Excluir |
|  | Deletecommenttooltip | Excluir |
|  | Sharebutton | Compartilhar |
|  | Sharecommenttooltip | Compartilhar |
|  | Likebutton | Curtir |
|  | Unlikebutton | Diferente |
|  | Replybutton | Responder |
|  | Replybuttonunique (Disponível para Bate-papo e Blog ativo.) | Responder |
|  | Reagybuttonplural (disponível para Bate-papo e Blog Live.) | Respostas |

![](assets/strings_responseoptions-150x35.png)

| Chave | Texto padrão |  |
|---|---|---|
| Sinalizar modal | Flagtitle | Comentário de % s do sinalizador |
|  | Flagsubtitle | Sinalizar como |
|  | Flagdefaultdefintoption | Selecionar |
|  | Flagspam | Spam |
|  | Flagspambutton | Spam |
|  | Flagspamcommenttooltip | Spam |
|  | Flagofensiva | Ofensiva |
|  | Flagoffensivebutton | Ofensiva |
|  | Flagoffensivecommenttooltip | Ofensiva |
|  | Flagdiscordisagree | Discordar |
|  | Flagdisagreebutton | Discordar |
|  | Flagdisagreecommenttooltip | Discordar |
|  | Flagofftopic | Tópico desligado |
|  | Flagofftopicbutton | Tópico desligado |
|  | Flagofftopiccommenttooltip | Tópico desligado |
|  | Flagemail | Email |
|  | Flagemailplaceholder | you@example.com |
|  | Flagnotes | Notas |
|  | Flagnotesplaceholder | Comece a digitar aqui… |
|  | Flagconfirmmbutton | OK |
|  | Flagcancelbutton | Cancelar |
|  | Flagconfirmmationmessage | % s comentário do sinalizador como % s? |
|  | Flagsuccessmsg | O comentário foi sinalizado. |

![](assets/strings_flagmodal-150x87.png)

| Chave | Texto padrão |  |
|---|---|---|
| Compartilhar modal | Sharetitle | Compartilhar comentário |
|  | Shareplaceholdertext | O que você acha? |
|  | Shaptabel | Compartilhar em: |
|  | Sharetexttwitter | blank |
|  | Sharetextfacebook | blank |
|  | Sharetextlinkedin | blank |
|  | Sharebuttontext | Compartilhar |
|  | Sharepermalink | Permalink |
|  | Loadingpermalink | Carregando URL curto… |
|  | Sharetext | Acabei de postar um comentário. Confira! |

![](assets/strings_sharemodal-150x59.png)

| Chave | Texto padrão |  |
|---|---|---|
| Responder modal | Postreplyasbutton | Comentar como… |
|  | Postreplybutton (disponível para usuários conectados.) | Comentário da postagem |
|  | Backtohotthreads | Voltar para Threads |

![](assets/strings_backto-150x48.png)

| Chave | Texto padrão |  |
|---|---|---|
| Twitter @ menção modal | Mentiontitle | Compartilhar menção |
|  | Mentionsubtitletwitter | Compartilhar tweet para: |
|  | Mentiondefaulttext | Eu mencionei você em um comentário do Livefyre! |
|  | Mentionconfirmmbutton | OK |
|  | Mentioncancelbutton | Cancelar |
|  | Mentionparam MentionErrorGeneral | Ops! Algo deu errado! O Livefyre foi alertado. |
|  | Mentionparam noneselected | Você deve ter pelo menos uma menção ativada. |
|  | Mentionmenutitle | Para ver e mencionar seus amigos |
|  | Mentiontwitterconnect | Conectar ao Twitter |
|  | Mentiontwitterfetching | Buscando amigos… |
|  | Mentionsuccessmsg | As menções foram enviadas com êxito. |

![](assets/strings_sharemention-150x60.png)

| Chave | Texto padrão |  |
|---|---|---|
| Editar modal | Disponível para administradores do Studio, Gerentes de usuário ou Moderadores |  |
| @ (@ menção.) | </> (Abre a janela html personalizada). |  |
|  | Customhtmldialogtitle (aparece como o cabeçalho do modal.) | Adicionar HTML personalizado |

![](assets/strings_moderatoreditmodal-150x49.png)

| Chave | Texto padrão |  |
|---|---|---|
| Opções de resposta do moderador | Disponível para administradores do Studio, Gerentes de usuário ou Moderadores. |  |
| Pendingcomment | pending |
|  | Banuserbutton | Excluir usuário |
|  | Banusertooltip | Proibir usuário |
|  | Bozobutton | Bozo |
|  | Bozocommenttooltip | Bozo |
|  | Featurebutton | Recurso |
|  | Featurecommenttooltip | Recurso |
|  | Unfeaturebutton | Não recurso |
|  | Featuredcommenttooltip | Não recurso |

![](assets/strings_adminoptions-150x33.png)

| Chave | Texto padrão |  |
|---|---|---|
| Excluir usuário do usuário | Disponível para administradores do Studio, Gerentes de usuário ou Moderadores. |  |
| Bantitle | Proibir usuário |  |
|  | Banconfirmation | Tem certeza de que deseja excluir esse usuário? |
|  | Banconfirmmbutton | OK |
|  | Bancancelbutton | Cancelar |

## Notificador do comentário {#section_qqt_pd4_xz}

Se ativado, disponível na parte inferior da página para todos os Aplicativos de conversa do Livefyre.

![](assets/strings_notifier-150x112.png)

|  | Chave | Texto padrão |
|---|---|---|
| Rótulos de notificador | Commentnotificador | Novo comentário |
|  | Commentnotificerplural | Novos comentários |
|  | Liveblognotificador | Nova publicação |
|  | Liveblognotificerplural | Novas publicações |

## Mensagens de erro {#section_omz_jxn_xz}

Strings disponíveis para mensagens de erro personalizáveis.

| Chave | Texto padrão |
|---|---|
| Errorautherror | Você não está autorizado a postar um comentário nesta conversa |
| Errorcommentsnotallowed | Comentários não são permitidos nesta conversa |
| Errordefault | Ocorreu um erro. Tente novamente. |
| Errorduplicate | Como você curtiram seu comentário, você não tem permissão para postá-lo duas vezes. |
| Erroreditduplicate | Você deve alterar o corpo do comentário ao editá-lo. |
| Erroreditnotallowed | Você não tem permissão para editar comentários nesta conversa. |
| Erroredittimeexceeded | Seu período de edição de comentário expirou. |
| Errorempty | Parece que você está tentando postar um comentário vazio. |
| Errorexpired | Sua sessão expirou. Recarregue a página. |
| Errorflagnotselected | Selecione um tipo de sinalizador. |
| Errorguestliked | Desculpe, somente aqueles com contas podem curtir o conteúdo. |
| Signatinsufficientpermissions | Permissões insuficientes |
| Issubinvalidchar | Parece que você está tentando postar um caractere inválido. |
| Issublikeowncomment | Não é possível curtir seu próprio comentário |
| Errormalformed | Parece que você está tentando postar conteúdo malformado. |
| Signatmaxchars | Seu comentário é muito longo. Edite e tente novamente. |
| Errormedianotavailable | A mídia não está mais visível. |
| Errorshowmais | Ocorreu um erro ao carregar mais comentários. |
| Multiplemedianotallowederror | Suas permissões concedem apenas um anexo de mídia por vez. |

## Formato e formato de data {#section_yz4_g5n_xz}

Traduza e personalize como as datas aparecem em cartões de conteúdo nos aplicativos de visualização.

| Chave | Texto padrão |
|---|---|
| Hoursago | {número} h |
| Hoursagosingular | {número} h |
| Justnow | 1s |
| Minutesago | {number} m |
| Minutesagosingular | {number} m |
| Monthdayformat | {dia} {monthabbrev} |
| Monthdayyearformat | {dia} {monthabbrev} {year} |
| Monthnames | janeiro, fevereiro, março, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro |
| Monthnamesabbrev | Jan, Feb, Mar, Apr, maio, Jun, Jul, Aug, Sep, Out, Nov, Dez |
| Secondsago | {número} s |
| Secondsagosingular | {número} s |

## Media Wall {#section_vwt_d5n_xz}

Strings disponíveis para o aplicativo de mural de mídia.

| Chave | Texto padrão |
|---|---|
| Featuredtext | Destaque |
| Sharebuttontext | Compartilhar |

| Chave | Texto padrão |
|---|---|
| Postbuttontext | O que está pensando? |
| Postmodaltitle | Poste seu comentário |
| Postmodalbutton | Poste seu comentário |
| Postmodalplaceholder | O que você gostaria de dizer? |
| Showmorebuttontext | Carregar mais |
| Sharebuttontext | Compartilhar |

## Mapa {#section_fxv_c5n_xz}

Strings disponíveis para Mapas.

| Chave | Texto padrão |
|---|---|
| Featuredtext | Destaque |
| Sharebuttontext | Compartilhar |

## Mosaico {#section_e2s_b5n_xz}

Strings disponíveis para Mosaicos.

| Chave | Texto padrão |
|---|---|
| Featuredtext | Destaque |
| Sharebuttontext | Compartilhar |

## Carrossel {#section_l2z_hkn_xz}

Strings disponíveis para o carrossel.

| Chave | Texto padrão |
|---|---|
| Featuredtext | Destaque |
| Sharebuttontext | Compartilhar |

## Cartão de recursos {#section_mw2_hkn_xz}

Strings disponíveis para o Cartão de recursos.

| Chave | Texto padrão |
|---|---|
| Featuredtext | Destaque |
| Sharebuttontext | Compartilhar |

## Carregar aplicativo {#section_grc_gkn_xz}

Strings disponíveis para o Upload App.

| Chave | Texto padrão |
|---|---|
| Postbuttontext | O que está pensando? |
| Postmodaltitle | Poste seu comentário |
| Postmodalbutton | Poste seu comentário |
| Postmodaltitleplaceholder | Inserir um título |
| Postmodalplaceholder | O que você gostaria de dizer? |
| Postmodalconfirmationtitle | Obrigado por postar! |
| Postmodalconfirmmationmessage | Sua publicação está sendo analisada. |
| Postmodalconfirmmationbutton | Concluído |
| title |  |
| message |  |
| Editorparam attachmentsrequired | Um anexo é obrigatório |
| Editorparam editorErrorBody | Adicione uma mensagem |
| Editorparam editorErrorDuplicate | Tanto quanto você desejar, não é possível postá-la duas vezes |
| Editorparam Genérico | Ocorreu um erro |
| Editorerrortitlerequked | Um título é obrigatório |

## Pesquisa {#section_pdg_fwh_xz}

Strings disponíveis para Pesquisas.

| Chave | Texto padrão |
|---|---|
| Totalexpresseslabel | % s total de votos |
| Sharestringtext | Acabei de votar em % s qual é seu voto? |
| Pollclosedlabel | No momento, esta pesquisa está fechada |

## Identidade do Livefyre {#section_zc3_xvh_xz}

Strings disponíveis para identidade do Livefyre.

| Chave | Texto padrão |
|--- |--- |
| Automaticallyfollowconversations | Siga as conversas automaticamente que eu ingressar |
| back | Voltar |
| bio | Biografia |
| create | Criar |
| Createanewaccount | Criar nova conta |
| Createnewaccountwithemail | Criar uma nova conta com e-mail |
| Changeavatar | Alterar avatar |
| Choosefile | Escolher arquivo |
| Completeaccount | Conta completa |
| Emailwhensomeonereplies | Enviar email quando alguém responder a mim |
| Emailcommentsifollow | Enviar comentários por email em conversas que eu segue |
| Emailsenttoresetpassword | Email enviado! Marque a caixa de entrada para redefinir sua senha |
| Emailverificationsent | Verificação de email enviada |
| Firstname | Nome |
| Forgotpassword | Esqueceu a senha? |
| Forgotyourpassword | Esqueceu sua senha? |
| Forgotyourpasswordinstructions | Digite seu nome de usuário ou endereço de e-mail abaixo, e nós enviaremos um link para alterar sua senha. |
| Forminputclosebuttontext | Fechar |
| Forminputcancelbuttontext | Cancelar |
| Forminputsavebuttontext | Salvar |
| Hasnotleftanycomments | não deixou comentários |
| Locationisfrom | é de |
| Labelavatar | Avatar |
| Labelcomments | Comentários |
| Labelconfirmnewpassword | Confirmar nova senha |
| Labelconfirmpassword | Confirmar senha |
| Labelemail | Endereço de email |
| Labellikes | Curtidas |
| Labelloading | Carregando |
| Labelnewpassword | Nova senha |
| Labelnotification | Notificações |
| Labelpassword | Senha |
| Labelprofile | Perfil |
| Labelusername | Nome de usuário |
| Labelusernameoremail | Nome de usuário ou email |
| Lastname | Sobrenome |
| Livefyreaccount | Conta do Livefyre |
| localização | Local |
| Loadingprofile | Carregando perfil |
| Newpassword | Nova senha |
| Oldpassword | Senha antiga |
| on | on |
| ou | ou |
| Passwordlinkexpired | O link clicado para redefinir sua senha expirou. Redefina a senha novamente e enviaremos um novo link. |
| Pleasecheckemailtocomplete | Verifique seu e-mail para concluir o registro. |
| posted | Postado |
| Poweredby | powered by |
| Profilenotificationimmediate | imediato |
| Profilenotificationhourly | por hora |
| Profilenotificationnever | nunca |
| Recentcomments | Comentários recentes |
| reset | Redefinir |
| Resetpassword | Redefinir senha |
| Signin | Entrar |
| Signinwith | Faça logon com |
| Signinwithemail | Fazer logon com email |
| Signup | Cadastrar-se |
| Socialaccount | Conta social |
| Successpasswordchanged | Sucesso! Sua senha foi alterada e agora você está conectado |
| Termsandconditions | Termos e condições |
| Termsandconditionsintro | Ao se inscrever, você aceita a |
| Termsofuse | Termos de uso |
| Termsofuseintro | Ao fazer logon, você concorda em |
| Thisuser | Este usuário |
| Verifypassword | Verificar senha |
| Filesizelimit | Máx. de 2 MB |
| accountnotfound | Conta não encontrada |
| Avatarimageexceedsize | Sua imagem de avatar excedeu o limite de arquivo de 2 mb |
| fieldisrequired | O campo aceita apenas um número inteiro |
| fieldonlyacceptsavalidemail | O campo aceita apenas um email válido |
| fieldonlyacceptsletters | O campo aceita somente letras |
| Filesizemustbelessthanmb | O tamanho do arquivo deve ser menor que {#}MB |
| invalidusernameorpassword | Nome de usuário ou senha inválido |
| minimumlengthofcharacters | Comprimento mínimo de {#} caracteres |
| maximumlengthofcharacters | Comprimento máximo de {#} caracteres |
| therewasanerror | Ocorreu um erro |
| thisfieldisrequired | Esse campo é obrigatório. |
| extensões de validação | Extensões de arquivo válidas |
| valuemustmatch | O valor deve corresponder |
| Passwordlength | tenha 6 a 32 caracteres. |
| Passwordcharacters | incluir caracteres de letras maiúsculas e minúsculas. |
| Passwordsymbols | incluir pelo menos um número e um símbolo. |
| Passwordusername | não contém seu nome de usuário. |
| Passwordpopovertitle | Sua senha precisa: |
| Passwordparam containsfirstname | A senha inserida contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, insira uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que a senha deve conter: 6 a 32 caracteres Um caractere maiúsculo A Um símbolo de minúsculo A |
| Passwordparam containslastname | A senha inserida contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, insira uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que a senha deve conter: 6 a 32 caracteres Um caractere maiúsculo A Um símbolo de minúsculo A |
| Passwordparam containsusername | A senha inserida contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, insira uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que a senha deve conter: 6 a 32 caracteres Um caractere maiúsculo A Um símbolo de minúsculo A |
| Passwordparam tooshort | Mínimo de 6 caracteres para pasword |
| Passwordparam toolong | Máximo de 32 caracteres para senha |
| Passwordparam missinguppercase | A senha deve conter pelo menos um caractere maiúsculo |
| Passwordparam missinglowercase | A senha deve conter pelo menos um caractere minúsculo |
| Passwordparam missingsymbol | A senha deve conter pelo menos um símbolo no conjunto `!@#$%^&*()?.,<>\’;:”[]{}|` |


