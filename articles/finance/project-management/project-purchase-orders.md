---
title: Zamówienia zakupu dla projektu
description: W tym artykule opisano różne metody, których można używać do tworzenia zamówień zakupu dla projektu. Wybrana metoda zależy od przeznaczenia zamówienia zakupu oraz od czasu zużywania kupionych towarów i zapisywania ich w ciężar projektu.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174565"
---
# <a name="purchase-orders-for-a-project"></a>Zamówienia zakupu dla projektu

[!include [banner](../includes/banner.md)]

W tym artykule opisano różne metody, których można używać do tworzenia zamówień zakupu dla projektu. Wybrana metoda zależy od przeznaczenia zamówienia zakupu oraz od czasu zużywania kupionych towarów i zapisywania ich w ciężar projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Metody tworzenia zamówienia zakupu

Można użyć jednej z następujących metod w celu utworzenia zamówienia zakupu w module Zarządzanie projektami i ich księgowanie. Przeznaczenie zamówienia zakupu decyduje o tym, kiedy jest ono zużywane i w efekcie kiedy towary są zapisywane w ciężar projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Cel</th>
<th>Zużycie towarów</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tworzenie zamówienia zakupu bezpośrednio z projektu</td>
<td>Użyj tej metody do zakupu towaru u zewnętrznego dostawcy w celu zużycia w projekcie. Zamówienie zakupu można utworzyć na dwa sposoby:
<ul>
<li>Z samego projektu. W tym przypadku projekt jest już zdefiniowany dla zamówienia zakupu.</li>
<li>Przechodząc do zamówienia zakupu projektu. Należy wybrać zarówno dostawcę, jak i projekt, dla których zostanie utworzone zamówienie zakupu.</li>
</ul></td>
<td>Towary są zużywane przy aktualizacji faktury dostawcy.</td>
</tr>
<tr class="even">
<td>Tworzenie zamówienia zakupu na podstawie zamówienia sprzedaży.</td>
<td>Ten metody należy używać do kupowania towarów w przypadku tworzenia zamówienia sprzedaży z projektu.</td>
<td>Towary są zużywane, gdy zamówienie sprzedaży jest fakturowane do odbiorcy.</td>
</tr>
<tr class="odd">
<td>Tworzenie zamówienia zakupu z zapotrzebowania na towar.</td>
<td>Tej metody należy używać do kupowania towarów w przypadku tworzenia zapotrzebowania na towar z projektu.</td>
<td>Towary są zużywane przy aktualizacji dokumentu dostawy dla zapotrzebowania na towar.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> W przypadku aktualizacji faktury od dostawcy lub dokumentu dostawy wyświetlany jest monit o aktualizację dokumentu dostawy w zapotrzebowaniu na towar.

Aby uzyskać więcej informacji, zobacz [Przyjmowanie towarów względem zamówienia zakupu z zapotrzebowania na towary](tasks/receive-items-purchase-order-item-requirement.md).

