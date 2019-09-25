---
description: Adicione o sinalizador userPrivacyOptOut à página para permitir que um visitante do site exclua esse rastreamento.
seo-description: Adicione o sinalizador userPrivacyOptOut à página para permitir que um visitante do site exclua esse rastreamento.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

Adicione o sinalizador `userPrivacyOptOut` à página para permitir que um visitante do site desative esse rastreamento.

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário nos aplicativos Livefyre.

Se você incorporar aplicativos Livefyre e um visitante não consentir no rastreamento, poderá configurar dinamicamente o Livefyre para desativar a funcionalidade para garantir a privacidade do visitante.

Quando configurado, o Livefyre:

* Desative o suporte de autenticação em Aplicativos.
* Desabilitar a contagem de tempo e geração de eventos
* Excluir cookies existentes criados por qualquer aplicativo que esteja na página
* Mídia proxy com imagens de domínios de terceiros para impedir que terceiros criem cookies
* Ativar o click-through da máscara de vídeo para vídeos de terceiros que exigem um clique adicional para visualização

## Configurar uma página para opção de não participação

As integrações que incorporam aplicativos Livefyre podem configurar o Livefyre quando um visitante do site não tiver concedido consentimento usando uma única variável JavaScript.

Instruções:

1. Adicione o sinalizador `userPrivacyOptOut` à página antes do `Livefyre.js` JavaScript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Adicione `Livefyre.js` à página em qualquer lugar depois `userPrivacyOptOut`.

   Os aplicativos Livefyre são instanciados com as configurações de privacidade elevadas.

   >[!NOTE]
   >
   >Não altere o valor de `userPrivacyOptOut` uma vez que os aplicativos Livefyre tenham sido carregados.

Certifique-se de que seu fluxo de trabalho de consentimento defina o `userPrivacyOptOut` como verdadeiro se um visitante do site optar por recusar.
