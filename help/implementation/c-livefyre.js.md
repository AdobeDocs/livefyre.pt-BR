---
description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.

`Livefyre.js` é a biblioteca principal que você pode instalar em cada página da Web habilitada para o Livefyre. Ela define o objeto global `window.Livefyre` e um único método público, `Livefyre.require`, que pode ser usado para carregar outras bibliotecas JavaScript do Livefyre que ajudam a [incorporar aplicativos do Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Integrar seu provedor de autenticação com Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e muito mais.

## Adicionar ao Site {#section_cst_twg_xz}

Adicione a seguinte tag `<script>` à sua página da Web ou modelo de site. Se possível, adicione-o à seção `<head>` do documento HTML para que ele seja carregado rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Este script incorporará um arquivo muito pequeno (~1 Kb) chamado escopo Livefyre.js que carregará subsequentemente a versão mais recente do Livefyre.js sobre o protocolo com o qual sua página da Web foi acessada (HTTP ou HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` é um carregador de módulo JavaScript personalizado, como  [curl.](https://github.com/cujojs/curl) jor  [RequireJS](https://requirejs.org/). Ele pode ser usado para carregar a maioria dos pacotes publicados pela Livefyre e apresenta um caminho de integração conveniente e intuitivo.

Os pacotes acessíveis por meio de `Livefyre.require` têm versão usando [Controle de versão semântico](https://semver.org/). Os pacotes podem ser necessários em uma versão específica ou em várias versões para que sua página da Web possa se beneficiar automaticamente dos novos recursos de correções de erros. Isso proporciona flexibilidade ao integrar o Livefyre no seu site. Há três níveis de pinos de versão que você pode usar com `Livefyre.require`.

* **package-name#1:** fixar na versão principal v1. Você obterá todas as novas atualizações que mantêm uma API compatível com versões anteriores. Fixar em uma versão principal para receber correções de erros e aprimoramentos de recursos secundários para essa versão.
* **package-name#1.1:** fixar na versão secundária v1.1. Você obterá todos os correções nesta versão secundária. O Livefyre Engineering sempre ignorará a versão secundária de um pacote se o comportamento padrão ou o escopo funcional forem alterados de forma a causar um comportamento novo e inesperado na sua página da Web. Fixar em uma versão secundária se desejar receber correções de erros automatizadas, mas nenhuma funcionalidade adicional ou alterações no comportamento padrão.
* **package-name#1.1.1:** Prender na versão v1.1.1 do patch. O comportamento dessa incorporação nunca será alterado, mesmo se houver correções de erros. Adicione a uma versão de patch se você tiver personalizações CSS extensas para seu site que dependem de uma estrutura de marcação de pacote que pode mudar ou se você tiver outros motivos para preferir que a versão do Livefyre que está sendo executada não será alterada de forma alguma.

Um exemplo de integração usando `Livefyre.require` pode ser semelhante a:

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

Perguntando quais pacotes do Livefyre JavaScript estão disponíveis por meio de `Livefyre.require`? Você sempre pode encontrar uma lista atualizada de pacotes compatíveis e suas versões mais recentes aqui: [packages.html](https://cdn.livefyre.com/packages.html).

## Teste de versões de pré-lançamento de pacotes {#section_pgm_dpg_xz}

Às vezes, você pode testar uma versão futura de um pacote do Livefyre para garantir que ele funcione em seu site ou para aceitar o teste de um recurso que esteja sendo desenvolvido a sua solicitação. Além de incluir um intervalo de versão semântica, o ambiente UAT de pré-lançamento pode ser especificado.

Por exemplo, o seguinte exigiria a versão UAT de `fyre.conv`, os aplicativos Comentários, Blog em tempo real e Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
