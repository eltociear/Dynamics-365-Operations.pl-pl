---
title: Tworzenie zamówień sprzedaży
description: W tej procedurze pokazano sposób tworzenia zamówienia sprzedaży.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d235e32c7607add770fbf47f248edd9d965b2c0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834083"
---
# <a name="create-sales-orders"></a>Tworzenie zamówień sprzedaży

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tej procedurze pokazano sposób tworzenia zamówienia sprzedaży. Procedurę można wykonać przy użyciu danych firmy demonstracyjnej USMF. Zamówienia sprzedaży są zwykle tworzone przez agenta rozliczeniowego zamówień sprzedaży. 

## <a name="enter-sales-order-header-details"></a>Wprowadzanie szczegółów nagłówka zamówienia sprzedaży
1. Przejdź do **Okienko nawigacyji > Moduły > Sprzedaż i marketing >Wszystkie zamówienia sprzedaży**.
2. Wybierz pozycję **Nowy**.
3. W polu **Konto konta** kliknij rozwijany przycisk, aby otworzyć wyszukiwanie.
4. Na liście znajdź i zaznacz rekord odbiorcy.
    - W tym przykładzie należy wybrać numer odbiorcy US-004.  
5. Kliknij przycisk **OK**.

## <a name="enter-sales-order-line-details"></a>Wprowadzanie szczegółów wiersza zamówienia sprzedaży
    
Produkty sprzedawane przez organizację mogą występować w wariantach zróżnicowanych według wymiarów, takich jak konfiguracja, kolor, rozmiar i styl. Ponadto konfiguracja produktów może określać używanie wymiarów magazynowania, takich jak oddział, magazyn i paleta, oraz wymiarów śledzenia, takich jak numery partii i numery seryjne. Po przypisaniu tych wymiarów należy wybierać ich wartości w wierszu zamówienia. Aby zwiększyć efektywność wprowadzania zamówień, warto dodać pola odpowiednich wymiarów do siatki zamówień.
    
1. W sekcji **Linie zamówienia sprzedaży** wybierz opcję **Linia zamówienia sprzedaży**.
2. Wybierz ​**Wymiary**.
    
    W tym przykładzie należy wybrać wymiary Kolor, Oddział i Magazyn. Wybrane tutaj wymiary będą wyświetlane w siatce zamówień sprzedaży. Jeśli chcesz zapamiętać swój wybór, zaznacz "Tak" w opcji **Zapisz ustawienia**.
    
3. Kliknij przycisk **OK**.
4. W polu **Numer produktu** kliknij rozwijany przycisk, aby otworzyć wyszukiwanie.
5. W tym przykładzie zaznacz numer towaru T0004.
    - Jeśli towar jest częścią kategorii sprzedaży, nazwa towaru będzie automatycznie wyświetlana w polu Kategoria sprzedaży.  
    - Jeśli pole wymiaru produktu już zawiera wartość, wynika to z tego, że wartość została skopiowana z rekordu produktu, gdzie jest zdefiniowana jako domyślny wymiar produktu. Wartość domyślną można w każdej chwili zmienić.   
6. W polu **Kolor** kliknij rozwijany przycisk, aby otworzyć wyszukiwanie.
7. Na liście znajdź i zaznacz odpowiedni rekord.
8. W polu **Ilość** wpisz liczbę.
    - Jeśli przedmiot jest sprzedawany w innych jednostkach niż w chwili zakupu, produkcji i przechowywania, a jednostka sprzedaży jest ustawiona w historii produktu, ta wartość zostanie wyświetlona w polu **Jednostka**. Wartość można zmienić w dowolnym momencie.   
    - Jeśli pole **Strona** już zawiera wartość, wartość została skopiowana z nagłówka zamówienia lub z ustawień zamówienia powiązanych z produktem. Wartość można zmienić w dowolnym momencie. Jeśli pole jest puste, wprowadź wartość.   
    - Jeśli pole **Cena jednostki** już zawiera wartość, wartość została skopiowana z zatwierdzonej umowy handlowej lub z historii produktu. (Cena jednostkowa może także pochodzić z umowy sprzedaży, ale proces tworzenia zamówień sprzedaży na podstawie umów sprzedaży różni się od pokazanego tutaj). Jeśli pole jest puste, wprowadź wartość.   
    - Pole **Rabat** zawiera wartość rabatu na jednostkę produktu. Aby obliczyć kwotę rabatu dla łącznej wartości wiersza, wartość rabatu jest mnożona przez ilość w wierszu. Jeśli pole **Rabat** już zawiera wartość, wartość została skopiowana z zatwierdzonej umowy handlowej lub z historii produktu. Jeśli pole jest puste, a chcesz przyznać odbiorcy rabat od wiersza, wprowadź wartość.  
    - Pole **Procent rabatu** zawiera wartość procentową, o którą należy zmniejszyć całkowitą kwotę brutto linii.  Jeśli pole **Procent rabatu** już zawiera wartość, wartość została skopiowana z zatwierdzonej umowy handlowej. Jeśli pole jest puste, a chcesz przyznać odbiorcy rabat od wiersza, wprowadź wartość. 
    - Pole kwota **Netto** zawiera wartość, która jest obliczana na podstawie ilości linii i ceny jednostkowej skorygowanej o rabaty.  Obliczoną wartość można samodzielnie zastąpić inną.  

## <a name="review-the-order-totals"></a>Przegląd sum zamówienia
1. W **Panelu akcji** wybierz **Zamówienie sprzedaży**.
2. Wybierz **Sumy**.
    
    Strona **Sumy** pokazuje szczegóły całego zamówienia. Obejmuje to kwotę sumy częściowej, czyli sumę wszystkich kwot netto z wierszy skorygowaną o ewentualne rabaty do wierszy, łączną kwotę faktury, czyli kwota sumy częściowej skorygowaną o ewentualne rabaty na poziomie zamówienia, opłaty, podatek, ewentualne limity kredytowe przyznane odbiorcy, itd. Kwota faktury jest kwotą, która pojawi się w dokumencie faktury wystawionej odbiorcy.  
    
3. Kliknij przycisk **OK**.
