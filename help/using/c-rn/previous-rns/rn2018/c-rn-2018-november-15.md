---
description: Notas de versão para a versão de 15 de novembro de 2018.
seo-description: Notas de versão para a versão de 15 de novembro de 2018.
seo-title: Notas de versão
solution: Experience Manager
title: Notas de versão
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: efb031b58f01ec69c8297a808998d25a0015f102
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---


# Notas de versão{#release-notes}

Notas de versão para a versão de 15 de novembro de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os novos recursos a seguir foram lançados na versão de produção desta versão:

* **Atualizações para a pesquisa e o fluxo do Instagram.** Você pode usar uma conta *comercial do* Instagram para:

   * Execute uma pesquisa social do Instagram por usuário (o usuário também deve ser uma conta comercial do Instagram).

   * Crie fluxos do Instagram a partir de uma conta de usuário específica do Instagram (a conta também deve ser uma conta comercial), incluindo a sua.

   * Solicite direitos para ativos do Instagram usando um fluxo de trabalho parcialmente automatizado.

   * Para obter informações sobre que tipo de contas do Instagram você precisa configurar e solicitar direitos do Instagram, consulte [Sobre contas](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)do Instagram.

* **Monitoramento automático de respostas de solicitação de direitos de uso para pesquisas baseadas em conta de negócios.** Somente para pesquisas baseadas em contas comerciais — a capacidade de monitorar automaticamente respostas a solicitações de direitos e atualizar o histórico de atividades no Livefyre está disponível.

Para obter mais informações sobre como solicitar direitos para contas do Instagram, consulte [Enviar solicitação de direitos do Instagram manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) e [Enviar uma solicitação](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)de direitos do Instagram parcialmente automatizada.

* **Integração com o Adobe Target.** Adicionada integração com a Adobe Target que permite compartilhar aplicativos Livefyre diretamente na sua biblioteca do Adobe Target Oferta. Para obter mais informações sobre como usar o Livefyre com a Adobe Target, consulte a documentação [do](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html)Público alvo.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

### Versão de produção

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Problema | AppService: Identidade do Livefyre | Correção de um problema em que clicar em não [!UICONTROL Reset to Default] redefinia o logotipo em Login Modal em Studio > Configurações de integração > Identidade do Livefyre na imagem padrão. |
| Problema | Biblioteca | Correção de um problema em que um vídeo carregado na Biblioteca e exibido em detalhes do ativo não era exibido corretamente. |
| Problema | Fluxos | Correção de um problema que impedia que os produtos fossem exibidos em uma regra de fluxo. |
| Problema | Fluxos | Correção de um problema em que as tags de produto não estavam disponíveis para uma regra de fluxo. |
| Aprimoramento | Studio | Corrigido um problema no qual a ID de produto não era exibida no Livefyre Studio. |
| Problema | Estúdio: ModQ | Correção de um problema em que o conteúdo excluído ainda era exibido no ModQ após ser excluído. |

### Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Problema | Componente social: Carrossel | Correção de um problema em que o link Compartilhar não respondia e copiava o URL como esperado no IE11 e no Mozilla Firefox. |