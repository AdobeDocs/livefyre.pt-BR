---
description: null
seo-description: null
seo-title: Uso do Filtro de profanidade
solution: Experience Manager
title: Uso do Filtro de profanidade
uuid: b 0 b 1 fbae-c 88 c -403 c -9 b 91-df 6620675 f 39
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Uso do Filtro de profanidade{#using-the-profanity-filter}

Todo o conteúdo publicado em um aplicativo Livefyre é verificado para profanidade. Se uma palavra incluída na lista de profanidade for encontrada no conteúdo ou no nome de exibição de um usuário, esse conteúdo será sinalizado «Profanity», permitindo filtrá-lo para pré-moderação, Regras, modq ou pesquisas gerais no Conteúdo do aplicativo.

>[!NOTE]
>
>O conteúdo dos administradores e gerentes do Studio não está sujeito à verificação da Regra de profanidade, e o conteúdo publicado por um Moderador não será sinalizado.

O Livefyre fornece uma lista de profanidade padrão. Você pode optar por aplicar essa lista no nível da rede, fornecer sua própria lista ou usar um agregado dos dois. Os sites individuais dentro da rede podem herdar a lista de perfis de rede ou usar uma lista personalizada para ser específica do site.

Para fornecer sua própria lista de perfis personalizados como padrão de rede, envie-a para seu gerente de contas do Livefyre.

## Ativação da filtragem de perfis {#section_yqc_qsk_f1b}

Ative e configure o filtro de profanidade em nível de rede e site. Desative o filtro de perfil no nível da rede para desativar automaticamente o filtro de profanidade para todos os sites herdados da rede.

>[!NOTE]
>
>Todo o conteúdo transmitido pelo Livefyre é verificado para profanidade. Se o conteúdo for encontrado, incluindo palavras contidas na lista de profanidade SEGURA padrão ou na lista personalizada de Profanity, ela será sinalizada como "Profanity". » Para configurar o Livefyre para executar ações automaticamente nesses itens, **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**acesse.

## Ativar o Filtro de perfil para uma rede {#section_twd_ssk_f1b}

1. Selecione **[!UICONTROL Network]** no menu suspenso de rede.
1. Ir **[!UICONTROL Settings > Network Settings > Moderation]**para.
1. Role para baixo até o **[!UICONTROL Profanity List]**e defina **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**como.

1. Use **[!UICONTROL Update Network Profanity List]** o campo para adicionar palavras à lista ou clique em uma palavra para removê-la da lista.

>[!NOTE]
>
>A edição da lista de perfis de nível de rede não afetará nenhuma lista em nível de site já vigente. Para garantir que as alterações da rede sejam feitas no site, selecione **[!UICONTROL Restore Network List]** -o depois que as alterações tiverem sido feitas.

## Ativar o Filtro de perfis para um site {#section_fld_wsk_f1b}

1. Selecione o site no menu suspenso de rede.
1. Ir **[!UICONTROL Settings > Site Settings > Moderation]**para.
1. Role para baixo até **[!UICONTROL Profanity List]** o e defina **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**como.

1. Escolha uma das seguintes opções:

   * Para herdar a Lista de perfis da rede (isso não é comum), defina **[!UICONTROL Use Site Profanity List]** como **[!UICONTROL OFF]**.

   * Para editar a lista de perfis especificamente para o site, defina **[!UICONTROL Use Site Profanity List]** para **[!UICONTROL On]** abrir o **[!UICONTROL Update Profanity List]** campo, onde você pode editar a lista:

      * Para remover uma palavra, clique na palavra.
      * Para adicionar uma palavra, digite a palavra na **[!UICONTROL Add new word]** caixa e na ocorrência **[!UICONTROL Return]**.

      * Para ver se uma palavra está incluída na lista, digite a palavra na **[!UICONTROL Test profanity filter]** caixa.
   * Para reimportar a lista de perfis de rede e aplicá-la ao site, clique **[!UICONTROL Restore Network List]**em.
   * Para limpar todo o conteúdo da lista e começar do zero, clique **[!UICONTROL Clear List]**em.


## Trabalhar com conteúdo que contém profanity {#section_epy_dtk_f1b}

Use a Lista de perfis para ajudar a filtrar suas pesquisas de conteúdo e criar Regras de pré-moderação para modq.

Para pesquisar o conteúdo que contém a profanidade, vá para **[!UICONTROL Library > App Content]**e **[!UICONTROL Filter by Flags]** marque a **[!UICONTROL Profanity]** caixa de seleção. Todo o conteúdo que foi capturado pelo Filtro de perfil para o site ou rede selecionada será exibido. Esta lista incluirá conteúdo inserido no aplicativo usando o socialsync e Fluxos.

Para criar regras de pré-moderação, a partir do Studio selecione **[!UICONTROL Settings > Network Settings > Moderation]**. Uma vez que o filtro de profanidade estiver ativado, uma nova regra será exibida, permitindo o sinalizador ou o conteúdo pré-moderado com profanidade. Por padrão, essa regra ativa **[!UICONTROL Premoderate]** automaticamente o conteúdo profane, que pode ser alterado **[!UICONTROL Trash it]** para ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se um único conteúdo estiver sujeito a vários tipos de regras (como regras SAFE e Sinalizar), mais estritas serão aplicadas. Por exemplo: Se a regra de Pré-moderação diz para Pré-moderar um conteúdo, mas uma Regra SAFE diz para lixeira, ela será travada.

## Exibir e atualizar a lista de perfis de uma rede {#section_qdb_btk_f1b}

1. Ir **[!UICONTROL Settings > Network Settings > Moderation]**para.
1. Role para baixo até **[!UICONTROL Profanity List]** a seção.
1. Defina **[!UICONTROL Enable Profanity Checking]** para **[!UICONTROL On]** exibir a lista habilitada para sua rede (padrão do Livefyre ou sua lista personalizada carregada) e editá-la. Você pode editar a lista das seguintes maneiras:
   * Para remover uma palavra, clique na palavra.
   * Para adicionar uma palavra, digite a palavra na **[!UICONTROL Add new word]** caixa e na ocorrência **[!UICONTROL Return]**.
   * Para ver se uma palavra está incluída na lista, digite a palavra na **[!UICONTROL Test profanity filter]** caixa.

>[!NOTE]
>
>Somente administradores e moderadores do Studio podem editar listas de perfis.

