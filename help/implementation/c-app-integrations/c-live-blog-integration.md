---
description: O Blog ativo permite que você inclua atualizações em tempo real e imagens dos próprios editores ao cobrir um evento ao vivo.
seo-description: O Blog ativo permite que você inclua atualizações em tempo real e imagens dos próprios editores ao cobrir um evento ao vivo.
seo-title: Blog ao vivo
solution: Experience Manager
title: Blog ao vivo
uuid: 5 ca 373 f 1-2008-45 ab -9 ec 2-1 e 295 af 4 e 368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Blog ao vivo{#live-blog}

O Blog ativo permite que você inclua atualizações em tempo real e imagens dos próprios editores ao cobrir um evento ao vivo.

## Blog ao vivo {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

O Blog ativo permite que você inclua atualizações em tempo real e imagens dos próprios editores ao cobrir um evento ao vivo.

## Integração {#c_live_blog_integration}

O Blog ativo permite que você inclua atualizações em tempo real e imagens dos próprios editores ao cobrir um evento ao vivo.

Para incorporar um aplicativo de blog ao vivo, siga o procedimento para incorporar um aplicativo. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). A seguir está um exemplo da aparência de um aplicativo de blog live incorporado.

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

Collectionmeta é um objeto JSON codificado. No exemplo acima, o objeto JSON pega o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## Objeto networkconfig {#c-networkconfig-object}

`NetworkConfig` O objeto é um objeto JSON que personaliza o sistema de autenticação para usuários da rede.

