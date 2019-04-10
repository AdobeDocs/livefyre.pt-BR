---
description: Os conjuntos de traduções permitem especificar idioma alternativo para
  aplicativos.
seo-description: Os conjuntos de traduções permitem especificar idioma alternativo
  para aplicativos.
seo-title: Conjuntos de tradução
solution: Experience Manager
title: Conjuntos de tradução
uuid: 88 b 705 e 5-57 c 8-4065-8 a 41-a 73546 bd 929 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Conjuntos de tradução{#translation-sets}

Os conjuntos de traduções permitem especificar idioma alternativo para aplicativos.

Use as configurações de tradução para localizar aplicativos em vários idiomas ou especificar texto alternativo para vários aplicativos de um local no Studio. Por exemplo, você pode garantir que todos os sites do idioma espanhol usem idiomas espanhol para todos os campos do aplicativo. Você também pode modificar o texto para que todos os campos correspondam à voz e ao comportamento do site ou rede.

Você pode especificar configurações de tradução para todos os aplicativos, exceto o Storify 2. Para obter mais informações sobre quais campos você pode localizar, consulte [Localizar strings](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Comentários, Blog ao vivo e Bate-papo compartilham o mesmo conjunto de sequências de caracteres dentro de um conjunto de traduções.

Especifique um conjunto de traduções para uma rede, um site, um aplicativo ou uma API.

Os conjuntos de traduções em níveis diferentes substituem-se entre si seguindo este padrão:

O conjunto de traduções da API substitui quaisquer conjuntos de traduções em qualquer nível (aplicativo, rede e site),
sobrescrevendo o conjunto de traduções de nível de rede e de site.
Os conjuntos de conversão de nível de site substituem os conjuntos de traduções de nível de rede.

## Revisar strings de texto {#c_review_text_strings}

Personalização das strings de texto para Revisões do Livefyre.

Esta página lista e descreve as strings disponíveis para personalização nos aplicativos Revisão. As strings listadas aqui são além das substituições padrão para os principais aplicativos do Livefyre, listadas em Personalizações de sequência de caracteres. Quando as duplicatas são listadas, as strings listadas nessas tabelas são o padrão para aplicativos de Revisão.

Erros de análise
de implementação/Autor
das
informações do fluxo de classificação/Informações
do usuário das informações
de publicação de conteúdo

## Implementação {#section-vsy-1k4-xz}

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das sequências de caracteres que deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

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

## Interface de avaliação/classificação {#section_iyv_zj4_xz}

Strings disponíveis para a interface de usuário Revisar e Classificação.

| Elemento | Chave | Texto padrão |
|--- |--- |--- |
| Botões | Editreviewbtn | Editar revisão |
|  | Reviewbtn | Gravar revisão |
|  | Reviewsclosed | Revisões encerradas |
|  | Showreviewbtn | Mostrar revisão |
|  | follow | Estou interessado |
|  | Sharetext | Acabei de escrever uma revisão. Confira! |
| Dicas de ferramentas de classificação | Ratingvalues | Uma matriz. Padrão = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Observação: Os valores na matriz devem ser duplicados para atribuir à metade esquerda e à direita de cada estrela o mesmo nome. |
| Subpartes de classificação | Ratingsubpartplaceholders | Uma matriz. Padrão = [] |
|  | Ratingsubparttitles | Uma matriz. Padrão = [] |
|  | Reviewstreamtitle | Em branco, por padrão. Título da seção de resumo da revisão. |
| Misc | Averagerating | Classificação média do usuário |
|  | Breakdownheader | Detalhamento da classificação |
|  | helpful | % s de % s encontrado útil |
|  | Helpfulplural | % s de % s encontrado útil |
|  | Saída | / |
|  | Ratingtype | star |

## Informações de fluxo {#section_wmv_yj4_xz}

Strings disponíveis para informações de fluxo de conteúdo e exibição.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Classificação | Sortby | *Em branco, por padrão.* |
|  | Sorthighestrated | [Classificação mais alta](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Classificação mais baixa](https://d.pr/i/huTd) |
|  | Sortmosthelpous | [Mais úteis](https://d.pr/i/huTd) |
| Fluxo contínuo. | Showmais | Mostrar mais |
| Fluxo de velocidade alta | Newcomment | Nova revisão |
|  | Newcomments | Novas revisões |
| Contador de escuta | Listenercount | pessoa que ouve |
|  | Listenercountplural | pessoas que escutam |
| Contagens de comentário | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelplural | Livereviews<strong> | </strong>% s |
| Contagens de notificador de comentário | Commentnotificador | Nova revisão |
|  | Commentnotificerplural | Novas revisões |

## Informações do autor/conteúdo {#section_osx_xj4_xz}

As classificações disponíveis para o autor e informações de conteúdo individual.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Sessão de grupo de grupo | Reviewscontentnotfoundmsg | [Esta revisão não está mais visível](https://d.pr/i/svXs) |
|  | Backtocomments | Voltar para revisões |

## Ações do usuário {#section_tlx_wj4_xz}

Strings disponíveis para ações do usuário: sinalizar, compartilhar e marcar conteúdo existente como útil.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Rodapé de comentário | Wasreviewhelpous | [Útil?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Útil? |
|  | Ownwasreviewhelpous | [Encontrado útil.](https://d.pr/i/Q0mA) |
|  | Reviewwashelpful | [Sim](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpous | [Não](https://d.pr/i/Q0mA) |
| Voto modal | Expressetitle | Essa revisão foi útil? |
|  | Votedownvotem | Não |
|  | Votereplytitle | Essa resposta foi útil? |
|  | Expressetitle | Esse comentário foi útil? |
|  | Manifesteupvotem | Sim |
| Sinalizar modal | Flagtitle | Análise % s do sinalizador |
|  | Flagsuccessmsg | A revisão foi sinalizada. |
| Sinalizar dispositivo móvel | Flagconfirmmationmessage | % s análise de % s como % s? |
| Menção modal | Mentiondefaulttext | Eu mencionei você em uma revisão do Livefyre! |
| Compartilhar modal | Sharetitle | Análise de compartilhamento |

## Funções de postagem {#section_yl1_wj4_xz}

Strings disponíveis para usuários que postam revisões.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Editor | Bodyplaceholder | Gravar revisão… |
|  | Posteditbutton | Editar |
|  | Posteditcancelbutton | Cancelar |
|  | Postasbutton | Revisar revisão como… |
|  | Postbutton | Revisão posterior |
|  | Postreplyasbutton | Publicar como… |
|  | Postreplybutton | Postagem |
|  | Sharebutton | Compartilhar |
|  | Titleplaceholder | Título… |

## Erros {#section_jbc_vj4_xz}

Strings disponíveis para mensagens de erro gerais.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Erros | Erroralreadyposted | Você só pode postar uma revisão. |
|  | Errorautherror | Você não está autorizado a postar uma revisão nesta conversa |
|  | Errorcommentsnotallowed | As revisões não podem ser publicadas neste momento |
|  | Errordislikeowncomment | Não é possível desabilitar sua própria revisão |
|  | Errorduplicate | Assim que você curtiram sua revisão, você não tem permissão para postá-la duas vezes. |
|  | Erroreditduplicate | Você deve alterar o corpo da revisão ao editá-lo. |
|  | Erroreditnotallowed | Você não tem permissão para editar revisões nesta conversa. |
|  | Erroredittimeexceeded | O período de edição da revisão expirou. |
|  | Errorempty | Parece que você está tentando postar uma revisão vazia. |
|  | Erroremptytitle | Parece que você está tentando postar um título vazio |
|  | Errorfieldrating | classificação de estrela |
|  | Errorfieldreview | review |
|  | Errorfieldtitle | title |
|  | Signatmaxchars | Sua revisão é muito longa. Edite e tente novamente. |
|  | Errormissingfields | Insira uma |
|  | Errorratingempty | Não é possível enviar uma classificação vazia |
|  | Errorratingnotset | Todas as classificações devem ser definidas |
|  | Errorratingnotvalid | A classificação deve ser um objeto |
|  | Errorshowmais | Ocorreu um erro ao carregar mais revisões. |
|  | Errortitlemaxchars | Seu título é muito longo. Edite e tente novamente. |
|  | Errorvoteowncomment | Não é possível votar sua própria revisão |

## Vincular strings de texto {#c_sidenotes_text_strings}

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
|  | Datetimemonths | Uma matriz. Padrão =[ ' janeiro ',' fevereiro ',' março ',' abril ',' maio ',' junho ',' julho ',' agosto ',' setembro ',' novembro ',' novembro ',' dezembro ' ] |
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

