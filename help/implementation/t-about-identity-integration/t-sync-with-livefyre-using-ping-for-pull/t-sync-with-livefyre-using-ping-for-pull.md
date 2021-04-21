---
description: Use o Ping for Pull para manter o Livefyre sincronizado com seu sistema de gerenciamento de usuários.
title: Sincronizar com o Livefyre usando o Ping para pull
exl-id: 01b5851d-9dc0-44dc-9c0d-0c467502450d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Sincronizar com Livefyre usando Ping para Pull{#sync-with-livefyre-using-ping-for-pull}

Use o Ping for Pull para manter o Livefyre sincronizado com seu sistema de gerenciamento de usuários.

Em geral, você ***Ping*** Livefyre sempre que um usuário do seu site/aplicativo atualizar seu perfil (nome de exibição, avatar etc.) e Livefyre ***Puxa*** o perfil atualizado desse usuário.

![](assets/Ping-for-Pull.png)

Ping para sequência de pull:

1. O cliente envia a solicitação de Ping para o Livefyre (incluindo o Usuário a ser atualizado).
1. Livefyre confirma o recebimento do Ping com HTTP 200/Success.
1. O Livefyre processa a solicitação de pull.
1. Livefyre filas Solicitação de pull.
1. Livefyre executa a Solicitação de pull para o endpoint para capturar informações atualizadas do usuário.
1. O cliente recebe a resposta de pull e valida.
1. O Livefyre atualiza Perfis Remotos com as informações de perfil externo incluídas no endpoint Pull .

Faça o ping do Livefyre sempre que um usuário atualizar as informações de seu perfil. Embora o tempo de conclusão do Ping for Pull possa variar dependendo da carga da rede, ele atualizará as informações do usuário em entre 1 e 10 minutos. As alterações de perfil atualizadas serão exibidas primeiro no Livefyre Studio > Usuários.

As informações atualizadas do Perfil serão exibidas nos aplicativos Livefyre após dois eventos:

* Um usuário faz logoff e, em seguida, faz logon novamente no aplicativo. Os valores de nome de exibição no userAuthToken têm prioridade sobre Ping para atualizações de Pull. Um usuário que efetuar logout/logon atualizará o token para atualizar a sessão.

   Para gerar novos userAuthTokens quando as informações do perfil forem atualizadas, use o SSO authDelegate para fazer logoff do usuário e, em seguida, faça logon novamente em segundo plano.

* Uma atualização do bootstrap para a Coleção incluirá as informações atualizadas (no máximo, a cada 5-10 minutos).

Para implementar o Ping for Pull no sistema de Perfil do usuário:

1. [Crie o ponto de extremidade de pull](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >A biblioteca Livefyre inclui um método syncUser para manter seus perfis de usuário atualizados. Pule as próximas duas etapas se você usar a biblioteca do Livefyre.

1. [Registre o endpoint Pull no Studio](#register_the_endpoint_with_studio).
1. [Crie o ping](#t_build_the_ping).
1. [Crie o Ping para Resposta de Puxo].(#reference_n3x_pzb_mz)
