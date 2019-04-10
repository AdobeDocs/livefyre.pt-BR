---
description: O Mecanismo de filtragem de spam e abuso do Livefyre (SAFE) é um processo
  em segundo plano que analisa todo o conteúdo recebido e está ativado para todos
  os clientes do Livefyre.
seo-description: O Mecanismo de filtragem de spam e abuso do Livefyre (SAFE) é um
  processo em segundo plano que analisa todo o conteúdo recebido e está ativado para
  todos os clientes do Livefyre.
seo-title: Regras SEGURAS
title: Regras SEGURAS
uuid: 2 f 91 d 0 d 4-dffe -4651-88 af -79 bbb 96 c 1 b 5 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Regras SEGURAS{#safe-rules}

O Mecanismo de filtragem de spam e abuso do Livefyre (SAFE) é um processo em segundo plano que analisa todo o conteúdo recebido e está ativado para todos os clientes do Livefyre.



O SAFE usa regras de padrão e modelos estatísticos para detectar postagens de spam, abuso, profanidade e massa (repetitiva). Você verá a referência ocasionalmente em outros produtos do Livefyre, especialmente as ferramentas de moderação e modq de conteúdo.

>[!NOTE]
>
>SAFE é somente inglês, exceto para a classificação por email em massa. Se precisar de suporte para outros idiomas, entre em contato com seu Gerente de contas estratégicas.

## Componentes do Studio usando SAFE {#section_k34_4tx_vy}

Sinalizadores aplicados por SAFE podem ser usados com os seguintes componentes do Studio:

* Regras

   É possível definir regras SEGURAS para sinalizar automaticamente o conteúdo e definir como o conteúdo sinalizado deve ser manipulado no **[!UICONTROL Network Settings]**.

   Por exemplo, um site pode definir uma tolerância muito baixa para Profanity e definir Regras SEGURAS que definem todo o conteúdo sinalizado como Profane para ser Bozo. Outros sites podem definir Regras que definem o conteúdo Profane para ser pré-moderado antes de entrar no stream.

* Modq

   É possível moderar o conteúdo sinalizado pelas regras SAFE e outras regras de moderação (por exemplo, SPAM, profanidade etc.), no modq.

* Conteúdo do aplicativo na biblioteca

   O conteúdo sinalizado pelo SAFE é listado no Conteúdo do aplicativo na **[!UICONTROL Library]** guia. É possível filtrar o conteúdo por sinalizadores para moderar o conteúdo.

## Opções de filtragem SEGURA {#section_pg5_ttx_vy}

O SAFE aplica os seguintes sinalizadores ao conteúdo filtrado e pode ser usado para criar regras e moderar o conteúdo no Livefyre Studio.

* **[!UICONTROL Profanity List]**: Conteúdo profane, conforme definido por uma lista de palavras-chave em inglês, com base em uso comum.

   O Filtro de profanidade procura por idioma profane, com base em uma lista de palavras testada. Se detectado, o conteúdo é Sinalizado sinalizado.

   >[!NOTE]
   >
   >O Livefyre também fornece um segundo filtro Lista de perfis, que pode ser personalizado nos níveis de Site e Rede. As regras criadas com a Lista de perfis terão precedência sobre regras automatizadas derivadas do filtro de Profanity SAFE. Para obter mais informações, consulte a seção Lista de perfis na documentação Configurações.

* **[!UICONTROL Mild Profanity]**: Palavras e frases geralmente não são aceitáveis em conversas polas, mas geralmente são aceitáveis em conversas casuais. Geralmente, essas palavras e frases são permitidas na televisão de rede.
* **[!UICONTROL Strong Profanity]**: Idioma muito forte, como expletives e frases não permitidos na televisão de rede e usado discretamente em filmes classificados e em telas de TV cabo maduras. Geralmente, essas palavras não são usadas na conversa ou conversa casual e são informadas em uma conversa de impolite com o objetivo de prejudicar o ouvinte.
* **[!UICONTROL SPAM]**: Conteúdo não solicitado, geralmente comercializado. Ele usa um modelo estatístico que depende de uma variedade de recursos (incluindo o conteúdo de comentário e urls) para sinalizar um conteúdo como SPAM. Você pode ajustar os limites de spam para personalizar as taxas de marcação de SPAM para sua rede ou site, por solicitação.
* **[!UICONTROL Mild Insult]**: Insultar conteúdo, conforme definido por uma lista de palavras-chave e padrões de frases.
* **[!UICONTROL Strong Insult]**: Insultar conteúdo, conforme definido por uma lista de palavras-chave e padrões de frases.
* **[!UICONTROL Hate Speech]**: Um insulto com base na ética ou na religião, especialmente quando a afiliação do grupo de metas está em uma minoria ou protegida.
* **[!UICONTROL ALL CAPS]**: Texto apresentado em todas as letras maiúsculas (lido como amarelo).
* **[!UICONTROL Mild Threat]**: Uma ameaça ou insulto que geralmente inclui algum tipo de profanidade mild direcionada a outra pessoa. Essa opção sinaliza possíveis ameaças com mais frequência, mas também tem uma taxa falsa mais alta do que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Uma ameaça ou insulto grave que menciona o dano bodily que menciona a uma ou mais pessoas, com maior profanidade. Essa opção sinaliza possíveis ameaças com menos frequência, mas também tem uma taxa de falsos positivos menor do que **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Uma imagem que pode ter nuances nela. Essa opção é sinalizada com menos frequência, mas também tem uma taxa de falsos positivos menor do que **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Uma imagem que pode ter nuances nela. Essa opção sinaliza a nuidade com mais frequência, mas também tem uma taxa falsa mais alta do que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informações de identificação pessoal): Informações que podem identificar o usuário. Isso pode incluir um endereço de email, endereço físico, número de seguro social (para clientes dos EUA), número do cartão de crédito, senha ou qualquer coisa que possa ser usada na fraude ou para conquistar a identidade de alguém.
* **[!UICONTROL Livefyre Recommends Trash]**. Defina a ação que o sistema executa quando a Recomendação de moderação automatizada identifica o conteúdo para rejeição. ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Para ativar o Recommendations Recommendations, entre em contato com a equipe de suporte do Adobe Livefyre.

## Manuseio de conteúdo não encontrado por SAFE {#section_pjy_5tx_vy}

Há vários meios disponíveis para lidar eficientemente com o conteúdo não encontrado por esse filtro. As opções abaixo são listadas na ordem recomendada do processo.

1. Como moderador, remova o conteúdo do stream.
1. Crie uma Regra de sinalização que informe se um conteúdo está marcado como Spam ou Ofensiva por cinco usuários, defina-o como Bozo.
1. Exclua o usuário que está postando conteúdo indesejado, para que todo o conteúdo vá diretamente para o estado do Bozo.
1. Adicione palavras específicas que devem sempre ser filtradas para a sua lista de perfis.

>[!NOTE]
>
>Se um moderador postar conteúdo que é capturado pelo Filtro de spam, ele ainda é sinalizado como Spam, mas é Aprovado automaticamente e não será definido como Bozo.

Se você notar tendências ou padrões de conteúdo não capturados por SAFE, envie o csms por email com as IDs de comentário e o texto.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Cartão de recursos](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Revisões](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Auxiliares](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

