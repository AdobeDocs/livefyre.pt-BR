---
description: Notas de versão para 15 de novembro de 2018.
title: Notas de versão
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# Notas de versão{#release-notes}

Notas de versão para 15 de novembro de 2018.

## Novos recursos {#section_syx_mdt_wcb}

Os seguintes novos recursos foram lançados na versão de produção desta versão:

* **Atualizações na pesquisa e no fluxo do Instagram.** Você pode usar uma conta comercial  *Instagram* para:

   * Realize uma pesquisa social do Instagram por usuário (o usuário também deve ser uma conta comercial do Instagram).

   * Crie fluxos do Instagram a partir de uma conta de usuário específica do Instagram (a conta também deve ser uma conta comercial), incluindo a sua.

   * Solicite direitos para ativos do Instagram usando um fluxo de trabalho parcialmente automatizado.

   * Para obter informações sobre que tipo de conta do Instagram você precisa configurar e solicitar direitos do Instagram, consulte [Sobre contas do Instagram](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Monitoramento automático de respostas de solicitação de direitos de uso para pesquisas com base em conta de negócios.** Somente para pesquisas baseadas em contas comerciais — a capacidade de monitorar automaticamente respostas a solicitações de direitos e atualizar o histórico de atividades no Livefyre está disponível.

Para obter mais informações sobre como solicitar direitos para contas do Instagram, consulte [Enviar solicitação de direitos do Instagram manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) e [Enviar uma solicitação de direitos do Instagram parcialmente automatizada](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integração com o Adobe Target.** Adição de integração com o Adobe Target, que permite compartilhar os aplicativos do Livefyre diretamente na Biblioteca de ofertas da Adobe Target. Para obter mais informações sobre como usar o Livefyre com Adobe Target, consulte a [documentação do Target](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html).

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

### Versão de produção

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Problema | AppService: Identidade do Livefyre | Correção de um problema em que clicar em [!UICONTROL Reset to Default] não redefinia o logotipo em Login Modal em Studio > Configurações de integração > Identidade do Livefyre para a imagem padrão. |
| Problema | Biblioteca | Correção de um problema em que um vídeo carregado na Biblioteca e visualizado em detalhes do ativo não era exibido corretamente. |
| Problema | Fluxos | Correção de um problema que impedia que os produtos fossem exibidos em uma regra de fluxo. |
| Problema | Fluxos | Correção de um problema em que as tags de produto não estavam disponíveis para uma regra de fluxo. |
| Aprimoramento | Studio | Correção de um problema em que a ID do produto não era exibida no Livefyre Studio. |
| Problema | Estúdio: ModQ | Correção de um problema em que o conteúdo excluído ainda era exibido no ModQ após ser excluído. |

### Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Problema | Componente social: Carrossel | Correção de um problema em que o link Compartilhar não respondia e copiava o URL conforme esperado no IE11 e no Mozilla Firefox. |
