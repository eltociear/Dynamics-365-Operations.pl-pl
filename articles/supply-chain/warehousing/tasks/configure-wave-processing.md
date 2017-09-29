--- 
title: "Konfigurowanie przetwarzania grupy czynności"
description: "W tym przewodniku opisano sposób konfigurowania kryteriów, które określają, jaka praca jest generowana dla magazynu podczas przetwarzania grupy czynności oraz czy grupy czynności są przetwarzane ręcznie czy automatycznie."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50988c689995dbb957af760c9c2c3b823f557c86
ms.contentlocale: pl-pl
ms.lasthandoff: 07/27/2017

---
# <a name="configure-wave-processing"></a>Konfigurowanie przetwarzania grupy czynności

[!include[task guide banner](../../includes/task-guide-banner.md)]

W tym przewodniku opisano sposób konfigurowania kryteriów, które określają, jaka praca jest generowana dla magazynu podczas przetwarzania grupy czynności oraz czy grupy czynności są przetwarzane ręcznie czy automatycznie. Kryteria można określić, definiując szablony grupy czynności i kwerendy, które dopasowują grupy czynności do zwolnionych wierszy w zamówieniach sprzedaży, zleceniach produkcyjnych i zleceniach Kanban. Przetwarzanie grup czynności jest stosowane w magazynach, które używają funkcji modułu Zarządzanie magazynem, a nie tych, które używają funkcji modułu Zarządzanie zapasami. Procedurę można wykonać przy użyciu danych firmy demonstracyjnej USMF.

1. Wybierz kolejno opcje Zarządzanie magazynem > Ustawienia > Grupy czynności > Szablony grupy czynności.
2. Kliknij przycisk Nowy.
3. W polu Nazwa szablonu grupy czynności wpisz wartość.
    * Podczas konfigurowania szablonu grupy czynności określasz kolejność, w jakiej szablony będą dopasowywane do zwolnionych wierszy zamówień sprzedaży, zleceń produkcyjnych lub kart Kanban. Podczas zwalniania wiersza do magazynu lub produkcji używa on pierwszego szablonu grupy czynności, którego kryteria spełnia. Zaleca się umieszczanie szablonów z najdokładniejszymi kryteriami u góry listy. Im szersze kryteria, tym łatwiej wiersz może je spełnić, co mogłoby spowodować, że wiersze będą przypisywane do niewłaściwych grup czynności.  
4. W polu Opis szablonu grupy czynności wpisz wartość.
5. W polu Oddział wprowadź lub wybierz wartość.
    * Jeśli używasz firmy demonstracyjnej USMF, można wybrać oddział 2.  
6. W polu Magazyn wprowadź lub wybierz wartość.
    * Jeśli używasz firmy USMF, można wybrać magazyn 24.  
7. W polu Automatyczne tworzenie grupy czynności ustaw wartość Tak.
    * Wybierz tę opcję, aby automatycznie utworzyć grupę czynności po zwolnieniu do magazynu zamówienia sprzedaży, zlecenia produkcyjnego lub karty kanban.  
8. W opcji Przetwarza grupę czynności w czasie uwalniania jej do magazynu zaznacz wartość Tak. 
    * Wybierz tę opcję, aby automatycznie przetworzyć grupę czynności i utworzyć pracę po zwolnieniu wiersza do magazynu.  
9. W polu Automatyczne uwolnienie grupy czynności ustaw wartość Tak. 
    * Gdy ta opcja jest wybrana, grupy czynności są uwalniane automatycznie. Praca pobierania jest tworzona i udostępniana na urządzeniach przenośnych.  
10. W opcji Przypisz do otwartych grup czynności zaznacz wartość Tak. 
    * Wiersze są przypisywane do grup czynności w oparciu o filtr kwerendy dla szablonu grupy czynności.  
11. W opcji Automatycznie przetwórz grupę czynności na progu zaznacz wartość Tak. 
    * Wybierz tę opcję, aby automatycznie wykonywać grupy czynności po osiągnięciu przez jego wartości progów dla wagi, wysyłki i wierszy określonych w grupie pól Progi grupy czynności. Ta opcja jest dostępna wyłącznie po wybraniu opcji Wysyłka w polu Typ szablonu grupy czynności.  
12. W polu Automatyczne zwalnianie pracy uzupełniania zapasów ustaw wartość Tak. 
    * Wybierz tę opcję, aby tworzyć pracę uzupełnienia opartą na żądaniu, i zwalniać ją automatycznie. Należy dodać do szablonu grupy czynności metodę grupy czynności uzupełnienia i utworzyć szablon uzupełnienia typu Popyt grupy czynności.  
13. Rozwiń sekcję Metody.
    * Metody szablonów grup czynności pozwalają sterować kolejnością działań wykonywanych na każdej grupie podczas jej przetwarzania. Na przykład może istnieć metoda uzupełniania zapasów dla grupy czynności. Po dodaniu metody jest ona automatycznie wyświetlana w odpowiednim miejscu w sekwencji etapów. Jeśli w opcji Automatyczne zwalnianie pracy uzupełniania zapasów zaznaczysz wartość Tak, trzeba dodać tutaj metodę uzupełniania zapasów.  
    * Atrybuty grupy czynności pełnią rolę filtrów ograniczających rodzaj towarów, które mogą używać grupy. Na przykład można określić grupę towarów.  
14. Kliknij przycisk Zapisz.
15. Zamknij stronę.
16. Wybierz kolejno opcje Zarządzanie magazynem > Ustawienia > Parametry zarządzania magazynem.
17. Rozwiń sekcję Przetwarzanie grupy czynności.
18. W polu Grupa przetwarzania wsadowego grupy czynności wpisz lub wprowadź wartość.
19. W opcji Przetwarzaj grupy czynności partiami zaznacz wartość Tak.
20. W polu Oczekiwanie na blokadę (ms) wprowadź liczbę.
    * Wprowadź czas w milisekundach, przez który nastąpi krok alokacji zaczeka na zasób systemowy zablokowany przez inny krok alokacji. Po przekroczeniu tego czasu grupa czynności nie jest przetwarzana i zostanie wyświetlony komunikat o błędzie.  
21. Kliknij przycisk Zapisz.
22. Zamknij stronę.
23. Wybierz kolejno opcje Kontrola produkcji > Ustawienia > Wybierz kolejno opcje Kontrola produkcji.
24. W polu Zwolnij do magazynu wybierz opcję.
    * W przypadku zamówień sprzedaży i zamówień Kanban zapasy muszą być zarezerwowane przed zwolnieniem zamówienia do magazynu. W przeciwnym razie towary lub wiersze alokacji nie mogą zostać przetworzone w grupie czynności. W przypadku zleceń produkcyjnych można również wybrać opcję Zezwalaj na częściową rezerwację. Na przykład jest to przydatne w przypadku materiałów, których produkcję należy uruchomić, a z zakończeniem procesu można poczekać na dostępność dodatkowych materiałów. Jeśli zostanie wybrana ta opcja, należy ręcznie powtórzyć zwolnienia do procesu magazynowego, gdy dodatkowe materiały stają się dostępne.  
25. Zamknij stronę.

