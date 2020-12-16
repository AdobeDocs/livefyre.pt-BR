---
description: Notas de versão para a versão de 1º de novembro de 2018.
seo-description: Notas de versão para a versão de 1º de novembro de 2018.
seo-title: 1 de novembro de 2018
solution: Experience Manager
title: 1 de novembro de 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 4%

---


# 1 de novembro de 2018{#november}

Notas de versão para a versão de 1º de novembro de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os novos recursos a seguir foram lançados na versão de produção desta versão:

* Tags inteligentes de vídeo

   Aproveite a tecnologia avançada de visão de computador, capacitada pela Adobe Sensei, para marcar automaticamente o conteúdo de vídeo quando você salvá-lo na Biblioteca. As Tags inteligentes ajudam você a gerenciar o UGC de forma mais eficiente, mas também criam regras de curadoria superprecisas (fluxos) que coletam conteúdo com base no que há no vídeo, não apenas no texto, o que economiza um esforço significativo para moderar conteúdo indesejado.

   Detalhes do recurso:

   * As tags inteligentes são automaticamente adicionadas aos vídeos obtidos de pesquisa social, fluxos e arquivos de vídeo carregados na Biblioteca. Tags de visualização nos detalhes do ativo para um vídeo individual
   * Tags em vídeos nos formatos .MP4, .MOV e AVI
   * Tags em vídeos de até 60 segundos ou 50 MB
   * Duas categorias de tags inteligentes se aplicam a vídeos: recursos (animais, objetos, locais, etc.) e ações (execução, marcha, canto, etc.)

   Para obter mais informações, consulte [Tags inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Limite da taxa do Instagram

   O Instagram alterou o número de solicitações que qualquer empresa que usa a API do Instagram, incluindo o Livefyre, pode fazer de 5.000 solicitações por hora por token para 200 solicitações por hora por token. Isso é conhecido como *limitação de taxa*. Para obter mais informações, consulte [Limitação da taxa do Instagram](/help/using/c-streams/c-instagram-rate-limiting.md).

* Arquivos de áudio na biblioteca

   Agora é possível executar as seguintes funções em arquivos de áudio do painel Biblioteca:

   * Pesquisar
   * Visualizar
   * Importar
   * Filtrar por arquivos de áudio
   * Arrastar e soltar arquivos no designer

## Problemas {#section_ehw_ndt_wcb}

Nenhum problema novo foi resolvido na versão de produção desta versão. Consulte a seção [acima](#c_rn/section_syx_mdt_wcb).

## Versão UAT {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Os problemas nas tabelas a seguir foram resolvidos na versão UAT desta versão.

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | RGPD | Todos os dados atribuídos a antigos clientes no Analytics serão excluídos. |
| Bug | Biblioteca | Correção de um problema em que um vídeo carregado na Biblioteca e exibido em detalhes do ativo não era exibido corretamente. |
| Bug | Mosaico | Correção de um problema em que um mosaico exibia o último conteúdo de um carrossel do Instagram como uma miniatura, em vez de um cartão. |
| Bug | Pesquisa social | Corrigido um problema no qual a pesquisa social do Instagram não funcionava como esperado. |

