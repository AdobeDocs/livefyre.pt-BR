---
description: Notas de versão para a versão de 16 de novembro de 2017.
seo-description: Notas de versão para a versão de 16 de novembro de 2017.
seo-title: 16 de novembro de 2017
solution: Experience Manager
title: 16 de novembro de 2017
uuid: e7d09640-d2c1-4d23-8fa6-ecc90d0b2daa
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 8%

---


# 16 de novembro de 2017{#november}

Notas de versão para a versão de 16 de novembro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | AEM, Biblioteca | Correção de um erro que não gerava resultados ao usar a pesquisa Tag e Classificação na Biblioteca. |
| Bug | Aplicativos | Correção de um problema em que a tag de recurso não era exibida em um único aplicativo de cartão. |
| Bug | Carrossel | Corrigido um problema no qual o Carousel não era exibido no Designer. |
| Bug | Comentários | Correção de contagens de comentários imprecisas em aplicativos de comentários. |
| Aprimoramento | Placa de recurso | O aplicativo Feature Card tem toda a funcionalidade de comércio ativada. |
| Aprimoramento | Película fotográfica | Adicionamos opções de redimensionamento para Película fotográfica para que o usuário possa ter mais controle sobre a aparência das imagens no aplicativo. |
| Bug | Threads instantâneos | Correção de mensagens de erro de Threads ativos para torná-las mais seguras. |
| Aprimoramento | Biblioteca | Os clientes têm a capacidade de excluir as Tags inteligentes aplicadas pelo sistema do AI. Uma vez excluídas, elas não verão essas tags nos resultados da pesquisa. |
| Bug | Biblioteca | Correção de um problema em que uma imagem não era exibida corretamente após adicioná-la à biblioteca a partir de uma pesquisa social. |
| Bug | Biblioteca | Correção de um problema com a lentidão da criação de pastas. |
| Bug | Biblioteca | Os usuários agora podem publicar arquivos .mov em Coleções. |
| Bug | Biblioteca | Imagens com caracteres especiais no título não eram carregadas na biblioteca, isso foi corrigido. |
| Aprimoramento | Biblioteca | Atualizamos nosso algoritmo de classificação de &quot;relevância&quot; quando um usuário pesquisa por tags inteligentes, então quando um usuário alterna a classificação de &quot;relevância&quot; na pesquisa de biblioteca, o novo algoritmo de classificação é ativado. Esse novo algoritmo de classificação leva em consideração, pontuações de precisão de tag inteligente, número de estrelas atribuídas pelo usuário e idade do documento. O objetivo é tornar a experiência de pesquisa de tags mais precisa para o usuário. |
| Aprimoramento | Biblioteca | Quando um cliente salva um ativo na biblioteca, o Livefyre emprega a tecnologia de aprendizado de máquina da Adobe Sensei para adicionar tags que descrevem o que está na imagem do ativo automaticamente. Isso permite que o usuário procure essas tags no sistema. |
| Aprimoramento | Biblioteca | Quando um cliente salva um ativo baseado em imagem na biblioteca, o Livefyre o coloca automaticamente em tag usando a tecnologia Adobe AI, extraindo recursos, categorias e propriedades estéticas do sistema. Isso permite que o usuário pesquise a biblioteca pelo que está dentro das imagens, não apenas pelo texto. |
| Bug | Identidade do Livefyre | Os avatars não estavam sendo carregados corretamente para a implementação da identidade LF da Microsoft, isso foi corrigido. |
| Bug | ModQ | Correção de um problema em que a pré-moderação de fluxos e o ModQ não exibiam todo o conteúdo corretamente. |
| Aprimoramento | Configurações | Os clientes agora podem visitar nossa política de privacidade e os termos do serviço em um rodapé em Configurações. |
| Aprimoramento | Fluxos | Correção de um erro na pré-moderação de regras de fluxo baseadas em email. |
| Aprimoramento | Fluxos | Adicionada a capacidade de filtrar o conteúdo de fluxo por idioma. |
| Aprimoramento | Usuários | Adicionada a capacidade de usar arquivos .png para avatars do usuário. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Gerenciador de aplicativos | Correção de um problema com a pesquisa de tags do aplicativo no App Manager. |
| Bug | Biblioteca | Correção de um problema que impedia a adição de estrelas para vários conteúdos de cada vez na Biblioteca de ativos. |
| Bug | Studio | Corrigido um problema que impedia que alguns usuários fizessem logon no Livefyre. |

