---
description: O Blog ao vivo permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.
title: Blog ao vivo
exl-id: e8a16b56-53c9-488e-9807-1cf80b62462e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 2%

---

# Blog ao vivo{#live-blog}

O Blog ao vivo permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

## Blog ao vivo {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

O Blog ao vivo permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

## Integração {#c_live_blog_integration}

O Blog ao vivo permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

Para incorporar um aplicativo de blog em tempo real, siga o procedimento para Incorporar um aplicativo. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Veja a seguir um exemplo de como um aplicativo Live Blog incorporado se parece.

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
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
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

CollectionMeta é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## Objeto NetworkConfig {#c-networkconfig-object}

O objeto `NetworkConfig` é um objeto JSON que personaliza o sistema de autenticação para usuários da rede.

O objeto `NetworkConfig` é um objeto JSON que contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **authDelegate** | ** objeto obrigatório | Usado para personalizar o sistema de autenticação para usuários de rede personalizados. |
| **rede** | ** string obrigatória Um nome de rede fornecido pelo Livefyre. Por exemplo: *yourname.fyre.co.* |
| **attachmentDelegate** | ** objeto opcional | Usado para especificar os tipos de anexos de mídia visíveis no fluxo do aplicativo. Para obter mais informações, consulte [Restrição de mídia](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
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
| **collectionMeta** | ** string obrigatória | Metadados codificados por JWT sobre a coleção. Consulte CollectionMeta Object para obter mais informações. |
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
| **anonymousFlaggingEnabled** | booleano | Define se os usuários convidados têm a opção de sinalizar conteúdo. O padrão é verdadeiro. |
| browserType | ** optionalString | Define o dispositivo para o qual o conteúdo de exibição deve ser gerado. Isso fará com que o CSS e algumas funcionalidades sejam alterados para se ajustar ao tipo de dispositivo de entrada. As opções são desktop, celular ou tablet. (Se deixado em branco, o padrão será a determinação do Google Agent para o formato de exibição.) |
| **checksum** | ** string opcional (recomendado) | Identifica o estado atual da CollectionMeta. Alterar esse valor fará com que o Livefyre atualize os dados no servidor com os novos valores em CollectionMeta. |
| **datetimeFormat** | **  função de objeto optionalstring | Especifica o formato datetime do conteúdo transmitido. Para obter mais informações, consulte Personalização de carimbos de data e hora. |
| disableAvatars | ** optionalbooleano | Impede a renderização de avatares no fluxo do aplicativo e, portanto, reduz o número de itens carregados no navegador. O padrão é falso. |
| disableIE8Shim | ** optionalbooleano | Desativa o shiv padrão usado pelo Livefyre para preencher politicamente o Internet Explorer 8 para que os elementos HTML5 sejam compatíveis. O Livefyre utiliza o seguinte projeto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . O padrão é falso.  Observação:  Se esse valor for falso, o polyfill de algum tipo deverá ser usado antes que o Livefyre Chat seja chamado para o suporte ao Internet Explorer 8. |
| **disableThirdPartyAnalytics** | ** optionalbooleano | Desativa sistemas de análise de terceiros (Quantserve e Google Analytics) que o Livefyre pode usar para medições internas. O padrão é falso. |
| **editorCss** | ** objeto opcional | Usado para personalizar o estilo do editor de comentários. Você pode criar um estilo para a cor de fundo do campo do editor, bem como para a cor, o tamanho e a família da fonte do texto que aparece dentro do editor.  Por exemplo: {plano de fundo: ‘#ccc’, cor: &quot;red&quot;, fonte: ’30px &quot;Helvetica Neue&quot;, Helvetica, Arial, Genebra, sans-serif’} |
| **initialNumVisible** | ** optionalinteger | Permite definir o número padrão de comentários visíveis em seu aplicativo após o carregamento. Pode ser um inteiro de 1 a 50. |
| **initialNumVisibleLegacy** | ** optionalinteger | Permite que você defina o número padrão de itens de conteúdo herdados visíveis em seu aplicativo após o carregamento. Pode ser um inteiro de 1 a 50. Se esse parâmetro não for especificado, o padrão será initialNumVisible.  Por exemplo: Se a Coleção incluir 100 comentários ativos e 100 legados, defina initalNumVisible:10 e initialNumVisibleLegacy:5, para exibir 10 comentários ativos (com um botão Mostrar mais) + 5 comentários de arquivamento (com um botão Mostrar mais). |
| **maxVisible** | ** optionalinteger | Define o número máximo de partes visíveis do conteúdo de nível superior no Aplicativo de Bate-papo. Se novas partes do conteúdo forem transmitidas, o conteúdo na parte inferior do fluxo será removido da página. Se o botão Show more.. for clicado, o parâmetro será ignorado e o usuário poderá mostrar o conteúdo desejado. (Use esse parâmetro para controlar o número de itens que aparecem na página em fluxos de alta velocidade.) |
| **postToButtons** | ** optionalarray | Usado para configurar quais provedores aparecem ao incorporar o Aplicativo de blog em tempo real. As opções disponíveis são duas (Twitter), fb (Facebook) e li (LinkedIn). O padrão é [ tw , fb ]. |
| **readOnly** | ** optionalbooleano | Desativa toda a interatividade da Coleção. Quando true, os usuários não poderão fazer logon no fluxo e não poderão Publicar, Editar, Responder ou Curtir o conteúdo. Quando verdadeiro, os usuários poderão Sinalizar e compartilhar conteúdo. O padrão é falso. |
| **fluxo** | ** objeto opcional | Contém opções para configurar o streaming do aplicativo. |
| stream.catchup | ** optionalinteger | Especifica o número de segundos antes do momento atual em que o fluxo deve ser carregado. Por padrão, o Livefyre carrega 50 partes do conteúdo e, em seguida, carrega todo o conteúdo enviado entre elas e o tempo atual. Em casos de uso muito rápidos, o conteúdo pode ser publicado rapidamente para permitir que o aplicativo &quot;acompanhe&quot; o presente. Use essa configuração para definir o número de segundos anteriores a agora para os quais o conteúdo será publicado (após o carregamento inicial do conteúdo). |
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
| **título** | ** string obrigatória | O título que deseja aplicar à Coleção. Isso geralmente corresponde ao título da página que exibe o aplicativo.  Por exemplo: &quot;A integração é tão divertida!&quot;  Observação:  O comprimento máximo de caracteres do título é de 255 caracteres. O campo de título não é compatível com entidades HTML. Codifique caracteres especiais usando UTF-8. |
| **url** | ** string obrigatória | O URL absoluto canônico que você deseja anexar a essa coleção. Esse URL será usado para gerar links para o aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e o Livefyre Studio.  Observação:  O Livefyre requer a utilização de um nome de domínio totalmente qualificado; o número da porta ou um retorno de chamada para resolver a configuração local não é necessário. Se estiver testando localmente, certifique-se de usar um domínio de URL de base válido. (Por exemplo: `https://customer.com` é válido, enquanto `https://localhost:5995` não é.) Depois de configurar o servidor da Web local para aceitar um nome de domínio totalmente qualificado, não serão necessários retornos de chamada ou resoluções e o desenvolvimento local poderá prosseguir conforme esperado. |
| **type** | ** requiredString | O tipo Collection . Deve ser o livechat . |

O objeto `CollectionMeta` também pode conter o seguinte parâmetro opcional:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **específicos** | ** optionalstring | Uma lista separada por vírgulas de palavras-chave ou frases únicas. Pesquise coleções por tags no Studio ou com a API de pesquisa. **Observação:** embora as tags adicionadas por meio do Studio possam conter espaços, as tags inseridas por meio da API não podem. Use sublinhados para definir tags que exibirão espaços na interface do usuário. (Por exemplo: use Monday_Quarterback para exibir Segunda-feira de Quarterback no Studio.) |

## Adicionar um manipulador de evento {#concept_D835C710A7214F6D921571E0770B6BC5}

Para registrar manipuladores de evento, use a chamada widget.on na função de retorno de chamada do aplicativo.

Por exemplo:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
