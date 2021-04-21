---
description: Notas de versão para 5 de outubro de 2017.
title: 5 de outubro de 2017
exl-id: 6e39a86e-82dd-47ff-ad68-2b483f8b1921
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 4%

---

# 5 de outubro de 2017{#october}

Notas de versão para 5 de outubro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Identidade do Livefyre | Clientes que usavam a identidade do Livefyre para fazer logon apresentavam problemas ao visualizar ou atualizar seus avatares ao postar em aplicativos de comentários. Isso foi corrigido agora, pois os avatares agora estão visíveis e disponíveis para atualização. |
| Bug | Rights Management | Correção de um bug na exibição de nomes de usuário longos na guia Modal de direitos . |
| Aprimoramento | Fluxos | Adição da capacidade de pressionar a tecla tab em um campo de texto Fluxos para concluir um termo de pesquisa. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Tira | Quando um cliente implanta um aplicativo de fita de filme, o UGC recém-transmitido terá um rótulo &quot;novo&quot; ao lado dele para identificá-lo rapidamente. |
| Aprimoramento | Tira | A Tira de arquivo é um aplicativo de visualização totalmente novo, projetado principalmente para mostrar o UGC em cenários de comércio eletrônico, como páginas de produtos ou sites transacionais. A Fita de filme alinha horizontalmente o UGC a ser exibido como um rolo de câmera, uma peça no momento. Os usuários finais podem navegar pela Tira de filme clicando nas setas laterais para rolar pelo conteúdo disponível. |
| Aprimoramento | Biblioteca | Os arquivos carregados na biblioteca por um cliente serão automaticamente concedidos direitos. Esse é um recurso útil quando os usuários ativam o filtro &quot;exigir direitos concedidos&quot; em seus aplicativos. |
| Aprimoramento | Identidade do Livefyre | Os clientes agora podem usar suas credenciais do GitHub para fazer logon na LIvefyre Identity e participar de nossos aplicativos de comentários. |
| Bug | Rights Management | Correção de um erro que permitia a inserção de caracteres unicode nas mensagens de Solicitação de direitos para ignorar a validação. |
| Aprimoramento | SEGURO | Foram adicionadas pequenas melhorias à detecção de spam SAFE. |
| Bug | Serviço | Usuários sem emails válidos têm emails construídos para eles. Correção de um problema com logs de produção em que o sistema não enviava emails para esses usuários. |
| Aprimoramento | Studio | Atualização do link Ajuda do Livefyre na barra de navegação superior. |
| Aprimoramento | Comércio UGC | Como cliente, agora posso criar um único aplicativo Livefyre (Mosaic, FilmStrip ou Media Wall) e incorporá-lo em várias páginas de produto, que filtra dinamicamente o UGC apropriado para cada página de produto (exemplo UGC com sapatos para uma página de produto Sapato). |
| Aprimoramento | Comércio UGC | Os clientes agora podem fazer upload manual de um catálogo de produtos do google no Livefyre studio usando uma exportação de arquivos JSON. Isso permite que o cliente emparelhe o UGC com produtos desse catálogo e os visualize em nossos aplicativos ativados para comércio. |
| Aprimoramento | Comércio UGC | Os clientes podem selecionar quais pastas de produto desejam usar ao filtrar o aplicativo de comércio eletrônico por ID de produto. Por exemplo, quero que minha nova filmagem apareça nas páginas de produtos de sapatos femininos e de sacos para mulheres, portanto, selecionarei apenas a &quot;coleção de sapatos femininos&quot; e as pastas de produtos &quot;Sacos para mulheres&quot;. |
| Aprimoramento | Comércio UGC | Os clientes do Livefyre agora podem filtrar o UGC publicado em seus aplicativos somente se tiverem sido concedidos direitos. Por exemplo, um cliente pode preparar e publicar uma seleção de itens, mas esses itens só serão renderizados no aplicativo quando tiverem sido direitos concedidos pelo autor. Isso é particularmente importante para os casos de uso do comércio eletrônico, em que o UGC é usado para fins comerciais. |
