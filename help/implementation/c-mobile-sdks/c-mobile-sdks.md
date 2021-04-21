---
description: Adicione o Livefyre aos seus aplicativos móveis nativos.
title: SDKs móveis
exl-id: e05001a4-6199-4d98-a661-123e031b657b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 4%

---

# SDKs móveis{#mobile-sdks}

Adicione o Livefyre aos seus aplicativos móveis nativos.

Há várias opções disponíveis para implementações móveis, dependendo da extensão da personalização que você planeja fazer:

* Aplicativos da Web móveis
* SDKs do Livefyre Android ou iOS
* APIs HTTP

## Aplicativos da Web móveis {#section_t2k_vpb_11b}

Os clientes que abrem uma página da Web em um dispositivo móvel recebem automaticamente um fluxo de conteúdo do Livefyre que é otimizado para dispositivos móveis, incluindo o estilo para ajustar o tamanho reduzido da tela e as modificações para lidar com eventos de toque.

>[!NOTE]
>
>Ao usar um Aplicativo Livefyre em um Android WebView, o parâmetro Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) deve ser definido como true. Se localStorage não estiver ativado, o Livefyre não poderá fazer logon de um usuário no aplicativo Livefyre.

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
* Threads principais
* Comentários da fila

Nos Mobile Web Apps, clicar no nome de um autor abre informações do cartão de visitas em uma nova página.

## Livefyre Android SDK ou iOS SDK {#section_zdz_spb_11b}

O Livefyre também fornece dois SDKs móveis: um iOS SDK e um Android SDK. Esses SDKs são wrappers em torno de nossos pontos de extremidade HTTP, criados para fornecer um método mais fácil de enviar e receber dados. Nenhuma interface é fornecida com esses SDKs, permitindo maior flexibilidade na exibição e uso do conteúdo no aplicativo móvel.

Os SDKs do Android e iOS são compatíveis com os seguintes recursos para Comentários, Blog ao vivo e Chat:

| Recursos do iOS: | Recursos do Android: |
|--- |--- |
| <ul><li> Publicar </li><li>Editar   </li><li>Segnalato </li><li>Curtir </li><li>Responder </li><li>Threads principais</li></ul> | <ul><li>Publicar </li><li>Editar   </li><li>Curtir </li><li>Responder </li><li>Threads principais</li></ul> |

## APIs HTTP {#section_yqb_qpb_11b}

As APIs HTTP são um grupo de endpoints que permitem criar conversas e conteúdo na plataforma Livefyre. Ele também alimenta todos os fluxos prontos do Livefyre. Embora essa solução exija mais tempo de desenvolvimento da sua equipe de engenharia, ela oferece maior flexibilidade ao usar o conjunto de produtos Livefyre e permite a integração móvel nativa.

>[!IMPORTANT]
>
>**Não** crie tokens de autenticação de usuário no cliente móvel, pois isso exigiria que você expusesse sua chave de rede secreta do Livefyre em um aplicativo não seguro. Para obter uma solução mais segura e robusta, consulte a seção Tokens de autenticação do usuário .
