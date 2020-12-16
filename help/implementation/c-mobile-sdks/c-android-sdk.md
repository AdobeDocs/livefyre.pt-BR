---
description: Crie aplicativos Android com o Livefyre.
seo-description: Crie aplicativos Android com o Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---


# Android SDK{#android-sdk}

Crie aplicativos Android com o Livefyre.

Use esta biblioteca para integrar os serviços do Livefyre ao seu aplicativo Android nativo. O [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornece uma camada fina em torno de nossos mecanismos de API comuns, com base no ambiente de desenvolvimento Gradle/Android Studio.

O Livefyre também fornece um [Revisões](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) aplicativo de amostra, com base neste SDK.

Este Livefyre Android SDK pode ser usado no Eclipse e no Android Studio.

>[!NOTE]
>
>Antes de instalar o Livefyre Android SDK, é necessário ter o [Android SDK](https://developer.android.com/sdk/index.html) instalado no ambiente. Você também deve incluir alguns pacotes SDK do Android adicionais, conforme descrito em Documentos do desenvolvedor do Android > .
>[Adicionar pacotes SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Use o Android SDK Manager (disponível na barra de ferramentas do Android Studio ou do Eclipse) para instalar todos os pacotes recomendados. Certifique-se de incluir também o Android Support Repository.

## Eclipse {#section_dtm_slv_zz}

Para adicionar o Livefyre Android SDK ao seu projeto no Eclipse:

1. Obtenha o mais recente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) do GitHub.
1. Start com um projeto existente ou criar um novo.
1. Para importar o StreamHub-Android-SDK para o seu espaço de trabalho, vá para **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Procure e selecione StreamHub-Android-SDK; agora deve ser exibido no explorador de pacotes.
1. Clique com o botão direito do mouse em seu projeto e selecione **[!UICONTROL Properties,]** e depois a guia Android.
1. Na seção Biblioteca, selecione **[!UICONTROL Add button,]** e, em seguida, selecione StreamHub-Android-SDK na lista de bibliotecas.
1. Clique em **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para adicionar o Livefyre Android SDK ao seu projeto no Android Studio:

1. Obtenha o mais recente [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) do GitHub.
1. Start com um projeto existente ou criar um novo.
1. Clique com o botão direito do mouse em seu projeto e selecione **[!UICONTROL Open Module Settings]**.
1. Selecione o botão **[!UICONTROL +]** no canto superior esquerdo da janela.
1. Selecione **[!UICONTROL Import Existing Project.]** (na nova versão do Android Studio, você pode encontrar **[!UICONTROL Import Existing Project]** em **[!UICONTROL More Modules]**.)

1. Procure e selecione StreamHub-Android-SDK.

O Android Studio pode solicitar a conversão do SDK em uma versão gradle; se isso ocorrer, selecione **[!UICONTROL next]** e **[!UICONTROL finish]**.

Vá para **pasta de projeto > pasta de aplicativo > arquivo build.gradle** sob dependências para adicionar a seguinte dependência:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Certifique-se de que a seguinte linha esteja em sua pasta **projeto > settings.gradle** arquivo:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Você pode personalizar configurações em Config.java.

## Clientes {#section_yfq_blv_zz}

O SDK do Android do StreamHub expõe várias classes de clientes que podem ser usadas para solicitar pontos de extremidade da API do Livefyre:

* **** AdminClientExchange é um token de autenticação de usuário para informações, chaves e outros metadados do usuário.

* **** BootstrapClientObtenha conteúdo e metadados recentes sobre uma coleção específica.

* **** StreamClientPoll um fluxo para uma coleção para recuperar conteúdo novo, atualizado e excluído.

* **** WriteClientPost, sinalize e curta o conteúdo em uma coleção.

