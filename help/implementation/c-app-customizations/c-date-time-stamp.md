---
description: Personalize os carimbos de data e hora usando o Livefyre. js.
seo-description: Personalize os carimbos de data e hora usando o Livefyre. js.
seo-title: Personalizar o carimbo de data e hora
solution: Experience Manager
title: Personalizar o carimbo de data e hora
uuid: 632 ea 405-56 b 7-4d 64-8 d 2 b -0 dd 0 a 7611 bd 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Personalizar o carimbo de data e hora{#customize-the-date-and-time-stamp}

Personalize os carimbos de data e hora usando o Livefyre. js.

Os aplicativos do Livefyre fornecem o parâmetro de opção, datetimeformat, para especificar o formato de data conforme descrito abaixo.

* [Terminologia](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatação](#c_date_time_stamp/section_ynx_gn4_xz)
* [Designação de símbolo](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologia {#section_xsk_jn4_xz}

* **Os carimbos de data e hora** absolutos são definidos como momentos exatos e específicos (por exemplo, January de janeiro de 2010pm 2:00)
* **Os carimbos de data e hora** relativos são definidos como horários gerais e menos precisos (por exemplo, 25 segundos atrás, 14 minutos atrás, 1 dia atrás, 1 ano atrás etc.)

## Formatação {#section_ynx_gn4_xz}

O parâmetro datetimeformat tem o seguinte comportamento padrão quando nenhum argumento é dado:

* Formato Datetime de: MMMM d yyyy (para 8 de janeiro de 2012)
* 20160 minutos (14 dias) até o tempo absoluto (14 dias até que carimbos de data e hora relativos se tornem carimbos de data e hora absolutos)

O parâmetro datetimeformat aceita três tipos de argumentos possíveis: datetime, format e string.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Um objeto que especifica absoluteformat e/ou minutesuntilabsolutetime. Um minutesuntilabsolutetime com um valor -1 tornará o tempo absoluto de tempo absoluto.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Uma função que assume como argumento um objeto Date e retorna uma string de datetime a ser exibida

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Designação de símbolo {#section_inq_2n4_xz}

As funções de formatação Datetime seguem a especificação de padrão, conforme definido no JDK, ICU e CLDR, com modificação pequena para uso típico no JS. Para obter mais informações, consulte a Documentação da Biblioteca de fechamento [do Google](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Os itens marcados com ' *' ainda não são suportados.

Os itens marcados com ' #' funcionam de forma diferente do Java.

A contagem de letras padrão determina o formato.

* **Texto:** 4 ou mais, use formulário completo. Menos que 4, use formulário abreviado ou abreviado se ele existir. (Por exemplo: «EEEE» produz «Segunda-feira», «EEE» produz «Mon».
* **Número:** o número mínimo de dígitos. Números mais curtos são adicionados a zero a esta quantia (por exemplo: Se «m» produzir «6», «mm» produz «06». O ano é manipulado especialmente; ou seja, se a contagem de "y" for 2, o ano será truncado para 2 dígitos. (Por exemplo: se «yyyy» produzir «1997», «yy» produz «97».) Diferentemente de outros campos, os segundos fracionais são padicionados à direita com zero.
* **Texto e número:** 3 ou mais, use texto. Menos que 3, use o número. (Por exemplo: «M» produz «1», «MM» produz «01», «MMM» produz «Jan» e «MMMM» produz «janeiro».

Qualquer caractere no padrão que não esteja nos intervalos [de «a». 'z'] e ['A '. 'Z'] será tratado como texto como citação. Por exemplo, caracteres como ": ','. ',',' #' e ' @' aparecerão no texto de tempo resultante mesmo que não sejam incorporados em aspas simples.
