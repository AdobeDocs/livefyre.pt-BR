---
description: Adicione o Livefyre ao seu aplicativo iOS nativo.
seo-description: Adicione o Livefyre ao seu aplicativo iOS nativo.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef 31 a -49 fc -4 b 25-b 0 c 5-300 f 27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Adicione o Livefyre ao seu aplicativo iOS nativo.

Use essa biblioteca de código aberto para integrar os serviços do Livefyre no aplicativo iOS nativo. O SDK do iOS do Livefyre streamhub fornece uma camada fina em torno dos mecanismos comuns de API, com base na excelente biblioteca afnetworking.

O Livefyre também fornece dois Aplicativos de amostra iOS com base neste SDK: Um Fluxo de comentários e um Aplicativo de amostra de Revisão.

## Integração do SDK em seu projeto como um pod de cacau (recomendado) {#section_qc5_h3v_zz}

A maneira mais conveniente de adicionar o streamhub-iOS SDK ao projeto é usar cocoapods. Se não tiver cocoapods, execute os cocoapods de instalação e configuração do pod. Este é um exemplo de Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Você também precisará adicionar um repositório de Specs à instalação cocoapod (isso vai clonar o diretório para `~/.cocoapods/repos` diretório):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Depois que o seu Podarquivo é criado na raiz do projeto do aplicativo e o repositório acima adicionado, execute:

```
pod install
```

Isso fará com que todas as dependências sejam baixadas e crie um arquivo myapp. xcworkspace, que você deve usar a partir de agora para abrir seu projeto do aplicativo no Xcode.

## Como um subprojeto Xcode {#section_jcm_g3v_zz}

Como alternativa, clone o repositório:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Em seguida, adicione o projeto Xcode (lfsclient. xcodeproj) ao aplicativo como um subprojeto (facilmente feito arrastando o arquivo lfsclient. xcodeproj para o painel do Navegador do projeto no Xcode).

Você também precisará fazer o mesmo com qualquer uma das dependências ([afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)).

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
>Para executar testes no Xcode 6, você deve adicionar $ (PLATFORM_ DIR)/Developer/Library/Frameworks para FRAMEWORK_ SEARCH_ PATHS em Pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704).

Você precisa de um arquivo lfstestconfig. plist do Livefyre, fornecido pelo Livefyre mediante solicitação.

## Documentação do Xcode {#section_arl_b3v_zz}

Você pode navegar pela [documentação](https://livefyre.github.com/StreamHub-iOS-SDK/) ou criar o destino «Documentação» no Xcode (requer que o appledoc seja instalado) no sistema.

## Requisitos {#section_m5l_13v_zz}

As versões do SDK do streamhub, desde a v 0.2.0, exigem o iOS 6.0 ou superior.

## Apêndice (suporte ao JSON) {#section_pcd_5hv_zz}

Para aqueles que estão olhando para os integrais do SDK do streamhub, observe que usamos uma versão modificada de [jsonkit](https://github.com/escherba/JSONKit) como o analisador JSON padrão (em vez de nsjsonserialization fornecido pela Apple). Precisamos fazer isso porque o analisador fornecido pela Apple não oferece suporte para decodificação de arquivos JSON que contêm números inteiros ou números de ponto flutuante maiores que aqueles que podem ser representados pelo sistema. Nossa versão modificada do jsonkit truncará números muito grandes para o máximo do sistema, em vez de lançar uma exceção.
