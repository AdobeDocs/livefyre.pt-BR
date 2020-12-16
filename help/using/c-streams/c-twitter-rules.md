---
description: Você pode criar regras de fluxo que extraem conteúdo do Twitter.
seo-description: Você pode criar regras de fluxo que extraem conteúdo do Twitter.
seo-title: Regras do Twitter
solution: Experience Manager
title: Regras do Twitter
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Regras do Twitter{#twitter-rules}

Você pode criar regras de fluxo que extraem conteúdo do Twitter.

Crie regras do Twitter com base em hashtags, palavras-chave, @menções ou autor.

Adicionar **[!UICONTROL Words]** e **[!UICONTROL Username]** para a sua regra retornará conteúdo que inclui ambas as entradas.

>[!NOTE]
>
>Livefyre segue as diretrizes de exibição do Twitter, e os clientes são responsáveis por seguir essas diretrizes também. Para obter mais informações, consulte a documentação do Twitter em seus [Requisitos de exibição](https://dev.twitter.com/terms/display-requirements).

Para criar Regras do Twitter para inserir conteúdo de feeds do Twitter em seu aplicativo ou pasta, você pode filtrar por:

* **[!UICONTROL Keywords]**
   * Digite **[!UICONTROL Keywords]** para ser incluído ou excluído do seu fluxo do Twitter. A especificação de valores para os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** retornará tweets que contêm o primeiro e não o segundo. Vários valores para um único campo podem ser inseridos e retornarão resultados que contenham qualquer um dos valores. Para usar o operador Booliano E para procurar por tweets com duas ou mais palavras, use dois e-mails (*&amp;*) para separar as duas palavras.
   * Por exemplo, inserir **[!UICONTROL Contains any of these words]** palavras-chave Giants, Posey e **[!UICONTROL Does not contain any of these words]** palavras-chave Dodger retornará todos os Tweets que incluem a palavra *Giants* ou *Posey* e não incluirá a palavra *Dodger*.
Para pesquisar por Tweets que incluem as palavras *Giants* e *Posey*, digite &quot;Giants &amp;&amp; Posey&quot;. Esse recurso é compatível apenas com os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** nas regras do Twitter.

* **[!UICONTROL Hashtags]**.
   * Digite **[!UICONTROL Hashtags]** para ser incluído ou excluído do seu fluxo do Twitter. A especificação de valores para os campos **[!UICONTROL Contains any of these words]** e **[!UICONTROL Does not contain any of these words]** retornará tweets que contêm hashtags no primeiro campo e não contêm hashtags no segundo. É possível inserir vários valores para um único campo. O fluxo retorna resultados que contêm qualquer um dos valores.

* **[!UICONTROL Usernames]**
   * Digite **[!UICONTROL @mentions]** ou **[!UICONTROL authors]** para entrar no fluxo, ou exclua do fluxo. Use as caixas de seleção para definir se **[!UICONTROL Retweets]** ou **[!UICONTROL replies]** de autores selecionados também devem ser incluídos.

   >[!NOTE]
   >
   >Você pode incluir ou excluir autores; não é possível combinar esses dois campos em uma única Regra do Twitter.

* **[!UICONTROL Minimum number of followers.]** Selecione o número de seguidores mínimo que o usuário deve ter para obter informações de suas publicações.
* **[!UICONTROL Location]**

   * Insira o local (cidade, código postal, endereço ou código geográfico no formato de latitude/longitude comum (+/- 90, +/- 180) ). Comece digitando um local para exibir um menu suspenso com sugestões. Selecione um local no menu suspenso. O mapa exibe um pino desse local. Ajuste o controle deslizante para selecionar um raio de 1 milha a 25 milhas para cada local. Se você não escolher um raio, Livefyre escolhe automaticamente um padrão de 8 milhas.
   >[!NOTE]
   >
   >Para ambos os campos, a distância será calculada a partir do centro do local de entrada.

   * É possível adicionar mais de um local e raio. Você pode excluir um local clicando no X ao lado do nome de um local na caixa.
   * Combine os campos **[!UICONTROL Is near this location]** e **[!UICONTROL Is not near this location]** para extrair conteúdo dentro de locais no campo **[!UICONTROL Is near this location]**, mas não perto dos locais no campo **[!UICONTROL Is not near this location]**.


* **[!UICONTROL Additional Filters]**
   * Use Filtros adicionais para refinar ainda mais sua Regra do Twitter. Defina se você irá:
      * Inclua **[!UICONTROL Replies]** nos tweets direcionados (se o fluxo se tornar de alta velocidade, esse recurso será automaticamente desativado).
      * Incluir tweets de **[!UICONTROL Verified Twitter accounts only.]**
      * Incluir **[!UICONTROL All Content]**, ou **[!UICONTROL Vines Only]**, ou **[!UICONTROL Images Only.]**
      * Inclua somente tweets que se originam de contas com o **[!UICONTROL Minimum number of followers]** selecionado (qualquer, 100, 500, 1000, 10.000 ou 100.000).

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
