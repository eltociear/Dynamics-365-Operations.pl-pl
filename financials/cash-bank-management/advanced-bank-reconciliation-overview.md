---
title: "Zaawansowanego uzgodnienia konta bankowego — omówienie"
description: "W tym artykule opisano przebieg procesu zaawansowanego uzgadniania konta bankowego. Funkcja zaawansowanego uzgadniania konta bankowego umożliwia importowanie wyciągów bankowych, a następnie ich automatyczne uzgadnianie z poziomu transakcji bankowych."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: deba55d5e1e376f3f4063f372bfe853fcaf20498
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Zaawansowanego uzgodnienia konta bankowego — omówienie

[!include[banner](../includes/banner.md)]


W tym artykule opisano przebieg procesu zaawansowanego uzgadniania konta bankowego. Funkcja zaawansowanego uzgadniania konta bankowego umożliwia importowanie wyciągów bankowych, a następnie ich automatyczne uzgadnianie z poziomu transakcji bankowych.

Funkcja zaawansowanego uzgodnienia konta bankowego pozwala importować wyciągi bankowe. Zaimportowany wyciąg z konta można następnie automatycznie uzgodnić z poziomu transakcji bankowych. Poniżej przedstawiono kroki w procesie zaawansowanego uzgadniania konta bankowego

1.  Konfigurowanie importu wyciągu bankowego.
    -   Importowanie wyciągów bankowych za pośrednictwem struktury danych jednostki.
    -   Trzy typowe formaty wyciągów bankowych są wbudowane: ISO20022, BAI2, i MT940.
    -   Funkcję można rozszerzyć na dowolny format.

2.  Należy ustawić kolejność na potrzeby zaawansowanego uzgadniania konta bankowego i zdefiniować reguł uzgadniania wyciągów bankowych.
    -   Reguły uzgadniania wyciągów to zestaw kryteriów, które są używane do filtrowania podczas procesu uzgadniania wierszy wyciągu bankowego z wierszami transakcji bankowych w programie Microsoft Dynamics 365 for Operations. W zależności od praktyk biznesowych klienta można skonfigurować więcej niż jedną regułę uzgadniania i zautomatyzować oraz zoptymalizować proces uzgadniania.

3.  Uzgadnianie wyciągów bankowych z transakcjami bankowymi w programie Dynamics 365 for Operations.
    -   Automatyczne dopasowywanie i tworzenie arkuszy uzgadniania konta.
    -   Bezpośrednie porównywanie wyciągów bankowych z transakcjami bankowymi w programie Dynamics 365 for Operations.
    -   Automatyczne księgowanie transakcji bankowych w programie Dynamics 365 for Operations, jeśli pojawiają się na wyciągu bankowym, ale nie ma ich w programie Dynamics 365 for Operations.
    -   Generowanie wyciągu uzgodnienia.





