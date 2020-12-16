---
description: Notas de versão para a versão de 5 de outubro de 2017.
seo-description: Notas de versão para a versão de 5 de outubro de 2017.
seo-title: 5 de outubro de 2017
title: 5 de outubro de 2017
uuid: 62e9e4ee-1644-4d22-9589-2e208a68aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 4%

---


# 5 de outubro de 2017{#october}

Notas de versão para a versão de 5 de outubro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Identidade do Livefyre | Os clientes que usavam a identidade do Livefyre para fazer login estavam enfrentando problemas ao visualizar ou atualizar seus avatares ao postar em aplicativos de comentários. Isso foi corrigido agora, já que os avatares agora estão visíveis e disponíveis para atualização. |
| Bug | Rights Management | Correção de um bug que exibia nomes de usuário longos na guia Rights Modal. |
| Aprimoramento | Fluxos | Adição da capacidade de pressionar a tecla tab em um campo de texto do Streams para concluir um termo de pesquisa. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Película fotográfica | Quando um cliente implanta um aplicativo de película, o UGC transmitido recentemente terá um rótulo &quot;novo&quot; ao lado dele para identificá-los rapidamente. |
| Aprimoramento | Película fotográfica | A Película fotográfica é um aplicativo de visualização totalmente novo, projetado principalmente para mostrar o UGC em cenários de comércio eletrônico, como páginas de produtos ou sites transacionais. Película fotográfica alinha horizontalmente o UGC para ser exibido como um rolo de câmera, uma peça de cada vez. Os usuários finais podem navegar pela Película fotográfica clicando nas setas laterais para percorrer o conteúdo disponível. |
| Aprimoramento | Biblioteca | Os arquivos carregados na biblioteca por um cliente serão automaticamente concedidos direitos. Este é um recurso útil quando os usuários ativaram o filtro &quot;direitos exigidos concedidos&quot; em seus aplicativos. |
| Aprimoramento | Identidade do Livefyre | Os clientes agora podem usar suas credenciais do Github para fazer logon na LIvefyre Identity e participar de nossos aplicativos de comentários. |
| Bug | Rights Management | Correção de um bug que permitia a inserção de caracteres unicode em mensagens de Solicitação de direitos para ignorar a validação. |
| Aprimoramento | SEGURO | Pequenas melhorias adicionadas à detecção de spam SAFE. |
| Bug | Serviço | Os usuários sem emails válidos têm emails construídos para eles. Correção de um problema com registros de produção em que o sistema não enviava emails para esses usuários. |
| Aprimoramento | Studio | Atualização do link Ajuda do Livefyre na barra de navegação superior. |
| Aprimoramento | Comércio UGC | Como cliente, agora posso criar um único aplicativo Livefyre (Mosaic, FilmStrip ou Media Wall) e incorporá-lo em várias páginas de produtos, que dinamicamente filtros o UGC apropriado para cada página de produto (por exemplo, UGC com sapatos para uma página de produto Shoe). |
| Aprimoramento | Comércio UGC | Os clientes agora podem fazer upload manual de um catálogo de produtos do google para o estúdio do Livefyre usando uma exportação de arquivo JSON. Isso permite que o cliente emparelhe o UGC com produtos desse catálogo e visualize-os em nossos aplicativos ativados para comércio. |
| Aprimoramento | Comércio UGC | Os clientes podem selecionar quais pastas de produto desejam usar ao filtrar seu aplicativo de comércio eletrônico por ID de produto. Por exemplo, quero que minha nova película apareça nas páginas de produtos para sapatos e bolsas para mulheres, portanto, selecionarei apenas as pastas de produtos &quot;Coleção de sapatos para mulheres&quot; e &quot;Sacos para mulheres&quot;. |
| Aprimoramento | Comércio UGC | Os clientes do Livefyre agora podem filtrar o UGC publicado em seus aplicativos somente se tiverem direitos concedidos. Por exemplo, um cliente pode preparar e publicar uma seleção de itens, mas esses itens só serão renderizados no aplicativo depois que tiverem sido concedidos pelo autor. Este aspecto é particularmente importante para os casos de utilização do comércio eletrônico, em que a UGC é utilizada para fins comerciais. |

