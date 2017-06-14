---
title: "Rezerwowanie takiej samej partii na potrzeby zamówienia sprzedaży"
description: "Ten artykuł przedstawia sposób konfigurowania produktu w celu umożliwienia rezerwacji zapasów z jednej partii zapasów."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1b63173d1efe45bf048b9c2eed4dc6250c9ee9f1
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Rezerwowanie takiej samej partii na potrzeby zamówienia sprzedaży

[!include[banner](../includes/banner.md)]


Ten artykuł przedstawia sposób konfigurowania produktu w celu umożliwienia rezerwacji zapasów z jednej partii zapasów.

Rezerwacja tej samej partii umożliwia rezerwowanie zapasu dla wiersza zamówienia sprzedaży z jednej partii zapasów. Na przykład klient zamawiający tapety może zażądać, by całe zamówienie zawierało towar z jednej partii, aby uniknąć różnic między rolkami. Aby skonfigurować produktu do użycia rezerwacji tej samej partii, w grupie modeli towaru, grupie wymiarów śledzenia i grupie wymiarów magazynowania muszą być aktywne następujące ustawienia przypisane do produktu:

-   **Grupy modeli towarów** — grupa musi mieć zaznaczone pola **Wybór tej samej partii** i **Konsoliduj zapotrzebowanie** w grupie pól **rezerwacji** dla zasad zapasów.
-   **Grupy wymiarów śledzenia** — grupa mieć zaznaczone pole **plan zapotrzebowania wg wymiaru** dla numeru partii.
-   **Grupy wymiarów magazynowania** — grupa musi mieć zaznaczone pole **plan zapotrzebowania wg wymiaru** dla opcji **Oddział** i **Magazyn**.

Podczas rezerwowania zapasów produktu w wierszu zamówienia sprzedaży, dla którego zdefiniowano dla wybór tej samej partii, program Microsoft Dynamics 365 for Operations próbuje zarezerwować zamówioną ilość z jednej partii zapasów. Uwzględnione są również wszelkie specyficzne wymagania atrybutów partii. Jeśli w pojedynczej partii nie ma wystarczającej ilości towaru, zostanie wyświetlona strona **Konflikt rezerwacji tej samej partii**. Na tej stronie opisano problemy, a także akcje, które należy wykonać, aby kontynuować wykonywanie rezerwacji. Następujące warunki mogą uniemożliwić zarezerwowane partii:

-   Dla kodu dyspozycji partii jest zaznaczona opcja **Blokuj rezerwację** dla sprzedaży oznaczonych jako **zablokowano**.
-   Partia wygasła, na podstawie daty ważności oraz jakiekolwiek dni możliwej sprzedaży. Element nadal można uznać za do rezerwacji, jeśli grupa modeli pozycji dla towaru jest ewidencjonowana według zasady FEFO, a okres przydatności jest kryterium pobrania.
-   Partia nie ma wystarczającej liczby pozostałych dni przydatności (według daty ważności, daty przydatności i liczby dni możliwej sprzedaży u odbiorcy).




