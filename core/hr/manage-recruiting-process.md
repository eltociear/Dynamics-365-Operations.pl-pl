---
title: "Zarządzanie procesem rekrutacji"
description: "W tym artykule opisano proces śledzenia czynności podczas rekrutacji, w tym działania związane z reklamowaniem wolnych stanowisk i rekrutacji kandydatów, śledzenie informacji o kandydatach i zgłoszeniach, prowadzenie rozmów kwalifikacyjnych z kandydatami oraz wybieranie jednego lub kilku kandydatów na wolne stanowiska w organizacji."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6276655f6e7d09f5bc8862ad456b834d8919e574
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017


---

# Zarządzanie procesem rekrutacji
<a id="manage-a-recruiting-process" class="xliff"></a>

[!include[banner](../includes/banner.md)]


W tym temacie opisano proces śledzenia czynności podczas rekrutacji, w tym działania związane z reklamowaniem wolnych stanowisk i rekrutacji kandydatów, śledzenie informacji o kandydatach i zgłoszeniach, prowadzenie rozmów kwalifikacyjnych z kandydatami oraz wybieranie jednego lub kilku kandydatów na wolne stanowiska w organizacji.

Przegląd
<a id="overview" class="xliff"></a>
--------

Projekty rekrutacji pomagają organizować kroki, które należy wykonać podczas wypełniania wolnych stanowisk w firmie. Kandydat to osoba, która ubiega się o zatrudnienie w firmie.  Zgłoszenie to wyrażone przez kandydata zainteresowanie zatrudnieniem w firmie, które może być powiązane z projektem rekrutacji w odniesieniu do konkretnego wolnego stanowiska.  Pojedynczy kandydat może mieć wiele zgłoszeń w obrębie tej samej firmy lub między różnymi firmami w organizacji.

Projekty rekrutacji
<a id="recruitment-projects" class="xliff"></a>
--------------------

Projekty rekrutacji pozwalają rekruterom na śledzenie postępu procesu wypełniania wolnych stanowisk.  Projekt rekrutacji identyfikuje dział oraz zadanie, dla których są wolne stanowiska. Projekty rekrutacji również śledzą następuję informacji o wolnych stanowiskach:
-   Określona liczba wolnych stanowisk
-   Osoba zarządzająca rekrutacją oraz alternatywna osoba kontaktowa dla stanowiska
-   Data zatwierdzenia zapotrzebowania
-   Termin zgłoszenia
-   Prognozowana data rozpoczęcia

Projekt rekrutacji zawiera **Ofertę pracy** używaną w systemie **Samoobsługi pracownika** do reklamowanie wolnego stanowiska. Aby wyświetlić wolne stanowisko pracownikom, projekt rekrutacji musi mieć **Ofertę pracy**, pole **Wyświetl na ekranie samoobsługi pracownika** musi mieć wartość Yes, **Ostateczny termin zgłoszenia** musi być ustawiony na datę przyszłą, a projekt rekrutacji musi mieć **Stan projektu** Rozpoczęty. W poniższej tabel wymieniono możliwe stany projektu rekrutacji i ich opisy.

| **Stan**    | **Wskazuje, że…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Zaplanowano | Proces rekrutacji jest przygotowywany.  Rekrutacja jeszcze się nie rozpoczęła. |
| Rozpoczęta   | Zgłoszenia są obecnie przyjmowane na wolne stanowiska w tym projekcie.                    |
| Zakończono  | Wszystkie wolne stanowiska w tym projekcie zostały wypełnione.                                          |
| Anulowano  | Rekrutacja została anulowana dla tego projektu.                                           |

Rekruterzy mogą również rejestrować **multimedia** używane do reklamowania wolnych stanowisk za pomocą zewnętrznych punktów, a także śledzić **rozwój** dla projektu lub zgłoszenia.

Kandydaci
<a id="applicants" class="xliff"></a>
----------

Kandydat to osoba, która ubiega się o pracę w firmie.  Kandydaci są wspólni dla wszystkich firm w organizacji, co powiększa pulę osób do wyszukiwania. Można zachować kompetencje, odwołania, wymagania związane z zakwaterowaniem, dane osobowe kandydatów. Po utworzeniu rekordu kandydata jest tworzony rekord tej osoby w globalnej książce adresowej. Na stronie **Kandydat** można przesyłać następujące informacje globalnej książki adresowej dla osób, które są kandydatami:
-   Informacje adresowe
-   Informacje kontaktowe
-   Informacje identyfikacyjne
-   Szczegóły nazwiska
-   Informacje osobiste

