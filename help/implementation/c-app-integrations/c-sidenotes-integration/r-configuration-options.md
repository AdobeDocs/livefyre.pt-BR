---
description: O objeto de configuração Observações é um objeto JSON usado para especificar o conteúdo renderizado pelo aplicativo Livefyre na página.
title: Opções de configuração de observações
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# Opções de configuração de observações {#sidenotes-configuration-options}

O objeto de configuração Observações é um objeto JSON usado para especificar o conteúdo renderizado pelo aplicativo Livefyre na página.

O objeto contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| authDelegate | ** objeto obrigatório | Estilo novo ou antigo de delegação de autenticação inicializada. |
| collectionMeta | ** objeto obrigatório | Consulte collectionMeta token para obter mais informações. |
| customIcon | ** optionalstring | Define o URL de um ícone de iniciador personalizado. O padrão é a bolha do Livefyre. |
| customStyles | ** objeto opcional | Adiciona estilos personalizados para alterar a aparência de Sidenotes. Para obter mais informações, consulte Estilos personalizados. |
| disableStream | ** optionalBoolean | Se true, desabilitará o streaming em tempo real nessa instância do Sidenotes (não em outros fluxos de comentários). O padrão é falso. |
| ambiente | ** optionalstring | Especifica o ambiente UAT do Livefyre. O único valor possível é `t402.livefyre.com`. Para produção, esse parâmetro deve ser removido. |
| iconVisibility | ** objeto opcional ou string | Define se o ícone de Observações será visível ao passar o mouse ou estático. Se essa for uma string, ela será usada para ambas as versões do ícone de bloco (vazio e tem observações). Se um objeto for, você deve especificar cada tipo: {empty: &quot;hover&quot;, num: &#39;static&#39;}. O padrão é estático. |
| inlineThreads | ** optionalbooleano | Se verdadeiro, os threads de identificações são inseridos diretamente após o bloco com o qual estão associados. O padrão é falso. |
| numSidenotesEl | ** opcional, objeto, string ou matriz | Especifica qual elemento o widget de contagem de observações será decorado. (Este widget mostra o número de observações na página e informações sobre as observações). Se o seletor de sequência corresponder a mais de um elemento, o primeiro será escolhido. (Usa especificação do seletor DOM CSS3.) |
| position | ** optionalstring | Determina a posição do pop-up quando um elemento com as observações ativadas é clicado. Os valores possíveis são &quot;inteligente&quot;, &quot;esquerda&quot;, &quot;direita&quot;, &quot;inferior&quot;. O padrão é &quot;inteligente&quot;, que alinha o pop-up à direita da página, a menos que não haja espaço suficiente (nesse caso, ele será movido para abaixo do conteúdo). |
| seletores | ** objeto, string ou matriz necessários | Especifica os elementos nos quais os ícones do iniciador devem aparecer. (Usa especificação do seletor DOM CSS3.) Se o objeto incluir uma seção &quot;inclui&quot; e uma seção &quot;exclui&quot; que aplicará o seletor de CSS a todas as inclusões correspondentes e removerá quaisquer elementos correspondentes às exclusões. Se a string incluir elementos correspondentes na página. Se a matriz listar os elementos a serem incluídos. |
| strings | ** objeto opcional | Adiciona strings de texto personalizadas para alterar qualquer idioma ou texto em todo o aplicativo. Para obter mais informações, consulte Strings personalizadas. |
| threadContainerEl | ** opcional, objeto, string ou matriz | Especifica um elemento no qual o thread de observações será exibido. Esse parâmetro permite reposicionar o thread. Se o seletor de sequência corresponder a mais de um elemento, o primeiro será escolhido. (Usa especificação do seletor DOM CSS3.) |
