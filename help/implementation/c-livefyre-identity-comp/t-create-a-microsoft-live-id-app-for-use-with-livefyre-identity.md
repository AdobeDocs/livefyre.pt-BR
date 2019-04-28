---
description: Você pode usar a identidade do Livefyre com a Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.
seo-description: Você pode usar a identidade do Livefyre com a Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.
seo-title: Criar um aplicativo Microsoft Live Identity para usar com a identidade do Livefyre
solution: Experience Manager
title: Criar um aplicativo Microsoft Live Identity para usar com a identidade do Livefyre
uuid: 0 c 13 e 1 bc -817 f -43 ed -85 d 5-09 c 9 e 95 b 6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo Microsoft Live Identity para usar com a identidade do Livefyre{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com a Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.

Para permitir que os usuários façam logon com suas credenciais do Microsoft Live Identity, o Livefyre exige as seguintes informações de identidade do Microsoft Live:

* ID do cliente (chave privada)
* Segredo do cliente (senha)

Para criar um aplicativo Microsoft Live Identity para uso com a identidade do Livefyre:

1. Criar ou fazer logon em uma conta do Microsoft Live em [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Crie um novo aplicativo ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. Clique em **[!UICONTROL Add Platform]**, em seguida, selecione Web como o tipo de plataforma.
1. Verifique se **[!UICONTROL Allow Implicit Flow]** a opção está marcada e digite o URL de redirecionamento, usando o nome da rede em vez de {network-name}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Gere um novo par de senhas/chave para obter a Chave privada.
1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, altere a **[!UICONTROL Enable Microsoft Live Login]** alternância para **[!UICONTROL On]**.
1. Insira a Microsoft Live Client ID e o Microsoft Live Client Secret.
1. Clique **[!UICONTROL Save Settings]** em.

Quando concluída, a página de detalhes do aplicativo Microsoft Live Identity listará a ID do cliente do aplicativo (Chave do consumidor) e o segredo do cliente (segredo do consumidor) para uso na página Configurações de integração do Studio.
