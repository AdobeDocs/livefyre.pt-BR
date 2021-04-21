---
description: Notas de versão para 9 de fevereiro de 2017.
title: 9 de fevereiro de 2017
exl-id: 155f8a43-17e5-40b2-ada0-32691f8a34e5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 5%

---

# 9 de fevereiro de 2017{#february}

Notas de versão para 9 de fevereiro de 2017.

## SocialSync para Twitter {#section_nv4_yry_wy}

O SocialSync for Twitter faz parte de nossa funcionalidade principal há vários anos. No entanto, à medida que nosso produto se desenvolveu e cresceu com o tempo, o SocialSync for Twitter se tornou um recurso de valor mais baixo que é usado atualmente por uma porção muito pequena de nossa base de clientes. Para melhorar a experiência geral do Livefyre para nossos clientes e concentrar os recursos de desenvolvimento em áreas de maior valor, desativaremos o recurso SocialSync for Twitter em 24 de fevereiro. O SocialSync para Facebook não será afetado por esta atualização. Em caso de dúvidas ou preocupações sobre essa atualização, entre em contato com o Livefyre CSM.

## Versão de produção {#section_r24_1m2_wy}

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Bug | Mural de mídia | Correção de um bug que permitia que os vídeos do Facebook fossem reproduzidos adequadamente. |
| Bug | ModQ | Correção de um erro que impedia que Objetos de email não fossem exibidos no Conteúdo de fluxo de email. |
| Bug | Mosaico | Adição de suporte adicional de acessibilidade ao Mosaic para permitir que os usuários alternem a guia entre cartões de conteúdo. |
| Bug | Resenhas | Correção de um erro que impedia que as edições de classificação fossem exibidas corretamente. |
| Bug | Pesquisa social | Correção de um erro que fazia com que o botão Mostrar mais fosse cortado nos resultados da Pesquisa em lista do Twitter. |
| Aprimoramento | Storify 2 | Aprimoramento do Storify 2 para oferecer suporte à pesquisa de conteúdo com gravação livre de cópias. Copywrite Free pesquisa no Flickr, Noun Project, Kuler, Pixabay e Unsplash para copiar imagens gratuitas. |
| Bug | Fluxos | Correção de um erro que impedia que as regras de fluxo do Tumblr fossem salvas. |
| Bug | Fluxos | Correção de um bug que gerava Ids do gerador incorretas no JSON da coleção para feeds RSS. |
| Aprimoramento | Fluxos | Foi feito um ajuste na configuração da opção &quot;Somente contas verificadas&quot; para ser desativada por padrão. |
| Aprimoramento | Fluxos | Adição de um novo recurso para permitir que categorias de conteúdo (por meio de uma Regra de fluxo) sejam incluídas na lista de permissões e ignorem a moderação. |
| Bug | Fluxos | Correção de um erro que fazia com que as configurações &quot;Premoderate&quot; e &quot;Media Premoderate&quot; fossem transferidas para uma regra de fluxo recém-criada. |

## Versão UAT {#section_dyx_yl2_wy}

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Bug | Aplicativos de conversa | Aprimoramento dos aplicativos de conversa para sempre vincularem aos perfis de usuário, mesmo sem uma integração completa de autenticação. |
| Bug | Mosaico | Correção de um bug que agora disponibiliza todas as imagens do Twitter por HTTPS. |
| Bug | Pesquisa social | Correção de um erro que fazia com que a marca de seleção verde &quot;salva&quot; não fosse exibida ao salvar ativos na Pesquisa social e visualizar ativos na Biblioteca. |
| Bug | Pesquisa social | Correção de um erro que impedia o funcionamento correto da opção &quot;Ocultar imagens explícitas&quot;. |
| Aprimoramento | Storify 2 | Aprimoramento do Storify 2 para oferecer suporte a permalinks que abrem um modal (antes, o aplicativo rolava para o local de publicação na página). No Designer do Storify 2, adicionamos uma configuração para alternar entre o comportamento de Rolagem e de Link manual modal. O comportamento do permalink modal será o comportamento padrão. |
| Aprimoramento | Storify 2 | Aprimoramento da integração do Storify 2 Google AMP para produzir um arquivo CSS menor. |
| Bug | Fluxos | Conteúdo aprimorado (imagens e vídeos) das Regras de fluxo de email a serem disponibilizadas via HTTPS. |
| Bug | Fluxos | Adição de um rótulo para o Valor do Raio da compilação em mapas nas Regras de fluxo do Twitter. |
| Bug | Fluxos | Correção de um bug com Regras de fluxo de página do Facebook e Facebook para inserir publicações com vários anexos de mídia adequadamente. |
| Bug | Studio | Correção de um erro que fazia com que vários &amp;&#39;s não fossem anexados ao URL ao usar filtros no Studio. |
| Bug | Studio | Correção de um erro que impedia que determinadas caixas de seleção nos filtros do Studio fossem desmarcadas. |
