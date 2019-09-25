---
description: Os clientes que usam o Janrain Capture e o Backplane podem usar o Livefyre Auth para logon único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos Livefyre quando fizerem logon no site.
seo-description: Os clientes que usam o Janrain Capture e o Backplane podem usar o Livefyre Auth para logon único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos Livefyre quando fizerem logon no site.
seo-title: Captura de Janrain/Backplane
solution: Experience Manager
title: Captura de Janrain/Backplane
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Captura de Janrain/Backplane{#janrain-capture-backplane}

Os clientes que usam o Janrain Capture e o Backplane podem usar o Livefyre Auth para logon único (SSO), permitindo que os usuários interajam imediatamente com seus aplicativos Livefyre quando fizerem logon no site.

Para se beneficiar dessa integração integrada de Captura/Backplane, é necessário fazer alterações na configuração do aplicativo Capture e da integração do Livefyre.js.

>[!NOTE]
>
>Ignore esta seção se você não estiver usando o Janrain Capture.

Para obter mais informações, consulte a documentação [de Backplane de](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)Janrain.

1. [Configure Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Opcional) [Adicione padrões do Livefyre ao aplicativo](#c_janrain_capture_backplane/section_z2s_txt_bbb)de captura.
1. [Crie o objeto AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Sincronize com o Livefyre com o Ping para puxar.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Etapa 1: Configurar captura {#section_r2f_kxt_bbb}

O Livefyre precisa de determinadas credenciais do aplicativo Janrain Capture.

1. Configure o aplicativo Janrain Capture.
1. Obtenha as seguintes informações para o Livefyre:

   * Acesso à sua instância do Janrain Capture.
   * Acesso ao seu painel de participação do Janrain.
   * Suas configurações e credenciais de Captura.
   * Suas credenciais de Envolvimento.
   * Seu URL de identidade.

>[!NOTE]
>
>Livefyre recebe dados diretamente do CNAME; portanto, esse URL de identidade não pode ser um registro CNAMEd (um URL personalizado CNAME) que é resolvido para o CNAME real do Janrain Capture.

## Etapa 2: (Opcional) Adicione padrões do Livefyre ao aplicativo de captura {#section_z2s_txt_bbb}

Adicione os padrões do Livefyre aos usuários armazenados no aplicativo Capture para permitir que você envie notificações por email aos usuários ou que eles sigam automaticamente conversas que os usuários comentam.

1. Complete a [Etapa 1: Configure Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Adicione os seguintes campos padrão do Livefyre. Todos os campos são opcionais.

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | String   | Notificar o usuário quando alguém fizer comentários em um artigo que esteja seguindo. Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_likes]** | String   | Notificar o usuário quando alguém curtir uma de suas postagens. Pode ser imediatamente, com frequência ou nunca. |
| **[!UICONTROL livefyre_replies]** | String   | Notificar o usuário quando alguém responder a uma de suas postagens.Pode ser imediata, frequente ou nunca. |
| **[!UICONTROL livefyre_moderator_comments]** | String   | Notificar o moderador quando alguém comenta sobre uma conversa que está moderando.Pode ser imediata, frequente ou nunca. |
| **[!UICONTROL livefyre_moderator_flags]** | String   | Notificar o moderador quando alguém sinalizar uma publicação em uma conversa que está moderando.Pode ser imediata, frequente ou nunca. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Booleano | Faça com que o usuário siga uma conversa automaticamente quando sair de uma publicação. Pode ser verdadeiro ou falso. |

## Etapa 3: Construa o objeto AuthDelegate para integração com Janrain {#section_asv_vyt_bbb}

O Livefyre.required fornece um plug-in que permite que o auth escute o barramento do Backplane Janrain.

### Logon {#login}

Quando uma mensagem de identidade/login é transmitida no canal Backplane, auth.authenticate() será chamado para você com o token de Autenticação Livefyre do usuário. Você ainda deve implementar um AuthDelegate.

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
>O objeto window.Backplane deve ser definido na sua página antes de chamar auth.plugin com o plug-in Livefyre Backplane. Para garantir que o objeto Backplane esteja disponível, chame o código de instanciação do Livefyre de um retorno de chamada onReady. Consulte seu contato com o Janrain para determinar quando outros aplicativos podem usar o objeto Backplane.



>[!NOTE]
>
>O delegado de autenticação varia dependendo da sua instância Janrain.

A seguir estão alguns exemplos de como um representante de autenticação pode procurar uma integração do Janrain Capture.

* `errback`:O retorno de chamada passado para o método de logon do delegado de autenticação
* `janrain`:A referência à variável de captura do Janrain.
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

* `finishLogout`: O retorno de chamada passado para o método de logon do delegado de autenticação.

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

Isso pode vincular-se a qualquer parte do site que você gostaria que os usuários visitem para exibir sua própria página de perfil. Este exemplo apenas imprime o objeto do autor passado.

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

Como Editar perfil, isso deve vincular à página de um usuário diferente do usuário conectado no momento. Isso pode ser implementado como você desejar. Este exemplo simplesmente registra o parâmetro author no console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Etapa 4: Sincronizar com o Livefyre com o Ping para obter a integração com o Janrain {#section_ilv_bzt_bbb}

Manter o Livefyre Remote Profiles sincronizado com o sistema de gerenciamento de usuários do Capture envolve uma série de etapas chamadas Ping for Pull. Esse processo requer que você obtenha um token de acesso válido do Janrain e passe esse token para um terminal especificado na etapa 3, abaixo.

1. Obtenha um código de acesso de Janrain.

   Para obter o código de acesso, forneça as credenciais necessárias, especifique user_type como "user" e uuid como uuid do usuário atual para atualizar. Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Troque o código de acesso por um token de acesso. Forneça as credenciais necessárias, o código de acesso recebido da etapa 1 e especifique o tipo_concessão como "código_autorização".

   Para obter mais informações, consulte [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Aperte o terminal "Ping to Pull Capture" do Livefyre.

   URL do ponto de extremidade: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] onde ***{networkName}*** é o nome de rede fornecido a você pelo Livefyre, e o token jrtoken é o recebido do Janrain na etapa 2.

   Depois de atingir este terminal, você recebe uma resposta 202 e o Livefyre inicia um processo assíncrono.

## How It All Works {#concept_mty_f31_2cb}

Para se beneficiar dessa integração integrada de Captura/Backplane, é necessário fazer algumas alterações na configuração do aplicativo Capture e da integração do Livefyre.js.

Janrain envia mensagens de login/logout bem-sucedidas pelo barramento Backplane, no qual o aplicativo Livefyre, quando configurado corretamente, escuta. Essas mensagens contêm todas as informações necessárias para mostrar os usuários do aplicativo como conectados ou desconectados. Os desenvolvedores podem visualizar as mensagens do barramento do Backplane inspecionando a guia Rede no console do desenvolvedor do seu navegador.

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

Se essas mensagens não estiverem aparecendo em suas solicitações de rede, o Livefyre não terá conhecimento das tentativas de logon/logout e, portanto, o Livefyre não poderá integrar o usuário ao aplicativo.
