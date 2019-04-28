---
description: Insira anúncios em seu fluxo de Comentários.
seo-description: Insira anúncios em seu fluxo de Comentários.
seo-title: Anúncios em comentários
solution: Experience Manager
title: Anúncios em comentários
uuid: f 8 d 6372 f -4468-4884-a 384-116180 b 4 c 748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Anúncios em comentários{#ads-in-comments}

Insira anúncios em seu fluxo de Comentários.

## Anúncios em comentários {#topic_CDD2ACF16AED4DE782725EE90089C04E}

Insira anúncios em seu fluxo de Comentários.

O recurso Publicidades do Livefyre no recurso Comentários permite que você injete anúncios em seu fluxo de comentário, defina a frequência com a qual os anúncios aparecem no stream e para criar as assinaturas síncronas e assíncronas de injeção de anúncio.

O Livefyre fornece o contêiner pelo qual você pode inserir um anúncio usando seu provedor de Soluções de gerenciamento de anúncio.

Para introduzir um anúncio, passe dois valores do Livefyre:

* A frequência na qual o anúncio deve ser inserido no Fluxo de comentário
* Uma função que serve o anúncio apropriado.

>[!NOTE]
>
>Os anúncios serão renderizados somente quando o posicionamento do anúncio estiver no visor. Os anúncios serão mostrados somente após os comentários pai (e não os encadeamentos), e os usuários não poderão comentar nesses anúncios. Essa API não permite que você especifique o tamanho do elemento no qual seus anúncios serão colocados.

## Integração {#concept_C99029E618EC49779E3117D2C303E4F1}

Para usar este recurso, crie um elemento div na página em que os anúncios serão colocados e, em seguida, passe o HTML do provedor de anúncio.

O Livefyre fornece dois tipos de posicionamento de anúncios: sincronizado e assíncrono. Ambos os tipos carregam seus anúncios somente quando o usuário rola a página de forma que a posição do anúncio esteja na visualização. Ambos também exigem que você retorne um elemento DOM (iframe ou div).

Para obter o anúncio, o método síncrono chama um repositório local, enquanto as chamadas assíncronas a um serviço externo.

### Síncrono

Para criar uma disposição síncrona, inclua o anúncio no delegado e volte ao próprio elemento de publicidade. O método síncrono chama um repositório local, permitindo que você controle sua própria geração de anúncios.

### Assíncrono

O método assíncrono exige que o elemento seja inserido no DOM antes de chamar o provedor de publicidade. Em seguida, seu provedor determina qual publicidade deve ser enviada e a retorna.

Para implementar anúncios assíncronos, crie um delegado que retorne um elemento no qual o anúncio será colocado e um retorno de chamada que fará o posicionamento do anúncio. O elemento retornado no delegado deve ter uma id exclusiva para o anúncio ser direcionado. O retorno de chamada inserirá o anúncio no elemento fornecido pela id exclusiva.

>[!NOTE]
>
>Dependendo do seu provedor de publicidade, o retorno de chamada se comportará de forma diferente.

Quando a página é carregada, os Anúncios em Comentários acessarão o delegado, digitam o elemento e, em seguida, chama o retorno de chamada que atualiza o elemento (definido anteriormente) com o anúncio.

## Parâmetros {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

Os parâmetros a seguir estão disponíveis para uso com esta chamada.

Para o objeto do anúncio:

* **atraso:****(opcional) integer** - define o número de comentários após o qual o primeiro anúncio será exibido. O padrão é 10.
* **frequência: (opcional) integer** - define o número de comentários depois que cada anúncio subsequente será exibido. Por exemplo: Digite 2 para exibir um anúncio como a cada terceiro comentário. O padrão é 10.
* **delegate:*****função necessária*** - A função chamada para introduzir anúncios no fluxo de Comentário.

O objeto delegado oferece suporte para invocações síncronas e assíncronas. O parâmetro que está sendo fornecido à função delegada, os dados, conterão:

* **título:****string** - O título da Coleção.
* **tags:****matriz** - Uma lista de tags associadas à Coleção.
* **id:****string** - O identificador de artigo da Coleção.
* **url:****string** - A URL da Coleção.
* **Networkid:****string** - A ID da rede da Coleção.
* **Siteid:****int** - a ID do site da coleção.

Esses itens são passados por meio do objeto convconfig em nosso exemplo e são explicados com mais detalhes [na](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) seção Introdução.

### Síncrono

O delegado retorna um objeto que contém:

* **elemento:*****elemento*DOM necessário** - o elemento que contém a publicidade a ser inserida no aplicativo.

**Assíncrono**: O delegado retorna um objeto que contém: O delegado retorna um objeto que contém duas propriedades: elemento e retorno de chamada:

* **elemento:*****elemento*DOM necessário** - o elemento que contém a publicidade a ser inserida no aplicativo.
* **retorno de chamada:*****função necessária*** - o retorno de chamada que manipulará a inserção do anúncio no elemento DOM acima.

Para o `Conv` objeto, é possível passar uma sequência de caracteres para indicar o título da seção do anúncio:

* **strings:****(opcional)** - Usado para personalizar o texto do cabeçalho de seus anúncios. «Patrocinado» por padrão.

## Exemplo síncrono {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## Exemplo assíncrono {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
