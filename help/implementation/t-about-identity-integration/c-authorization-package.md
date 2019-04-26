---
description: Instale o Pacote de autenticação para ativar a autenticação do usuário,
  para que os usuários possam interagir com seus aplicativos.
seo-description: Instale o Pacote de autenticação para ativar a autenticação do usuário,
  para que os usuários possam interagir com seus aplicativos.
seo-title: Pacote de autenticação
solution: Experience Manager
title: Pacote de autenticação
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Pacote de autenticação{#authentication-package}

Instale o Pacote de autenticação para ativar a autenticação do usuário, para que os usuários possam interagir com seus aplicativos.

Os aplicativos do Livefyre usam o pacote global de autenticação para associar usuários com ações do aplicativo. O pacote de autenticação está disponível `Livefyre.require`.

Para ativar a autenticação na página, adicione `Livefyre.js` primeiro o `<head>` elemento de sua página da Web ou modelo de site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Usar o Livefyre. exigir a ativação de autenticação é semelhante ao uso de outros pacotes. O código de integração para exigir a autenticação dessa autenticação é:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Depois de incluída como acima, o `Livefyre.require`módulo Auth expõe os seguintes métodos que você pode chamar para notificar outros aplicativos na página sobre eventos relacionados à autenticação.

| Método | Descrição |
|--- |--- |
| `.login(callback)` | Acione o fluxo de logon conforme implementado pelo authdelegate registrado. Geralmente, somente os aplicativos autenticados por autenticação chamarão isso, e não a própria página de hospedagem. |
| `.logout(callback)` | Notificar se o usuário final fez logout por alguns meios externos e que todos os aplicativos dependentes devem limpar seu estado de autenticação até o próximo logon. Isso eliminará a sessão interna mantida por Auth. |
| `.authenticate(credentials)` | Notificar autenticação que um usuário autenticou por alguns meios externos e um token de autenticação do Livefyre foi adquirido para o usuário final. Use-o se você definir um cookie com o token do Livefyre ou ter um token para o usuário e desejar registrar explicitamente o usuário. Por exemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegar os detalhes de implementação da autenticação (por exemplo, seu fluxo de autenticação personalizado) a um objeto definido. Isso deve ser chamado pela página de host para ativar recursos interativos dos aplicativos do Livefyre. |

