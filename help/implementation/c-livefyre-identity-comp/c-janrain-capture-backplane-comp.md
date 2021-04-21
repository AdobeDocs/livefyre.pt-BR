---
description: Os clientes que usam a Captura do Comboio e o Backplane podem usar a Autenticação do Livefyre para Logon Único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos do Livefyre quando fazem logon no site.
title: Captura/Backplane do Janrain
exl-id: c7e6cfef-7570-4f9c-9d2c-79f890ee5c49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 1%

---

# Captura/Backplane do Janrain{#janrain-capture-backplane}

Os clientes que usam a Captura do Comboio e o Backplane podem usar a Autenticação do Livefyre para Logon Único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos do Livefyre quando fazem logon no site.

Para se beneficiar dessa integração interna de Captura/Backplane, é necessário fazer alterações na configuração do aplicativo Capture e da integração Livefyre.js.

>[!NOTE]
>
>Pule esta seção se não estiver usando o Janrain Capture.

Para obter mais informações, consulte a [documentação do Backplane do Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Configure Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Opcional) [Adicionar padrões do Livefyre ao seu aplicativo de captura](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Crie o objeto AuthDelegate .](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronize com o Livefyre com o Ping for Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Etapa 1: Configurar Captura {#section_r2f_kxt_bbb}

O Livefyre precisa de determinadas credenciais do aplicativo de Captura do Windows.

1. Configure o aplicativo de Captura do Comboio.
1. Obtenha as seguintes informações para o Livefyre:

   * Acesso à sua instância de Captura do Comboio.
   * Acesso ao seu painel do Mobilizar.
   * Suas configurações e credenciais de Captura.
   * Suas credenciais do Engage.
   * Seu URL de identidade.

>[!NOTE]
>
>Livefyre recebe dados diretamente do CNAME; portanto, esse URL de identidade não pode ser um registro CNAMEd (um CNAME de URL personalizado) que é resolvido para o CNAME real da Captura do Janrain.

## Etapa 2: (Opcional) Adicione os padrões do Livefyre ao aplicativo de captura {#section_z2s_txt_bbb}

Adicione os padrões do Livefyre aos usuários armazenados em seu aplicativo Capture para permitir que você envie aos usuários notificações por email ou permita que eles sigam automaticamente as conversas comentadas pelos usuários.

1. Conclua [Etapa 1: Configure Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Adicione os seguintes campos padrão do Livefyre. Todos os campos são opcionais.

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | String   | Notificar o usuário quando alguém comentar em um artigo que esteja seguindo. Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_likes]** | String   | Notifique o usuário quando alguém curtir uma de suas publicações. Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_replies]** | String   | Notificar o usuário quando alguém responder a uma de suas postagens.Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_moderator_comments]** | String   | Notifique o moderador quando alguém comenta em uma conversa que está moderando.Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_moderator_flags]** | String   | Notifique o moderador quando alguém sinalizar uma publicação em uma conversa que está moderando.Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Faça com que o usuário siga automaticamente uma conversa quando sair de uma publicação. Pode ser verdadeiro ou falso. |

## Etapa 3: Criar o objeto AuthDelegate para integração do Janrain {#section_asv_vyt_bbb}

Livefyre.require fornece um plug-in que permite que o auth ouça o barramento do Backplane Janrain.

### Logon {#login}

Quando uma mensagem de identidade/login é transmitida no canal Backplane, auth.authentication() será chamado para você com o token de autenticação Livefyre do usuário. Você ainda deve implementar um AuthDelegate.

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
>O objeto window.Backplane deve ser definido na página antes de chamar auth.plugin com o plug-in Livefyre Backplane. Para garantir que o objeto Backplane esteja disponível, chame o código de instanciação do Livefyre a partir de um retorno de chamada onReady. Consulte o contato do Janrain para determinar quando outros aplicativos podem usar o objeto Backplane.



>[!NOTE]
>
>O delegado de autenticação varia de acordo com a instância do Janrain.

A seguir estão alguns exemplos de como um representante de autenticação pode procurar uma integração com o Janrain Capture.

* `errback`: O retorno de chamada passado para o método de logon do delegado de autenticação
* `janrain`: A referência para a variável de captura do Janrain.
* `window.Backplane`: Uma referência ao objeto Backplane.

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

* `finishLogout`: O retorno de chamada foi passado para o método de logon do delegado de autenticação.

* `window.Backplane`: Uma referência ao objeto Backplane.

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

Isso pode vincular-se a qualquer parte do site que você gostaria que os usuários visitem para visualizar sua própria página de perfil. Este exemplo apenas imprime o objeto do autor transmitido.

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

Como Editar perfil, isso deve vincular a uma página de usuário diferente da página que está conectada no momento. Isso pode ser implementado da maneira que você entender. Este exemplo simplesmente registra o parâmetro author no console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Etapa 4: Sincronizar com o Livefyre com o Ping for Pull for Janrain Integration {#section_ilv_bzt_bbb}

Manter os perfis remotos do Livefyre sincronizados com seu sistema de gerenciamento de usuários do Capture envolve uma série de etapas chamadas Ping for Pull. Esse processo requer que você obtenha um token de acesso válido do Janrain e, em seguida, transmita esse token para um endpoint especificado na etapa 3, abaixo.

1. Obtenha um código de acesso de Janrain.

   Para obter o código de acesso, forneça as credenciais necessárias, especifique o user_type como &quot;user&quot; e o uuid como o uuid do usuário atual para atualizar. Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Troque o código de acesso por um token de acesso. Forneça as credenciais necessárias, o código de acesso recebido da etapa 1 e especifique o grant_type como &quot;authorization_code&quot;.

   Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Clique no ponto de extremidade &quot;Ping to Pull Capture&quot; do Livefyre.

   URL do ponto de extremidade: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] onde ***{networkName}*** é o nome de rede fornecido a você pelo Livefyre, e o jrtoken é o token recebido do Janrain na etapa 2.

   Depois de atingir esse terminal, você receberá uma resposta 202 e o Livefyre iniciará um processo assíncrono.

## Como tudo funciona {#concept_mty_f31_2cb}

Para se beneficiar dessa integração interna de Captura/Backplane, é necessário fazer algumas alterações na configuração do aplicativo Capture e da integração Livefyre.js.

Janrain envia mensagens de login/logout bem-sucedidas por meio do barramento Backplane, no qual o aplicativo Livefyre, quando configurado corretamente, escuta. Essas mensagens contêm todas as informações necessárias para mostrar aos usuários do aplicativo como conectados ou desconectados. Os desenvolvedores podem visualizar as mensagens do barramento do Backplane inspecionando a guia Rede no console do desenvolvedor do navegador.

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

Se essas mensagens não estiverem aparecendo nas solicitações de rede, o Livefyre não estará ciente das tentativas de logon/logout e, portanto, o Livefyre não poderá integrar o usuário ao aplicativo.
