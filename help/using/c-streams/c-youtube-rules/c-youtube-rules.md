---
description: Você pode criar regras de fluxo que extraem conteúdo das regras do YouTube.
seo-description: Você pode criar regras de fluxo que extraem conteúdo das regras do YouTube.
seo-title: Regras do YouTube
solution: Experience Manager
title: Regras do YouTube
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Regras do YouTube {#youtube-rules}

Você pode criar regras de fluxo que extraem conteúdo das regras do YouTube.

Crie regras do YouTube com base em Usuário, Canal ou Lista de Reprodução.

Para criar regras do YouTube para inserir conteúdo do YouTube no aplicativo ou na pasta, é possível filtrar por:

* **[!UICONTROL User]**
   * Digite a sequência vanity de **[!UICONTROL User]** para incluir vídeos do Usuário no Fluxo.
   * Por exemplo, se o URL do feed do Usuário que você deseja inserir for `https://www.youtube.com/user/livefyresupport`, basta inserir `livefyresupport`.

* **[!UICONTROL Channel]**
   * Digite a string vanity de **[!UICONTROL Channel]** para incluir vídeos de um Canal no Stream.
   * Por exemplo, se o URL do feed do Canal que você deseja inserir for `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, basta digitar `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Digite a string vanity de **[!UICONTROL Playlist]** para incluir vídeos de uma lista de reprodução no Stream.
   * Por exemplo, se o URL do feed da lista de reprodução que você deseja inserir for `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, basta inserir `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se estiver definido como:
   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 15 itens de conteúdo em seu feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 15 itens de conteúdo no feed ao stream com uma data de publicação que é a mesma que a data de criação da regra de fluxo ou posterior.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
