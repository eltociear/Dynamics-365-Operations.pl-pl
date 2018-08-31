---
title: "Poddawanie zwróconych towarów inspekcji"
description: "Zwrócone towary można poddawać inspekcji."
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: df209cfdbdef591e9f24161b3651316c43d69ee0
ms.contentlocale: pl-pl
ms.lasthandoff: 05/08/2018

---


# <a name="take-returned-items-through-inspection"></a>Poddawanie zwróconych towarów inspekcji 

[!include [banner](../includes/banner.md)]


1.  Kliknij kolejno opcje **Zarządzanie zapasami** \> **Okresowe** \> **Zarządzanie jakością** \> **Zlecenia kwarantanny**.

2.  Znajdź wiersz zamówienia odpowiadający zwracanemu towarowi, który jest sprawdzany.

    > [!NOTE]
    > <P>Zlecenie kwarantanny może być skojarzone tylko z jednym kodem towaru. Jeśli dziesięć towarów o różnych kodach zostanie zwróconych w ramach jednej wysyłki i wysłanych do kwarantanny, spowoduje to utworzenie dziesięciu odrębnych zleceń kwarantanny.</P>

3.  Po sprawdzeniu towaru należy w polu **Kod dyspozycji** wybrać odpowiednią opcję wskazującą, co zrobić z towarem i jak mają być obsługiwane powiązane transakcji finansowe. Jako przykłady można tu wymienić zwrócenie towaru do magazynu i zwrócenie pieniędzy odbiorcy, przeznaczenie towaru na odpadki i wysłanie odbiorcy towaru zastępczego lub zwrócenie towaru klientowi bez zwracania pieniędzy.
    
    > [!NOTE]
    > <P>Jeśli tego samego kodu dyspozycji nie można przypisać do wielu zwróconych towarów w partii o jednym numerze towaru, należy podzielić zlecenie kwarantanny (<STRONG>Funkcje</STRONG> &gt; <STRONG>Podziel</STRONG>), aby przypisać inny kod dyspozycji do każdej podpartii.</P>


4.  Po zakończeniu inspekcji kliknij przycisk **Zgłoszenie wyrobów gotowych**, aby zwolnić zwrócone towary i utworzyć wpis w arkuszu przyjazdu towaru. Następnie osoba lub dział, który przyjął towary, przetworzy arkusz w odniesieniu do towarów oczekujących na zwrot do magazynu.
    
    – lub –
    
    Zakończ zlecenie kwarantanny i przenieś towary bezpośrednio z powrotem do zapasów, używając jednej z funkcji **Zapasy**.

5.  Zamknij formularz, aby zapisać zmiany.

## <a name="see-also"></a>Informacje dodatkowe

[Określanie sposobu likwidacji zwróconych towarów](specify-how-to-dispose-of-returned-items.md)

  


