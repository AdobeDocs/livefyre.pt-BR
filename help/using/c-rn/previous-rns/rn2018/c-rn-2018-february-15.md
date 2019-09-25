---
description: Notas de versão para a versão de 15 de fevereiro de 2018.
seo-description: Notas de versão para a versão de 15 de fevereiro de 2018.
seo-title: 15 de fevereiro de 2018
solution: Experience Manager
title: 15 de fevereiro de 2018
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# February 15, 2018{#february}

Notas de versão para a versão de 15 de fevereiro de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Tags inteligentes.**

   Livefyre usa a tecnologia de reconhecimento de imagem do Adobe Sensei para marcar automaticamente as imagens salvas na biblioteca.
Com Tags inteligentes, é possível economizar um tempo significativo na pesquisa e na moderação de conteúdo. Com Tags inteligentes, é possível:

   * Pesquisar imagens salvas para obter conteúdo preciso com base no conteúdo da imagem, em vez de somente texto
   * Coletar conteúdo em fluxos com base em termos de pesquisa precisos que analisam a imagem, em vez de somente texto
   Para obter mais informações sobre Tags inteligentes, consulte Tags [inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Mensagens do produto.** Agora, quando você faz logon no Livefyre Studio, uma janela de anúncios é exibida para exibir atualizações sobre novos recursos.
* **UGC para Carousel.** Agora você pode usar todas as funções do Comércio UGC no aplicativo Livefyre Carousel. Você pode criar um botão de chamada de ação e conectar seu catálogo de produtos ao aplicativo para criar uma experiência que pode ser comprada no Carrossel.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Problema | ModQ | Correção de um problema em que as postagens do Instagram marcadas como aprovadas ou desfeitas estavam entrando novamente na fila. |
| Aprimoramento | Gerenciamento de direitos | Adicionado um aprimoramento para exibir um aviso ao tentar usar contas do Instagram expiradas ao fazer solicitações de direitos. |
| Problema | Tendências | Corrigido um problema no aplicativo de tendências que ainda permitia HTTP às vezes, em vez de HTTPS. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Aplicativos | Adicionada a capacidade de excluir aplicativos do Livefyre. |
| Problema | Pesquisas | As pesquisas foram alteradas para usar HTTPS exclusivamente. Anteriormente, as pesquisas ainda podiam ser usadas com HTTP. |
| Problema | UGC | Correção de um problema em que o UGC em um aplicativo de visualização não filtrava por ID de produto como esperado. |

