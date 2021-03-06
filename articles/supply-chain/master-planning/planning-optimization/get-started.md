---
title: Rozpocznij pracę z optymalizacją planowania
description: W tym temacie wyjaśniono, jak zacząć używanie funkcji optymalizacji planowania.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076139"
---
# <a name="get-started-with-planning-optimization"></a>Rozpocznij pracę z optymalizacją planowania

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Funkcja optymalizacji planowania nie obsługuje obecnie wszystkich funkcji dostępnych w aparacie planowania wbudowanym w rozwiązanie Microsoft Dynamics 365 Supply Chain Management. Dlatego ważne jest, aby ocenić, czy aktualnie dostępna w optymalizacji planowania funkcja ma spełniać wymagania użytkownika. Domyślnie funkcja optymalizacji planowania nie jest domyślnie włączona w usłudze Dynamics Lifecycle Services (usługi LCS). Z tego względu użytkownik ma możliwość wykonania oceny przed jej włączeniem.

Ostatecznie Optymalizacja planowania zastąpi istniejący wbudowany silnik planowania Supply Chain Management.

Przed włączeniem optymalizacji planowania zdecydowanie zaleca się dokonanie oceny wyników analizy pasującej do optymalizacji planowania. Aby uzyskać więcej informacji, zobacz [Analiza dopasowywania optymalizacją planowania](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Licencjonowanie

Jeśli planowanie główne można uruchomić za pomocą bieżącej licencji, nie trzeba kupować dodatkowej licencji, aby zacząć korzystać z optymalizacji planowania.

### <a name="install-the-add-in"></a>Instalacja aplikacji dodatkowych

Aby skorzystać z optymalizacji planowania, zainstaluj dodatek optymalizacji planowania dla Dynamics 365 Supply Chain Management. Można uzyskać dostęp do dodatku z projektu usługi LCS i włączyć funkcję optymalizacji planowania z poziomu interfejsu użytkownika Supply Chain Management.

> [!NOTE]
> Wymóg na optymalizację planowania to środowisko wysokiej dostępności z włączonymi usługami LCS (a nie środowisko OneBox), z Dynamics 365 Supply Chain Management w wersji 10.0.7 lub nowszej.

1. Zaloguj się do usługi LCS i otwórz żądane środowisko.
1. Przejdź do **Pełne szczegóły**.
1. Przewiń w dół do pozycji skróconej karty **Zarządzaj dodatkami środowiskowymi**.
1. Wybierz opcję **Zainstaluj nowy dodatek**.
1. Wybierz **Planowanie optymalizacji**.
1. Postępuj zgodnie z instrukcją instalacji i zaakceptuj warunki.
1. Wybierz **Zainstaluj**.
1. W skróconej karcie **Dodatki środowiska** widać, czy jest instalowana Optymalizacja planowania.
1. Po kilku minutach **Instalowanie** zmieni się na **Zainstalowane** (konieczne może być odświeżenie strony). Po zainstalowaniu można już aktywować optymalizację planowania w systemie Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Integracja optymalizacji planowania

Aby określić, czy dodatek optymalizacji planowania ma być używany w planowaniu głównym, należy przejść do **Planowanie główne** \> **Ustawienia** \> **Integracja optymalizacji planowania**.

#### <a name="connection-status"></a>Stan połączenia

Stan połączenia wskazuje bieżący stan połączenia między Supply Chain Management a usługą optymalizacji planowania. Poniższa tabela przedstawia możliwe wartości.

| Stan połączenia | Opis | Czy można użyć optymalizacji planowania? |
|---|---|---|
| Połączono | Ustanowiono połączenie między usługą optymalizacji planowania i Supply Chain Management. | Tak |
| Włączanie połączenia | Obecnie trwa żądanie włączenia połączenia do usługi optymalizacji planowania. | Nie |
| Rozłączono | Nie istnieje połączenie z usługą optymalizacji planowania. Połączenie można włączyć z usługi LCS, jak opisano wcześniej w tym temacie. | Nie |
| Wyłączanie połączenia | Obecnie trwa żądanie wyłączania połączenia do usługi optymalizacji planowania. | Nie |
| Pobieranie informacji o stanie | System oczekuje na informacje o stanie z usługi optymalizacji planowania. | Nie |

#### <a name="the-use-planning-optimization-option"></a>Opcja Zastosuj optymalizację planowania

Ustawienie opcji **Zastosuj optymalizację** planowania określa, który Aparat planowania będzie używany w planowaniu głównym:

- **Tak** — Optymalizacja planowania jest używana do planowania głównego.
- **Nie** – wbudowany silnik planowania Supply Chain Management jest używany do planowania głównego.

> [!NOTE]
> Jeśli istniejące zadania wsadowe planowania utworzone dla wbudowanego silnika planowania Supply Chain Management dostaw są wyzwalane, a opcja **Użyj optymalizacji planowania** jest ustawiona na wartość **tak**, zadania te nie powiodą się.

### <a name="integration-with-the-setup"></a>Integracja z ustawieniami

Jeśli opcja Podgląd optymalizacji planowania jest włączona, planowanie główne jest wykonywane przy użyciu dodatku Optymalizacja planowania. W takim przypadku wpływa to na wyniki i funkcje planowania głównego.

## <a name="related-resources"></a>Powiązane zasoby

[Warunki i postanowienia dla wersji zapoznawczej](https://go.microsoft.com/fwlink/?linkid=2015274)

[Omówienie planowania optymalizacji](planning-optimization-overview.md)

[Analiza dopasowywania optymalizacją planowania](planning-optimization-fit-analysis.md)

[Wyświetlanie dzienników historii i planowania planów](plan-history-logs.md)

[Stosowanie filtrów do planu](plan-filters.md)

[Anuluj planowanie pracy](cancel-planning-job.md)
