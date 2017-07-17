---
title: "Pakiet zawartości usługi Power BI Rozwój pracownika etatowego"
description: "W tym temacie opisano pakiet zawartość Rozwój pracownika etatowego dostępny dla usługi Power BI. Wyjaśniono, jak uzyskać dostęp do raportów, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: JCart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: d25f3be5821a02ea618a2356878bf2904765a6f7
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017

---

# Pakiet zawartości usługi Power BI Rozwój pracownika etatowego
<a id="employee-development-power-bi-content" class="xliff"></a>

[!include[banner](../includes/banner.md)]

W tym temacie opisano pakiet zawartość **Rozwój pracownika etatowego** dostępny dla usługi Microsoft Power BI. Wyjaśniono, jak uzyskać dostęp do raportów, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.

## Przechodzenie do pakietu zawartości usługi Power BI
<a id="accessing-the-power-bi-content" class="xliff"></a>

Jeśli używasz programu Microsoft Dynamics 365 for Finance and Operations Enterprise Edition z aktualizacją z lipca 2017 r., pakiet zawartości **Rozwój pracownika etatowego** znajduje się w bibliotece zasobów wspólnych w usłudze Microsoft Dynamics Lifecycle Services (LCS). Aby dowiedzieć się więcej o pobieraniu pakietu zawartości i jego łączeniu z firmowymi danymi, zobacz [Pakiety zawartości dla usługi Power BI w usłudze LCS od Microsoft i partnerów](power-bi-content-microsoft-partners.md).

## Raporty umieszczone w pakiecie zawartości usługi Power BI
<a id="reports-that-are-included-in-the-power-bi-content" class="xliff"></a>
Raporty dostępne w pakiecie zawartości usługi Power BI **Rozwój pracownika etatowego** mają wykresy i tabele przedstawiające dodatkowe informacje. W poniższej tabeli opisano dostępne raporty.

| Raport                        | Zawartość |
|-------------------------------|----------|
| Przegląd rozwoju pracowników | Podsumowanie innych raportów |
| Analiza kwalifikacji pracowników       | Typy umiejętności pracowników i podział umiejętności pracowników według typów |
| Analiza poziomu kwalifikacji pracowników | Poziomy umiejętności pracowników według działów, pracownicy według poziomów umiejętności i typów umiejętności oraz i najniższe i najwyższe poziomy poszczególnych umiejętności |
| Profil kwalifikacji                 | Profil kwalifikacji wybranego pracownika etatowego |
| Analiza kwalifikacji                | Umiejętności według typu i kategorii |
| Analiza oceny wydajności   | Pracownicy o najniższej i najwyższej ocenie według zadań, oceny pracowników według działów, pracownicy według ocen i typów stanowisk oraz najwyższe i najniższe oceny na poszczególnych stanowiskach  |
| Analiza wydajności pracowników etatowych | Oceny pracowników dla wybranych ocen dokonywanych przez menedżerów |

