---
description: Permite que os usuários selecionem a frequência e o conteúdo de notificações.
seo-description: Permite que os usuários selecionem a frequência e o conteúdo de notificações.
seo-title: Notificações por email
solution: Experience Manager
title: Notificações por email
uuid: 27 head133-bd 8 d -4949-8146-1254 c 160 d 3 af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Notificações por email{#email-notifications}

Permite que os usuários selecionem a frequência e o conteúdo de notificações.

**Habilite notificações por email para usuários e moderadores.**

Os aplicativos do Livefyre permitem ativar notificações por email para usuários e moderadores, com base em ações específicas. As notificações são baseadas no momento em que o conteúdo é postado no stream, permitindo que os usuários permaneçam envolvidos em conversas que estão relacionadas e sejam notificadas quando alguém curtir ou responde a um de seus comentários.

Os usuários e os moderadores podem participar de uma notificação por e-mail e podem definir a frequência com a qual e-mails são recebidos. Esta seção descreve como configurar e personalizar essas notificações por email.

* Opções de e-mail do usuário: opções de notificação de usuário disponíveis.
* Opções de e-mail do moderador: opções de notificação de moderador disponíveis.
* Opções de emails de identidade do Livefyre: e-mails enviados como parte da identidade do Livefyre. Esses emails são relevantes somente para os Clientes de identidade do Livefyre.
* Sincronização de dados com o Livefyre: manter preferências de sincronização com o Livefyre.
* Personalização de emails: personalizações de e-mail disponíveis.

Use as **opções Configurações &gt; Configurações de integração &gt; Enviar** notificações por email para personalizar notificações por e-mail para sua rede.

>[!NOTE]
>
>Para garantir que seus usuários finais não recebam email não intencional, nenhuma notificação por email será enviada do ambiente UAT do Livefyre.

**Opções de e-mail do usuário**

O Livefyre permite permitir que os usuários recebam notificações por email da atividade do site. Use as configurações de integração fornecidas pelo Livefyre com o Livefyre para permitir que os usuários selecionem suas preferências para programação de notificações.

>[!NOTE]
>
>Os emails são enviados apenas para o conteúdo publicado manualmente no stream, e não para o conteúdo obtido de socialsync.

Para permitir que os usuários definam suas preferências de notificação, inclua uma seção Notificação por email nas Configurações do usuário para o sistema de perfil do usuário. Adicione os campos correspondentes ao esquema do banco de dados do perfil do usuário, em seguida, gerencie as configurações do usuário usando o Ping para Extrair. (Trabalhe com seu Gerente de integração técnica para definir frequências padrão para sua rede. Se você for um cliente de Perfis empresariais, passe os padrões selecionados para a equipe de entrega do Livefyre para configuração no banco de dados do Livefyre.)

Os usuários em seu site podem seguir uma conversa e começar a receber notificações por e-mail clicando no **[!UICONTROL +Follow]** botão no editor de comentário. As preferências de notificação são definidas no nível da rede do Livefyre. Todas as configurações do usuário serão aplicadas a todos os sites e conversas na rede.

**Padrões recomendados**

* Alguém comentando em uma conversa que estou seguindo: ** resumo por hora**
* Alguém gosta de um dos meus comentários: ** resumo por hora**
* Alguém responde a um dos meus comentários: ** imediatamente**
* Siga as conversas automaticamente quando deixar um comentário: ** desativado** (desmarcado)

**Observação**: As notificações por email se baseiam no momento em que o conteúdo é aprovado para inclusão no stream.

O Livefyre oferece duas opções de frequência de email:

* Imediatamente
* Resumo por hora

**Imediatamente**

Emails enviados imediatamente exibem o texto da publicação, o título do artigo, o nome de usuário do autor e um **link de Resposta** que leva o usuário para o conteúdo na página. Esses emails também incluem um link **para cancelar a inscrição** no rodapé, permitindo que os usuários cancelem a inscrição nas notificações por e-mail para essa coleção. Clicar em** cancelar inscrição** levará-os para uma página de confirmação informando que eles não assinaram a coleção.

**Resumo por hora**

Os emails enviados em um resumo por hora exibem todo o conteúdo, respostas ao conteúdo e curtidas no conteúdo na última hora (ou assim,) por aplicativo que o usuário está seguindo. Se o usuário estiver seguindo vários aplicativos na rede, eles receberão um email compilado para cada aplicativo.

>[!NOTE]
>
>Em conversas sem novo conteúdo por mais de várias horas, os usuários com resumo por hora ativados receberão aviso imediatamente após uma nova postagem de conteúdo.

**Opções de e-mail do moderador**

Os moderadores podem aceitar receber emails para conteúdo publicado em um aplicativo que estão seguindo e para comentários sinalizados ou ofensivos em um aplicativo que estão moderando. **Observação:** Nenhum email será enviado quando os usuários sinalizarem um comentário com Discordar ou Desligado, já que essas categorias não são consideradas importantes para a notificação do moderador.

Os campos moderador_ comentários e moderadores_ flag também devem ser adicionados ao esquema de banco de dados da página de usuário do moderador de moderador para permitir que os moderadores atualizem a frequência de suas notificações por e-mail e recusem se desejarem. O Livefyre recomenda que você defina esses dois campos de notificação por email para **nunca**. As opções incluem **nunca** (padrão), **imediatamente** e **frequentemente**.

**Email do moderador (conteúdo sinalizado):**

Quando o conteúdo é sinalizado em um aplicativo moderado, o e-mail enviado para o moderador exibe o conteúdo sinalizado, o nome do usuário que sinalizou o conteúdo e um link de volta para a página de conteúdo.

Quando um usuário alterar suas preferências de notificação por email no seu site, sincronize a atualização com o sistema de perfil remoto do Livefyre usando o Livefyre&#39;s Ping for Pull.

**Sincronização de dados com o Livefyre**

## Personalização de emails {#section_jxb_c5k_yy}

Vários campos nos modelos de notificação por email podem ser alterados para ajustar seu estilo e sua marca.

* **[!UICONTROL From Email Address]**

   O «endereço de email» para todas as notificações por email pode ser personalizado para ser consistente com sua marca. O Livefyre recomenda **noreply@customerdomain.com**, substituindo **customerdomainwith** seu nome de domínio. O padrão é **noreply@livefyre.com**. Passe seu «endereço de email» para o seu Gerente de integração técnico para obter a configuração no banco de dados do Livefyre para sua rede.

   >[!NOTE]
   >
   >Deixe este campo em branco para desativar notificações por e-mail para sua rede

* **[!UICONTROL Email Logo]**

   O logotipo exibido em notificações por email pode ser personalizado para exibir o logotipo da sua empresa, em vez do logotipo padrão do Livefyre, usando a guia Marca da página **Configurações** de rede do Studio. Essa personalização está disponível somente no nível da rede, não no nível do site e está disponível apenas para clientes pagos do Livefyre.

* **[!UICONTROL Custom Templates]**

   Se desejar, é possível implementar um modelo de email totalmente personalizado. No entanto, isso exigirá um esforço de desenvolvimento e pode gerar custos de serviços profissionais. Entre em contato com seu Gerente de contas para obter mais detalhes.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Cartão de recursos](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Revisões](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

