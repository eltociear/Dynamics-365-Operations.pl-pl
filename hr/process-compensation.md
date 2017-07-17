---
title: Przetwarzanie wynagrodzenia
description: "Funkcjonalność przetwarzania wynagrodzeń pozwala obliczyć nowe kwoty podstawy wynagrodzenia dla pracowników w oparciu o korektę wyrównawczą, cele podwyżki uznaniowej i wydajność."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6e30357b0bca8745b69bff19a55828b180c3b829
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017


---

# Przetwarzanie wynagrodzenia
<a id="process-compensation" class="xliff"></a>
Funkcjonalność przetwarzania wynagrodzeń pozwala obliczyć nowe kwoty podstawy wynagrodzenia dla pracowników w oparciu o korektę wyrównawczą, cele podwyżki uznaniowej i wydajność. Ten wpis na blogu omawia podstawowy przepływ przetwarzania wynagrodzeń w systemach stałych wynagrodzeń bez uwzględniania wydajności.

## Planowanie nowych kwot wynagrodzeń i budżetów
<a id="plan-the-new-compensation-amounts-and-budgets" class="xliff"></a>
Aby dać pracownikom podwyżkę uznaniową, należy skonfigurować budżet stałych podwyżek dla każdego z działów: Zarządzanie wynagrodzeniami > Linki > Cele podwyżki uznaniowej. (Alternatywnie można otworzyć ten formularz z poziomu działu: Organizacja > Działy). W tym oknie można dodatkowo określić, czy pracownicy w określonym związku zawodowym lub lokalizacji powinni otrzymać inny procent podwyżki. Pola **Budżet** i **Waluta** służą celom informacyjnym i mogą służyć do zanotowania kwoty waluty dla budżetu.

## Konfigurowanie przetwarzania wynagrodzenia
<a id="set-up-the-compensation-process" class="xliff"></a>
Zdarzenie procesowe umożliwia określenie parametrów przetwarzania wynagrodzeń. Obejmuje to okres do dnia, który ma zostać użyty do wyznaczenia kwot wynagrodzeń,  oraz datę, od kiedy nowe kwoty wynagrodzeń powinny obowiązywać.

Opcjonalnie można uwzględnić datę określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia, jeśli w którymkolwiek systemie stałych wynagrodzeń jest używana reguła zatrudnienia Procent. W takich systemach każdy, kto został zatrudniony po dacie rozpoczęcia cyklu, a przed datą określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia, otrzyma 100% obliczonej podwyżki uznaniowej lub podwyżki ogólnej. Każdy, kto został zatrudniony po dacie określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia, a przed datą zakończenia cyklu, otrzyma część obliczonej podwyżki zgodnie z liczbą dni w cyklu, przez jaką był zatrudniony. Na przykład jeśli nasz cykl trwa od 1 stycznia do 31 grudnia i mamy datę zatrudnienia z wynagrodzeniem proporcjonalnym wg stałej stawki ustawioną na 1 kwietnia, to pracownik zatrudniony w marcu otrzyma pełną obliczoną podwyżkę, podczas gdy pracownik zatrudniony 1 lipca otrzyma około połowy obliczonej podwyżki.

Zdarzenie procesowe **-Data stałego punktu odniesienia** jest używane tylko do przetwarzania w niektórych systemach wynagrodzeń o zmiennej wysokości i nie będzie omówione w tym wpisie na blogu. **Termin przeglądu** to termin na złożenie wszystkich propozycji płacowych, tak aby nowe kwoty wynagrodzeń mogły zostać załadowane do rekordu pracownika. Data przeglądu ma wyłącznie charakter informacyjny.

Po zapisaniu parametrów zdarzenia procesowego można kliknąć przycisk **Ustawienia** i wskazać systemy wynagrodzeń, które mają zostać uwzględnienie w tej sesji przetwarzania, oraz czynności akcje związane ze stałym wynagrodzeniem, które mają zostać wykonane dla każdego systemu.

Kliknij przycisk **Dodaj** na górnej karcie, aby dodać system wynagrodzeń do zdarzenia procesowego. Kolumny **Użyj innej dźwigni finansowej**, **Współczynnik dźwigni finansowej** i **Opis dźwigni finansowej** są używane tylko dla systemów wynagrodzeń o zmiennej wysokości i nie będą omówione w tym temacie.

