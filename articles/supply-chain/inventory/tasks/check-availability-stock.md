---
title: "Sprawdzanie dostępności zapasów w magazynie"
description: "Ta procedura pokazuje, jak sprawdzić ilość dostępnych i fizycznie dostępnych zapasów towaru o określonym numerze."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d103eb52a498e6273b1fdb43fc10dae4133e76b2
ms.contentlocale: pl-pl
ms.lasthandoff: 07/27/2017

---
# Sprawdzanie dostępności zapasów w magazynie

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ta procedura pokazuje, jak sprawdzić ilość dostępnych i fizycznie dostępnych zapasów towaru o określonym numerze. Przedstawia również, jak uzyskać informacje o podaży towaru. Fizycznie dostępne zapasy to zapasy na stanie, które są dostępne, to znaczy kupione, przyjęte i zarejestrowane. Zapasy na stanie obejmują dostępne zapasy będące na stanie, ale również zapasy, które zostały zamówione i są oczekiwane, ale jeszcze nie zostały przyjęte ani zarejestrowane. Można przejść tę procedurę przy użyciu danych firmy demonstracyjnej USMF lub własnych danych. Jeśli używasz firmy USMF, można wybrać wyświetlone przykładowe wartości. Te zadania zazwyczaj wykonuje pracownik magazynu.


## Sprawdzanie ilości dostępnych zapasów towaru
1. Wybierz kolejno opcje Zarządzanie zapasami > Zapytania i raporty > Dostępne zapasy.
2. Zaznacz wiersz Numer towaru.
    * Aby wykonać zapytanie o dostępne zapasy według kodów towarów, zaznacz wiersz, gdzie ustawienie Tabela ma wartość Dostępne zapasy, a ustawienie Pole wartość Numer towaru.  
3. W polu Kryteria wybierz towar, o który chcesz wykonać zapytanie.
    * Jeśli używasz danych firmy demonstracyjnej USMF, można wybrać wartość „M9201”.  
4. Kliknij przycisk OK.
5. Kliknij opcję Wymiary.
    * Karta Wymiary pozwala wybrać ilość szczegółów, jaka będzie wyświetlana o dostępnych zapasach. Aby uzyskać dane dotyczące rezerwacji, należy wyświetlić wszystkie wymiary magazynowe dla towarów używających zaawansowanych procesów magazynowych (WHS).  
6. Kliknij przycisk OK.
7. W okienku akcji kliknij pozycję Informacje pokrewne.
    * Jeśli tego nie widać, może być konieczne kliknięcie przycisku wielokropka (...), aby wyświetlić dodatkowe opcje okienka akcji.  
8. Kliknij przycisk Przegląd dostaw.
    * Karta Przegląd dostaw zawiera informacje o dostawie określonego towaru, takie jak ilość dostępnych zapasów, czas realizacji i informacje o dostawcy.  
9. Rozwiń sekcję Dostępne.
10. Rozwiń sekcję Dostawcy.
11. Zamknij stronę.
12. Zamknij stronę.

## Sprawdzanie ilości fizycznie dostępnych zapasów
1. Wybierz kolejno opcje Zarządzanie magazynem > Zapytania i raporty > Fizycznie dostępne zapasy.
2. W polu Numer towaru wpisz wartość.
    * Można użyć pól Oddział i Magazyn, aby wyfiltrować listę towarów.  
3. Odśwież stronę.
4. Kliknij opcję Wyświetl wymiary.
    * Karta Wyświetlanie wymiarów pozwala wybrać ilość szczegółów, jaka będzie wyświetlana o dostępnych zapasach.  
5. Kliknij przycisk OK.
6. Zamknij stronę.

## Sprawdzanie ilości dostępnych zapasów według lokalizacji
1. Wybierz kolejno opcje Zarządzanie magazynem > Zapytania i raporty > Dostępne zapasy według lokalizacji.
2. W polu Magazyn wpisz wartość.
    * Jeśli używasz danych firmy demonstracyjnej USMF, można wybrać wartość „51”.  
3. Odśwież stronę.
4. Kliknij opcję Wyświetl wymiary.
5. Kliknij przycisk OK.
6. Zamknij stronę.
