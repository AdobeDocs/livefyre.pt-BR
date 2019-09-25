---
description: Permite que os usuários selecionem sua frequência de notificação e conteúdo.
seo-description: Permite que os usuários selecionem sua frequência de notificação e conteúdo.
seo-title: Notificações por e-mail
solution: Experience Manager
title: Notificações por e-mail
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Notificações por e-mail{#email-notifications}

Permite que os usuários selecionem sua frequência de notificação e conteúdo.

**Ative notificações por email para seus usuários e moderadores.**

Os aplicativos Livefyre permitem ativar notificações por email para seus usuários e moderadores, com base em ações específicas. As notificações são baseadas no momento em que o conteúdo é postado no stream, permitindo que os usuários permaneçam envolvidos em conversas que lhes interessam e sejam notificados quando alguém curtir ou responder a um de seus comentários.

Os usuários e moderadores podem aceitar ou recusar a notificação por email e podem definir a frequência com que os emails são recebidos. Esta seção descreve como configurar e personalizar essas notificações por email.

* Opções de email do usuário: opções de notificação de usuário disponíveis.
* Opções de email do moderador: opções de notificação do moderador disponíveis.
* Opções de e-mails de identidade do Livefyre: e-mails enviados como parte da Livefyre Identity. Esses e-mails são relevantes apenas para os clientes de identidade do Livefyre.
* Sincronização de dados com o Livefyre: manter as preferências sincronizadas com o Livefyre.
* Personalizando e-mails: personalizações de email disponíveis.

Use as opções **Configurações &gt; Configurações de integração &gt; Configuração** de notificação por email para personalizar notificações por email para sua rede.

>[!NOTE]
>
>Para garantir que os usuários finais não recebam emails indesejados, nenhuma notificação por email é enviada do ambiente UAT do Livefyre.

**Opções de email do usuário**

O Livefyre permite que você permita que os usuários recebam notificações por email sobre a atividade do site. Use as configurações de integração do Perfil de usuário fornecidas pelo Livefyre para permitir que os usuários selecionem suas preferências para agendamentos de notificação.

>[!NOTE]
>
>Os emails são enviados somente para conteúdo publicado manualmente no stream, e não para conteúdo extraído do SocialSync.

Para permitir que os usuários definam suas preferências de notificação, inclua uma seção Notificação por email nas Configurações do usuário para seu sistema de perfil de usuário. Adicione os campos correspondentes ao esquema do banco de dados do perfil do usuário e gerencie as configurações do usuário usando o Ping for Pull. (Entre em contato com seu Gerenciador de integração técnica para definir as frequências padrão para sua rede. Se você for um cliente de Perfis Corporativos, passe os padrões selecionados para a equipe de entrega do Livefyre para configuração no banco de dados do Livefyre.)

Os usuários do seu site podem seguir uma conversa e começar a receber notificações por email clicando no **[!UICONTROL +Follow]** botão no editor de comentários. As preferências de notificação são definidas no nível de rede do Livefyre. Todas as configurações do usuário serão aplicadas a todos os sites e conversas na rede.

**Padrões recomendados**

* Alguém comenta em uma conversa que eu estou seguindo:*** por hora, resumo**
* Alguém gosta de um dos meus comentários:*** por hora, resumo**
* Alguém responde a um dos meus comentários:** imediatamente**
* Conversações de acompanhamento automático quando deixo um comentário:** desligado** (desmarcado)

**Observação**: As notificações por email são baseadas no momento em que o conteúdo é aprovado para inclusão no fluxo.

O Livefyre oferece duas opções de frequência de email:

* Imediatamente
* Resumo por hora

**Imediatamente**

Os emails enviados imediatamente exibem o texto da postagem, o título do artigo, o nome de usuário do autor e um link **Responder** que leva o usuário ao conteúdo da página. Esses e-mails também incluem um link para **cancelar a assinatura** no rodapé, permitindo que os usuários cancelem a assinatura das notificações por e-mail para essa coleção. Clicar em **unsubscribe **irá levá-los para uma página de confirmação informando-os que foram cancelados da Coleção.

**Resumo por hora**

Os emails enviados em um resumo por hora exibem todo o conteúdo, respondem ao conteúdo e curtidas no conteúdo na última hora (ou assim) por aplicativo que o usuário está seguindo. Se o usuário estiver seguindo vários aplicativos na rede, ele receberá um email de compilação para cada aplicativo.

>[!NOTE]
>
>Em conversas sem novo conteúdo por mais de várias horas, os usuários com a compilação por hora ativada receberão aviso imediatamente após uma nova publicação de conteúdo.

**Opções de email do moderador**

Os moderadores podem aceitar receber emails por conteúdo publicado em um aplicativo que estão acompanhando, e por comentários marcados como Spam ou Offensive em um aplicativo que estão moderando. **** Observação: Nenhum email será enviado quando os usuários sinalizarem um comentário com Discordar ou Sem Tópico, pois essas categorias não são consideradas importantes para a notificação do moderador.

Os campos moderator_comments e moderator_flags também devem ser adicionados ao esquema da página de configurações do perfil do usuário moderador para permitir que os moderadores atualizem a frequência de suas notificações por email e recusem se desejarem. Livefyre recomenda que você defina esses dois campos de notificação por email do moderador para **nunca**. As opções incluem **nunca** (padrão), **imediatamente** e **com frequência**.

**Email do moderador (conteúdo sinalizado):**

Quando o conteúdo é sinalizado em um aplicativo moderado, o email enviado ao moderador exibirá o conteúdo que foi sinalizado, o nome de usuário que sinalizou o conteúdo e um link de volta para a página de conteúdo.

Quando um usuário alterar suas preferências de notificação por email em seu site no sistema de perfil, sincronize a atualização com o sistema de perfil remoto Livefyre usando o Ping for Pull do Livefyre.

**Sincronização de dados com o Livefyre**

## Personalização de emails {#section_jxb_c5k_yy}

Vários campos nos modelos de notificação por email podem ser alterados para se ajustarem ao seu estilo e marca.

* **[!UICONTROL From Email Address]**

   O "endereço de email de origem" para todas as notificações por email pode ser personalizado para ser consistente com sua marca. Livefyre recomenda **noreply@customerdomain.com**, substituindo o domínio **** do cliente pelo nome do domínio. (O padrão é **noreply@livefyre.com**.) Transmita seu "endereço de email" preferencial para o Gerenciador de integração técnica para configuração no banco de dados Livefyre da sua rede.

   >[!NOTE]
   >
   >Deixe este campo em branco para desativar notificações por email para sua rede

* **[!UICONTROL Email Logo]**

   O logotipo exibido nas notificações por email pode ser personalizado para exibir o logotipo da sua empresa, em vez do logotipo padrão do Livefyre, usando a guia Marca da página Configurações **de** rede do Studio. Essa personalização está disponível somente no nível da rede, não no nível do site, e está disponível somente para clientes pagos da Livefyre.

* **[!UICONTROL Custom Templates]**

   Se desejar, é possível implementar um modelo de email totalmente personalizado. No entanto, isso exigirá algum esforço de desenvolvimento e poderá acarretar custos de serviços profissionais. Entre em contato com seu Gerente de conta para obter detalhes.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