Zapisz rekord i kliknij przycisk **Dodaj** na dolnej karcie, aby dodać akcje związane ze stałym wynagrodzeniem dla wybranego systemu wynagrodzeń. Użyj opcji Włącz rekomendacje, jeśli chcesz mieć możliwość wprowadzenia innej kwoty niż obliczona podwyżka podstawowa dla czynności. Jeśli chcesz, aby czynność była obliczana w zależności od wyniku poprzedniej czynności w celu połączenia wielu czynności dotyczących wynagrodzeń, zaznacz opcję Użyj poprzedniego wyniku. Akcje związane ze stałym wynagrodzeniem to rodzaje logiki wynagrodzeń, którym można nadawać opisowe nazwy. W systemach typu Kategoria lub Pasmo można dodawać tylko akcje związane ze stałym wynagrodzeniem, które mają jeden z następujących typów:

| Typ akcji związanej ze stałym wynagrodzeniem | Funkcja                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kapitał własny                        | W czynnościach wyrównywania stawka płacy pracownika na ostatni dzień cyklu jest porównywana z najniższym punktem odniesienia dla poziomu wskazanego na stanowiska pracownika. Jeśli stawka płacy pracownika jest niższa od minimalnego punktu odniesienia, zostanie obliczona podwyżka konieczna do osiągnięcia minimalnego punktu przez pracownika.                                                                                |
| Wartość                         | W czynnościach uznaniowych podwyżka jest obliczana na podstawie stawki płacy pracownika na ostatni dzień cyklu oraz procentu podwyżki znalezionego w budżecie stałych podwyżek dla działu, związku zawodowego i lokalizacji pracownika.                                                                                                                                                                                         |
| Ogólne                       | W czynnościach ogólnych podwyżka jest obliczana na podstawie wartości procentowej lub pracownikom jest przyznawana kwota ryczałtowa. Jest to uzależnione od ustawień stałych wynagrodzeń na karcie Ogólne.                                                                                                                                                                                                                        |
| Awans                     | Czynności awansowania to nazwane miejsce, gdzie można przyznawać podwyżki. Dlatego pamiętaj o zaznaczeniu opcji **Włącz rekomendacje**, tak aby można było wprowadzać propozycje dla pracowników mających otrzymać awans.  Pracownicy bez proponowanej podwyżki nie będą mieli akcji Awans dodanej do swoich rekordów stałego wynagrodzenia.                                                                       |
| Inna zmiana poziomu            | W powyższym przykładzie akcją związaną ze stałym wynagrodzeniem o typie Inna zmiana poziomu jest akcja zatytułowana Degradacja. Generuje ona zerową (bez zmian) podwyżkę podstawową, w związku z czym można wpisać kwotę propozycji korygującą stawkę płacy pracownika. (Upewnij się, że zaznaczysz opcję **Włącz rekomendacje**). Pracownicy bez propozycji nie będą mieli tej akcji dodanej do swoich rekordów stałego wynagrodzenia. |

Do planu wynagrodzeń skokowych można dodać wyłącznie akcję związaną ze stałym wynagrodzeniem o typie Krok.

| Typ akcji związanej ze stałym wynagrodzeniem | Funkcja                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Krok                           | Na karcie Ogólne wskaż, czy ta akcja kroku powinna przenosić pracowników w przód o 0 kroków, 1 krok, czy 2 kroki.                                                                                  |
|                                | **0 kroki** — Pracownik otrzyma stawkę płacy dla bieżącego kroku, na którym się znajduje.                                                                                                                      |
|                                | **1 krok** — System sprawdzi, czy pracownik jest już w ostatnim punkcie odniesienia dla swojego poziomu.                                                                                             |
|                                | **2 kroki** — System przeniesie pracownika w przód o dwa kroki na jego bieżącym poziomie. Jeśli pracownik osiągnął już ostatni punkt odniesienia na swoim poziomie, system może go przenieść o jeden krok lub nawet zero kroków. |

