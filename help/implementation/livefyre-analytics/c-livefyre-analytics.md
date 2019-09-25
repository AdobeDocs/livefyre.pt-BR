---
description: 'null'
seo-description: 'null'
seo-title: Usar o Livefyre com outra ferramenta do Analytics
solution: Experience Manager
title: Usar o Livefyre com outra ferramenta do Analytics
uuid: 26c835f6-aced-41f7-abe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Usar o Livefyre com outra ferramenta do Analytics{#use-livefyre-with-other-analytics-tool}

Você pode usar as ferramentas de análise para coletar dados sobre interações do usuário com aplicativos Livefyre. Você pode usar o Adobe Analytics ou uma ferramenta de sua escolha.

Para usar o Livefyre com uma ferramenta de sua escolha (não o Adobe Analytics), siga o procedimento descrito nesta página.

## Etapa 1: Configurar manipulador de eventos {#section_ngm_gzl_pdb}

Configure um manipulador de eventos nas páginas em que você usa aplicativos Livefyre. Isso permite coletar dados dos Aplicativos nessa página que você pode usar para análise.

Adicione Livefyre.js a uma página para configurar o manipulador de eventos. Livefyre.js é carregado de forma assíncrona. Para reduzir o tamanho do arquivo e melhorar o desempenho da carga, as análises não estão disponíveis imediatamente. Você deve pesquisar o objeto analytics até que os dados estejam disponíveis. Coloque esse script em qualquer lugar na página ou agrupe-o em seus próprios scripts compilados.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Etapa 2: Implementar função de manipulador

Quando a funcionalidade Livefyre.analytics estiver disponível na página, implemente a função analyticsHandler para enviar os eventos recebidos ao provedor de análises de sua escolha.

1. O manipulador do Analytics recebe uma matriz de eventos que devem ser repetidos e enviados individualmente ou em lote, se o provedor suportar.
1. Mapeie os dados de eventos recebidos pelo manipulador para um formato que seu provedor de análises exija.
1. Envie os dados para o provedor de análises.

