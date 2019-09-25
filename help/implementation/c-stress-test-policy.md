---
description: Executar testes de esforço contra a plataforma Livefyre.
seo-description: Executar testes de esforço contra a plataforma Livefyre.
seo-title: Política de teste de stress
solution: Experience Manager
title: Política de teste de stress
uuid: f2d49b55-f4fc-485f-9aea17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Política de teste de stress{#stress-test-policy}

Executar testes de esforço contra a plataforma Livefyre.

Este documento fornece orientação sobre a execução de testes de esforço contra a plataforma Livefyre. Os testes ad hoc realizados pelos clientes sem notificação são estritamente proibidos. Para mais sobre atividades [proibidas e permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Os testes de stress são opcionais. Você não é obrigado ou deve realizar um teste de estresse. O Adobe Livefyre realiza testes de estresse e validações regulares como parte do processo de lançamento. Se você optar por executar testes, este documento descreve os requisitos e restrições para a realização de testes de estresse.

## Notificação {#section_ihs_bfz_vdb}

Você deve notificar o especialista em sucesso do cliente Livefyre e o consultor técnico da Adobe sobre os testes planejados três ou mais semanas antes de iniciar.

Para notificar o Livefyre, envie as seguintes informações ao especialista em sucesso do cliente Livefyre e ao consultor técnico da Adobe:

* Objetivo e descrição do ensaio
* Caso de uso contra o qual você está testando
* Lista de todas as APIs do Livefyre que você planeja usar no teste
* Data, hora e duração do teste
* Endereços IP dos quais você iniciará os testes

## Exigências {#section_khs_bfz_vdb}

Você só pode realizar testes se eles atenderem aos seguintes requisitos:

* Você deve receber uma aprovação explícita, por escrito, de um consultor técnico da Adobe por 3 semanas ou mais antes de começar o teste.
* **Você só pode realizar testes na rede UAT.**
* Você deve testar em relação a cenários realistas. Por exemplo, você pode não supor que sua propriedade atenderá *milhões* de solicitações de postagem todos os dias, porque esse cenário não é realista. Se precisar de assistência para determinar se o cenário é realista ou não, pergunte ao especialista em sucesso do cliente Livefyre ou ao consultor técnico da Adobe.
* Os testes devem ser realizados durante o horário comercial para o fuso horário padrão do Pacífico \(UTC -7\).
* Talvez seja necessário produzir dados e seu raciocínio para o teste.

## Governação {#section_mhs_bfz_vdb}

Livefyre reserva-se o direito de encerrar um teste a qualquer momento se você executar um teste:

* Na Rede de produção.
* Sem a aprovação expressa por escrito de um consultor técnico da Adobe com três semanas ou mais de antecedência.
* Contra cenários irreais.

O Livefyre encerra os testes bloqueando o acesso às APIs, desabilitando a Livefyre Networks e recusando uma solicitação de teste de carga se ela não atender aos requisitos.
