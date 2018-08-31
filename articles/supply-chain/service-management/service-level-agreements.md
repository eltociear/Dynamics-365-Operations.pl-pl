---
title: "Umowy dotyczące poziomu usług"
description: "Podpisując umowę dotyczącą poziomu usług, klient akceptuje minimalny czas reakcji liczony od momentu przyjęcia zgłoszenia przez firmę usługową do chwili rozwiązania problemu."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: pl-pl
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>Umowy dotyczące poziomu usług        

[!include [banner](../includes/banner.md)]


Umowa dotycząca poziomu usług jest zawierana między firmą usługową a klientem korzystającym z jej usług. Podpisując ją, klient akceptuje minimalny czas reakcji liczony od momentu przyjęcia zgłoszenia przez firmę usługową do chwili rozwiązania problemu.

W umowie takiej jest zdefiniowany standardowy poziom usług oferowanych klientom. Ponadto zawarty jest w niej jednoznacznie określony termin wykonania usługi.

W celu zapewnienia klientom różnych poziomów usług można przygotować dowolną liczbę umów dotyczących tych poziomów.

## <a name="create-a-service-level-agreement"></a>Tworzenie umowy dotyczącej poziomu usług

1.  Kliknij kolejno opcje **Zarządzanie serwisem** \> **Ustawienia** \> **Umowy serwisowe** \> **Umowy dotyczące poziomu usług**.

2.  W polu **Umowa dotycząca poziomu usług** nadaj nazwę umowie SLA.

3.  Wprowadź dozwolony czas rozwiązywania problemu zasygnalizowanego w zgłoszeniu serwisowym, do jakiego klient jest uprawniony na mocy umowy dotyczącej poziomu usług. Następnie wybierz kalendarz, jeśli ma on zostać uwzględniony w umowie.

## <a name="apply-a-service-level-agreement"></a>Stosowanie umowy dotyczącej poziomu usług

Umowa dotycząca poziomu usług jest stosowana bezpośrednio do umowy serwisowej.

Zlecenia serwisowe utworzone ręcznie i dołączone do umowy serwisowej z przypisaną umową dotyczącą poziomu usług są analizowane z uwzględnieniem tej drugiej umowy.

Z kolei zlecenia serwisowe utworzone automatycznie nie są dołączane do umowy dotyczącej poziomu usług.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Stosowanie umowy dotyczącej poziomu usług do umowy serwisowej

1.  Kliknij kolejno opcje **Zarządzanie serwisem** \> **Wspólne** \> **Umowy serwisowe** \> **Umowy serwisowe**. Zaznacz umowę serwisową, do której chcesz stosować umowę SLA, a następnie w **okienku akcji** kliknij przycisk **Edytuj**.

2.  W polu **Umowa dotycząca poziomu usług** wybierz umowę SLA, którą chcesz przypisać.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Stosowanie umowy dotyczącej poziomu usług do grupy umów serwisowych

1.  Kliknij kolejno opcje **Zarządzanie serwisem** \> **Ustawienia** \> **Umowy serwisowe** \> **Grupy umów serwisowych**.

2.  W polu **Umowa dotycząca poziomu usług** wybierz umowę SLA, którą chcesz przypisać.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Monitorowanie czasu realizacji zlecenia serwisowego na podstawie umowy dotyczącej poziomu usług

Po utworzeniu nowego zlecenia serwisowego dla umowy serwisowej, która ma przypisaną umowę dotycząca poziomu usług, jest inicjowany przedział czasu na wykonanie usługi, a system zaczyna monitorować czas realizacji. Ponadto można skonfigurować następujące opcje:

  - Istnieje możliwość rozpoczęcia i zatrzymania rejestracji czasu odnośnie do zlecenia serwisowego. Pozwala to zarejestrować łączny czas realizacji zleceń serwisowych.

  - Możliwe jest monitorowanie zgodności z przedziałem czasu zdefiniowanym w umowie dotyczącej poziomu usług.

  - Istnieje możliwość zdefiniowania kodów przyczyn, które muszą zostać określone w przypadku przekroczenia przedziału czasu zdefiniowanego w umowie dotyczącej poziomu usług.

## <a name="see-also"></a>Informacje dodatkowe

[Podgląd zgodności z umowami SLA](view-compliance-with-service-level-agreements.md)

  


