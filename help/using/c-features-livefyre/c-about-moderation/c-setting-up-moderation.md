---
description: Use a guia Moderação para definir regras de pré-moderação para conteúdo recebido, incluindo listas de profanidade, regras de sinalizador e endereços IP proibidos.
seo-description: Use a guia Moderação para definir regras de pré-moderação para conteúdo recebido, incluindo listas de profanidade, regras de sinalizador e endereços IP proibidos.
seo-title: Configuração da moderação
solution: Experience Manager
title: Configuração da moderação
uuid: 0ec53fdb-08c2-4058-88cb-2f6f4b56a95b
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---


# Configuração da moderação{#setting-up-moderation}

Use a guia Moderação para definir regras de pré-moderação para conteúdo recebido, incluindo listas de profanidade, regras de sinalizador e endereços IP proibidos.

## Como a moderação funciona {#section_kyf_gvc_t1b}

É possível moderar o conteúdo das seguintes maneiras:

* Pré-moderar automaticamente o conteúdo para filtrar o conteúdo indesejado com base nas regras que você configurou antes de publicar o conteúdo.
* Exclua ou aprove manualmente o conteúdo que foi sinalizado usando a pré-moderação automática usando o ModQ ou o Conteúdo do aplicativo na Biblioteca.
* Identifique os visitantes do site que publicam repetidamente conteúdo ofensivo para impedir sua publicação, proibindo usuários específicos do Livefyre, usuários sociais ou endereços IP.
* Identifique pessoas e conteúdo que podem sempre ser exibidos permitindo a lista de usuários ou desativando filtros para fluxos, sites ou redes específicos.

Você pode pré-moderar automaticamente o conteúdo das seguintes maneiras:

* Configure regras para sinalizar automaticamente certos tipos de conteúdo:

   * Configurar regras de sinalização para conteúdo que é sinalizado pelo sinalizador de visitantes do site usando **[!UICONTROL Settings > Moderation > Rules]**
   * Configure regras SAFE usando **[!UICONTROL Settings > Moderation > Rules]**
   * Bloquear usuários específicos do Twitter usando **[!UICONTROL Settings > Streams]**
   * Proibir endereços IP usando **[!UICONTROL Settings > Bans]**
   * Proibir regiões IP por código de país por solicitação. O conteúdo proibido será marcado como SPAM.

* Crie uma lista de palavras que você considera profanidade na Lista Profanity em **[!UICONTROL Settings > Moderation > Rules]** para sua Rede ou Site.
* Permitir que usuários da lista (sempre permitir que o conteúdo desses usuários seja exibido) usando ou desativando filtros para fluxos, sites ou redes específicos.

Depois de configurar suas listas de profanidade, filtros SAFE e regras, você pode escolher pré-moderar o conteúdo e aplicar os filtros SAFE em fluxos. Para obter mais informações, consulte [Opções de regras de fluxo para todas as regras de fluxo](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre marca o conteúdo como **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]** etc. dependendo de onde o conteúdo vem, de onde ele será publicado e de quais regras você configurou no sistema. A tabela a seguir descreve as ações que Livefyre toma, dependendo desses fatores, em detalhes.

## Como a moderação funciona

| O conteúdo vem de: | Enviando conteúdo para: | Status de aprovação |
|--- |--- |--- |
| Biblioteca | Aplicativo | Conteúdo aprovado |
| Pesquisa social | Aplicativo | Conteúdo aprovado |
| Regra de fluxo | Aplicativo | O conteúdo está marcado como lixo eletrônico pelo filtro SAFE? <br><ul><li>Não - Fluxo de trabalho de moderação de fluxo para aplicativo</li><li>Sim - Conteúdo Tracejado</li></ul> |
| Biblioteca | Pasta | Sem status (na pasta, não publicado, não arrastado) |
| Pesquisa social | Pasta | Sem status (na pasta, não publicado, não arrastado) |
| Regra de fluxo | Pasta | O conteúdo está marcado como lixo eletrônico pelo filtro SAFE? <br><ul><li>Não - Sem status (na pasta, não publicado, não arrastado)</li><li>Sim - Conteúdo Tracejado</li></ul> |
| Post do aplicativo | Aplicativo | O conteúdo está marcado como lixo eletrônico pelo filtro SAFE? <br><ul><li>Não - Fluxo de trabalho de moderação pós-aplicativo</li><li>Sim - Conteúdo Tracejado</li></ul> |

## Fluxo de trabalho de moderação de fluxo para aplicativo {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Antes que o conteúdo de um fluxo seja publicado em um aplicativo, o Livefyre realiza as seguintes verificações para determinar o que fazer com o conteúdo:

1. Se SAFE sinalizar o conteúdo como lixo eletrônico ou queda, o Livefyre trava o conteúdo.
1. Se SAFE não sinalizar o conteúdo como lixo eletrônico, Livefyre verifica se a pré-moderação está ativada.
1. Se a pré-moderação estiver ativada, o Livefyre marca o conteúdo como pendente.
1. Se você configurar as regras do ModQ, o Livefyre enviará o conteúdo para o ModQ.
1. Se a pré-moderação não estiver ativada, o Livefyre verifica se o SAFE sinalizou o conteúdo.
1. Se o SAFE sinalizou o conteúdo, o Livefyre aprova o conteúdo e publica-o no aplicativo.
1. Se SAFE sinaliza o conteúdo e você não configurou regras SAFE, o Livefyre aprova o conteúdo e publica o conteúdo no aplicativo.
1. Se SAFE sinalizar o conteúdo e você configurar regras SAFE, o Livefyre verificará se você configurou regras SAFE para o Stream.
1. Se você configurar regras SAFE para o fluxo, o Livefyre aprova o conteúdo e publica o conteúdo no aplicativo. Se você não configurou as regras SAFE para o fluxo, o Livefyre usa as regras SAFE de moderação para determinar como lidar com o conteúdo (enviar para ModQ, lixo, etc.).

