---
description: Notas de versão da versão de November 5 de novembro de 25 18.
seo-description: Notas de versão da versão de November 5 de novembro de 25 18.
seo-title: Notas de versão
solution: Experience Manager
title: Notas de versão
uuid: 34 e 64943-dea 6-46 ac -9 fcc -8 febeab 6 aa 42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# Notas de versão{#release-notes}

Notas de versão da versão de November 5 de novembro de 25 18.

## Novos recursos {#section_syx_mdt_wcb}

Os novos recursos a seguir foram lançados na versão de produção desta versão:

* **Atualizações na pesquisa e no fluxo do Instagram.** Você pode usar uma *conta de negócios do Instagram* para:

   * Realize uma pesquisa social do Instagram por usuário (o usuário deve ser uma conta de negócios do Instagram também).

   * Crie fluxos do Instagram de uma conta específica do usuário do Instagram (a conta também deve ser uma conta comercial), incluindo os seus próprios.

   * Direitos de solicitação para ativos do Instagram usando um fluxo de trabalho parcialmente automatizado.

   * Para obter informações sobre o tipo de contas do Instagram que você precisa configurar e solicitar direitos do Instagram, consulte [Sobre contas](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)do Instagram.

* **Monitoramento automático de direitos de uso solicita respostas para pesquisas com base em conta empresarial.** Somente pesquisas com base em contas comerciais—a capacidade de monitorar automaticamente respostas a solicitações de direitos e atualizar o histórico de atividades no Livefyre está disponível.

Para obter mais informações sobre como solicitar direitos para contas do Instagram, consulte [Enviar solicitação de direitos do Instagram manualmente](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) e [Enviar uma solicitação de direitos do Instagram parcialmente automatizada](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integração do Adobe Target.** Integração adicionada com o Adobe Target permite compartilhar aplicativos do Livefyre diretamente na Biblioteca de ofertas do Adobe Target. Para obter mais informações sobre como usar o Livefyre com o Adobe Target, consulte [a documentação do Target](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

### Versão de produção

| Tipo de edição | Componente | Nota de versão |
|--- |--- |--- |
| Problema | Appservice: Identidade do Livefyre | Correção de um problema em que clicar [em! Redefinir o UICONTROL para o padrão] não redefine o logotipo em Modal de logon em Studio &gt; Configurações de integração &gt; Identidade do Livefyre para a imagem padrão. |
| Problema | Biblioteca | Correção de um problema em que um vídeo carregado na Biblioteca e exibido no detalhe do ativo não era exibido corretamente. |
| Problema | Fluxos | Correção de um problema que impedia que os produtos fossem exibidos em uma regra de fluxo. |
| Problema | Fluxos | Correção de um problema em que tags de produto não estavam disponíveis para uma regra de fluxo. |
| Aprimoramento | Studio | Correção de um problema em que a ID de produto não era exibida no Livefyre Studio. |
| Problema | Studio: Modq | Corrigido um problema no qual o conteúdo excluído ainda era exibido na modq depois de ser excluído. |

### Versão do UAT

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Problema | Componente social: Carrossel | Correção de um problema em que o link Compartilhar não respondia e copiava o URL como esperado no IE 11 e no Mozilla Firefox. |