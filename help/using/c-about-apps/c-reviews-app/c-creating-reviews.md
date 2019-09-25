---
description: As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um aplicativo de revisão que atenda às suas necessidades e marcas.
seo-description: As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um aplicativo de revisão que atenda às suas necessidades e marcas.
seo-title: Criação de um aplicativo de revisões
solution: Experience Manager
title: Criação de um aplicativo de revisões
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criação de um aplicativo de revisões{#creating-a-reviews-app}

As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um aplicativo de revisão que atenda às suas necessidades e marcas.

Use o aplicativo de revisões ao incorporá-lo personalizado ao seu site como um aplicativo JS. Não é possível criar um aplicativo de revisões no Livefyre Studio. Para criar um aplicativo de revisões em seu site, consulte Integração [de](/help/implementation/c-app-integrations/c-reviews-integration.md)revisões.


## Classificações {#section_hs5_c4h_21b}

As classificações são o valor numérico que os usuários atribuem à Revisão. Cada Revisão deve incluir uma Classificação, que é mostrada como um sistema de 5 estrelas por padrão. (Embora as classificações sejam exibidas de 0,5 a 5 no aplicativo, o Livefyre armazena uma proporção de X/100 no backend, de modo que 1 estrela é 20/100 e 2 estrelas é 40/100. Essa proporção é exibida ao exibir as revisões no Studio.)

A escala de classificação de 0,5 a 5 pode ser configurada até uma classificação de 100, com metade das classificações também disponíveis.

Para obter mais informações, consulte o campo maxRating para o objeto Reviews consoleConfig.

## Estilo do ícone de classificação {#section_cqn_c4h_21b}

Os ícones de classificação podem ser personalizados para se ajustarem à sua marca e estilo.

Para obter mais informações, consulte **[!UICONTROL Configure Star Ratings]** em Revisões personalizadas.

## Dimensões de classificação {#section_cnx_snh_21b}

Dimensões de classificação são as categorias sobre as quais seus revisores estão classificando seu produto ou serviço. Exemplos de dimensões de classificação são "desempenho", "design", "custo", "geral" ou qualquer outra categoria escolhida.

O padrão é exibir uma dimensão de classificação "geral", no entanto, você pode definir e implementar várias dimensões de classificação, conforme exibido no exemplo abaixo.

Para obter mais informações, consulte o campo ratingDimensions em Revisar metadados da coleção.

## Revisar campos de texto {#section_xcm_4nh_21b}

Você também pode incluir campos de texto adicionais no produto ou experiência que está sendo revisada. (Por exemplo, os campos de texto podem incluir Pros e Cons ou Não perder.) O número, o título e o texto padrão do campo são personalizáveis. Os usuários deverão preencher todos os campos de texto, bem como o título da revisão, o corpo e a classificação, para publicarem sua revisão. Não é possível incluir campos de texto opcionais.

Para obter mais informações, consulte o campo ratingDimensions para Analisar Metadados de Coleta.

## Resumo da revisão {#section_ysz_lnh_21b}

Por padrão, uma seção de resumo é exibida na parte superior do aplicativo de revisões. Esta seção inclui uma visualização da Classificação Média de Usuário e o Detalhamento da Classificação para a Coleção de Revisões, exibindo somente números inteiros. Esta seção é somente leitura e pode ser ocultada se desejar.

Para obter mais informações, consulte o campo ratingSummaryEnabled para o objeto Concig de revisões.

## Filtro Spam e Profanação {#section_hcm_jnh_21b}

O texto do Título e do Corpo de uma Revisão é passado pelo Filtro de Spam e pelo Filtro de Profanação assim que a Revisão é publicada.

## Personalização de texto {#section_tjf_hnh_21b}

As strings de texto, incluindo dicas de ferramentas e rótulos, podem ser personalizadas para idioma ou para se ajustar à sua marca.

## Respondendo a uma revisão {#section_yng_fnh_21b}

Os usuários podem responder à sua própria revisão ou à de outra em cada coleção de revisões. Somente os usuários conectados podem postar uma resposta para uma revisão.

A opção para os usuários responderem a uma Revisão está ativada no Studio. Os proprietários podem alternar essa configuração para o nível Rede, Site ou Coleção. Os moderadores podem ativar essa configuração somente para suas coleções.

## SocialSync e Preparar {#section_llh_2nh_21b}

Como as Revisões são projetadas para adicionar um valor numérico para cada parte do conteúdo enviado, o SocialSync e o Curate não são compatíveis com as Revisões.

## Revisões de APIs {#section_xrh_wmh_21b}

As APIs de revisão estão disponíveis para permitir que você exiba a classificação média do usuário e as informações de detalhamento de classificação e a atividade de análise do usuário em outras seções do site.

[Classificações e revisões](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** O Ponto Final da API do Bootstrap permite que sua revisão seja lida por mecanismos de pesquisa como o Google, para que o conteúdo e as palavras-chave possam melhorar a otimização do mecanismo de pesquisa.

* **[!UICONTROL Average User Ratings]** A API de Classificações Médias de Usuário recupera a classificação média de usuário para uma ou mais Coleções de Revisões, permitindo que você crie uma visualização dessas informações em uma página de índice ou adicione a uma página de índice de pesquisa.

* **[!UICONTROL Ratings Breakdown]** A API Detalhamento de classificações recupera um detalhamento de todas as classificações de uma coleção de revisões específica e permite criar uma visualização que exibe o número de revisões associadas a cada classificação de estrela.

* **[!UICONTROL User Reviews]** A API de revisões do usuário recupera as revisões mais recentes de um usuário específico. Essa atividade pode ser usada para exibir as revisões de um usuário em sua página de perfil público.
