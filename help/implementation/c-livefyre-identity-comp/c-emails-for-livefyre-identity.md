---
description: null
seo-description: null
seo-title: E-mails para identidade do Livefyre
solution: Experience Manager
title: E-mails para identidade do Livefyre
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# E-mails para identidade do Livefyre{#emails-for-livefyre-identity}

A identidade do Livefyre envia os seguintes e-mails:

* [Email de redefinição de senha](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Email de verificação](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Enviar verificação por e-mail para usuários](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Email de boas-vindas](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Enviar e-mail de boas-vindas para usuários](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Você pode personalizar a aparência de todos os emails de identidade do Livefyre em **[!UICONTROL Integration Settings > Email Notifications.]**

## Email de redefinição de senha {#section_nd1_whs_p1b}

O Livefyre envia automaticamente um email de redefinição de senha quando um usuário tenta redefinir sua senha.

O e-mail de redefinição de senha tem a seguinte aparência:

**Assunto:** Redefinir senha

**Corpo:**

Ei lá *< username >*,

Houve uma solicitação para alterar a senha do seu perfil em *< nome da rede >*.

Se solicitado, clique no link a seguir para escolher uma nova senha: *< URL de redefinição de senha >*.

*< Nome_ usuário >*, *< nome da rede >*e *< URL de redefinição de senha >* são gerados dinamicamente com base no visitante do site e na rede.

## Email de verificação {#section_ak5_xhs_p1b}

Você pode enviar um e-mail verificação do endereço de e-mail de um usuário. Para enviar emails de verificação, ative a opção Configurações **de integração > Identidade do Livefyre**.

O e-mail de verificação tem a seguinte aparência:

**Assunto:** Verificação de email

**Corpo:**

Hello *< username >*,

Clique no link a seguir (ou cole no navegador) para verificar sua conta: *< URL de verificação >*.

Esse link expirará em 24 horas.

Obrigado,

A equipe *< nome do cliente >* equipe

*< Nome de usuário >*, *< nome da rede >*e *< URL de verificação >* são gerados dinamicamente com base no visitante do site e na rede.

## Enviar uma verificação por email para usuários {#section_vyv_yhs_p1b}

Você pode enviar um email para um usuário para verificar o endereço de email utilizado para cadastrar-se em uma conta. Para enviar um e-mail de verificação:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique **em Configurações de integração > Identidade do Livefyre.**

1. Navegue até **Tipos de logon**.
1. Clique **em Exigir verificação por e-mail** para enviar um e-mail aos usuários que verifica o endereço de e-mail usado para cadastrar-se para uma conta.
1. Navegue até **Email de rede** para configurar **o logotipo para e-mail**, o endereço de email para usar como o endereço do endereço (**Email de**) e o nome de exibição para usar no endereço de email (**Nome de exibição por email**).

## Email de boas-vindas {#section_z2v_zhs_p1b}

Você pode enviar um email de boas-vindas para os usuários. Para enviar emails de boas-vindas, ative a opção Configurações **de integração** > **Identidade do Livefyre**.

O email de boas-vindas é desta forma:

**Assunto:** Bem-vindo ao *< nome do cliente >*

**Corpo:**

Hello *< username >*,

Uma conta foi criada para você em *< nome do cliente >*.

Esta conta foi criada em *< URL de referência >* de endereço IP *< Endereço IP >*.

Caso isso tenha acontecido, você pode ignorar com segurança esse email.

Caso não tenha feito isso, entre em contato com o `support@livefyre.com`

Agradecimentos

The *"customer name"* Team

*" Nome de usuário "," nome do cliente "," URL de referência "e* " Endereço IP "são gerados dinamicamente com base no visitante do site e na rede.

## Enviar um email de boas-vindas para um usuário {#section_kjp_c3s_p1b}

Você pode enviar um email de boas-vindas para um usuário depois de cadastrar-se em uma conta. O Studio envia esse email depois de enviar um e-mail de verificação, se você configurar um e-mail de verificação. Para enviar um email de boas-vindas:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique em **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navegue **[!UICONTROL Email Settings]**até.

1. Clique **[!UICONTROL Send Welcome Emails To New Users]** em para ativar o envio e-mails.
1. Navegue até **[!UICONTROL Network Email]** Configurar *o logotipo para e-mail*, o endereço de e-mail para usar como o endereço do endereço (**Email de**) e o nome de exibição para usar no endereço de email (**Nome de exibição por email**).