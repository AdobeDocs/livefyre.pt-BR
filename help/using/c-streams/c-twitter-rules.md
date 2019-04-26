---
description: Você pode criar regras de fluxo que puxam conteúdo do Twitter.
seo-description: Você pode criar regras de fluxo que puxam conteúdo do Twitter.
seo-title: Regras do Twitter
solution: Experience Manager
title: Regras do Twitter
uuid: a 7 fd 2398-fd 6 b -4 c 24-92 b 2-7471176 d 7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regras do Twitter{#twitter-rules}

Você pode criar regras de fluxo que puxam conteúdo do Twitter.

Crie regras do Twitter com base em hashtags, palavras-chave, @ menções ou autor.

A adição **[!UICONTROL Words]** e a **[!UICONTROL Username]** regra de retorno retornarão conteúdo que inclui ambas as entradas.

>[!NOTE]
>
>O Livefyre acessa as diretrizes de exibição do Twitter, e os clientes são responsáveis por aderir a essas diretrizes. Para obter mais informações, consulte a documentação do Twitter sobre os requisitos [de exibição](https://dev.twitter.com/terms/display-requirements).

Para criar Regras do Twitter para extrair conteúdo de feeds do Twitter em seu aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Keywords]**
   * Digite **[!UICONTROL Keywords]** a ser incluído ou excluído do seu fluxo do Twitter. Especificar valores para os **[!UICONTROL Contains any of these words]** dois **[!UICONTROL Does not contain any of these words]** campos retornará Tweets que contêm o primeiro e não conterão o segundo. Vários valores de um único campo podem ser inseridos e retornarão resultados que contêm qualquer um dos valores. Para usar o operador Booleano E para pesquisar Tweets com duas ou mais palavras neles, use dois (*& &*) para separar as duas palavras.
   * Por exemplo, inserir **[!UICONTROL Contains any of these words]** palavras-chave Giants, Posey e palavra **[!UICONTROL Does not contain any of these words]** -chave Dodger retornará todos os tweets que incluem a palavra *Giants* ou *Posey* e não incluam a palavra *Dodger*.
Para pesquisar Tweets que incluem as palavras *Giants* e *Posey*, digite «Giants & & Posey». Esse recurso é suportado apenas para os **[!UICONTROL Contains any of these words]****[!UICONTROL Does not contain any of these words]** campos e as regras do Twitter.

* **[!UICONTROL Hashtags]**.
   * Digite **[!UICONTROL Hashtags]** a ser incluído ou excluído do seu fluxo do Twitter. Especificar valores para os **[!UICONTROL Contains any of these words]** dois **[!UICONTROL Does not contain any of these words]** campos retornará Tweets que contêm hashtags no primeiro campo e não contêm hashtags no segundo campo. Você pode inserir vários valores para um único campo. O fluxo retorna os resultados que contêm qualquer um dos valores.

* **[!UICONTROL Usernames]**
   * Digite **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** insira o fluxo ou exclua do stream. Use as caixas de seleção para definir se **[!UICONTROL Retweets]****[!UICONTROL replies]** os autores selecionados também devem ser incluídos.
   >[!NOTE]
   >
   >Você pode incluir ou excluir autores; não é possível combinar esses dois campos em uma única Regra do Twitter.

* **[!UICONTROL Minimum number of followers.]** Selecione o número mínimo de seguidores que o usuário deve ter para obter informações de suas postagens.
* **[!UICONTROL Location]**

   * Insira o local (cidade, código postal, endereço ou geocódigo no formato de latitude/longitude comum (+/- 90, +/- 180)). Comece a digitar um local para exibir um menu suspenso com sugestões. Selecione um local no menu suspenso. O mapa exibe um pino desse local. Ajuste o controle deslizante para selecionar um raio de one mm para 25 milhas para cada localização. Se você não escolher um raio, o Livefyre escolhe automaticamente um padrão de oito milhas.
   >[!NOTE]
   >
   >Para ambos os campos, a distância será calculada a partir do centro do local de entrada.

   * Você pode adicionar mais de um local e raio. É possível excluir um local clicando no X ao lado do nome de um local na caixa.
   * Combine os **[!UICONTROL Is near this location]** campos e **[!UICONTROL Is not near this location]** os campos para obter conteúdo dentro de locais no **[!UICONTROL Is near this location]** campo, mas não próximo dos locais no **[!UICONTROL Is not near this location]** campo.


* **[!UICONTROL Additional Filters]**
   * Use Filtros adicionais para refinar ainda mais sua Regra do Twitter. Defina se você irá:
      * Incluir **[!UICONTROL Replies]** aos tweets direcionados (se o stream se tornar maior velocidade, esse recurso será desativado automaticamente.)
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]**ou **[!UICONTROL Images Only.]**
      * Inclua apenas Tweets que se originam de contas com a selecionada **[!UICONTROL Minimum number of followers]** (qualquer, 100, 500, 1000, 10,000 ou 100,000).

Para opções adicionais de regras de Fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