## Aplikacje
<a id="applications" class="xliff"></a>
Na stronie **Zgłoszenie** można rejestrować informacje pochodzące z otrzymanych podań o pracę. Zgłoszenie jest wyrażeniem przez kandydata zainteresowania wolnym stanowiskiem w organizacji.  Aby utworzyć zgłoszenie, kandydat musi już istnieć jako kandydat lub osoba w systemie.
Podania o pracę przesłane przez kandydata w sieci web są podaniami oczekiwanymi złożonymi w reakcji na ofertę pracy lub są podaniami złożonymi przez kandydata bez związku z ofertami. Podania oczekiwane są automatycznie kojarzone z projektem rekrutacyjnym, którego dotyczyło ogłoszenie. Podania bez związku z ofertami są kojarzone z projektem rekrutacji określonym w polu **Rekrutacja** na stronie **Parametry zasobów ludzkich**.
### Stan zgłoszenia
<a id="application-status" class="xliff"></a>

Stan zgłoszenia wskazuje, w jakim miejscu procesu rekrutacji jest podanie o pracę. W poniższej tabel wymieniono możliwe stany zgłoszenia i ich opisy.

| Stan    | Wskazuje, że…                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Odebrano  | Data otrzymania zgłoszenia.                                                             |
| Potwierdzono | Do kandydata zostało wysłane powiadomienie w celu potwierdzenia przyjęcia jego zgłoszenia.            |
| Rozmowa kwalifikacyjna | Do kandydata może zostać wysłane zaproszenie na rozmowę kwalifikacyjną.                                     |
| Odrzucenie | Do kandydata może zostać wysłane pismo informujące o odrzuceniu podania o pracę.                                          |
| Anulowano  | Do kandydata może zostać wysłane potwierdzenie wypłaty. Ten stan jest przypisywany ręcznie. |
| Zatrudniono  | Do kandydata może zostać wysłana oferta zatrudnienia.                                         |

### Akcje korespondencyjne
<a id="correspondence-actions" class="xliff"></a>

Akcja korespondencyjna dla **Zgłoszenia** określa szablon dokumentu lub wiadomości e-mail, który ma zostać użyty do komunikacji z kandydatem, który przesłał zgłoszenie. Można skojarzyć elementy **Zakładki zgłoszeń** z akcjami korespondencyjnymi, aby w komunikacji z kandydatami można było używać wartości ze stron Zgłoszenie, Kandydat, Rozmowa kwalifikacyjna i Projekt rekrutacji.  Elementy **Szablony wiadomości e-mail dotyczące zgłoszeń** można tworzyć dla akcji korespondencyjnych do szybkiego wysyłania e-maili do kandydatów, którzy mają zgłoszenie z określoną kombinacją stanu i akcji korespondencyjnej. Na przykład można wysłać e-mail z potwierdzeniem do wszystkich zgłoszeń z ustawieniem **Stan** jako Odebrane i ustawieniem **Akcja korespondencyjna** jako Odebrane.  Po wysłaniu e-maila można automatycznie zaktualizować stan zgłoszenia.

## Marszruta zgłoszenia
<a id="application-routing" class="xliff"></a>

Jeśli zgłoszenie ma zostać przejrzane przez kilku pracowników, w celu zarządzania tym procesem można tworzyć listę obiegową pracowników na stronie **Marszruta zgłoszenia**.

## Rozmowy kwalifikacyjne
<a id="interviews" class="xliff"></a>

Elementy **Rozmowy kwalifikacyjne z kandydatami** można planować na stronie **Zgłoszenia**.  Użyj przycisku **Wyślij informacje o spotkaniu**, aby wysłać plik kalendarza z informacją o terminie rozmowy kwalifikacyjnej do kandydata i osoby przeprowadzającej rozmowę kwalifikacyjną.

## Mapowanie umiejętności
<a id="skill-mapping" class="xliff"></a>

**Mapowanie umiejętności** i **Profile mapowania kwalifikacji** mogą służyć do identyfikowania kandydatów dopasowanych do wolnego stanowiska.

## Zatrudnianie kandydatów
<a id="hiring-applicants" class="xliff"></a>

Kandydatów zatrudnia się na stronie **Zgłoszenia**. Po zatrudnieniu kandydata rekord zgłoszenia otrzymuje stan **Zatrudniony**, a rekord osoby w globalnej książce adresowej jest kojarzony z rekordem nowego pracownika. Zmiany w danych globalnej książki adresowej dla nowego rekordu pracownika są również wyświetlane w rekordzie kandydata. Zmniejsza to ilość danych, które trzeba wprowadzić, gdyby nowy pracownik złożył wniosek o zatrudnienie na innym stanowisku w tym samym przedsiębiorstwie.  Aby zatrudnić istniejącego pracownika na nowym stanowisku, kliknij opcję **Zmień stanowisko** w menu rozwijanym **Stan zgłoszenia** i uruchom proces przeniesienia.





