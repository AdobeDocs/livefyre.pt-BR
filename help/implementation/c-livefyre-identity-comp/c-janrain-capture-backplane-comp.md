---
description: Os clientes que usam o Janrain Capture e o Backplano podem usar o Livefyre
  Auth para logon único (SSO), permitindo que os usuários interajam imediatamente
  com seus aplicativos do Livefyre quando fizerem logon em seu site.
seo-description: Os clientes que usam o Janrain Capture e o Backplano podem usar o
  Livefyre Auth para logon único (SSO), permitindo que os usuários interajam imediatamente
  com seus aplicativos do Livefyre quando fizerem logon em seu site.
seo-title: Janrain Capturar/Plano de Fundo
solution: Experience Manager
title: Janrain Capturar/Plano de Fundo
uuid: 776 e 9626-db 04-4 c 34-adfe -681 a 71 b 552 c 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capturar/Plano de Fundo{#janrain-capture-backplane}

Os clientes que usam o Janrain Capture e o Backplano podem usar o Livefyre Auth para logon único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos do Livefyre quando fizerem logon em seu site.

Para aproveitar essa integração integrada Capturar/Backplano, você deve fazer alterações na configuração tanto no aplicativo Capturar como na integração do Livefyre. js.

>[!NOTE]
>
>Ignore esta seção se você não estiver usando o Janrain Capture.

Para obter mais informações, consulte [a documentação do Plano de fundo do Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configuração de captura.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Opcional) [Adicione padrões do Livefyre ao seu aplicativo Capturar](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Crie o objeto authdelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronize com o Livefyre com Ping para Extrair.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Etapa 1: Configurar captura {#section_r2f_kxt_bbb}

O Livefyre precisa de certas credenciais do seu aplicativo Janrain Capture.

1. Configure o aplicativo Janrain Capture.
1. Colete as seguintes informações do Livefyre:

   * Acesso à sua instância de Janrain Capture.
   * Acesso ao painel de Janelas Mobilizar.
   * Suas configurações e credenciais de captura.
   * Suas credenciais Envolver.
   * Seu URL de identidade.

>[!NOTE]
>
>O Livefyre recebe dados diretamente do CNAME; portanto, esse URL de identidade não pode ser um registro cname (uma vanity URL CNAME) que resolve o CNAME real de Janrain Capture.

## Etapa 2: (Opcional) Adicionar padrões do Livefyre ao seu aplicativo Capturar {#section_z2s_txt_bbb}

Adicione padrões do Livefyre aos usuários armazenados no aplicativo Capturar para permitir que você envie notificações por e-mail aos usuários ou permita que eles sigam automaticamente conversas que os usuários comentam.

1. Completar [etapa 1: Configuração de captura](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Adicione os seguintes campos padrão do Livefyre. Todos os campos são opcionais.

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | String | Notificar o usuário quando alguém fizer comentários em um artigo que está seguindo. Pode ser imediatamente, frequentemente ou nunca. |
| **[!UICONTROL livefyre_likes]** | String | Notificar usuário quando alguém curtir uma de suas postagens. Pode ser imediatamente, frequentemente ou nunca. |
| **[!UICONTROL livefyre_replies]** | String | Notificar o usuário quando alguém responder a uma de suas postagens. Pode ser imediatamente, frequentemente ou nunca. |
| **[!UICONTROL livefyre_moderator_comments]** | String | Notificar moderador quando alguém comentar em uma conversa que está moderando. Pode ser imediatamente, frequentemente ou nunca. |
| **[!UICONTROL livefyre_moderator_flags]** | String | Notificar moderador quando alguém sinaliza uma publicação em uma conversa que está moderando. Pode ser imediatamente, frequentemente ou nunca. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booliano | Faça com que o usuário siga uma conversa automaticamente quando ele sair de uma publicação. Pode ser verdadeiro ou falso. |

## Etapa 3: Criar o objeto authdelegate para a integração com Janrain {#section_asv_vyt_bbb}

O Livefyre. requer um plug-plugin que permita a autenticação de um ônibus de Janrain Backflight.

### Logon {#login}

Quando uma mensagem de identidade/logon é transmitida no canal de Backmap, o auth. authenticate () será chamado para você com o token de Autenticação do Livefyre do usuário. Você ainda deve implementar um authdelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>O objeto window. Backactivity deve ser definido na página antes de chamar auth. plugin com o plug-plugin do Livefyre Backplanet. Para garantir que o objeto Plano retroativo esteja disponível, chame o código de instanciação do Livefyre de um retorno de chamada onready. Entre em contato com o contato do Janrain para determinar quando outros aplicativos podem usar o objeto Backplano.



>[!NOTE]
>
>Seu delegado de autenticação variará dependendo da sua instância de Janrain.

Estes são alguns exemplos de como um representante de autenticação pode procurar uma integração de Janrain Capture.

* `errback`: O retorno de chamada passado para o método de logon do seu autenticador
* `janrain`: A referência à variável de captura do Janrain.
* `window.Backplane`: Uma referência ao objeto backplano.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

### Logout {#logout}

* `finishLogout`: O retorno de chamada passado para o método de logon do seu autenticador de autenticação.

* `window.Backplane`: Uma referência ao objeto backplano.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

### Editar perfil {#editprofile}

Isso pode ser vinculado a qualquer parte do site que você deseja que os usuários visitem para visualizar sua própria página de perfil. Este exemplo apenas imprime o objeto do autor passado.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### Exibir perfil {#viewprofile}

Como Editar perfil, isso deve vincular à página de um usuário diferente do usuário atualmente conectado. Isso pode ser implementado no entanto, você pode ser ajustado. Esse exemplo simplesmente registra o parâmetro do autor para o console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Etapa 4: Sincronizar com o Livefyre com Ping para integração com Janrain {#section_ilv_bzt_bbb}

Manter perfis remotos do Livefyre em sincronização com o sistema de gerenciamento de usuários Capturar envolve uma série de etapas chamadas Ping para Extração. Esse processo requer um token de acesso válido do Janrain e passa esse token para um terminal especificado na etapa 3 abaixo.

1. Obtenha um código de acesso do Janrain.

   Para obter o código de acesso, forneça as credenciais necessárias, especifique o user_ type como «user» e o uuid como o uuid do usuário atual para atualizar. Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Comercializa o código de acesso de um token de acesso. Forneça as credenciais necessárias, o código de acesso recebido da etapa 1 e especifique o tipo de concessão_ type como «autorização_ code».

   Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Atinja o terminal do Livefyre «Ping para captura de captura».

   URL do endpoint: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] em que ***{networkname}*** é o nome da rede fornecido pelo Livefyre, e o jrtoken é o token recebido de Janrain na etapa 2.

   Após chegar a este endpoint, você receberá uma resposta 202 e o Livefyre iniciará um processo assíncrono.

## Como tudo funciona {#concept_mty_f31_2cb}

Para se beneficiar dessa integração integrada Capturar/Backplano, você deve fazer alterações de configuração no aplicativo Capturar e na integração do Livefyre. js.

Janrain envia mensagens de login/logout bem-sucedidas por meio do ônibus Plano de fundo, no qual o aplicativo Livefyre, quando configurado corretamente, escuta. Essas mensagens contêm todas as informações necessárias para mostrar usuários do aplicativo como conectados ou desconectados. Os desenvolvedores podem exibir as mensagens de ônibus Plano de fundo inspecionando a guia Rede no console do desenvolvedor do navegador.

## Exemplo de código de logon {#section_ftt_tvp_mz}

Solicitação:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Resposta:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Resposta vazia:

```
Backplane.response([]);
```

## Exemplo de código de logout {#section_t52_svp_mz}

Solicitação:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Resposta:

```
Backplane.finishInit("{CHANNEL}");
```

Se essas mensagens não estiverem aparecendo em suas solicitações de rede, o Livefyre não estará ciente das tentativas de logon/logout e, portanto, o Livefyre não poderá integrar o usuário ao aplicativo.
