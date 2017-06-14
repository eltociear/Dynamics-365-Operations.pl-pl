---
title: Czeki postdatowane
description: "Ten artykuł zawiera informacje o obsłudze czeków postdatowanych w programie Microsoft Dynamics 365 for Operations. Czeki postdatowane są wystawiane do celów wykonywania i odbierania płatności w przyszłości. W związku z tym czeki można zrealizować dopiero od określonego dnia."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3e59ae5126cd21e668459686133ba8bcf728df3
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="postdated-checks"></a>Czeki postdatowane

[!include[banner](../includes/banner.md)]


Ten artykuł zawiera informacje o obsłudze czeków postdatowanych w programie Microsoft Dynamics 365 for Operations. Czeki postdatowane są wystawiane do celów wykonywania i odbierania płatności w przyszłości. W związku z tym czeki można zrealizować dopiero od określonego dnia.

Program Microsoft Dynamics 365 for Operations obsługuje pełny cykl zarządzania dla czeków postdatowanych w modułach Rozrachunki z odbiorcami i Rozrachunki z dostawcami, jak pokazano w poniższej tabeli.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenariusz</th>
<th>Szczegóły</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurowanie czeków postdatowanych</td>
<td>Należy utworzyć nową metodę płatności oraz określić procedurę płatności umożliwiającą rozliczanie kont czeków wystawionych, czeków otrzymanych i potrąconej zaliczki na podatek.</td>
</tr>
<tr class="even">
<td>Rejestruje czek postdatowany dla dostawcy i księgowanie</td>
<td>Zapisujesz szczegóły czeku postdatowanego wystawionego dostawcy. Po zaksięgowaniu płatności zobowiązanie wobec dostawcy jest rozpoznawane, ale konto bankowe nie jest jeszcze uznawane. Zamiast tego jest używane konto rozliczeniowe.</td>
</tr>
<tr class="odd">
<td>Rejestrowanie i księgowanie czeku postdatowanego dla odbiorcy</td>
<td>Zapisujesz szczegóły czeku postdatowanego otrzymanego od odbiorcy. Po zaksięgowaniu płatności należność od odbiorcy jest księgowana po stronie kredytowej, ale konto bankowe nie jest jeszcze obciążane. Zamiast tego jest używane konto rozliczeniowe.</td>
</tr>
<tr class="even">
<td>Rejestrowanie i księgowanie zastępczego czeku postdatowanego dla dostawcy lub odbiorcy</td>
<td>
Jeśli oryginalny czek dla dostawcy lub odbiorcy został zniszczony lub utracony, można wystawić zastępczy czek postdatowany. Podczas rejestrowania szczegółów czeku podaj odwołanie do oryginalnego czeku oraz wskaż, że nowy czek zastępuje oryginał. Można również zaksięgować czek zastępczy.</td>
</tr>
<tr class="odd">
<td>Przenoszenie czeku postdatowanego odbiorcy do dostawcy</td>
<td>Po otrzymaniu czeku postdatowanego od odbiorcy można go przenieść do dostawcy jako płatność.</td>
</tr>
<tr class="even">
<td>Rozliczenia postdatowanego czeku dla odbiorcy lub dostawcy</td>
<td>Rozliczanie w dniu terminu płatności czeku postdatowanego, który został zaksięgowany na koncie pomostowym dla odbiorcy lub dostawcy. Po rozliczeniu czeku konto bankowe jest ostatecznie obciążane lub uznawane względem użytego wcześniej konta rozliczeniowego.</td>
</tr>
<tr class="odd">
<td>Anulowanie postdatowanego czeku dla dostawcy</td>
<td>Zaksięgowany czek postdatowany można anulować w następujących sytuacjach: - Czek jest zwracany przez bank.
- Czeku dotyczy błędna faktura.
- Dokonywana jest płatność gotówką względem czeku.
</td>
</tr>
<tr class="even">
<td>Zatrzymywanie płatności czeku postdatowanego</td>
<td>Można zatrzymać zapłatę czeku postdatowanego wystawionego dostawcy, np. z powodu niewystarczających funduszy, zmiany warunków umowy z dostawcą, dostawy wadliwych towarów przez dostawcę lub zwrotu towarów do dostawcy. Zatrzymać można zapłatę tylko czeków nierozliczonych.</td>
</tr>
</tbody>
</table>






