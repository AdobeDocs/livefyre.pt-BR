---
description: Adicione o sinalizador userPrivacyOptOut à página para permitir que um visitante do site opt out esse rastreamento.
seo-description: Adicione o sinalizador userPrivacyOptOut à página para permitir que um visitante do site opt out esse rastreamento.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

Adicione o sinalizador `userPrivacyOptOut` à página para permitir que um visitante do site opt out desse rastreamento.

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário em seus aplicativos Livefyre.

Se você incorporar aplicativos Livefyre e um visitante não consentir no rastreamento, poderá configurar dinamicamente o Livefyre para desativar a funcionalidade para garantir a privacidade do visitante.

Quando configurado, o Livefyre:

* Desative o suporte de autenticação em Aplicativos.
* Desabilitar a geração de Livecount e evento
* Excluir cookies existentes criados por qualquer aplicativo que esteja na página
* Mídia proxy com imagens de domínios de terceiros para impedir que terceiros criem cookies
* Ative o click-through da máscara de vídeo para vídeos de terceiros que exigem um clique adicional para visualização

## Configurar uma página para opção de não participação

As integrações que incorporam aplicativos Livefyre podem configurar o Livefyre quando um visitante do site não tiver concedido consentimento usando uma única variável JavaScript.

Instruções:

1. Adicione o sinalizador `userPrivacyOptOut` à página antes do JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Adicione `Livefyre.js` à página em qualquer lugar após `userPrivacyOptOut`.

   Os aplicativos Livefyre são instanciados com as configurações de privacidade elevadas.

   >[!NOTE]
   >
   >Não altere o valor de `userPrivacyOptOut` depois que os aplicativos Livefyre forem carregados.

Certifique-se de que seu fluxo de trabalho de consentimento defina `userPrivacyOptOut` como verdadeiro se um visitante do site optar por opt out.
