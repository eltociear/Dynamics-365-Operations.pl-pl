---
title: "Przygotowanie do zarządzania kosztami standardowymi wyprodukowanych towarów"
description: "W tym temacie opisano etapy przygotowywania się do zarządzania kosztami wytwarzanych towarów."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 605f4c6391e9c40b1b80fab93d61b88553369069
ms.openlocfilehash: 6f52d2d90d655d1ab465e1808ca55ef3d5ea9e56
ms.contentlocale: pl-pl
ms.lasthandoff: 01/19/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="15310-103">Przygotowanie do zarządzania kosztami standardowymi wyprodukowanych towarów</span><span class="sxs-lookup"><span data-stu-id="15310-103">Prepare to maintain standard costs for manufactured items</span></span>

<span data-ttu-id="15310-104">W tym temacie opisano etapy przygotowywania się do zarządzania kosztami wytwarzanych towarów.</span><span class="sxs-lookup"><span data-stu-id="15310-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="15310-105">Kroki dla towarów wytwarzanych różnią się nieco od kroków dla towarów zakupionych.</span><span class="sxs-lookup"><span data-stu-id="15310-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="15310-106">Zasady przypisane do towarów wytwarzanych mogą wpływać na obliczanie kosztów nadrzędnych towarów wytwarzanych.</span><span class="sxs-lookup"><span data-stu-id="15310-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="15310-107">Aby się przygotować do zarządzania kosztami towarów wytwarzanych, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="15310-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="15310-108">Przypisz grupa modeli pozycji do wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="15310-109">Grupa modeli pozycji wskazuje, że będą używane koszty standardowe.</span><span class="sxs-lookup"><span data-stu-id="15310-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="15310-110">Przypisz grupę towarów do wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="15310-111">Grupa towarów zawiera konta księgowe dotyczące wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="15310-112">Konta księgowe wytwarzanego towaru używającego modelu zapasów opartego na kosztach standardowych obsługują różne odchylenia produkcji, odchylenia zmian kosztów i przeszacowania kosztów zapasów.</span><span class="sxs-lookup"><span data-stu-id="15310-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="15310-113">Przypisz magazynową jednostkę miary do towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="15310-114">Koszty towaru są zawsze wyrażane w jednostkach miary zapasów.</span><span class="sxs-lookup"><span data-stu-id="15310-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="15310-115">Nie przypisuj grupy kosztów do wytwarzanego towaru, dopóki towar nie jest traktowany jako zakupiony towar.</span><span class="sxs-lookup"><span data-stu-id="15310-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="15310-116">Przypisz grupę obliczeń listy składowej (BOM) do wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="15310-117">Grupa obliczeń BOM towaru określa warunki ostrzeżeń, które mają zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="15310-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="15310-118">W ten sposób po zakończeniu obliczania BOM mogą być generowane komunikaty ostrzegawcze o możliwych źródłach błędów w obliczeniach.</span><span class="sxs-lookup"><span data-stu-id="15310-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="15310-119">Na przykład komunikat ostrzegawczy może wystąpić, gdy aktywna lista BOM lub marszruta nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="15310-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="15310-120">Grupa obliczeń BOM zawiera zasadę zatrzymania rozłożenia, która określa, kiedy wytworzony towar powinien być traktowany jako zakupiony.</span><span class="sxs-lookup"><span data-stu-id="15310-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="15310-121">Jeśli wytworzony towar ma koszty stałe, przypisz mu standardową ilość zamówienia.</span><span class="sxs-lookup"><span data-stu-id="15310-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="15310-122">Standardowa ilość zamówienia to księgowa wielkość partii na potrzeby amortyzacji kosztów stałych.</span><span class="sxs-lookup"><span data-stu-id="15310-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="15310-123">Przykłady kosztów stałych to m.in. czasy przezbrajania w operacjach marszruty czy stała ilość składnika na liście BOM.</span><span class="sxs-lookup"><span data-stu-id="15310-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="15310-124">Określ BOM dla wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="15310-125">Można zdefiniować jedną lub więcej wersji BOM.</span><span class="sxs-lookup"><span data-stu-id="15310-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="15310-126">Sprawdź, czy wersje zostały oznaczone jako zatwierdzone i aktywne oraz mają przydzielone odpowiednie daty obowiązywania.</span><span class="sxs-lookup"><span data-stu-id="15310-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="15310-127">Wersja BOM może obowiązywać w całej firmie lub w wybranym oddziale.</span><span class="sxs-lookup"><span data-stu-id="15310-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="15310-128">Określ marszrutę dla wytwarzanego towaru.</span><span class="sxs-lookup"><span data-stu-id="15310-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="15310-129">Można zdefiniować jedną lub więcej wersji marszruty.</span><span class="sxs-lookup"><span data-stu-id="15310-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="15310-130">Sprawdź, czy wersje zostały oznaczone jako zatwierdzone i aktywne oraz mają przydzielone odpowiednie daty obowiązywania.</span><span class="sxs-lookup"><span data-stu-id="15310-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="15310-131">Wersja marszruty musi obowiązywać w wybranym oddziale.</span><span class="sxs-lookup"><span data-stu-id="15310-131">The route version must be site-specific.</span></span>

<span data-ttu-id="15310-132">Jeśli chcesz używać informacji o marszrucie do wyceny, potrzebne są dodatkowe czynności przygotowawcze.</span><span class="sxs-lookup"><span data-stu-id="15310-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="15310-133">Na przykład kategorie kosztów przypisane do operacji marszrut muszą być prawidłowe i kompletne.</span><span class="sxs-lookup"><span data-stu-id="15310-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="15310-134">Powiązane tematy</span><span class="sxs-lookup"><span data-stu-id="15310-134">Related topics</span></span>
--------

[<span data-ttu-id="15310-135">Amortyzowanie kosztów stałych wytworzonego towaru</span><span class="sxs-lookup"><span data-stu-id="15310-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="15310-136">Konfigurowanie produktów, które mogą być produkowane lub zamawiane</span><span class="sxs-lookup"><span data-stu-id="15310-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

