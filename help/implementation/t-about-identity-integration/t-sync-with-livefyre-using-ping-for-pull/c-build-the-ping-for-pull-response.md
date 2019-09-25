---
description: Crie a resposta Ping for Pull para transmitir informações atualizadas do usuário ao Livefyre.
seo-description: Crie a resposta Ping for Pull para transmitir informações atualizadas do usuário ao Livefyre.
seo-title: Criar o Ping para Resposta de Puxo
solution: Experience Manager
title: Criar o Ping para Resposta de Puxo
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Criar o Ping para Resposta de Puxo{#build-the-ping-for-pull-response}

Crie a resposta Ping for Pull para transmitir informações atualizadas do usuário ao Livefyre.

| Tipo | Propriedade | Descrição |
|--- |--- |--- |
| String *necessária* | id | A ID de usuário do usuário em seu sistema de perfil. Isso deve ser exclusivo em todos os usuários da rede e nunca deve ser alterado. |
| String *necessária* | nome_da_exibição | O nome de exibição do usuário. Isso será renderizado com o Livefyre Content publicado pelo usuário. |
| Objeto *opcional, mas recomendado* | name | Strings para definir os nomes formatados do usuário, o primeiro, o meio e os sobrenomes. |
| String *opcional, mas recomendado* | email | Endereço de email do usuário. Usado para enviar notificações por email. |
| String *opcional, mas recomendado* | image_url | URL para um avatar a ser exibido para o usuário. Livefyre dimensiona as imagens carregadas para 100×100, 75×75 ou 50×50 pixels, conforme apropriado. Para obter melhores resultados, os usuários devem carregar uma imagem quadrada, a 100×100 pixels. Para garantir que a imagem de avatar seja atualizada no Livefyre, modifique o image_url para cada atualização de imagem, de modo que Ping for Pull detecte que a imagem foi alterada. Por exemplo, anexe um carimbo de data e hora ao nome do arquivo ou incremente as alterações na imagem. Observação:  Todos os URLs devem ser totalmente qualificados e acessíveis. |
| String *opcional, mas recomendado* | profile_url | URL para a página de perfil do usuário em seu site. |
| String *opcional, mas recomendado* | settings_url | URL para uma página onde os usuários podem definir as configurações de perfil do usuário para seu site. |
| Matriz *opcional, mas recomendado* | específicos | Usado para atribuir usuários a grupos de usuários. As tags podem incluir de 1 a 63 caracteres alfanuméricos e sublinhados. |
| Booliano *opcional, mas recomendado* | autofollow_conversations | Define se um usuário deseja seguir automaticamente uma Coleção após postá-la. Ao seguir uma coleção, os usuários recebem notificações por email quando outros usuários participam. Pode ser verdadeiro ou falso. O padrão é true. |
| Objeto *opcional, mas recomendado* | email_notifications | Define a frequência das notificações por email do Livefyre disponíveis. Podem ser definidas frequências diferentes para cada tipo de notificação. Por padrão, nenhuma notificação será enviada. <br><ul><li> emite notificações imediatamente após o evento listado. </li><li>geralmente emite notificações em lotes. </li><li> nunca enviará uma notificação por email para a atividade. </li><li>*comentários*: Define quando notificações são enviadas quando outros usuários postam conteúdo em Coleções que esse usuário está seguindo. </li><li>*respostas*: Define quando notificações são enviadas quando outro usuário responde ao conteúdo desse usuário.</li><li>*curtidas*: Define quando notificações são enviadas quando outro usuário gosta do conteúdo desse usuário.</li><li>*moderator_comments*: Define quando as notificações são enviadas a moderadores quando os usuários postam conteúdo em qualquer Coleção na Rede.</li><li>*moderator_flags*: Define quando as notificações são enviadas a moderadores quando outros usuários sinalizam o conteúdo em qualquer Coleção na Rede.</li></ul> |
| String *opcional* | localização | Um local enviado pelo usuário. |
| String *opcional* | bio | Uma autobiografia enviada pelo usuário. |
| Matriz *opcional* | sites | Uma matriz de sites enviados pelo usuário. Máx. = 2. |
| Objeto *opcional* | display_rules | Define quais propriedades de perfil são publicamente visíveis para outros usuários. Cada parâmetro disponível leva a entrada Booleana true ou false. Parâmetros disponíveis:  <br><ul><li>bio </li><li> localização</li><li>  gênero </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Booliano *opcional* | moderador | Define se o usuário tem privilégios de moderador na rede. |
| Booliano *opcional* | gravatar_disabled | Define se o uso de um gravatar por Livefyre deve ser desativado se nenhum image_url for fornecido. |

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
