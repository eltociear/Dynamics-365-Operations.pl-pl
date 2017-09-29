---
title: "Planowanie w trybie mieszanym — łączenie sourcingu dyskretnego, procesowego i produkcji oszczędnej"
description: "Ten artykuł zawiera informacje o mieszanym trybie planowania. W planowaniu w trybie mieszanym można modelować łańcuch dostaw na podstawie przepływu materiałów. Program Microsoft Dynamics 365 for Finance and Operations zapewnia, że przepływ materiałów następuje zgodnie z modelami, bez względu na wybrane zasady dostawy (karty Kanban, zlecenia produkcyjne, zamówienia zakupu, szarże produkcyjne lub zamówienia przeniesienia)."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9dbbe540c919d27bafcc10614f308e5b6ba313f1
ms.contentlocale: pl-pl
ms.lasthandoff: 06/13/2017

---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Planowanie w trybie mieszanym — łączenie sourcingu dyskretnego, procesowego i produkcji oszczędnej

[!include[banner](../includes/banner.md)]


Ten artykuł zawiera informacje o mieszanym trybie planowania. W planowaniu w trybie mieszanym można modelować łańcuch dostaw na podstawie przepływu materiałów. Program Microsoft Dynamics 365 for Finance and Operations zapewnia, że przepływ materiałów następuje zgodnie z modelami, bez względu na wybrane zasady dostawy (karty Kanban, zlecenia produkcyjne, zamówienia zakupu, szarże produkcyjne lub zamówienia przeniesienia). 

Można wybrać ogólną strategię dostarczania produktów, niezależnie od struktury produktów.  

Na przykład możesz mieć formant Kanban w montażu, w którym materiały są pozyskiwane z obszaru montażowego według zleceń produkcyjnych, kart Kanban, przeniesień, zamówień partii lub dowolnej kombinacji elementów odpowiadającej charakterystyce łańcucha dostaw, i zachować pełną widoczność całego procesu zaopatrzenia. To ułatwia optymalizację procesów w łańcuch dostaw i zapewnia lepszą jego widoczność.  

Szczegółowość zasad zaopatrzenia, które są używane w planowaniu głównym, zależy od wymiarów magazynowych włączonych jako wymiary zapotrzebowania. Aby włączyć planowanie główne do kontrolowania uzupełniania zapasów i dostaw w różnego rodzaju lokalizacjach (np. oddzielając przestrzeń produkcyjną dla różnych jednostek produkcyjnych lub oddzielając różne typy magazynów materiałów i gotowych wyrobów), najlepiej jest włączyć jako wymiary zapotrzebowania opcje Oddział i Magazyn. Magazyn może też być pomijany jako wymiar zapotrzebowania. W takim przypadku podczas korzystania z zarządzania magazynem wszystkie przeniesienia wewnątrz magazynu są kontrolowane przez pracę magazynu, a wszystkie przeniesienia między magazynami mogą być kontrolowane przez karty Kanban wypłat.

## <a name="supply-policies"></a>Zasady dostaw
Mieszany tryb planowania w programie Finance and Operations kontroluje sposób dostarczania produktów i, na podstawie podaży, określa, jak są wydawane zapotrzebowania pochodne (zużycie towarów z listą składową \[BOM\]). Na podstawie typu zamówienia system automatycznie pozyskuje materiałów według wymagań.  

Zasady dostawy można zdefiniować na poziomie produktu lub dowolnym poziomie szczegółowości, który zaspokaja konkretne wymagania. Poziom szczegółowości zasad dostaw określa się na stronie **Domyślne ustawienia zamówień**.  

Zasady dostaw mogą być kontrolowane przez produkt, wymiary towarów (konfiguracja, kolor i rozmiar), oddział i magazyn. Ustawienia wprowadza się na stronie **Zapotrzebowanie na towar**.  

Domyślny typ zamówienia określa, co jest generowane w planowaniu głównym.  

Niezależnie od tego, jak jest modelowany łańcuch dostaw, program Finance and Operations obsługuje kombinację zasad dostaw używanych w organizacji. Można mieść zlecenia produkcyjne pozyskiwane z kart Kanban. Można też mieć zamówienie partii, które wymaga produktu dostarczanego przez przeniesienia lub karty Kanban.  

Program Finance and Operations sprawdza, czy przepływ materiałów postępuje zgodnie z modelem.  

Magazyn pobrania materiału jest przydzielany dynamicznie w czasie wykonywania po zdefiniowaniu zasad dostaw.  

Zazwyczaj karty Kanban nie są tworzone dla przyszłych dat, ponieważ karty kanban mają krótki cykl życia. Aby zachować pełną widoczność łańcucha dostaw, wprowadziliśmy nowe pojęcie „planowanej karty Kanban”, która służy do obliczania zapotrzebowań pochodnych i pomaga zagwarantować, że wymagania są pozyskiwane według tej samej logiki, która jest używana do tworzenia rzeczywistej karty kanban.  

Ta sama logika obowiązuje dla wszystkich innych typów zasad dostaw. Dlatego długoterminowe planowanie opiera się na tej samej logice, która ma być stosowana w odniesieniu do rzeczywistych zamówień po zatwierdzeniu produkcji i dostaw.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Zasady alokacji materiałów w całym łańcuchu dostaw — zużycie zasobów na listach BOM
Zużycie zasobów jest ważną funkcją. Zużycie zasobów umożliwia dynamiczny wybór magazynu pobrania materiałów na podstawie zasad dostaw (typ zamówienia), a także ułatwia obsługę danych bazowych.  

Zużycie zasobów wymaga, aby magazyn, z którego materiały są pobierane, był przypisywany na podstawie sposobu dostarczania produktu. Innymi słowy w czasie wykonywania system znajduje zasoby, które powinny być używane do produkcji. W oparciu o te zasoby system znajduje magazyn pobrania.  

Dla pracy, która jest niezależna od zasad dostaw, nie trzeba zmieniać informacji na liście BOM w przypadku zmiany dostawy. W przypadku zmian „ad hoc” program Finance and Operations zapewnia, że materiały są pozyskiwane z odpowiedniego magazynu.

## <a name="process-manufacturing--the-production-type"></a>Produkcja procesowa — typ produkcji
Aby zapewnić pełną elastyczność w trybie mieszanym, zalecamy używanie produkcyjnych list BOM dla wszystkich produktów. Można następnie używać tych zleceń produkcyjnych, kart Kanban, zleceń przeniesienia lub zamówień zakupu do dostarczenia produktu. Dla produkcji procesowej należy użyć typu produkcji **Formuła**, **Produkt towarzyszący**, **produkt uboczny** lub **Element planowania**. Karty Kanban i zamówienia produkcyjne nie mogą być używane do tych typów produkcji.



