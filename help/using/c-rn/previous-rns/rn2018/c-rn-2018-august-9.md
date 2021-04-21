---
description: Notas de versão de 9 de agosto de 2018.
title: 9 de agosto de 2018
exl-id: 7b2fb562-33bf-4c34-ab83-5fc34f5d1f4f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 8%

---

# 9 de agosto de 2018{#august}

Notas de versão de 9 de agosto de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

**Tags inteligentes de vídeo:** os usuários agora podem ver tags inteligentes para vídeos com menos de 50 MB.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Conteúdo do aplicativo | Correção de um problema que impedia os administradores e gerentes de conteúdo de editar conteúdo no Conteúdo do aplicativo. |
| Aprimoramento | Aplicativos | As redes sociais fizeram alterações na privacidade, o que significa que as menções sociais não serão mais suportadas pelo Facebook ou Twitter. |
| Aprimoramento | Aplicativos | As redes sociais fizeram mudanças na privacidade. O recurso &quot;Publicar em&quot; que publica automaticamente o conteúdo nas redes sociais (Facebook, LinkedIn, Twitter) foi removido. |
| Aprimoramento | RGPD | Remoção do modo de alternância para detalhes da página de detalhes da solicitação em Configurações > Privacidade. A alternância do modo de detalhes ainda pode ser acessada adicionando /dbg ao final do URL. |
| Bug | Integração: AEM | Correção de um problema em que arrastar e soltar aplicativos Livefyre no AEM parecia criar vários aplicativos. |
| Bug | Biblioteca | Correção de um problema em que um ativo não era salvo corretamente na biblioteca. |
| Bug | Identidade do Livefyre | Correção de um problema com a identidade LF que causava erros 403 ao fazer logon. |
| Bug | Pesquisa social | Correção de um problema em que os usuários não conseguiam pesquisar por publicações públicas do Facebook usando a opção URL na Pesquisa social. |
| Aprimoramento | Sincronização social | As redes sociais fizeram alterações na privacidade, o que significa que a Sincronização social não será mais compatível com o Facebook. |
| Aprimoramento | Fluxos | Agora, ao excluir um aplicativo, você exclui todos os fluxos associados a ele. |
| Aprimoramento | Studio | Os clientes agora têm a capacidade de emitir eventos do Livefyre para o Adobe Analytics individualmente, em vez de em lotes. |
| Aprimoramento | Studio | As janelas modais exibidas em aplicativos de conversação para redes sociais agora serão janelas modais da rede social em vez do Adobe Experience Manager Livefyre ou outras janelas modais de marca. |

## Versão UAT

Os problemas nas tabelas a seguir foram resolvidos na versão da UAT.

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | RGPD | Correção de um problema em que as mensagens de rejeição não eram exibidas em alguns vídeos do Instagram. |
| Bug | Biblioteca | Correção de um problema em que um cartão com direitos concedidos manualmente exibia o status errado da solicitação de direitos. |
| Bug | Biblioteca | Correção de um problema em que um ativo não podia ser salvo em uma pasta. |
| Bug | Biblioteca/Pesquisa | A capacidade de pesquisar URLs do Instagram na Pesquisa do Social foi restaurada. |
| Bug | ModQ | Correção de um problema em que o Menu Mais informações no ModQ não era exibido quando esperado. |
| Bug | Rights Management | Correção de um problema em que a classificação no ModQ deve estar em uma posição fixa quando a página é rolada. |
| Bug | Fluxos | Correção de um problema com a visualização de fluxos no ambiente de preparo. |
| Aprimoramento | Fluxos | Adição de um botão Seguro para trabalho (SFW) e Não seguro para trabalho (NSFW) para fluxos. |
| Aprimoramento | Studio | Adição da funcionalidade de tag inteligente ao conteúdo carregado na Biblioteca do Livefyre Studio por meio do FileStack (recurso de upload em todos os ativos). |
