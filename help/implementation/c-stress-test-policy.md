---
description: Execute testes de stress na plataforma Livefyre.
seo-description: Execute testes de stress na plataforma Livefyre.
seo-title: Política de teste de stress
solution: Experience Manager
title: Política de teste de stress
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Política de teste de stress{#stress-test-policy}

Execute testes de stress na plataforma Livefyre.

Este documento fornece orientação sobre como executar testes de stress na plataforma do Livefyre. O teste ad-hoc por clientes sem notificação é totalmente proibido. Para mais informações sobre [atividades proibidas e permitidas](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Os testes de stress são opcionais. Não é necessário ou esperado executar um teste de stress. O Adobe Livefyre realiza testes de stress e validações comuns como parte do processo de lançamento. Se optar por executar testes, este documento descreve os requisitos e restrições para a condução de testes de stress.

## Notificação {#section_ihs_bfz_vdb}

Você deve notificar o especialista em sucesso do Livefyre e o consultor técnico da Adobe sobre os testes planejados três ou mais semanas antes de planejar iniciar.

Para notificar o Livefyre, envie as seguintes informações para seu Especialista em sucesso do cliente do Livefyre e Consultor técnico da Adobe:

* Finalidade e descrição do teste
* O caso de uso que você está testando
* Lista de qualquer apis do Livefyre que você planeja usar no teste
* Data, hora e duração do teste
* Endereços IP dos quais você iniciará os testes

## Requisitos {#section_khs_bfz_vdb}

Você só poderá fazer testes se cumprirem os seguintes requisitos:

* Você deve receber uma aprovação explícita e por escrito de um consultor técnico da Adobe 3 semanas ou mais antes de iniciar o teste.
* **Você só pode executar testes na rede UAT.**
* É necessário testar cenários realistas. Por exemplo, talvez você não suponha que sua propriedade oferecerá milhões *de* solicitações de postagem todos os dias, porque isso não é um cenário realista. Se precisar de assistência para determinar se o cenário é realista ou não, pergunte ao especialista em sucesso do Livefyre ou consultor técnico da Adobe.
* Os testes devem ser conduzidos durante o horário comercial para o fuso horário do Pacífico\ (UTC -7\).
* Talvez seja necessário produzir dados e seu raciocínio para o teste.

## Governança {#section_mhs_bfz_vdb}

O Livefyre reserva o direito de encerrar um teste a qualquer momento se você executar um teste:

* Na Rede Produção.
* Sem aprovação explícita e por escrito de um consultor técnico da Adobe três semanas ou mais antecipadamente.
* Contra cenários inreais.

O Livefyre encerra os testes bloqueando o acesso às apis, desabilitar o Livefyre Networks e recusar uma solicitação de teste de carga se não atender aos requisitos.