## Wykonywanie procesu wynagrodzenia
<a id="run-the-compensation-process" class="xliff"></a>
Po skonfigurowaniu niezbędnych pól dat, systemów wynagrodzeń i czynności w zdarzeniu procesowym można kliknąć przycisk **Uruchom proces** na stronie Zdarzenie procesu. Wykonanie tej czynności spowoduje otwarcie okna dialogowego Uruchom zdarzenia procesowe wynagrodzeń. W tym oknie dialogowym można kliknąć opcję **Pokaż wyniki przetwarzania**, aby zobaczyć, jak kwoty wynagrodzeń zostały obliczone dla każdego pracownika. Kliknięcie przycisku **OK** spowoduje uruchomienie przetwarzania wynagrodzeń dla wszystkich pracowników istniejących w wybranych systemach wynagrodzeń na dzień zakończenia cyklu.

## Wyświetlanie wyników przetwarzania
<a id="view-the-process-results" class="xliff"></a>
Aby wyświetlić wyniki przetwarzania, otwórz stronę **Wyniki procesu**. Po każdym uruchomieniu zdarzenia procesowego jest tworzone nowe zdarzenie dotyczące wynagrodzeń. W ten sposób można wykonywać przebiegi próbne, wprowadzać korekty i uruchamiać zdarzenia związane z wynagrodzeniami wiele razy, aby zobaczyć, jak różne zmiany wpływają na wynagrodzenia pracowników.

Strona Wyniki procesu zawiera informacje na temat sesji przetwarzania, w tym czas wykonania przetwarzania, nazwa użytkownika, który uruchomił proces, oraz czy wystąpiły błędy podczas wykonywania procesu. Można również zaznaczyć opcję **Zablokowane**, aby wyłączyć przycisk **Załaduj wynagrodzenie** i uniemożliwić wszystkim osobom ładowanie zdarzeń dotyczących wynagrodzenia do rekordów pracowników. Kliknięcie przycisku **Wyniki pracowników** spowoduje wyświetlenie listy pracowników uwzględnionych w sesji przetwarzania.

Okno Wyniki pracownika etatowego zawiera informacje na temat samego procesu, a także o wszelkich czynnościach związanych z wynagrodzeniami wykonanych w procesie. Sekcja Stałe wynagrodzenie będzie zawierać rekord dla każdej akcji uwzględnionej w zdarzeniu procesowym dla systemu wynagrodzeń. Kolumny Bieżąca podstawa i Propozycja zawierają więcej informacji dla akcji wybranej w sekcji Stałe wynagrodzenie. Jeśli czynność ma zaznaczoną opcję Włącz rekomendacje, pola Rekomendacja będzie można edytować. Pozwoli to na ręczne korygowanie kwot dla pracownika. Uwaga: Jeśli dla akcji w zdarzeniu procesowym zaznaczono opcję Użyj poprzedniego wyniku, należy ręcznie zaktualizować kwoty dla wszystkich zależnych akcji.

Po dokonaniu przeglądu kwot wynagrodzeń dla pracownika i wprowadzeniu korekt w proponowanych wartościach można zmienić wartość atrybutu **Stan** w wierszu **Zdarzenie pracownika**, aby wskazać, czy zdarzenie zostało zatwierdzony, czy też powinno być ignorowane. Opcjonalnie można wymazać wszystkie zmiany propozycji płacowych dla pracownika, klikając przycisk **Oblicz ponownie**. Spowoduje to oznaczenie istniejącego zdarzenia pracownika stanem Ignoruj i utworzenie nowego zdarzenia pracownika z przeliczonymi wartościami.

## Ładowanie zatwierdzonych zmian wynagrodzeń
<a id="loading-approved-compensation-changes" class="xliff"></a>
Gdy jedno lub więcej zdarzeń pracowników otrzyma aktualizację stanu do Zatwierdzone, mogą zostać załadowane do rekordów stałego wynagrodzenia pracowników. Można to zrobić poprzez zaznaczenie pojedynczo każdego zdarzenia pracownika i kliknięcie przycisku Załaduj wynagrodzenie pracownika etatowego na stronie Wyniki pracownika etatowego albo poprzez kliknięcie przycisku **Załaduj wynagrodzenie** na stronie Wyniki procesu i załadowanie na raz wszystkich zatwierdzonych zdarzeń pracowników.

Kliknięcie przycisku **OK** w oknie dialogowym **Załaduj wynagrodzenie** spowoduje dodanie wierszy niezerowych akcji dotyczących wynagrodzeń do strony **Stałe wynagrodzenie pracownika etatowego**.
