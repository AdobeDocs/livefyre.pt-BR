---
description: O objeto Sidenotes Config é um objeto JSON usado para especificar o conteúdo
  renderizado pelo aplicativo do Livefyre na página.
seo-description: O objeto Sidenotes Config é um objeto JSON usado para especificar
  o conteúdo renderizado pelo aplicativo do Livefyre na página.
seo-title: Opções de configuração de sidenotes
solution: Experience Manager
title: Opções de configuração de sidenotes
uuid: 067 e 51 e 6-9720-4226-a 805-c 7 a 07 c 8 cdaa 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Opções de configuração de sidenotes{#sidenotes-configuration-options}

O objeto Sidenotes Config é um objeto JSON usado para especificar o conteúdo renderizado pelo aplicativo do Livefyre na página.

O objeto contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| Authdelegate | *required* object | Delegação de autenticação inicializada de estilo novo ou antigo. |
| Collectionmeta | *required* object | Consulte collectionmeta token para obter mais informações. |
| Customicon | *optional* string | Define o URL de um ícone personalizado de inicialização. Padrões para a bolha do Livefyre. |
| Customstyles | *optional* object | Adiciona estilos personalizados para alterar a aparência e o comportamento das Sidenotes. Para obter mais informações, consulte Estilos personalizados. |
| Disablestream | *optional* Boolean | Se verdadeiro, desativa o streaming em tempo real desta instância de Sidenotes (e não em outros fluxos de comentário). O padrão é false. |
| environment | *optional* string | Especifica o ambiente UAT do Livefyre. O único valor possível é `t402.livefyre.com`. Para produção, esse parâmetro deve ser removido. |
| Iconvisibility | *objeto ou* string opcional | Define se o ícone de Sidenotes estará visível ao passar o mouse ou estático. Se essa for uma string, ela será usada para ambas as versões do ícone de bloco (vazia e tem Sidenotes). Se um objeto, você deve especificar cada tipo: {empty: ' passar ', num: ' static '}. O padrão é estático. |
| Inlinethreads | *optional* boolean | Se verdadeiro, os threads de Sidenote são inseridos diretamente depois do bloco com o qual estão associados. O padrão é false. |
| Numsidenotesel | *objeto,* string ou matriz opcional | Especifica qual elemento o widget de contagem de Sidenotes irá decorar. (Esse widget mostra o número de sidriotes na página e informações sobre as Sidenotes.) Se o seletor de string corresponder a mais de um elemento, o primeiro será escolhido. (Usa a spec do seletor DOM CSS 3.) |
| position | *optional* string | Determina a posição do pop-up quando um elemento com Sidenotes ativados é clicado. Os valores possíveis são "inteligente", "left", "right", "bottom". O padrão é'inteligente ', que alinha o pop-up à direita da página, a menos que não haja espaço suficiente (nesse caso, se for movido para baixo do conteúdo). |
| seletores | *objeto,* string ou matriz necessário | Especifica os elementos nos quais os ícones do iniciador devem aparecer. (Usa a spec do seletor DOM CSS 3.) Se o objeto, incluir uma seção «incluir» e uma seção «exclui» que aplique o seletor de CSS para qualquer correspondência incluída, e remova quaisquer elementos que correspondam as exclusões. Se a sequência estiver incluída, incluirá quaisquer elementos correspondentes na página. Se array, lista os elementos a serem incluídos. |
| strings | *optional* object | Adiciona strings de texto personalizadas para alterar qualquer idioma ou texto em todo o aplicativo. Para obter mais informações, consulte Strings personalizadas. |
| Threadcontainerel | *objeto,* string ou matriz opcional | Especifica um elemento no qual a encadeamento de sidriota será exibida. Esse parâmetro permite reposicionar o encadeamento. Se o seletor de string corresponder a mais de um elemento, o primeiro será escolhido. (Usa a spec do seletor DOM CSS 3.) |

