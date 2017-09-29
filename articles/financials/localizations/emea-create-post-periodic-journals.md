---
title: "Okresy podziału w arkuszach okresowych"
description: "Arkusze okresowe są czasami nazywane arkuszami cyklicznymi, ponieważ kwota, tekst i inne informacje są powtarzane zawsze podczas księgowania arkusza. Podczas tworzenia arkusza należy określić interwał czasowy dla cyklu, taki jak dni lub miesiące. Można także określić liczbę okresów, dla których arkusz będzie księgowany."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9b07d2c274d3e4818ffd917a730aeba3e5dff76c
ms.contentlocale: pl-pl
ms.lasthandoff: 07/27/2017

---

# <a name="split-periods-in-periodic-journals"></a>Okresy podziału w arkuszach okresowych

[!include[banner](../includes/banner.md)]


Arkusze okresowe są czasami nazywane arkuszami cyklicznymi, ponieważ kwota, tekst i inne informacje są powtarzane zawsze podczas księgowania arkusza. Podczas tworzenia arkusza należy określić interwał czasowy dla cyklu, taki jak dni lub miesiące. Można także określić liczbę okresów, dla których arkusz będzie księgowany.

Aby wielokrotnie pobierać i księgować wiersze transakcji, można użyć strony **Arkusze okresowe**. Dla firm w Czechach, Estonii, na Węgrzech, Łotwie, Litwie, w Polsce i Rosji strona **Arkusze okresowe** została rozszerzona o funkcjonalność podziału na okresy. Aby uzyskać więcej informacji, zobacz [Księgowanie arkusza okresowego](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)

### <a name="example-split-for-periods-in-periodic-journals"></a>Przykład: Podział na okresy w arkuszach okresowych

Firma ubezpieczeniowa oferuje organizacji rabat na przedpłatę polisy ubezpieczeniowej na cały rok. Płatność jest zaksięgowana na koncie aktywów, takich jak przedpłaty na ubezpieczenia. Następnie miesięczny koszt ubezpieczenia jest amortyzowany w ciągu roku przez utworzenie arkusza okresowego, który zawiera kredyt na koncie przedpłat na ubezpieczenia i debet na koncie kosztów ubezpieczenia. W takim przypadku można użyć funkcji podziału na okresy. Kliknij przycisk **Podziel na okresy** znajdujący się w okienku akcji na stronie **Wiersze arkusza** **okresowego**, a następnie wypełnij następujące pola.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pole**             | **Opis**                                                                                                                                                                                             |
| **Data rozpoczęcia**        | Wybierz datę dla pierwszego wiersza arkusza okresowego.                                                                                                                                                        |
| **Liczba okresów** | Wprowadź liczbę okresów, na które zostanie podzielony wiersz dziennika. Ta wartość określa liczbę nowych transakcji, które zostaną wygenerowane. Kwota transakcji jest równo dzielona między nowymi transakcjami. |
| **Jednostka**              | Wybierz jednostkę miary okresu.                                                                                                                                                                  |
| **Zakres czasowy**   | Określ interwał (odstęp czasu) między okresami księgowania.                                                                                                                                                              |

Na przykład aby wygenerować kwartalne księgowania, wprowadź **4** w polu **Liczba okresów**, zaznacz opcję **Miesiące** w polu **Jednostka** i wprowadź **3** w polu **Zakres czasowy**. System generuje cztery wiersze arkusza, każdy dla jednej czwartej wprowadzonej kwoty wiersza arkusza, w 3-miesięcznych interwałach. Podobna funkcjonalność jest również dostępna dla arkusza finansowego. Podczas wyświetlania wierszy arkusza finansowego wybierz kolejno opcje **Arkusz okresowy** &gt; **Zapisz arkusz**.



