---
title: Aktualizacje fizyczne i finansowe
description: "W tym temacie przedstawiono typy transakcji, które przekładają się na zwiększanie lub zmniejszanie ilości zapasów."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a0eeb5a57f9b82150150752c64e89c2c91856889
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017

---

# <a name="physical-and-financial-updates"></a>Aktualizacje fizyczne i finansowe

[!include[banner](../includes/banner.md)]


W tym temacie przedstawiono typy transakcji, które przekładają się na zwiększanie lub zmniejszanie ilości zapasów. 

W programie Microsoft Dynamics 365 for Finance and Operations transakcje magazynowe można zaktualizowane fizycznie i finansowo. Niektóre typy transakcji fizycznych i finansowych zwiększają ilości zapasów, podczas gdy inne je zmniejszają.

## <a name="physical-increases"></a>Wzrost fizyczny
Po zaksięgowaniu transakcji fizycznej stan tej transakcji przyjmuje wartość **Otrzymano**. Oto transakcje, które stanowią wzrost fizyczny:

-   zamówienie zakupu — przychód,
-   zwrot dokumentu dostawy zamówienia sprzedaży,
-   Zgłaszanie zlecenia produkcyjnego jako zakończonego
-   według produktów na liście pobrania zlecenia produkcyjnego.

## <a name="financial-increases"></a>Wzrost finansowy
Po zaksięgowaniu finansowej transakcji przychodu stan rekordu tej transakcji powodującej zwiększenie ilości przyjmuje wartość **Zakupiono**. Oto transakcje, które stanowią wzrost finansowy:

-   Faktura dostawcy
-   faktura zamówienia zakupu do zwrotu,
-   wycena zlecenia produkcyjnego,
-   Arkusze magazynowe z ilością dodatnią, takie jak przeniesienie, zyski i straty, zliczanie, BOM i przeniesienie.

## <a name="transactions-that-increase-quantity"></a>Transakcje, które zwiększają ilość
Transakcje zwiększające ilość są księgowane według dynamicznych średnich kosztów własnych. Po zaksięgowaniu transakcji zwiększających ilość program Finance and Operations oblicza średnią kroczącą kosztu własnego na podstawie tych wszystkich transakcji dla każdego wymiaru zapasów podlegającego śledzeniu finansowemu. Aby uzyskać informacje o uruchamianiu średnich kosztów własnych, zobacz [Dynamiczne średnie koszty własne](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transakcje, które zmniejszają ilość
Finance and Operations używa obliczonej średniej kroczącej kosztu własnego podczas księgowania transakcji, która zmniejsza ilość, niezależnie od tego, który model zapasów jest powiązany z danymi zapasami. Wymaga to, aby transakcja, która zmniejsza ilość nie została wcześniej oznaczona dla innej transakcji przed zaksięgowaniem. Jeśli fizycznie dostępne zapasy osiągną ilość ujemną, w programie Finance and Operations jest używany koszt zapasów zdefiniowany dla towaru na stronie **Pozycja**. **Uwaga:** Jeśli włączono funkcję wielooddziałowości, to koszt ten będzie zastępczo używany jako koszt magazynowy, zdefiniowany dla oddziału na stronie **Ustawienia domyślne zamówień**.

## <a name="physical-issues-vs-financial-issues"></a>Rozchody fizyczne a finansowe
Po zaksięgowaniu transakcji fizycznego rozchodu stan rekordu transakcji przyjmuje wartość **Zmniejszono**. Oto transakcje stanowiące fizyczne rozchody:

-   arkusz listy pobrań zlecenia produkcyjnego,
-   dokument dostawy zamówienia sprzedaży,
-   zwrot dokumentu dostawy zamówienia zakupu.

Po zaksięgowaniu transakcji finansowej stan rekordu tej transakcji przyjmuje wartość **Sprzedano**. Oto transakcje stanowiące finansowe rozchody:

-   Kończenie zlecenia produkcyjnego
-   Faktura dla zamówienia sprzedaży
-   Zwrot z faktury od dostawcy
-   Arkusze magazynowe z ilością ujemną, takie jak przeniesienie, zyski i straty, zliczanie, BOM i przeniesienie.

Transakcje zmniejszające ilość są księgowane według dynamicznych średnich kosztów własnych. Z tego powodu proces zamknięcia magazynu jest wymagany w celu rozliczenia transakcji rozchodu z transakcjami przychodu, według modelu magazynu przypisanego dla danego towaru.



