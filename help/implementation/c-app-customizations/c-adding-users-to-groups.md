---
description: Adicione uma tag de usuário a uma conta para adicionar um usuário a um
  grupo.
seo-description: Adicione uma tag de usuário a uma conta para adicionar um usuário
  a um grupo.
seo-title: Adicionar usuários a grupos
solution: Experience Manager
title: Adicionar usuários a grupos
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Adicionar usuários a grupos{#adding-users-to-groups}

Adicione uma tag de usuário a uma conta para adicionar um usuário a um grupo.

As Tags de usuário podem ser implementadas tanto para sistemas de perfil proprietários quanto para empresas, podendo ser adicionadas a contas por vários meios:

* A criação de proprietários e moderadores por meio do Studio atribui a Tag de usuário "Moderador" à conta.
* Criar grupos de usuários e adicionar usuários a eles por meio do Studio aplica automaticamente Tags de usuário com o nome do grupo aos usuários selecionados.
* As Tags do usuário também podem ser aplicadas diretamente às Contas usando a chamada [Adicionar](https://api.livefyre.com/docs#add-user-tag) tag do usuário ou o Ping para extrair.

>[!NOTE]
>
>Os dois métodos da API, a chamada Adicionar tag do usuário e o método Ping para Pull, substituirão todas as tags anteriormente atribuídas à Conta por outros meios. Portanto, selecione um método e use-o de forma consistente durante o processo.

## Adicionar um usuário a um Grupo da página Usuários no Studio {#section_qgq_nbw_xz}

* Clique **[!UICONTROL Add Group]** no rótulo do grupo abaixo de qualquer nome de usuário para abrir o menu de grupos.
* Role pela lista e localize o grupo para o qual deseja adicionar o usuário. Você pode inserir um nome de grupo na **[!UICONTROL Search]** caixa na parte superior da lista suspensa.
* Clique na caixa de seleção ao lado dos grupos aos quais o usuário deve ser adicionado e clique em retornar.

O perfil do usuário exibirá o nome do grupo (se o usuário estiver somente em um grupo) ou o número de grupos aos quais o usuário pertence.

## Adicionar um usuário a um grupo usando a chamada Adicionar tag do usuário {#section_kn3_gbw_xz}

Passe o lftoken do usuário e o nome da tag selecionada com a solicitação POST

Por exemplo:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Para obter mais informações, consulte Referência de API > [Adicionar tag do usuário](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Adicionar um usuário a um Grupo usando Ping para Extrair {#section_kyj_11w_xz}

Use a matriz de tags para atribuir usuários a grupos de usuários. (As tags podem incluir 1-63 caracteres alfanuméricos e sublinhados.)

Por exemplo:

```
"tags": ["moderator", "brand_advocate"],
```

## Adicionar um usuário a um grupo usando perfis remotos {#section_uyn_scv_xz}

Adicione tags de usuário ao perfil remoto, usado para sincronizar os dados do usuário entre o seu sistema de perfil personalizado e o Livefyre, para os usuários específicos.
