---
title: Badanie/rozwiązywanie wyjątków
description: Zasady dotyczące faktur od dostawców są uruchamiane podczas księgowania faktur od dostawców przy użyciu strony Faktura od dostawcy oraz po otwarciu strony naruszeń zasad faktur od dostawców.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189345"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="6a812-103">Badanie/rozwiązywanie wyjątków</span><span class="sxs-lookup"><span data-stu-id="6a812-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a812-104">Zasady dotyczące faktur od dostawców są uruchamiane podczas księgowania faktur od dostawców przy użyciu strony Faktura od dostawcy oraz po otwarciu strony naruszeń zasad faktur od dostawców.</span><span class="sxs-lookup"><span data-stu-id="6a812-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="6a812-105">Można także skonfigurować przepływ pracy faktur od dostawcy, aby uruchamiał zasady dotyczące faktur od dostawców podczas każdego przesłania faktur do przepływu.</span><span class="sxs-lookup"><span data-stu-id="6a812-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="6a812-106">Zasady faktur od dostawców nie dotyczą faktur, które zostały utworzone w rejestrze faktur lub arkuszu faktur.</span><span class="sxs-lookup"><span data-stu-id="6a812-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="6a812-107">Funkcja sprawdzania poprawności uzgadniania faktur nie używa zasad dotyczących faktur od dostawców, ale jest konfigurowana na stronie Parametry modułu rozrachunków z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="6a812-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="6a812-108">To nagranie wykorzystuje firmę demonstracyjną USMF.</span><span class="sxs-lookup"><span data-stu-id="6a812-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="6a812-109">Czynności te wykonuje menedżer ds. rozrachunków z dostawcami lub menedżer księgowości.</span><span class="sxs-lookup"><span data-stu-id="6a812-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="6a812-110">Zanim rozpoczniesz, upewnij się, że wybrano klucz konfiguracji Uzgadnianie faktur.</span><span class="sxs-lookup"><span data-stu-id="6a812-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="6a812-111">Przygotowanie do tworzenia zasad dotyczących faktur od dostawców</span><span class="sxs-lookup"><span data-stu-id="6a812-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="6a812-112">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia > Parametry modułu rozrachunków z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="6a812-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="6a812-113">Kliknij kartę Weryfikacja faktury.</span><span class="sxs-lookup"><span data-stu-id="6a812-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="6a812-114">Zaznacz lub wyczyść pole wyboru Automatycznie aktualizuj stan nagłówka faktury.</span><span class="sxs-lookup"><span data-stu-id="6a812-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="6a812-115">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="6a812-115">Click OK.</span></span>
5. <span data-ttu-id="6a812-116">W polu Księguj fakturę z rozbieżnościami zaznacz opcję.</span><span class="sxs-lookup"><span data-stu-id="6a812-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="6a812-117">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-117">Close the page.</span></span>
7. <span data-ttu-id="6a812-118">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia zasad > Zasady dotyczące faktur od dostawców.</span><span class="sxs-lookup"><span data-stu-id="6a812-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="6a812-119">Kliknij opcję Parametry.</span><span class="sxs-lookup"><span data-stu-id="6a812-119">Click Parameters.</span></span>
9. <span data-ttu-id="6a812-120">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="6a812-120">Click btnAdd.</span></span>
10. <span data-ttu-id="6a812-121">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="6a812-122">Tworzenie typów reguł dla faktur od dostawców</span><span class="sxs-lookup"><span data-stu-id="6a812-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="6a812-123">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia zasad > Typy reguł faktur od dostawców.</span><span class="sxs-lookup"><span data-stu-id="6a812-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="6a812-124">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="6a812-124">Click New.</span></span>
3. <span data-ttu-id="6a812-125">W polu Nazwa reguły wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="6a812-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="6a812-126">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="6a812-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6a812-127">W polu Nazwa kwerendy kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="6a812-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6a812-128">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="6a812-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6a812-129">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="6a812-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6a812-130">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="6a812-130">Click Save.</span></span>
9. <span data-ttu-id="6a812-131">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="6a812-132">Definiowanie zasad dotyczących faktur od dostawców</span><span class="sxs-lookup"><span data-stu-id="6a812-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="6a812-133">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia zasad > Zasady dotyczące faktur od dostawców.</span><span class="sxs-lookup"><span data-stu-id="6a812-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="6a812-134">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="6a812-134">Click New.</span></span>
3. <span data-ttu-id="6a812-135">W polu Nazwa wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="6a812-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6a812-136">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="6a812-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6a812-137">Rozwiń lub zwiń sekcję Organizacje zasad.</span><span class="sxs-lookup"><span data-stu-id="6a812-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="6a812-138">W drzewie zaznacz pozycję „Contoso Entertainment System USA”.</span><span class="sxs-lookup"><span data-stu-id="6a812-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="6a812-139">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="6a812-139">Click Add.</span></span>
8. <span data-ttu-id="6a812-140">Rozwiń lub zwiń sekcję Reguły zasad.</span><span class="sxs-lookup"><span data-stu-id="6a812-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="6a812-141">Kliknij przycisk Utwórz regułę.</span><span class="sxs-lookup"><span data-stu-id="6a812-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="6a812-142">W polu Opis reguły wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="6a812-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="6a812-143">Kliknij przycisk Filtr.</span><span class="sxs-lookup"><span data-stu-id="6a812-143">Click Filter.</span></span>
12. <span data-ttu-id="6a812-144">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="6a812-144">Click Add.</span></span>
13. <span data-ttu-id="6a812-145">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="6a812-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="6a812-146">W polu Tabela kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="6a812-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="6a812-147">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="6a812-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6a812-148">W polu Tabela pochodna kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="6a812-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="6a812-149">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="6a812-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="6a812-150">W polu Pole kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="6a812-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="6a812-151">W polu Pole wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="6a812-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="6a812-152">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-152">Close the page.</span></span>
21. <span data-ttu-id="6a812-153">W polu Kryteria wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="6a812-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="6a812-154">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="6a812-154">Click OK.</span></span>
23. <span data-ttu-id="6a812-155">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="6a812-155">Click OK.</span></span>
24. <span data-ttu-id="6a812-156">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-156">Close the page.</span></span>
25. <span data-ttu-id="6a812-157">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="6a812-157">Close the page.</span></span>
