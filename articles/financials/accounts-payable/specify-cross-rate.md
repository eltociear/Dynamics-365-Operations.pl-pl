---
title: "Określ kurs krzyżowy"
description: "Ten temat zawiera informacje o kursach krzyżowych w programie Microsoft Dynamics 365 for Finance and Operations."
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: pl-pl
ms.lasthandoff: 08/09/2018

---

# <a name="specify-the-cross-rate"></a>Określ kurs krzyżowy

[!include [banner](../includes/banner.md)]

W tym temacie wyjaśniono przeznaczenie kursu krzyżowego oraz sposobu określania kursu krzyżowego, gdy płatność jest rozliczana z fakturą. Użyć kursu krzyżowego podczas stosowania wszystkich poniższych kryteriów: 
-   W przypadku rozliczania płatności z faktury. 
-   Wiersz płatności i faktura używają różnych walut. 
-   Żadna waluta nie jest walutą rozliczeniową. 

Kurs krzyżowy nie jest używany do obliczania przeliczenia waluty płatności transakcji na walutę rozliczeniową płatności. Zamiast tego w celu obliczenia kwoty w walucie transakcyjnej płatności i kwoty w walucie rozliczeniowej płatności są pobierane kursy wymiany z tabel kursów wymiany. 

Na przykład gdy walutą rozliczeniową jest USD, a CAD jest waluta faktury, wtedy płatności waluty dokonywane są w EUR. Kurs krzyżowy umożliwia wprowadzenie kursu wymiany do przetłumaczenia bezpośrednio między EUR a CAD, a nie jest konieczne tłumaczenie wersji USD. Po wybraniu faktury i płatności głównej dla wiersza faktury można wprowadzić kurs krzyżowy. Kurs ten określa przelicznik między walutami transakcji w dniu dokonania rozliczenia.

1.  Przejdź do jednej z następujących stron:
- **Rozrachunki z odbiorcami > Wspólne > Odbiorcy > Wszyscy odbiorcy** 
- **Rozrachunki z dostawcami > Wspólne > Dostawcy > Wszyscy dostawcy** 
- **Zaopatrzenie i sourcing > Wspólne > Dostawcy > Wszyscy dostawcy**
2.  Wybierz odbiorcę lub dostawcę, dla którego są rozliczane otwarte transakcje. 
3.  Dla odbiorcy na stronie listy **Wszyscy odbiorcy** wybierz kolejno opcje **Windykacja > Rozlicz otwarte transakcje**. Dla dostawcy na stronie listy **Wszyscy dostawcy** wybierz kolejno opcje **Faktura > Rozlicz otwarte transakcje**. 
4.  Wybierz transakcję właściwą dla płatności głównej, a następnie kliknij przycisk **Oznacz płatność**. Pole wyboru w kolumnie **Zaznacz** jest zaznaczone, a ikona informacji jest wyświetlana w kolumnie **Płatność główna**. 
5.  W polu **Kurs krzyżowy** wprowadź przelicznik między walutą faktury a walutą płatności na dzień dokonania rozliczenia. 
