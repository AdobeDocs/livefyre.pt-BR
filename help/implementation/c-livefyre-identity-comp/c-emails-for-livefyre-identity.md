---
title: Emails para a identidade do Livefyre
description: Emails para a identidade do Livefyre
exl-id: c8127eef-8fb8-4703-ba34-ef12453f1754
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 1%

---

# Emails para identidade do Livefyre{#emails-for-livefyre-identity}

O Livefyre Identity envia os seguintes emails:

* [Email de redefinição de senha](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Email de verificação](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Enviar verificação de email para usuários](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Email de Boas-vindas](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Enviar Email de boas-vindas para usuários](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Você pode personalizar a aparência de todos os emails de identidade do Livefyre em **[!UICONTROL Integration Settings > Email Notifications.]**

## Redefinir senha do email {#section_nd1_whs_p1b}

O Livefyre envia automaticamente um email de redefinição de senha quando um usuário tenta redefinir sua senha.

O email de redefinição de senha tem esta aparência:

**Assunto:** Redefinir senha

**Corpo:**

Olá, *&lt;username>*,

Houve uma solicitação para alterar a senha do seu perfil em *&lt;nome da rede>*.

Se você solicitou isso, clique no link a seguir para escolher uma nova senha: *&lt;URL de redefinição de senha>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* são gerados dinamicamente com base no visitante do site e na rede.

## Email de verificação {#section_ak5_xhs_p1b}

Você pode enviar um email verificando o endereço de email de um usuário. Para enviar emails de verificação, você deve ativar a opção em **Integration Settings > Livefyre Identity**.

O email de verificação tem esta aparência:

**Assunto:** Verificação por correio eletrônico

**Corpo:**

Olá *&lt;nome de usuário>*,

Clique no link a seguir (ou cole no navegador) para verificar sua conta: *&lt;URL de verificação>*.

Este link expirará em 24 horas.

Obrigado,

A equipe *&lt;nome do cliente>*

*&lt;username>*,  *&lt;network name=&quot;&quot;>* e  *&lt;verification URL=&quot;&quot;>* são gerados dinamicamente com base no visitante do site e na rede.

## Enviar uma verificação de email para os usuários {#section_vyv_yhs_p1b}

Você pode enviar um email a um usuário para verificar o endereço de email que ele usa para se inscrever em uma conta. Para enviar um email de verificação:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique em **Configurações de integração > Identidade do Livefyre.**

1. Navegue até **Tipos de logon**.
1. Clique em **Exigir verificação de email** para enviar um email aos usuários que verifique o endereço de email que eles usam para se inscrever em uma conta.
1. Navegue até **Email de Rede** para configurar o **Logotipo para Email**, o endereço de email a ser usado como o endereço de origem (**Email From**) e o nome de exibição a ser usado para o endereço de email de origem (**Nome de exibição de email**).

## Email de Boas-vindas {#section_z2v_zhs_p1b}

Você pode enviar um email de boas-vindas para os usuários. Para enviar emails de boas-vindas, você deve ativar a opção em **Configurações de integração** > **Identidade do Livefyre**.

O email de boas-vindas tem esta aparência:

**Assunto:** Bem-vindo ao  *&lt;customer name=&quot;&quot;>*

**Corpo:**

Olá *&lt;nome de usuário>*,

Uma conta foi criada para você em *&lt;nome do cliente>*.

Esta conta foi criada em *&lt;URL de referência>* a partir do endereço IP *&lt;Endereço IP>*.

Se você fez isso, pode ignorar com segurança esse email.

Se você não fez isso, entre em contato com `support@livefyre.com`

Obrigado

A equipe *&quot;nome do cliente&quot;*

*&quot;Nome de usuário&quot;, &quot;nome do cliente&quot;, &quot;URL de referência&quot;* e &quot;Endereço IP&quot; são gerados dinamicamente com base no visitante do site e em sua rede.

## Enviar um email de boas-vindas a um usuário {#section_kjp_c3s_p1b}

Você pode enviar um email de boas-vindas a um usuário depois que ele se inscrever em uma conta. O Studio envia este email após enviar um email de verificação, se você configurar um email de verificação. Para enviar um email de boas-vindas:

1. No Studio, clique no ícone de engrenagem para modificar as configurações de rede.
1. Clique em **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navegue até **[!UICONTROL Email Settings]**.

1. Clique em **[!UICONTROL Send Welcome Emails To New Users]** para habilitar o envio de emails.
1. Navegue até **[!UICONTROL Network Email]** para configurar o *Logotipo para Email*, o endereço de email a ser usado como o endereço de origem (**Email From**) e o nome de exibição a ser usado para o endereço de email de origem (**Nome de exibição de email**).
