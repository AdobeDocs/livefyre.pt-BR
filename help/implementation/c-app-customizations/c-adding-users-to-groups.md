---
description: Adicione uma tag de usuário a uma conta para adicionar um Usuário a um grupo.
title: Adicionar usuários a grupos
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Adicionar usuários a grupos{#adding-users-to-groups}

Adicione uma tag de usuário a uma conta para adicionar um Usuário a um grupo.

As Tags de usuário podem ser implementadas para sistemas de perfil proprietários e corporativos e podem ser adicionadas a contas por vários meios:

* Criar proprietários e moderadores por meio do Studio atribui a tag de usuário &quot;Moderador&quot; à conta.
* Criar grupos de usuários e adicionar usuários a eles por meio do Studio aplica automaticamente Tags de usuário com o nome do grupo aos usuários selecionados.
* As Tags de usuário também podem ser aplicadas diretamente a Contas que usam a chamada [Adicionar tag de usuário HTTP](https://api.livefyre.com/docs#add-user-tag) ou Ping para pull.

>[!NOTE]
>
>Ambos os métodos de API, a chamada HTTP Adicionar tag de usuário e o método Ping for Pull , substituirão quaisquer tags atribuídas anteriormente à conta por outros meios. Portanto, selecione um método e use-o de forma consistente ao longo do seu processo.

## Adicionar um usuário a um Grupo na página Usuários no Studio {#section_qgq_nbw_xz}

* Clique em **[!UICONTROL Add Group]** ou no rótulo do grupo abaixo de qualquer nome de usuário para abrir o menu de grupos.
* Percorra a lista e localize o grupo ao qual deseja adicionar o usuário. Você pode inserir um nome de grupo na caixa **[!UICONTROL Search]** na parte superior da lista suspensa.
* Clique na caixa de seleção ao lado dos grupos aos quais o usuário deve ser adicionado e clique em retornar.

O perfil do usuário exibirá o nome do grupo (se o usuário estiver somente em um grupo) ou o número de grupos aos quais o usuário pertence.

## Adicione um usuário a um grupo usando a chamada Adicionar tag de usuário {#section_kn3_gbw_xz}

Passe o LFToken do usuário e o nome da tag selecionada com a solicitação de POST

Por exemplo:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Para obter mais informações, consulte Referência da API > [Adicionar tag de usuário](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Adicionar um usuário a um grupo usando Ping para Puxar {#section_kyj_11w_xz}

Use a matriz de tags para atribuir usuários a grupos de usuários. (As tags podem incluir de 1 a 63 caracteres alfanuméricos e sublinhados.)

Por exemplo:

```
"tags": ["moderator", "brand_advocate"],
```

## Adicionar um usuário a um grupo usando Perfis remotos {#section_uyn_scv_xz}

Adicione tags de usuário ao Perfil remoto, usadas para sincronizar dados de usuário entre seu sistema de perfil personalizado e o Livefyre, para usuários específicos.
