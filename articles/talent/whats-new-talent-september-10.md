---
title: "Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (10 września 2018 r.)"
description: "W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: pl-pl
ms.lasthandoff: 09/12/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (10 września 2018 r.)

[!include [banner](includes/banner.md)]

**Kompilacja 8.1.138.0**

W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Możliwość określania konkretnej pory dnia we wnioskach o czas wolny (połowy dnia)

Jeśli obszar roboczy Urlopy i nieobecności jest skonfigurowany tak, aby wnioski o czas wolny były przesyłane w dniach, teraz można włączyć określanie połowy dni. Odtąd gdy użytkownicy przesyłają wnioski o czas wolny, mogą wskazać, czy proszą o zwolnienie na pierwszą, czy drugą połowę dnia.

Domyślnie ta opcja jest wyłączona. Aby pracownicy mogli prosić o czas wolny na pierwszą lub drugą połowę dnia, należy włączyć tę opcję w obszarze **Urlopy i nieobecności** w oknie Parametry zasobów ludzkich.

Uprawnieniem zabezpieczeń dla tej funkcji jest Obsługa parametrów zasobów ludzkich.

## <a name="validation-of-leave-and-absence-entries"></a>Sprawdzanie poprawności wpisów urlopów i nieobecności

Zależnie od konfiguracji funkcjonalności urlopów pracownicy, którzy próbują przesłać wnioski o czas wolny na okres dłuższy niż ich dzień roboczy, otrzymują komunikat ostrzegawczy. Innymi słowy są ostrzegani, jeśli próbują wziąć więcej wolnego niż jeden pełny dzień w danym dniu.

Ta funkcja weryfikacji jest zawsze włączona. Ilekroć pracownicy przekroczą zdefiniowany próg dzienny, otrzymują ostrzeżenie w swoich wnioskach o czas wolny.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Dodatkowe pola instrukcji warunkowych w przepływach pracy

Dodano więcej pól w instrukcjach warunkowych i symbolach zastępczych w kilku przepływach pracy w aplikacji Core HR.

Następujące pola zostały dodane do przepływów pracy wynagradzania, rozwiązywania stosunku pracy i przenoszenia:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Pozycja
- Organizacja zawodowa
- Dział
- PositionType
- CompLocation
- Tytuł
- Funkcja
- JobType
- JobFamily
- JobFunction

Następujące pola zostały dodane do przepływu pracy stanowiska:

- Pozycja
- Organizacja zawodowa
- Dział
- PositionType
- CompLocation
- Tytuł
- Funkcja
- JobType
- JobFamily
- JobFunction

Pola w instrukcjach warunkowych i symbolach zastępczych są dostępne dla wszystkich użytkowników, którzy mają dostęp do konfigurowania opisanych powyżej przepływy pracy.

## <a name="navigation-to-attract-from-personnel-management"></a>Przechodzenie do aplikacji Attract z obszaru roboczego Zarządzanie pracownikami

Jeżeli w obszarze roboczym Zarządzanie personelem nie widać skonfigurowanej aplikacji Attract, sekcja **Kandydaci do zatrudnienia** kieruje użytkowników do rozpoczęcia pracy z aplikacją Attract, podczas gdy wcześniej był wyświetlany komunikat „Brak elementów do wyświetlenia w tym widoku”.

## <a name="other-changes"></a>Inne zmiany

Ta wersja zawiera kilka dodatkowych poprawek błędów:

- Podczas zatrudniania zleceniobiorcy karta **Wynagrodzenie** nie powinna być dostępne na stronie wniosku/akcji.
- W trakcie procesu wnioskowania o zakończenie zatrudnienia można kontynuować dopiero wtedy, gdy wszystkie wymagane pola będą zawierały dane.
- Rozwiązano problemy z porządkiem sortowania i wyświetlaniem dat w funkcjach analizy w obszarze roboczym Zarządzanie pracownikami.
