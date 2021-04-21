---
description: Execute testes de estresse na plataforma Livefyre.
title: Política de teste de estresse
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Política de teste de estresse{#stress-test-policy}

Execute testes de estresse na plataforma Livefyre.

Este documento fornece orientação sobre a execução de testes de estresse na plataforma Livefyre. O teste ad hoc por clientes sem notificação é estritamente proibido. Para obter mais informações sobre [atividades proibidas e permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Os testes de estresse são opcionais. Você não é obrigado ou espera-se que realize um teste de estresse. Adobe Livefyre realiza testes de estresse e validações regulares como parte do processo de lançamento. Se você optar por executar testes, este documento descreve os requisitos e restrições para realizar testes de estresse.

## Notificação {#section_ihs_bfz_vdb}

Você deve notificar seu especialista em sucesso do cliente Livefyre e consultor técnico do Adobe dos testes planejados três ou mais semanas antes de quando planeja começar.

Para notificar o Livefyre, envie as seguintes informações para seu especialista em sucesso do cliente Livefyre e consultor técnico do Adobe:

* Objetivo e descrição do ensaio
* Caso de uso contra o qual você está testando
* Lista de quaisquer APIs do Livefyre que você planeja usar no teste
* Data, hora e duração do teste
* Endereços IP a partir dos quais você iniciará os testes

## Exigências {#section_khs_bfz_vdb}

Você pode realizar testes somente se eles atenderem aos seguintes requisitos:

* Você deve receber aprovação expressa por escrito de um consultor técnico da Adobe 3 semanas ou mais antes de começar o teste.
* **Você só pode realizar testes na rede UAT.**
* Você deve testar cenários realistas. Por exemplo, você pode não assumir que sua propriedade atenderá *milhões* de solicitações de publicação todos os dias, pois esse não é um cenário realista. Se precisar de assistência para determinar se o cenário é realista ou não, pergunte ao especialista em sucesso do cliente Livefyre ou consultor técnico Adobe.
* Os testes devem ser realizados durante o horário comercial para o fuso horário padrão do Pacífico \(UTC -7\).
* Talvez seja necessário produzir dados e seu raciocínio para o teste.

## Governança {#section_mhs_bfz_vdb}

O Livefyre reserva-se o direito de encerrar um teste a qualquer momento se você executar um teste:

* Na Rede de Produção.
* Sem a aprovação expressa e por escrito de um consultor técnico da Adobe com três semanas de antecedência ou mais.
* Contra cenários irreais.

O Livefyre encerra os testes bloqueando o acesso às APIs, desativando as redes Livefyre e recusando uma solicitação de teste de carga se não atender aos requisitos.
