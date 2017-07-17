---
title: "Wyświetlanie i ocena wyników kwestionariusza"
description: "W tym temacie wyjaśniono, jak można wyświetlać i oceniać wyniki kwestionariuszy wypełnianych przez respondentów."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b7c4a612d54f3ae8967be930c0b98e4783fd8200
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# Wyświetlanie i ocena wyników kwestionariusza
<a id="view-and-evaluate-the-results-of-a-questionnaire" class="xliff"></a>

[!include[banner](includes/banner.md)]


W tym temacie wyjaśniono, jak można wyświetlać i oceniać wyniki kwestionariuszy wypełnianych przez respondentów. 

Po wypełnieniu kwestionariusza przez respondentów można wyświetlić i ocenić wyniki na kilka sposobów:

-   **Zakończone sesje odpowiedzi** — wyświetlanie szczegółowych informacji dotyczących kwestionariuszy wypełnionych przez respondentów i generowanie raportów do podsumowania odpowiedzi i uzyskanych punktów.
-   **Grupy wyników** — wyświetlanie szczegółów grup wyników i statystyk kwestionariusza. Statystyki grupy wyników mogą być generowane dla sesji pojedynczej odpowiedzi kwestionariusza lub dla wszystkich sesji odpowiedzi.
-   **Statystyki kwestionariusza** — umożliwia określenie kryteriów do obliczania statystyk dla określonej grupy respondentów.

Można również generować różne raporty w celu wyświetlania wyników, które są sortowane według sesji odpowiedzi, osoby lub grupy wyników. Dostępne są następujące raporty, które są powiązane z wypełnionymi kwestionariuszami:

-   Odpowiedzi
-   Odpowiedzi na kwestionariusz
-   Odpowiedzi na osobę
-   Analiza informacji zwrotnych

## Wyniki sesji odpowiedzi
<a id="answer-session-results" class="xliff"></a>
Kiedy respondenci wypełnią kwestionariusz, można wyświetlić wyniki zakończonych sesji odpowiedzi. Sesja odpowiedzi jest odpowiedzią jednego użytkownika na kwestionariusz. Umożliwia wyświetlenie szczegółowych informacji o sesji odpowiedzi na stronie **Odpowiedzi**. Sesje odpowiedzi, które są uwzględnione na stronie **Odpowiedzi** są filtrowane na różne sposoby, w zależności od tego, jak strona zostanie otwarta:

-   Wszystkie kwestionariusze
-   Wybrane kwestionariusze
-   Wybrana osoba

Na stronie **Odpowiedzi** można wyświetlić szczegóły dotyczące punktów uzyskanych, odpowiedzi respondenta w poszczególnych grupach wyników i hierarchii pytań, użytych w wybranym kwestionariuszu, jeśli użyto hierarchii pytań. Można również wygenerować i wydrukować następujące raporty:

-   **Raport wyników** — graficzna prezentacja uzyskanych punktów według grupy wyników dla wybranej sesji odpowiedzi.
-   **Raport odpowiedzi** — pokazuje odpowiedzi wybrane przez respondenta dla każdego pytania w kwestionariuszu.
-   **Niepoprawne odpowiedzi** — pokazuje informacje dotyczące nieprawidłowych odpowiedzi wybranych przez respondenta.

> **Uwaga**
>   Raport **Wyniki** jest dostępny tylko w przypadku korzystania z grup wyników w kwestionariuszu i jeśli wybrano opcję **Strona wyników** na stronie **Kwestionariusze**. Strona **Odpowiedzi** oraz raport **Nieprawidłowe odpowiedzi** są dostępne tylko w przypadku wybrania opcji **Raport odpowiedzi** na stronie **Kwestionariusze**.

## Statystyki kwestionariusza
<a id="questionnaire-statistics" class="xliff"></a>
Można użyć statystyk kwestionariusza do analizy wyników wypełnionego kwestionariusza na podstawie obliczeń zdefiniowanych przez użytkownika. Aby zdefiniować obliczenia, należy wykonać następujące zadania:

-   Wybierz kryteria obliczania i wyświetlania statystyk.
    -   Możesz wyświetlać statystyki według kwestionariusza, pytań, wierszy pytań lub grup wyników.
    -   Wybierz typ wykresu, który będzie używany podczas wyświetlania wyników.
    -   Wybierz typy osób z sieci, np. pracownicy, osoby kontaktowe lub kandydaci, których odpowiedzi mają zostać uwzględnione. Można również uwzględnić odpowiedzi z kwestionariuszy, które zostały wypełnione anonimowo.
    -   Skonfiguruj interwały opartych na wieku lub stażu do analizowania wyników.
-   Wymierz lub sprawdź poprawność ustawień, które precyzują zakres statysty. Na przykład wybierając kod pocztowy, można analizować wyniki dla wszystkich respondentów w konkretnym obszarze geograficznym.
-   Określ lub sprawdź poprawność kryteriów do analizy wyników według cech respondenta lub kwestionariusza. Na przykład, wybierając **kod pocztowy**, można analizować korelację między lokalizacją respondenta i poprawnymi odpowiedziami.

Ustawienia określone przez użytkownika są zapisywane i mogą być używane do okresowego ponownego obliczania wyników.

Informacje dodatkowe
<a id="see-also" class="xliff"></a>
--------

[Projektowanie kwestionariuszy](design-questionnaires.md)

[Używanie kwestionariuszy](questionnaires.md)

[Dystrybucja i wypełnianie kwestionariuszy](distribute-questionnaires.md)



