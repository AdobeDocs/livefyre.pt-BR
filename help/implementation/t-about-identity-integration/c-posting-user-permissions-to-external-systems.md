---
description: O Livefyre usa uma interface PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.
seo-description: O Livefyre usa uma interface PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.
seo-title: Contabilização de permissões de usuário para sistemas externos (opcional)
solution: Experience Manager
title: Contabilização de permissões de usuário para sistemas externos (opcional)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---


# Contabilização de permissões de usuário para sistemas externos (opcional){#posting-user-permissions-to-external-systems-optional}

O Livefyre usa uma interface PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.

## Tipos de usuários no Livefyre Studio

| Tipo de usuário | Descrição |
|--- |--- |
| proprietário | Esse usuário é proprietário, pode moderar o conteúdo e atribuir novos moderadores. |
| admin | Esse usuário é um moderador e pode moderar o conteúdo. |
| membro | Este usuário está na lista de permissões. O conteúdo postado não passa por filtros de spam ou profanidade, e não requer aprovação em fluxos pré-moderados. |
| none | Este usuário é padrão e não tem permissões especiais. |
| difusão | Este usuário foi proibido de participar de qualquer conversa. |

Para postar permissões de usuário em sistemas externos, você deve registrar um URL que receba dados de permissões como solicitações POST.

Por exemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parâmetro | Descrição |
|--- |--- |
| networkName | Seu Livefyre forneceu o nome da rede. |
| token | Token de sistema válido. |
| url | URL para registro. |

O URL registrado deve aceitar POSTs com os seguintes dados como tipo de conteúdo: application/x-www-form-urlencoded.

| Parâmetro | Descrição |
|--- |--- |
| jid | JID do usuário cuja afiliação foi alterada. Um JID é uma string do formulário `user_id@network`. |
| filiação | Nome das permissões atribuídas, que devem ser uma das seguintes:  `{admin | member | none | outcast | owner}` |

Para obter informações adicionais sobre como atualizar as configurações de afiliação do usuário, consulte a Referência [da API](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)Adicionar afiliação de usuário.
