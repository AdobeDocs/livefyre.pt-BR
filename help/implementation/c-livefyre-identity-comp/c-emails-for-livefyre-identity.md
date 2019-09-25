---
description: 'null'
seo-description: 'null'
seo-title: Emails para a identidade do Livefyre
solution: Experience Manager
title: Emails para a identidade do Livefyre
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Emails para a identidade do Livefyre{#emails-for-livefyre-identity}

A Livefyre Identity envia os seguintes emails:

* [Email de redefinição de senha](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Email de verificação](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Enviar verificação por email para usuários](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Email de Boas-vindas](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Enviar email de boas-vindas aos usuários](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Você pode personalizar a aparência de todos os e-mails de identificação do Livefyre em **[!UICONTROL Integration Settings > Email Notifications.]**

## Email de redefinição de senha {#section_nd1_whs_p1b}

O Livefyre envia automaticamente um email de redefinição de senha quando um usuário tenta redefinir sua senha.

O e-mail de redefinição de senha tem a seguinte aparência:

**** Assunto: Redefinir senha

**Corpo:**

Ei, aqui *&lt;nome de usuário&gt;*,

Houve uma solicitação para alterar a senha do seu perfil em *&lt;nome da rede&gt;*.

Se você solicitou isso, clique no link a seguir para escolher uma nova senha: *&lt;URL de redefinição de senha&gt;*.

*&lt;Nome do usuário&gt;*, *&lt;nome da rede&gt;* e *&lt;URL de redefinição de senha&gt;* são gerados dinamicamente com base no visitante do site e na sua rede.

## Email de verificação {#section_ak5_xhs_p1b}

Você pode enviar um email verificando o endereço de email de um usuário. Para enviar emails de verificação, ative a opção em Configurações de **integração &gt; Identidade** do Livefyre.

O e-mail de verificação tem a seguinte aparência:

**** Assunto: Verificação de email

**Corpo:**

Olá *&lt;nome do usuário&gt;*,

Clique no link a seguir (ou cole em seu navegador) para verificar sua conta: *&lt;URL de verificação&gt;*.

Este link expirará em 24 horas.

Obrigado,

A equipe *&lt;nome do cliente&gt;*

*&lt;Nome do usuário&gt;*, *&lt;nome da rede&gt;* e *&lt;URL de verificação&gt;* são gerados dinamicamente com base no visitante do site e na sua rede.

## Enviar uma verificação por email aos usuários {#section_vyv_yhs_p1b}

Você pode enviar um email para um usuário para verificar o endereço de email que ele usa para se inscrever em uma conta. Para enviar um email de verificação:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique em Configurações **de integração &gt; Identidade do Livefyre.**

1. Navegue até Tipos **de** logon.
1. Clique em **Exigir verificação** de e-mail para enviar um e-mail aos usuários que verifique o endereço de e-mail que eles usam para se inscrever em uma conta.
1. Navegue até Email **** de rede para configurar o **Logotipo para Email**, o endereço de email a ser usado como o endereço de formulário (**Email de**) e o nome de exibição a ser usado para o endereço de email de formulário (Nome **de exibição de** email).

## Email de Boas-vindas {#section_z2v_zhs_p1b}

Você pode enviar um email de boas-vindas aos usuários. Para enviar emails de boas-vindas, você deve ativar a opção em Configurações **de** integração &gt; **Livefyre Identity**.

O email de boas-vindas é assim:

**** Assunto: Bem-vindo ao *&lt;nome do cliente&gt;*

**Corpo:**

Olá *&lt;nome do usuário&gt;*,

Uma conta foi criada para você em *&lt;nome do cliente&gt;*.

Esta conta foi criada em *&lt;URL de referência&gt;* a partir do endereço IP *&lt;Endereço IP&gt;*.

Se você fez isso, pode ignorar esse email com segurança.

Se você não fez isso, entre em contato com `support@livefyre.com`

Obrigado

Equipe do *"nome do cliente"*

*"Nome de usuário", "nome do cliente",* "URL de referência" e "Endereço IP" são gerados dinamicamente com base no visitante do site e na sua rede.

## Enviar um email de boas-vindas a um usuário {#section_kjp_c3s_p1b}

Você pode enviar um email de boas-vindas para um usuário depois que ele se inscrever para uma conta. O Studio envia este email após ele enviar um email de verificação, se você configurar um email de verificação. Para enviar um email de boas-vindas:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique em **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navegue até **[!UICONTROL Email Settings]**.

1. Clique em **[!UICONTROL Send Welcome Emails To New Users]** para ativar o envio de emails.
1. Navegue até **[!UICONTROL Network Email]** para configurar o *Logotipo para Email*, o endereço de email a ser usado como o endereço de formulário (**Email - De**) e o nome de exibição a ser usado para o endereço de email de formulário (Nome **de exibição de** email).
