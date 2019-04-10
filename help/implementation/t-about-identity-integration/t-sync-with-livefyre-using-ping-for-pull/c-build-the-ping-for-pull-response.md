---
description: Crie a resposta Ping para extrair para transmitir informações atualizadas
  do usuário para o Livefyre.
seo-description: Crie a resposta Ping para extrair para transmitir informações atualizadas
  do usuário para o Livefyre.
seo-title: Criar o ping para resposta extraída
solution: Experience Manager
title: Criar o ping para resposta extraída
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar o ping para resposta extraída{#build-the-ping-for-pull-response}

Crie a resposta Ping para extrair para transmitir informações atualizadas do usuário para o Livefyre.

| Tipo | Propriedade | Descrição |
|--- |--- |--- |
| String *obrigatória* | id | A ID do usuário do usuário no seu sistema de perfil. Isso deve ser exclusivo em todos os usuários na rede e nunca deve ser alterado. |
| String *obrigatória* | display_ name | O nome de exibição do usuário. Isso será renderizado com conteúdo do Livefyre publicado pelo usuário. |
| Objeto *opcional, mas recomendado* | name | Sequências de caracteres para definir os nomes formatados, o primeiro, o meio e o sobrenome do usuário. |
| Sequência *opcional, mas recomendada* | email | Endereço de email do usuário. Usado para enviar notificações por e-mail. |
| Sequência *opcional, mas recomendada* | image_ url | URL para um avatar para ser exibido para o usuário. O Livefyre dimensiona imagens carregadas para 100 × 100, 75 × 75 ou 50 × 50 pixels, conforme apropriado. Para obter melhores resultados, os usuários devem carregar uma imagem quadrada, a 100 × 100 pixels. Para garantir que a imagem de avatar seja atualizada no Livefyre, modifique a imagem_ url para cada atualização de imagem, de modo que Ping para extrair detecta que a imagem foi alterada. Por exemplo, anexe um carimbo de data e hora ao nome do arquivo ou incremente a imagem. Observação: Todos os urls devem ser totalmente qualificados e acessíveis. |
| Sequência *opcional, mas recomendada* | profile_ url | URL para a página de perfil do usuário no site. |
| Sequência *opcional, mas recomendada* | settings_ url | URL para uma página em que os usuários podem configurar as configurações de perfil do usuário para o site. |
| Matriz *opcional, mas recomendada* | tags | Usado para atribuir usuários a grupos de usuários. As tags podem incluir 1-63 caracteres alfanuméricos e sublinhados. |
| *Booliano opcional, mas recomendado* | autofollow_ conversations | Define se um usuário deseja seguir automaticamente uma coleção depois de postá-la. Ao seguir uma Coleção, os usuários recebem notificações por email quando outros usuários participam. Pode ser verdadeiro ou falso. Assume como padrão o padrão. |
| Objeto *opcional, mas recomendado* | email_ notificações | Define a frequência de notificações por email do Livefyre disponíveis. Diferentes frequências podem ser definidas para cada tipo de notificação. Por padrão, nenhuma notificação será enviada. <br><ul><li> imediatamente emite notificações imediatamente após o evento listado. </li><li>frequentemente emite notificações em lotes. </li><li> nunca enviará a notificação por e-mail para a atividade. </li><li>*comentários*: Define quando as notificações são enviadas quando outros usuários postam conteúdo em Coleções que este usuário está seguindo. </li><li>*respostas*: Define quando as notificações são enviadas quando outro usuário responde ao conteúdo do usuário.</li><li>*curtir*: Define quando as notificações são enviadas quando outro usuário gosta do conteúdo deste usuário.</li><li>*moderador_ comentários*: Define quando as notificações são enviadas a moderadores quando os usuários postam conteúdo em qualquer coleção na rede.</li><li>*moderator_flags*: Defines when notifications are sent to moderators when other users flag content in any Collection in the Network.</li></ul> |
| Sequência *opcional* | localização | Um local enviado pelo usuário. |
| Sequência *opcional* | bio | Uma autobiografia enviada pelo usuário. |
| *Matriz opcional* | sites | Uma matriz de sites enviados pelo usuário. Máx. = 2. |
| Objeto *opcional* | display_ rules | Define quais propriedades do perfil são publicamente visíveis para outros usuários. Cada parâmetro disponível apresenta verdadeiro ou falso entrada booleana. Parâmetros disponíveis: <br><ul><li>bio </li><li> localização</li><li>  gênero </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| *Booliano opcional* | moderador | Define se o usuário tem privilégios de moderador na rede. |
| *Booliano opcional* | registatar_ disabled | Define se você deseja desabilitar o uso do Livefyre de um registro se nenhum image_ url for fornecido. |

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
