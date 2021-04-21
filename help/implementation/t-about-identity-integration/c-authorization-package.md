---
description: Instale o Pacote de autenticação para habilitar a autenticação de usuário, para que os usuários possam interagir com seus aplicativos.
title: Pacote de autenticação
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# Pacote de Autenticação{#authentication-package}

Instale o Pacote de autenticação para habilitar a autenticação de usuário, para que os usuários possam interagir com seus aplicativos.

Os aplicativos Livefyre usam o pacote de autenticação global para associar usuários às ações do aplicativo. O pacote de autenticação está disponível por meio de `Livefyre.require`.

Para habilitar a autenticação na página, primeiro adicione `Livefyre.js` ao elemento `<head>` de sua página da Web ou modelo de site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

O uso de Livefyre.require para ativar o auth é semelhante ao uso de require para chamar outros pacotes. O código de integração para exigir autenticação é semelhante a:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Métodos {#section_ojx_1lz_fz}

Depois de incluído como acima usando `Livefyre.require`, o módulo Auth expõe os seguintes métodos que você pode chamar para notificar outros aplicativos na página sobre eventos relacionados à autenticação.

| Método | Descrição |
|--- |--- |
| `.login(callback)` | Acione o fluxo de logon conforme implementado pelo AuthDelegate registrado. Geralmente, somente os aplicativos ativados por autenticação chamarão isso, e não a própria página de host. |
| `.logout(callback)` | Notifique à autenticação que o usuário final fez logoff por alguns meios externos e que todos os aplicativos confiáveis devem apagar seu estado de autenticação até o próximo logon. Isso limpará a sessão interna mantida pelo Auth. |
| `.authenticate(credentials)` | Notifique o Auth de que um usuário foi autenticado por alguns meios externos e que um Token de autenticação do Livefyre foi obtido para o usuário final. Use essa opção se você definir um cookie com o token Livefyre ou tiver um token para o usuário e desejar fazer logon explícito no usuário. Por exemplo: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegar os detalhes de implementação da autenticação (por exemplo, o fluxo de autenticação personalizado) a um objeto definido. Isso deve ser chamado pela página de host para ativar os recursos interativos dos aplicativos do Livefyre. |
