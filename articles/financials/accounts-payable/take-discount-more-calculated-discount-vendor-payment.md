---
title: "Zastosowanie rabatu większego niż obliczony dla płatności dla dostawcy"
description: "Ten artykuł prowadzi przez scenariusz, w którym do kwoty jest stosowany rabat gotówkowy większy niż rabat pierwotnie dostępny na fakturze. Taki scenariusz może wystąpić, jeśli organizacja zawrze z dostawcą umowę, aby zapłacić kwotę mniejszą niż podana na fakturze."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 08d7c4981aba7e7c092a6f21d3b63635e76437bf
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Zastosowanie rabatu większego niż obliczony dla płatności dla dostawcy

[!include[banner](../includes/banner.md)]


Ten artykuł prowadzi przez scenariusz, w którym do kwoty jest stosowany rabat gotówkowy większy niż rabat pierwotnie dostępny na fakturze. Taki scenariusz może wystąpić, jeśli organizacja zawrze z dostawcą umowę, aby zapłacić kwotę mniejszą niż podana na fakturze. 

Dostawca 3051 daje firmie Fabrikam rabat gotówkowy w wysokości 4%, jeżeli faktura zostanie opłacona w ciągu 7 dni. 29 czerwca April wprowadza fakturę na kwotę 1000,00. Dostawca zgadza się na przyznanie rabatu w wysokości 60,00 zamiast kwoty 40,00 dostępnej dla tej faktury. April rejestruje jednorazową płatność za pomocą arkusza płatności rozrachunków z dostawcami. Wprowadza dostawcę dla płatności, a następnie otwiera stronę **Rozliczanie transakcji**. Oznacza fakturę i zmienia wartość w polu **Kwota rabatu gotówkowego** na **-60,00**.
| Zaznacz     | Użyj rabatu gotówkowego | Załącznik   | Konto | Data      | Data wymagalności  | Faktura | Kwota w walucie transakcji | Waluta | Kwota do rozliczenia |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Wybrano | Normalna            | Inv-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1000,00                       | USD      | 940,00           |

Informacje o rabacie pojawiają się w dolnej części strony **Rozliczanie transakcji**.
|                              |           |
|------------------------------|-----------|
| Data rabatu gotówkowego           | 7/12/2015 |
| Kwota rabatu gotówkowego         | 60,00     |
| Użyj rabatu gotówkowego            | Normalna    |
| Pobrany rabat gotówkowy          | 0,00      |
| Kwota rabatu gotówkowego do pobrania | 60,00     |

Następnie April arkusz płatności. Faktura jest całkowicie rozliczona przy użyciu płatności 940,00 i rabatu 60,00.



