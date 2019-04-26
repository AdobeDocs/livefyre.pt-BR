---
description: Criar aplicativos Android desenvolvidos pelo Livefyre.
seo-description: Criar aplicativos Android desenvolvidos pelo Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Criar aplicativos Android desenvolvidos pelo Livefyre.

Use essa biblioteca para integrar os serviços do Livefyre no aplicativo Android nativo. O [Livefyre streamhub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) fornece uma camada fina em torno dos mecanismos de API comuns, com base no ambiente de desenvolvimento Gradle/Android Studio.

O Livefyre também fornece [um Aplicativo](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) de amostra, com base neste SDK.

Este SDK do Livefyre Android pode ser usado no Eclipse e no Android Studio.

>[!NOTE]
>
>Antes de instalar o SDK do Livefyre Android, é necessário ter o [Android SDK](https://developer.android.com/sdk/index.html) instalado em seu ambiente. Você também deve incluir alguns pacotes adicionais do Android SDK, conforme descrito nos documentos do desenvolvedor do Android >.
>[Adição de pacotes SDK](https://developer.android.com/sdk/installing/adding-packages.html)

Use o Android SDK Manager (disponível na barra de ferramentas do Android Studio ou Eclipse) para instalar todos os pacotes recomendados. Certifique-se de incluir também o Repositório de suporte para Android.

## Eclipse {#section_dtm_slv_zz}

Para adicionar o SDK do Livefyre Android ao projeto no Eclipse:

1. Obtenha o [streamhub-Android-SDK mais recente](https://github.com/Livefyre/StreamHub-Android-SDK) do github.
1. Comece com um projeto existente ou crie uma nova.
1. Para importar o streamhub-Android-SDK para a sua área de trabalho **[!UICONTROL File > Import > General > Existing Project into Workspace]**, acesse.
1. Navegue e selecione o streamhub-Android-SDK; agora deve ser exibido no pacote do explorer.
1. Clique com o botão direito do mouse em seu projeto e selecione **[!UICONTROL Properties,]** a guia Android.
1. Na seção Biblioteca, selecione, **[!UICONTROL Add button,]** em seguida, streamhub-Android-SDK na lista de bibliotecas.
1. Clique **[!UICONTROL Apply]** em e **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

Para adicionar o SDK do Livefyre Android ao projeto no Android Studio:

1. Obtenha o [streamhub-Android-SDK mais recente](https://github.com/Livefyre/StreamHub-Android-SDK) do github.
1. Comece com um projeto existente ou crie uma nova.
1. Clique com o botão direito do mouse em seu projeto e selecione **[!UICONTROL Open Module Settings]**.
1. Selecione o **[!UICONTROL +]** botão no canto superior esquerdo da janela.
1. Selecione **[!UICONTROL Import Existing Project.]** (na nova versão do Android studio, você pode encontrar **[!UICONTROL Import Existing Project]** abaixo **[!UICONTROL More Modules]**.)

1. Navegue e selecione o streamhub-Android-SDK.

O Android Studio pode solicitar que você converta o SDK para a versão gradle; se isso ocorrer, selecione **[!UICONTROL next]** -o em seguida **[!UICONTROL finish]**.

Vá para **pasta do projeto > pasta do aplicativo > build. gradle** em dependências para adicionar a seguinte dependência:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Verifique se a linha a seguir está **no** arquivo pastas > configurações. gradle:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Você pode personalizar configurações de dentro de Config. java.

## Clientes {#section_yfq_blv_zz}

O streamhub Android SDK expõe várias classes de cliente que podem ser usadas para solicitar pontos finais da API do Livefyre:

* **Adminclient** Exchange um token de autenticação de usuário para informações, chaves e outros metadados do usuário.

* **Bootstrapclient** Obter conteúdo recente e metadados sobre uma Coleção específica.

* **Streamclient** Pesquisa um fluxo para uma coleção para recuperar conteúdo novo, atualizado e excluído.

* **Writeclient** Post, sinalizador e conteúdo semelhante em uma coleção.

