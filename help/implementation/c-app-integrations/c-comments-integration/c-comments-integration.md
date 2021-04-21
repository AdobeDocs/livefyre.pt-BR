---
description: Habilite os comentários ao vivo em sua página.
title: Comentários
exl-id: d62b3dc1-3c5e-45f6-9b21-ea1edcda9812
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 2%

---

# Comentários{#comments}

Habilite os comentários ao vivo em sua página. Os comentários permitem que você substitua seu sistema de comentários padrão por conversas em tempo real na sua página.

## Integração {#concept_4093E8BAA96A464BA74D263DA031C0B0}

A incorporação do aplicativo Comentários segue o processo de incorporação de um aplicativo principal descrito em Introdução > Incorporação de um aplicativo.

### Exemplo

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Conforme observado na seção Building CollectionMeta, CollectionMeta é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## Objeto NetworkConfig {#c-networkconfig-object}

O objeto `NetworkConfig` é um objeto JSON que personaliza o sistema de autenticação para usuários da rede.
O objeto `NetworkConfig` é um objeto JSON que contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **authDelegate** | **  objeto obrigatório | Usado para personalizar o sistema de autenticação para usuários de rede personalizados. |
| **rede** | Sequência *necessária* | Um nome de rede fornecido pela Livefyre. Por exemplo: *yourname.fyre.co.* |
| **attachmentDelegate** | ** objeto opcional | Usado para especificar os tipos de anexos de mídia visíveis no fluxo do aplicativo. Para obter mais informações, consulte [Restrição de mídia](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strings** | ** objeto opcional | Usado para personalizar cadeias de caracteres de texto dos elementos HTML em qualquer um dos aplicativos principais do Livefyre. Para obter mais informações, consulte [Personalizações da cadeia de caracteres](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objeto ConvConfig {#c-convconfig-object}

O objeto `convConfig` é um objeto JSON usado para especificar o conteúdo renderizado pelo aplicativo Livefyre na página.

>[!NOTE]
>
>Os parâmetros de objeto `convConfig` listados aqui não se aplicam ao aplicativo Revisões. Para obter informações de integração sobre o aplicativo Reviews usando o objeto `convConfig`, consulte Revisar integração.

O objeto `ConvConfig` contém os seguintes parâmetros obrigatórios:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **articleId** | ** string obrigatória | Identifica exclusivamente uma coleção no seu site. Geralmente, isso corresponde a uma chave primária de banco de dados ou ID da postagem em seu CMS. Por exemplo: &quot;pós-42&quot;. Limite de 255 caracteres.  Observação:  Se você usar o URL do artigo como articleId, verifique se a string está codificada em MD5 ou SHA-1. |
| **authPageReload** | **  optionalbooleano | Aplica-se ao aplicativo Comentários: Permite controlar se o comentário de um usuário é armazenado localmente durante o processo de autenticação. Se verdadeiro, se um usuário digitar um comentário e fizer logon no aplicativo, o comentário será armazenado localmente e será inserido novamente no campo de conteúdo após o logon e a atualização da página. Se for falso, o conteúdo inserido será limpo durante o processo de logon e deverá ser digitado novamente. |
| **collectionMeta** | ** string obrigatória | Metadados codificados por JWT sobre a coleção. Consulte [CollectionMeta](#c_collectionmeta_object) Objeto para obter mais informações. |
| **el** | ** string obrigatória | A ID de um elemento DOM ao qual o fluxo de conteúdo será renderizado. |
| **siteId** | ** string obrigatória | A ID fornecida pelo Livefyre para o site ou aplicativo ao qual a coleção pertence. Por exemplo: &quot;303617&quot;. |

>[!NOTE]
>
>O parâmetro `app` não é necessário para uma implementação do aplicativo Comentários.

O objeto `ConvConfig` também pode conter os seguintes parâmetros opcionais:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **actionButtons** | ** optionalarray | Uma matriz de botões de ação personalizados para adicionar a um conteúdo ao lado dos botões Compartilhar e Sinalizar. Para obter mais informações, consulte Adicionar botões personalizados. |
| **animações** | ** optionalbooleano | Define se as animações serão executadas no aplicativo Livefyre. Defina como falso para desativar animações. O padrão é true. |
| **anonymousFlaggingEnabled** | ** optionalbooleano | Define se os usuários convidados têm a opção de sinalizar conteúdo. O padrão é verdadeiro. |
| **browserType** | ** optionalstring | Define o dispositivo para o qual o conteúdo de exibição deve ser gerado. Isso fará com que o CSS e algumas funcionalidades sejam alterados para se ajustar ao tipo de dispositivo de entrada. As opções são desktop, celular ou tablet. (Se deixado em branco, o padrão será a determinação do Google Agent para o formato de exibição.) |
| **checksum** | ** recommendations dedstring | Identifica o estado atual da CollectionMeta. Alterar esse valor fará com que o Livefyre atualize os dados no servidor com os novos valores em CollectionMeta. |
| **datetimeFormat** | **  função de objeto optionalstring | Especifica o formato datetime do conteúdo transmitido. Para obter mais informações, consulte Personalização de carimbos de data e hora. |
| **disableAvatars** | ** optionalbooleano | Impede a renderização de avatares no fluxo do aplicativo e, portanto, reduz o número de itens carregados no navegador. O padrão é falso. |
| **disableIE8Shim** | ** optionalbooleano | Desativa o shiv padrão usado pelo Livefyre para preencher politicamente o Internet Explorer 8 para que os elementos HTML5 sejam compatíveis. O Livefyre utiliza o seguinte projeto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . O padrão é falso.  Observação:  Se esse valor for falso, o polyfill de algum tipo deverá ser usado antes que o Livefyre Chat seja chamado para o suporte ao Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalbooleano | Desativa sistemas de análise de terceiros (Quantserve e Google Analytics) que o Livefyre pode usar para medições internas. O padrão é falso. |
| **editorCss** | ** objeto opcional | Usado para personalizar o estilo do editor de comentários. Você pode criar um estilo para a cor de fundo do campo do editor, bem como para a cor, o tamanho e a família da fonte do texto que aparece dentro do editor.  Por exemplo: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** optionalinteger | Permite definir o número padrão de comentários visíveis em seu aplicativo após o carregamento. Pode ser um inteiro de 1 a 50. |
| **initialNumVisibleLegacy** | ** optionalinteger | Permite que você defina o número padrão de itens de conteúdo herdados visíveis em seu aplicativo após o carregamento. Pode ser um inteiro de 1 a 50. Se esse parâmetro não for especificado, o padrão será initialNumVisible.  Por exemplo: Se a Coleção incluir 100 comentários ativos e 100 legados, defina initalNumVisible:10 e initialNumVisibleLegacy:5, para exibir 10 comentários ativos (com um botão Mostrar mais) + 5 comentários de arquivamento (com um botão Mostrar mais). |
| **maxVisible** | ** optionalinteger | Define o número máximo de partes visíveis do conteúdo de nível superior no Aplicativo de Bate-papo. Se novas partes do conteúdo forem transmitidas, o conteúdo na parte inferior do fluxo será removido da página. Se o botão Show more.. for clicado, o parâmetro será ignorado e o usuário poderá mostrar o conteúdo desejado. (Use esse parâmetro para controlar o número de itens que aparecem na página em fluxos de alta velocidade.) |
| **postToButtons** | ** optionalarray | Usado para configurar quais provedores aparecem ao incorporar o Aplicativo de blog em tempo real. As opções disponíveis são duas (Twitter), fb (Facebook) e li (LinkedIn). O padrão é [ tw , fb ]. |
| **readOnly** | ** optionalbooleano | Desativa toda a interatividade da Coleção. Quando true, os usuários não poderão fazer logon no fluxo e não poderão Publicar, Editar, Responder ou Curtir o conteúdo. Quando verdadeiro, os usuários poderão Sinalizar e compartilhar conteúdo. O padrão é falso. |
| **fluxo** | ** objeto opcional | Contém opções para configurar o streaming do aplicativo. |
| **stream.catchup** | ** optionalinteger | Especifica o número de segundos antes do momento atual em que o fluxo deve ser carregado. Por padrão, o Livefyre carrega 50 partes do conteúdo e, em seguida, carrega todo o conteúdo enviado entre elas e o tempo atual. Em casos de uso muito rápidos, o conteúdo pode ser publicado rapidamente para permitir que o aplicativo &quot;acompanhe&quot; o presente. Use essa configuração para definir o número de segundos anteriores a agora para os quais o conteúdo será publicado (após o carregamento inicial do conteúdo). |
| **stream.delay** | ** optionalinteger | Especifica o número de segundos entre solicitações de transmissão. Use esse parâmetro para ajudar a controlar o fluxo do conteúdo e atrasar a frequência com que o DOM é atualizado.  Observação:  Se definido como muito grande, o fluxo pode ficar para trás. |


>[!NOTE]
>
>Você pode enviar um ou mais objetos `convConfig` durante a inicialização do aplicativo para exibir vários aplicativos na mesma página. Esteja ciente de que aplicativos extras usam recursos e o desempenho do navegador podem degradar conforme o número aumenta.

## CollectionMeta Object {#c-collectionmeta-object}

O objeto `CollectionMeta` é um objeto JSON que especifica os metadados a serem armazenados na coleção.

`CollectionMeta` é sempre codificado antes de ser passado para o Livefyre para fins de segurança. O valor codificado é passado para o objeto `ConvConfig` mostrado acima.

>[!NOTE]
>
>Você deve adicionar código do lado do servidor para codificar o objeto JSON `CollectionMeta`. Consulte Criar tokens do lado do servidor para obter mais informações.

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **articleId** | ** string obrigatória | Uma ID exclusiva para a coleção. |
| **título** | ** string obrigatória | O título que deseja aplicar à Coleção. Isso geralmente corresponde ao título da página que exibe o aplicativo.  Por exemplo: &quot;A integração é tão divertida!&quot; <br>**Observação:**  o comprimento máximo de caracteres do título é de 255 caracteres. O campo de título não é compatível com entidades HTML. Codifique caracteres especiais usando UTF-8. |
| **url** | ** string obrigatória | O URL absoluto canônico que você deseja anexar a essa coleção. Esse URL será usado para gerar links para o aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e o Livefyre Studio.  <br>**** O NoteLivefyre requer o uso de um nome de domínio totalmente qualificado; o número da porta ou um retorno de chamada para resolver a configuração local não é necessário. Se estiver testando localmente, certifique-se de usar um domínio de URL de base válido. <br>Por exemplo:  `https://customer.com` é válido, mas não  `https://localhost:5995` é. Depois de configurar o servidor da Web local para aceitar um nome de domínio totalmente qualificado, não serão necessários retornos de chamada ou resoluções e o desenvolvimento local poderá prosseguir conforme esperado. |
| **type** | ** string obrigatória | O tipo Collection . Deve ser `livechat`. |

O objeto `CollectionMeta` também pode conter o seguinte parâmetro opcional:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **específicos** | ** optionalstring | Uma lista separada por vírgulas de palavras-chave ou frases únicas. Pesquise Coleções por tags no Studio ou com a API de pesquisa. <br> **Observação:** embora as tags adicionadas por meio do Studio possam conter espaços, as tags inseridas por meio da API não podem. Use sublinhados para definir tags que exibirão espaços na interface do usuário. (Por exemplo: use `Monday_Quarterback` para exibir o Quarterback de segunda-feira no Studio.) |

## Adicionar um manipulador de evento {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Para registrar manipuladores de evento, use a chamada widget.on na função de retorno de chamada do aplicativo.

### Por exemplo

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
