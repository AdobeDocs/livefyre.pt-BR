---
description: 'null'
seo-description: nulo
seo-title: Imposição SSL
solution: Experience Manager
title: Imposição SSL
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 2%

---


# Aplicação SSL{#ssl-enforcement}

Para garantir que seus dados permaneçam protegidos, estamos descontinuando o HTTP a favor do HTTPS. O Adobe Livefyre desativará completamente todas as cifras HTTP e SSL/TLS inseguras até o final de agosto de 2018. Este é um Adobe Standard projetado para proteger a privacidade de você e de seus usuários.

## Quem é afetado? {#section_jf2_4yz_kcb}

Isso pode afetar os clientes da Livefyre que:

* Chamadas de servidor para servidor de seu CRM, CMS, WordPress ou outro cliente.
* Integrações móveis (aplicativos Android e iOS)
* Aplicativos personalizados ou código personalizado

## O que preciso fazer? {#section_unv_dc5_kcb}

1. Todos os clientes do Livefyre devem se comunicar com todas as APIs via HTTPS para todo o tráfego, incluindo:

   * Integrações entre servidores (CRM, CMS, WordPress etc.)
   * Integrações móveis (aplicativos Android e iOS)
   * Aplicativos personalizados (SDK do Streamhub ou diretamente codificados).

1. O servidor para servidor e os clientes HTTP móveis devem suportar TLS 1.2
1. Altere os nomes dos hosts de `{*}.<network>.fyre.co` para `<network>.{*}.fyre.co`. Por exemplo, o nome do host `example.network.fyre.co` muda para `network.`example.fyre.co&quot;. Por exemplo:

   * `bootstrap.<network_name>.fyre.co` para `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` para `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` para `<network_name>.admin.fyre.co`

## Como faço para saber se fiz as mudanças? {#section_sqk_5d5_kcb}

Você já pode usar HTTPS, mas o Livefyre recomenda que você verifique o duplo, especialmente se você:

* Chamadas de servidor para servidor do CMS ou CRM.
* Código personalizado ou use SDKs para aplicativos personalizados em Javascript ou Mobile.
* Se sua integração tiver mais de um ano.
* Se a tecnologia em sua pilha for mais velha que um ano.

Mesmo que você já use HTTPS, verifique se seus clientes da API suportam TLS 1.2.

## Como posso verificar se meus clientes da API suportam TLS 1.2? {#section_nd1_j25_kcb}

Uma pessoa que trabalha no desenvolvimento do site pode:

* Identifique o software cliente.
* Identifique a versão.
* Leia a documentação para garantir que o cliente da API suporte TLS 1.2.
* Ative o modo de depuração, se necessário.

## Suporte a Java para TLS 1.2 {#section_lwn_rwk_ycb}

Oracle e OpenJDK JVMs para Java 8 e posterior são configurados para usar TLS 1.2, por padrão, para todas as conexões SSL. Não é necessário executar nenhuma ação adicional se você usar o Java 8 ou posterior.

Os usuários do Java 7 ou anterior devem consultar a documentação pública sobre como ativar o TLS 1.2.

## Por que preciso alterar meus nomes de host? {#section_d5q_p25_kcb}

O Livefyre não tem certificados SSL nos domínios `{*}.<network>.fyre.co`. Basta alterar o URL para HTTPS para quebrar o aplicativo.

## Preciso atualizar para a versão mais recente dos SDKs do Livefyre? {#section_dw5_s25_kcb}

Não. Em vez disso, você pode corrigir o código. Para corrigir o código, modifique algumas strings estáticas e recrie o código. Se o cliente HTTP estiver desatualizado, você também precisará atualizar ou usar outro cliente.

## Quanto tempo levará isto? {#section_lgd_v25_kcb}

O tempo necessário depende da configuração. Se você tiver uma implementação simples, levará pouco tempo para confirmar. Se você tiver muitas personalizações, precisará testar e implantar o código atualizado nos servidores ou novos aplicativos nas App Stores. Para obter melhores resultados, recomendamos que você faça uma auditoria inicial do trabalho para que possa planejar qualquer trabalho de longo prazo.

## Qual é o cronograma para concluir esse trabalho? {#section_kgk_w25_kcb}

O Livefyre desativará a porta 80 (HTTP) para nossos serviços até o final de agosto de 2018 e oferecerá suporte somente a conexões com o 443 (HTTPS). Os navegadores e outros clientes que tentarem usar HTTP falharão.

## Quando eu preciso terminar este trabalho? {#section_rvb_x25_kcb}

Todos os clientes devem usar o HTTPS até o final de julho de 2018. Se você não conseguir cumprir esse prazo, entre em contato com nossa equipe em prioritysupport@livefyre.com.
