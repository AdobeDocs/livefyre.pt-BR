---
description: O objeto de configuração Sidenotes é um objeto JSON usado para especificar o conteúdo que o aplicativo Livefyre renderiza na página.
seo-description: O objeto de configuração Sidenotes é um objeto JSON usado para especificar o conteúdo que o aplicativo Livefyre renderiza na página.
seo-title: Opções de configuração do Sidenotes
solution: Experience Manager
title: Opções de configuração do Sidenotes
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Opções de configuração do Sidenotes{#sidenotes-configuration-options}

O objeto de configuração Sidenotes é um objeto JSON usado para especificar o conteúdo que o aplicativo Livefyre renderiza na página.

O objeto contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| authDelegate | *objeto obrigatório* | Delegação de autenticação inicializada de estilo novo ou antigo. |
| collectionMeta | *objeto obrigatório* | Consulte collectionMeta token para obter mais informações. |
| customIcon | *cadeia opcional* | Define o URL de um ícone de iniciador personalizado. O padrão é a bolha do Livefyre. |
| customStyles | *objeto opcional* | Adiciona estilos personalizados para alterar a aparência de Sidenotes. For more information, see Custom Styles. |
| disableStream | *booleano opcional* | Se verdadeiro, desativa o streaming em tempo real nessa instância do Sidenotes (não em outros streams de comentários). O padrão é falso. |
| ambiente | *cadeia opcional* | Especifica o ambiente UAT do Livefyre. O único valor possível é `t402.livefyre.com`. Para produção, esse parâmetro deve ser removido. |
| iconVisibility | *objeto ou string opcional* | Defines whether the Sidenotes icon will be visible upon hover or static. Se for uma string, ela será usada para ambas as versões do ícone de bloco (vazio e com Sidenotes). Se um objeto, você deve especificar cada tipo: {vazio: "pairar", num: ‘static’}. O padrão é estático. |
| inlineThreads | *booleano opcional* | Se verdadeiro, os threads do Sidenote são inseridos diretamente após o bloco ao qual estão associados. O padrão é falso. |
| numSidenotesEl | *objeto, string ou matriz opcional* | Especifica qual elemento o widget de contagem de Sidenotes será decorado. (Este widget mostra o número de notas de identificação na página e as informações sobre as notas de identificação.) Se o seletor de string corresponder a mais de um elemento, o primeiro será escolhido. (Usa especificação do seletor DOM CSS3.) |
| position | *cadeia opcional* | Determina a posição do pop-up quando um elemento com Sidenotes ativado é clicado. Os valores possíveis são "smart", "left", "right", "bottom". O padrão é "inteligente", que alinha o pop-up à direita da página, a menos que não haja espaço suficiente (nesse caso, ele se moverá para baixo do conteúdo). |
| seletores | *objeto, string ou matriz necessários* | Especifica os elementos nos quais os ícones do iniciador devem aparecer. (Usa especificação do seletor DOM CSS3.) Se o objeto incluir uma seção "inclui" e uma seção "exclui" que aplicará o seletor de CSS a qualquer inclusão correspondente e removerá quaisquer elementos que correspondam às exclusões. Se string, incluirá quaisquer elementos correspondentes na página. Se a matriz lista os elementos a serem incluídos. |
| strings | *objeto opcional* | Adiciona strings de texto personalizadas para alterar qualquer idioma ou texto no aplicativo. Para obter mais informações, consulte Strings personalizadas. |
| threadContainerEl | *objeto, string ou matriz opcional* | Especifica um elemento no qual o thread de sidenotes será exibido. Esse parâmetro permite reposicionar o thread. Se o seletor de string corresponder a mais de um elemento, o primeiro será escolhido. (Usa especificação do seletor DOM CSS3.) |

