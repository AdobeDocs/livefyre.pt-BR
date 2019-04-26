---
description: Respostas a Perguntas frequentes (faqs) sobre Solicitações de privacidade
  do RGPD Ready.
seo-description: Respostas a Perguntas frequentes (faqs) sobre Solicitações de privacidade
  do RGPD Ready.
seo-title: Perguntas frequentes sobre solicitação de privacidade
solution: Experience Manager
title: Perguntas frequentes sobre solicitação de privacidade
uuid: 0 cd 6 f 0 d 2-504 d -46 e 9-ac 46-070536 cda 086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Perguntas frequentes sobre solicitação de privacidade{#privacy-request-faqs}

Respostas a Perguntas frequentes (faqs) sobre Solicitações de privacidade do RGPD Ready.

* **Como os visitantes do site podem recusar serem rastreados em um site que usa aplicativos do Livefyre?** Quando um visitante do site recusa, a implementação do cliente deve indicar ao Livefyre que o usuário não optou antes de instanciar um aplicativo. Livefyre has created a way to do this with the JavaScript option, `userPrivacyOptOut`. Para saber mais sobre como usar `userPrivacyOptOut`, consulte [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Quando `userPrivacyOptOut` o sinalizador estiver definido como true, todos os aplicativos na página não transmitirão dados aos servidores do Livefyre usando cookies ou outro método. O Livefyre não atualizará o armazenamento local com dados que possam ser usados para rastrear visitantes do site. Se uma fonte não for compatível com um proxy, o Livefyre exibirá uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa origem.

   Se você usar a identidade do Livefyre, os usuários poderão optar por excluir o perfil ou criar um relatório de dados acompanhados para sua conta de usuário.

* **Como evitar coletar conteúdo futuro de um visitante do site que não tenha optado?** Use `userPrivacyOptOut` em `livefyre.js` uma página da Web que usa aplicativos do Livefyre. Para obter mais informações, `userPrivacyOptOut`consulte [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Como posso gerar um relatório e excluir os dados dos Usuários do aplicativo ou proprietários de contas sociais?**[Solicitações de privacidade](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para gerar um relatório e excluir dados do usuário dos Aplicativos.

* **Como posso remover todo o conteúdo de um visitante?** O Livefyre não mantém informações persistentes sobre os visitantes do site, exceto na forma de cookies para identificação exclusiva dos recursos do Livecount. Livecount é uma contagem de visitantes transientos e em tempo real no site. Nenhum histórico é retido depois que o visitante deixa ou limpa os cookies.

   Crie uma [solicitação de privacidade](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para excluir a conta. Livefyre exclui ou torna o perfil do usuário e qualquer registro associado anônimo.

* **Como remover conteúdo de um usuário registrado?** Crie uma [Solicitação de privacidade](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) para excluir a conta. O perfil do usuário e os registros associados serão completamente destruídos.

   >[!NOTE]
   >
   >Esta ação não pode ser desfeita.

* **Como posso produzir um relatório de dados acompanhados de um funcionário atual ou anterior?**[Visualize um Relatório](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) de privacidade para gerar um relatório de dados rastreados para uma conta de usuário.

* **O fluxo social do Livefyre é compatível?** Quando um usuário exclui uma publicação ou tweet de sua rede social, em 24 horas, o conteúdo também é excluído de todas as fontes no Livefyre. Isso se aplica ao Twitter e ao Facebook.

