---
title: "Definiowanie i obsługa kanałów sprzedaży detalicznej"
description: "Ten artykuł zawiera omówienie procesu konfigurowania sklepów tradycyjnych (fizycznych), określanych jako „sklepy detaliczne” (sklepy sieci sprzedaży) w programie Microsoft Dynamics 365 for Operations. Znajdują się tu informacje o zadaniach, które należy wykonać przed i po skonfigurowaniu sklepu detalicznego."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3de01350eafcccad8c49ac32eb2509a3d2975b6
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-maintain-retail-channels"></a>Definiowanie i obsługa kanałów sprzedaży detalicznej

[!include[banner](includes/banner.md)]


Ten artykuł zawiera omówienie procesu konfigurowania sklepów tradycyjnych (fizycznych), określanych jako „sklepy detaliczne” (sklepy sieci sprzedaży) w programie Microsoft Dynamics 365 for Operations. Znajdują się tu informacje o zadaniach, które należy wykonać przed i po skonfigurowaniu sklepu detalicznego.

Moduł Handel detaliczny i inny w programie Dynamics 365 for Operations obsługuje wiele kanałów sieci sprzedaży, takich jak sklepy internetowe, biura obsługi i sklepy tradycyjne. W module Handel detaliczny i inny sklep tradycyjny jest nazywany sklepem detalicznym. Każdy sklep detaliczny ma własne metody płatności, grupy cenowe, kasy punktów sprzedaży, konta przychodów i wydatków oraz personel. Wszystkie te elementy sklepu detalicznego należy skonfigurować przed jego utworzeniem. Po utworzeniu sklepu detalicznego, można przypisać produkty, które mają trafić do sklepu. Rejestry, pracowników i odbiorców również można przypisać do sklepu. Na koniec należy dodać nowy sklep do hierarchii organizacyjnej.

## <a name="setting-up-retail-stores"></a>Konfigurowanie sklepów detalicznych
Przed skonfigurowaniem sklepu detalicznego w programie Dynamics 365 for Operations należy wykonać niektóre zadania wymagań wstępnych. Następnie można utworzyć sklep detaliczny i dodać szczegóły.

### <a name="prerequisites"></a>Wymagania wstępne

Przed skonfigurowaniem sklepu detalicznego należy wykonać następujące zadania:

1.  Konfigurowanie struktury organizacji i hierarchii organizacyjnych dla asortymentów sieci sprzedaży, uzupełnień i raportowania.
2.  Konfigurowanie magazynu reprezentującego sklep detaliczny.
3.  Konfigurowanie sekwencji identyfikatorów dla sklepów detalicznych, zestawień dotyczących sklepu i załączników do zestawień.
4.  Konfigurowanie parametrów sprzedaży detalicznej.
5.  Konfigurowanie metod płatności, które akceptuje sklep.
6.  Do przetwarzania transakcji karty kredytowej w kasach punktów sprzedaży (POS) detalicznej można też skonfigurować usługi płatności.
7.  Konfigurowanie grup podatków.
8.  Konfigurowanie produktów sieci sprzedaży. W ramach tego zadania należy także skonfigurować hierarchie produktów sieci sprzedaży, asortymentów produktów i wariantów produktu.
9.  Konfigurowanie grup cenowych produktów.
10. Konfigurowanie kalkulacji cen produktu sieci sprzedaży. W ramach tego zadania można również ustawić korekty cen, rabaty i okresy rabatu.
11. Konfigurowanie członków personelu. **Uwaga:** Należy również przypisać odpowiednie uprawnienia do pracowników, tak aby mogli się logować i wykonywać zadania za pomocą systemu Dynamics 365 for Operations z aplikacją Retail POS.
12. Konfigurowanie profilów Retail POS, które mają zostać przypisane do danego sklepu. Konfigurowanie profilów obejmuje wiele zadań, takich jak konfigurowanie rejestrów, konfigurowanie profilów trybu offline i konfigurowanie profilów i formatów paragonu.

Przejrzyj wszystkie zadania zawarte w wymaganiach wstępnych i wykonaj tylko te, które odnoszą się do Ciebie.

### <a name="set-up-a-retail-store"></a>Konfigurowanie sklepu sieci sprzedaży

Po zakończeniu zadania wymagań wstępnych wykonaj te zadania, aby skonfigurować szczegóły sklepu detalicznego:

1.  Tworzenie sklepu detalicznego.
2.  Przypisywanie grupy podatków do sklepu.
3.  Przypisywanie akceptowanych metod płatności do sklepu.
4.  Dodawanie szczegółów do opisów produktów dla produktów, które oferujesz w sklepach detalicznych. Na przykład można dodawać obrazy i tekst sformatowany RTF. Te informacje szczegółowe o produkcie są wyświetlane w różnych kontekstach, takich jak kasy w punkcie sprzedaży lub wydrukowane etykiety.
5.  Dodawanie sklepu sieci sprzedaży do domyślnej hierarchii organizacyjnej przypisanej do celu **Asortyment sieci sprzedaży**, **Uzupełnianie zapasów sieci sprzedaży** lub **Raportowanie sieci sprzedaży**.

### <a name="after-you-set-up-a-retail-store"></a>Po skonfigurowaniu sklepu detalicznego

Po wprowadzeniu szczegółów sklepu detalicznego zakończ te zadania, aby wysłać nowe dane sklepu detalicznego do Retail POS.

1.  Konfigurowanie kas w punkcie sprzedaży dla sklepu.
2.  Dodawanie asortymentów produktów do sklepu.
3.  Przetwarzanie asortymentów, aby wygenerować listę produktów, które są uwzględnione w asortymencie i aby udostępnić produkty w sklepie detalicznym.
4.  Wysyłanie danych, takich jak sekwencje numerów, profile sprzętu, układy ekranu punktu sprzedaży do kas Retail POS.
5.  Publikowanie sklepu detalicznego, aby wysyłać dane sklepu do Retail POS.
6.  Uruchamianie zadań, aby wysyłać dane sklepu do Retail POS.

## <a name="organization-hierarchies"></a>Hierarchie organizacyjne
Handel detaliczny używa hierarchii organizacyjnych w systemie Microsoft Dynamics AX do struktury w kanałach sprzedaży detalicznej. Hierarchie organizacji reprezentują relacje między organizacjami, które składają się na działalność. Podczas konfigurowania sklepów, można je dodawać do hierarchii organizacyjnej. Sklepy współdzielą wówczas dane używane do asortymentów, uzupełnienia i raportów.



