---
description: Adicione o Livefyre ao seu aplicativo iOS nativo.
seo-description: Adicione o Livefyre ao seu aplicativo iOS nativo.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Adicione o Livefyre ao seu aplicativo iOS nativo.

Use essa biblioteca de código aberto para integrar os serviços do Livefyre ao seu aplicativo iOS nativo. O Livefyre StreamHub iOS SDK fornece uma camada fina em torno de nossos mecanismos de API comuns, com base na excelente biblioteca AFNetworking.

O Livefyre também fornece dois aplicativos de amostra do iOS baseados neste SDK: um fluxo de comentários e um aplicativo de amostra de revisões.

## Integração do SDK ao seu projeto como um pod de cacau (recomendado) {#section_qc5_h3v_zz}

A maneira mais conveniente de adicionar o SDK do StreamHub-iOS ao seu projeto é usar o CocoaPods. Se você não tiver CocoaPods, execute gem install coapods e configuração de pod. Este é um exemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Você também precisará adicionar um repositório Specs à sua instalação do CocoaPod (isso irá cloná-lo para o `~/.cocoapods/repos` diretório):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Depois que o arquivo Podfile for criado na raiz do projeto do aplicativo e o repositório acima adicionado, execute:

```
pod install
```

Isso baixará todas as dependências e criará um arquivo MyApp.xcworkspace, que você deve usar a partir de agora para abrir o projeto do aplicativo no Xcode.

## Como um subprojeto Xcode {#section_jcm_g3v_zz}

Como alternativa, clone o repositório:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Em seguida, adicione o projeto Xcode (LFSClient.xcodeproj) ao seu aplicativo como um subprojeto (facilmente feito arrastando o arquivo LFSClient.xcodeproj para o painel Navegador do projeto no Xcode).

Você também precisará fazer o mesmo com qualquer uma das dependências ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Baixar tudo de uma vez (não recomendado) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Para executar testes no Xcode 6, você deve adicionar $(PLATFORM_DIR)/Developer/Library/Frameworks a FRAMEWORK_SEARCH_PATHS em Pods-test-XCTest+OHHTTPStubSuiteCleanUp[podhttps://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Você precisa do arquivo LFSTestConfig.plist do Livefyre, que o Livefyre fornece mediante solicitação.

## Documentação do Xcode {#section_arl_b3v_zz}

Você pode navegar na [documentação](https://livefyre.github.com/StreamHub-iOS-SDK/) ou pode criar o destino "Documentação" no seu Xcode (requer que o apedoc esteja instalado) no sistema.

## Exigências {#section_m5l_13v_zz}

As versões do SDK do iOS do StreamHub desde a v0.2.0 exigem o iOS 6.0 ou superior.

## Apêndice (suporte a JSON) {#section_pcd_5hv_zz}

Para aqueles que estão olhando para os internais do SDK do StreamHub-iOS, observe que usamos uma versão modificada do [JSONKit](https://github.com/escherba/JSONKit) como o analisador JSON padrão (em vez de NSJSONSerialization fornecido pela Apple). Tivemos que fazer isso porque o analisador fornecido pela Apple não oferece suporte à decodificação de arquivos JSON que contêm números inteiros ou números de ponto flutuante maiores que os que podem ser representados pelo sistema. Nossa versão modificada do JSONKit trunca números muito grandes para o máximo correspondente do sistema, em vez de lançar uma exceção.
