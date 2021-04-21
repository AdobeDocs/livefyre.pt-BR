---
description: Você pode criar regras de fluxo que obtêm conteúdo das regras do YouTube.
title: Regras do YouTube
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Regras do YouTube {#youtube-rules}

Você pode criar regras de fluxo que obtêm conteúdo das regras do YouTube.

Crie regras do YouTube com base em Usuário, Canal ou Lista de reprodução.

Para criar Regras do YouTube para extrair conteúdo do YouTube para seu aplicativo ou Pasta, você pode filtrar por:

* **[!UICONTROL User]**
   * Insira a string personalizada para um **[!UICONTROL User]** para incluir vídeos do Usuário no Stream.
   * Por exemplo, se o URL do feed de usuário que você deseja inserir for `https://www.youtube.com/user/livefyresupport`, basta inserir `livefyresupport`.

* **[!UICONTROL Channel]**
   * Insira a personalização de string para um **[!UICONTROL Channel]** para incluir vídeos de um Canal no Stream.
   * Por exemplo, se o URL do feed de Canal que você deseja inserir for `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, basta inserir `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Insira a string personalizada para um **[!UICONTROL Playlist]** para incluir vídeos de uma lista de reprodução no Stream.
   * Por exemplo, se o URL do feed da Lista de reprodução que você deseja inserir for `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, basta inserir `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se estiver definido como:
   * **[!UICONTROL Enabled]**, Livefyre adiciona os primeiros 15 itens de conteúdo em seu feed ao fluxo, independentemente da data da publicação.
   * **[!UICONTROL Disabled]**, Livefyre adiciona os primeiros 15 itens de conteúdo em seu feed ao fluxo com uma data de publicação que é a mesma data de criação da regra de fluxo ou posterior.

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
