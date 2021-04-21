---
description: Notas de versão de 21 de setembro de 2017.
title: 21 de setembro de 2017
exl-id: 6d01710e-dab4-4065-85c5-b00f45d8d4fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 6%

---

# 21 de setembro de 2017{#september}

Notas de versão de 21 de setembro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Comentários | Os clientes agora podem definir o comprimento máximo para Comentários como parte de sua configuração de rede. |
| Bug | Aplicativo móvel | Este erro corrige um problema em como as respostas aninhadas eram renderizadas no Mobile quando os avatares estavam desativados. |
| Bug | Mosaico | Correção de um erro de produção que fazia com que o Mosaic exibisse Caixas cinza no IE11 no UGC. |
| Aprimoramento | Mosaico | Os clientes agora podem especificar o número de cartões a serem exibidos no aplicativo de visualização do Mosaic. |
| Bug | Rights Management | Correção de um bug que impedia um usuário do Studio de solicitar direitos no conteúdo do Instagram Carrossel. |
| Bug | Studio | Adição de mensagens de erro mais claras ao criar novos Sites. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Aplicativos | Os clientes agora podem criar um único aplicativo do Livefyre (Mosaic, Filmstrip ou Mural de Mídia) e incorporá-lo em várias páginas de produto, que filtram dinamicamente o UGC apropriado para cada página de produto (por exemplo, o UGC marcado para sapatos é exibido na página de produto do sapato). |
| Aprimoramento | Tira | No aplicativo Filmstrip, há um banner &quot;Novo&quot; que sinaliza o novo conteúdo no aplicativo para que os usuários finais possam identificar rapidamente o novo conteúdo. |
| Aprimoramento | Identidade do Livefyre | Os clientes agora podem usar suas credenciais do GitHub para fazer logon na identidade do Livefyre e participar de nossos aplicativos de comentários. |
| Bug | Rights Management | Correção de um erro que permitia a inserção de caracteres unicode nas mensagens de Solicitação de direitos para ignorar a validação. |
| Aprimoramento | Studio | Atualização do link Ajuda do Livefyre na barra de navegação superior. |
| Aprimoramento | Comércio UGC | Os clientes agora podem fazer upload manual de um catálogo de produtos do Google no estúdio LF usando uma exportação de arquivo JSON. Isso permite que o cliente emparelhe o UGC com produtos desse catálogo e os visualize em nossos aplicativos ativados para comércio. |
| Aprimoramento | Comércio UGC | Os clientes podem selecionar quais pastas de produto desejam usar ao filtrar o aplicativo de comércio eletrônico por ID de produto. Por exemplo, eu quero que minha nova Filmstrip apareça nas páginas de produto de sacos para mulheres e sapatos para sapatos para mulheres, portanto, selecionarei apenas a &quot;coleção de sapatos para mulheres&quot; e as pastas de produtos &quot;Sacos para mulheres&quot;. |
| Aprimoramento | Comércio UGC | Os clientes do Livefyre agora podem filtrar o UGC publicado em seus aplicativos somente se tiverem direitos concedidos. Por exemplo, um cliente pode preparar e publicar uma seleção de itens, mas esses itens só serão renderizados no aplicativo depois que tiverem sido direitos concedidos pelo autor. Isso é particularmente importante para os casos de uso do comércio eletrônico, em que o UGC é usado para fins comerciais. |
