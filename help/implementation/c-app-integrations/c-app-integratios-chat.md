---
description: Adicionar bate-papo ao vivo à sua página.
seo-description: Adicionar bate-papo ao vivo à sua página.
seo-title: Bate-papo
solution: Experience Manager
title: Bate-papo
uuid: d6761a69-efa5-4ad3-abaf-1ba8e6c17f94
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Bate-papo{#chat}

Adicionar bate-papo ao vivo à sua página.

O bate-papo permite que seu público-alvo se engaje em conversas em tempo real em torno de eventos ao vivo. O conteúdo é exibido como um fluxo contínuo, encorajando a rápida participação no diálogo que se desenrola.

Versão atual: Uso do bate-papo `fyre.conv v3.0.0.`

## Integração {#concept_0A99792A7E89403F95D082D52D600F17}

A incorporação do aplicativo de bate-papo segue o processo de incorporação de um aplicativo principal descrito em Introdução &gt; [Incorporação de um aplicativo](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps).

Exemplo:

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
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
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

Conforme observado na seção [CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) , CollectionMeta é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de sua codificação JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## NetworkConfig Object {#c-networkconfig-object}

O `NetworkConfig` objeto é um objeto JSON que personaliza o sistema de autenticação para usuários da rede.

O `NetworkConfig` objeto é um objeto JSON que contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| authDelegate | *objeto obrigatório* | Usado para personalizar o sistema de autenticação para usuários de rede personalizados. |
| rede | *string necessária* | Um nome de rede fornecido pelo Livefyre. Por exemplo: *yourname.fyre.co.* |
| attachmentDelegate | Objeto | Usado para especificar os tipos de anexos de mídia visíveis no fluxo do aplicativo. Para obter mais informações, consulte [Restrição de mídia](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| strings | *objeto opcional* | Usado para personalizar strings de texto dos elementos HTML em qualquer um dos aplicativos principais do Livefyre. Para obter mais informações, consulte Personalizações [de sequência de caracteres](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objeto ConvConfig {#c-convconfig-object}

O `convConfig` objeto é um objeto JSON usado para especificar o conteúdo que o aplicativo Livefyre renderiza na página.

>[!NOTE]
>
>Os parâmetros de `convConfig` objeto listados aqui não se aplicam ao aplicativo Revisões. Para obter informações de integração sobre o aplicativo Revisões usando o `convConfig` objeto, consulte Revisões de integração.

O `ConvConfig` objeto contém os seguintes parâmetros obrigatórios:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| articleId | *required string* | Uniquely identifies a Collection within your Site. Usually, this corresponds to a database primary key or Post ID within your CMS.  For example: “post-42”. Limite de 255 caracteres.  Observação:  If you use the article URL as your articleId, make certain the string is MD5 or SHA-1 encoded. |
| collectionMeta | *required string* | Metadados codificados por JWT sobre a coleção. Consulte [CollectionMeta Object](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) para obter mais informações. |
| el | *required string* | A ID de um elemento DOM ao qual o fluxo de conteúdo será renderizado. |
| siteId | *required string* | The Livefyre-provided ID for the website or application to which the Collection belongs. Por exemplo: "303617". |

>[!NOTE]
>
>The  parameter is not required for a Comments App implementation.`app`

The  object may also contain the following optional parameters:`ConvConfig`

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| actionButtons | *matriz opcional* | Uma matriz de botões de ação personalizados para adicionar a um conteúdo ao lado dos botões Compartilhar e Sinalizar. Para obter mais informações, consulte Adicionar botões personalizados. |
| animações | *optional boolean* | Define se as animações serão executadas no aplicativo Livefyre. Defina como false para desativar as animações. O padrão é true. |
| anonimousFlaggingEnabled | *booleano opcional* | Define se os usuários convidados têm a opção de sinalizar o conteúdo. O padrão é verdadeiro. |
| browserType | *cadeia opcional* | Define o dispositivo para o qual o conteúdo de exibição deve ser gerado. Isso fará com que o CSS e alguma funcionalidade sejam alterados para se ajustar ao tipo de dispositivo de entrada. As opções são desktop, dispositivo móvel ou tablet. (Se deixado em branco, o padrão será a determinação do Google Agent para o formato de exibição.) |
| soma | *sequência recomendada* (recomendado) | Identifica o estado atual da CollectionMeta. Alterar esse valor fará com que o Livefyre atualize os dados no servidor com os novos valores no CollectionMeta. |
| datetimeFormat | *optional string  Object  Function* | Especifica o formato datetime do conteúdo transmitido. Para obter mais informações, consulte Personalizar carimbos de data e hora. |
| disableAvatars | *booleano opcional* | Impede que avatars sejam renderizados no fluxo do aplicativo e, portanto, reduz o número de itens carregados no navegador. O padrão é falso. |
| disableIE8Shim | *optional boolean* | Disables the default shiv used by Livefyre to polyfill Internet Explorer 8 so that HTML5 elements are supported. Livefyre uses the following project:  https://github.com/aFarkas/html5shiv. [](https://github.com/aFarkas/html5shiv) O padrão é falso.  Observação:  If this value is false, polyfill of some sort must be used before Livefyre Chat is invoked for Internet Explorer 8 support. |
| disableThirdPartyAnalytics | *optional bBoolean* | Disables third party analytics systems (Quantserve and Google Analytics) that Livefyre may use for internal measurements. O padrão é falso. |
| editorCss | *objeto opcional* | Used to customize the comment editor styling. You may style the editor field background color as well as the font color, size, and family of the text that appears inside the editor.  Por exemplo: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | *optional integer* | Allows you to set the default number of comments visible in your App upon load. Pode ser um número inteiro de 1 a 50. |
| initialNumVisibleLegacy | *número inteiro opcional* | Allows you to set the default number of legacy content items visible in your App upon load. Pode ser um número inteiro de 1 a 50. Se esse parâmetro não for especificado, o padrão será initialNumVisible.  Por exemplo: Se sua coleção incluir 100 comentários ativos e 100 herdados, defina initalNumVisible:10 e initialNumVisibleLegacy:5, para exibir 10 comentários ativos (com um botão Mostrar mais) + 5 comentários de arquivamento (com um botão Mostrar mais). |
| maxVisible | *número inteiro opcional* | Define o número máximo de partes visíveis de conteúdo de nível superior no aplicativo de bate-papo. Se novas partes do fluxo de conteúdo forem inseridas, o conteúdo na parte inferior do fluxo será removido da página. Se o botão Mostrar mais... for clicado, o parâmetro será ignorado e o usuário poderá exibir o conteúdo desejado. (Use esse parâmetro para controlar o número de itens que aparecem na página em fluxos de alta velocidade.) |
| postToButtons | *matriz opcional* | Usado para configurar quais provedores aparecem ao incorporar o Aplicativo de Blog ao vivo. As opções disponíveis são duas (Twitter), fb (Facebook) e li (LinkedIn). O padrão é [ dois, fb ]. |
| readOnly | *booleano opcional* | Desativa toda a interatividade da coleção. Quando verdadeiro, os usuários não poderão fazer logon no fluxo e não poderão postar, editar, responder ou curtir conteúdo. Quando verdadeiro, os usuários poderão Sinalizar e compartilhar conteúdo. O padrão é falso. |
| stream | *objeto opcional* | Contém opções para configurar o streaming do aplicativo. |
| stream.catchup | *número inteiro opcional* | Especifica o número de segundos anteriores ao momento atual que o fluxo deve carregar. Por padrão, o Livefyre carrega 50 pedaços de conteúdo e, em seguida, carrega todo o conteúdo enviado entre esses e o atual. In very fast use cases, content may be posted too quickly to allow the App to ‘catch up’ to the present. Use this setting to define the number of seconds previous to now for which content will be posted (after the initial content load). |
| stream.delay | *optional integer* | Specifies the number of seconds between streaming requests. Use this parameter to help control the flow of content and delay how often the DOM is updated.  Observação:  If set too large, the stream may fall behind. |


>[!NOTE]
>
>You can pass one or more  objects during App initialization to display multiple Apps on the same page. `convConfig` Observe que aplicativos extras usam recursos e desempenho do navegador podem diminuir à medida que o número aumenta.

## Objeto CollectionMeta {#c-collectionmeta-object}

O `CollectionMeta` objeto é um objeto JSON que especifica metadados a serem armazenados na coleção.

`CollectionMeta` é sempre codificado antes de ser passado para o Livefyre para fins de segurança. O valor codificado é passado para o `ConvConfig` objeto mostrado acima.

>[!NOTE]
>
>É necessário adicionar um código do lado do servidor para codificar o objeto `CollectionMeta` JSON. Consulte Criar tokens do lado do servidor para obter mais informações.

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| articleId | *string necessária* | Uma ID exclusiva para a coleção. |
| title | *string necessária* | O título que você deseja aplicar à Coleção. Isso geralmente corresponde ao título da página que exibe o aplicativo.  Por exemplo: "A integração é tão divertida!"  Observação:  O comprimento máximo de caracteres para o título é de 255 caracteres. O campo de título não suporta entidades HTML. Codifique caracteres especiais usando UTF-8. |
| url | *string necessária* | O URL absoluto canônico que você deseja anexar a esta coleção. Esse URL será usado para gerar links de volta ao aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e Livefyre Studio.  Observação:  O Livefyre requer a utilização de um nome de domínio totalmente qualificado; o número da porta ou um retorno de chamada para resolver a configuração local não é necessário. Se estiver testando localmente, certifique-se de usar um domínio de URL base válido. (Por exemplo: `https://customer.com` é válido, mas não `https://localhost:5995` é.) Depois de configurar seu servidor Web local para aceitar um nome de domínio totalmente qualificado, não serão necessários retornos de chamada ou resoluções, e o desenvolvimento local poderá continuar como esperado. |
| type | *string necessária* | O tipo de Coleção. Deve ser um discurso vivo. |

O `CollectionMeta` objeto também pode conter o seguinte parâmetro opcional:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| específicos | *cadeia opcional* | A comma-separated list of single keywords or phrases. Pesquisar coleções por tags no Studio ou com a API de pesquisa.  Observação: While tags added through Studio may contain spaces, tags entered through the API cannot. Use sublinhados para definir tags que exibirão espaços na interface do usuário. (Por exemplo: use Segunda_Trimestre para exibir Segunda-feira Trimestre no Studio.) |

## Adicionar um manipulador de eventos {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Para registrar manipuladores de eventos, use a chamada widget.on na função de retorno de chamada do aplicativo.

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

Para obter mais informações e obter uma lista de eventos disponíveis, consulte Eventos [Javascript](../c-app-customizations/c-javascript-events.md#c_javascript_events).
