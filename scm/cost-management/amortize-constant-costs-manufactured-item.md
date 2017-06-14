---
title: "Amortyzowanie kosztów stałych wytworzonego towaru"
description: "Stałe koszty wytworzonego towaru odzwierciedlają czas przezbrajania dla danej operacji oraz składniki o stałej ilości lub stałą ilość odpadków."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f9c6e9a10befec1775fe031295f0a29d936a8ed8
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortyzowanie kosztów stałych wytworzonego towaru

[!include[banner](../includes/banner.md)]


Stałe koszty wytworzonego towaru odzwierciedlają czas przezbrajania dla danej operacji oraz składniki o stałej ilości lub stałą ilość odpadków. 

Podczas amortyzowania tych kosztów stałych w obliczonych kosztach wytworzonego towaru jest używana koncepcja wielkości partii do wyceny. Nazwa tej koncepcji ma kilka synonimów, na przykład „księgowa wielkość partii”. Również koncepcja amortyzowania kosztów stałych ma kilka nazw, np. „proporcjonalne koszty stałe”.
Ilość w wielkości partii do wyceny dla wyprodukowanego towaru jest używana do obliczenia listy składowej (BOM). Wielkość ta zależy od sposobu inicjowania i wykonywania obliczeń BOM, tak jak przedstawiono poniżej:
-   Domyślna ilość obliczania w obliczeniach BOM towaru — Standardowa ilość zamówienia towaru z zapasów pełni rolę wielkości partii do wyceny, ale wartość domyślna może być większą ilością w celu odzwierciedlenia wielokrotności ilości zamówienia towaru. Standardową ilość zamówienia towaru oraz wielokrotność można zdefiniować w ramach domyślnych ustawień zamówień lub ustawień zamówień właściwych dla oddziału.
-   Określona ilość obliczania w obliczeniach BOM towaru — określona ilość obliczania służy jako wycena rozmiaru partii danego towaru. Na początku ilość obliczania jest równa standardowej ilości zamówienia towaru, ale wartość domyślną można ręcznie zastąpić. Podana ilość obliczania reprezentuje wielkość partii do wyceny dla określonego towaru i dla wytworzonych składników, których typem wiersza BOM jest Produkcja. Jest to spowodowane założeniem, że składnik zostanie wyprodukowany w ściśle określonej ilości. Rozmiar partii do wyceny innych wytwarzanych składników mających typ wiersza BOM Towar będzie odzwierciedlać standardową ilość zamówienia.
-   Określona ilość obliczania produkcji na zamówienie w obliczeniach BOM towaru — określona ilość obliczania służy jako wycena rozmiaru partii towaru i jego wyprodukowanych składników, gdy w obliczeniach BOM jest używany tryb rozłożenia produkcji na zamówienie. Zakłada się, że wytwarzane składniki będą produkowane aż do osiągnięcia określonej ilości, tak jak w przypadku wytwarzanych składników o typie wiersza BOM Produkcja.
-   Określona ilość obliczania w obliczeniach BOM zależnych od zamówienia — obliczenia BOM zależne od zamówienia mogą być wykonywane w wypadku elementu wiersza w zamówieniu sprzedaży, ofercie sprzedaży lub zleceniu serwisowym. Podana ilość obliczania jest równa ilości pierwotnej pozycji w wierszu, ale ilość domyślną można zastąpić. Można wybrać, czy w obliczeniach BOM zależnych od zamówienia jest używany tryb rozłożenia produkcji na zamówienie, czy wielopoziomowy tryb rozłożenia.

Obliczona kwota zamortyzowanych stałych kosztów wytworzonego towaru jest określana jako opłaty.





