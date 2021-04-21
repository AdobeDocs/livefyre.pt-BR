---
description: O Livefyre usa uma interface PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.
title: Postando permissões do usuário em sistemas externos (Opcional)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 4%

---

# Postando Permissões de Usuário em Sistemas Externos (Opcional){#posting-user-permissions-to-external-systems-optional}

O Livefyre usa uma interface PUSH para enviar informações externas do sistema sobre alterações nas permissões do usuário.

## Tipos de usuários no Livefyre Studio

| Tipo de usuário | Descrição |
|--- |--- |
| proprietário | Esse usuário é um proprietário, pode moderar o conteúdo e atribuir novos moderadores. |
| admin | Este usuário é um moderador e pode moderar conteúdo. |
| membro | Esse usuário é incluído na lista de permissões. O conteúdo postado não passa por spam ou filtros de rentabilidade e não requer aprovação em fluxos pré-moderados. |
| none | Este usuário é padrão e não tem permissões especiais. |
| difusão | Este usuário foi proibido de participar de qualquer conversa. |

Para publicar permissões de usuário em sistemas externos, você deve registrar um URL que receba dados de permissões como solicitações de POST.

Por exemplo:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parâmetro | Descrição |
|--- |--- |
| networkName | Seu Livefyre forneceu o nome da rede. |
| token | Token de sistema válido. |
| url | URL para registrar. |

O URL registrado deve aceitar POSTs com os seguintes dados como tipo de conteúdo: application/x-www-form-urlencoded.

| Parâmetro | Descrição |
|--- |--- |
| jid | JID do usuário cuja afiliação foi alterada. Um JID é uma string do formulário `user_id@network`. |
| afiliação | Nome das permissões atribuídas, que devem ser uma das seguintes:  `{admin | member | none | outcast | owner}` |

Para obter informações adicionais sobre como atualizar as configurações de afiliação de usuários, consulte [Adicionar Referência da API de Afiliação de Usuário](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
