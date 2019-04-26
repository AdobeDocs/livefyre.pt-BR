---
description: Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza
  o conteúdo.
seo-description: Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza
  o conteúdo.
seo-title: Arquitetura
solution: Experience Manager
title: Arquitetura
uuid: 94358 e 6 c -954 a -4 a 52-9 bb 2-d 800 b 2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Arquitetura{#architecture}

Saiba mais sobre as convenções do Livefyre e como o Livefyre organiza o conteúdo.

Esta seção fornece uma visão geral da Arquitetura de rede do Livefyre.

## Visão geral de redes e sites

O Livefyre organiza os usuários e o conteúdo por rede e site. Cada rede pode ter uma ou mais contas de usuário associadas a ela, e cada rede pode incluir um ou mais sites do Livefyre. Um site do Livefyre é um agrupamento arbitrário de coleções. Uma coleção é mapeada para uma ID do artigo em seu CMS.

## Entendendo redes {#section_hqt_4m4_xz}

Os clientes com vários domínios podem compartilhar contas de usuário em todos os domínios, usando uma única rede do Livefyre. Os clientes que desejam manter contas de usuário separadas para domínios diferentes exigirão redes separadas do Livefyre.

As configurações podem ser aplicadas a sites, redes e coleções (chamadas de conversões na ilustração acima).

>[!NOTE]
>
>Algumas configurações estão disponíveis somente no nível da rede (como preferências de notificação por email, e-mail de endereço e logotipos personalizados de email). Se quiser que essas configurações sejam diferentes para cada domínio, você deve usar várias redes.

## Entendendo sites {#section_vjw_nm4_xz}

Um site é um agrupamento arbitrário de artigos. O agrupamento é útil, pois permite que você atribua moderadores diferentes a grupos diferentes de conteúdo. Os moderadores e proprietários podem ser configurados para moderar o conteúdo e configurar configurações de administração na rede ou no nível do site. Se você deseja que alguns moderadores vejam apenas determinadas Coleções, essas coleções podem ser configuradas como um site separado do Livefyre.

>[!NOTE]
>
>Não há limite para o número de sites que você pode ter na rede personalizada.

## Diagrama de sequência de aplicativos {#section_mw2_lm4_xz}

Se você estiver tentando implementar a função personalizada com os endpoints fornecidos pelo Livefyre, ou simplesmente depurar um problema, isso ajuda a entender como funciona o aplicativo de solicitação/resposta do aplicativo Livefyre.

![](assets/appsequencediagram.png)

1. Quando o cliente atingir seu site, instancie o aplicativo do Livefyre com a ID do site e a ID do artigo.
1. Se desejar autenticar o usuário (valioso para a avaliação de tráfego, além de proteção do site), envie o Livefyre as informações do site e o token do Perfil do usuário.
1. Envie o Livefyre a ID do site e a ID do artigo para inicializar o aplicativo.

   O Livefyre retorna o conteúdo inicial.

   Envie este conteúdo para a página e exiba o aplicativo.

1. Para atualizar o conteúdo exibido na página, envie o Livefyre a ID de evento mais recente da sua página. Se algum novo conteúdo estiver disponível, ele será retornado.

   Recarregue sua página com novo conteúdo e repita o processo indefinidamente.

1. Se você permitir que os usuários postem novo conteúdo, acione um evento quando novo conteúdo for postado no site para postar o conteúdo no Livefyre. O Livefyre retornará um fluxo atualizado, que pode ser usado para atualizar seu site.
