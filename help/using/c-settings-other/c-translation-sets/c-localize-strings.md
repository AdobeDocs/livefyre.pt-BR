---
description: Personalização das strings dos aplicativos Livefyre.
seo-description: Personalização das strings dos aplicativos Livefyre.
seo-title: Localize sequências de caracteres
solution: Experience Manager
title: Localize sequências de caracteres
uuid: c0ab352d-5d3a-45d7-bbd0-aed165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 8%

---


# Localize strings{#localize-strings}

Personalização das strings dos aplicativos Livefyre.

As strings de texto para a maioria dos elementos HTML em qualquer aplicativo Livefyre podem ser personalizadas. Isso proporciona a flexibilidade para alterar o texto de elementos HTML renderizados, como o botão &quot;Publicar como&quot;, o texto &quot;Contagem de comentários&quot; ou o botão &quot;Entrar&quot;, para qualquer string UTF-8 válida. Use esse recurso para adicionar personalidade à sua implementação do fluxo ou para localizar o idioma no aplicativo para sua base de usuários.

* Comentários, Bate-papo e Blog ao vivo

   * [Implementação](#c-localize-strings/section_im4_224_xz)
   * [Acesso à conta](#c-localize-strings/section_cm3_d24_xz)
   * [Informações de fluxo](#c-localize-strings/section_wx1_c24_xz)
   * [Classificação de fluxo](#c-localize-strings/section_ih2_124_xz)
   * [Informações do conteúdo](#c-localize-strings/section_llv_yd4_xz)
   * [Conteúdo em destaque](#c-localize-strings/section_gmw_vd4_xz)
   * [Editor de texto](#c-localize-strings/section_ky5_td4_xz)
   * [Opções de resposta](#c-localize-strings/section_zvt_qd4_xz)
   * [Notificador de comentários](#c-localize-strings/section_qqt_pd4_xz)
   * [Mensagens de erro](#c-localize-strings/section_omz_jxn_xz)

* [Formato de data e hora](#c-localize-strings/section_yz4_g5n_xz)
* [Mídia](#c-localize-strings/section_vwt_d5n_xz)
* [Mapa](#c-localize-strings/section_fxv_c5n_xz)
* [Mosaico](#c-localize-strings/section_e2s_b5n_xz)
* [Carrossel](#c-localize-strings/section_l2z_hkn_xz)
* [Placa de recurso](#c-localize-strings/section_mw2_hkn_xz)
* [Pesquisa](#c-localize-strings/section_pdg_fwh_xz)
* [Identidade do Livefyre](#c-localize-strings/section_zc3_xvh_xz)
* Mais:
   * [Rever strings de texto](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Sidenotes](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## Implementação {#section_im4_224_xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das strings que você deseja substituir para o objeto de configuração JavaScript. Se você não fornecer um campo, o texto padrão será usado.

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

Esta página lista todas as strings de texto que podem ser personalizadas para os aplicativos principais do Livefyre.

## Acesso à conta {#section_cm3_d24_xz}

Strings disponíveis para o processo de autenticação e nos menus de usuário autenticados.

![](assets/strings_threadheader-150x40.png)

| Elemento | Chave | Texto padrão |
|---|---|---|
|  | displayName | %s |
|  | editProfile | Editar perfil |
|  | notificationSettings | Configurações de notificação |
|  | siteAdmin | Admin Console (links para o Studio) |
|  | signOut | Sair |

## Informações de fluxo {#section_wx1_c24_xz}

Strings disponíveis para informações e exibição do fluxo de conteúdo. Lista o número de pessoas que estão ouvindo, o número de publicações no aplicativo e permite que os usuários façam logon ou acessem suas informações de conta.

| Chave | Texto padrão | Dados de fluxo |
|---|---|---|
|  | commentCountLabelZero | %s comentário |
|  | commentCountLabel | %s comentário |
|  | commentCountLabelPlural | %s comentários |
|  | listenerCount | pessoa ouvindo |
|  | listenerCountPlural | pessoas ouvindo |
|  | liveblogPostCountLabelZero | postar |
|  | liveblogPostCountLabel | postar |
|  | liveblogPostCountLabelPlural | posts |
| Opções de encadeamento | threadBreakoutButton | Mostrar todo o thread |
|  | toggleCollapse | Alternar Recolher |
| Comentários em fila/alta velocidade | atualizar | Atualizar |
|  | newComment | Novo comentário |
|  | newComments | Novos comentários |
|  | newReply | nova resposta |
|  | newReplies | novas respostas |

## Classificação de fluxo {#section_ih2_124_xz}

Permite que os usuários classifiquem o conteúdo retornado por idade ou popularidade.

![](assets/strings_newestoldesttop-1-150x56.png)

| Chave | Texto padrão | Opções de cabeçalho |
|---|---|---|
|  | sortNewest | Mais recente |
|  | sortOldest | Mais antiga |
|  | sortTopComments | Principais comentários |
|  | sortHotThreads | Threads instantâneos |
|  | sortSeparator |  |  |
|  | streamSorting | Carregando |
|  | topCommentsContentNotFoundMsg | Ainda não há curtidas suficientes. |
|  | hotThreadsContentNotFoundMsg | Ainda não há encadeamentos suficientes. |
|  | streamRefreshMsg | Veja as novidades. |
| Opções de rodapé | archiveHeaderTitle | Do arquivo |
|  | archiveShowMore | Mostrar mais |
|  | showMore | Mostrar mais comentários |
|  | showMoreLiveblog | Mostrar mais postagens |

![](assets/strings_threadend-150x47.png)

## Informações do conteúdo {#section_llv_yd4_xz}

Informações de publicação do Lista: nome de usuário, quaisquer tags de usuário aplicadas e tempo de postagem.

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| Chave | Texto padrão | Autor |
|---|---|---|
|  | moderador | moderador |
|  | hovercardViewProfile | Visualização Perfil completo |
| Informações da postagem | timeJustNow | agora mesmo |
|  | timeMinutsAgo | minuto atrás |
|  | timeMinutosAgoPlural | minutos atrás |
|  | timeHoursAgo | hora atrás |
|  | timeHoursAgoPlural | horas atrás |
|  | timeDaysAgo | dia atrás |
|  | timeDaysAgoPlural | dias atrás |
|  | LikePlural | Curtidas |
|  | LikeSingular | Curtir |
|  | moderatorEditTimestamp | Editado por um Moderador |
|  | commentTombstone | Este comentário foi excluído |
|  | permalinkNotFoundMsg | Este comentário não está mais visível. |
|  | quickProfileTooltip | Perfil rápido |

## Conteúdo em destaque {#section_gmw_vd4_xz}

Se ativado, o conteúdo em destaque é listado na parte superior do fluxo.

|  | Chave | Texto padrão |
|---|---|---|
| Etiquetas em destaque |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | featureCommentsTag | Em destaque |
|  | featureCommentsTitlePlural | Comentários em destaque |

## Editor de texto {#section_ky5_td4_xz}

Por padrão, disponível na parte superior da página para todos os usuários.

![](assets/strings_texteditor-1-150x77.png)

|  | Chave | Texto padrão |
|---|---|---| 
| Botões Editor | follow | + Seguir |
|  | unfollow | - Não seguir |
|  | liveblogfollow | Siga o Blog ao vivo |
|  | liveblogUnfollow | Cancelar a execução do Live Blog |
|  | postButton(Disponível para usuários conectados.) | Comentário da postagem |
|  | postAsButton(Disponível para usuários não autenticados.) | Publicar comentário como... |
|  | postEditButton | Editar comentário |
|  | postEditAsButton | Editar comentário como... |
|  | postEditCancelButton | Cancelar |
|  | editorDisabled | Esta conversa está atualmente fechada para novos comentários. |
| Opções de bate-papo | livechatPostButtonLabel | Publicar |
|  | livechatPostEditButton | Editar   |
|  | livechatWindowsInstruction | Pressione Ctrl+Enter para postar |
|  | livechatOtherInstruction | Pressione command+enter para postar |

## Opções de resposta {#section_zvt_qd4_xz}

Salvo indicação em contrário, disponível para todos os usuários conectados. Passe o mouse sobre um painel de conteúdo para acessá-lo.

![](assets/strings_banusermodal-150x36.png)

| Chave | Texto padrão |  |
|---|---|---|
| Opções de resposta do usuário | Disponível para usuários finais. |  |
| flagButton | Segnalato |
|  | flagCommentTooltip | Segnalato |
|  | editButton(Disponível somente para autores e moderadores, se ativado). | Editar   |
|  | deleteButton(Disponível somente para autores e moderadores, se ativado). | Excluir |
|  | deleteCommentTooltip | Excluir |
|  | shareButton | Compartilhar |
|  | shareCommentTooltip | Compartilhar |
|  | likeButton | Curtir |
|  | unlikeButton | Curtir (desfazer) |
|  | replyButton | Responder |
|  | replyButtonSingular(Disponível para bate-papo e Blog ao vivo.) | Responder |
|  | replyButtonPlural(Disponível para bate-papo e Blog ao vivo). | Respostas |

![](assets/strings_responseoptions-150x35.png)

| Chave | Texto padrão |  |
|---|---|---|
| Sinalizar modal | flagTitle | Sinalizar o comentário de %s |
|  | flagSubtitle | Sinalizar como |
|  | flagDefaultSelectOption | Selecionar |
|  | flagSpam | Spam |
|  | flagSpamButton | Spam |
|  | flagSpamCommentTooltip | Spam |
|  | flagOffensive | Ofensivo |
|  | flagOffensiveButton | Ofensivo |
|  | flagOffensiveCommentTooltip | Ofensivo |
|  | flagDisagree | Discordar |
|  | flagDisagreeButton | Discordar |
|  | flagDisagreeCommentTooltip | Discordar |
|  | flagOffTopic | Tópico desativado |
|  | flagOfftopicButton | Tópico desativado |
|  | flagOfftopicCommentTooltip | Tópico desativado |
|  | flagEmail | Email |
|  | flagEmailPlaceholder | you@example.com |
|  | flagNotes | Notas |
|  | flagNotesPlaceholder | Start digitando aqui... |
|  | flagConfirmButton | OK |
|  | flagCancelButton | Cancelar |
|  | flagConfirmationMessage | Sinalizar o comentário de %s como %s? |
|  | flagSuccessMsg | O comentário foi sinalizado. |

![](assets/strings_flagmodal-150x87.png)

| Chave | Texto padrão |  |
|---|---|---|
| Compartilhar modal | shareTitle | Comentário de compartilhamento |
|  | sharePlaceholderText | O que você acha? |
|  | shareLabel | Compartilhar em: |
|  | shareTextTwitter | em branco |
|  | shareTextFacebook | em branco |
|  | shareTextLinkedin | em branco |
|  | shareButtonText | Compartilhar |
|  | sharePermalink | Permalink |
|  | loadingPermalink | Carregando url curto... |
|  | shareText | Acabei de postar um comentário. Confira! |

![](assets/strings_sharemodal-150x59.png)

| Chave | Texto padrão |  |
|---|---|---|
| Resposta modal | postReplyAsButton | Publicar comentário como... |
|  | postReplyButton(Disponível para usuários conectados). | Comentário da postagem |
|  | backToHotThreads | Voltar para Threads Hot |

![](assets/strings_backto-150x48.png)

| Chave | Texto padrão |  |
|---|---|---|
| @menção no Twitter modal | referenceTitle | Menção de compartilhamento |
|  | saidSubtitleTwitter | Compartilhar tweet em: |
|  | referenceDefaultText | Mencionei-o num comentário do Livefyre! |
|  | referenceConfirmButton | OK |
|  | referenceCancelButton | Cancelar |
|  | referenceErrorGeneral | Oops! Algo deu errado! Livefyre foi alertado. |
|  | referenceErrorNoneSeleted | Você deve ter pelo menos uma menção ativada. |
|  | referenceMenuTitle | Para ver e mencionar seus amigos |
|  | mençãoTwitterConnect | Conectar-se ao Twitter |
|  | saidTwitterFetching | A Obter Amigos... |
|  | referenceSuccessMsg | As menções foram enviadas com êxito. |

![](assets/strings_sharemention-150x60.png)

| Chave | Texto padrão |  |
|---|---|---|
| Editar modal | Disponível para administradores do Studio, gerentes de usuários ou moderadores |  |
| @(@menção.) | &lt;/>(Abre a janela html personalizada.) |  |
|  | customHtmlDialogTitle(Aparece como o cabeçalho do modal.) | Adicionar HTML personalizado |

![](assets/strings_moderatoreditmodal-150x49.png)

| Chave | Texto padrão |  |
|---|---|---|
| Opções de resposta do moderador | Disponível para administradores do Studio, gerentes de usuário ou moderadores. |  |
| pendenteComment | pendente |
|  | banUserButton | Usuário da proibição |
|  | banUserTooltip | Usuário da proibição |
|  | bozoButton | Bozo |
|  | bozoCommentTooltip | Bozo |
|  | featureButton | Recurso |
|  | featureCommentTooltip | Recurso |
|  | unfeatureButton | Desrecurso |
|  | featureCommentTooltip | Desrecurso |

![](assets/strings_adminoptions-150x33.png)

| Chave | Texto padrão |  |
|---|---|---|
| modal Ban User | Disponível para administradores do Studio, gerentes de usuário ou moderadores. |  |
| banTitle | Usuário da proibição |  |
|  | banConfirmation | Tem certeza de que deseja proibir este usuário? |
|  | banConfirmButton | OK |
|  | banCancelButton | Cancelar |

## Notificador de comentários {#section_qqt_pd4_xz}

Se ativado, disponível na parte inferior da página para todos os aplicativos de conversação do Livefyre.

![](assets/strings_notifier-150x112.png)

|  | Chave | Texto padrão |
|---|---|---|
| Etiquetas do notificador | commentNotifier | Novo comentário |
|  | commentNotifierPlural | Novos comentários |
|  | liveblogNotifier | Nova postagem |
|  | liveblogNotifierPlural | Novas postagens |

## Mensagens de erro {#section_omz_jxn_xz}

Strings disponíveis para mensagens de erro personalizáveis.

| Chave | Texto padrão |
|---|---|
| errorAuthError | Você não está autorizado a postar um comentário nesta conversa |
| errorCommentsNotAllowed | Comentários não são permitidos nesta conversa |
| errorDefault | Ocorreu um erro. Tente novamente. |
| errorDuplicate | Por mais que você tenha gostado do seu comentário, não é permitido postá-lo duas vezes. |
| errorEditDuplicate | É necessário alterar o corpo do comentário ao editá-lo. |
| errorEditNotAllowed | Você não tem permissão para editar comentários nesta conversa. |
| errorEditTimeExceeded | Seu período de edição de comentários expirou. |
| errorEmpty | Parece que você está tentando postar um comentário vazio. |
| errorExpired | Sua sessão expirou. Recarregue a página. |
| errorFlagNotSeleted | Selecione um tipo de sinalizador. |
| errorGuestLiked | Só os que têm contas podem gostar de conteúdo. |
| errorInsuficientesPermissions | Permissões insuficientes |
| errorInvalidChar | Parece que você está tentando postar um caractere inválido. |
| errorLikeOwnComment | Você não pode curtir seu próprio comentário |
| errorMalformation | Parece que você está tentando publicar conteúdo malformado. |
| errorMaxChars | Desculpe, seu comentário é muito longo. Edite e tente novamente. |
| errorMediaNotAvailable | A mídia não está mais visível. |
| errorShowMore | Erro ao carregar mais comentários. |
| MultipleMediaNotAllowedError | Suas permissões concedem apenas um anexo de mídia por vez. |

## Formato de data e hora {#section_yz4_g5n_xz}

Traduza e personalize como as datas são exibidas nos cartões de conteúdo nos aplicativos de visualização.

| Chave | Texto padrão |
|---|---|
| horas atrás | {número}h |
| horasAgoSingular | {número}h |
| justNow | 1s |
| minutos atrás | {número} m |
| minutosAgoSingular | {número} m |
| monthDayFormat | {day} {monthAbbrev} |
| monthDayYearFormat | {day} {monthAbbrev} {year} |
| monthNames | Janeiro, Fevereiro, Março, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro |
| monthNamesAbbrev | Jan, Fev, Mar, Abr, Maio, Jun, Jul, Ago, Set, Out, Nov, Dez |
| segundosAgo | {number} s |
| secondAgoSingular | {number} s |

## Media Wall {#section_vwt_d5n_xz}

Strings disponíveis para o aplicativo Media Wall.

| Chave | Texto padrão |
|---|---|
| featureText | Em destaque |
| shareButtonText | Compartilhar |

| Chave | Texto padrão |
|---|---|
| postButtonText | O que você acha? |
| postModalTitle | Publicar seu comentário |
| postModalButton | Publicar seu comentário |
| postModalPlaceholder | O que você gostaria de dizer? |
| showMoreButtonText | Carregar mais |
| shareButtonText | Compartilhar |

## Mapa {#section_fxv_c5n_xz}

Strings disponíveis para Mapas.

| Chave | Texto padrão |
|---|---|
| featureText | Em destaque |
| shareButtonText | Compartilhar |

## Mosaico {#section_e2s_b5n_xz}

Strings disponíveis para mosaicos.

| Chave | Texto padrão |
|---|---|
| featureText | Em destaque |
| shareButtonText | Compartilhar |

## Carrossel {#section_l2z_hkn_xz}

Strings disponíveis para Carousel.

| Chave | Texto padrão |
|---|---|
| featureText | Em destaque |
| shareButtonText | Compartilhar |

## Placa de recurso {#section_mw2_hkn_xz}

Strings disponíveis para a placa de recurso.

| Chave | Texto padrão |
|---|---|
| featureText | Em destaque |
| shareButtonText | Compartilhar |

## Carregar aplicativo {#section_grc_gkn_xz}

Strings disponíveis para o aplicativo de upload.

| Chave | Texto padrão |
|---|---|
| postButtonText | O que você acha? |
| postModalTitle | Publicar seu comentário |
| postModalButton | Publicar seu comentário |
| postModalTitlePlaceholder | Inserir um título |
| postModalPlaceholder | O que você gostaria de dizer? |
| postModalConfirationTitle | Obrigado por postar! |
| postModalConfirmationMessage | Sua postagem está sendo revisada. |
| postModalConfirmationButton | Concluído |
| title |  |
| message |  |
| editorErrorAttachmentsRequired | É necessário um anexo |
| editorErrorBody | Adicione uma mensagem |
| editorErrorDuplicate | Por mais que goste da sua nota, não pode postá-la duas vezes |
| editorErrorGeneric | Houve um erro |
| editorErrorTitleRequired | Um título é obrigatório |

## Pesquisa {#section_pdg_fwh_xz}

Strings disponíveis para pesquisas.

| Chave | Texto padrão |
|---|---|
| totalVotesLabel | Total de votos de %s |
| shareStringText | Acabei de votar em %s qual é o seu voto? |
| pollClosedLabel | Esta pesquisa está atualmente fechada |

## Livefyre Identity {#section_zc3_xvh_xz}

Strings disponíveis para o Livefyre Identity.

| Chave | Texto padrão |
|--- |--- |
| automaticamenteSeguirConversações | Acompanhar automaticamente as conversas em que participo |
| back | Voltar |
| bio | Biografia |
| create | Criar  |
| createANewAccount | Criar nova conta |
| createNewAccountWithEmail | Criar uma nova conta com email |
| changeAvatar | Alterar avatar |
| choiceFile | Selecionar arquivo |
| completeAccount | Conta completa |
| emailWhenAlguémReplies | Enviar e-mail quando alguém me responder |
| emailCommentsIFollow | Enviar comentários por email em conversas que eu seguir |
| emailSenttoResetPassword | E-mail enviado! Procure na sua caixa de entrada um link para redefinir a senha |
| emailVerificationSent | Verificação de email enviada |
| firstName | Nome |
| EsqueciSenha | Esqueceu a senha? |
| EsqueciSuaSenha | Esqueceu sua senha? |
| EsqueciSuasInstruçõesDeSenha | Insira seu nome de usuário ou endereço de email abaixo e enviaremos um link para alterar sua senha. |
| formInputCloseButtonText | Close |
| formInputCancelButtonText | Cancelar |
| formInputSaveButtonText | Salvar |
| hasNotLeftAnyComments | não deixou nenhum comentário |
| locationIsFrom | é de |
| labelAvatar | Avatar |
| labelComments | Comentários |
| labelConfirmNewPassword | Confirmar nova senha |
| labelConfirmPassword | Confirmar senha |
| labelEmail | Email Address |
| labelLikes | Curtidas |
| labelLoading | Carregando |
| labelNewPassword | Nova senha |
| labelNotification | Notificações |
| labelPassword | Senha |
| labelProfile | Perfil |
| labelUsername | Nome de usuário |
| labelUsernameOrEmail | Nome de usuário ou email |
| lastName | Sobrenome |
| livefyreAccount | Conta Livefyre |
| localização | Localização |
| loadingProfile | Carregando Perfil |
| newPassword | Nova senha |
| oldPassword | Senha antiga |
| on | on |
| ou | ou |
| passwordLinkExpired | O link que você clicou para redefinir sua senha expirou. Redefina sua senha novamente e lhe enviaremos um novo link. |
| por favor, verifiqueEmailToComplete | Verifique seu e-mail para concluir a inscrição. |
| postado | Postado |
| powerBy | acionado por |
| profileNotificationImmediate | immediate |
| profileNotificationHhour | por hora |
| profileNotificationnever | never |
| recentComments | Comentários recentes |
| redefinir | Reset |
| resetPassword | Redefinir senha |
| signIn | Conectar |
| signInWith | Fazer logon com |
| signInWithEmail | Fazer logon com email |
| signUp | Inscreva-se |
| socialAccount | Conta social |
| successPasswordChanged | Sucesso! Sua senha foi alterada e agora você está conectado |
| termsAndConditions | Termos e condições |
| termsAndConditionsIntro | Ao se inscrever, você aceita a variável |
| termsOfUse | Termos de uso |
| termsOfUseIntro | Ao fazer logon, você concorda em |
| thisUser | Este usuário |
| verifyPassword | Verificar senha |
| fileSizeLimit | 2 MB máx |
| accountnotfound | Conta não encontrada |
| avatarImageExceedSize | Sua imagem de avatar excedeu o limite de arquivos 2mb |
| campo desnecessário | O campo aceita apenas um número inteiro |
| fieldonlyaccept tsavalidemail | O campo só aceita um email válido |
| fieldonlyaccept | O campo só aceita letras |
| filesizemustbelessthan MB | O tamanho do arquivo deve ser menor que {#}MB |
| invalidusernameorpassword | Nome de usuário ou senha inválidos |
| minimumlength thofacter | Comprimento mínimo de {#} caracteres |
| maximumlength thofcaracteres | Comprimento máximo de {#} caracteres |
| havia um erro | Houve um erro |
| este campo desnecessário | Esse campo é obrigatório. |
| validfileextensions | Extensões de arquivo válidas |
| valuemustmatch | O valor deve corresponder |
| passwordLength | ter entre 6 e 32 caracteres. |
| passwordCharacters | incluem caracteres em maiúsculas e minúsculas. |
| passwordSymbols | inclua pelo menos um número e um símbolo. |
| passwordUsername | não contém seu nome de usuário. |
| passwordPopoverTitle | Sua senha precisa: |
| passwordErrorContainsFirstName | A senha digitada contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, digite uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que sua senha precisa conter: De 6 a 32 caracteres Um caractere maiúsculo Um símbolo A de caractere minúsculo |
| passwordErrorContainsLastName | A senha digitada contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, digite uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que sua senha precisa conter: De 6 a 32 caracteres Um caractere maiúsculo Um símbolo A de caractere minúsculo |
| passwordErrorContainsUsername | A senha digitada contém seu nome de usuário, nome ou sobrenome. Por motivos de segurança, digite uma senha que não contenha seu nome de usuário, nome ou sobrenome. Lembre-se também de que sua senha precisa conter: De 6 a 32 caracteres Um caractere maiúsculo Um símbolo A de caractere minúsculo |
| passwordErrorTooShort | Mínimo de 6 caracteres para senha |
| passwordErrorTooLong | Máximo de 32 caracteres para senha |
| passwordErrorMissingUppercase | A senha deve conter pelo menos um caractere maiúsculo |
| passwordErrorMissingLowercase | A senha deve conter pelo menos um caractere minúsculo |
| passwordErrorMissingSymbol | A senha deve conter pelo menos um símbolo no conjunto `!@#$%^&*()?.,<>\’;:”[]{}|` |


