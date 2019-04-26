---
description: Personalização das strings de texto para Revisões do Livefyre.
seo-description: Personalização das strings de texto para Revisões do Livefyre.
seo-title: Revisar strings de texto
solution: Experience Manager
title: Revisar strings de texto
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Revisar strings de texto{#review-text-strings}

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
|  | Reviewbtn | [Gravar revisão](https://d.pr/i/QscA) |
|  | Reviewsclosed | [Revisões encerradas](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [Mostrar revisão](https://d.pr/i/onxU) |
|  | follow | Estou interessado |
|  | Sharetext | Acabei de escrever uma revisão. Confira! |
| Dicas de ferramentas de classificação | Ratingvalues | Uma matriz. Padrão = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Observação: Os valores na matriz devem ser duplicados para atribuir à metade esquerda e à direita de cada estrela o mesmo nome. |
| Subpartes de classificação | Ratingsubpartplaceholders | Uma matriz. Padrão = `[]` |
|  | Ratingsubparttitles | Uma matriz. Padrão = `[]` |
|  | Reviewstreamtitle | Em branco, por padrão. Título da seção de resumo da revisão. |
| Misc | Averagerating | [Classificação média do usuário](https://d.pr/i/QscA) |
|  | Breakdownheader | [Detalhamento da classificação](https://d.pr/i/QscA) |
|  | helpful | % s de % s encontrado útil |
|  | Helpfulplural | % s de % s encontrado útil |
|  | Saída | / |
|  | Ratingtype | star |

## Informações de fluxo {#section_wmv_yj4_xz}

Strings disponíveis para informações de fluxo de conteúdo e exibição.

| Elemento | Chave | Texto padrão |
|---|---|---|
| Classificação | Sortby | Em branco, por padrão. |
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

