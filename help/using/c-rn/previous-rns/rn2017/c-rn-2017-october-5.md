---
description: Notas de versão de 5 de outubro de 2017.
seo-description: Notas de versão de 5 de outubro de 2017.
seo-title: 5 de outubro de 2017
title: 5 de outubro de 2017
uuid: 62 e 9 e 4 ee -1644-4 d 22-9589-2 e 208 a 68 aaeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 5 de outubro de 2017{#october}

Notas de versão de 5 de outubro de 2017.

## Versão de produção

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Identidade do Livefyre | Os clientes que usam a identidade do Livefyre para fazer login tiveram problemas ao ver ou atualizar seus avatars ao postar em aplicativos de comentários. Isso foi corrigido agora, já que os avatars agora estão visíveis e estão disponíveis para atualização. |
| Bug | Gerenciamento de direitos | Correção de um erro com a exibição de nomes de usuário longos na guia Direito modal. |
| Aprimoramento | Fluxos | Adição da capacidade de acessar a tecla tab em um campo de texto Fluxos para concluir um termo de pesquisa. |

## Versão do UAT

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Película fotográfica | Quando um cliente implanta um aplicativo de película de filme, o UGC transmitido recentemente terá um rótulo &quot;novo&quot; ao lado de sua identificação rápida. |
| Aprimoramento | Película fotográfica | Película fotográfica é um novo aplicativo de visualização, desenvolvido principalmente para mostrar UGC em cenários de comércio eletrônico, como páginas de produtos ou sites transacionais. A Película fotográfica alinha horizontalmente o UGC a ser exibido como um rolo da câmera, uma parte no momento. Os usuários finais podem navegar em Película fotográfica clicando nas setas laterais para percorrer o conteúdo disponível. |
| Aprimoramento | Biblioteca | Os arquivos carregados na biblioteca por um cliente serão concedidos automaticamente. Esse recurso é útil quando os usuários ativaram o filtro &quot;exigir direitos concedidos&quot; em seus aplicativos. |
| Aprimoramento | Identidade do Livefyre | Os clientes agora podem usar suas credenciais Github para fazer logon na identidade do livefyre e participar de nossos aplicativos de comentários. |
| Bug | Gerenciamento de direitos | Correção de um erro que permitia a inserção de caracteres unicode em mensagens de Solicitação de direitos para ignorar a validação. |
| Aprimoramento | SAFE | Pequenas melhorias adicionadas à detecção de SPAM SAFE. |
| Bug | Serviço | Os usuários sem e-mails válidos têm e-mails construídos para eles. Correção de um problema com registros de produção nos quais o sistema não enviou emails para esses usuários. |
| Aprimoramento | Studio | Atualização do link Ajuda do Livefyre na barra de navegação superior. |
| Aprimoramento | Comércio UGC | Como cliente, agora posso criar um aplicativo único do Livefyre (Mosaic, filmstrip ou Media Wall) e incorporá-lo em várias páginas de produtos, que filtra dinamicamente o UGC apropriado para cada página de produto (por exemplo, UGC com sapatos para uma página de produto do Shoe). |
| Aprimoramento | Comércio UGC | Os clientes agora podem carregar manualmente um catálogo de produtos do Google no Livefyre studio usando uma exportação de arquivo JSON. Isso permite que o cliente ignore UGC com produtos desse catálogo e visualize-os em nossos aplicativos habilitados para comércio. |
| Aprimoramento | Comércio UGC | Os clientes podem selecionar quais pastas de produto deseja usar ao filtrar seu aplicativo de comércio eletrônico por ID de produto. Por exemplo, quero que minha nova película apareça em calçados femininos e em fotos de produtos femininos. Portanto, selecionarei apenas as pastas de produto &quot;Coleção de sapatos femininos&quot; e &quot;Camuras femininas&quot;. |
| Aprimoramento | Comércio UGC | Os clientes do Livefyre agora podem filtrar o UGC publicado em seus aplicativos somente se tiverem sido direitos concedidos. Por exemplo, um cliente pode preparar e publicar uma seleção de itens, mas esses itens só serão renderizados no aplicativo depois que tiverem direitos concedidos pelo autor. Isso é especialmente importante para casos de uso de comércio eletrônico, onde o UGC é usado para fins comerciais. |

