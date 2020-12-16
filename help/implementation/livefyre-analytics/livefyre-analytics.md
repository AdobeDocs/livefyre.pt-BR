---
description: Analise a atividade de usuário, conteúdo e moderador do site.
seo-description: Analise a atividade de usuário, conteúdo e moderador do site.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Analytics{#analytics}

Analise a atividade de usuário, conteúdo e moderador do site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analise a atividade de usuário, conteúdo e moderador do site.

O Livefyre Analytics fornece acesso aos dados de sua rede em painéis fáceis de ler para Conversações, Moderação e dados do usuário. Use esses painéis para monitorar a atividade e executar análises rápidas em seu site.

Os painéis podem ser filtrados por site, data e atividade. Use o menu suspenso Rede na parte superior esquerda da janela para selecionar um site a ser exibido. Depois de gerado, clique no cabeçalho de uma coluna para classificar ou passe o mouse sobre o gráfico para obter informações mais específicas sobre qualquer ponto de dados.

Esta página descreve:

* Selecionar um [Intervalo de datas](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) para o seu painel
* [Mostrando / Ocultando Atividades disponíveis](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Exportação de dados de Painel](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [O Painel Coleções](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [O Painel de moderação](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [O Painel Usuários](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Atualmente, o Analytics suporta atividades originárias dos aplicativos e da moderação do Livefyre Core. A maioria das atividades incluídas nesses painéis também está disponível por meio de [Eventos JavaScript Livefyre](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/), que podem ser usados para potencializar sua própria ferramenta de análise personalizada ou de terceiros.

## Intervalo de datas {#concept_798C438120E643B6BE262C9997DC87C4}

Clique no menu suspenso de datas para selecionar um intervalo a ser exibido. Use as datas rápidas ou selecione um start e uma data final nos calendários fornecidos.

![](assets/analytics-date-range.png)

Datas rápidas:

* **Hoje:** exibe dados da meia-noite na manhã do dia atual, até a última hora completa antes deste momento.
* **Ontem:** exibe os dados das 24 horas anteriores.
* **7 dias:** exibe os dados dos 7 dias anteriores, não incluindo hoje.
* **30 dias:** exibe os dados dos 30 dias anteriores, não incluindo hoje.
* **Esta semana:** exibe dados da meia-noite na manhã do último domingo, até a última hora completa antes deste momento.
* **Este mês:** exibe dados da meia-noite na manhã do primeiro dia do mês atual, até a última hora completa antes deste momento.
* **Semana passada:** exibe os dados da semana passada.
* **Mês passado:** exibe os dados do mês passado.

## Mostrando/Ocultando Atividades {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Atividades são ações que os usuários executam em seu site, incluindo comentários, sinalização, compartilhamento e moderação. Use o menu suspenso **Mostrar/Ocultar Atividades** para selecionar atividades que você deseja incluir no painel.

>[!NOTE]
>
>Selecionar novos eventos para o filtro renderizará novamente a página sem alterar o URL.

![](assets/analytics-show-hide-activities.png)

As atividades disponíveis variam de acordo com o tipo de painel e a exportação, podendo incluir:

* **Postagens:** Exibe dados da meia-noite na manhã do dia atual, até a última hora completa antes desse momento.
* **Respostas:** Exibe os dados das 24 horas anteriores.
* **Curtir:** exibe os dados dos 7 dias anteriores, não incluindo hoje.
* **Descurtidas:** exibe os dados dos últimos 30 dias, não incluindo hoje.
* **Contém mídia:** exibe dados da meia-noite na manhã do último domingo, até a última hora completa antes deste momento.
* **Post tem upload de foto:** exibe dados da meia-noite na manhã do primeiro dia do mês atual, até a última hora completa antes deste momento.
* **A postagem tem um link:** exibe os dados da semana passada.
* **Postagem tem @menções:** Exibe os dados do mês passado.
* **Aprovado:** Exibe os dados do mês passado.
* **Bozo&#39;d:** Exibe os dados do mês passado.
* **Tracejado:** Exibe os dados do mês passado.
* **Total de moderação:** exibe os dados do mês passado.

## Exportando dados de Painel {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Use o menu suspenso **Exportar** para exportar seus dados de painel como um arquivo CSV.

* Resumo diário (somente coleções): exporta os últimos talentos diários da semana completa para cada coleção.
* Dados da tabela: exporta todos os dados de coleções acumuladas (todas as colunas e todas as linhas no relatório atual).
* Dados brutos: exporta todos os eventos individuais usados para criar o relatório acumulado atual.

>[!NOTE]
>
>Esses relatórios podem levar alguns minutos para serem exportados. Todos os carimbos de data e hora são do horário Unix.

## Coleções {#concept_228D8E5553784DB8BABF3819A5FF0345}

A atividade de usuários do Collections painel por coleção permite que você determine o conteúdo mais envolvente (e o menos). Cada coleção listada inclui um link para a página na qual pode ser encontrada.

![](assets/analytics-collections.png)

## Moderação {#concept_98689B1E804B43CEA21E3F456107CCD9}

O painel de Moderação lista eventos por moderador, permitindo que você avalie a atividade deles. Use este relatório para encontrar seus Moderadores mais ativos e suas ações de moderação mais comuns.

>[!NOTE]
>
>As atividades de moderação automatizadas do Livefyre serão listadas para o nome de moderador Livefyre System.

![](assets/analytics-moderation.png)

## Usuários {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

O painel Usuários mostra a atividade do site por usuário, permitindo que você analise como usuários individuais estão interagindo com o site. Use este painel para localizar seus usuários mais ativos em todo o site e avaliar as atividades mais populares do site.

![](assets/analytics-users.png)

