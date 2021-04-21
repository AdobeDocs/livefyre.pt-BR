---
description: Crie aplicativos Android com o Livefyre.
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Android SDK{#android-sdk}

Crie aplicativos Android com o Livefyre.

Use essa biblioteca para integrar os serviços do Livefyre ao seu aplicativo Android nativo. O [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornece uma camada fina em torno de nossos mecanismos de API comuns, com base no ambiente de desenvolvimento Gradle/Android Studio.

Livefyre também fornece um aplicativo de amostra [Resviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App), com base nesse SDK.

Esse SDK do Livefyre Android pode ser usado no Eclipse e no Android Studio.

>[!NOTE]
>
>Antes de instalar o Livefyre Android SDK, você deve ter o [Android SDK](https://developer.android.com/sdk/index.html) instalado em seu ambiente. Você também deve incluir alguns pacotes adicionais de SDK do Android, conforme descrito em Documentos do desenvolvedor do Android > .
>[Adicionar pacotes SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Use o Android SDK Manager (disponível na barra de ferramentas do Android Studio ou Eclipse) para instalar todos os pacotes recomendados. Certifique-se de incluir também o Repositório de Suporte do Android.

## Eclipse {#section_dtm_slv_zz}

Para adicionar o Livefyre Android SDK ao seu projeto no Eclipse:

1. Obtenha o [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) mais recente do GitHub.
1. Comece com um projeto existente ou crie um novo.
1. Para importar o StreamHub-Android-SDK para o seu espaço de trabalho, vá para **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. Navegue e selecione o StreamHub-Android-SDK; agora deve ser exibido no gerenciador de pacotes.
1. Clique com o botão direito no projeto e selecione **[!UICONTROL Properties,]** e depois a guia Android.
1. Na seção Biblioteca , selecione **[!UICONTROL Add button,]** e selecione StreamHub-Android-SDK na lista de bibliotecas.
1. Clique em **[!UICONTROL Apply]** e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para adicionar o Livefyre Android SDK ao seu projeto no Android Studio:

1. Obtenha o [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) mais recente do GitHub.
1. Comece com um projeto existente ou crie um novo.
1. Clique com o botão direito no projeto e selecione **[!UICONTROL Open Module Settings]**.
1. Selecione o botão **[!UICONTROL +]** no canto superior esquerdo da janela.
1. Selecione **[!UICONTROL Import Existing Project.]** (Na nova versão do Android Studio, você pode encontrar **[!UICONTROL Import Existing Project]** em **[!UICONTROL More Modules]**.)

1. Navegue e selecione o SDK do StreamHub-Android.

O Android Studio pode solicitar a conversão do SDK para a versão de gradle; se isso ocorrer, selecione **[!UICONTROL next]** e **[!UICONTROL finish]**.

Vá para **project folder > app folder > build.gradle** sob dependências para adicionar a seguinte dependência:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Certifique-se de que a linha a seguir esteja em seu arquivo **project folder > settings.gradle**:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Você pode personalizar configurações de dentro do Config.java.

## Clientes {#section_yfq_blv_zz}

O SDK do Android do StreamHub expõe várias classes de clientes que podem ser usadas para solicitar pontos de extremidade da API do Livefyre:

* **** AdminClientExchange um token de autenticação de usuário para informações de usuário, chaves e outros metadados.

* **** Conteúdo e metadados recentes do BootstrapClientGet sobre uma coleção específica.

* **** StreamClientPoll um fluxo para uma coleção para recuperar conteúdo novo, atualizado e excluído.

* **** WriteClientPost, flag e como conteúdo em uma coleção.
