---
title: "Zarządzanie informacjami o pracownikach za pomocą przepływów pracy"
description: "W tym temacie wyjaśniono, jak za pomocą funkcji przepływów pracy dostępnych w module Zasoby ludzkie zarządzać informacjami o pracownikach. Można na przykład skojarzyć przepływ pracy ze stanowiskiem oraz skonfigurować przepływ pracy zatwierdzania, który jest uruchamiany, gdy pracownicy zmodyfikuje swój rekord."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 806860e5df9252c074e04e9e1670f4215fd94ca2
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Zarządzanie informacjami o pracownikach za pomocą przepływów pracy

[!include[banner](includes/banner.md)]


W tym temacie wyjaśniono, jak za pomocą funkcji przepływów pracy dostępnych w module Zasoby ludzkie zarządzać informacjami o pracownikach. Można na przykład skojarzyć przepływ pracy ze stanowiskiem oraz skonfigurować przepływ pracy zatwierdzania, który jest uruchamiany, gdy pracownicy zmodyfikuje swój rekord.

Funkcjonalność przepływów pracy zawarta w module Zasoby ludzkie oferuje wiele przepływów pracy do zarządzania działaniami dotyczącymi zasobów ludzkich. Ponadto są dostępne liczne opcje umożliwiające modyfikowanie konkretnych przepływów pracy i ich kojarzenie z hierarchią raportowania. Dostępne są przepływy pracy pomagające zarządzać zmianami w kilku standardowych typach informacji o pracownikach. Przepływ pracy można skojarzyć ze stanowiskiem. Następnie jeśli pracownicy zmodyfikują swoje rekordy pracowników, będzie uruchamiany przepływ pracy, który wymaga zatwierdzenia, zanim nowe informacje zostaną zapisane. Przepływy pracy są wstępnie zdefiniowane dla następujących typów informacji, aby ułatwić efektywne zarządzanie zmianami i zachować rzetelność danych pracowników:

-   Numery identyfikacyjne
-   Kursy
-   Wykształcenie
-   Wizerunek
-   Wypożyczone elementy
-   Doświadczenie zawodowe
-   Doświadczenie w projekcie
-   Umiejętności
-   Stanowiska zaufania
-   Akcje w module Zasoby ludzkie
-   Rejestracja na kurs

Kiedy pracownicy są zatrudniani, przenoszeni lub zwalniani, przepływ pracy może zawierać proces weryfikacji. W ten sposób w ramach przepływu pracy można sprawdzić dokument lub zdefiniować warunki czynności. Po zakończeniu procesu weryfikacji następuje finalizacja dokumentu lub czynność, a przepływ pracy przechodzi do ostatniego etapu zatwierdzania.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Kojarzenie przepływu pracy z hierarchią stanowisk
Przepływ pracy można skojarzyć z dowolną skonfigurowaną hierarchią. Na przykład jeśli stanowisko jest skojarzone z macierzową hierarchią raportowania, można skonfigurować przepływ pracy, który kieruje wydatki danego projektu do kierownika projektu zamiast do menedżera pracownika skojarzonego z tym stanowiskiem. Aby utworzyć nowy przepływ pracy lub zmodyfikować istniejący przepływ pracy, na stronie **Przepływy pracy modułu Zasoby ludzkie** kliknij przycisk **Nowy**. Zaznacz przepływ pracy na liście, a zostanie uruchomiony projektant przepływów pracy. Za pomocą projektanta można utworzyć nowy przepływ pracy lub zmienić kroki w istniejącym przepływie pracy. Po modyfikacji istniejącego przepływu pracy zmiany zostaną zapisane jako nowa wersja. W związku z tym zawsze można wrócić do poprzedniej wersji, jeśli trzeba.

## <a name="configure-a-human-resources-workflow"></a>Konfigurowanie przepływu pracy dla modułu Zasoby ludzkie
Aby skonfigurować podstawowy przepływ pracy uruchamiany w momencie, gdy pracownicy proszą o zmiany ich osobistych numerów identyfikacyjnych, wykonaj następujące czynności:

1.  Na stronie **Przepływy pracy modułu Zasoby ludzkie** kliknij przycisk **Nowy**.
2.  Na liście dostępnych przepływów pracy wybierz opcję **Numery identyfikacyjne**.
3.  Kliknij przycisk **Uruchom**, aby uruchomić projektanta przepływów pracy, a następnie w odpowiedzi na monit wprowadź swoją nazwę użytkownika i hasło.
4.  Przeciągnij element **Zatwierdź numer identyfikacyjny** z listy elementów przepływu pracy na kanwę projektanta.
5.  Połącz element zatwierdzania z czynnościami **Rozpocznij** i **Zakończ**.
6.  Kliknij dwukrotnie pozycję **Element zatwierdzania**, a następnie kliknij prawym przyciskiem myszy i wybierz polecenie **Właściwości**.
7.  Wykonaj następujące kroki, aby dodać instrukcje elementu pracy:
    1.  Wybierz opcję **Przypisanie**, a następnie w polu typu przypisania wybierz opcję **Hierarchia**.
    2.  W obszarze **Hierarchia** zaznacz opcję **Konfigurowalna hierarchia**.
    3.  Dodaj warunek zatrzymania i zamknij stronę.

8.  Wykonaj wszelkie dodatkowe instrukcje (nie powinny być generowane żadne dodatkowe ostrzeżenia).
9.  Kliknij przycisk **Zapisz i zamknij**. Gdy zostanie otwarte okno dialogowe, wybierz opcję **Uaktywnij**.
10. Wybierz kolejno opcje **Zasoby ludzkie** &gt; **Stanowiska** &gt; **Typy hierarchii stanowisk**.
11. Wybierz opcję **Macierz**.
12. Dodaj przepływ pracy **Numer identyfikacyjny pracownika** do listy.




