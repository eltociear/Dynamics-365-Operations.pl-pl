---
title: Sprawdzanie jakości towarów
description: W tym temacie wyjaśniono sposób przetwarzania zlecenia kontroli jakości.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855693"
---
# <a name="inspect-the-quality-of-goods"></a>Sprawdzanie jakości towarów

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tym temacie wyjaśniono sposób przetwarzania zlecenia kontroli jakości. Zadania z przewodnika można wykonać przy użyciu danych firmy demonstracyjnej USMF. Przed rozpoczęciem tej przykładowej procedury należy potwierdzić zamówienia zakupu „000016” i zaksięgować dokument przyjęcia produktów. Spowoduje to automatyczne utworzenie zlecenia kontroli jakości. Kontrole jakości są zazwyczaj wykonywane przez pracownika ds. kontroli jakości.


## <a name="select-a-quality-order"></a>Wybieranie zlecenia kontroli jakości
1. W okienku nawigacji otwórz **Moduły > Zarządzanie zapasami > Zadania okresowe > Zarządzanie jakością > Zlecenia kontroli jakości**.
2. Przed rozpoczęciem tej procedury wybierz utworzone zlecenie kontroli jakości.  

## <a name="record-test-results"></a>Rejestrowanie wyników testów
1. Wybierz opcję **Wyniki**.
2. Wybierz opcję **Edycja**.
3. W polu **Liczba wyników** wprowadź liczbę.
4. W polu **Wynik** wybierz odpowiedni rekord z menu rozwijanego.  
- W tym przykładzie wynik bazuje na wstępnie zdefiniowanym wyniku. Zwyczajowo rejestruje się bardziej szczegółowy wynik inspekcji, na przykład rozmiaru lub innego wymiaru.  
5. Wybierz opcję **Zapisz**.
6. Zamknij stronę.

## <a name="validate-the-quality-order"></a>Sprawdź poprawność zlecenia kontroli jakości
1. Wybierz **Potwierdź**.
2. W polu **Poprawność sprawdzona przez** wybierz użytkownika wykonującego inspekcję z menu rozwijanego.  
3. Kliknij opcję **Wybierz**.
4. Kliknij przycisk **OK**.
5. Zamknij stronę.

