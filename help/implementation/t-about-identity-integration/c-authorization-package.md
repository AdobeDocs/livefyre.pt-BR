---
description: Instale o pacote de autenticação para ativar a autenticação do usuário, de modo que os usuários possam interagir com seus aplicativos.
seo-description: Instale o pacote de autenticação para ativar a autenticação do usuário, de modo que os usuários possam interagir com seus aplicativos.
seo-title: Pacote de autenticação
solution: Experience Manager
title: Pacote de autenticação
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---


# Pacote de autenticação{#authentication-package}

Instale o pacote de autenticação para ativar a autenticação do usuário, de modo que os usuários possam interagir com seus aplicativos.

Os aplicativos Livefyre usam o pacote de autenticação global para associar usuários às ações do aplicativo. O pacote de autenticação está disponível por meio de `Livefyre.require`.

Para habilitar a autenticação na sua página, primeiro adicione `Livefyre.js` ao elemento `<head>` da sua página da Web ou modelo de site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

O uso do Livefyre.demand para ativar o auth é semelhante ao uso do exigir para chamar outros pacotes. O código de integração para exigir autenticação é semelhante a:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Depois de incluído como acima usando `Livefyre.require`, o módulo Auth expõe os seguintes métodos que você pode chamar para notificar outros aplicativos na página sobre eventos relacionados à autenticação.

| Método | Descrição |
|--- |--- |
| `.login(callback)` | Acione o fluxo de logon como implementado pelo AuthDelegate registrado. Geralmente, somente aplicativos ativados por autenticação chamarão isso, e não a própria página do host. |
| `.logout(callback)` | Notifique o Auth de que o usuário final fez logout por algum meio externo e que todos os aplicativos confiáveis devem apagar seu estado de autenticação até o próximo login. Isso limpará a sessão interna mantida pelo Auth. |
| `.authenticate(credentials)` | Notifique o Auth de que um usuário foi autenticado por algum meio externo e que um Livefyre Authentication Token foi obtido para o usuário final. Use-o se você definir um cookie com o token Livefyre ou tiver um token para o usuário e quiser fazer logon explicitamente no usuário. Por exemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegar os detalhes de implementação da autenticação (por exemplo, seu fluxo de autenticação personalizado) a um objeto que você definir. Isso deve ser chamado pela página de host para ativar os recursos interativos dos aplicativos Livefyre. |

