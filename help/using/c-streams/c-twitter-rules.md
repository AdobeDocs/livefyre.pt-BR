---
description: Você pode criar Regras de fluxo que obtêm conteúdo do Twitter.
title: Regras do twitter
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Regras do twitter{#twitter-rules}

Você pode criar Regras de fluxo que obtêm conteúdo do Twitter.

Crie regras do Twitter com base em hashtags, palavras-chave, @menções ou autor.

Adicionar **[!UICONTROL Words]** e **[!UICONTROL Username]** para sua regra retornará conteúdo que inclui ambas as entradas.

>[!NOTE]
>
>A Livefyre adere às diretrizes de exibição da Twitter e os clientes são responsáveis por seguir essas diretrizes também. Para obter mais informações, consulte a documentação da Twitter sobre seus [Requisitos de exibição](https://dev.twitter.com/terms/display-requirements).

Para criar Regras do Twitter para extrair conteúdo dos feeds do Twitter para seu aplicativo ou Pasta, você pode filtrar por:

* **[!UICONTROL Keywords]**
   * Insira **[!UICONTROL Keywords]** para ser incluído ou excluído do fluxo do Twitter. A especificação de valores para os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** retornará Tweets que contêm o primeiro e não contêm o segundo. Vários valores para um único campo podem ser inseridos e retornarão resultados que contenham qualquer um dos valores. Para usar o operador booleano AND para procurar por tweets com duas ou mais palavras, use dois &quot;E&quot; comercial (*&amp;*) para separar as duas palavras.
   * Por exemplo, inserir **[!UICONTROL Contains any of these words]** palavras-chave Giants, Posey e **[!UICONTROL Does not contain any of these words]** palavra-chave Dodger retornará todos os Tweets que incluem a palavra *Giants* ou *Posey* e não incluirá a palavra *Dodger*.
Para procurar por Tweets que incluem as palavras *Giants* e *Posey*, digite &quot;Giants &amp; Posey&quot;. Esse recurso é compatível somente para os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** nas regras do Twitter.

* **[!UICONTROL Hashtags]**.
   * Insira **[!UICONTROL Hashtags]** para ser incluído ou excluído do fluxo do Twitter. A especificação de valores para os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** retornará Tweets que contêm hashtags no primeiro campo e não contêm hashtags no segundo. É possível inserir vários valores para um único campo. O fluxo retorna resultados que contêm qualquer um dos valores.

* **[!UICONTROL Usernames]**
   * Insira **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** para entrar no fluxo ou excluir do fluxo. Use as caixas de seleção para definir se **[!UICONTROL Retweets]** ou **[!UICONTROL replies]** de autores selecionados também devem ser incluídos.

   >[!NOTE]
   >
   >Você pode incluir ou excluir autores; não é possível combinar esses dois campos em uma única Regra do Twitter.

* **[!UICONTROL Minimum number of followers.]** Selecione o número mínimo de seguidores que o usuário deve ter para obter informações de suas publicações.
* **[!UICONTROL Location]**

   * Insira o local (cidade, código postal, endereço ou geocódigo no formato de latitude/longitude comum (+/- 90, +/- 180) ). Comece digitando um local para exibir um menu suspenso com sugestões. Selecione um local no menu suspenso. O mapa exibe um pino desse local. Ajuste o controle deslizante para selecionar um raio de uma milha a 25 milhas para cada local. Se você não escolher um raio, o Livefyre escolhe automaticamente um padrão de 8 milhas.
   >[!NOTE]
   >
   >Para ambos os campos, a distância será calculada a partir do centro do local de entrada.

   * Você pode adicionar mais de um local e raio. Você pode excluir um local clicando no X ao lado do nome de um local na caixa.
   * Combine os campos **[!UICONTROL Is near this location]** e **[!UICONTROL Is not near this location]** para extrair conteúdo em locais no campo **[!UICONTROL Is near this location]**, mas não próximo aos locais no campo **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Use Filtros adicionais para refinar ainda mais sua Regra do Twitter. Defina se deseja:
      * Inclua **[!UICONTROL Replies]** nos tweets direcionados (se o fluxo se tornar de alta velocidade, esse recurso será desativado automaticamente).
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Inclua **[!UICONTROL All Content]**, ou **[!UICONTROL Vines Only]**, ou **[!UICONTROL Images Only.]**
      * Inclua somente Tweets que se originam de contas com o **[!UICONTROL Minimum number of followers]** selecionado (qualquer, 100, 500, 1000, 10.000 ou 100.000).

Para obter opções adicionais de Regra de fluxo para todas as regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
