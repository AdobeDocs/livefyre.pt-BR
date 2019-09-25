---
description: 'null'
seo-description: 'null'
seo-title: Usando o Filtro de Profanidade
solution: Experience Manager
title: Usando o Filtro de Profanidade
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Usando o Filtro de Profanidade{#using-the-profanity-filter}

Todo o conteúdo publicado em um aplicativo Livefyre é verificado quanto à profanidade. Se uma palavra incluída na lista de profanidade for encontrada no conteúdo ou no nome de exibição de um usuário, esse conteúdo será sinalizado como "Profanidade", permitindo que você a filtre por Premoderação, Regras, ModQ ou pesquisas gerais no Conteúdo do aplicativo.

>[!NOTE]
>
>O conteúdo dos Administradores e Gerentes do Studio não está sujeito à verificação Regra de Profanidade, e o conteúdo publicado por um Moderador não será sinalizado.

Livefyre fornece uma lista de profanidade padrão. Você pode optar por aplicar essa lista no nível da rede, fornecer sua própria lista ou usar um agregado dos dois. Os sites individuais dentro da sua rede podem herdar a Lista de perfis da rede ou usar uma lista personalizada para ser específica do site.

Para fornecer sua própria lista de profanidade personalizada como padrão de rede, envie-a para o gerente de conta do Livefyre.

## Ativação da filtragem de lucros {#section_yqc_qsk_f1b}

Ative e configure o filtro de profanidade tanto no nível da rede quanto do site. Desative o filtro de profanidade no nível da rede para desativar automaticamente o filtro de profanidade para todos os sites herdados da rede.

>[!NOTE]
>
>Todo o conteúdo que passa pelo Livefyre é verificado quanto à profanidade. Se for encontrado conteúdo que inclui palavras contidas na lista de profanidade SAFE padrão ou na lista de Profanidade personalizada, ele será marcado como "Profanidade". Para definir o Livefyre para agir automaticamente nestes itens, vá **[!UICONTROL Enable Profanity Checking]** para **[!UICONTROL ON]**.

## Ativar o filtro de lucratividade para uma rede {#section_twd_ssk_f1b}

1. Selecione **[!UICONTROL Network]** no menu suspenso de rede.
1. Ir para **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Role para baixo até o **[!UICONTROL Profanity List]** e defina **[!UICONTROL Enable Profanity Checking]** como **[!UICONTROL ON]**.

1. Use o **[!UICONTROL Update Network Profanity List]** campo para adicionar palavras à lista ou clique em uma palavra para removê-la da lista.

>[!NOTE]
>
>A edição da Lista de lucratividade no nível da rede não afetará nenhuma Lista no nível do site já em vigor. Para garantir que as alterações da rede sejam feitas no site, selecione **[!UICONTROL Restore Network List]** o site depois que as alterações forem feitas.

## Ativar o Filtro de Profanação para um Site {#section_fld_wsk_f1b}

1. Selecione o site no menu suspenso de rede.
1. Ir para **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Role para baixo até a página **[!UICONTROL Profanity List]** e defina **[!UICONTROL Enable Profanity Checking]** como **[!UICONTROL ON]**.

1. Escolha uma das seguintes opções:

   * Para herdar a Lista de Profissionais da rede (isso não é comum), defina **[!UICONTROL Use Site Profanity List]** como **[!UICONTROL OFF]**.

   * Para editar a Lista de Profanidade especificamente para o site, defina **[!UICONTROL Use Site Profanity List]** para **[!UICONTROL On]** abrir o **[!UICONTROL Update Profanity List]** campo, onde você pode editar a lista:

      * Para remover uma palavra, clique na palavra.
      * Para adicionar uma palavra, digite-a na **[!UICONTROL Add new word]** caixa e pressione **[!UICONTROL Return]**.

      * Para ver se uma palavra está incluída na lista, digite-a na **[!UICONTROL Test profanity filter]** caixa.
   * Para reimportar a lista de lucros da rede e aplicá-la ao site, clique em **[!UICONTROL Restore Network List]**.
   * Para limpar todo o conteúdo da lista e começar do zero, clique em **[!UICONTROL Clear List]**.


## Trabalhar com conteúdo que contém profissionalismo {#section_epy_dtk_f1b}

Use a Lista de perfis para ajudar a filtrar suas pesquisas de conteúdo e criar Regras de visualização para o ModQ.

Para procurar conteúdo que contenha profanidade, vá até **[!UICONTROL Library > App Content]** e marque a caixa de seleção **[!UICONTROL Filter by Flags]** **[!UICONTROL Profanity]** . Todo o conteúdo capturado pelo Filtro de lucratividade do site ou da rede selecionada será exibido. Essa lista incluirá o conteúdo extraído no aplicativo usando o SocialSync e os Streams.

Para criar regras de Premoderation, selecione **[!UICONTROL Settings > Network Settings > Moderation]** no Studio. Assim que o filtro de profanidade for ativado, uma nova regra será exibida, permitindo que você Sinalize ou Prepare o conteúdo que contém profanidade. Por padrão, essa regra ativa automaticamente **[!UICONTROL Premoderate]** para conteúdo profano, que pode ser alterado para **[!UICONTROL Trash it]** ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se um único conteúdo estiver sujeito a vários tipos de regras (como regras SAFE e Flag), será aplicado o mais rigoroso. Por exemplo: Se sua regra de Premoderação disser para Premoderizar um conteúdo, mas uma regra SAFE disser para Lixeira, ela será Lixada.

## Exibir e atualizar a lista de profissões de uma rede {#section_qdb_btk_f1b}

1. Ir para **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Role para baixo até a **[!UICONTROL Profanity List]** seção.
1. Defina **[!UICONTROL Enable Profanity Checking]** para exibir **[!UICONTROL On]** a Lista ativada para sua rede (padrão do Livefyre ou sua lista personalizada carregada) e edite-a. Você pode editar a lista das seguintes maneiras:
   * Para remover uma palavra, clique na palavra.
   * Para adicionar uma palavra, digite-a na **[!UICONTROL Add new word]** caixa e pressione **[!UICONTROL Return]**.
   * Para ver se uma palavra está incluída na lista, digite-a na **[!UICONTROL Test profanity filter]** caixa.

>[!NOTE]
>
>Somente administradores e moderadores do Studio podem editar Listas de Profanidade.

