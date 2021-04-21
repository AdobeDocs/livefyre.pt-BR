---
description: Crie o Ping for Pull response para transmitir informações atualizadas do usuário ao Livefyre.
title: Criar o ping para resposta de pull
exl-id: 81c398fd-2acb-4e39-a2b3-c96921b1192b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Criar o ping para resposta de pull{#build-the-ping-for-pull-response}

Crie o Ping for Pull response para transmitir informações atualizadas do usuário ao Livefyre.

| Tipo | Propriedade | Descrição |
|--- |--- |--- |
| Sequência *necessária* | id | A ID de usuário do usuário em seu sistema de perfil. Isso deve ser exclusivo em todos os usuários da rede e nunca deve ser alterado. |
| Sequência *necessária* | nome_da_exibição | O nome de exibição do usuário. Isso será renderizado com o Livefyre Content publicado pelo usuário. |
| Objeto *opcional, mas recomendado* | name | Cadeias de caracteres para definir o nome, o meio e o sobrenome formatados pelo usuário. |
| Sequência *opcional, mas recomendada* | email | Endereço de email do usuário. Usado para enviar notificações por email. |
| Sequência *opcional, mas recomendada* | image_url | URL para um avatar a ser exibido para o usuário. Livefyre dimensiona imagens enviadas para 100×100, 75×75 ou 50×50 pixels, conforme apropriado. Para melhores resultados, os usuários devem carregar uma imagem quadrada, a 100×100 pixels. Para garantir que a imagem do avatar seja atualizada no Livefyre, modifique o image_url para cada atualização de imagem, de modo que o Ping for Pull detecte que a imagem foi alterada. Por exemplo, anexe um carimbo de data e hora ao nome do arquivo ou incremente as alterações da imagem. Observação:  Todos os URLs devem ser totalmente qualificados e acessíveis. |
| Sequência *opcional, mas recomendada* | profile_url | URL para a página de perfil do usuário em seu site. |
| Sequência *opcional, mas recomendada* | settings_url | URL para uma página em que os usuários podem definir as configurações de perfil do usuário para seu site. |
| Matriz *opcional, mas recomendado* | específicos | Usado para atribuir usuários a grupos de usuários. As tags podem incluir de 1 a 63 caracteres alfanuméricos e sublinhados. |
| Booleano *opcional, mas recomendado* | autofollow_conversations | Define se um usuário deseja seguir automaticamente uma Coleção após publicar nela. Ao seguir uma Coleção, os usuários recebem notificações por email quando outros usuários participam. Pode ser verdadeiro ou falso. O padrão é true. |
| Objeto *opcional, mas recomendado* | email_notifications | Define a frequência das notificações por email disponíveis do Livefyre. Podem ser estabelecidas frequências diferentes para cada tipo de notificação. Por padrão, nenhuma notificação será enviada. <br><ul><li> O emite notificações imediatamente após o evento listado. </li><li>O geralmente emite notificações em lotes. </li><li> nunca enviará uma notificação por email para a atividade. </li><li>*comentários*: Define quando as notificações são enviadas quando outros usuários postam conteúdo em Coleções que este usuário está seguindo. </li><li>*Respostas*: Define quando as notificações são enviadas quando outro usuário responde ao conteúdo deste usuário.</li><li>*curtidas*: Define quando as notificações são enviadas quando outro usuário gosta do conteúdo deste usuário.</li><li>*moderator_comments*: Define quando as notificações são enviadas aos moderadores quando os usuários postam conteúdo em qualquer Coleção na Rede.</li><li>*moderator_flags*: Define quando as notificações são enviadas aos moderadores quando outros usuários sinalizam o conteúdo em qualquer Coleção na Rede.</li></ul> |
| Sequência *opcional* | localização | Um local enviado pelo usuário. |
| Sequência *opcional* | bio | Uma autobiografia enviada pelo usuário. |
| Matriz *opcional* | sites | Uma matriz de sites enviados pelo usuário. Máx. = 2. |
| Objeto *opcional* | display_rules | Define quais propriedades do perfil são publicamente visíveis para outros usuários. Cada parâmetro disponível leva a entrada booleana true ou false. Parâmetros disponíveis:  <br><ul><li>bio </li><li> localização</li><li>  gênero </li><li>nameimage </li><li> url_perfil_remoto</li></ul> |
| Booleano *opcional* | moderador | Define se o usuário tem privilégios de moderador em toda a rede. |
| Booleano *opcional* | gravatar_desativado | Define se o Livefyre deve desativar o uso de um gravatar se nenhum image_url for fornecido. |

## Exemplo de resposta {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
