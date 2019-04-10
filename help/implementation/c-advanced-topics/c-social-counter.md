---
description: Conte o número de itens sociais preparados.
seo-description: Conte o número de itens sociais preparados.
seo-title: Contador social
solution: Experience Manager
title: Contador social
uuid: fa 9 aa 1 a 8-6 a 04-4 bc 1-9 bfe-e 42 c 1250 fd 48
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Contador social{#social-counter}

Conte o número de itens sociais preparados. Para obter uma lista completa de endpoints disponíveis, consulte a seção Referência [da API](https://api.livefyre.com/docs) do Livefyre.

A API de contador do Social retorna contagens para regras de curadoria correspondentes em uma determinada coleção para intervalos durante um período de tempo.

>[!NOTE]
>
>Essa API está disponível somente para hashtags do Twitter.

API de contador social:

* Recurso
* Tipos de regras
* Resposta

## Recurso {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **Networkname:** Seu nome de rede fornecido pelo Livefyre. Por exemplo: ** em `labs.fyre.co`.
* **query:** O hash codificado com base em url 64 de todo o site, ID do artigo, tuitos do tipo de regras para as quais as informações de contagem devem ser buscadas (pré-codificadas)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >A consulta está limitada a 10 site, a ID do artigo, as tuimes do tipo de regra. (O exemplo anterior conteria 3 pontos.)

* **de** `(optional)` especifica o período relativo ou absoluto para o gráfico; de especifica o início e padrão há 24 horas, se omitido.
* **até** `(optional)` especifica o período relativo ou absoluto para o gráfico; até que seja especificado o início e padrão do tempo atual (agora), se omitido.

### Tempo relativo

| Abreviação | Unidade |
|---|---|
| s | Segundos |
| min | Minutos |
| h | Horas |
| d | Dias |
| w | Semanas |
| mon | 30 dias (mês) |
| y | 365 dias (ano) |

Exemplo:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Tempo absoluto {#section_xqr_jgc_11b}

FORMAT: HH: MM_ AAAAMMDD

| Abreviação | Significado |
|---|---|
| HH | Horas (em formato de relógio de 24 h) |
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

Para obter contagens no último minuto para a ID do site `123456` e do artigo `some-article-id` e o tipo de regra `2`, por exemplo: `123456:some-article-id;2:`

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
