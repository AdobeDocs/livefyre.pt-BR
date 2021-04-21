---
title: Uso do filtro de lucratividade
description: Uso do filtro de lucratividade
exl-id: 6ea7d913-f562-42a5-a6ea-241aa4e1089a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Uso do Filtro de Profanação{#using-the-profanity-filter}

Todo o conteúdo publicado em um aplicativo Livefyre é verificado para detecção de profanidade. Se uma palavra incluída na lista de profanidade for encontrada no conteúdo ou no nome de exibição de um usuário, esse conteúdo será sinalizado como &quot;Profanidade&quot;, permitindo filtrá-lo para Premoderação, Regras, ModQ ou pesquisas gerais no Conteúdo do aplicativo.

>[!NOTE]
>
>O conteúdo dos Administradores do Studio e Gerentes não está sujeito à verificação de Regra de lucratividade, e o conteúdo publicado por um Moderador não será sinalizado.

Livefyre fornece uma lista de perfis padrão. Você pode optar por aplicar essa lista no nível da rede, fornecer sua própria lista ou usar uma agregação dos dois. Sites individuais dentro da sua rede podem herdar a Lista de Persistência da rede ou usar uma lista personalizada para ser específica do site.

Para fornecer sua própria lista de perfis personalizada como padrão da rede, envie-a para o gerente de conta do Livefyre.

## Ativando a Filtragem de lucratividade {#section_yqc_qsk_f1b}

Ative e configure o filtro de profanidade no nível da rede e do site. Desative o filtro de profanidade no nível da rede para desabilitar automaticamente o filtro de profanidade para todos os sites que herdam da rede.

>[!NOTE]
>
>Todo o conteúdo que passa pelo Livefyre é verificado em busca de profanidade. Se for encontrado conteúdo que inclui palavras contidas na lista de profanidade SAFE padrão ou em sua lista de Perfil personalizado, ele será sinalizado como &quot;Profanidade&quot;. Para definir o Livefyre para executar ações automaticamente nesses itens, ative **[!UICONTROL Enable Profanity Checking]** para **[!UICONTROL ON]**.

## Ativar o Filtro de Perfil para uma Rede {#section_twd_ssk_f1b}

1. Selecione **[!UICONTROL Network]** no menu suspenso da rede.
1. Ir para **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Role para baixo até **[!UICONTROL Profanity List]** e defina **[!UICONTROL Enable Profanity Checking]** para **[!UICONTROL ON]**.

1. Use o campo **[!UICONTROL Update Network Profanity List]** para adicionar palavras à lista ou clique em uma palavra para removê-la da lista.

>[!NOTE]
>
>Editar a Lista de Perfis no nível da rede não afetará nenhuma Lista no nível do site já existente. Para garantir que as alterações da rede sejam feitas no site, selecione **[!UICONTROL Restore Network List]** para o site depois que as alterações forem feitas.

## Ativar o Filtro de Perfil para um Site {#section_fld_wsk_f1b}

1. Selecione o site no menu suspenso da rede.
1. Ir para **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Role para baixo até **[!UICONTROL Profanity List]** e defina **[!UICONTROL Enable Profanity Checking]** para **[!UICONTROL ON]**.

1. Escolha uma das seguintes opções:

   * Para herdar a Lista de perfis da rede (isso não é comum), defina **[!UICONTROL Use Site Profanity List]** como **[!UICONTROL OFF]**.

   * Para editar a Lista de perfis especificamente para o site, defina **[!UICONTROL Use Site Profanity List]** como **[!UICONTROL On]** para abrir o campo **[!UICONTROL Update Profanity List]**, onde é possível editar a lista:

      * Para remover uma palavra, clique na palavra .
      * Para adicionar uma palavra, digite-a na caixa **[!UICONTROL Add new word]** e pressione **[!UICONTROL Return]**.

      * Para ver se uma palavra está incluída na lista, digite-a na caixa **[!UICONTROL Test profanity filter]**.
   * Para reimportar a Lista de perfis de rede e aplicá-la ao site, clique em **[!UICONTROL Restore Network List]**.
   * Para limpar todo o conteúdo da lista e começar do zero, clique em **[!UICONTROL Clear List]**.


## Trabalhar com conteúdo que contém proficiência {#section_epy_dtk_f1b}

Use a Lista de perfis para ajudar a filtrar suas pesquisas de conteúdo e criar Regras de personalização para o ModQ.

Para procurar conteúdo contendo profanidade, vá para **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** e marque a caixa de seleção **[!UICONTROL Profanity]**. Todo o conteúdo capturado pelo Filtro de perfil do site ou da rede selecionada será exibido. Esta lista incluirá o conteúdo extraído para o aplicativo usando SocialSync e Streams.

Para criar regras de Premoderação, no Studio, selecione **[!UICONTROL Settings > Network Settings > Moderation]**. Depois que o filtro de profanidade for ativado, uma nova regra será exibida, permitindo Sinalizar ou Classificar conteúdo personalizado contendo profanidade. Por padrão, essa regra ativa automaticamente **[!UICONTROL Premoderate]** para conteúdo de perfil, que pode ser alterado para **[!UICONTROL Trash it]** ou **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Se um único conteúdo estiver sujeito a vários tipos de regras (como as regras SAFE e Flag), será aplicado o mais rigoroso. Por exemplo: Se sua regra de Premoderação disser para Premoderizar um conteúdo, mas uma regra SAFE disser para enviá-lo para a lixeira, ele será enviado para a lixeira.

## Exibir e atualizar a lista de perfis de uma rede {#section_qdb_btk_f1b}

1. Ir para **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Role para baixo até a seção **[!UICONTROL Profanity List]**.
1. Defina **[!UICONTROL Enable Profanity Checking]** como **[!UICONTROL On]** para exibir a Lista ativada para sua rede (padrão do Livefyre ou lista personalizada carregada) e edite-a. Você pode editar a lista das seguintes maneiras:
   * Para remover uma palavra, clique na palavra .
   * Para adicionar uma palavra, digite-a na caixa **[!UICONTROL Add new word]** e pressione **[!UICONTROL Return]**.
   * Para ver se uma palavra está incluída na lista, digite-a na caixa **[!UICONTROL Test profanity filter]**.

>[!NOTE]
>
>Somente administradores e moderadores do Studio podem editar Listas de perfis.
