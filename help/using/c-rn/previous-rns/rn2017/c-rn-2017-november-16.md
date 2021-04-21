---
description: Notas de versão para 16 de novembro de 2017.
title: 16 de novembro de 2017
exl-id: 167b8c7d-f2fb-4735-9681-d349646ec3eb
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 8%

---

# 16 de novembro de 2017{#november}

Notas de versão para 16 de novembro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | AEM, Biblioteca | Correção de um bug que não resultava no retorno de nenhum resultado ao usar a pesquisa de Tag e Classificação na Biblioteca. |
| Bug | Aplicativos | Correção de um problema em que a tag do recurso não era exibida em um único aplicativo de cartão. |
| Bug | Carrossel | Correção de um problema em que o Carrossel não era exibido no Designer. |
| Bug | Comentários | Correção de contagens de comentários imprecisas em aplicativos de comentários. |
| Aprimoramento | Placa de recurso | O aplicativo de placa de recurso tem toda a funcionalidade de comércio ativada. |
| Aprimoramento | Tira | Adicionamos opções de redimensionamento para Filmstrip para que o usuário possa ter mais controle sobre a aparência das imagens no aplicativo. |
| Bug | Threads principais | Correção de mensagens de erro de Hot Threads para torná-las mais seguras. |
| Aprimoramento | Biblioteca | Os clientes podem excluir as Tags inteligentes aplicadas pelo sistema de IA. Depois de excluídas, elas não verão essas tags nos resultados da pesquisa. |
| Bug | Biblioteca | Correção de um problema em que uma imagem não era exibida corretamente após adicioná-la à biblioteca a partir de uma pesquisa social. |
| Bug | Biblioteca | Correção de um problema de lentidão na criação de pastas. |
| Bug | Biblioteca | Agora os usuários podem publicar arquivos .mov em Coleções. |
| Bug | Biblioteca | Imagens com caracteres especiais no título não eram carregadas na biblioteca, isso foi corrigido. |
| Aprimoramento | Biblioteca | Atualizamos nosso algoritmo de Classificação de &quot;relevância&quot; quando um usuário pesquisa por tags inteligentes, de modo que, quando um usuário alterna a classificação de &quot;relevância&quot; na pesquisa da biblioteca, o novo algoritmo de classificação é ativado. Esse novo algoritmo de classificação leva em consideração, pontuações de precisão de tag inteligente, número de estrelas atribuídas por usuário e idade do documento. O objetivo é tornar a experiência de pesquisa de tags mais precisa para o usuário. |
| Aprimoramento | Biblioteca | Quando um cliente salva um ativo na biblioteca, o Livefyre emprega a tecnologia de aprendizado de máquina da Adobe Sensei para adicionar tags que descrevem o que está na imagem do ativo automaticamente. Isso permite que o usuário procure essas tags no sistema. |
| Aprimoramento | Biblioteca | Quando um cliente salva um ativo baseado em imagem na biblioteca, o Livefyre o insere automaticamente em tags usando a tecnologia Adobe AI, extraindo recursos, categorias e propriedades estéticas do sistema. Isso permite que o usuário pesquise a biblioteca pelo que está dentro das imagens, não apenas o texto. |
| Bug | Identidade do Livefyre | Os avatars não eram carregados corretamente para a implementação da identidade LF da Microsoft, isso foi corrigido. |
| Bug | ModQ | Correção de um problema em que a pré-moderação dos fluxos e o ModQ não exibiam todo o conteúdo corretamente. |
| Aprimoramento | Configurações | Os clientes podem visitar nossa política de privacidade e os termos do serviço em um rodapé em Configurações. |
| Aprimoramento | Fluxos | Correção de um erro para pré-moderação de regras de fluxo baseadas em email. |
| Aprimoramento | Fluxos | Adição da capacidade de filtrar o conteúdo do fluxo por idioma. |
| Aprimoramento | Usuários | Adicionada a capacidade de usar arquivos .png para avatares do usuário. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Gerenciador de aplicativos | Correção de um problema com a pesquisa de tag do aplicativo no Gerenciador de aplicativos. |
| Bug | Biblioteca | Correção de um problema que impedia a adição de estrelas para vários conteúdos de cada vez na Biblioteca de ativos. |
| Bug | Studio | Correção de um problema que impedia alguns usuários de fazer logon no Livefyre. |
