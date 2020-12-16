---
description: Notas de versão para a versão de 21 de setembro de 2017.
seo-description: Notas de versão para a versão de 21 de setembro de 2017.
seo-title: 21 de setembro de 2017
title: 21 de setembro de 2017
uuid: 1132b48a-f85c-4e05-b312-0093db9ebc8f
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 6%

---


# 21 de setembro de 2017{#september}

Notas de versão para a versão de 21 de setembro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Comentários | Os clientes agora podem definir o comprimento máximo para Comentários como parte de sua configuração de rede. |
| Bug | Aplicativo móvel | Esse erro corrige um problema sobre como as respostas aninhadas eram renderizadas no Mobile quando os avatars estavam desativados. |
| Bug | Mosaico | Correção de um erro de produção que fazia com que o mosaico exibisse Caixas cinzas no IE11 no UGC. |
| Aprimoramento | Mosaico | Os clientes agora podem especificar o número de cartões a serem exibidos no aplicativo de visualização Mosaico. |
| Bug | Rights Management | Correção de um erro que impedia um usuário do Studio de solicitar direitos no conteúdo do Instagram Carousel. |
| Bug | Studio | Adicionadas mensagens de erro mais claras ao criar novos Sites. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Aplicativos | Os clientes agora podem criar um único aplicativo Livefyre (Mosaico, Película fotográfica ou Mídia) e incorporá-lo em várias páginas de produtos, que filtrem dinamicamente o UGC apropriado para cada página de produto (por exemplo, o UGC marcado para tênis é exibido na página de produtos para sapatos). |
| Aprimoramento | Película fotográfica | No aplicativo Película fotográfica há um banner &quot;Novo&quot; que marca o novo conteúdo no aplicativo para que os usuários finais possam identificar rapidamente o conteúdo novo. |
| Aprimoramento | Identidade do Livefyre | Os clientes agora podem usar suas credenciais do Github para fazer logon na identidade do Livefyre e participar de nossos aplicativos de comentários. |
| Bug | Rights Management | Correção de um bug que permitia a inserção de caracteres unicode em mensagens de Solicitação de direitos para ignorar a validação. |
| Aprimoramento | Studio | Atualização do link Ajuda do Livefyre na barra de navegação superior. |
| Aprimoramento | Comércio UGC | Os clientes agora podem fazer upload manual de um catálogo de produtos do Google para o estúdio LF usando uma exportação de arquivo JSON. Isso permite que o cliente emparelhe o UGC com produtos desse catálogo e visualize-os em nossos aplicativos ativados para comércio. |
| Aprimoramento | Comércio UGC | Os clientes podem selecionar quais pastas de produto desejam usar ao filtrar seu aplicativo de comércio eletrônico por ID de produto. Por exemplo, eu quero que minha nova Película fotográfica apareça nas páginas de produtos para sapatos e bolsas para mulheres, portanto eu selecionarei apenas as pastas de produtos &quot;Coleção de sapatos femininos&quot; e &quot;Sacos para mulheres&quot;. |
| Aprimoramento | Comércio UGC | Os clientes do Livefyre agora podem filtrar o UGC publicado em seus aplicativos somente se tiverem direitos concedidos. Por exemplo, um cliente pode preparar e publicar uma seleção de itens, mas esses itens só serão renderizados no aplicativo depois que tiverem sido concedidos pelo autor. Este aspecto é particularmente importante para os casos de utilização do comércio eletrônico, em que a UGC é utilizada para fins comerciais. |

