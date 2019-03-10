---
title: Definiowanie procesu częściowej inwentaryzacji ciągłej w lokalizacji
description: Używając planów inwentaryzacji ciągłej do tworzenia pracy inwentaryzacji, można kierować faktycznymi operacjami zliczania poprzez ustawienie żądania, aby były zliczane tylko konkretne produkty i warianty produktów, a nie wszystkie zapasy dostępne w lokalizacji.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2019
ms.locfileid: "373416"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="fa880-103">Definiowanie procesu częściowej inwentaryzacji ciągłej w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="fa880-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa880-104">Używając planów inwentaryzacji ciągłej do tworzenia pracy inwentaryzacji, można kierować faktycznymi operacjami zliczania poprzez ustawienie żądania, aby były zliczane tylko konkretne produkty i warianty produktów, a nie wszystkie zapasy dostępne w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fa880-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="fa880-105">Wyfiltrowując określone produkty, kierownik magazynu może zmniejszyć pracochłonność przeglądu, zapobiec błędom konsolidacji i zaoszczędzić czas.</span><span class="sxs-lookup"><span data-stu-id="fa880-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="fa880-106">Zazwyczaj zadania konfiguracyjne wykonuje kierownik magazynu.</span><span class="sxs-lookup"><span data-stu-id="fa880-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="fa880-107">Można przejść tę procedurę przy użyciu danych firmy demonstracyjnej USMF lub własnych danych.</span><span class="sxs-lookup"><span data-stu-id="fa880-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="fa880-108">Tworzenie szablonu pracy inwentaryzacji ciągłej</span><span class="sxs-lookup"><span data-stu-id="fa880-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="fa880-109">Wybierz kolejno opcje Zarządzanie magazynem > Ustawienia > Praca > Szablony pracy.</span><span class="sxs-lookup"><span data-stu-id="fa880-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="fa880-110">W polu Typ zlecenia wybierz opcję „Inwentaryzacja ciągła”.</span><span class="sxs-lookup"><span data-stu-id="fa880-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="fa880-111">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa880-111">Click New.</span></span>
4. <span data-ttu-id="fa880-112">W polu Numer sekwencyjny wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa880-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fa880-113">Sortowanie odbywa się w porządku od najmniejszej liczby do największej liczby.</span><span class="sxs-lookup"><span data-stu-id="fa880-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fa880-114">Wartość musi być większa od 0 (zera).</span><span class="sxs-lookup"><span data-stu-id="fa880-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="fa880-115">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="fa880-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="fa880-116">W polu Szablon pracy wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="fa880-117">W polu Opis szablonu pracy wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="fa880-118">W polu Identyfikator puli pracy wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="fa880-119">W polu Priorytet pracy wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa880-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="fa880-120">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="fa880-120">Click Save.</span></span>
11. <span data-ttu-id="fa880-121">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa880-121">Click New.</span></span>
12. <span data-ttu-id="fa880-122">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="fa880-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fa880-123">W polu Typ pracy zaznacz opcję „Inwentaryzacja”.</span><span class="sxs-lookup"><span data-stu-id="fa880-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="fa880-124">W polu Identyfikator klasy roboczej wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="fa880-125">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="fa880-125">Click Save.</span></span>
16. <span data-ttu-id="fa880-126">Kliknij opcję Podziały wierszy pracy.</span><span class="sxs-lookup"><span data-stu-id="fa880-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="fa880-127">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa880-127">Click New.</span></span>
18. <span data-ttu-id="fa880-128">W polu Numer sekwencyjny wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa880-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fa880-129">Sortowanie odbywa się w porządku od najmniejszej liczby do największej liczby.</span><span class="sxs-lookup"><span data-stu-id="fa880-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fa880-130">Wartość musi być większa od 0 (zera).</span><span class="sxs-lookup"><span data-stu-id="fa880-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="fa880-131">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="fa880-131">Click Save.</span></span>
20. <span data-ttu-id="fa880-132">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="fa880-132">Close the page.</span></span>
21. <span data-ttu-id="fa880-133">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="fa880-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="fa880-134">Tworzenie planu inwentaryzacji ciągłej</span><span class="sxs-lookup"><span data-stu-id="fa880-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="fa880-135">Wybierz kolejno opcje Zarządzanie magazynem > Ustawienia > Inwentaryzacja ciągła > Plany inwentaryzacji ciągłej.</span><span class="sxs-lookup"><span data-stu-id="fa880-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="fa880-136">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa880-136">Click New.</span></span>
3. <span data-ttu-id="fa880-137">W polu Identyfikator planu inwentaryzacji ciągłej wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="fa880-138">W polu Opis wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa880-139">W polu Maksymalna liczba inwentaryzacji ciągłych wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa880-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="fa880-140">W polu Szablon pracy wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="fa880-141">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa880-141">Click New.</span></span>
8. <span data-ttu-id="fa880-142">W polu Numer sekwencyjny wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa880-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fa880-143">Sortowanie odbywa się w porządku od najmniejszej liczby do największej liczby.</span><span class="sxs-lookup"><span data-stu-id="fa880-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fa880-144">Wartość musi być większa od 0 (zera).</span><span class="sxs-lookup"><span data-stu-id="fa880-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="fa880-145">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="fa880-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="fa880-146">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="fa880-146">Click Save.</span></span>
11. <span data-ttu-id="fa880-147">Kliknij opcję Definiuj zapytanie produktu.</span><span class="sxs-lookup"><span data-stu-id="fa880-147">Click Define product query.</span></span>
12. <span data-ttu-id="fa880-148">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="fa880-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fa880-149">W polu Kryteria wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa880-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="fa880-150">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="fa880-150">Click OK.</span></span>
15. <span data-ttu-id="fa880-151">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="fa880-151">Close the page.</span></span>
