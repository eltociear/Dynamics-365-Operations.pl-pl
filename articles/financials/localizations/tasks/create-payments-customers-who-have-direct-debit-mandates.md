--- 
title: "Tworzenie płatności dla odbiorcy, który ma pozwolenie na polecenie zapłaty"
description: "W tej procedurze pokazano sposób generowania pliku płatności poleceniem zapłaty ISO20022 dla odbiorcy, który ma skonfigurowaną obsługę poleceń zapłaty i fakturę do zapłaty."
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: pl-pl
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Tworzenie płatności dla odbiorcy, który ma pozwolenie na polecenie zapłaty

[!include[task guide banner](../../includes/task-guide-banner.md)]

W tej procedurze pokazano sposób generowania pliku płatności poleceniem zapłaty ISO20022 dla odbiorcy, który ma skonfigurowaną obsługę poleceń zapłaty i fakturę do zapłaty. Tworzenie i księgowanie faktury jest opcjonalne. Zamiast mieć fakturę do zapłaty można przed wygenerowaniem pliku płatności wybrać w arkuszu zgodę, aby umożliwić obsługę scenariusza przedpłaty od odbiorcy.



Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej DEMF.



Jest to piąta z pięciu procedur, które razem przedstawiają proces płatności od odbiorców przy użyciu konfiguracji raportowania elektronicznego. Przed wykonaniem tego zadania należy wykonać wcześniejsze zadania. Najpierw należy zaimportować konfiguracje elektronicznego raportowania płatności od odbiorcy oraz skonfigurować metodę płatności, firmę i informacje o odbiorcy. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Księgowanie faktury niezależnej z danymi polecenia zapłaty
1. Wybierz kolejno opcje Rozrachunki z odbiorcami > Faktury > Wszystkie faktury niezależne.
2. Kliknij przycisk Nowy.
3. W polu Konto odbiorcy wprowadź lub wybierz wartość.
    * Na przykład zaznacz DE-010.  
4. W polu Metoda płatności wprowadź lub wybierz wartość.
    * Na przykład wybierz opcję Elektroniczne.  
5. W polu Identyfikator zgody na polecenie zapłaty wprowadź lub wybierz wartość.
6. Kliknij przycisk Dodaj wiersz.
7. W polu Opis wpisz wartość.
8. W polu Konto główne podaj żądane wartości.
9. Wprowadź liczbę w polu Cena jednostkowa.
10. Kliknij przycisk Księguj.
11. Kliknij przycisk OK.

## <a name="create-a-payment"></a>Tworzenie płatności
1. Wybierz kolejno opcje Rozrachunki z odbiorcami > Płatności > Arkusz płatności.
2. Kliknij przycisk Nowy.
3. W polu Nazwa wprowadź lub wybierz wartość.
4. Kliknij przycisk Wiersze.
5. Kliknij opcję Propozycja płatności.
6. Kliknij opcję Utwórz propozycję płatności.
7. Rozwiń sekcję Rekordy do uwzględnienia.
8. Kliknij przycisk Filtr.
9. Na liście zaznacz wiersz w tabeli Transakcje odbiorcy oraz pole Metoda płatności.
    * Można zastosować dowolne kryteria w celu wybrania transakcji z odbiorcą, które mają zostać opłacone. W tym przykładzie należy użyć opcji Elektroniczne jako metody płatności do wyfiltrowania transakcji.  
10. W polu Kryteria wprowadź lub wybierz wartość.
11. Kliknij przycisk OK.
12. Kliknij przycisk OK.
13. Kliknij opcję Utwórz płatności.

## <a name="generate-a-payment-file"></a>Generowanie pliku płatności

