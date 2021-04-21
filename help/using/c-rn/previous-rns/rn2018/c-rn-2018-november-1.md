---
description: Notas de versão de 1 de novembro de 2018.
title: 1 de novembro de 2018
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 4%

---

# 1 de novembro de 2018{#november}

Notas de versão de 1 de novembro de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes novos recursos foram lançados na versão de produção desta versão:

* Tags inteligentes de vídeo

   Aproveite a tecnologia avançada de visão de computador, viabilizada pela Adobe Sensei, para marcar automaticamente o conteúdo de vídeo ao salvá-lo na Biblioteca. As Tags inteligentes ajudam você a gerenciar o UGC de forma mais eficaz, mas também criam regras de curadoria superprecisas (fluxos) que coletam conteúdo com base no que está no vídeo, não apenas no texto, evitando esforços significativos de moderação de conteúdo indesejado.

   Detalhes do recurso:

   * As tags inteligentes são adicionadas automaticamente aos vídeos obtidos da pesquisa social, dos fluxos e dos arquivos de vídeo na Biblioteca. Exibir tags nos detalhes do ativo de um vídeo individual
   * Tags de vídeo nos formatos .MP4, .MOV e AVI
   * Tags de vídeos de até 60 segundos ou 50 MB
   * Duas categorias de tags inteligentes se aplicam a vídeos: recursos (animais, objetos, locais, etc.) e ações (correr, andar, cantar, etc.)

   Para obter mais informações, consulte [Tags inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limite da taxa de instagram

   A instagram alterou o número de solicitações que qualquer empresa que use a API do Instagram, incluindo o Livefyre, pode fazer de 5.000 solicitações por hora por token para 200 solicitações por hora por token. Isso é conhecido como *rate limit*. Para obter mais informações, consulte [Limite da Taxa de Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Arquivos de áudio na biblioteca

   Agora é possível executar as seguintes funções em arquivos de áudio do painel Biblioteca:

   * Pesquisar
   * Visualizar
   * Importar
   * Filtrar por arquivos de áudio
   * Arrastar e soltar arquivos no designer

## Problemas {#section_ehw_ndt_wcb}

Nenhum novo problema foi resolvido na versão de produção desta versão. Consulte a seção [acima de](#c_rn/section_syx_mdt_wcb).

## Versão UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Os problemas nas tabelas a seguir foram resolvidos na versão UAT desta versão.

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | RGPD | Todos os dados atribuídos a clientes anteriores no Analytics serão excluídos. |
| Bug | Biblioteca | Correção de um problema em que um vídeo carregado na Biblioteca e visualizado em detalhes do ativo não era exibido corretamente. |
| Bug | Mosaico | Correção de um problema em que o Mosaic exibia a última parte do conteúdo de um carrossel do Instagram como miniatura, em vez de um cartão. |
| Bug | Pesquisa social | Correção de um problema em que a pesquisa social no Instagram não funcionava conforme o esperado. |
