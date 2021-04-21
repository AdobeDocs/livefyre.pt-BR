---
description: Ao implementar os aplicativos Livefyre, o estilo de implementação depende do seu caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.
title: Integrações de aplicativos CMS
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# Integrações de aplicativos CMS{#cms-app-integrations}

Ao implementar os aplicativos Livefyre, o estilo de implementação depende do seu caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.

A integração do Livefyre é independente de qualquer plataforma de CMS e Perfil de usuário e Auth. Implemente o Livefyre de uma ou mais formas, dependendo do caso de uso e das necessidades.

Você pode usar a integração tradicional para criar componentes personalizados de AEM.

## Visão geral do tipo de integração de aplicativo CMS

| Tipo | Requisito de desenvolvimento | Recursos | Pontos positivos | Limitações |
|--- |--- |--- |--- |--- |
| App Designer | Muito baixa | Crie incorporações JS no Studio para adicionar a páginas sem um desenvolvedor <br>Estilo limitado e Configurações disponíveis </br>Caso de uso: Páginas de uso único (cobertura do evento, campanhas, hubs) | Capaz de ativar e executar um aplicativo em um curto período de tempo. <br>As configurações podem ser feitas por um membro não técnico. <br>Alterações fáceis em tempo real em configurações | Deve criar um aplicativo usando o Livefyre Studio primeiro <br>Não automatizado |
| Livefyre.js | Médio | Integre aplicativos no JavaScript de suas páginas <br>Caso de uso: Modelos reutilizáveis (conteúdo editorial, revisões de produtos) | Usar o conjunto completo de personalizações e configurações do aplicativo <br>Automatiza o processo para instanciar dinamicamente os aplicativos de dentro do CMS em suas páginas | Precisa de um desenvolvedor na frente. |
| APIs do SDK | Advanced | Recupere seu conteúdo do Livefyre para usar em aplicativos personalizados <br>Personalize o front-end além da oferta suportada <br>Caso de uso: Integrações do Data/Analytics e aplicativos front-end personalizados | Poder total sobre a aparência do aplicativo | Requer desenvolvimento à frente. <br>Maior nível de esforço de desenvolvimento para implementar. |
