---
title: Korygowanie wartości kosztowych dostępnych zapasów
description: Na stronie Korygowanie dostępnych zapasów można skorygować wartość kosztów ilości dostępnych zapasów po wykonaniu procesu zamknięcia zapasów.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2417a278e58f4309873ab4d33b0d1f1686081951
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556122"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Korygowanie wartości kosztowych dostępnych zapasów

[!include [banner](../includes/banner.md)]

Na stronie Korygowanie dostępnych zapasów można skorygować wartość kosztów ilości dostępnych zapasów po wykonaniu procesu zamknięcia zapasów.

Można użyć strony **Korygowanie dostępnych zapasów** do korygowania wartości kosztu dostępnych zapasów po uruchomieniu procesu zamknięcia magazynu. **Uwaga:** Aby otworzyć stronę **Korygowanie dostępnych zapasów**, na stronie **Zamknięcie i korekta** wybierz rekord zakończonego procesu zamknięcia zapasów, a następnie kliknij kolejno opcje **Korekta** &gt; **Dostępne**. **Przykład:** W lutym są realizowane następujące transakcje:

-   1 lutego: magazynowy przychód finansowy o ilości 2 i koszcie 10,00 USD;
-   5 lutego: magazynowy przychód finansowy o ilości 1 i koszcie 13,00 USD;
-   19 lutego: finansowy rozchód z magazynu o ilości 1 i bieżącym koszcie średnim 11,00 USD.

Ten towar został skonfigurowany przy użyciu modelu zapasów FIFO (pierwsze na wejściu, pierwsze na wyjściu), a zamknięcie zapasów zostało wykonane 28 lutego. Transakcja wydania finansowego o wartości 11,00 USD zostanie rozliczona względem przyjęcia finansowego z 1 lutego oraz zostanie wykonana korekta o wysokości 1,00 USD. Następujące przyjęcia na magazyn będą zawierać otwarte ilości magazynowe:

-   1 lutego: ilość 1, koszt 10,00 USD
-   5 lutego: ilość 1, koszt 13,00 USD

Aby ustawić koszt tych dwóch towarów na 15,00 USD, należy skorygować otwarte ilości dostępnych zapasów w ostatnim okresie zamknięcia magazynu za pomocą opcji korekty dostępnych zapasów. **Uwaga:** Datą księgowania transakcji korekty dostępnych zapasów będzie dzień ostatniego zamknięcia magazynu. Tego ustawienia nie można zmodyfikować.
