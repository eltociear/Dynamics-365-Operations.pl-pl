---
title: Kończenie zlecenia produkcyjnego
description: W tej procedurze pokazano sposób kończenia zlecenia produkcyjnego.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555846"
---
# <a name="end-a-production-order"></a>Kończenie zlecenia produkcyjnego

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tej procedurze pokazano sposób kończenia zlecenia produkcyjnego. Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej USMF. Jest to ostatnia z siedmiu procedur, które wyjaśniają cykl życia zlecenia produkcyjnego.


## <a name="end-a-production-order"></a>Kończenie zlecenia produkcyjnego
1. Wybierz kolejno opcje Kontrola produkcji > Zlecenia produkcyjne > Wszystkie zlecenia produkcyjne.
    * Zaznacz zlecenie produkcyjne o stanie Zgłoszone jako gotowe.  
2. W okienku akcji kliknij opcję Zlecenie produkcyjne.
3. Kliknij opcję Koniec.
    * Na tej stronie możesz potwierdzić, że chcesz zakończyć zlecenie produkcyjne.  
4. Kliknij kartę Ogólne.
5. W polu Data wprowadź datę.
6. W polu Metoda odpadków wybierz opcję „Alokacja”.
    * Po wybraniu metody alokacji koszty z materiałów uznanych za odpadki są dodawane do wyrobów gotowych.  
7. Kliknij przycisk OK.

## <a name="validate-calculation-results"></a>Sprawdzanie poprawności wyników obliczeń
1. W okienku akcji kliknij pozycję Zarządzanie kosztami.
2. Kliknij przycisk Wyświetl porównanie kosztów.
    * Po zakończeniu zlecenia produkcyjnego można porównywać szacowany koszt własny ze zrealizowanym kosztem własnym w celu uzyskania obrazu odchyleń względem kosztów produkcji.  
