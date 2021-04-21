---
description: Adicione o Livefyre ao aplicativo iOS nativo.
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

Adicione o Livefyre ao aplicativo iOS nativo.

Use essa biblioteca de código aberto para integrar serviços do Livefyre ao seu aplicativo iOS nativo. O Livefyre StreamHub iOS SDK fornece uma camada fina em torno de nossos mecanismos comuns de API, com base na excelente biblioteca AFNetworking.

O Livefyre também fornece dois aplicativos de amostra do iOS com base neste SDK: um fluxo de comentários e um aplicativo de amostra de revisões.

## Integração do SDK ao seu projeto como um pod de cacau (recomendado) {#section_qc5_h3v_zz}

A maneira mais conveniente de adicionar o SDK do StreamHub-iOS ao seu projeto é usar o CocoaPods. Se você não tiver o CocoaPods, execute gem install coapods e pod setup (configuração de pod). Veja um exemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Você também precisará adicionar um repositório Specs à sua instalação do CocoaPod (isso irá cloná-lo para o diretório `~/.cocoapods/repos`):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Depois que o Podfile for criado na raiz do projeto do aplicativo e o repositório acima adicionado, execute:

```
pod install
```

Isso baixará todas as dependências e criará um arquivo MyApp.xcworkspace, que deve ser usado a partir de agora para abrir o projeto do aplicativo no Xcode.

## Como um subprojeto Xcode {#section_jcm_g3v_zz}

Como alternativa, clone o repositório:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Em seguida, adicione o projeto Xcode (LFSClient.xcodeproj) ao seu aplicativo como um subprojeto (facilmente, basta arrastar o arquivo LFSClient.xcodeproj para o painel do Navegador de projetos no Xcode).

Você também precisará fazer o mesmo com qualquer uma das dependências ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Baixe tudo de uma vez (não recomendado) {#section_rpb_f3v_zz}

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
>Para executar testes no Xcode 6, você deve adicionar $(PLATFORM_DIR)/Developer/Library/Frameworks a FRAMEWORK_SEARCH_PATHS em Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704).

Você precisa do arquivo LFSTestConfig.plist do Livefyre, que o Livefyre fornece mediante solicitação.

## Documentação do Xcode {#section_arl_b3v_zz}

Você pode navegar pela [documentação](https://livefyre.github.com/StreamHub-iOS-SDK/) ou pode criar o destino &quot;Documentação&quot; no seu Xcode (requer que o appledoc seja instalado) no seu sistema.

## Exigências {#section_m5l_13v_zz}

As versões do SDK do iOS do StreamHub desde a v0.2.0 exigem o iOS 6.0 ou superior.

## Apêndice (suporte a JSON) {#section_pcd_5hv_zz}

Para aqueles que estão olhando para os internais do SDK do StreamHub-iOS, observe que usamos uma versão modificada de [JSONKit](https://github.com/escherba/JSONKit) como o analisador JSON padrão (em vez de NSJSONSerialization fornecido pela Apple). Tivemos que fazer isso porque o analisador fornecido pela Apple não suporta a decodificação de arquivos JSON que contêm números inteiros ou números de ponto flutuante maiores que aqueles que podem ser representados pelo sistema. Nossa versão modificada de JSONKit trunca números muito grandes para o máximo do sistema correspondente, em vez de lançar uma exceção.
