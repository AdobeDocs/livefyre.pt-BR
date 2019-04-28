---
description: A biblioteca principal do Livefyre usada para potencializar o Livefyre em seu site.
seo-description: A biblioteca principal do Livefyre usada para potencializar o Livefyre em seu site.
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

A biblioteca principal do Livefyre usada para potencializar o Livefyre em seu site.

`Livefyre.js` é a biblioteca principal que você pode instalar em todas as páginas da Web ativadas pelo Livefyre. Ele define o objeto global `window.Livefyre` e um único método público, `Livefyre.require`que pode ser usado para carregar outras bibliotecas javascript do Livefyre que ajudam com [a incorporação de aplicativos Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [a integração do provedor de autenticação com o Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) e muito mais.

## Adicionar ao site {#section_cst_twg_xz}

Adicione `<script>` a seguinte tag à página da Web ou ao modelo do site. Se possível, adicione-o à `<head>` seção do documento HTML para que ele carregue rapidamente.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Esse script incorporará um arquivo muito pequeno (~ 1 Kb) chamado do scout Livefyre. js que carregará subsequentemente a versão mais recente do Livefyre. js sobre o protocolo com o qual sua página da Web foi acessada (HTTP ou HTTPS).

## Livefyre. requer {#section_ipq_hwg_xz}

`Livefyre.require` é um carregador de módulo javascript personalizado como [curl. js](https://github.com/cujojs/curl) ou [requirejs](https://requirejs.org/). Ele pode ser usado para carregar a maioria dos pacotes publicados pelo Livefyre e apresenta um caminho de integração conveniente e intuitivo.

Os pacotes acessíveis são `Livefyre.require` organizados por meio de controle de versão [Semantic versão](https://semver.org/). Os pacotes podem ser necessários em uma versão específica ou em um intervalo de versões para que sua página da Web possa se beneficiar automaticamente com novos recursos de bugs. Isso proporciona flexibilidade ao integrar o Livefyre ao seu site. Há três níveis de fixação que podem ser usados `Livefyre.require`.

* **package-name # 1:** Fixar a versão principal v 1. Você receberá todas as novas atualizações que mantenham uma API compatível com versões anteriores. Fixar a uma versão importante para receber correções de erros e pequenas melhorias de recursos para essa versão.
* **package-name # 1.1:** Fixar a versão menor v 1.1. Você obterá todos os erros nesta pequena versão. A engenharia do Livefyre sempre mapeará a versão secundária de um pacote se seu comportamento padrão ou escopo funcional mudar de uma forma que possa causar um comportamento novo e inesperado na sua página da Web. Fixar a uma versão menor se desejar receber correções de erros automatizadas, mas nenhuma funcionalidade adicional ou alterações no comportamento padrão.
* **package-name # 1.1.1:** Fixar à versão de correção v 1.1.1. O comportamento dessa incorporação nunca mudará, mesmo se houver erros. Fixar a uma versão de correção se tiver várias personalizações de CSS para o site que dependem da estrutura de marcação de um pacote que pode ser alterada, ou se você tiver outros motivos para preferir que a versão do Livefyre que você está executando não mudará de forma alguma.

Um exemplo de integração com o exemplo `Livefyre.require` seria:

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

Perguntando quais pacotes Javascript do Livefyre estão disponíveis `Livefyre.require`? Você sempre pode encontrar uma lista atualizada dos pacotes suportados e suas versões mais recentes aqui: [packages.html](https://cdn.livefyre.com/packages.html).

## Teste das versões de pré-lançamento dos pacotes {#section_pgm_dpg_xz}

Às vezes, você pode testar uma versão futura de um pacote do Livefyre para verificar se funcionará em seu site ou para aceitar um recurso que está sendo desenvolvido em sua solicitação. Além de incluir um intervalo de Versão Semântica, o ambiente de pré-lançamento do UAT pode ser especificado.

Por exemplo, o a seguir exigiria a versão UAT dos `fyre.conv`aplicativos de Comentários, Blogs ao vivo e Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
