---
description: Notas de versão para 15 de fevereiro de 2018.
title: 15 de fevereiro de 2018
exl-id: 7276de37-c8cd-4e85-bc92-90c272e5bf94
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# 15 de fevereiro de 2018{#february}

Notas de versão para 15 de fevereiro de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Tags inteligentes.**

   O Livefyre usa a tecnologia de reconhecimento de imagem da Adobe Sensei para marcar automaticamente as imagens salvas na biblioteca.
Com as Tags inteligentes, é possível economizar um tempo significativo na pesquisa e na moderação do conteúdo. Com Tags inteligentes, você pode:

   * Pesquise imagens salvas para obter conteúdo preciso com base no conteúdo da imagem, em vez de somente texto
   * Colete conteúdo em fluxos com base em termos de pesquisa precisos que analisam a imagem, em vez de somente texto

   Para obter mais informações sobre Tags inteligentes, consulte [Tags inteligentes](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **Mensagens no produto.** Agora, quando você faz logon no Livefyre Studio, uma janela de anúncios aparece para exibir atualizações sobre novos recursos.
* **UGC para carrossel.** Agora você pode usar todas as funções do UGC Commerce no aplicativo Livefyre Carousel. Você pode criar um botão de ação de chamada e conectar o catálogo de produtos ao aplicativo para criar uma experiência de compra no Carrossel.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Problema | ModQ | Correção de um problema em que publicações do Instagram marcadas como aprovadas ou enviadas para a lixeira eram inseridas novamente na fila. |
| Aprimoramento | Rights Management | Adição de um aprimoramento para exibir um aviso ao tentar usar contas Instagram expiradas enquanto faz Solicitações de direitos. |
| Problema | Tendências | Correção de um problema em que o Aplicativo de tendência ainda permitia HTTP às vezes, em vez de HTTPS. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Aplicativos | Adicionada a capacidade de excluir aplicativos do Livefyre. |
| Problema | Pesquisas | Pesquisa alterada para usar exclusivamente HTTPS. Anteriormente, as Pesquisas ainda tinham permissão para serem usadas com HTTP. |
| Problema | UGC | Correção de um problema em que o UGC em um aplicativo de visualização não era filtrado por ID de produto conforme esperado. |
