---
title: "Wartości obiektu zapasów"
description: "Ten artykuł zawiera informacje o sposobie obliczania wartości obiektu zapasów."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3149edfb54bad12fad043b78d9a6d3a7527f18e1
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-object-values"></a>Wartości obiektu zapasów

[!include[banner](../includes/banner.md)]


Ten artykuł zawiera informacje o sposobie obliczania wartości obiektu zapasów. 

Nowa funkcja o nazwie **Ilość fizyczna**pozwala zobaczyć wartości zapasów określonego obiektu magazynu. 

Obiekt kosztów reprezentuje poziom podmiotu, w którym są wykonywane operacje księgowania zapasów. Aby uzyskać więcej informacji o obiektach kosztów, zobacz temat [Obiekty kosztów](cost-object.md). 

Aby wyświetlić wartości określonego obiektu zapasów, kliknij opcję **Ilość fizyczna** na stronie **Obiekt kosztów**. Obliczanie wartości obiektu zapasów: 

Obiekt zapasów.Wartość = Obiekt kosztów.Średni koszt jednostkowy × Obiekt zapasów.Ilość 

Poniższy przykład pokazuje sposób obliczania wartości obiektu zapasów i obiektu kosztów. Zarejestrowane są dwa zdarzenia dokumentu przyjęcia produktów dla pozycji A:

-   Dokument przyjęcia produktów 1: ilość = 100 sztuk., Kwota = 1000,00 USD, Oddział = 1, Magazyn = 11, Nr partii = B1
-   Dokument przyjęcia produktów 2: ilość = 50 sztuk., Kwota = 800,00 USD, Oddział = 1, Magazyn = 11, Nr partii = B2

Poniższa tabela przedstawia wynik obliczeń dla obiektu kosztów. Wyniki można wyświetlać na stronie **Obiekt kosztów**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ obiektu</th>
<th>Numer pozycji</th>
<th>Oddział</th>
<th>Ilość</th>
<th>Jednostka magazynowa</th>
<th>Wartość</th>
<th>Średni koszt jednostkowy</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Obiekt kosztów</td>
<td>I</td>
<td>1 przypada na wpłatę z zysku na rzecz budżetu państwa</td>
<td>150</td>
<td>Szt.</td>
<td><p>1800,00 USD</p></td>
<td><p>12,00 USD</p></td>
</tr>
</tbody>
</table>

Poniższa tabela przedstawia wynik obliczeń dla obiektu magazynu. Wyniki można wyświetlać, klikając **Ilość fizyczna** na stronie **Obiekt kosztów**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Typ obiektu</th>
<th>Numer pozycji</th>
<th>Oddział</th>
<th>Magazyn</th>
<th>Numer partii</th>
<th>Ilość</th>
<th>Jednostka magazynowa</th>
<th>Wartość</th>
<th>Średni koszt jednostkowy</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Obiekt magazynu</td>
<td>I</td>
<td>1 przypada na wpłatę z zysku na rzecz budżetu państwa</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Szt.</td>
<td><p>1200,00 USD</p></td>
<td><p>12,00 USD</p></td>
</tr>
<tr class="even">
<td>Obiekt magazynu</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Szt.</td>
<td><p>600,00 USD</p></td>
<td><p>12,00 USD</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Informacje dodatkowe
--------

[Obiekty kosztów](cost-object.md)

[Wpisy kosztów](cost-entries.md)

[Nowości i zmiany w programie Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)



