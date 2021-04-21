---
title: Usar o Livefyre com outra ferramenta do Analytics
description: Usar o Livefyre com outra ferramenta do Analytics
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Usar o Livefyre com outra ferramenta do Analytics{#use-livefyre-with-other-analytics-tool}

Você pode usar as ferramentas de análise para coletar dados sobre as interações do usuário com os aplicativos do Livefyre. Você pode usar o Adobe Analytics ou uma ferramenta de sua escolha.

Para usar o Livefyre com uma ferramenta de sua escolha (não a Adobe Analytics), siga o procedimento descrito nesta página.

## Etapa 1: Configurar o manipulador de eventos {#section_ngm_gzl_pdb}

Configure um manipulador de eventos nas páginas em que você usa os aplicativos do Livefyre. Isso permite coletar dados dos aplicativos nessa página que você pode usar para o Analytics.

Adicione Livefyre.js a uma página para configurar o manipulador de eventos. O Livefyre.js é carregado de forma assíncrona. Para reduzir o tamanho do arquivo e melhorar o desempenho da carga, as análises não estão disponíveis imediatamente. Você deve pesquisar o objeto do analytics até que os dados estejam disponíveis. Coloque esse script em qualquer lugar na página ou agrupá-lo em seus próprios scripts compilados.

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

## Etapa 2: Implementar a função do manipulador

Quando a funcionalidade Livefyre.analytics estiver disponível na página, implemente a função analyticsHandler para enviar os eventos recebidos ao provedor de análises de sua escolha.

1. O manipulador de análise recebe uma matriz de eventos que devem ser repetidos e enviados individualmente ou em lote, se o provedor oferecer suporte a isso.
1. Mapeie os dados do evento recebidos pelo manipulador para um formato exigido pelo provedor de análises.
1. Envie os dados para seu provedor de análises.
