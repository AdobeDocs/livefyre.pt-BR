---
description: O Livefyre Spam and Abuse Filtering Engine (SAFE) é um processo em segundo plano que analisa todo o conteúdo recebido e está habilitado para todos os clientes do Livefyre.
seo-description: O Livefyre Spam and Abuse Filtering Engine (SAFE) é um processo em segundo plano que analisa todo o conteúdo recebido e está habilitado para todos os clientes do Livefyre.
seo-title: Regras de segurança
title: Regras de segurança
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Regras de segurança{#safe-rules}

O Livefyre Spam and Abuse Filtering Engine (SAFE) é um processo em segundo plano que analisa todo o conteúdo recebido e está habilitado para todos os clientes do Livefyre.



O SAFE usa regras de padrões, bem como modelos estatísticos para detectar spam, abuso, profanidade e publicações em massa (repetitivas). Você verá isso referenciado de tempos em tempos em outros produtos do Livefyre, principalmente as ferramentas de moderação de conteúdo e o ModQ.

>[!NOTE]
>
>SAFE é somente em inglês, exceto para classificação de envio de mensagens em massa. Se precisar de suporte para outros idiomas, entre em contato com seu Gerente de conta estratégico.

## Componentes do Studio usando SAFE {#section_k34_4tx_vy}

Sinalizadores aplicados pelo SAFE podem ser usados com os seguintes componentes do Studio:

* Regras

   Você pode definir regras SAFE para sinalizar automaticamente o conteúdo e definir como o conteúdo sinalizado deve ser manipulado no **[!UICONTROL Network Settings]**.

   Por exemplo, um site pode definir uma tolerância muito baixa para Profanity e definir Regras SAFE que definem todo o conteúdo sinalizado como Profane como Bozo. Outros sites podem definir Regras que definem o conteúdo de Profane a ser pré-moderado antes de entrar no fluxo.

* ModQ

   É possível moderar o conteúdo sinalizado pelas regras SAFE e outras regras de pré-moderação (por exemplo, SPAM, profanidade etc.), no ModQ.

* Conteúdo do aplicativo na biblioteca

   O conteúdo sinalizado por SAFE está listado no Conteúdo do aplicativo na **[!UICONTROL Library]** guia. Você pode filtrar o conteúdo por sinalizadores para moderar o conteúdo.

## Opções de filtro SAFE {#section_pg5_ttx_vy}

O SAFE aplica os seguintes sinalizadores ao conteúdo filtrado e pode ser usado para criar regras e moderar conteúdo no Livefyre Studio.

* **[!UICONTROL Profanity List]**: Conteúdo profissional, conforme definido por uma lista de palavras-chave em inglês, com base em uso comum.

   O Filtro de Profanidade procura linguagem profana, com base em uma lista de palavras testadas. Se detectado, o conteúdo é sinalizado como Profane.

   >[!NOTE]
   >
   >O Livefyre também fornece um segundo filtro de Lista de Profanidade, que você pode personalizar nos níveis de Site e Rede. As regras criadas com a Lista de Profanidade terão prioridade sobre as regras automatizadas provenientes do filtro Profanidade SAFE. Para obter mais informações, consulte a seção Lista de perfis na documentação Configurações.

* **[!UICONTROL Mild Profanity]**: Palavras e frases geralmente não são aceitáveis em conversas educadas, mas geralmente são aceitáveis em conversas casuais. Geralmente, essas palavras e frases são permitidas na televisão de rede.
* **[!UICONTROL Strong Profanity]**: Um idioma muito forte, como exceções e frases não permitidas na televisão em rede e usadas com moderação em filmes com classificação R e programas maduros de TV a cabo. Geralmente, essas palavras não são usadas em conversas educadas ou casuais e são ditas em uma conversa mal educada com a intenção de prejudicar o ouvinte.
* **[!UICONTROL SPAM]**: Conteúdo não solicitado, geralmente comercial. Ele usa um modelo estatístico que depende de uma variedade de recursos (incluindo conteúdo de comentários e URLs) para sinalizar um conteúdo como SPAM. Você pode ajustar os limites de spam para personalizar as taxas de marcação SPAM para sua rede ou site, por solicitação.
* **[!UICONTROL Mild Insult]**: Conteúdo isolante, conforme definido por uma lista de palavras-chave e padrões de frases.
* **[!UICONTROL Strong Insult]**: Conteúdo isolante, conforme definido por uma lista de palavras-chave e padrões de frases.
* **[!UICONTROL Hate Speech]**: Um insulto com base na etnia ou religião, especialmente quando a filiação do grupo-alvo é minoritária ou protegida.
* **[!UICONTROL ALL CAPS]**: Texto apresentado em todas as letras maiúsculas (lido como gritando).
* **[!UICONTROL Mild Threat]**: Uma ameaça ou insulto que geralmente inclui algum tipo de profanação leve direcionada a outra pessoa. Essa opção sinaliza possíveis ameaças com mais frequência, mas também tem uma taxa de falsos positivos mais alta do que **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Uma ameaça ou insulto grave que mencione danos corporais acionáveis a uma ou mais pessoas, muitas vezes com forte profanação. Essa opção sinaliza possíveis ameaças com menos frequência, mas também tem uma taxa de falsos positivos mais baixa do que **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Uma imagem que pode ter nudez nela. Essa opção sinaliza a nudez com menos frequência, mas também tem uma taxa de falsos positivos mais baixa do que **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Uma imagem que pode ter nudez nela. Essa opção marca a nudez com mais frequência, mas também tem uma taxa de falsos positivos mais alta do que **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Informações pessoais identificáveis): Informações que podem identificar o usuário. Isso pode incluir um endereço de email, endereço físico, número de segurança social (para clientes dos EUA), número de cartão de crédito, uma senha ou qualquer coisa que possa ser usada em fraudes ou para obter a identidade de alguém.
* **[!UICONTROL Livefyre Recommends Trash]**. Defina a ação que o sistema executa quando a Recomendação de moderação automática identifica o conteúdo para rejeição.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Para ativar as Recomendações de moderação, entre em contato com seu profissional de suporte do Adobe Livefyre.

## Manuseio de conteúdo não capturado pelo SAFE {#section_pjy_5tx_vy}

Há vários meios disponíveis para lidar eficazmente com o conteúdo não capturado por esse filtro. As opções abaixo são listadas na ordem de processo recomendada.

1. Como moderador, remova o conteúdo do fluxo.
1. Crie uma regra de sinalizador que indique se um conteúdo for sinalizado como Spam ou Ofensivo por cinco usuários, defina-o como Bozo.
1. Proibir o usuário que está postando conteúdo indesejado, de modo que todo o conteúdo seja direcionado diretamente para o estado Bozo.
1. Adicione palavras específicas que devem ser sempre filtradas na sua lista de profanidade.

>[!NOTE]
>
>Se um moderador postar o conteúdo capturado pelo nosso Filtro de spam, ele ainda será sinalizado como Spam, mas será automaticamente Aprovado e não será definido como Bozo.

Se você notar tendências ou padrões de conteúdo não capturados pelo SAFE, envie um email para seus CSM com as IDs de comentários e o texto.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

