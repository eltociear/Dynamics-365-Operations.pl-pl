---
title: ER Używanie plików zarządzania dokumentami w danych wyjściowych formatu (Część 5 — Modyfikacja i inicjowanie formatu)
description: W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli administratora systemu lub dewelopera raportowania elektronicznego może tak skonfigurować format raportowania elektronicznego (ER), aby w danych wyjściowych raportowania elektronicznego używać plików zarządzania danymi (załączników).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550701"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER Używanie plików zarządzania dokumentami w danych wyjściowych formatu (Część 5 — Modyfikacja i inicjowanie formatu)

[!include [task guide banner](../../includes/task-guide-banner.md)]

W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli administratora systemu lub dewelopera raportowania elektronicznego może tak skonfigurować format raportowania elektronicznego (ER), aby w danych wyjściowych raportowania elektronicznego używać plików zarządzania danymi (załączników). Kroki można wykonać na danych firmy DEMF.

W celu wykonania tych kroków należy najpierw wykonać kroki procedury „ER Używanie plików zarządzania dokumentami w danych wyjściowych formatu (Część 4: Inicjowanie formatu)”.

Procedura dotyczy funkcji dodanej w programie Dynamics 365 for Operations w wersji 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Modyfikowanie formatu w celu dodania do generowanych komunikatów treści załączników w formacie binarnym
1. Wybierz kolejno opcje Administrowanie organizacją > Raportowanie elektroniczne > Konfiguracje.
2. W drzewie rozwiń węzeł „Model faktur sprzedaży”.
3. W drzewie rozwiń węzeł „Model faktur sprzedaży\Model faktur sprzedaży (niestandardowy)”.
4. W drzewie zaznacz element „Model faktur sprzedaży\Model faktur sprzedaży (niestandardowy)\Przykładowy komunikat faktury elektronicznej”.
5. Kliknij przycisk Konstruktor.
    * W generowanych danych wyjściowych wprowadzisz komunikat towarzyszący fakturze jako plik XML z kodowaniem UNICODE.  
6. Kliknij przycisk Dodaj element główny, aby otworzyć rozwijane okno dialogowe.
7. W drzewie zaznacz element „Wspólne\Plik”.
8. W polu Nazwa wpisz „Komunikat Xml”.
    * Komunikat Xml  
9. W polu Kodowanie wpisz „UTF-8”.
    * UTF-8  
10. Kliknij przycisk OK.
    * Skonfiguruj generowanie danych wyjściowych w formacie spakowanego pliku.  
11. Kliknij przycisk Dodaj element główny, aby otworzyć rozwijane okno dialogowe.
12. W drzewie zaznacz element „Wspólne\Folder”.
13. W polu Nazwa wpisz „Dane wyjściowe Zip”.
    * Dane wyjściowe Zip  
14. Kliknij przycisk OK.
15. W drzewie zaznacz element „Dane wyjściowe Zip”.
    * Dodaj załączniki do generowanego pliku zip jako pliki z oryginalnymi nazwami i rozszerzeniami.  
16. Kliknij przycisk Dodaj, aby otworzyć rozwijane okno dialogowe.
17. W drzewie zaznacz element „Wspólne\Plik”.
18. W polu Nazwa wpisz „Załączony plik”.
    * Załączony plik  
19. Kliknij przycisk OK.
20. W drzewie zaznacz element „Dane wyjściowe Zip\Załączony plik”.
21. Kliknij przycisk Dodaj, aby otworzyć rozwijane okno dialogowe.
22. W drzewie zaznacz element „Tekst\Base64”.
23. Kliknij przycisk OK.

## <a name="map-new-format-elements-to-data-model"></a>Mapowanie elementów nowego formatu na model danych
1. Kliknij kartę Mapowanie.
2. W drzewie rozwiń model„”
3. W drzewie rozwiń węzeł „model\Załączniki faktur”.
4. W drzewie zaznacz element „Dane wyjściowe Zip\Załączony plik\Base64”.
5. W drzewie zaznacz element „model\Załączniki faktur\Zawartość pliku”.
6. Kliknij opcję Powiąż.
7. W drzewie zaznacz element „Dane wyjściowe Zip\Załączony plik”.
8. Kliknij opcję Edytuj nazwę pliku.
9. W drzewie rozwiń model„”
10. W drzewie rozwiń węzeł „model\Załączniki faktur”.
11. W drzewie zaznacz element „model\Załączniki faktur\Nazwa pliku”.
12. Kliknij opcję Dodaj źródło danych.
13. Kliknij przycisk Zapisz.
14. Zamknij stronę.
15. W drzewie zaznacz element „model\Załączniki faktur”.
16. Kliknij opcję Powiąż.
17. Kliknij przycisk Zapisz.
18. Zamknij stronę.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Generowanie zaprojektowanego raportu dla wybranej faktury
1. Kliknij przycisk Uruchom.
2. Rozwiń sekcję Rekordy do uwzględnienia ().
3. Kliknij przycisk Filtr.
4. Zaznacz wiersz z arkuszem faktur dla odbiorcy i polem Zamówienie sprzedaży.
5. W polu kryteriów „Zamówienie sprzedaży” wpisz numer zamówienia 000148.
    * 000148  
6. Kliknij przycisk OK.
7. Kliknij przycisk OK.
    * Przejrzyj wygenerowane dane wyjściowe. Należy zauważyć, że oprócz komunikat faktury w formacie XML dla każdego załącznika utworzono również jeden plik. Pliki załączników są umieszczane w spakowanych danych wyjściowych w formacie binarnym.  

