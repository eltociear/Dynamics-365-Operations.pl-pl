---
title: Przykład dni redukcji
description: Przykład dni redukcji.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564515"
---
# <a name="reduction-days-example"></a>Przykład dni redukcji 

[!include [banner](../includes/banner.md)]


Utworzono transakcję dla subskrypcji utrzymania wykupionej przez klienta, jak to pokazano w poniższej tabeli.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Data Od</p></th>
<th><p>Data Do</p></th>
<th><p>Subskrypcja</p></th>
<th><p>Typ subskrypcji</p></th>
<th><p>Project</p></th>
<th><p>Kategoria</p></th>
<th><p>Waluta sprzedaży</p></th>
<th><p>Cena sprzedaży</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 marca 2011</p></td>
<td><p>31 marca 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Normalna</strong></p></td>
<td><p>9013</p></td>
<td><p>KatSub2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Klient zgłasza, że nie potrzebuje serwisu przez dwa dni (10 i 11 marca). Zgadzasz się na ograniczenie subskrypcji w tych dniach.

Tworzysz nową transakcję typu **Dni redukcji**, jak to opisano w poniższej tabeli.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Data Od</p></th>
<th><p>Data Do</p></th>
<th><p>Subskrypcja</p></th>
<th><p>Typ subskrypcji</p></th>
<th><p>Project</p></th>
<th><p>Kategoria</p></th>
<th><p>Waluta sprzedaży</p></th>
<th><p>Cena sprzedaży</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 marca 2011</p></td>
<td><p>11 marca 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Dni redukcji</strong></p></td>
<td><p>9013</p></td>
<td><p>KatSub2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


W czasie fakturowania transakcji za miesiąc marzec 2011 roku cena sprzedaży 200 EUR zostaje obniżona o 12,90 EUR. Należność z tytułu transakcji subskrypcji wynosi zatem 187,10 EUR, a łączna wartość faktury dla dwóch transakcji wynosi 187,10 EUR.

## <a name="see-also"></a>Informacje dodatkowe

[Zmniejszanie dni na opłaty subskrypcji](reduce-the-days-on-subscription-fees.md)

  