Wykresy i kafelki w tych raportach można filtrować oraz przypinać do pulpitu nawigacyjnego. Aby uzyskać więcej informacji na temat filtrowania i przypinania w narzędziu Power BI, zobacz [Tworzenie i konfigurowanie pulpitu nawigacyjnego](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## Opis modelu danych i jednostek
<a id="understanding-the-data-model-and-entities" class="xliff"></a>
| Jednostka                   | Zawartość                                                                                                   | Powiązania z innymi jednostkami |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Przesunięcie kalendarza          | Przesunięcia kalendarzy dla raportów wycinkowych                                                                          | Przeszłe przypisania stanowisk, Trend stanowisk, Trend pracowników, Pracownik z rozwiązanym stosunkiem pracy 
| Firma                  | Firmy, według których będą filtrowane raporty                                                                             | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Bieżące stanowisko         | Stanowiska na obecny dzień, równoważnik pełnego etatu (FTE), wolne stanowiska i stanowiska wolne do obsadzenia | Zadanie, Stanowisko |
| Bieżący pracownik etatowy         | Liczba pracowników na obecny dzień, wiek i stan osobowy                                                         | Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Tytuł pracownika, Dane demograficzne, Zadanie, Zatrudnienie, Stanowisko |
| Data                     | Dni, tygodnie, miesiące i lata                                                                             | Przeszłe przypisania stanowisk, Trend stanowisk, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Dane demograficzne             | Data urodzenia, płeć, pochodzenie etniczne i stan cywilny                                                   | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Zatrudnienie               | Data rozpoczęcia, data zakończenia i data przejścia                                                                  | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Położenie geograficzne      | Miejscowość, kod pocztowy i województwo                                                           | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Stanowisko                      | Funkcja, typ i tytuł                                                                                  | Bieżące stanowisko, Bieżący pracownik etatowy |
| Przeszłe przypisania stanowisk | Przyczyna przypisania, data rozpoczęcia, data zakończenia i zadanie                                                           | Przesunięcie kalendarza, Data, Zadanie, Stanowisko |
| Pozycja                 | Dział, równoważnik pełnego etatu, stanowisko, typ stanowiska i tytuł                                                        | Bieżące stanowisko, Bieżący pracownik etatowy |
| Trend stanowisk           | Stanowiska zajmowane w okresie, równoważnik pełnego etatu i zadanie                                                                          | Przesunięcie kalendarza, Data, Zadanie, Stanowisko |
| Przełożony               | Imię, drugie imię i nazwisko                                                                       | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Pracownik z rozwiązanym stosunkiem pracy      | Zwolnieni pracownicy, data rozwiązania stosunku pracy, tytuł, stanowisko i zadanie                                             | Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Przesunięcie kalendarza, Data, Tytuł pracownika, Dane demograficzne, Zatrudnienie, Zadanie, Stanowisko |
| Nazwisko pracownika etatowego            | Imię, drugie imię i nazwisko                                                                       | Bieżący pracownik, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Tytuł pracownika           | Tytuł i data ustalenia stażu pracy                                                                                   | Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników |
| Trend pracowników           | Liczba pracowników w okresie, stan osobowy, firma i stanowisko                                                        | Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Przesunięcie kalendarza, Data, Tytuł pracownika, Dane demograficzne, Zatrudnienie, Zadanie |
| Stanowisko                      | Funkcja, typ i tytuł                                                                                      | Bieżący pracownik, Bieżące stanowisko, Trend pracowników, Umiejętności preferowane w zadaniu, Przeszłe przypisania stanowisk, Trend stanowisk, Pracownik z rozwiązanym stosunkiem pracy |
| Umiejętności preferowane w zadaniu      | Ważność, ocena, umiejętności i poziom umiejętności                                                                 | Stanowisko |
| Analiza kwalifikacji pracowników  | Certyfikaty, poziom, data poziomu i umiejętności                                                                    | Nazwisko pracownika etatowego, Kwalifikacje |  
| Wydajność              | Ocena, opis i model oceniania                                                                      | Bieżący pracownik, Bieżące stanowisko, Trend pracowników, Umiejętności preferowane w zadaniu, Przeszłe przypisania stanowisk, Trend stanowisk, Pracownik z rozwiązanym stosunkiem pracy |
|  Kwalifikacje                   | Umiejętności, typ umiejętności i klasyfikacja                                                                              | Analiza kwalifikacji pracowników, Umiejętności preferowane w zadaniu |                                                                                                                        

Te jednostki zostały użyte do utworzenia obliczanych miar w modelu danych. Następnie obliczane miary są używane do obliczania kluczowych wskaźników wydajności (KPI) i generowania raportów, które są używane w pakiecie zawartości usługi Power BI. Jeśli chcesz umieścić dodatkowe obliczenia w raportach i na pulpicie nawigacyjnym, możesz z usługi LCS pobrać plik .pbix i go zmodyfikować. Ten plik jest domyślnym modelem danych, który został użyty do utworzenia pakietu zawartości usługi Power BI. Po wprowadzeniu wszystkich modyfikacji można utworzyć organizacyjny pakiet zawartości i pulpit nawigacyjny, który zawiera dodane informacje.
