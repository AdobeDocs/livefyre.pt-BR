---
description: Para ativar um logon social, use o Studio para adicionar as credenciais dos aplicativos sociais à integração do Livefyre e personalizar o Modal de logon.
title: Uso do Studio para conectar seus aplicativos sociais à implementação do Livefyre
exl-id: 2ccb9737-8c59-4c1d-93d3-61f913b3cdd6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Uso do Studio para conectar seus aplicativos sociais à sua implementação do Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para ativar um logon social, use o Studio para adicionar as credenciais dos aplicativos sociais à integração do Livefyre e personalizar o Modal de logon.

## Personalização do modal de logon {#section_v4c_hv2_3z}

O modal de logon permite personalizar as informações que os usuários verão ao fazer logon nos aplicativos. Você pode personalizar a janela modal.

* **Logotipo:** Faça o upload de um logotipo para ser usado nos modais de logon.
* **Família de fontes:** selecione uma fonte para corresponder à sua marca.
* **Cor da marca:** Insira uma cor hexadecimal a ser usada para o texto específico na modal.
* **URL dos Termos e condições:** insira o URL da página de Termos e condições de sua empresa. Este campo é necessário para uso com a identidade do Livefyre.

## Tradução da identidade do Livefyre {#section_xxt_z52_3z}

Você pode criar e modificar conjuntos de tradução para cadeias de texto no Livefyre Identity.

Consulte Conjuntos de tradução para obter mais informações sobre o uso de conjuntos de tradução com identidade do Livefyre.

Consulte Identidade do Livefyre para obter mais informações sobre as strings específicas que você pode personalizar para a Identidade do Livefyre.

## Habilitar logon com email {#section_dlv_wzt_bbb}

Permitir que os usuários usem seus endereços de email para fazer logon e interagir com os Aplicativos do site.

Para habilitar o logon usando uma conta nativa do Livefyre:

1. Navegue até **[!UICONTROL Integration Settings]** no Livefyre Studio.
1. Alterne o botão **[!UICONTROL Enable Login with Email]** para **[!UICONTROL On]**.

## Ativar logon usando uma conta do Facebook {#section_ph3_515_bbb}

Conecte sua conta do Facebook ao Livefyre para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para habilitar o logon usando uma conta do Facebook:

1. Alterne o botão **[!UICONTROL Enable Login with Facebook]** para **[!UICONTROL ON]**.

1. Adicione os **[!UICONTROL App ID]** e **[!UICONTROL App Secret]** do seu aplicativo Facebook.

   Esses valores são listados no painel de desenvolvedores do Facebook para o aplicativo, disponível em [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Habilitar logon com o Google {#section_fq3_kb5_bbb}

Conecte sua conta do Google+ ao Livefyre para permitir que os usuários usem seus logons do Google+ para interagir com aplicativos em seu site.

Para habilitar o logon usando uma conta do Google+:

1. Alterne o botão **[!UICONTROL Enable Login with Google]** para **[!UICONTROL ON]**.

1. Adicione os **[!UICONTROL Client ID]** e **[!UICONTROL Client secret]** do seu aplicativo do Google.

   Esses valores estão listados na interface do projeto da Google Cloud Platform, disponível em [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar essas informações, vá para **[!UICONTROL API Manager > Credentials]** e clique no nome do projeto.

## Habilitar um logon usando uma conta do Twitter {#section_iyz_wb5_bbb}

Conecte sua conta do Twitter ao Livefyre para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.

Para habilitar o logon usando uma conta do Twitter:

1. Alterne o botão **[!UICONTROL Enable Login with Twitter]** para **[!UICONTROL ON]**.

1. Adicione os **[!UICONTROL Consumer Key (API Key)]** e **[!UICONTROL Consumer Secret (API Secret)]** do seu aplicativo Twitter.

   Esses valores são listados na página **[!UICONTROL Keys and Access Tokens]** do aplicativo Twitter, disponível em [https://apps.twitter.com/](https://apps.twitter.com/).

## Ativar logon usando um Yahoo! Conta {#section_s1q_3c5_bbb}

Conecte seu Yahoo! para permitir que os usuários usem seu Yahoo! logons para interagir com aplicativos do site.

Para habilitar o logon usando um Yahoo! account:

1. Alterne o botão **[!UICONTROL Enable Login with Yahoo!]** para **[!UICONTROL ON]**.

1. Adicione seu Yahoo! app&#39;s **[!UICONTROL Client ID]** e **[!UICONTROL Client Secret]**.

   Esses valores estão listados no Yahoo! página de detalhes do aplicativo, disponível em [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Habilitar logon usando uma conta do Microsoft Live {#section_z42_4c5_bbb}

Conecte sua conta do Microsoft Live ID ao Livefyre para permitir que os usuários usem seus logons do Microsoft Live ID para interagir com os aplicativos do seu site.

Para habilitar o logon usando uma conta do Microsoft Live ID:

1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, alterne o botão **[!UICONTROL Enable Microsoft Live Login]** para **[!UICONTROL On]**.

1. Insira **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Clique em **[!UICONTROL Save Settings]**.

   Os valores **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]** são listados na página de detalhes do aplicativo Microsoft Live ID.

## Conecte seus aplicativos sociais à identidade do Livefyre {#section_on2_vc5_bbb}

Permita que os usuários usem a implementação do Livefyre Identity para aplicativos em seu site.

1. Criar um aplicativo.
1. Navegue até **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** > **[!UICONTROL Livefyre Identity]**.

1. Insira as credenciais necessárias do aplicativo para o aplicativo que você criou.
