---
description: Adicione o Livefyre aos seus aplicativos móveis nativos.
seo-description: Adicione o Livefyre aos seus aplicativos móveis nativos.
seo-title: Sdks móveis
solution: Experience Manager
title: Sdks móveis
uuid: 84 c 7 ca 1 c -3401-492 a-bfa 5-62 b 996947 a 44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sdks móveis{#mobile-sdks}

Adicione o Livefyre aos seus aplicativos móveis nativos.

Há várias opções disponíveis para implementações móveis, dependendo da extensão da personalização que você planeja fazer:

* Aplicativos móveis da Web
* Livefyre Android ou sdks do iOS
* Apis HTTP

## Aplicativos móveis da Web {#section_t2k_vpb_11b}

Os clientes que abrem uma página da Web em um dispositivo móvel obtêm automaticamente um fluxo de conteúdo do Livefyre otimizado para dispositivos móveis, incluindo estilo para ajustar o tamanho de tela e as modificações reduzidas para lidar com eventos de toque.

>[!NOTE]
>
>Ao usar um aplicativo Livefyre em um webview Android, o parâmetro [websettings. setdomstorageenabled](https://developer.android.com/reference/android/webkit/WebSettings.html) do Android deve ser definido como verdadeiro. Se localstorage não estiver ativado, o Livefyre não poderá registrar um usuário no aplicativo Livefyre.

Para otimizar para dispositivos móveis, o Livefyre limita os recursos de Comentários, Blog ao vivo e Aplicativo de bate-papo definido para incluir:

* Postagem
* Editar
* Sinalizar
* Curtir
* Responder
* Contagem de ouvinte
* Contagem de comentários
* Moderação pendente em linha
* Calvercards
* Principais comentários
* Hot Threads
* Comentários da fila

Em Aplicativos da Web móvel, clicar no nome de um autor abre informações sobre o cartão em uma nova página.

## Livefyre Android SDK ou iOS SDK {#section_zdz_spb_11b}

O Livefyre também oferece dois sdks móveis: um SDK do iOS e um Android SDK. Esses sdks são vinculados aos nossos pontos finais HTTP, criados para fornecer um método mais fácil para enviar e receber dados. Nenhuma interface é fornecida com esses sdks, permitindo maior flexibilidade com a forma como o conteúdo é exibido e usado no aplicativo móvel.

Os sdks do Android e iOS são compatíveis com os seguintes recursos para Comentários, Blog ao vivo e Bate-papo:

| Recursos do iOS: | Recursos do Android: |
|--- |--- |
| <ul><li> Postagem </li><li>Editar </li><li>Sinalizar </li><li>Curtir </li><li>Responder </li><li>Hot Threads</li></ul> | <ul><li>Postagem </li><li>Editar </li><li>Curtir </li><li>Responder </li><li>Hot Threads</li></ul> |

## Apis HTTP {#section_yqb_qpb_11b}

As apis HTTP são o grupo de pontos finais que permite criar conversas e conteúdo na plataforma Livefyre. Ele também capacita todo o Livefyre para fora dos fluxos da caixa. Embora essa solução exija mais tempo de desenvolvimento da equipe de engenharia, ela proporciona maior flexibilidade ao usar o conjunto de produtos do Livefyre e permite a integração nativa para dispositivos móveis.

>[!IMPORTANT]
>
>**Não** crie tokens de autenticação de usuário no cliente móvel, pois isso exige que você exponha sua chave de rede secreta do Livefyre em um aplicativo não seguro. Para obter uma solução mais robusta e segura, consulte a seção Tokens de autenticação do usuário.

