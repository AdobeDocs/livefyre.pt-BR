---
description: Adicione o Livefyre aos seus aplicativos móveis nativos.
seo-description: Adicione o Livefyre aos seus aplicativos móveis nativos.
seo-title: SDKs móveis
solution: Experience Manager
title: SDKs móveis
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDKs móveis{#mobile-sdks}

Adicione o Livefyre aos seus aplicativos móveis nativos.

Há várias opções disponíveis para implementações móveis, dependendo da extensão da personalização que você planeja fazer:

* Aplicativos Web móveis
* Livefyre Android ou iOS SDKs
* APIs HTTP

## Aplicativos Web móveis {#section_t2k_vpb_11b}

Os clientes que abrem uma página da Web em um dispositivo móvel recebem automaticamente um fluxo de conteúdo do Livefyre otimizado para dispositivos móveis, incluindo estilização para ajustar ao tamanho reduzido da tela e modificações para lidar com eventos de toque.

>[!NOTE]
>
>Ao usar um aplicativo Livefyre em um Android WebView, o parâmetro Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) deve ser definido como true. Se localStorage não estiver habilitado, o Livefyre não poderá fazer logon de um usuário no aplicativo Livefyre.

Para otimizar para dispositivos móveis, o Livefyre limita o conjunto de recursos Comentários, Blog ao vivo e Aplicativo de bate-papo para incluir:

* Publicar
* Editar  
* Segnalato
* Curtir
* Responder
* Contagem de Listener
* Contagem de comentários
* Moderação pendente em linha
* Cartões
* Principais comentários
* Threads instantâneos
* Comentários da fila

Em Aplicativos Web móveis, clicar no nome de um autor abre informações de cartão de visitas em uma nova página.

## Livefyre Android SDK ou iOS SDK {#section_zdz_spb_11b}

O Livefyre também fornece dois SDKs móveis: um iOS SDK e um Android SDK. Esses SDKs são wrappers em torno de nossos pontos finais HTTP, criados para fornecer um método mais fácil de enviar e receber dados. Nenhuma interface é fornecida com esses SDKs, permitindo maior flexibilidade com como o conteúdo é exibido e usado no aplicativo móvel.

Os SDKs para Android e iOS são compatíveis com os seguintes recursos para Comentários, Blog ao vivo e Bate-papo:

| Recursos do iOS: | Recursos do Android: |
|--- |--- |
| <ul><li> Publicar </li><li>Editar   </li><li>Segnalato </li><li>Curtir </li><li>Responder </li><li>Threads instantâneos</li></ul> | <ul><li>Publicar </li><li>Editar   </li><li>Curtir </li><li>Responder </li><li>Threads instantâneos</li></ul> |

## APIs HTTP {#section_yqb_qpb_11b}

As APIs HTTP são o grupo de pontos de extremidade que permite criar conversas e conteúdo na plataforma Livefyre. Ele também alimenta todos os fluxos de Livefyre. Embora essa solução exija mais tempo de desenvolvimento da sua equipe de engenharia, ela oferece maior flexibilidade ao usar o conjunto de produtos Livefyre e permite a integração móvel nativa.

>[!IMPORTANT]
>
>**Não** crie tokens de autenticação de usuário no cliente móvel, pois isso exigiria que você expusesse sua chave de rede secreta do Livefyre em um aplicativo não protegido. Para obter uma solução mais robusta e segura, consulte a seção Tokens de autenticação do usuário.

