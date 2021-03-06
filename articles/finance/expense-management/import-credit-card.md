---
title: Import i obsługa transakcji kartą kredytową
description: W tym temacie wyjaśniono sposób importowania i obsługi transakcji kartą kredytową dotyczących wydatków. Te transakcje można skonfigurować tak, aby były automatycznie importowane wg cyklicznego harmonogramu lub można je importować ręcznie w razie potrzeby.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187574"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Import i obsługa transakcji kartą kredytową

[!include [banner](../includes/banner.md)]

Transakcje kartą kredytową dotyczące wydatków można skonfigurować tak, aby były automatycznie importowane wg cyklicznego harmonogramu. Alternatywnie transakcje można zaimportować ręcznie w razie potrzeby. Transakcje kartą kredytową są importowane za pośrednictwem jednostki danych Transakcje kartą kredytową.

Aby uzyskać więcej informacji o jednostkach danych, zobacz [Jednostki danych](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Importowanie transakcji kart kredytowych

1. Na stronie **Transakcje karty kredytowej** wybierz opcję **Importuj transakcje**. Jeżeli otwierasz zarządzanie danymi po raz pierwszy, przed kontynuacją system musi zaktualizować listę jednostek danych.
2. W polu **Nazwa** wprowadź unikatowy opis zadana.
3. W polu **Format danych źródłowych** wybierz format pliku zawierający transakcje karty kredytowej do zaimportowania.
4. Wybierz opcję **Przekaż**, a następnie znajdź i wybierz plik do zaimportowania.
5. Po przekazaniu pliku sprawdź poprawność mapowania pliku transakcji karty kredytowej i kolumn jednostki danych Transakcje karty kredytowej, wybierając łącze **Wyświetl mapę** na kafelku. Jeżeli występują błędy mapowania lub musisz zmienić mapowanie, wprowadź zmiany w mapowaniu na karcie **Wizualizacja mapowania** lub karcie **Szczegóły mapowania**.
6. Aby zautomatyzować transakcje karty kredytowej, wybierz opcję **Utwórz cykliczne zadanie danych**. Następnie można ustawić cykle określający częstotliwość importowania transakcji karty kredytowej. Po zakończeniu wybierz przycisk **OK**.
7. Aby zaimportować wybrany plik teraz wybierz opcję **Importuj**.
8. Jeżeli podczas importowania wystąpi błąd, można wyświetlić dziennik wykonania lub dane pośrednie, aby zobaczyć błędy, które można usunąć, aby zapewnić pomyślny import.

> [!NOTE]
> Jeżeli musisz zaimportować plik w więcej niż jednym formacie, należy utworzyć osobne zadania importu dla każdego typu formatu.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ponowne przypisywanie transakcji karty kredytowej dla pracowników, których zatrudnienie zostało zakończone.

Po zakończeniu zatrudnienia pracownika jego konto usług Active Directory Domain Services (AD DS) jest wyłączane. Mogą jednak istnieć aktywne transakcje karty kredytowej, które muszą zostać zaliczone i zwrócone. Na stronie **Transakcje karty kredytowej** można zmienić przypisanie pracownika dla każdej transakcji kartą kredytową, której powiązany pracownik zakończył zatrudnienie.

Wybierz co najmniej jedną transakcję karty kredytowej, a następnie wybierz opcję **Przypisz ponownie transakcje**. Następnie możesz wybrać innego pracownika, aby przypisać do niego transakcje karty kredytowej. Po zmianie przypisania transakcji kartą kredytową transakcje można wybrać dla raportu o wydatkach i opłacić za pomocą zwykłego procesu uiszczania należności wykazanych w raporcie z wydatków.
