---
description: Use o Ping for Pull para manter o Livefyre sincronizado com seu sistema de gerenciamento de usuários.
seo-description: Use o Ping for Pull para manter o Livefyre sincronizado com seu sistema de gerenciamento de usuários.
seo-title: Sincronizar com o Livefyre usando o Ping para puxar
solution: Experience Manager
title: Sincronizar com o Livefyre usando o Ping para puxar
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Sincronizar com o Livefyre usando o Ping para o Pull{#sync-with-livefyre-using-ping-for-pull}

Use o Ping for Pull para manter o Livefyre sincronizado com seu sistema de gerenciamento de usuários.

Em geral, você ***Ping*** Livefyre sempre que um usuário do seu site/aplicativo atualizar seu perfil (nome de exibição, avatar etc.) e Livefyre ***Pulls*** o perfil atualizado desse usuário.

![](assets/Ping-for-Pull.png)

Ping para Sequência de Baixa Automática:

1. O cliente envia a solicitação de Ping para o Livefyre (incluindo a atualização do usuário).
1. Livefyre confirma o recebimento do Ping com HTTP 200/Êxito.
1. O Livefyre processa a solicitação de recebimento.
1. Livefyre filas Solicitação de recebimento.
1. O Livefyre executa a solicitação de puxamento para o terminal para capturar informações atualizadas do usuário.
1. O cliente recebe a resposta de recebimento e valida.
1. O Livefyre atualiza Perfis remotos com as informações de perfil externo incluídas no ponto de extremidade de Puxo.

Faça o ping do Livefyre sempre que um usuário atualizar suas informações de perfil. Embora o tempo de conclusão de Ping para Pull possa variar dependendo da carga da rede, ele atualizará as informações do usuário em 1 a 10 minutos. As alterações de perfil atualizadas serão exibidas primeiro no Livefyre Studio > Usuários.

As informações atualizadas do Perfil aparecerão nos aplicativos Livefyre após dois eventos:

* Um usuário faz logout e, em seguida, faz login novamente no aplicativo. Os valores de nome de exibição no userAuthToken têm prioridade sobre Ping para atualizações de Puxo. Um usuário que fizer logout/login atualizará o token para atualizar a sessão.

   Para gerar novos userAuthTokens quando as informações do perfil forem atualizadas, use o SSO authDelegate para fazer logout do usuário e login novamente em segundo plano.

* Uma atualização do bootstrap para a coleção traz as informações atualizadas (no máximo, a cada 5 a 10 minutos).

Para implementar o Ping for Pull no sistema de Perfil do usuário:

1. [Crie o ponto de extremidade](#t_build_the_pull_endpoint) de Puxo.

   >[!NOTE]
   >
   >A biblioteca do Livefyre inclui um método syncUser para manter seus perfis de usuário atualizados. Ignore as próximas duas etapas se você usar a biblioteca do Livefyre.

1. [Registre o ponto de extremidade de Puxo no Studio](#register_the_endpoint_with_studio).
1. [Crie o Ping](#t_build_the_ping).
1. [Crie o Ping para obter uma resposta].(#reference_n3x_pzb_mz)
