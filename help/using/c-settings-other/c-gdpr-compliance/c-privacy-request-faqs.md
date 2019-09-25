---
description: Respostas às Perguntas frequentes sobre as Solicitações de privacidade Prontas para RGPD.
seo-description: Respostas às Perguntas frequentes sobre as Solicitações de privacidade Prontas para RGPD.
seo-title: Perguntas frequentes sobre a solicitação de privacidade
solution: Experience Manager
title: Perguntas frequentes sobre a solicitação de privacidade
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Perguntas frequentes sobre a solicitação de privacidade{#privacy-request-faqs}

Respostas às Perguntas frequentes sobre as Solicitações de privacidade Prontas para RGPD.

* **Como os visitantes do site podem optar por não ser rastreados em um site que usa aplicativos Livefyre?** Quando um visitante do site optar por não participar, a implementação do cliente deve indicar ao Livefyre que o usuário optou por não participar antes de instanciar um aplicativo. Livefyre criou uma maneira de fazer isso com a opção JavaScript, `userPrivacyOptOut`. Para obter mais informações sobre como usar `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando o sinalizador `userPrivacyOptOut` estiver definido como true, quaisquer Aplicativos na página não transmitirão dados aos servidores Livefyre usando cookies ou outro método. O Livefyre então não atualizará o armazenamento local com dados que poderiam ser usados para rastrear os visitantes do site. Se uma fonte não suportar um proxy, o Livefyre exibe uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa fonte.

   Se você usar a Livefyre Identity, os usuários podem optar por excluir seus perfis ou criar um relatório de dados rastreados para sua conta de usuário.

* **Como impedir a coleta de conteúdo futuro de um visitante do site que tenha optado por não participar?** Use `userPrivacyOptOut` `livefyre.js` em uma página da Web que use aplicativos Livefyre. Para obter mais informações, consulte `userPrivacyOptOut`userPrivacyOptOut [](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Como faço para gerar um relatório e excluir os dados para Usuários do aplicativo ou proprietários de contas sociais?** Solicitações [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacidade para gerar um relatório e excluir dados do usuário dos Aplicativos.

* **Como remover todo o conteúdo de um visitante?** O Livefyre não mantém informações persistentes sobre os visitantes do site, exceto na forma de cookies para identificá-los exclusivamente para os recursos do LiveCount. O Livecount é uma contagem transitória e em tempo real de visitantes no site. Nenhum histórico é retido depois que o visitante sai ou apaga os cookies.

   Crie uma Solicitação [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacidade para excluir a conta. O Livefyre exclui ou torna anônimo o perfil do usuário e quaisquer registros associados.

* **Como faço para remover o conteúdo de um usuário registrado?** Crie uma solicitação [de](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) privacidade para excluir a conta. O perfil do usuário e quaisquer registros associados serão completamente destruídos.

   >[!NOTE]
   >
   >Esta ação não pode ser desfeita.

* **Como produzir um relatório de dados rastreados de um funcionário atual ou anterior?** [Visualize um Relatório](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) de privacidade para gerar um relatório de dados rastreados para uma conta de usuário.

* **O Livefyre Social Stream é compatível?** Quando um usuário exclui uma publicação ou tweet de sua rede social, em 24 horas o conteúdo também é excluído de todas as fontes no Livefyre. Isso se aplica ao Twitter e Facebook.

