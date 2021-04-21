---
title: Imposição de SSL
description: Imposição de SSL
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Imposição SSL{#ssl-enforcement}

Para garantir que seus dados permaneçam seguros, estamos descontinuando o HTTP em favor do HTTPS. O Adobe Livefyre desativará completamente todas as cifras HTTP e não garantirá o SSL/TLS até o final de agosto de 2018. Este é um Adobe Standard projetado para proteger a privacidade de você e seus usuários.

## Quem é afetado? {#section_jf2_4yz_kcb}

Isso pode afetar os clientes do Livefyre que:

* Chamadas de servidor para servidor a partir de seu CRM, CMS, WordPress ou outro cliente.
* Integrações móveis (aplicativos Android e iOS)
* Aplicativos personalizados ou código personalizado

## O que preciso fazer? {#section_unv_dc5_kcb}

1. Todos os clientes do Livefyre devem se comunicar com todas as APIs via HTTPS para todo o tráfego, incluindo:

   * Integrações de servidor para servidor (CRM, CMS, WordPress etc.)
   * Integrações móveis (aplicativos Android e iOS)
   * Aplicativos personalizados (SDK do Streamhub ou codificados diretamente).

1. Os clientes HTTP de servidor para servidor e de dispositivo móvel devem ser compatíveis com o TLS 1.2
1. Altere nomes de host de `{*}.<network>.fyre.co` para `<network>.{*}.fyre.co`. Por exemplo, o nome do host `example.network.fyre.co` muda para `network.`example.fyre.co&quot;. Por exemplo:

   * `bootstrap.<network_name>.fyre.co` para `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` para `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` para `<network_name>.admin.fyre.co`

## Como posso saber se fiz as mudanças? {#section_sqk_5d5_kcb}

Você já pode usar HTTPS, mas o Livefyre recomenda verificar novamente, especialmente se você tiver:

* Chamadas de servidor para servidor do CMS ou CRM.
* Código personalizado ou use SDKs para aplicativos personalizados no Javascript ou Mobile.
* Se a integração tiver mais de um ano.
* Se a tecnologia em sua pilha for mais antiga do que um ano.

Mesmo que você já use HTTPS, deverá verificar se os clientes da API são compatíveis com TLS 1.2.

## Como posso verificar se meus clientes de API são compatíveis com TLS 1.2? {#section_nd1_j25_kcb}

Uma pessoa que trabalha no desenvolvimento do site pode:

* Identifique o software cliente.
* Identifique a versão.
* Leia a documentação para garantir que o cliente da API seja compatível com TLS 1.2.
* Ative o modo de depuração, se necessário.

## Suporte a Java para TLS 1.2 {#section_lwn_rwk_ycb}

As JVMs Oracle e OpenJDK para Java 8 e posterior são configuradas para usar TLS 1.2, por padrão, para todas as conexões SSL. Não é necessário tomar nenhuma ação adicional se você usar o Java 8 ou posterior.

Os usuários do Java 7 ou anterior devem consultar a documentação pública sobre como ativar o TLS 1.2.

## Por que preciso alterar meus nomes de host? {#section_d5q_p25_kcb}

O Livefyre não tem certificados SSL em domínios `{*}.<network>.fyre.co`. Basta alterar o URL para HTTPS e quebrar o aplicativo.

## Preciso atualizar para a versão mais recente dos SDKs do Livefyre? {#section_dw5_s25_kcb}

Não. Em vez disso, você pode corrigir o código. Para corrigir o código, você modifica algumas cadeias de caracteres estáticas e recria o código. Se o cliente HTTP estiver desatualizado, também será necessário atualizar ou usar um diferente.

## Quanto tempo levará isso? {#section_lgd_v25_kcb}

O tempo necessário depende da configuração. Se você tiver uma implementação simples, levará pouco tempo para confirmar. Se você tiver muitas personalizações, precisará testar e implantar o código atualizado nos servidores ou novos aplicativos nas App Stores. Para obter melhores resultados, recomendamos que você faça uma auditoria inicial do trabalho para que possa planejar qualquer trabalho de longo prazo.

## Qual é o calendário para a conclusão deste trabalho? {#section_kgk_w25_kcb}

O Livefyre desativará a porta 80 (HTTP) para nossos serviços até o final de agosto de 2018 e oferecerá suporte somente às conexões com o 443 (HTTPS). Os navegadores e outros clientes, que tentam usar HTTP, falharão.

## Quando preciso terminar este trabalho? {#section_rvb_x25_kcb}

Todos os clientes devem usar HTTPS até o final de julho de 2018. Se não conseguir cumprir esse prazo, entre em contato com nossa equipe em prioritysupport@livefyre.com.
