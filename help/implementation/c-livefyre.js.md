---
description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
seo-description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.

`Livefyre.js` é a biblioteca principal que você pode instalar em cada página da Web ativada pelo Livefyre. Ele define o `window.Livefyre` objeto global e um único método público, `Livefyre.require`que pode ser usado para carregar outras bibliotecas do Livefyre JavaScript que ajudam a [incorporar aplicativos](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)Livefyre, [integrar seu provedor de autenticação ao Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e muito mais.

## Adicionar ao site {#section_cst_twg_xz}

Adicione a seguinte `<script>` tag à sua página da Web ou modelo de site. Se possível, adicione-o à `<head>` seção do documento HTML para que seja carregado rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Este script incorporará um arquivo muito pequeno (~1 Kb) chamado escopo Livefyre.js que carregará subsequentemente a versão mais recente do Livefyre.js sobre o protocolo com o qual sua página da Web foi acessada (HTTP ou HTTPS).

## Livefyre.requirements {#section_ipq_hwg_xz}

`Livefyre.require` é um carregador de módulo JavaScript personalizado, como [curl.js](https://github.com/cujojs/curl) ou [RequireJS](https://requirejs.org/). Ele pode ser usado para carregar a maioria dos pacotes publicados pelo Livefyre e apresenta um caminho de integração conveniente e intuitivo.

Os pacotes acessíveis por meio `Livefyre.require` são controle de versão usando o controle de versão [semântico](https://semver.org/). Os pacotes podem ser necessários em uma versão específica ou em várias versões para que sua página da Web possa se beneficiar automaticamente dos novos recursos de correções de erros. Isso proporciona flexibilidade ao integrar o Livefyre no seu site. Existem três níveis de pinning de versão que você pode usar com `Livefyre.require`.

* **** package-name#1: Fixar na versão principal v1. Você obterá todas as novas atualizações que mantêm uma API compatível com versões anteriores. Fixar em uma versão principal para receber correções de erros e aprimoramentos de recursos secundários para essa versão.
* **** package-name#1.1: Fixar na versão secundária v1.1. Você obterá todos os erros nesta versão secundária. O Livefyre Engineering sempre pulará a versão secundária de um pacote se seu comportamento padrão ou escopo funcional forem alterados de uma forma que possa causar um comportamento novo e inesperado na sua página da Web. Faça o ping em uma versão secundária se desejar receber correções automáticas de erros, mas nenhuma funcionalidade adicional ou alterações no comportamento padrão.
* **** package-name#1.1.1: Fixar na versão v1.1.1 do patch. O comportamento dessa incorporação nunca mudará, mesmo que haja erros. Faça o ping em uma versão de patch se você tiver personalizações CSS extensas para seu site que dependem da estrutura de marcação de um pacote que pode mudar ou se você tiver outros motivos para preferir que a versão do Livefyre que você está executando não seja alterada de forma alguma.

Um exemplo de integração que usa `Livefyre.require` pode ser semelhante a:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Pacotes disponíveis {#section_ygd_dwg_xz}

Por meio de quais pacotes Livefyre JavaScript estão disponíveis? `Livefyre.require` Você sempre pode encontrar uma lista atualizada dos pacotes suportados e suas versões mais recentes aqui: [packages.html](https://cdn.livefyre.com/packages.html).

## Testando versões de pré-lançamento de pacotes {#section_pgm_dpg_xz}

Às vezes, você pode testar uma versão futura de um pacote do Livefyre para verificar se ele funcionará em seu site ou para aceitar o teste de um recurso que está sendo desenvolvido a seu pedido. Além de incluir um intervalo de versões semânticas, o ambiente UAT de pré-lançamento pode ser especificado.

Por exemplo, o seguinte exigiria a versão UAT de aplicativos, Comentários, Blog ao vivo e Bate-papo. `fyre.conv`

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
