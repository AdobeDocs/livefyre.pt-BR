---
description: Você pode criar regras de fluxo que extraem conteúdo do email.
seo-description: Você pode criar regras de fluxo que extraem conteúdo do email.
seo-title: Regras de email
solution: Experience Manager
title: Regras de email
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Regras de email{#email-rules}

Você pode criar regras de fluxo que extraem conteúdo do email.

A criação de fluxos baseados em email permite que você poste conteúdo diretamente em um aplicativo ou pasta por email.

Use esse recurso para permitir que os contribuidores postem diretamente para seus aplicativos ou para a Biblioteca de ativos de seu computador ou dispositivo móvel.

Assim que a regra for criada, qualquer email que contenha uma imagem ou um arquivo de vídeo enviado para o endereço de email listado será publicado diretamente no aplicativo ou na Biblioteca de ativos, conforme especificado. Os emails enviados com vários anexos postarão todos os arquivos no local apropriado. Os emails enviados para o endereço listado contendo apenas texto não farão nada.

Depois de enviados, os campos do email serão usados para preencher os seguintes itens para o conteúdo:

* **[!UICONTROL From:]** Usado como autor do conteúdo, se a conta de usuário existir. Se não houver uma conta para o remetente, o autor será listado como anônimo.
* **[!UICONTROL Subject:]** Usado para o título do conteúdo.
* **[!UICONTROL Body:]** Usado para preencher detalhes de conteúdo no Studio.
* **[!UICONTROL Attachments:]** Os arquivos de mídia devem ser anexados ou o email será ignorado. Os tipos de arquivos suportados incluem 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT e WMV. O total de anexos deve estar abaixo de 25 MB.

Para obter opções adicionais de regras de fluxo para todas as regras de fluxo, consulte Opções de regra de [fluxo para todas as regras](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de fluxo.
