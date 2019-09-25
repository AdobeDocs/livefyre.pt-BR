---
description: Crie aplicativos Android com o Livefyre.
seo-description: Crie aplicativos Android com o Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Crie aplicativos Android com o Livefyre.

Use esta biblioteca para integrar os serviços do Livefyre ao seu aplicativo Android nativo. O [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornece uma camada fina em torno de nossos mecanismos de API comuns, com base no ambiente de desenvolvimento do Gradle/Android Studio.

O Livefyre também fornece um aplicativo de amostra de [revisões](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , com base neste SDK.

Este Livefyre Android SDK pode ser usado no Eclipse e no Android Studio.

>[!NOTE]
>
>Antes de instalar o Livefyre Android SDK, é necessário ter o SDK [do](https://developer.android.com/sdk/index.html) Android instalado no ambiente. Você também deve incluir alguns pacotes SDK do Android adicionais, conforme descrito em Documentos do desenvolvedor do Android &gt; .
>[Adding SDK Packages](https://developer.android.com/sdk/installing/adding-packages.html)

Use the Android SDK Manager (available from the Android Studio or Eclipse toolbar) to install all recommended packages. Be certain to also include the Android Support Repository.

## Eclipse {#section_dtm_slv_zz}

To add the Livefyre Android SDK to your project in Eclipse:

1. Get the latest StreamHub-Android-SDK from GitHub.[](https://github.com/Livefyre/StreamHub-Android-SDK)
1. Start with an existing project or create a new one.
1. To import the StreamHub-Android-SDK into your workspace go to .**[!UICONTROL File > Import > General > Existing Project into Workspace]**
1. Browse and select the StreamHub-Android-SDK; it should now show in the package explorer.
1. Right click on your project and select  then the Android tab.**[!UICONTROL Properties,]**
1. Under the Library section, select  then select StreamHub-Android-SDK from the list of libraries.**[!UICONTROL Add button,]**
1. Click on  and .**[!UICONTROL Apply]****[!UICONTROL OK]**

## Android Studio {#section_vpw_klv_zz}

To add the Livefyre Android SDK to your project in Android Studio:

1. Get the latest StreamHub-Android-SDK from GitHub.[](https://github.com/Livefyre/StreamHub-Android-SDK)
1. Comece com um projeto existente ou crie um novo.
1. Clique com o botão direito do mouse em seu projeto e selecione **[!UICONTROL Open Module Settings]**.
1. Selecione o **[!UICONTROL +]** botão no canto superior esquerdo da janela.
1. Selecione **[!UICONTROL Import Existing Project.]** (na nova versão do Android Studio, você pode encontrar **[!UICONTROL Import Existing Project]** em **[!UICONTROL More Modules]**.)

1. Navegue e selecione StreamHub-Android-SDK.

O Android Studio pode solicitar a conversão do SDK em uma versão gradle; se isso ocorrer, selecione **[!UICONTROL next]** e depois **[!UICONTROL finish]**.

Vá para a pasta **do projeto &gt; pasta do aplicativo &gt; arquivo build.gradle** sob dependências para adicionar a seguinte dependência:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Certifique-se de que a seguinte linha esteja na sua pasta de **projeto &gt; settings.gradle** file:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Você pode personalizar configurações em Config.java.

## Clientes {#section_yfq_blv_zz}

O SDK do Android do StreamHub expõe várias classes de clientes que podem ser usadas para solicitar pontos de extremidade da API Livefyre:

* **AdminClient** Exchange um token de autenticação de usuário para informações, chaves e outros metadados do usuário.

* **BootstrapClient** Obtenha conteúdo e metadados recentes sobre uma coleção específica.

* **StreamClient** Pesquisa um fluxo para uma coleção para recuperar conteúdo novo, atualizado e excluído.

* **WriteClient** Post, flag e curtir conteúdo em uma coleção.

