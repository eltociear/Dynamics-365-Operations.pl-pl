--- 
title: "Konfigurowanie wyceny konfigurowalnych produktów opartej na atrybutach"
description: "W tej procedurze pokazano sposób konfigurowania wyceny opartej na atrybutach."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: pl-pl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurowanie wyceny konfigurowalnych produktów opartej na atrybutach

[!include[task guide banner](../../includes/task-guide-banner.md)]

W tej procedurze pokazano sposób konfigurowania wyceny opartej na atrybutach. Warunkiem wstępnym jest istnienie modelu konfiguracji produktu, który ma jeden lub więcej składników i atrybutów. W przykładzie użyto modelu produktu Głośnik o wysokiej jakości zawartego w danych firmy demonstracyjnej USMF. Zazwyczaj procedurę wykonuje menedżer produktu.


## <a name="create-a-new-price-model"></a>Tworzenie nowego modelu ceny
1. Kliknij opcję Definicja modelu wariantu produktu.
2. Kliknij opcję Modele konfiguracji produktu.
3. Na liście zaznacz wiersz Głośnik o wysokiej jakości, ale nie klikaj łącza z nazwą.
4. W okienku akcji kliknij pozycję Model.
5. Kliknij opcję Modele ceny.
6. Kliknij przycisk Nowy.
7. W polu Nazwa modelu ceny wpisz wartość.
    * Użyj nazwy, która sprawi, że model będzie łatwy do zidentyfikowania.  
8. Wypełnij pole Opis.
9. Kliknij przycisk Zapisz.

## <a name="add-price-elements"></a>Dodawanie elementów ceny
1. Kliknij przycisk Edytuj.
    * Każdy składnik w modelu produktu może mieć element ceny podstawowej i dowolną liczbę reguł wyrażenia ceny. Można również dodawać ceny w różnych walutach.  
2. W polu Wyrażenie podstawy ceny wpisz wartość.
    * Na przykład wpisz 100.   Wyrażenie ceny podstawowej może być wartością liczbową lub mieć formę obliczenia arytmetycznego, w którym występuje jeden lub więcej atrybutów.  
3. Kliknij przycisk Dodaj.
4. W polu Nazwa wpisz „Rosewood”.
    * Nazwa wyrażenia ceny pomaga stwierdzić, co reprezentuje element ceny. W tym przykładzie tworzymy element ceny dla opcji wykończenie głośnika palisandrem.  
5. Kliknij opcję Edytuj warunek.
    * Warunek cenowy pomaga zagwarantować, że element wyrażenia ceny jest uwzględniany w cenie sprzedaży tylko wtedy, gdy występuje określona kombinacja atrybutów.  
6. W polu ConstraintBody wpisz „CabinetFinish=="Rosewood"”.
7. Kliknij przycisk OK.
8. W polu Wyrażenie wpisz wartość.
    * Na przykład wpisz 50.  
9. Zamknij stronę.
10. Zamknij stronę.

