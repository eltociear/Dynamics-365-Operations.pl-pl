---
title: "Zarządzanie cyklem życia konfiguracji raportowania elektronicznego"
description: "W tym temacie opisano sposób zarządzania cyklem życia konfiguracji aparatu raportowania elektronicznego (ER) w programie Microsoft Dynamics 365 for Finance and Operations."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b1f5da07ffff5e34d8c73012a1e3c85fe1546fda
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Zarządzanie cyklem życia konfiguracji Raportowania elektronicznego

[!include[banner](../includes/banner.md)]


W tym temacie opisano sposób zarządzania cyklem życia konfiguracji aparatu raportowania elektronicznego (ER) w programie Microsoft Dynamics 365 for Finance and Operations.

<a name="overview"></a>Przegląd
--------

Raportowanie elektroniczne (ER) jest aparatem, który obsługuje dokumenty elektroniczne wymagane ustawowo i specyficzne dla danego kraju w programie Microsoft Dynamics 365 for Finance and Operations. Zasadniczo moduł ER umożliwia wykonywanie następujących zadań dla pojedynczego dokumentu elektronicznego. Aby uzyskać więcej szczegółowych informacji, zobacz [Raportowanie elektroniczne — omówienie](general-electronic-reporting.md).

-   Projektowanie szablonu dokumentu elektronicznego:
    -   identyfikacja wymaganych źródeł danych, które mogą być prezentowane w dokumencie:
        -   Bazowe dane programu Finance and Operations, takie jak tabele danych, jednostki danych i klasy.
        -   Właściwości specyficzne dla procesów, takie jak data i godzina wykonania oraz strefa czasowa.
        -   Parametry wejściowe użytkownika, określane przez użytkownika podczas wykonywania.
    -   Definiowanie wymaganych elementów dokumentu oraz ich topologii w celu określenia formatu finalnego dokumentu.
    -   Konfigurowanie żądanego przepływu danych z wybranych źródeł danych do zdefiniowanych elementów dokumentu (za pomocą powiązań źródeł danych ze składnikami formatu dokumentu) i określanie logiki kontroli procesu.
-   Udostępnianie szablonu pozwalające używać go w innych wystąpieniach programu Finance and Operations:
    -   Przekształcanie szablonu dokumentu utworzonego w programie Finance and Operations na konfigurację raportowania elektronicznego, a następnie eksportowanie konfiguracji z bieżącego wystąpienia programu Finance and Operations jako pakietu XML, który może być przechowywany lokalnie lub w usłudze LCS.
    -   Przekształcanie konfiguracji ER na szablon dokumentu programu Finance and Operations.
    -   Import pakietu XML przechowywanego lokalnie lub w usłudze LCS do bieżącego wystąpienia programu Finance and Operations.
-   Dostosowywanie szablonu dokumentu elektronicznego:
    -   Pobieranie szablonu z usługi LCS do bieżącego wystąpienia programu Finance and Operations jako konfiguracji ER.
    -   Projektowanie niestandardowej wersji konfiguracji ER z zachowaniem odniesienia do wersji bazowej.
-   Integracja szablonu z określonym procesem biznesowym w celu udostępnienia go w programie Finance and Operations:
    -   Konfigurowanie ustawień programu Finance and Operations, tak aby zaczął używać konfiguracji ER, poprzez utworzenie odwołania do tej konfiguracji w parametrze związanym z procesem. Na przykład utworzenie odwołania do konfiguracji ER w określonej metodzie płatności dla rozrachunków z dostawcami w celu generowania komunikatu płatności elektronicznej do przetwarzania faktur.
-   Używanie szablonu w określonym procesie biznesowym:
    -   Uruchamianie konfiguracji ER w określonym procesie biznesowym (na przykład w celu generowania komunikatu płatności elektronicznej do przetwarzania faktur po wybraniu metody płatności odwołującej się do konfiguracji ER).

## <a name="concepts"></a>Koncepcje
Następujące role i pokrewne działania są powiązane z cyklem życia konfiguracji ER:

| Rola                                       | Działania                                                      | opis                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konsultant funkcjonalny raportowania elektronicznego | Tworzenie i zarządzanie składnikami ER (modelami i formatami).           | Pracownik biznesowy, który projektuje modele danych ER specyficzne dla domeny, projektuje wymagane szablony dokumentów elektronicznych i tworzy im odpowiednie powiązania.                                                                           |
| Deweloper raportowania elektronicznego             | Tworzenie i zarządzanie mapowaniami modelu danych.                          | Specjalista ds. programu Finance and Operations, który wybiera żądane źródła danych programu Finance and Operations i wiąże je z modelami danych ER specyficznymi dla domeny.                                                                 |
| Kierownik ds. księgowania                      | Konfigurowanie ustawień procesów odwołujących się do artefaktów ER. | Na przykład rola **Kierownik ds. księgowania**, która pozwala używać ustawień konfiguracji ER w określonej metodzie płatności w module rozrachunków z dostawcami w celu generowania komunikatu płatności elektronicznej do przetwarzania faktur. |
| Pracownik ds. płatności rozrachunków z dostawcami            | Używanie artefaktów ER w określonym procesie biznesowym.                | Na przykład rola **Pracownik ds. płatności rozrachunków z dostawcami** umożliwiająca generowanie komunikatów płatności elektronicznych do przetwarzania faktur na podstawie formatu ER skonfigurowanego dla określonej metody płatności.           |

## <a name="er-configuration-development-lifecycle"></a>Cykl życia tworzenia konfiguracji ER
Zalecamy projektować konfiguracje raportowania elektronicznego w środowisku programistycznym jako odrębnym wystąpieniu programu Finance and Operations z następujących przyczyn:

-   Użytkownicy posiadający rolę **Deweloper raportowania elektronicznego** lub **Konsultant funkcjonalny raportowania elektronicznego** mogą edytować konfiguracje i uruchamiać je do celów testowych. Ten scenariusz może powodować wywoływanie metod klas i tabel mogących uszkadzać dane firmy i spowalniać działanie wystąpienia programu Finance and Operations.
-   Wywołania metod klas i tabel jako źródeł danych ER konfiguracji ER nie są ograniczone przez punkty wejścia do programu Finance and Operations ani logowanie do zasobów firmy. Dlatego poufne dane firmy mogą być dostępne dla użytkowników posiadających rolę **Deweloper raportowania elektronicznego** lub **Konsultant funkcjonalny raportowania elektronicznego**.

Konfiguracje ER zaprojektowane w środowisku programistycznym można przesłać do środowiska testowego w celu oceny konfiguracji (właściwa integracja procesów, poprawność wyników, wydajność) oraz sprawdzenia jakości (właściwe prawa dostępu według ról, podział obowiązków itd.). Do tego celu mogą służyć funkcje wymieniania się konfiguracją ER. Na koniec sprawdzone konfiguracje ER można przesłać do usługi LCS, gdzie zostaną udostępnione subskrybentom usługi, lub do środowiska produkcyjnego na potrzeby użytku wewnętrznego, jak pokazano na poniższej ilustracji. ![Cykl życia konfiguracji ER](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Informacje dodatkowe
--------

[Raportowanie elektroniczne — omówienie](general-electronic-reporting.md)



