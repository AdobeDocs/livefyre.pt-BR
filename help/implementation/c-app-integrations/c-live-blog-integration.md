---
description: O Live Blog permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.
seo-description: O Live Blog permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.
seo-title: Blog ao vivo
solution: Experience Manager
title: Blog ao vivo
uuid: 5ca373f1-2008-45ab-9ec2-1e295af4e368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Blog ao vivo{#live-blog}

O Live Blog permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

## Blog ao vivo {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

O Live Blog permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

## Integração {#c_live_blog_integration}

O Live Blog permite que você apresente atualizações e imagens em tempo real dos próprios editores do site ao cobrir um evento ao vivo.

Para incorporar um aplicativo de blog ao vivo, siga o procedimento para Incorporar um aplicativo. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). A seguir está um exemplo da aparência de um Aplicativo de Blog incorporado.

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

O `NetworkConfig` objeto é um objeto JSON que personaliza o sistema de autenticação para usuários da rede.

O `NetworkConfig` objeto é um objeto JSON que contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **authDelegate** | *objeto obrigatório* | Usado para personalizar o sistema de autenticação para usuários de rede personalizados. |
| **rede** | *cadeia de caracteres necessária* Um nome de rede fornecido pelo Livefyre. Por exemplo: *yourname.fyre.co.* |
| **attachmentDelegate** | *objeto opcional* | Usado para especificar os tipos de anexos de mídia visíveis no fluxo do aplicativo. Para obter mais informações, consulte [Restrição de mídia](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strings** | *objeto opcional* | Usado para personalizar strings de texto dos elementos HTML em qualquer um dos aplicativos principais do Livefyre. Para obter mais informações, consulte Personalizações [de sequência de caracteres](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objeto ConvConfig {#c-convconfig-object}

O `convConfig` objeto é um objeto JSON usado para especificar o conteúdo que o aplicativo Livefyre renderiza na página.

>[!NOTE]
>
>Os parâmetros de `convConfig` objeto listados aqui não se aplicam ao aplicativo Revisões. Para obter informações de integração sobre o aplicativo Revisões usando o `convConfig` objeto, consulte Revisões de integração.

O `ConvConfig` objeto contém os seguintes parâmetros obrigatórios:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **articleId** | *string necessária* | Identifica exclusivamente uma coleção no seu site. Normalmente, isso corresponde a uma chave primária do banco de dados ou ID da postagem dentro do CMS. Por exemplo: "pós-42". Limite de 255 caracteres.  Observação:  Se você usar o URL do artigo como articleId, certifique-se de que a sequência de caracteres esteja codificada em MD5 ou SHA-1. |
| **collectionMeta** | *string necessária* | Metadados codificados por JWT sobre a coleção. Consulte CollectionMeta Object para obter mais informações. |
| **el** | *string necessária* | A ID de um elemento DOM ao qual o fluxo de conteúdo será renderizado. |
| **siteId** | *string necessária* | A ID fornecida pelo Livefyre para o site ou aplicativo ao qual a coleção pertence. Por exemplo: "303617". |

>[!NOTE]
>
>O `app` parâmetro não é necessário para uma implementação do aplicativo Comentários.

O `ConvConfig` objeto também pode conter os seguintes parâmetros opcionais:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **actionButtons** | *matriz opcional* | Uma matriz de botões de ação personalizados para adicionar a um conteúdo ao lado dos botões Compartilhar e Sinalizar. Para obter mais informações, consulte Adicionar botões personalizados. |
| **animações** | *booleano opcional* | Define se as animações serão executadas no aplicativo Livefyre. Defina como false para desativar as animações. O padrão é true. |
| **anonimousFlaggingEnabled** | booleano | Define se os usuários convidados têm a opção de sinalizar o conteúdo. O padrão é verdadeiro. |
| browserType | *cadeia opcional* | Define o dispositivo para o qual o conteúdo de exibição deve ser gerado. Isso fará com que o CSS e alguma funcionalidade sejam alterados para se ajustar ao tipo de dispositivo de entrada. As opções são desktop, dispositivo móvel ou tablet. (Se deixado em branco, o padrão será a determinação do Google Agent para o formato de exibição.) |
| **soma** | *sequência opcional* (recomendado) | Identifica o estado atual da CollectionMeta. Alterar esse valor fará com que o Livefyre atualize os dados no servidor com os novos valores no CollectionMeta. |
| **datetimeFormat** | *função de objeto de string opcional* | Especifica o formato datetime do conteúdo transmitido. Para obter mais informações, consulte Personalizar carimbos de data e hora. |
| disableAvatars | *booleano opcional* | Impede que avatars sejam renderizados no fluxo do aplicativo e, portanto, reduz o número de itens carregados no navegador. O padrão é falso. |
| disableIE8Shim | *booleano opcional* | Desativa o shiv padrão usado pelo Livefyre para preencher politicamente o Internet Explorer 8, de modo que os elementos HTML5 sejam suportados. O Livefyre utiliza o seguinte projeto:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . O padrão é falso.  Observação:  Se esse valor for falso, o preenchimento de algum tipo deve ser usado antes que o Livefyre Chat seja chamado para suporte ao Internet Explorer 8. |
| **disableThirdPartyAnalytics** | *booleano opcional* | Desativa sistemas de análise de terceiros (Quantserve e Google Analytics) que o Livefyre pode usar para medidas internas. O padrão é falso. |
| **editorCss** | *objeto opcional* | Usado para personalizar o estilo do editor de comentários. Você pode estilizar a cor de fundo do campo do editor, bem como a cor, o tamanho e a família da fonte do texto que aparece dentro do editor.  Por exemplo: {fundo: ‘#ccc’, cor: "red", fonte: ’30px "Helvetica Neue", Helvetica, Arial, Genebra, sans-serif’} |
| **initialNumVisible** | *número inteiro opcional* | Permite que você defina o número padrão de comentários visíveis no aplicativo após o carregamento. Pode ser um número inteiro de 1 a 50. |
| **initialNumVisibleLegacy** | *número inteiro opcional* | Permite que você defina o número padrão de itens de conteúdo herdados visíveis no aplicativo após o carregamento. Pode ser um número inteiro de 1 a 50. Se esse parâmetro não for especificado, o padrão será initialNumVisible.  Por exemplo: Se sua coleção incluir 100 comentários ativos e 100 herdados, defina initalNumVisible:10 e initialNumVisibleLegacy:5, para exibir 10 comentários ativos (com um botão Mostrar mais) + 5 comentários de arquivamento (com um botão Mostrar mais). |
| **maxVisible** | *número inteiro opcional* | Define o número máximo de partes visíveis de conteúdo de nível superior no aplicativo de bate-papo. Se novas partes do fluxo de conteúdo forem inseridas, o conteúdo na parte inferior do fluxo será removido da página. Se o botão Mostrar mais... for clicado, o parâmetro será ignorado e o usuário poderá exibir o conteúdo desejado. (Use esse parâmetro para controlar o número de itens que aparecem na página em fluxos de alta velocidade.) |
| **postToButtons** | *matriz opcional* | Usado para configurar quais provedores aparecem ao incorporar o Aplicativo de Blog ao vivo. As opções disponíveis são duas (Twitter), fb (Facebook) e li (LinkedIn). O padrão é [ dois, fb ]. |
| **readOnly** | *booleano opcional* | Desativa toda a interatividade da coleção. Quando verdadeiro, os usuários não poderão fazer logon no fluxo e não poderão postar, editar, responder ou curtir conteúdo. Quando verdadeiro, os usuários poderão Sinalizar e compartilhar conteúdo. O padrão é falso. |
| **stream** | *objeto opcional* | Contém opções para configurar o streaming do aplicativo. |
| stream.catchup | *número inteiro opcional* | Especifica o número de segundos anteriores ao momento atual que o fluxo deve carregar. Por padrão, o Livefyre carrega 50 pedaços de conteúdo e, em seguida, carrega todo o conteúdo enviado entre esses e o atual. Em casos de uso muito rápido, o conteúdo pode ser publicado muito rapidamente para permitir que o aplicativo "acompanhe" o presente. Use essa configuração para definir o número de segundos anteriores a agora para o qual o conteúdo será publicado (após a carga inicial do conteúdo). |
| **stream.delay** | *número inteiro opcional* | Especifica o número de segundos entre as solicitações de streaming. Use esse parâmetro para ajudar a controlar o fluxo de conteúdo e atrasar a frequência com que o DOM é atualizado.  Observação:  Se definido como grande demais, o fluxo pode ficar para trás. |


>[!NOTE]
>
>Você pode passar um ou mais `convConfig` objetos durante a inicialização do aplicativo para exibir vários aplicativos na mesma página. Observe que aplicativos extras usam recursos e desempenho do navegador podem diminuir à medida que o número aumenta.

## Objeto CollectionMeta {#c-collectionmeta-object}

O `CollectionMeta` objeto é um objeto JSON que especifica metadados a serem armazenados na coleção.

`CollectionMeta` é sempre codificado antes de ser passado para o Livefyre para fins de segurança. O valor codificado é passado para o `ConvConfig` objeto mostrado acima.

>[!NOTE]
>
>É necessário adicionar um código do lado do servidor para codificar o objeto `CollectionMeta` JSON. Consulte Criar tokens do lado do servidor para obter mais informações.

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **articleId** | *string necessária* | Uma ID exclusiva para a coleção. |
| **título** | *string necessária* | O título que você deseja aplicar à coleção. Isso geralmente corresponde ao título da página que exibe o aplicativo.  Por exemplo: "A integração é tão divertida!"  Observação:  O comprimento máximo de caracteres para o título é de 255 caracteres. O campo de título não suporta entidades HTML. Codifique caracteres especiais usando UTF-8. |
| **url** | *string necessária* | O URL absoluto canônico que você deseja anexar a esta coleção. Esse URL será usado para gerar links de volta ao aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e Livefyre Studio.  Observação:  O Livefyre requer a utilização de um nome de domínio totalmente qualificado; o número da porta ou um retorno de chamada para resolver a configuração local não é necessário. Se estiver testando localmente, certifique-se de usar um domínio de URL base válido. (Por exemplo: `https://customer.com` é válido, mas não `https://localhost:5995` é.) Depois de configurar seu servidor Web local para aceitar um nome de domínio totalmente qualificado, não serão necessários retornos de chamada ou resoluções, e o desenvolvimento local poderá continuar como esperado. |
| **type** | *string necessária* | O tipo de Coleção. Deve ser um discurso vivo. |

O `CollectionMeta` objeto também pode conter o seguinte parâmetro opcional:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **específicos** | *cadeia opcional* | Uma lista separada por vírgulas de palavras-chave únicas ou frases. Pesquisar coleções por tags no Studio ou com a API de pesquisa. **** Observação: Embora as tags adicionadas pelo Studio possam conter espaços, as tags inseridas por meio da API não podem. Use sublinhados para definir tags que exibirão espaços na interface do usuário. (Por exemplo: use Segunda_Trimestre para exibir Segunda-feira Trimestre no Studio.) |

## Adicionar um manipulador de eventos {#concept_D835C710A7214F6D921571E0770B6BC5}

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

