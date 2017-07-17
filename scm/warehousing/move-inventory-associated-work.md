---
title: "Przenoszenie zapasów za pomocą skojarzonej pracy w module Zarządzanie magazynem"
description: "W tym temacie opisano sposób konfigurowania i stosowania potwierdzenia pobrania sztuk z urządzenia przenośnego."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: d2db0431a3f749cbdaf35cc5108851f1e116bc96
ms.contentlocale: pl-pl
ms.lasthandoff: 06/20/2017


---

# Przenoszenie zapasów za pomocą skojarzonej pracy w module Zarządzanie magazynem
<a id="movement-of-inventory-with-associated-work-in-warehouse-management" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Za pomocą przesunięcia zapasów użytkownik może zdecydować, którzy pracownicy magazynu będą mogli przenosić zarezerwowane zapasy. Zapewnia to elastyczność w magazynach regulowanych, gdzie można zdecydować, aby nie zezwolić pracownikowi na wybieranie nowej lokalizacji pobrania dla już utworzonej pracy pobrania. Umożliwia to również kierownikowi magazynu kontrolowanie, jakie możliwości powinni mieć niektórzy mniej doświadczeni pracownicy.

Elastyczność zarządzania codziennymi operacjami pracowników magazynu może być przydatne w scenariuszach takich jak te:

## Scenariusz 1
<a id="scenario-1" class="xliff"></a>
Firma ma stosunkowo mały obszar przyjęcia i jest on zatłoczony paletami i pudełkami oczekującymi na odłożenie. Danego dnia jest oczekiwana duża przesyłka, więc pracownik przyjmujący decyduje się na wyczyszczenie obszaru przyjęcia poprzez przeniesienie niektórych palet do pomocniczego obszaru pośredniego rozładunku.

## Scenariusz 2
<a id="scenario-2" class="xliff"></a>
Doświadczony pracownik magazynu zauważył w magazynie możliwość skonsolidowania towarów w jednym miejscu zamiast je dzielić między 3 znajdujące się blisko siebie lokalizacje z małą ilością w każdej z nich. Pracownik chce skonsolidować ilości, przenosząc towary z każdej lokalizacji do tej samej lokalizacji i na ten sam numer identyfikacyjny.

## Scenariusz 3
<a id="scenario-3" class="xliff"></a>
Paleta oczekuje na wysyłkę w lokalizacji pośredniej, takiej jak STAGE01, która znajduje się w pobliżu bramy dokowej BAYDOOR01. Jednak z powodu zmiany planów ciężarówka ma podjechać do bramy dokowej BAYDOOR04. Pracownik ds. spedycji wie o tym i musi się upewnić, że ciężarówka nie będzie musiała czekać na załadunek z lokalizacji STAGE01. Dlatego pracownik decyduje się przenieść towary tej wysyłki z lokalizacji STAGE01 do lokalizacji STAGE04, która znajduje się bliżej nowego miejsca docelowego.

### Bieżące ograniczenia
<a id="current-limitations" class="xliff"></a>

Rezerwacje pracy, które można przenosić, są ograniczone do zamówienia sprzedaży, wydania zamówienia przeniesienia, przyjęcia zamówienia przeniesienia, zamówienia zakupu i pracy uzupełniania zapasów.

Przenoszenie towarów jest ograniczone w celu zapobieżenia dzieleniu wierszy pracy. Oznacza to, że jeśli masz wiersz pracy na 100 sztuk towaru A z lokalizacji Loc1, nie będzie można przenieść tylko 30 sztuk towaru A z tej lokalizacji do innej lokalizacji. To doprowadziłoby do podziału istniejącego wiersza pracy na 30 i 70 sztuk, ponieważ lokalizacje teraz są różne.

W scenariuszach z lokalizacjami pośrednimi, gdzie numer identyfikacyjny, z którego lub pod który są przesuwane towary, są ustawione jako docelowy numer identyfikacyjny dla zlecenia produkcyjnego, można przesuwać tylko całą zawartość numeru identyfikacyjnego, tak aby nie podzielić zawartości docelowego numeru identyfikacyjnego.
Obecnie są obsługiwane tylko przesunięcia ad hoc. Oznacza to, że nie będzie można przesuwać zarezerwowanych zapasów za pomocą przesunięć przy użyciu elementów menu szablonu na urządzeniu przenośnym.

### Ustawianie uprawnień do przesuwania zarezerwowanych zapasów dla poszczególnych pracowników
<a id="set-up-the-permission-to-move-reserved-inventory-for-individual-workers" class="xliff"></a>

Dla pracownika, który powinien mieć możliwość przesuwania zarezerwowanych zapasów, należy zaznaczyć pole wyboru **Zezwalaj na przesuwanie zapasów za pomocą skojarzonej pracy** w obszarze **Zarządzanie magazynem** > **ustawienia** > **Pracownik**.  

### Dodanie w starszych wersjach
<a id="backported" class="xliff"></a>

Ta funkcja została także dodana wstecznie do systemu Microsoft Dynamics AX 2012 R3 i będzie dostępna w ramach zbiorczej aktualizacji CU12.
Ponadto można ją pobrać oddzielnie jako pakiet KB 3192548. 