`NetworkConfig` O objeto é um objeto JSON que contém os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **Authdelegate** | *required* object | Usado para personalizar o sistema de autenticação para usuários personalizados da rede. |
| **rede** | *string necessária* um nome de rede fornecido pelo Livefyre. Por exemplo: *yourname. fyre. co.* |
| **Attachmentdelegate** | *optional* object | Usado para especificar os tipos de anexos de mídia visíveis no fluxo do aplicativo. Para obter mais informações, consulte [Restringir mídia](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strings** | *optional* object | Usado para personalizar strings de texto dos elementos HTML em qualquer um dos aplicativos do Livefyre principais. Para obter mais informações, consulte [Personalizações de cadeia de caracteres](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Objeto convconfig {#c-convconfig-object}

`convConfig` O objeto é um objeto JSON usado para especificar o conteúdo renderizado pelo aplicativo Livefyre na página.

>[!NOTE]
>
>Os `convConfig` parâmetros de objeto listados aqui não se aplicam ao aplicativo de Revisão. Para obter informações de integração sobre o aplicativo Resenhas usando `convConfig` o objeto, consulte Integração de revisões.

O `ConvConfig` objeto contém os seguintes parâmetros obrigatórios:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **Articleid** | *required* string | Identifica exclusivamente uma coleção dentro do site. Geralmente, isso corresponde a uma chave primária ou ID de publicação do banco de dados em seu CMS. Por exemplo: «pós -42». Limite de 255 caracteres. Observação: Se você usar o URL do artigo como articleid, certifique-se de que a sequência seja MD 5 ou SHA -1 codificada. |
| **Collectionmeta** | *required* string | Metadados codificados JWT sobre a Coleção. Consulte collectionmeta Object para obter mais informações. |
| **el** | *required* string | A ID de um elemento DOM ao qual o fluxo de conteúdo será renderizado. |
| **Siteid** | *required* string | A ID do Livefyre fornecida para o site ou aplicativo ao qual a coleção pertence. Por exemplo: «303617». |

>[!NOTE]
>
>O `app` parâmetro não é necessário para uma implementação de Aplicativo de comentários.

O `ConvConfig` objeto também pode conter os seguintes parâmetros opcionais:

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **Actionbuttons** | *optional* array | Uma matriz de botões de ação personalizada a serem adicionados a um conteúdo ao lado dos botões Compartilhar e Sinalizar. Para obter mais informações, consulte Adicionar botões personalizados. |
| **animações** | *optional* boolean | Define se as animações serão executadas no aplicativo Livefyre. Defina como falso para desativar animações. Assume como padrão o padrão. |
| **Anonymousflaggingenabled** | booleano | Define se os usuários convidados têm a opção de sinalizar conteúdo. O padrão é verdadeiro. |
| Browsertype | *optional* String | Define o dispositivo para o qual o conteúdo da exibição deve ser gerado. Isso fará com que o CSS e alguma funcionalidade sejam alterados para se ajustar ao tipo de dispositivo de entrada. As opções são desktop, móvel ou tablet. (Se deixado em branco, o agente do Google assumirá a determinação do formato de exibição.) |
| **checksum** | *sequência opcional* (recomendado) | Identifica o estado atual de collectionmeta. Alterar esse valor fará com que o Livefyre atualize os dados no servidor com os novos valores em collectionmeta. |
| **Datetimeformat** | *função de* objeto string opcional | Especifica o formato de datetime do conteúdo transmitido. Para obter mais informações, consulte Personalizar carimbos de data e hora. |
| Disableavatars | *optional* boolean | Impede a renderização dos avatars no fluxo do aplicativo e, portanto, reduz o número de itens carregados no navegador. O padrão é false. |
| disableIE8Shim | *optional* boolean | Desativa o shiv padrão usado pelo Livefyre para preencher o Internet Explorer 8 de forma que os elementos HTML 5 sejam suportados. O Livefyre usa o seguinte projeto: [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . O padrão é false. Observação: Se esse valor for falso, o polimento de alguma classificação deverá ser usado antes que o Livefyre Chat seja chamado para suporte ao Internet Explorer 8. |
| **Disablethirdpartyanalytics** | *optional* boolean | Desativa os sistemas de análise de terceiros (Quantserve e Google Analytics) que o Livefyre pode usar para medições internas. O padrão é false. |
| **Editorcss** | *optional* object | Usado para personalizar o estilo do editor de comentários. Você pode estilo a cor de fundo do campo do editor, bem como a cor, o tamanho e a família da fonte do texto que aparece dentro do editor. Por exemplo: {background: &#39; # ccc &#39;, cor: &#39; red &#39;, font: &#39; 30 px&#39;Helvetica Neue &quot;, Helvetica, Arial, Geneva, sans-serif &#39;} |
| **Initialnumvisible** | *optional* integer | Permite definir o número padrão de comentários visíveis no aplicativo após a carga. Pode ser um número inteiro de 1 a 50. |
| **Initialnumvisiblelegacy** | *optional* integer | Permite definir o número padrão de itens de conteúdo herdados visíveis no aplicativo após a carga. Pode ser um número inteiro de 1 a 50. Se esse parâmetro não for especificado, o padrão será initialnumvisible. Por exemplo: Se a coleção incluir comentários legados 100 ativos e 100, defina initalnumvisible: 10 e initialnumvisiblelegacy: 5, para exibir 10 comentários ativos (com um botão Mostrar mais) + 5 comentários (com um botão Mostrar mais). |
| **Maxvisible** | *optional* integer | Define o número máximo de partes visíveis de conteúdo de nível superior no aplicativo de bate-papo. Se novas partes do fluxo de conteúdo fizerem parte, o conteúdo na parte inferior do fluxo será removido da página. Se o botão Mostrar mais… for clicado, o parâmetro será ignorado e o usuário será gratuito para mostrar o conteúdo desejado. (Use esse parâmetro para controlar o número de itens que aparecem na página em fluxos altos de velocidade.) |
| **Posttobuttons** | *optional* array | Usado para configurar quais provedores são exibidos ao incorporar o aplicativo de blog ao vivo. As opções disponíveis são tw (Twitter), fb (Facebook) e li (linkedin). Padrões para [ tw, fb ]. |
| **Readonly** | *optional* boolean | Desativa toda a interatividade para a Coleção. Quando verdadeiro, os usuários não conseguirão fazer logon no stream e não poderão Publicar, Editar, Responder ou Curtir conteúdo. Quando verdadeiro, os usuários poderão sinalizar e compartilhar conteúdo. O padrão é false. |
| **stream** | *optional* object | Contém opções para configurar o streaming do aplicativo. |
| stream. catchup | *optional* integer | Especifica o número de segundos antes do momento atual que o stream deve carregar. Por padrão, o Livefyre carrega 50 partes de conteúdo e carrega todo o conteúdo enviado entre eles e o momento atual. Em casos de uso muito rápido, o conteúdo pode ser postado rapidamente para permitir que o aplicativo &quot;capture&quot; para o presente. Use essa configuração para definir o número de segundos antes para o qual o conteúdo será publicado (após a carga do conteúdo inicial). |
| **stream. delay** | *optional* integer | Especifica o número de segundos entre as solicitações de transmissão. Use esse parâmetro para ajudar a controlar o fluxo de conteúdo e atrasar a frequência com que o DOM é atualizado. Observação: Se definido muito grande, o stream pode ficar inativo. |


>[!NOTE]
>
>Você pode passar um ou mais `convConfig` objetos durante a inicialização do aplicativo para exibir vários aplicativos na mesma página. Observe que os aplicativos adicionais usam recursos do navegador e o desempenho pode piorar conforme o número aumenta.

## Collectionmeta Object {#c-collectionmeta-object}

`CollectionMeta` O objeto é um objeto JSON que especifica os metadados para armazenar na coleção.

`CollectionMeta` é sempre codificado antes de ser passado para o Livefyre para segurança. O valor codificado é passado para o `ConvConfig` objeto mostrado acima.

>[!NOTE]
>
>É necessário adicionar código do lado do servidor para codificar o `CollectionMeta` objeto JSON. Consulte Criar tokens do servidor para obter mais informações.

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| **Articleid** | *required* string | Uma ID exclusiva para a Coleção. |
| **title** | *required* string | O título que você deseja aplicar à Coleção. Isso geralmente corresponde ao título da página que exibe o Aplicativo. Por exemplo: «A integração é tão divertida! » Observação: A extensão máxima de caracteres do título é de 255 caracteres. O campo de título não suporta entidades HTML. Codifice caracteres especiais usando UTF -8. |
| **url** | *required* string | O URL canônico canônico que deseja anexar a esta coleção. Esse URL será usado para gerar links de volta ao aplicativo a partir de conteúdo compartilhado no Facebook e Twitter, notificações por email e Livefyre Studio. Observação: O Livefyre exige o uso de um nome de domínio totalmente qualificado; o número da porta ou uma chamada de retorno para resolver a configuração local não é necessária. Se estiver testando localmente, certifique-se de usar um domínio de URL base válido. (Por exemplo: `https://customer.com` é válido, embora `https://localhost:5995` não seja.) Depois que você configurar seu servidor Web local para aceitar um nome de domínio totalmente qualificado, não será necessário retornar chamadas ou resoluções, e o desenvolvimento local poderá continuar conforme esperado. |
| **type** | *required* String | O tipo de coleção. Deve ser livechat. |

O `CollectionMeta` objeto também pode conter o seguinte parâmetro opcional:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| **tags** | *optional* string | Uma lista separada por vírgulas ou frases separadas. Pesquisar coleções por tags no Studio ou com a API de pesquisa. **Observação:** Embora as tags adicionadas por meio do Studio possam conter espaços, as tags inseridas por meio da API não podem. Use sublinhados para definir tags que exibirão espaços na interface do usuário. (Por exemplo: use Second_ Quarterback para exibir o Quarterback da segunda-feira no Studio.) |

## Adicionar um manipulador de eventos {#concept_D835C710A7214F6D921571E0770B6BC5}

Para registrar manipuladores de evento, use a chamada de widget. on na função de retorno de chamada do aplicativo.

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

