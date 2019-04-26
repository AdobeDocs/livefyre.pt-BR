---
description: Quando você implementa aplicativos do Livefyre, o estilo da implementação
  depende do caso de uso. Esta página explica os recursos das três maneiras de criar
  um aplicativo.
seo-description: Quando você implementa aplicativos do Livefyre, o estilo da implementação
  depende do caso de uso. Esta página explica os recursos das três maneiras de criar
  um aplicativo.
seo-title: Integrações de aplicativos CMS
solution: Experience Manager
title: Integrações de aplicativos CMS
uuid: 14 fd 7 e 36-0 e 50-4 ae 3-97 f 0-2 de 731 c 184 f 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Integrações de aplicativos CMS{#cms-app-integrations}

Quando você implementa aplicativos do Livefyre, o estilo da implementação depende do caso de uso. Esta página explica os recursos das três maneiras de criar um aplicativo.

A integração do Livefyre é agnóstico a qualquer CMS, Perfil do usuário e plataforma de Autenticação. Implemente o Livefyre de uma ou mais formas, dependendo do caso de uso e dos requisitos.

Você pode usar a integração tradicional para criar componentes AEM personalizados.

## Visão geral do tipo de integração do aplicativo CMS

| Tipo | Requisito de desenvolvimento | Recursos | Vantagens | Limitações |
|--- |--- |--- |--- |--- |
| App Designer | Muito baixo | Crie uma JS embutida no Studio para adicionar a páginas sem um estilo <br>e configurações de estilo limitado e </br>configurações disponíveis: Páginas de uso único (cobertura de eventos, campanhas, hubs) | É possível fazer um aplicativo para cima e em execução em pouco tempo. <br>As configurações podem ser feitas por um membro não técnico. <br>Facilitar as alterações nas configurações | Deve criar um aplicativo usando o Livefyre Studio primeiro <br>não automatizado |
| Livefyre. js | Médio | Integrar aplicativos no javascript de suas páginas <br>caso de uso: Modelos reutilizáveis (conteúdo editorial, revisões de produtos) | Usar o conjunto completo de personalizações e configurações do Aplicativo <br>Automatiza o processo para instanciar dinamicamente Aplicativos de dentro de seu CMS em suas páginas | Precisa de um desenvolvedor para frente. |
| Apis do SDK | Avançado | Recupere o conteúdo do Livefyre a ser usado para aplicativos personalizados <br>Personalizar front-end além de ofertas que oferecem suporte <br>para uso: Integrações de dados/análises e aplicativos front-end personalizados | Poder completo sobre a aparência do aplicativo | Requer desenvolvimento para frente. <br>Nível mais alto de esforços desenvolvidos para implementar. |
