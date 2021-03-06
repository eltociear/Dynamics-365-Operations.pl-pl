---
title: Tworzenie zamówienia sprzedaży dla konfigurowalnego produktu
description: Ta procedura pokazuje sposób zastosowania szablonu konfiguracji do produktu w zamówieniu sprzedaży.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39ccb68ba76cd710412df6a46fc624608d02902b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844544"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Tworzenie zamówienia sprzedaży dla konfigurowalnego produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ta procedura pokazuje sposób zastosowania szablonu konfiguracji do produktu w zamówieniu sprzedaży. W przykładzie użyto modelu głośnika D0006 zawartego w danych firmy demonstracyjnej USMF. Zazwyczaj z tej procedury korzysta osoba przetwarzająca zamówienia sprzedaży.


## <a name="create-a-sales-order"></a>Utwórz zamówienie sprzedaży
1. Kliknij opcję Przetwarzanie zamówienia sprzedaży i dotyczące go zapytania.
2. Kliknij przycisk Nowy.
3. Kliknij opcję zamówienie sprzedaży.
4. W polu Konto odbiorcy zaznacz wartość US-001. 
5. Kliknij przycisk OK.
6. W polu Numer pozycji wybierz wartość D0006.
    * Dla tego zadania należy wybrać konfigurowalny produkt.  
7. Kliknij opcję Produkt i dostawa.
8. Kliknij opcję Konfiguruj wiersz.
    * Należy zauważyć, że cena zmieniła się na podstawie wybranej konfiguracji, a pole Uwzględnij kabel jest teraz ustawiony na wartość Prawda.  
    * Zwróć uwagę na domyślną cenę i ustawienia wybrane dla kabla.  
9. Kliknij przycisk Szablon ładunku.
    * W tym przykładzie pokazano, jak można zastosować szablon w celu wybrania wstępnie zdefiniowanej konfiguracji. Jeśli używasz tej procedury jako przewodnika po zadaniu i chcesz widzieć inne dostępne wartości atrybutów, kliknij przycisk Odblokuj.  
10. Kliknij przycisk OK.
11. Kliknij przycisk OK.
12. Rozwiń sekcję Szczegóły wiersza.
13. Kliknij kartę Produkt.
    * Konfiguracja towaru jest teraz wyświetlana w obszarze wymiarów produktu.  
14. Zamknij stronę.

## <a name="select-the-product-configuration"></a>Wybór konfiguracji produktu

