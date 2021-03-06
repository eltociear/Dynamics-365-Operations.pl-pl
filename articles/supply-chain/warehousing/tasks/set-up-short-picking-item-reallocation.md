---
title: Konfigurowanie zmiany alokacji pozycji na potrzeby pobierania w niedomiarze
description: Ta procedura pokazuje, jak umożliwić pracownikom magazynu szybkie znajdowanie alternatywnych lokalizacji, jeżeli nie ma wystarczających zapasów w lokalizacji, do której zostali skierowani.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916767"
---
# <a name="set-up-short-picking-item-reallocation"></a>Konfigurowanie zmiany alokacji pozycji na potrzeby pobierania w niedomiarze

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ta procedura pokazuje, jak umożliwić pracownikom magazynu szybkie znajdowanie alternatywnych lokalizacji, jeżeli nie ma wystarczających zapasów w lokalizacji, do której zostali skierowani. Istnieje możliwość używania procesu automatycznej zmiany alokacji, który wykorzystuje dyrektywy lokalizacji do pobierania towarów, jeśli są one dostępne w innej lokalizacji. Alternatywnie w przypadku używania ręcznej zmiany alokacji na urządzeniu przenośnym jest wyświetlana lista lokalizacji z dostępnymi ilościami, dzięki czemu pracownik magazynu może wybrać lokalizację do pobrania zapasów. Procedurę można wykonać przy użyciu danych firmy demonstracyjnej USMF. Procedura dotyczy funkcji dodanej w programie Dynamics 365 for Operations w wersji 1611.


## <a name="set-up-work-exceptions"></a>Ustaw wyjątki pracy
1. W **okienku nawigacji** przejdź do **Zarządzanie magazynem > Ustawienia > Praca > Wyjątki dotyczące pracy**.
2. Kliknij przycisk **Nowy**. Istnieje możliwość zdefiniowania kilku wyjątków dotyczących pracy z różnymi zasadami zmiany alokacji towarów, aby umożliwić pracownikowi magazynu wybór towaru na podstawie potrzeb przesyłki, którą akurat przetwarza.  
3. W polu **Kod wyjątku pracy** wpisz wartość. Zatytułuj wyjątek dotyczący pracy w taki sposób, aby wskazywał, do czego wyjątek jest używany. Na przykład: Ręczne pobieranie w niedomiarze.  
4. W polu **Opis** wpisz wartość.
5. W polu typ **Wyjątku** zaznacz wartość „Pobranie w niedomiarze”.
6. Zaznacz pole wyboru **Korekta zapasów**. Ta opcja oznacza, że zapasy będą automatycznie korygowane na 0 w lokalizacji pobierania w niedomiarze.  
7. W polu **Kod domyślnego typu korekty** wprowadź lub wybierz wartość. Na przykład w firmie USMF można wybrać pozycję „Usuń Res Adj Out”.  
8. W polu **Zmiana alokacji pozycji** wybierz opcję „Ręcznie”. Jeśli wybierzesz opcję Ręcznie lub Automatyczne i ręczne, pracownikowi magazynu trzeba włączyć funkcję stosowania ręcznej zmiany alokacji.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurowanie pracownika do używania ręcznej zmiany alokacji
1. Zamknij stronę.
2. W **okienku nawigacji** przejdź do **Zarządzanie magazynem > Ustawienia > Pracownik**.
3. Kliknij przycisk **Edytuj**.
4. Na liście zaznacz pracownika 24.
5. Rozwiń skróconą kartę **Praca**.
6. W polu **Zezwalaj na ręczną zmianę alokacji pozycji** wybierz opcję „Tak”.

