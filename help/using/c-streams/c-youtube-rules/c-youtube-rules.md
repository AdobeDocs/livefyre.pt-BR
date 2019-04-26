---
description: Você pode criar regras de fluxo que puxam conteúdo de regras do youtube.
seo-description: Você pode criar regras de fluxo que puxam conteúdo de regras do youtube.
seo-title: Regras do youtube
solution: Experience Manager
title: Regras do youtube
uuid: ec 6 a 3780-7119-45 c 3-8 ab 2-fb 0 f 9803 d 161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# Regras do youtube {#youtube-rules}

Você pode criar regras de fluxo que puxam conteúdo de regras do youtube.

Crie regras do youtube com base em Usuário, Canal ou Lista de reprodução.

Para criar regras do youtube para extrair conteúdo do youtube no aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL User]**
   * Insira a string personalizada **[!UICONTROL User]** para incluir vídeos do usuário no Stream.
   * Por exemplo, se o URL do feed do usuário que você deseja inserir for `https://www.youtube.com/user/livefyresupport`, basta inserir `livefyresupport`.

* **[!UICONTROL Channel]**
   * Insira a string personalizada **[!UICONTROL Channel]** para incluir vídeos de um Canal no Stream.
   * Por exemplo, se o URL do feed de canal que você deseja inserir for `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`, basta inserir `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Insira a string personalizada para **[!UICONTROL Playlist]** incluir vídeos de uma Lista de reprodução no Stream.
   * Por exemplo, se o URL do feed da Lista de reprodução que você deseja inserir for `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`, basta inserir `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Se isso for definido como:
   * **[!UICONTROL Enabled]**, o Livefyre adiciona os primeiros 15 itens de conteúdo do feed ao stream, independentemente da data de publicação.
   * **[!UICONTROL Disabled]**, o Livefyre adiciona os primeiros 15 itens de conteúdo no feed ao stream com uma data de publicação que é igual à data de criação da regra de fluxo ou posterior.

Para opções adicionais de regras de Fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
