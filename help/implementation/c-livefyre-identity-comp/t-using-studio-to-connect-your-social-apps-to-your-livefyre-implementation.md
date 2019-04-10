---
description: Para habilitar um login social, use o Studio para adicionar as credenciais
  de aplicativos sociais à integração do Livefyre e personalize o modal de logon.
seo-description: Para habilitar um login social, use o Studio para adicionar as credenciais
  de aplicativos sociais à integração do Livefyre e personalize o modal de logon.
seo-title: Usando o Studio para conectar seus aplicativos sociais à implementação
  do Livefyre
title: Usando o Studio para conectar seus aplicativos sociais à implementação do Livefyre
uuid: be 14869 c-e 0 df -48 cd-a 1 f 3-99 eb 953 dd 9 ce
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Usando o Studio para conectar seus aplicativos sociais à implementação do Livefyre{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Para habilitar um login social, use o Studio para adicionar as credenciais de aplicativos sociais à integração do Livefyre e personalize o modal de logon.

## Personalização do modal de logon {#section_v4c_hv2_3z}

O modal de logon permite que você personalize as informações que seus usuários verão ao fazer logon nos seus aplicativos. Você pode personalizar a janela modal.

* **Logotipo:** Carregue um logotipo para uso nas modais de logon.
* **Família de fontes:** Selecione uma fonte para corresponder à marca.
* **Cor da marca:** Insira uma cor hexadecimal para ser usada para texto específico dentro do modal.
* **URL de termos e condições:** Insira o URL da página Termos e condições da sua empresa. Esse campo é necessário para uso com a identidade do Livefyre.

## Tradução de identidade do Livefyre {#section_xxt_z52_3z}

É possível criar e modificar conjuntos de traduções para strings de texto na Identidade do Livefyre.

Consulte Conjuntos de tradução para obter mais informações sobre como usar conjuntos de traduções com Identidade do Livefyre.

Consulte Identidade do Livefyre para saber mais sobre as strings específicas que você pode personalizar para a identidade do Livefyre.

## Ativar logon com email {#section_dlv_wzt_bbb}

Permita que os usuários usem seus endereços de email para fazer logon e interagir com aplicativos em seu site.

Para ativar o logon usando uma conta nativa do Livefyre:

1. Navegue até **[!UICONTROL Integration Settings]** o Livefyre Studio.
1. Alterne para a **[!UICONTROL Enable Login with Email]** alternância **[!UICONTROL On]**.

## Ativar logon usando uma conta do Facebook {#section_ph3_515_bbb}

Conecte sua conta do Facebook ao Livefyre para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.

Para ativar o logon usando uma conta do Facebook:

1. Alterne para a **[!UICONTROL Enable Login with Facebook]** alternância **[!UICONTROL ON]**.

1. Adicione seu aplicativo do Facebook **[!UICONTROL App ID]** e **[!UICONTROL App Secret]**.

   Esses valores estão listados no painel de desenvolvedores do Facebook para o aplicativo, disponível em [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Ativar logon com o Google {#section_fq3_kb5_bbb}

Conecte sua conta do Google + ao Livefyre para permitir que os usuários usem seus logons do Google + para interagir com Aplicativos no seu site.

Para ativar o logon usando uma conta do Google +:

1. Alterne para a **[!UICONTROL Enable Login with Google]** alternância **[!UICONTROL ON]**.

1. Adicione seu aplicativo do Google **[!UICONTROL Client ID]** e **[!UICONTROL Client secret]**.

   Esses valores estão listados na interface do projeto da plataforma do Google Cloud, disponível em [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library). Para recuperar essas informações, vá para **[!UICONTROL API Manager > Credentials]**e clique no nome do projeto.

## Ativar um logon usando uma conta do Twitter {#section_iyz_wb5_bbb}

Conecte sua conta do Twitter ao Livefyre para permitir que os usuários usem seus logons do Twitter para interagir com Aplicativos no seu site.

Para ativar o logon usando uma conta do Twitter:

1. Alterne para a **[!UICONTROL Enable Login with Twitter]** alternância **[!UICONTROL ON]**.

1. Adicione seu aplicativo do Twitter **[!UICONTROL Consumer Key (API Key)]** e **[!UICONTROL Consumer Secret (API Secret)]**.

   Esses valores estão listados na **[!UICONTROL Keys and Access Tokens]** página do seu aplicativo do Twitter, disponível em [https://apps.twitter.com/](https://apps.twitter.com/).

## Habilitar logon usando um Yahoo! Conta {#section_s1q_3c5_bbb}

Conecte seu Yahoo! conta ao Livefyre para permitir que os usuários usem seus Yahoo! logons para interagir com aplicativos em seu site.

Para ativar o logon usando um Yahoo! :

1. Alterne para a **[!UICONTROL Enable Login with Yahoo!]** alternância **[!UICONTROL ON]**.

1. Adicione o Yahoo! e **[!UICONTROL Client ID]****[!UICONTROL Client Secret]**.

   Esses valores estão listados no Yahoo! página de detalhes do aplicativo, disponível em [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Ativar logon usando uma conta Microsoft Live {#section_z42_4c5_bbb}

Conecte sua conta do Microsoft Live ID ao Livefyre para permitir que os usuários usem seus logons de ID do Microsoft Live para interagir com Aplicativos no seu site.

Para ativar o logon usando uma conta do Microsoft Live ID:

1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**, altere a **[!UICONTROL Enable Microsoft Live Login]** alternância para **[!UICONTROL On]**.

1. Insira o **[!UICONTROL Microsoft Live Client ID (Private Key)]** e **[!UICONTROL Microsoft Live Client Secret (Password)]**.

1. Clique **[!UICONTROL Save Settings]**em.

   Os **[!UICONTROL Microsoft Live Client ID (Private Key)]** valores e os **[!UICONTROL Microsoft Live Client Secret (Password)]** valores são listados na página de detalhes do aplicativo Microsoft Live ID.

## Conecte seus aplicativos do Social à identidade do Livefyre {#section_on2_vc5_bbb}

Permita que os usuários usem sua implementação de identidade do Livefyre para aplicativos em seu site.

1. Criar um aplicativo.
1. Navegue **[!UICONTROL Studio]** até > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**.

1. Insira as credenciais do aplicativo necessárias para o aplicativo criado.