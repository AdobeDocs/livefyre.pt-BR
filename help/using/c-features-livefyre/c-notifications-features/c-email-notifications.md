---
description: Permita que os usuários selecionem a frequência e o conteúdo da notificação.
title: Notificações por e-mail
exl-id: 46821382-ac93-4523-a0ac-84535e76d367
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Notificações por e-mail{#email-notifications}

Permita que os usuários selecionem a frequência e o conteúdo da notificação.

**Ativar notificações por email para usuários e moderadores.**

Os Aplicativos Livefyre permitem habilitar as notificações por email para seus usuários e moderadores, com base em ações específicas. As notificações são baseadas no momento em que o conteúdo é postado no stream, permitindo que os usuários permaneçam envolvidos em conversas que lhes interessam e sejam notificados quando alguém curtir ou responder a um de seus comentários.

Usuários e moderadores podem aceitar ou rejeitar a notificação por email e podem definir a frequência com que os emails são recebidos. Esta seção descreve como configurar e personalizar essas notificações de email.

* Opções de email do usuário: opções de notificação de usuário disponíveis.
* Opções de email do moderador: opções disponíveis de notificação do moderador.
* Opções de emails de identidade do Livefyre: emails enviados como parte do Livefyre Identity. Esses emails são relevantes apenas para clientes de identidade do Livefyre.
* Sincronização de dados com o Livefyre: a manutenção das preferências é sincronizada com o Livefyre.
* Personalizando emails: personalizações de email disponíveis.

Use as opções **Settings > Integration Settings > Email Notification Setup** para personalizar as notificações por email de sua rede.

>[!NOTE]
>
>Para garantir que os usuários finais não recebam emails não intencionais, nenhuma notificação por email é enviada do ambiente UAT do Livefyre.

**Opções de email do usuário**

O Livefyre permite que os usuários recebam notificações por email das atividades do site. Use as configurações de integração do Perfil de usuário fornecidas pela Livefyre para permitir que os usuários selecionem suas preferências para agendamentos de notificação.

>[!NOTE]
>
>Os emails são enviados somente para conteúdo publicado manualmente no stream, e não para conteúdo extraído do SocialSync.

Para permitir que os usuários definam suas preferências de notificação, inclua uma seção Notificação por email nas Configurações do usuário para seu sistema de perfil de usuário. Adicione os campos correspondentes ao esquema do banco de dados do perfil do usuário e gerencie as configurações do usuário usando Ping for Pull. (Entre em contato com seu Gerenciador de integração técnica para definir frequências padrão para a sua rede. Se você for um cliente de Perfis empresariais, passe os padrões selecionados para a equipe de delivery do Livefyre para configuração no banco de dados do Livefyre.)

Os usuários do site podem seguir uma conversa e começar a receber notificações por email clicando no botão **[!UICONTROL +Follow]** no editor de comentários. As preferências de notificação são definidas no nível de rede do Livefyre. Todas as configurações do usuário serão aplicadas a todos os sites e conversas em sua rede.

**Padrões recomendados**

* Alguém comenta em uma conversa e eu estou seguindo:** resumo por hora**
* Alguém gosta de um dos meus comentários:** resumo por hora**
* Alguém responde a um dos meus comentários:** imediatamente**
* Conversações de acompanhamento automático quando deixo um comentário:** off** (desmarcado)

**Observação**: As notificações por email são baseadas no momento em que o conteúdo é aprovado para inclusão no fluxo.

Livefyre oferece duas opções de frequência de email:

* Imediatamente
* Resumo por hora

**Imediatamente**

Os emails enviados exibem imediatamente o texto da publicação, o título do artigo, o nome de usuário do autor e um link **Responder** que leva o usuário para o conteúdo na página. Esses emails também incluem um link **unsubscribe** no rodapé, permitindo que os usuários cancelem a assinatura das notificações por email dessa coleção. Clicar em **cancelar inscrição **os levará a uma página de confirmação informando que a subscrição da coleção foi cancelada.

**Resumo por hora**

Os emails enviados em um resumo por hora exibem todo o conteúdo, respondem ao conteúdo e curtidas no conteúdo na última hora (aproximadamente) por aplicativo que o usuário está seguindo. Se o usuário estiver seguindo vários aplicativos em sua rede, ele receberá um email de resumo para cada aplicativo.

>[!NOTE]
>
>Em conversas sem novo conteúdo por mais de várias horas, os usuários com a compilação por hora ativada receberão aviso imediatamente após uma nova publicação de conteúdo.

**Opções de email do moderador**

Os moderadores podem aceitar receber emails para conteúdo publicado em um aplicativo que estejam seguindo, e para comentários sinalizados como spam ou ofensivo em um aplicativo, eles estão moderando. **Observação:** nenhum email será enviado quando os usuários sinalizarem um comentário com Discordo ou Tópico, pois essas categorias não são consideradas importantes para a notificação do moderador.

Os campos moderator_comments e moderator_flags também devem ser adicionados ao esquema da página de configurações do perfil do usuário do moderador para permitir que os moderadores atualizem a frequência de suas notificações de email e excluam se desejarem. Livefyre recomenda definir esses dois campos de notificação de email do moderador para **never**. As opções incluem **never** (padrão), **imediatamente** e **frequentemente**.

**Email do moderador (conteúdo sinalizado):**

Quando o conteúdo é sinalizado em um aplicativo moderado, o email enviado ao moderador exibirá o conteúdo que foi sinalizado, o nome de usuário que sinalizou o conteúdo e um link de volta à página de conteúdo.

Quando um usuário alterar suas preferências de notificação por email no seu site no sistema de perfis, sincronize a atualização para o sistema de perfis remotos do Livefyre usando o Ping for Pull do Livefyre.

**Sincronização de dados com o Livefyre**

## Personalizar emails {#section_jxb_c5k_yy}

Vários campos nos modelos de notificação por email podem ser alterados para se ajustarem ao seu estilo e marca.

* **[!UICONTROL From Email Address]**

   O &quot;do endereço de email&quot; de todas as notificações por email pode ser personalizado para ser consistente com sua marca. Livefyre recomenda **noreply@customerdomain.com**, substituindo **customerdomain** pelo seu nome de domínio. (O padrão é **noreply@livefyre.com**.) Passe seu &quot;endereço de email&quot; preferencial para o Gerenciador de integração técnica para configuração no banco de dados do Livefyre para sua rede.

   >[!NOTE]
   >
   >Deixe este campo em branco para desabilitar notificações por email para sua rede

* **[!UICONTROL Email Logo]**

   O logotipo exibido nas notificações por email pode ser personalizado para exibir o logotipo de sua empresa, em vez do logotipo padrão do Livefyre, usando a guia Marca da página **Configurações de rede** do Studio. Essa personalização está disponível somente no nível da rede, não no nível do site, e está disponível somente para clientes pagos do Livefyre.

* **[!UICONTROL Custom Templates]**

   É possível implementar um modelo de email totalmente personalizado, se desejar. No entanto, isso exigirá algum esforço de desenvolvimento e poderá implicar custos com serviços profissionais. Entre em contato com seu Gerente de conta para obter detalhes.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mural de mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
