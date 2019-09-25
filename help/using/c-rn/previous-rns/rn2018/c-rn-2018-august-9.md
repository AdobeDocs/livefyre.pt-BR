---
description: Notas de versão de 9 de agosto de 2018.
seo-description: Notas de versão de 9 de agosto de 2018.
seo-title: 9 de agosto de 2018
solution: Experience Manager
title: 9 de agosto de 2018
uuid: c59ae5ec-9d26-41c4-9a98-cb95c89ee26a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 9 de agosto de 2018{#august}

Notas de versão de 9 de agosto de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

**** Tags inteligentes de vídeo: Os usuários agora podem ver tags inteligentes para vídeos com menos de 50 MB.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Conteúdo do aplicativo | Correção de um problema que impedia administradores e gerentes de conteúdo de editar conteúdo no Conteúdo do aplicativo. |
| Aprimoramento | Aplicativos | As redes sociais fizeram alterações na privacidade que significam que as menções sociais não serão mais suportadas no Facebook ou no Twitter. |
| Aprimoramento | Aplicativos | As redes sociais fizeram mudanças na privacidade. O recurso "Publicar em" que publica automaticamente conteúdo em redes sociais (Facebook, LinkedIn, Twitter) foi removido. |
| Aprimoramento | RGPD | Removed the toggle for details mode from the request details page under Settings &gt; Privacy. A alternância do modo de detalhes ainda pode ser acessada adicionando /dbg no final do URL. |
| Bug | Integração: AEM | Correção de um problema em que arrastar e soltar aplicativos Livefyre no AEM parecia criar vários aplicativos. |
| Bug | Biblioteca | Correção de um problema em que um ativo não era salvo corretamente na biblioteca. |
| Bug |  Identidade do Livefyre | Correção de um problema com a identidade LF que causava erros 403 ao fazer logon. |
| Bug | Pesquisa social | Correção de um problema em que os usuários não conseguiam pesquisar por publicações públicas do Facebook usando a opção URL na Pesquisa social. |
| Aprimoramento | Sincronização social | As redes sociais fizeram alterações de privacidade que significam que a Sincronização social não será mais suportada no Facebook. |
| Aprimoramento | Fluxos | Agora, ao excluir um aplicativo, você exclui todos os fluxos associados a esse aplicativo. |
| Aprimoramento | Studio | Os clientes agora têm a capacidade de emitir eventos do Livefyre para o Adobe Analytics individualmente, em vez de em lotes. |
| Aprimoramento | Studio | As janelas modais exibidas nos aplicativos de conversação para redes sociais agora serão janelas modais da rede social em vez do Adobe Experience Manager Livefyre ou de outras janelas modais de marca. |

## Versão UAT

Os problemas nas tabelas a seguir foram resolvidos na versão UAT.

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | RGPD | Corrigido um problema no qual as mensagens de não participação não eram exibidas em alguns vídeos do Instagram. |
| Bug | Biblioteca | Correção de um problema em que um cartão com direitos concedidos exibia manualmente o status errado de solicitação de direitos. |
| Bug | Biblioteca | Correção de um problema em que um ativo não podia ser salvo em uma pasta. |
| Bug | Biblioteca/pesquisa | A capacidade de pesquisar URLs do Instagram no Social Search foi restaurada. |
| Bug | ModQ | Correção de um problema em que o menu Mais informações no ModQ não era exibido onde esperado. |
| Bug | Gerenciamento de direitos | Correção de um problema em que a classificação no ModQ deveria estar em uma posição fixa quando a página é rolada. |
| Bug | Fluxos | Correção de um problema com a exibição de fluxos no ambiente de preparo. |
| Aprimoramento | Fluxos | Adição de um alternador Safe For Work (SFW) e Not Safe For Work (NSFW) para Streams. |
| Aprimoramento | Studio | Adição da funcionalidade de tag inteligente ao conteúdo carregado na biblioteca do Livefyre Studio via FileStack (funcionalidade de upload em todos os ativos). |

