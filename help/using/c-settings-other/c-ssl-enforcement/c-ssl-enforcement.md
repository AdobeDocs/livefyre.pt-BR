---
description: 'null'
seo-description: 'null'
seo-title: Aplicação de SSL
solution: Experience Manager
title: Aplicação de SSL
uuid: e 64 af 8 c 2-3 ab 6-4034-b 385-0 e 552 d 828 c 6 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aplicação de SSL{#ssl-enforcement}

Para garantir que seus dados permaneçam protegidos, estamos obsoletos em HTTP, favorecendo HTTPS. O Adobe Livefyre desativará todos os ciphers SSL/TLS inseguros e inseguros até o fim de agosto de 2018. Este é um Adobe Standard projetado para proteger sua privacidade e seus usuários.

## Quem é afetado? {#section_jf2_4yz_kcb}

Isso pode afetar os clientes do Livefyre que têm:

* Chamadas de servidor a servidor de seu CRM, CMS, Wordpress ou outro cliente.
* Integrações móveis (aplicativos Android e iOS)
* Aplicativos personalizados ou código personalizado

## O que preciso fazer? {#section_unv_dc5_kcb}

1. Todos os clientes do Livefyre devem se comunicar com todas as apis por HTTPS para todo o tráfego, incluindo:

   * Servidor para Integrações do servidor (CRM, CMS, Wordpress etc.)
   * Integrações móveis (aplicativos Android e iOS)
   * Aplicativos personalizados (SDK simplificado ou codificada diretamente).

1. Servidor para clientes do servidor e HTTP móvel devem oferecer suporte para TLS 1.2
1. Alterar nomes de hosts `{*}.<network>.fyre.co` para `<network>.{*}.fyre.co`. Por exemplo, o nome do host `example.network.fyre.co` muda para `network.`example. fyre. co «. Por exemplo:

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## Como faço para saber se fiz as alterações? {#section_sqk_5d5_kcb}

Você já pode usar HTTPS, mas o Livefyre recomenda a verificação dupla, especialmente se você tiver:

* Chamadas de servidor a servidor do CMS ou CRM.
* Código personalizado ou uso de sdks para aplicativos personalizados em Javascript ou Mobile.
* Se a integração tiver mais de um ano.
* Se a tecnologia na pilha for superior a um ano.

Mesmo que você já use HTTPS, verifique se os clientes da API suportam TLS 1.2.

## Como faço para verificar se meus clientes da API suportam TLS 1.2? {#section_nd1_j25_kcb}

Uma pessoa que trabalha no desenvolvimento do site pode:

* Identifique o software cliente.
* Identifique a versão.
* Ler a documentação para garantir que o cliente da API seja compatível com TLS 1.2.
* Ative o modo de depuração, se necessário.

## Suporte Java para TLS 1.2 {#section_lwn_rwk_ycb}

O Oracle e o openjdk jvms para Java 8 e versões posteriores são configurados para usar TLS 1.2, por padrão, para todas as conexões SSL. Não é necessário realizar nenhuma ação adicional se você usar o Java 8 ou posterior.

Os usuários do Java 7 ou anterior devem consultar a documentação pública sobre como ativar o TLS 1.2.

## Por que preciso alterar meus nomes de host? {#section_d5q_p25_kcb}

O Livefyre não tem certificados SSL em `{*}.<network>.fyre.co` domínios. Simplesmente alterar o URL para HTTPS quebra o aplicativo.

## Preciso atualizar para a versão mais recente dos sdks do Livefyre? {#section_dw5_s25_kcb}

Não. Em vez disso, você pode corrigir o código. Para corrigir o código, você modifica algumas strings estáticas e recria o código. Se o cliente HTTP estiver desatualizado, você precisará atualizar também ou usar outro.

## Quanto tempo isso levará? {#section_lgd_v25_kcb}

O tempo necessário depende da configuração. Se você tiver uma implementação simples, deverá levar pouco tempo para confirmar. Se você tiver muitas personalizações, será necessário testar e implantar o código atualizado nos servidores ou novos aplicativos para App Stores. Para obter melhores resultados, recomendamos que você faça uma auditoria inicial do trabalho para que você possa planejar qualquer trabalho mais longo.

## Qual é a linha do tempo para concluir esse trabalho? {#section_kgk_w25_kcb}

O Livefyre desativará a porta 80 (HTTP) para nossos serviços até o fim de agosto de 2018 e suportará apenas conexões a 443 (HTTPS). Navegadores e outros clientes, que tentam usar HTTP, falharão.

## Quando preciso concluir esse trabalho? {#section_rvb_x25_kcb}

Todos os clientes precisam usar HTTPS até o fim de julho de 2018. Se não conseguir cumprir esse prazo, entre em contato com a nossa equipe em prioritysupport@livefyre.com.
