---
description: null
seo-description: null
seo-title: Usar o Livefyre com outra ferramenta do Analytics
solution: Experience Manager
title: Usar o Livefyre com outra ferramenta do Analytics
uuid: 26 c 835 f 6-aced -41 f 7-aabe -418 afce 8 a 829
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Usar o Livefyre com outra ferramenta do Analytics{#use-livefyre-with-other-analytics-tool}

Você pode usar as ferramentas de análise para reunir dados sobre interações do usuário com aplicativos do Livefyre. Você pode usar o Adobe Analytics ou uma ferramenta de sua escolha.

Para usar o Livefyre com uma ferramenta de sua escolha (não o Adobe Analytics), siga o procedimento descrito nesta página.

## Etapa 1: Configurar o manipulador de eventos {#section_ngm_gzl_pdb}

Configure um manipulador de eventos nas páginas onde você usa aplicativos do Livefyre. Isso permite coletar dados dos aplicativos na página que você pode usar para análises.

Adicione o Livefyre. js a uma página para configurar o manipulador de eventos. O Livefyre. js carrega de forma assíncrona. Para reduzir o tamanho do arquivo e melhorar o desempenho de carregamento, as análises não estão disponíveis imediatamente. Você deve pesquisar o objeto analytics até que os dados estejam disponíveis. Coloque esse script em qualquer lugar na página ou agrupe-o dentro de seus próprios scripts compilados.

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

Depois que a funcionalidade Livefyre. analytics estiver disponível na página, implemente a função analyticshandler para enviar os eventos recebidos para o provedor de análises de sua escolha.

1. O manipulador de análises recebe uma matriz de eventos que devem ser iterados e enviados individualmente ou como um lote, se o seu provedor o suportar.
1. Mapeie os dados do evento recebidos pelo manipulador para um formato que seu provedor de análise requer.
1. Envie os dados para o seu provedor de análise.

