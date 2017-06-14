---
title: "Czas i frekwencja w sieci sprzedaży"
description: "W tym temacie opisano scenariusze obsługiwane w zakresie zarządzania czasem i frekwencją w module Microsoft Dynamics 365 for Operations — Handel detaliczny."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 021f0ce8ee73ede482b2b74fce93f61a886288fc
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="retail-time-and-attendance"></a>Czas i frekwencja w sieci sprzedaży

[!include[banner](includes/banner.md)]


W tym temacie opisano scenariusze obsługiwane w zakresie zarządzania czasem i frekwencją w module Microsoft Dynamics 365 for Operations — Handel detaliczny. 

<a name="manage-worker-setup-and-scheduling"></a>Zarządzanie ustawieniami i planowaniem pracowników
----------------------------------

### <a name="initial-configuration"></a>Pierwotna konfiguracja 

-   Włącz kreatora konfiguracji.
-   Zarejestruj pracowników jako pracowników odpowiedzialnych za rejestrację czasu.

### <a name="plan-worker-schedules"></a>Planowanie harmonogramów pracowników

-   Zastosuj profil za pomocą planowania pracy. Aby uzyskać więcej informacji, zobacz <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Aby uzyskać więcej informacji o etapach konfiguracji, zobacz <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Konfiguracja właściwa dla sieci sprzedaży

-   Włącz profil funkcji dla Zegara, dla pracowników, którzy mają być odpowiedzialni za rejestrację czasu. Kliknij kolejno opcje **Profile funkcji punktu sprzedaży** &gt; **Funkcje** &gt; **Rejestracje czasu w punkcie sprzedaży** &gt; **Włącz rejestracje czasu**.
-   Skonfiguruj grupy uprawnień w punkcie sprzedaży, aby włączyć uprawnienie Wyświetlanie wpisów zegara. To uprawnienie pozwala wyświetlać rejestracje zegara innych pracowników w danym sklepie (i w każdym innym sklepie, z którym użytkownik jest skojarzony, za pomocą książki adresowej). Można włączyć uprawnienie dla roli Menedżer, ale nie dla roli Kasjer. Kliknij kolejno opcje **Grupy uprawnień punktu sprzedaży** &gt; **Wyświetlanie wpisów zegara**.

## <a name="register-time"></a>Czas rejestracji
### <a name="cashier-and-non-cashier-time-registrations"></a>Rejestracje czasu dla roli Kasjer i ról innych niż Kasjer

-   W punkcie sprzedaży:
    -   Operacje rejestrowania:
        -   Zaloguj się przy użyciu operację bez użycia szuflady lub jak Nowa zmiana.
        -   Wybierz operację Zegar.
        -   Wybierz żądaną operację:
            -   Wejście
            -   Przerwa w pracy
            -   Przerwa na lunch
            -   Wyjście

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Bieżący stan</th>
    <th>Dostępne operacje</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Wejście</td>
    <td><ul>
    <li>Przerwa w pracy</li>
    <li>Przerwa na lunch</li>
    <li>Wyjście</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Przerwa w pracy</td>
    <td>Wejście</td>
    </tr>
    <tr class="odd">
    <td>Przerwa na lunch</td>
    <td>Wejście</td>
    </tr>
    <tr class="even">
    <td>Wyjście</td>
    <td>Wejście</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Wyświetl komunikat potwierdzający i sprawdź, czy godzina aktualnego działania jest prawidłowa.
-   Dziennik:
    -   Kliknij **Dziennik**, aby wyświetlić działanie zegara.
    -   Za pomocą filtrów czasu możesz wybrać różne okna czasowe.
    -   Jeśli pracujesz w wielu lokalizacjach sklepów, widoczne są rejestracje czasu we wszystkich sklepach, w których rejestrujesz czas. Za pomocą filtra sklepu możesz wyświetlać rejestracje czas z wybranego sklepu.

<!-- -->

-   Różne strefy czasowe:
    -   W przypadku wyświetlenia czasu z innej lokalizacji (dla dziennika kasjera lub za pomocą opcji **Wyświetlanie wpisów zegara** dla menedżera) i gdy ta lokalizacja jest w innej strefie czasowej, widoczne rejestracje czasu są konwertowane na czas lokalny. Załóżmy, że zarządzasz dwoma sklepami — w Arizonie i Nevadzie. Kasjer rejestruje przyjście do pracy o godzinie 9:00 w Arizonie. W tym momencie w Nevadzie jest godzina 8:00. Jeśli więc jesteś w Nevadzie i przeglądasz dane rejestracji czasu, wskazywana jest godzina 8:00.

## <a name="view-worker-time-registrations"></a>Wyświetlanie rejestracji czasu pracownika
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Wyświetlanie rejestracji czasu pracownika i filtrowanie według sklepu lub typu aktywności

W punkcie sprzedaży:

-   Wybierz **Wyświetlanie wpisów zegara**.
-   Widać działania rejestracji czasu dla wszystkich pracowników przypisanych do tych samych sklepów, do których jesteś przypisany Ty.
-   Za pomocą filtrów typu działania i sklepu możesz filtrować rejestracje czasu.

## <a name="process-and-manage-time-registrations"></a>Przetwarzanie rejestracji czasu i zarządzanie nimi
Użytkownik programu Dynamics 365 for Operations — Handel detaliczny wykonuje procedurę obliczania, zatwierdzania i przesłania rejestracji czasu do listy płac.

### <a name="primary-operations"></a>Podstawowe operacje

-   Oblicz
-   Zatwierdź
-   Prześlij do listy płac

### <a name="other-common-operations"></a>Inne częste operacje

-   Grupowe wyrejestrowania
-   Rejestrowanie nieobecności

Aby uzyskać więcej informacji na temat przetwarzania rejestracji czasu i nieobecności, zobacz <https://technet.microsoft.com/en-us/library/aa573180.aspx>.



