---
description: Instalação das bibliotecas do Livefyre Server-side tarefa
seo-description: Instalação das bibliotecas do Livefyre Server-side tarefa
seo-title: Instalação
solution: Experience Manager
title: Instalação
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---


# Instalação{#installation}


## Java {#section_yd3_3zk_rz}

Para instalar a biblioteca Java, adicione essa dependência ao POM do seu projeto:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

A biblioteca Java possui dependências nos seguintes módulos:

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Para obter mais informações, leia os documentos do Java ou consulte a fonte em [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Para instalar a biblioteca NodeJS, execute esta linha:

`$ npm install livefyre`

A biblioteca NodeJS tem dependências nos seguintes módulos:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Para obter mais informações, leia os documentos do NodeJs ou consulte a fonte em [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Links: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Para instalar a biblioteca PHP com o Composer, adicione isso ao seu composer.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Em seguida, instale usando:

```
composer.phar install 
```

Se você **not** usar o Composer, obtenha a versão mais recente da biblioteca usando:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Para usar a biblioteca, adicione o seguinte ao script PHP:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

A biblioteca PHP tem dependências nos seguintes módulos:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Para obter mais informações, leia os documentos PHP ou consulte a fonte em [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Links: [ext-json](https://php.net/manual/en/book.json.php), [Pedidos](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Para instalar a biblioteca Python, execute esta linha:

`$ pip install livefyre`

A biblioteca Python tem dependências nos seguintes módulos:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Para obter mais informações, leia os documentos Python ou consulte a fonte em [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Links: [PyJWT](https://github.com/progrium/pyjwt), [Pedidos](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Para instalar a biblioteca Ruby, adicione esta linha ao arquivo Gemfile de seu aplicativo:

```
gem 'livefyre' 
```

Ou instale-o você mesmo:

`$ gem install livefyre`

A biblioteca Ruby tem dependências nos seguintes módulos:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Para obter mais informações, leia os documentos Ruby ou consulte a fonte em [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Links: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [Endereçável](https://github.com/sporkmonger/addressable)
