---
description: Conte o número de itens sociais com curadoria.
seo-description: Conte o número de itens sociais com curadoria.
seo-title: Contador social
solution: Experience Manager
title: Contador social
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Contador social{#social-counter}

Conte o número de itens sociais com curadoria. Para obter uma lista completa dos pontos de extremidade disponíveis, consulte a seção Referência [da](https://api.livefyre.com/docs) API Livefyre.

A API Contador Social retorna contagens de regras de curadoria correspondentes em uma determinada coleção para intervalos ao longo de um período de tempo.

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

* **** networkName: Seu Livefyre forneceu o nome da rede. Por exemplo: *laboratórios* em `labs.fyre.co`.
* **** consulta: O hash codificado em base64 para url de todo o site, a ID do artigo, os tuplos do tipo de regra para os quais as informações de contagem devem ser buscadas (pré-codificadas)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >A consulta é limitada a 10 sites, ID de artigo, tuplas de tipo de regra. (O exemplo anterior contém 3 tuplas.)

* **from** `(optional)` especifica o período de tempo relativo ou absoluto para gráfico; from especifica o início e o padrão é 24 horas atrás, se omitido.
* **até** `(optional)` especificar o período de tempo relativo ou absoluto para o gráfico; até especificar o início e o padrão para a hora atual (agora), se omitido.

### Tempo relativo

| Abreviação | Unidade |
|---|---|
| s | Segundos |
| min | Minutos |
| h | Horas |
| d | Dias |
| w | Semanas |
| mon | 30 dias (mês) |
| y | 365 Dias (Ano) |

Exemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tempo absoluto {#section_xqr_jgc_11b}

FORMATO: HH:MM_YYYMMDD

| Abreviação | Significado |
|---|---|
| HH | Horas (no formato de relógio 24h) |
| MM | Minutos |
| YYYY | Ano de 4 dígitos |
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

Para obter contagens no último minuto para a ID do site `123456` e do artigo `some-article-id` e tipo de regra `2`, por exemplo: `123456:some-article-id;2:`

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
