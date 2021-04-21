---
description: Respostas às perguntas frequentes sobre as solicitações de privacidade prontas para GDPR.
title: Perguntas frequentes sobre solicitações de privacidade
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# Perguntas frequentes sobre solicitações de privacidade{#privacy-request-faqs}

Respostas às perguntas frequentes sobre as solicitações de privacidade prontas para GDPR.

* **Como os visitantes do site podem recusar o rastreamento em um site que usa aplicativos do Livefyre?** Quando um visitante do site recusa, a implementação do cliente deve indicar ao Livefyre que o usuário optou por não participar antes de instanciar um aplicativo. Livefyre criou uma maneira de fazer isso com a opção JavaScript, `userPrivacyOptOut`. Para obter mais informações sobre como usar `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando o sinalizador `userPrivacyOptOut` é definido como true, qualquer aplicativo na página não transmitirá dados aos servidores do Livefyre usando cookies ou outro método. O Livefyre então não atualizará o armazenamento local com dados que podem ser usados para rastrear visitantes do site. Se uma fonte não suportar um proxy, o Livefyre exibe uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa fonte.

   Se você usar a Livefyre Identity, os usuários podem optar por excluir o perfil ou criar um relatório de dados rastreados para a conta de usuário.

* **Como impedir a coleta de conteúdo futuro de um visitante do site que optou por não participar?** Use  `userPrivacyOptOut` com  `livefyre.js` em uma página da Web que use aplicativos do Livefyre. Para obter mais informações sobre `userPrivacyOptOut`, consulte [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Como faço para gerar um relatório e excluir os dados de Usuários do aplicativo ou proprietários de contas sociais?** [Solicitações de privacidade ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para gerar um relatório e excluir dados do usuário dos aplicativos.

* **Como remover todo o conteúdo de um visitante?** O Livefyre não mantém informações persistentes sobre visitantes do site, exceto na forma de cookies para identificá-los exclusivamente para os recursos do Livecount. Livecount é uma contagem transitória e em tempo real de visitantes no site. Nenhum histórico é retido depois que o visitante sai ou apaga os cookies.

   Crie um [Solicitações de privacidade](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para excluir a conta. O Livefyre exclui ou torna anônimo o perfil de usuário e quaisquer registros associados.

* **Como remover o conteúdo de um usuário registrado?** Crie uma Solicitação  [de privacidade para ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) excluir a conta. O perfil de usuário e quaisquer registros associados serão completamente destruídos.

   >[!NOTE]
   >
   >Esta ação não pode ser desfeita.

* **Como faço para produzir um relatório de dados rastreado de um funcionário atual ou anterior?** [Exiba um ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) Relatório de privacidade para gerar um relatório de dados rastreados para uma conta de usuário.

* **O Livefyre Social stream é compatível?** Quando um usuário exclui uma publicação ou tweet de sua rede social, em 24 horas o conteúdo também é excluído de todas as fontes no Livefyre. Isso se aplica ao Twitter e ao Facebook.
