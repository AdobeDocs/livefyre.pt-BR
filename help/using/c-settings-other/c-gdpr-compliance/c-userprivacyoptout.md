---
description: Adicione o sinalizador userPrivacyOptOut à página para permitir que um visitante do site exclua esse rastreamento.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

Adicione o sinalizador `userPrivacyOptOut` à página para permitir que um visitante do site exclua esse rastreamento.

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário nos aplicativos do Livefyre.

Se você incorporar aplicativos do Livefyre e um visitante não consentir com o rastreamento, é possível configurar dinamicamente o Livefyre para desativar a funcionalidade e garantir a privacidade do visitante.

Quando configurado, o Livefyre:

* Desative o suporte de autenticação em aplicativos.
* Desabilitar Livecount e geração de evento
* Exclua os cookies existentes criados por qualquer aplicativo que esteja na página
* Mídia de proxy com imagens de domínios de terceiros para impedir que terceiros criem cookies
* Ativar click-through de máscara de vídeo para vídeos de terceiros que exigem um clique adicional para visualização

## Configurar uma página para opção de não participação

Integrações que incorporam os aplicativos Livefyre podem configurar o Livefyre quando um visitante do site não tiver consentido usando uma única variável JavaScript.

Instruções:

1. Adicione o sinalizador `userPrivacyOptOut` à página antes do JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Adicione `Livefyre.js` à página em qualquer lugar depois de `userPrivacyOptOut`.

   Os aplicativos Livefyre são instanciados com as configurações de privacidade elevadas.

   >[!NOTE]
   >
   >Não altere o valor de `userPrivacyOptOut` após o carregamento dos aplicativos do Livefyre.

Certifique-se de que o fluxo de trabalho de consentimento defina `userPrivacyOptOut` como true se um visitante do site optar por rejeitar.
