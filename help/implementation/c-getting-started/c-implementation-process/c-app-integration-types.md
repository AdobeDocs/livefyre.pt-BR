---
description: Quando você implementa aplicativos Livefyre, o estilo de implementação depende do caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.
seo-description: Quando você implementa aplicativos Livefyre, o estilo de implementação depende do caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.
seo-title: Integrações de aplicativos CMS
solution: Experience Manager
title: Integrações de aplicativos CMS
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# Integrações de aplicativos CMS{#cms-app-integrations}

Quando você implementa aplicativos Livefyre, o estilo de implementação depende do caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.

A integração do Livefyre é agnóstica a qualquer plataforma CMS, Perfil do usuário e Auth. Implemente o Livefyre de uma ou mais formas, dependendo do caso de uso e dos requisitos.

Você pode usar a integração tradicional para criar componentes personalizados AEM.

## Visão geral do tipo de integração do aplicativo CMS

| Tipo | Requisito de desenvolvimento | Recursos | Pontos positivos | Limitações |
|--- |--- |--- |--- |--- |
| App Designer | Muito Baixo | Crie incorporações JS no Studio para adicionar a páginas sem um desenvolvedor <br>Estilo e configurações limitados disponíveis </br>Caso de uso: Páginas de uso único (cobertura do evento, campanhas, hubs) | Capaz de ativar e executar um aplicativo em um curto período de tempo. <br>As configurações podem ser feitas por um membro não técnico. <br>Alterações rápidas nas configurações | É necessário criar um aplicativo usando o Livefyre Studio primeiro <br>Não automatizado |
| Livefyre.js | Médio | Integre aplicativos ao JavaScript de suas páginas <br>Caso de uso: Modelos reutilizáveis (conteúdo editorial, revisões de produtos) | Usar o conjunto completo de configurações e personalizações do aplicativo <br>Automatiza o processo para instanciar dinamicamente aplicativos de dentro do CMS em suas páginas | Preciso de um desenvolvedor na frente. |
| APIs SDK | Advanced | Recupere seu conteúdo do Livefyre para usar em aplicativos personalizados <br>Personalize o front-end além da oferta suportada <br>Caso de uso: Integrações de dados/análises e aplicativos front-end personalizados | Poder total sobre a aparência do aplicativo | Requer desenvolvimento à frente. <br>Nível mais alto de esforço de desenvolvimento para implementar. |
