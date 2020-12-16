---
description: Permite que os usuários selecionem sua frequência de notificação e conteúdo.
seo-description: Permite que os usuários selecionem sua frequência de notificação e conteúdo.
seo-title: Notificações por e-mail
solution: Experience Manager
title: Notificações por e-mail
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 1%

---


# Notificações por e-mail{#email-notifications}

Permite que os usuários selecionem sua frequência de notificação e conteúdo.

**Habilite notificações por email para seus usuários e moderadores.**

Os aplicativos Livefyre permitem ativar notificações por email para seus usuários e moderadores, com base em ações específicas. As notificações são baseadas no momento em que o conteúdo é postado no stream, permitindo que os usuários permaneçam envolvidos em conversas que lhes interessam e sejam notificados quando alguém curtir ou responder a um de seus comentários.

Usuários e Moderadores podem opt in ou não receber notificações por email e podem definir a frequência com que os emails são recebidos. Esta seção descreve como configurar e personalizar essas notificações por email.

* Opções de email do usuário: opções de notificação de usuário disponíveis.
* Opções de email do moderador: opções de notificação do moderador disponíveis.
* Opções de e-mails de identidade do Livefyre: e-mails enviados como parte da Livefyre Identity. Esses e-mails são relevantes apenas para os clientes de identidade do Livefyre.
* Sincronização de dados com o Livefyre: manter as preferências sincronizadas com o Livefyre.
* Personalizando e-mails: personalizações de email disponíveis.

Use as opções **Configurações > Configurações de integração > Configuração de notificação por email** para personalizar notificações por email para sua rede.

>[!NOTE]
>
>Para garantir que os usuários finais não recebam emails indesejados, nenhuma notificação por email é enviada do ambiente Livefyre UAT.

**Opções de email do usuário**

O Livefyre permite que os usuários recebam notificações por email da atividade do site. Use as configurações de integração de Perfil do usuário fornecidas pelo Livefyre para permitir que os usuários selecionem suas preferências para agendamentos de notificação.

>[!NOTE]
>
>Os emails são enviados somente para conteúdo publicado manualmente no stream, e não para conteúdo extraído do SocialSync.

Para permitir que os usuários definam suas preferências de notificação, inclua uma seção Notificação por email nas Configurações do usuário para seu sistema de perfil do usuário. Adicione os campos correspondentes ao schema do banco de dados do perfil do usuário e gerencie as configurações do usuário usando o Ping for Pull. (Entre em contato com seu Gerenciador de integração técnica para definir as frequências padrão para sua rede. Se você for um cliente do Enterprise Perfis, passe os padrões selecionados para a equipe do Livefyre delivery para configuração no banco de dados do Livefyre.)

Os usuários do site podem seguir uma conversa e começar a receber notificações por email clicando no botão **[!UICONTROL +Follow]** no editor de comentários. As preferências de notificação são definidas no nível de rede do Livefyre. Todas as configurações do usuário serão aplicadas a todos os sites e conversas na rede.

**Padrões recomendados**

* Alguém comenta em uma conversa que eu estou seguindo:*** por hora, resumo**
* Alguém gosta de um dos meus comentários:*** por hora, resumo**
* Alguém responde a um dos meus comentários:** imediatamente**
* Conversações de acompanhamento automático quando deixo um comentário:** desligado** (desmarcado)

**Observação**: As notificações por email são baseadas no momento em que o conteúdo é aprovado para inclusão no fluxo.

O Livefyre oferta duas opções de frequência de e-mail:

* Imediatamente
* Resumo por hora

**Imediatamente**

Os emails enviados imediatamente exibem o texto da postagem, o título do artigo, o nome de usuário do autor e um link **Responder** que leva o usuário ao conteúdo da página. Esses e-mails também incluem um link **unsubscribe** no rodapé, permitindo que os usuários cancelem a assinatura das notificações por e-mail para essa coleção. Clicar em **unsubscribe **irá levá-los para uma página de confirmação informando-os que foram cancelados da Coleção.

**Resumo por hora**

Os emails enviados em um resumo por hora exibem todo o conteúdo, respondem ao conteúdo e curtidas no conteúdo na última hora (ou assim) por aplicativo que o usuário está seguindo. Se o usuário estiver seguindo vários aplicativos na rede, ele receberá um email de compilação para cada aplicativo.

>[!NOTE]
>
>Em conversas sem novo conteúdo por mais de várias horas, os usuários com a compilação por hora ativada receberão aviso imediatamente após uma nova publicação de conteúdo.

**Opções de email do moderador**

Os moderadores podem opt in por receber e-mails para conteúdo publicado em um aplicativo que estão acompanhando e para comentários marcados como Spam ou Offensive em um aplicativo que estão moderando. **Observação:** nenhum email será enviado quando os usuários sinalizarem um comentário com Discordar ou Sem Tópico, pois essas categorias não são consideradas importantes para a notificação do moderador.

Os campos moderator_comments e moderator_flags também devem ser adicionados ao schema da página de configurações de perfil do usuário moderador para permitir que os moderadores atualizem a frequência das notificações por email e opt out se desejarem. Livefyre recomenda que você defina esses dois campos de notificação por email do moderador para **never**. As opções incluem **never** (padrão), **imediatamente** e **frequentemente**.

**Email do moderador (conteúdo sinalizado):**

Quando o conteúdo é sinalizado em um aplicativo moderado, o email enviado ao moderador exibirá o conteúdo que foi sinalizado, o nome de usuário que sinalizou o conteúdo e um link de volta para a página de conteúdo.

Quando um usuário alterar suas preferências de notificação por email em seu site no sistema do perfil, sincronize a atualização com o sistema do perfil remoto Livefyre usando o Ping for Pull do Livefyre.

**Sincronização de dados com o Livefyre**

## Personalizando e-mails {#section_jxb_c5k_yy}

Vários campos nos modelos de notificação por email podem ser alterados para se ajustarem ao seu estilo e marca.

* **[!UICONTROL From Email Address]**

   O &quot;endereço de e-mail de origem&quot; para todas as notificações por e-mail pode ser personalizado para ser consistente com sua marca. Livefyre recomenda **noreply@customerdomain.com**, substituindo **customerdomain** pelo seu nome de domínio. (O padrão é **noreply@livefyre.com**.) Transmita seu &quot;endereço de email&quot; preferencial para o Gerenciador de integração técnica para configuração no banco de dados Livefyre da sua rede.

   >[!NOTE]
   >
   >Deixe este campo em branco para desativar notificações por email para sua rede

* **[!UICONTROL Email Logo]**

   O logotipo exibido nas notificações por e-mail pode ser personalizado para exibir o logotipo da sua empresa, em vez do logotipo padrão do Livefyre, usando a guia Marca da página **Configurações de rede** do Studio. Essa personalização está disponível somente no nível da rede, não no nível do site, e está disponível somente para clientes pagos da Livefyre.

* **[!UICONTROL Custom Templates]**

   Se desejar, é possível implementar um modelo de email totalmente personalizado. No entanto, isso exigirá algum esforço de desenvolvimento e poderá acarretar custos de serviços profissionais. Entre em contato com seu Gerente de conta para obter detalhes.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

