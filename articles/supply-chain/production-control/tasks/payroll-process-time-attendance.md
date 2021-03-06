---
title: Włączanie procesu listy płac obliczanej na podstawie czasu i frekwencji
description: W tej procedurze pokazano sposób włączania procesu listy płac dla modułu Czas i frekwencja.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a52ad77d3f03898d26c225900fe79ca30493a67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843536"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Włączanie procesu listy płac obliczanej na podstawie czasu i frekwencji

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tej procedurze pokazano sposób włączania procesu listy płac dla modułu Czas i frekwencja. Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Tworzenie typu płacy z powiązaną stawką płacy
1. Czas i frekwencja > Ustawienia > Lista płac > Typy płac
2. Kliknij przycisk Nowy.
3. W polu Typ płacy wpisz wartość.
4. Wypełnij pole Opis.
5. Kliknij przycisk Zapisz.
6. Kliknij przycisk Stawki.
    * Stawki dla typów płac są konfigurowane w odniesieniu do określonych przedziałów czasowych, a dla poszczególnych pracowników można tworzyć indywidualne stawki. Nie zawsze jest konieczne tworzenie stawek dla typów płacy w module Czas i frekwencja. Te informacje mogą już istnieć w systemie listy płac, który służy do generowania pensji.  
7. Kliknij przycisk Nowy.
8. Na liście oznacz wybrany wiersz.
9. W polu Stawka wpisz liczbę.
10. Kliknij przycisk Zapisz.

## <a name="create-a-pay-agreement"></a>Tworzenie umowy płacowych
1. Zamknij stronę.
2. Zamknij stronę.
3. Przejdź do okna Umowy płacowe.
    * Czas i frekwencja > Ustawienia > Umowy płacowe  
4. Kliknij przycisk Nowy.
5. W polu Umowa płacowa wpisz wartość.
6. Wypełnij pole Opis.
7. Kliknij przycisk Zapisz.
8. Kliknij przycisk Wiersze umowy.
9. Kliknij przycisk Nowy.
10. Na liście oznacz wybrany wiersz.
11. W polu Typ profilu wprowadź lub wybierz wartość.
12. W polu Typ płacy wprowadź lub wybierz wartość.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Konfigurowanie umowy płacowej dla pracownika rozliczanego według czasu i rejestracji
1. Zamknij stronę.
2. Zamknij stronę.
3. Przejdź do okna Pracownicy odpowiedzialni za rejestrację czasu.
    * Czas i frekwencja > Ustawienia > Pracownicy odpowiedzialni za rejestrację czasu  
4. Na liście kliknij łącze w wybranym wierszu.
5. Kliknij kartę Zatrudnienie.
6. Rozwiń sekcję Rejestracja czasu.
7. Kliknij przycisk Edytuj.
8. W polu Umowa płacowa wprowadź lub wybierz wartość.

