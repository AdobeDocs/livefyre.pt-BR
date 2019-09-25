---
description: Analise a atividade de usuário, conteúdo e moderador do site.
seo-description: Analise a atividade de usuário, conteúdo e moderador do site.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

Analise a atividade de usuário, conteúdo e moderador do site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analise a atividade de usuário, conteúdo e moderador do site.

O Livefyre Analytics fornece acesso aos dados de sua rede em painéis fáceis de ler para Conversações, Moderação e dados do usuário. Use esses painéis para monitorar a atividade e executar análises rápidas em seu site.

Os painéis podem ser filtrados por site, data e atividade. Use o menu suspenso Rede na parte superior esquerda da janela para selecionar um site a ser exibido. Depois de gerado, clique no cabeçalho de uma coluna para classificar ou passe o mouse sobre o gráfico para obter informações mais específicas sobre qualquer ponto de dados.

Esta página descreve:

* Selecionar um intervalo de [datas](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) para seu painel
* [Mostrando / Ocultando Atividades Disponíveis](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Exportar dados do painel](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [O painel Coleções](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [O painel Moderação](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [O painel Usuários](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Atualmente, o Analytics suporta atividades originadas dos aplicativos e moderação principais do Livefyre. A maioria das atividades incluídas nesses painéis também está disponível por meio dos eventos [JavaScript do](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)Livefyre, que podem ser usados para potencializar sua própria ferramenta de análise personalizada ou de terceiros.

## Intervalo de datas {#concept_798C438120E643B6BE262C9997DC87C4}

Clique no menu suspenso de datas para selecionar um intervalo a ser exibido. Use as datas rápidas ou selecione uma data inicial e final nos calendários fornecidos.

![](assets/analytics-date-range.png)

Datas rápidas:

* **** Hoje: Exibe dados da meia-noite na manhã do dia atual, até a última hora completa antes deste momento.
* **** Ontem: Exibe os dados das 24 horas anteriores.
* **** 7 dias: Exibe os dados dos 7 dias anteriores, não incluindo hoje.
* **** 30 dias: Exibe os dados dos 30 dias anteriores, não incluindo hoje.
* **** Esta semana: Exibe dados da meia-noite da manhã do último domingo, até a última hora completa antes desse momento.
* **** Este mês: Exibe dados da meia-noite na manhã do primeiro dia do mês atual, até a última hora completa antes deste momento.
* **** Semana passada: Exibe os dados da semana passada.
* **** Mês passado: Exibe os dados do mês passado.

## Mostrando/Ocultando Atividades {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

As atividades são ações que os usuários executam em seu site, incluindo comentários, sinalização, compartilhamento e moderação. Use o menu suspenso **Mostrar/ocultar atividades** para selecionar as atividades que deseja incluir no painel.

>[!NOTE]
>
>Selecionar novos eventos para o filtro renderizará novamente a página sem alterar o URL.

![](assets/analytics-show-hide-activities.png)

As atividades disponíveis variam por tipo de painel e exportação, e podem incluir:

* **** Publicações: Exibe dados da meia-noite na manhã do dia atual, até a última hora completa antes deste momento.
* **** Respostas: Exibe os dados das 24 horas anteriores.
* **** Curtidas: Exibe os dados dos 7 dias anteriores, não incluindo hoje.
* **** Descurtidas: Exibe os dados dos 30 dias anteriores, não incluindo hoje.
* **** Contém mídia: Exibe dados da meia-noite da manhã do último domingo, até a última hora completa antes desse momento.
* **** A publicação tem upload de fotos: Exibe dados da meia-noite na manhã do primeiro dia do mês atual, até a última hora completa antes deste momento.
* **** A postagem tem um link: Exibe os dados da semana passada.
* **** A postagem tem @menções: Exibe os dados do mês passado.
* **** Aprovado: Exibe os dados do mês passado.
* **** Bozo'd: Exibe os dados do mês passado.
* **** Tracejado: Exibe os dados do mês passado.
* **** Moderação total: Exibe os dados do mês passado.

## Exportar dados do painel {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Use o menu suspenso **Exportar** para exportar os dados do painel como um arquivo CSV.

* Resumo diário (somente coleções): exporta os últimos talentos diários da semana completa para cada coleção.
* Dados da tabela: exporta todos os dados de coleções acumuladas (todas as colunas e todas as linhas no relatório atual).
* Dados brutos: exporta todos os eventos individuais usados para criar o relatório de rollup atual.

>[!NOTE]
>
>Esses relatórios podem levar alguns minutos para serem exportados. Todos os carimbos de data e hora são do horário Unix.

## Coleções {#concept_228D8E5553784DB8BABF3819A5FF0345}

O painel Coleções lista a atividade do usuário por Coleção, permitindo que você determine seu conteúdo mais envolvente (e menos). Cada coleção listada inclui um link para a página na qual pode ser encontrada.

![](assets/analytics-collections.png)

## Moderação {#concept_98689B1E804B43CEA21E3F456107CCD9}

O painel Moderação lista eventos por moderador, permitindo que você avalie suas atividades. Use este relatório para encontrar seus Moderadores mais ativos e suas ações de moderação mais comuns.

>[!NOTE]
>
>As atividades de moderação automatizadas do Livefyre serão listadas para o nome de moderador Livefyre System.

![](assets/analytics-moderation.png)

## Usuários {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

O painel Usuários mostra a atividade do site por usuário, permitindo que você analise como usuários individuais estão interagindo com o site. Use este painel para localizar seus usuários mais ativos em todo o site e avaliar as atividades mais populares do site.

![](assets/analytics-users.png)

