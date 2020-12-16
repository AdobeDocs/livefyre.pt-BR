---
description: Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza o conteúdo.
seo-description: Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza o conteúdo.
seo-title: Arquitetura
solution: Experience Manager
title: Arquitetura
uuid: 94358e6c-954a-4a52-9bb2-d800b2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# Arquitetura{#architecture}

Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza o conteúdo.

Esta seção fornece uma visão geral da Livefyre Network Architecture.

## Visão geral de redes e sites

O Livefyre organiza usuários e conteúdo por rede e site. Cada rede pode ter uma ou mais contas de usuário associadas a ela, e cada rede pode incluir um ou mais sites do Livefyre. Um site do Livefyre é um agrupamento arbitrário de coleções. Uma coleção mapeia para uma ID de artigo no CMS.

## Noções básicas sobre redes {#section_hqt_4m4_xz}

Os clientes com vários domínios podem compartilhar contas de usuário em todos os domínios, usando uma única rede Livefyre. Os clientes que desejam manter contas de usuário separadas para domínios diferentes exigirão redes Livefyre separadas.

As configurações podem se aplicar a sites, redes e coleções (chamada de conversa na ilustração acima).

>[!NOTE]
>
>Algumas configurações estão disponíveis somente no nível da rede (como preferências de notificação por email, email do endereço e logotipos personalizados por email). Se desejar que essas configurações sejam diferentes para cada domínio, você deve usar várias redes.

## Noções básicas sobre sites {#section_vjw_nm4_xz}

Um site é um agrupamento arbitrário de artigos. O agrupamento é útil, pois permite que você atribua moderadores diferentes a grupos diferentes de conteúdo. Os moderadores e proprietários podem ser configurados para moderar o conteúdo e configurar as configurações administrativas na rede ou no nível do site. Se você deseja que alguns moderadores vejam apenas certas Coleções, essas Coleções podem ser configuradas como um site separado do Livefyre.

>[!NOTE]
>
>Não há limite para o número de sites que você pode ter em sua rede personalizada.

## Diagrama de sequência do aplicativo {#section_mw2_lm4_xz}

Quer você esteja tentando implementar uma função personalizada com pontos de extremidade fornecidos pelo Livefyre, ou simplesmente precise depurar um problema, isso ajuda a entender como o fluxo de solicitação/resposta do aplicativo Livefyre funciona.

![](assets/appsequencediagram.png)

1. Quando seu cliente acessa seu site, instancie o aplicativo Livefyre com a ID do site e a ID do artigo.
1. Se desejar autenticar o usuário (valioso para a avaliação de tráfego, bem como para a proteção do site), envie ao Livefyre as informações do site e o token de Perfil do usuário.
1. Envie o Livefyre para a ID do site e a ID do artigo para inicializar o aplicativo.

   Livefyre retorna o conteúdo inicial.

   Envie este conteúdo para a página e exiba o aplicativo.

1. Para atualizar o conteúdo exibido na página, envie o Livefyre para a ID de Evento mais recente da sua página. Se algum novo conteúdo estiver disponível, ele será retornado.

   Recarregue sua página com novo conteúdo e repita o processo indefinidamente.

1. Se você permitir que os usuários publiquem novo conteúdo, dispare um evento quando novo conteúdo for publicado em seu site para postá-lo no Livefyre. O Livefyre retornará um fluxo atualizado, que pode ser usado para atualizar seu site.
