---
description: Para ativar um login social, use o Studio para adicionar as credenciais dos aplicativos sociais à integração do Livefyre e personalize o Modal de login.
seo-description: Para ativar um login social, use o Studio para adicionar as credenciais dos aplicativos sociais à integração do Livefyre e personalize o Modal de login.
seo-title: Uso do Studio para conectar seus aplicativos sociais à implementação do Livefyre
title: Uso do Studio para conectar seus aplicativos sociais à implementação do Livefyre
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---


# Uso do Studio para conectar seus aplicativos sociais à implementação do Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para ativar um login social, use o Studio para adicionar as credenciais dos aplicativos sociais à integração do Livefyre e personalize o Modal de login.

## Personalização do modal de logon {#section_v4c_hv2_3z}

O modal de logon permite personalizar as informações que seus usuários verão ao fazer logon em seus aplicativos. Você pode personalizar a janela modal.

* **Logotipo:** Carregue um logotipo para usar nos seus modelos de login.
* **Família de fontes:** selecione uma fonte para corresponder à sua marca.
* **Cor da marca:** insira uma cor hexadecimal a ser usada para o texto específico no modal.
* **URL dos termos e condições:** insira o URL da página dos termos e condições da sua empresa. Este campo é necessário para o uso com o Livefyre Identity.

## Traduzindo a identidade do Livefyre {#section_xxt_z52_3z}

Você pode criar e modificar conjuntos de traduções para strings de texto na Identidade do Livefyre.

Consulte Conjuntos de tradução para obter mais informações sobre como usar conjuntos de tradução com a Livefyre Identity.

Consulte Identidade do Livefyre para obter mais informações sobre as strings específicas que você pode personalizar para a Identidade do Livefyre.

## Habilitar logon com email {#section_dlv_wzt_bbb}

Permita que os usuários usem seus endereços de email para fazer logon e interagir com os aplicativos do site.

Para ativar o logon usando uma conta nativa do Livefyre:

1. Navegue até **[!UICONTROL Integration Settings]** no Livefyre Studio.
1. Alterne a alternância **[!UICONTROL Enable Login with Email]** para **[!UICONTROL On]**.

## Habilitar logon usando uma conta do Facebook {#section_ph3_515_bbb}

Conecte sua conta do Facebook ao Livefyre para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para ativar o logon usando uma conta do Facebook:

1. Alterne a alternância **[!UICONTROL Enable Login with Facebook]** para **[!UICONTROL ON]**.

1. Adicione **[!UICONTROL App ID]** e **[!UICONTROL App Secret]** do seu aplicativo do Facebook.

   Esses valores estão listados no painel de desenvolvedores do Facebook para o aplicativo, disponível em [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Habilitar logon com o Google {#section_fq3_kb5_bbb}

Conecte sua conta do Google+ ao Livefyre para permitir que os usuários usem seus logons do Google+ para interagir com os aplicativos do site.

Para ativar o logon usando uma conta do Google+:

1. Alterne a alternância **[!UICONTROL Enable Login with Google]** para **[!UICONTROL ON]**.

1. Adicione os **[!UICONTROL Client ID]** e **[!UICONTROL Client secret]** do seu aplicativo do Google.

   Esses valores estão listados na interface de projeto da plataforma Google Cloud, disponível em [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar essas informações, vá para **[!UICONTROL API Manager > Credentials]** e clique no nome do projeto.

## Habilitar um logon usando uma conta do Twitter {#section_iyz_wb5_bbb}

Conecte sua conta do Twitter ao Livefyre para permitir que os usuários usem seus logons do Twitter para interagir com os Aplicativos em seu site.

Para ativar o logon usando uma conta do Twitter:

1. Alterne a alternância **[!UICONTROL Enable Login with Twitter]** para **[!UICONTROL ON]**.

1. Adicione os aplicativos do Twitter **[!UICONTROL Consumer Key (API Key)]** e **[!UICONTROL Consumer Secret (API Secret)]**.

   Esses valores estão listados na página **[!UICONTROL Keys and Access Tokens]** do seu aplicativo do Twitter, disponível em [https://apps.twitter.com/](https://apps.twitter.com/).

## Ative o logon usando um Yahoo! Conta {#section_s1q_3c5_bbb}

Conecte seu Yahoo! ao Livefyre para permitir que os usuários usem seu Yahoo! faça logon para interagir com os aplicativos do site.

Para ativar o logon usando um Yahoo! account:

1. Alterne a alternância **[!UICONTROL Enable Login with Yahoo!]** para **[!UICONTROL ON]**.

1. Adicione seu Yahoo! app&#39;s **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

   Esses valores estão listados no Yahoo! página de detalhes do aplicativo, disponível em [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Habilitar logon usando uma conta Microsoft Live {#section_z42_4c5_bbb}

Conecte sua conta do Microsoft Live ID ao Livefyre para permitir que os usuários usem seus logons do Microsoft Live ID para interagir com os aplicativos do site.

Para habilitar o logon usando uma conta do Microsoft Live ID:

1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, alterne a alternância **[!UICONTROL Enable Microsoft Live Login]** para **[!UICONTROL On]**.

1. Insira **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Clique em **[!UICONTROL Save Settings]**.

   Os valores **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]** estão listados na página de detalhes do aplicativo Microsoft Live ID.

## Conecte seus aplicativos sociais à identidade do Livefyre {#section_on2_vc5_bbb}

Permita que os usuários usem sua implementação do Livefyre Identity para aplicativos em seu site.

1. Criar um aplicativo.
1. Navegue até **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** **[!UICONTROL Livefyre Identity]**.

1. Digite as credenciais do aplicativo necessárias para o aplicativo que você criou.