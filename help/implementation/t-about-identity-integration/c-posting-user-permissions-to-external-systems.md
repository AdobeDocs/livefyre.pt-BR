---
description: O Livefyre usa uma interface de PUSH para enviar informações externas
  do sistema sobre alterações nas permissões do usuário.
seo-description: O Livefyre usa uma interface de PUSH para enviar informações externas
  do sistema sobre alterações nas permissões do usuário.
seo-title: Publicar permissões de usuário para sistemas externos (opcional)
solution: Experience Manager
title: Publicar permissões de usuário para sistemas externos (opcional)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Publicar permissões de usuário para sistemas externos (opcional){#posting-user-permissions-to-external-systems-optional}

O Livefyre usa uma interface de PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.

## Tipos de usuários no Livefyre Studio

| Tipo de usuário | Descrição |
|--- |--- |
| proprietário | Esse usuário é um proprietário, pode moderar o conteúdo e atribuir novos moderadores. |
| admin | Esse usuário é um moderador e pode moderar o conteúdo. |
| membro | Esse usuário é descartado. O conteúdo postado não passa por filtros de spam ou profanidade, e não exige aprovação em fluxos pré-moderados. |
| none | Esse usuário é um usuário padrão e não tem permissões especiais. |
| saída | Esse usuário foi proibido de participar de qualquer conversão. |

Para publicar permissões de usuário em sistemas externos, você deve registrar um URL que receba dados de permissões como solicitações POST.

Por exemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parâmetro | Descrição |
|--- |--- |
| Networkname | Seu nome de rede fornecido pelo Livefyre. |
| token | Token válido do sistema. |
| url | URL para registro. |

O URL registrado deve aceitar Postagens com os seguintes dados como tipo de conteúdo: application/x-www-form-urlencoded.

| Parâmetro | Descrição |
|--- |--- |
| jid | JID do usuário cuja afiliação é alterada. Uma JID é uma string do formulário `user_id@network`. |
| afiliação | Nome das permissões atribuídas, que devem ser um dos seguintes: `{admin | member | none | outcast | owner}` |

Para obter mais informações sobre a atualização das configurações de afiliação do usuário, consulte [a Referência](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)da API de afiliação de usuário.
