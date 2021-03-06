---
title: Potwierdzanie zamówień sprzedaży
description: Ta procedura przedstawia sposób potwierdzenia zamówień sprzedaży.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9274a90ffbf6e5703d3ed97a8b974227b25c2a0
ms.sourcegitcommit: 62d66f98d4bbf916e19184506b90055bb68d219f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/28/2019
ms.locfileid: "1924385"
---
# <a name="confirm-sales-orders"></a>Potwierdzanie zamówień sprzedaży

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ta procedura przedstawia sposób potwierdzenia zamówień sprzedaży. Zobaczysz, jak potwierdzić pojedyncze zamówienie, a jak wiele zamówień na raz. Te zadania zazwyczaj wykonuje agenta rozliczeniowego zamówień sprzedaży. Można wykonać tę procedurę przy użyciu danych firmy demonstracyjnej USMF lub własnych danych. Przed rozpoczęciem upewnij się, że istnieje kilka otwartych zamówień sprzedaży dla tego samego odbiorcy. Jeśli używasz firmy USMF, można użyć odbiorcy US-027.


## <a name="confirm-a-single-sales-order"></a>Potwierdzanie jednego zamówienia sprzedaży
1. Przejdź do **Okienko nawigacyji > Moduły > Sprzedaż i marketing >Wszystkie zamówienia sprzedaży**.
2. Na liście odszukaj i zaznacz zamówienie, które chcesz potwierdzić.
3. Kliknij łącze na numerze zamówienia sprzedaży, aby otworzyć wybrane zamówienie.
4. W **Panelu akcji** kliknij **Sprzedaj**.
5. Kliknij opcję **Potwierdź zamówienie sprzedaży**.
6. Rozwiń sekcję **Parametry**. Sprawdź, czy w opcji **Księgowanie** jest ustawiona wartość „Tak”.  
7. W opcji **Drukowanie potwierdzenia** zaznacz wartość „Tak”. Pole **Sprawdzanie limitu kredytu** określa metodę używaną do obliczania pozostałego kredytu odbiorcy. Domyślnie kod jest kopiowany ze strony Parametry modułu rozrachunków z odbiorcami. Jeśli chcesz pominąć sprawdzanie limitu kredytu podczas potwierdzania określonego zamówienia sprzedaży, ustawić pole **Sprawdzanie limitu kredytu** na „Brak”. Należy jednak pamiętać, że nawet w przypadku, gdy to pole ustawiono na wartość „Brak”, sprawdzanie limitu kredytu będzie wciąż wykonywane, jeśli w danych głównych odbiorcy wybrano opcję **Wymagany limit kredytu**. 
8. Kliknij przycisk **OK**.
9. Kliknij przycisk **Tak**.
10. Zamknij stronę.
11. W **okienku akcji** kliknij pozycję **Opcje**.
12. Kliknij przycisk **Zmień widok**.
13. Kliknij opcję **Widok nagłówka**. Po potwierdzeniu zamówienia pole **Stan dokumentu** jest ustawiane na „Potwierdzenie”. 
14. W **Panelu akcji** kliknij **Sprzedaj**.
15. Kliknij opcję **Potwierdzenie zamówienia sprzedaży**.
16. Zamknij stronę.

## <a name="confirm-multiple-sales-orders-at-once"></a>Potwierdzanie wielu zamówień sprzedaży jednocześnie
1. Wybierz kolejno opcje **Sprzedaż i marketing > Zamówienia sprzedaży > Potwierdzenie zamówienia > Potwierdź zamówienie sprzedaży**.
2. Kliknij opcję **Wybierz**.
3. Na karcie **Zakres** na liście znajdź i zaznacz rekord odwołujący się do pola **Konto odbiorcy**.
4. W polu **Kryteria** kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.
5. Na liście znajdź i wybierz konto odbiorcy mające wiele zamówień, które chcesz potwierdzić grupowo. Jeśli używasz firmy USMF, można wybrać klienta US-027.  
6. Kliknij przycisk **OK**.
    - Karta **Przegląd** zawiera listę zamówień, które spełniają kryteria zapytania. Zamówienia te zostaną uwzględnione w potwierdzeniu.  
    - Pole **Aktualizacja zbiorcza** w sekcji **Parametry** określa parametr, przy użyciu którego wiele zamówień ma być sumowanych do jednego dokumentu potwierdzenia. Domyślnie opcja jest kopiowana z ustawienia Wartości **Wartości domyślne aktualizacji zbiorczej** znajdującego się na stronie **Parametry modułu rozrachunków z odbiorcami**.  
7. W pola **Aktualizacja zbiorcza** zaznacz opcję „Zamówienie”. Minimalne parametry, które są wymagane do tworzenia aktualizacji zbiorczych, to **Konto płatnika** i **Waluta**. Oznacza to, że aktualizacje zbiorcze mające różne konta płatnika i różne waluty są niedozwolone. Dodatkowe parametry można skonfigurować na stronie **Parametry aktualizacji zbiorczej**, która jest dostępna ze strony **Parametry modułu rozrachunków z odbiorcami**. 
8. W polu **Zamówienie sprzedaży** kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.
9. Na liście zaznacz numer zamówienia, które chcesz, aby było zamówieniem zbiorczym.
10. Kliknij przycisk **Rozmieść**.
11. Kliknij przycisk **OK**.
12. Kliknij przycisk **OK**.

