---
description: Adicione o sinalizador userprivacyoptout à página para permitir que um
  visitante do site opte por não participar desse rastreamento.
seo-description: Adicione o sinalizador userprivacyoptout à página para permitir que
  um visitante do site opte por não participar desse rastreamento.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyoptout{#userprivacyoptout}

Adicione `userPrivacyOptOut` o sinalizador à página para permitir que um visitante do site opte por não participar desse rastreamento.

O Livefyre fornece eventos javascript para rastrear a atividade do usuário em seus Aplicativos do Livefyre.

Se você incorporar Aplicativos do Livefyre e um visitante não aprovar o rastreamento, você poderá configurar dinamicamente o Livefyre para desativar a funcionalidade para garantir a privacidade do visitante.

Quando configurado, o Livefyre:

* Desativar o suporte a autenticação em Aplicativos.
* Desativar a geração de Livecount e event
* Excluir cookies existentes criados por qualquer aplicativo que esteja na página
* Mídia de proxy com imagens de domínios de terceiros para impedir que terceiros criem cookies
* Habilitar click-through de máscara de vídeo para vídeos de terceiros que exigem um clique adicional para visualizar

## Configurar uma página para recusar

Integrações que incorporam aplicativos do Livefyre podem configurar o Livefyre quando um visitante do site não concedeu consentimento usando uma única variável javascript.

Instruções:

1. Adicione `userPrivacyOptOut` o sinalizador à página antes do `Livefyre.js` javascript:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Adicione `Livefyre.js` à página em qualquer lugar depois `userPrivacyOptOut`.

   Os aplicativos do Livefyre instanciam com as configurações de privacidade elevadas.

   >[!NOTE]
   >
   >Não altere o valor de `userPrivacyOptOut` uma vez que os Aplicativos do Livefyre carregaram.

Certifique-se de que seu fluxo de trabalho de consentimento define o `userPrivacyOptOut` verdadeiro se um visitante do site optar por recusar.
