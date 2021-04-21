---
description: As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um aplicativo de revisão que corresponda às suas necessidades e identidade visual.
title: Criação de um aplicativo de revisões
exl-id: 14f074d2-922c-4997-8d7d-f2c92f069e07
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Criação de um aplicativo de revisão{#creating-a-reviews-app}

As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um aplicativo de revisão que corresponda às suas necessidades e identidade visual.

Use o aplicativo de Revisões ao incorporá-lo personalizado ao seu site como um aplicativo JS. Não é possível criar um aplicativo de Revisões no Livefyre Studio. Para criar um aplicativo de Revisões no site, consulte [Revisar integração](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Classificações {#section_hs5_c4h_21b}

As classificações são o valor numérico que seus usuários atribuem à Revisão. Cada Revisão deve incluir uma Classificação, que é mostrada como um sistema de 5 estrelas por padrão. (Embora as classificações sejam exibidas como 0,5 - 5 no aplicativo, o Livefyre armazena uma proporção de X/100 no back-end, de modo que 1 estrela é 20/100 e 2 estrelas é 40/100. Essa proporção é exibida ao visualizar as revisões no Studio.)

A escala de classificação de 0,5 a 5 pode ser configurada até uma classificação de 100, com meia classificação também disponível.

Para obter mais informações, consulte o campo maxRating para o objeto Reviews conig.

## Ícone de classificação de estilo {#section_cqn_c4h_21b}

Os ícones de classificação podem ser personalizados para se ajustarem à sua marca e estilo.

Para obter mais informações, consulte **[!UICONTROL Configure Star Ratings]** em Revisões de personalização.

## Dimension de classificação {#section_cnx_snh_21b}

As dimensões de classificação são as categorias sobre as quais seus revisores estão classificando seu produto ou serviço. Exemplos de dimensões de classificação são &quot;desempenho&quot;, &quot;design&quot;, &quot;custo&quot;, &quot;geral&quot; ou qualquer outra categoria escolhida.

O padrão é exibir uma dimensão de classificação &quot;geral&quot;, no entanto, você pode definir e implementar várias dimensões de classificação, conforme exibido no exemplo abaixo.

Para obter mais informações, consulte o campo ratingDimensions em Revisar metadados da coleção.

## Revisar campos de texto {#section_xcm_4nh_21b}

Você também pode incluir campos de texto adicionais sobre o produto ou experiência que está sendo analisada. (Por exemplo, os campos de texto podem incluir Vantagens e desvantagens ou Não faltar.) O número, o título e o texto padrão do campo são personalizáveis. Os usuários deverão preencher todos os campos de texto, bem como o título da revisão, o corpo e a classificação, para publicar sua análise. Não é possível incluir campos de texto opcionais.

Para obter mais informações, consulte o campo ratingDimensions para Revisar metadados da coleção.

## Resumo da revisão {#section_ysz_lnh_21b}

Por padrão, uma seção de resumo é exibida na parte superior do Aplicativo de revisões. Esta seção inclui uma visualização da Classificação média de usuário e o Detalhamento de classificação da coleção de revisões, exibindo somente números inteiros. Esta seção é somente leitura e pode ser ocultada, se desejado.

Para obter mais informações, consulte o campo ratingSummaryEnabled para o objeto ConfirmReviews .

## Filtro de spam e lucratividade {#section_hcm_jnh_21b}

O texto do Título e do Corpo de uma Revisão é passado por nosso Filtro de Spam e Filtro de Profanação assim que a Revisão é postada.

## Personalização de texto {#section_tjf_hnh_21b}

As cadeias de texto, incluindo dicas de ferramentas e rótulos, podem ser personalizadas para idioma ou para se adequarem à sua marca.

## Respondendo a uma revisão {#section_yng_fnh_21b}

Os usuários podem responder à sua própria análise ou à de outra em cada coleção de revisões. Somente os usuários conectados podem postar uma resposta em uma revisão.

A opção para os usuários responderem a uma Revisão está ativada no Studio. Os proprietários podem alternar essa configuração para o nível Rede, Site ou Coleção. Os moderadores podem ativar essa configuração somente para suas Coleções.

## SocialSync e Preparar {#section_llh_2nh_21b}

Como as Revisões são projetadas para adicionar um valor numérico para cada parte do conteúdo enviado, o SocialSync e a Preparar não são compatíveis com as Revisões.

## Revisa APIs {#section_xrh_wmh_21b}

As APIs de revisão estão disponíveis para permitir que você exiba informações de classificação média do usuário e análise de classificação e atividade do usuário em outras seções do site.

[Avaliações e revisões](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** O Ponto de extremidade da API do Bootstrap permite que sua análise seja lida por mecanismos de pesquisa como o Google, de modo que o conteúdo e as palavras-chave possam melhorar a otimização do mecanismo de pesquisa.

* **[!UICONTROL Average User Ratings]** A API de Classificações Médias de Usuário recupera a classificação média de usuário para uma ou mais Coleções de Revisões, permitindo que você crie uma visualização dessas informações em uma página de índice ou adicione a uma página de índice de pesquisa.

* **[!UICONTROL Ratings Breakdown]** A API Análise de classificações recupera um detalhamento de todas as classificações para uma coleção de revisões específica e permite criar uma visualização que exibe o número de revisões associadas a cada classificação de estrelas.

* **[!UICONTROL User Reviews]** A API de Revisões do Usuário recupera as revisões mais recentes de um usuário específico. Essa atividade pode ser usada para exibir as revisões de um usuário em sua página de perfil público.
