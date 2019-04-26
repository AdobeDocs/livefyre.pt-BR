---
description: As revisões oferecem uma ampla variedade de personalizações, permitindo
  que você crie um Aplicativo de revisão que corresponda às suas necessidades e marca.
seo-description: As revisões oferecem uma ampla variedade de personalizações, permitindo
  que você crie um Aplicativo de revisão que corresponda às suas necessidades e marca.
seo-title: Criar um aplicativo de revisão
solution: Experience Manager
title: Criar um aplicativo de revisão
uuid: 6 caeafe 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo de revisão{#creating-a-reviews-app}

As revisões oferecem uma ampla variedade de personalizações, permitindo que você crie um Aplicativo de revisão que corresponda às suas necessidades e marca.

Use o Aplicativo de revisão por incorporação personalizada no site como um aplicativo JS. Não é possível criar um Aplicativo de revisão no Livefyre Studio. Para criar um Aplicativo de revisão em seu site, consulte [Integração de revisões](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Classificações {#section_hs5_c4h_21b}

As classificações são o valor numérico que seus usuários atribuem à Revisão. Cada revisão deve incluir uma Classificação, que é exibida como um sistema de star estrela por padrão. (Enquanto as classificações são exibidas como 0.5 - 5 no aplicativo, o Livefyre armazena uma proporção de X/100 no backend, de tal forma que 1 estrela é 20/100 e 2 estrelas é 40/100. Essa proporção é exibida ao exibir as revisões no Studio.)

A escala de classificação de 0.5 a 5 pode ser configurada até uma classificação de 100, com meia classificação também disponível.

Para obter mais informações, consulte o campo maxrating para o objeto Reviews convig.

## Estilo do ícone de classificação {#section_cqn_c4h_21b}

Os ícones de classificação podem ser personalizados para se ajustar à marca e ao estilo.

Para obter mais informações, consulte **[!UICONTROL Configure Star Ratings]** em Revisões personalização.

## Dimensões de classificação {#section_cnx_snh_21b}

As dimensões de classificação são as categorias sobre as quais seus revisores classificam seu produto ou serviço. Exemplos de dimensões de classificação são «desempenho», «design», «custo», «geral» ou qualquer outra categoria escolhida.

O padrão é exibir uma dimensão de classificação "geral", no entanto, você pode definir e implementar várias dimensões de classificação, como mostrado no exemplo abaixo.

Para obter mais informações, consulte o campo ratingdimensões em Analisar metadados de coleção.

## Revisar campos de texto {#section_xcm_4nh_21b}

Você também pode incluir campos de texto adicionais sobre o produto ou experiência que está sendo analisada. (Por exemplo, campos de texto podem incluir Pros e Cons, ou Não.) O número, o título e o texto padrão do campo são personalizáveis. Os usuários serão solicitados a preencher todos os campos de texto, assim como o título, o corpo e a classificação da revisão, para publicar sua revisão. Não é possível incluir campos de texto opcionais.

Para obter mais informações, consulte o campo ratingdimensões para os Metadados de coleção de revisão.

## Resumo da análise {#section_ysz_lnh_21b}

Por padrão, uma seção de resumo é exibida na parte superior do Aplicativo de revisões. Esta seção inclui uma visualização da Classificação média do usuário e Detalhamento de classificação para a Coleção de revisões, exibindo apenas números inteiros. Esta seção é somente leitura e pode ser ocultada se desejar.

Para obter mais informações, consulte o campo ratingsummaryenabled para o objeto Reviews convconfig.

## Filtro de spam e profanidade {#section_hcm_jnh_21b}

O texto de Título e Corpo de uma revisão é passado pelo Filtro de spam e Filtro de profanidade assim que a Revisão é publicada.

## Personalização de texto {#section_tjf_hnh_21b}

As sequências de texto, incluindo dicas de ferramentas e rótulos, podem ser personalizadas para idioma ou para ajustar sua marca.

## Responder a uma revisão {#section_yng_fnh_21b}

Os usuários podem responder a sua própria Revisão em cada Collection Collection. Somente os usuários conectados podem postar uma resposta para uma revisão.

A opção para que os usuários respondam a uma Revisão é ativada no Studio. Os proprietários podem alternar essa configuração para o nível Rede, Site ou Coleção. Os moderadores podem ativar essa configuração somente para suas Coleções.

## Socialsync e Preparar {#section_llh_2nh_21b}

Como as Revisões são projetadas para adicionar um valor numérico para cada parte do conteúdo enviado, o socialsync e a Preparação não são compatíveis com as Revisões.

## Apis de revisão {#section_xrh_wmh_21b}

As apis de revisão estão disponíveis para permitir a exibição de informações médias de classificação do usuário e análise de classificação, bem como a atividade de análise de usuário em outras seções do site.

[Classificações e revisões](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** O Endpoint da API de bootstrap permite que a revisão seja lida por mecanismos de pesquisa, como Google, para que o conteúdo e as palavras-chave possam melhorar a otimização do mecanismo de pesquisa.

* **[!UICONTROL Average User Ratings]** A API de Classificação média de usuário recupera a classificação média do usuário de uma ou mais Coleções, permitindo criar uma visualização dessas informações em uma página de índice ou adicionar a uma página de índice de pesquisa.

* **[!UICONTROL Ratings Breakdown]** A API de Detalhamento de Classificações recupera o detalhamento de todas as classificações de uma Coleção de revisões específica e permite criar uma visualização que exibe o número de revisões associadas a cada classificação de estrela.

* **[!UICONTROL User Reviews]** A API de revisão do usuário recupera as revisões mais recentes de um usuário específico. Essa atividade pode ser usada para exibir as revisões de um usuário na página de perfil pública.
