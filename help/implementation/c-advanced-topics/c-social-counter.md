---
description: Conte o número de itens sociais preparados.
title: Contador social
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 10%

---

# Contador Social{#social-counter}

Conte o número de itens sociais preparados. Para obter uma lista completa de endpoints disponíveis, consulte a seção Livefyre [API Reference](https://api.livefyre.com/docs) .

A API do contador social retorna contagens de regras de preparação correspondentes em uma determinada coleção para intervalos ao longo de um período.

>[!NOTE]
>
>Essa API está disponível somente para hashtags do Twitter.

API do contador social:

* Recurso
* Tipos de regras
* Resposta

## Recurso {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Seu Livefyre forneceu o nome da rede. Por exemplo: *labs* em `labs.fyre.co`.
* **consulta:** o hash codificado base64 seguro para url de todo o site, ID do artigo, tuplos do tipo regra para os quais as informações de contagem devem ser buscadas (pré-codificadas)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >O query é limitado a 10 sites, ID de artigo, tuplos de tipo de regra. (O exemplo anterior contém 3 tuplas.)

* **** `(optional)` especifica o período relativo ou absoluto para o gráfico; from especifica o início e o padrão é 24 horas atrás, se omitido.
* **** `(optional)` especifica o período de tempo relativo ou absoluto para o gráfico; até especifica o início e o padrão é a hora atual (agora), se omitida.

### Hora relativa

| Abreviação | Unidade |
|---|---|
| s | Segundos |
| min | Minutes |
| h | Horas |
| d | Dias |
| w | Semanas |
| gemido | 30 Dias (Mês) |
| y | 365 Dias (Ano) |

Exemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tempo absoluto {#section_xqr_jgc_11b}

FORMATO: HH:MM_AAAAAMDD

| Abreviação | Significado |
|---|---|
| HH | Horas (em formato de relógio de 24 horas) |
| MM | Minutes |
| YYYY | Ano de 4 Dígitos |
| MM | Mês |
| DD | Dia |

Exemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Tipos de regras {#section_v53_xqb_11b}

| Valor | Tipo |
|---|---|
| 2 | Twitter |

Exemplo:

Para obter contagens no último minuto para o site `123456` e a ID do artigo `some-article-id` e o tipo de regra `2`, por exemplo: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Exemplo de resposta:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