## Fluxo de trabalho de moderação pós-aplicativo {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Antes que o conteúdo de uma publicação do aplicativo seja publicado em um aplicativo, o Livefyre realiza as seguintes verificações para determinar o que fazer com o conteúdo:

1. Se o filtro SAFE sinalizar o conteúdo como suspenso, o Livefyre soltará o conteúdo.
1. Se SAFE não sinalizar o conteúdo como queda, Livefyre verifica se a pré-moderação está ativada. Se a pré-moderação estiver ativada, o Livefyre marca o conteúdo como pendente. Se você configurar as regras do ModQ, o Livefyre enviará o conteúdo para o ModQ como pendente. Caso contrário, o conteúdo permanece em um status pendente no Conteúdo do aplicativo na Biblioteca.
1. Se a pré-moderação não estiver ativada, o Livefyre verifica se o SAFE sinalizou o conteúdo. Caso contrário, o Livefyre aprova o conteúdo e o publica no aplicativo.
1. Se o SAFE sinaliza o conteúdo e você configura regras SAFE, o Livefyre usa a regra SAFE para determinar como lidar com o conteúdo (enviar para ModQ, lixo, etc.). Se SAFE sinaliza o conteúdo e você não configurou regras SAFE, o Livefyre aprova o conteúdo e publica o conteúdo no aplicativo.

## Filtros em massa {#section_lyk_ktx_vy}

O Filtro em massa procura conteúdo repetitivo publicado em todas as redes Livefyre em um curto período de tempo. Se detectado, esse conteúdo é sinalizado como em massa e depois descartado por padrão. Embora o conteúdo em massa possa ser gerado pelo usuário (como &quot;Touchdown!&quot;) publicado repetidamente em um bate-papo durante um jogo popular de futebol), a maioria se origina de campanhas de spam. Esse filtro não depende da linguagem e funciona com qualquer idioma. Para personalizar o filtro em massa, entre em contato com o suporte do Livefyre.

## Regras {#section_gqz_ksk_f1b}

Use a seção Regras para criar regras de pré-moderação, com base em sinalizadores SAFE e aplicados pelo usuário. Esse painel oferta dois tipos de regras:

* **[!UICONTROL Flag Rules:]** especifique uma ação que deve ser executada em um comentário sinalizado por usuários um número definido de vezes.
* **[!UICONTROL SAFE Rules:]**combina sinalizadores SAFE com ações para executar o conteúdo sinalizado.

Para criar Regras de sinalização, selecione o sinalizador (Ofensivo, Sem tópico, Discordar ou Spam), digite o número de vezes que ele deve ser aplicado a um conteúdo e selecione a ação a ser executada. É possível definir uma Regra de Sinalizador para cada opção de sinalizador (Ofensivo, Desativado, Discordo ou Spam).

Você pode criar regras nos níveis Rede, Site e Stream. As regras de nível do site herdam as regras de rede, a menos que você configure as regras do Site de forma diferente. As regras de fluxo herdam as regras do Site, a menos que você as configure de forma diferente.

Ações disponíveis:

* **[!UICONTROL Trash it:]**envia o comentário sinalizado para o lixo.
* **[!UICONTROL Bozo it:]** oculta o comentário sinalizado de todos os usuários, exceto seu autor, para quem ele permanece visível.
* **[!UICONTROL Pending:]** define o conteúdo como pendente. Se você definir Premoderation como ON em **[!UICONTROL Settings > ModQ]**, ele estará no ModQ. Caso contrário, estará somente no Conteúdo do aplicativo.

>[!NOTE]
>
>Livefyre recomenda que você crie regras para comentários do Bozo que são marcados como Spam ou Ofensivo por cinco usuários.

## Moderação Recommendations {#section_ec3_vr3_2cb}

Você pode usar as recomendações de moderação para ajudar a determinar como moderar o conteúdo publicado por visitantes do site nos aplicativos Livefyre. O Indicador de recomendação de moderação recomenda quando é provável que um conteúdo seja descartado, com base em quais ações você tomou anteriormente em conteúdo semelhante. Para usar o Recommendations de moderação:

1. Ative a funcionalidade de Moderação do Recommendations entrando em contato com o profissional de suporte do Adobe Livefyre.
1. Configure as recomendações de moderação nas Configurações de rede.

   Configure as recomendações de moderação usando a configuração **[!UICONTROL Livefyre Recommends Trash]** em **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Configure uma regra SAFE para informar ao Livefyre o que fazer com o conteúdo que a recomendação de moderação identifica como conteúdo que provavelmente será descartado. Para obter mais informações sobre como configurar uma regra SAFE para a opção **[!UICONTROL Livefyre Recommends Trash]**, consulte [Moderação](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Use o **[!UICONTROL Moderation Recommendation Indicator]** no ModQ ou no Conteúdo do aplicativo para filtrar o conteúdo que a recomendação de moderação identifica como susceptível de ser arrastado.

   No ModQ, o indicador tem a seguinte aparência:  ![](assets/mod_reco1.png)

   Para obter mais informações sobre como usar o Recommendations de moderação para moderar o conteúdo no ModQ, consulte [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   No conteúdo do aplicativo, as recomendações de moderação são as seguintes:  ![](assets/modreco3.png)

   Para obter mais informações sobre como usar o Recommendations de moderação no conteúdo do aplicativo, consulte [Moderar conteúdo usando conteúdo do aplicativo](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
