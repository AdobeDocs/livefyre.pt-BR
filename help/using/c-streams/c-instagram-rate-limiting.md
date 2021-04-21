---
description: A instagram alterou o número de solicitações que qualquer empresa que use a API do Instagram, incluindo o Livefyre, pode fazer de 5.000 solicitações por hora por token para 200 solicitações por hora por token. Isso é conhecido como limitação de taxa.
title: Limite da taxa de instagram
exl-id: b13db09b-fb5a-4711-a566-d0976172e35e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Solução de problemas: Limites no conteúdo do Instagram {#instagram-rate-limiting}

A instagram alterou o número de solicitações que qualquer empresa que use a API do Instagram, incluindo o Livefyre, pode fazer de 5.000 solicitações por hora por token para 200 solicitações por hora por token. Isso é conhecido como *rate limit*.

Um token é igual a uma conta do Instagram.

Você pode encontrar um erro que limita sua capacidade de pesquisar ou obter conteúdo do Instagram porque:

* Estão usando uma conta para mais de um fluxo
* Ter um grande número de fluxos do Instagram
* Pode estar usando hashtags de alto volume (por exemplo, `#cats` ou `#beach`)

Para reduzir o impacto da limitação da taxa de Instagram:

* Conecte várias contas do Instagram à sua rede. Para obter informações sobre como adicionar contas Instagram em sua rede, consulte [Sobre contas Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)
Desative os fluxos Instagram que você não está usando
Certifique-se de que os fluxos sejam direcionados com as palavras-chave certas e use os filtros de Tag inteligente para tornar as consultas mais precisas. Para obter informações sobre como usar filtros de tags inteligentes, consulte [Tags inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md)
Minimize o tempo em que várias pessoas estão usando a mesma conta do Instagram em uma rede para preparar o conteúdo do Instagram.
