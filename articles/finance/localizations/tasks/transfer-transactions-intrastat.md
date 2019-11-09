---
title: Przesyłanie transakcji do systemu Intrastat
description: Ta procedura pokazuje, jak skonfigurować parametry systemu Intrastat i przesłać do niego transakcje.
author: Anasyash
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 919c3cd755458f46a9f083415aa196c703fcf338
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183827"
---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="882cd-103">Przesyłanie transakcji do systemu Intrastat</span><span class="sxs-lookup"><span data-stu-id="882cd-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="882cd-104">Ta procedura pokazuje, jak skonfigurować parametry systemu Intrastat i przesłać do niego transakcje.</span><span class="sxs-lookup"><span data-stu-id="882cd-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="882cd-105">Procedurę utworzono przy użyciu danych firmy demonstracyjnej DEMF.</span><span class="sxs-lookup"><span data-stu-id="882cd-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="882cd-106">Tworzenie nowego i aktualizowanie istniejącego kodu asortymentu</span><span class="sxs-lookup"><span data-stu-id="882cd-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="882cd-107">W okienku nawigacji otwórz **Moduły > Zarządzanie informacjami o produktach > Ustawienia > Kategorie i atrybuty > Hierarchie kategorii**.</span><span class="sxs-lookup"><span data-stu-id="882cd-107">In the Navigation pane, go to **Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="882cd-108">Na liście znajdź lub zaznacz rekord **Kody asortymentu Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-108">In the list, find or select the record **Intrastat commodity codes.**</span></span>
3. <span data-ttu-id="882cd-109">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="882cd-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="882cd-110">W drzewie zaznacz rekord.</span><span class="sxs-lookup"><span data-stu-id="882cd-110">In the tree, select a record.</span></span> <span data-ttu-id="882cd-111">Na przykład wybierz **Intrastat\Głośnik**.</span><span class="sxs-lookup"><span data-stu-id="882cd-111">For example, select **Intrastat\Speaker**.</span></span>  
5. <span data-ttu-id="882cd-112">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-112">Click **Edit**.</span></span>
6. <span data-ttu-id="882cd-113">Rozwiń skróconą kartę **Handel zagraniczny**.</span><span class="sxs-lookup"><span data-stu-id="882cd-113">Expand the **Foreign trade** fastTab.</span></span>
7. <span data-ttu-id="882cd-114">W polu **Jednostki dodatkowe** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-114">In the **Additional units** field, enter or select a value.</span></span> <span data-ttu-id="882cd-115">Na przykład wybierz opcję **szt.**.</span><span class="sxs-lookup"><span data-stu-id="882cd-115">For example, choose **pcs**.</span></span>  
8. <span data-ttu-id="882cd-116">W polu **Waga nie ma zastosowania** zaznacz wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="882cd-116">Select **Yes** in the **Weight not applicable** field.</span></span>
9. <span data-ttu-id="882cd-117">W drzewie zaznacz element **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-117">In the tree, select **Intrastat**.</span></span>
10. <span data-ttu-id="882cd-118">Kliknij węzeł kategorii **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-118">Click **New category node**.</span></span>
11. <span data-ttu-id="882cd-119">W polu **Nazwa** wprowadź nazwę asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-119">In the **Name** field, enter the name of commodity.</span></span> <span data-ttu-id="882cd-120">Na przykład wpisz **Inny towar**.</span><span class="sxs-lookup"><span data-stu-id="882cd-120">For example, type **Other commodity**.</span></span>  
12. <span data-ttu-id="882cd-121">W polu **Kod** wprowadź kod asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-121">In the **Code** field, enter the commodity code.</span></span> <span data-ttu-id="882cd-122">Na przykład wpisz **995 00 00**.</span><span class="sxs-lookup"><span data-stu-id="882cd-122">For example, type **995 00 00**.</span></span>  
13. <span data-ttu-id="882cd-123">W polu Przyjazna nazwa wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-123">In the Friendly name field, type a value.</span></span> <span data-ttu-id="882cd-124">Na przykład wpisz **Inny**.</span><span class="sxs-lookup"><span data-stu-id="882cd-124">For example, type **Other**.</span></span>  
14. <span data-ttu-id="882cd-125">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="882cd-125">Click **Save**.</span></span>
15. <span data-ttu-id="882cd-126">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="882cd-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="882cd-127">Przypisywanie kodu asortymentu do hierarchii produktów i zwolnionego produktu</span><span class="sxs-lookup"><span data-stu-id="882cd-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="882cd-128">Skorzystaj z opcji szybkiego filtrowania, aby znaleźć rekordy.</span><span class="sxs-lookup"><span data-stu-id="882cd-128">Use the quick filter to find records.</span></span> <span data-ttu-id="882cd-129">Na przykład wyfiltruj według pola **Nazwa** z wartością **sprzedaż**.</span><span class="sxs-lookup"><span data-stu-id="882cd-129">For example, filter on the **Name** field with a value of **sales**.</span></span>
2. <span data-ttu-id="882cd-130">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="882cd-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="882cd-131">W drzewie rozwiń **węzeł kategorii**.</span><span class="sxs-lookup"><span data-stu-id="882cd-131">In the tree, expand **a category node**.</span></span> <span data-ttu-id="882cd-132">Na przykład rozwiń węzeł **Hierarchia sprzedaży\Domowy zestaw audio**.</span><span class="sxs-lookup"><span data-stu-id="882cd-132">For example, expand **Sales hierarchy\Home audio**.</span></span>  
4. <span data-ttu-id="882cd-133">W drzewie zaznacz **kategorię, którą chcesz przypisać do kodu asortymentu**.</span><span class="sxs-lookup"><span data-stu-id="882cd-133">In the tree, select **the category to assign to the commodity code**.</span></span> <span data-ttu-id="882cd-134">Na przykład zaznacz element \*\*Hierarchia sprzedaży\Domowy zestaw audio\Głośniki.</span><span class="sxs-lookup"><span data-stu-id="882cd-134">For example, select \*\*Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="882cd-135">Rozwiń skróconą kartę **Kody asortymentu**.</span><span class="sxs-lookup"><span data-stu-id="882cd-135">Expand the **Commodity codes** fastTab.</span></span>
6. <span data-ttu-id="882cd-136">Kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-136">Click **Add**.</span></span>
7. <span data-ttu-id="882cd-137">W polu **Wybierz hierarchię** zaznacz opcję **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-137">In the **Select hierarchy** field, select **Intrastat**.</span></span>
8. <span data-ttu-id="882cd-138">Na liście znajdź i zaznacz kod asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-138">In the list, find and select the commodity code.</span></span> <span data-ttu-id="882cd-139">Na przykład wybierz **920 20 34 Głośnik”**.</span><span class="sxs-lookup"><span data-stu-id="882cd-139">For example, select **920 20 34 Speaker**.</span></span>  
9. <span data-ttu-id="882cd-140">Kliknij strzałkę w prawo, aby wybrać kod.</span><span class="sxs-lookup"><span data-stu-id="882cd-140">Click the right arrow to select code.</span></span>
10. <span data-ttu-id="882cd-141">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-141">Click **OK**.</span></span>
11. <span data-ttu-id="882cd-142">W okienku nawigacji przejdź do opcji **Moduły > Zarządzanie informacjami o produktach > Produkty > Wydane produkty**.</span><span class="sxs-lookup"><span data-stu-id="882cd-142">In the Navigation pane, go to **Modules > Product information management > Products > Released products**.</span></span>
12. <span data-ttu-id="882cd-143">Z listy wybierz zwolniony produkt, który przypiszesz do kodu asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-143">In the list, choose the released product that you will assign to the commodity code.</span></span> <span data-ttu-id="882cd-144">Na przykład wybierz opcję **D0001**.</span><span class="sxs-lookup"><span data-stu-id="882cd-144">For example, choose **D0001**.</span></span>  
13. <span data-ttu-id="882cd-145">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-145">Click **Edit**.</span></span>
14. <span data-ttu-id="882cd-146">Rozwiń skróconą kartę **Handel zagraniczny**.</span><span class="sxs-lookup"><span data-stu-id="882cd-146">Expand the **Foreign trade** fastTab.</span></span>
15. <span data-ttu-id="882cd-147">W polu **Asortyment** wprowadź kod asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-147">In the **Commodity** field, enter the commodity code.</span></span> <span data-ttu-id="882cd-148">Na przykład wybierz wartość **920 20 34 Głośnik**.</span><span class="sxs-lookup"><span data-stu-id="882cd-148">For example, select value **920 20 34 Speaker**.</span></span>    
16. <span data-ttu-id="882cd-149">W polu **% opłat dodatkowych** wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="882cd-149">In the **Charges percentage** field, enter a number.</span></span> <span data-ttu-id="882cd-150">Na przykład wpisz **3**.</span><span class="sxs-lookup"><span data-stu-id="882cd-150">For example, enter **3**.</span></span>  
17. <span data-ttu-id="882cd-151">W polu **Kraj/region** wprowadź lub wybierz kraj albo region pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="882cd-151">In the **Country/region** field, enter or select a country or region of origin.</span></span> <span data-ttu-id="882cd-152">Na przykład zaznacz **AUT**.</span><span class="sxs-lookup"><span data-stu-id="882cd-152">For example, select **AUT**.</span></span>  
18. <span data-ttu-id="882cd-153">Rozwiń skróconą kartę **Zapasy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-153">Expand the **Manage inventory** fastTab.</span></span>
19. <span data-ttu-id="882cd-154">W polu **Waga netto** wpisz wagę w kg.</span><span class="sxs-lookup"><span data-stu-id="882cd-154">In the **Net weight** field, enter a weight in kg.</span></span> <span data-ttu-id="882cd-155">Na przykład wpisz **2.5**.</span><span class="sxs-lookup"><span data-stu-id="882cd-155">For example, enter **2.5**.</span></span>  
20. <span data-ttu-id="882cd-156">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="882cd-156">Click **Save**.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="882cd-157">Konfigurowanie kodów transakcji Intrastat i parametrów handlu zagranicznego</span><span class="sxs-lookup"><span data-stu-id="882cd-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="882cd-158">W okienku nawigacji otwórz **Moduły > Podatek > Ustawienia > Handel zagraniczny > Kody transakcji**.</span><span class="sxs-lookup"><span data-stu-id="882cd-158">In the Navigation pane, go to **Modules > Tax > Setup > Foreign trade > Transaction codes**.</span></span>
2. <span data-ttu-id="882cd-159">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-159">Click **New**.</span></span>
3. <span data-ttu-id="882cd-160">W polu **Kod transakcji** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-160">In the **Transaction code** field, type a value.</span></span> <span data-ttu-id="882cd-161">Na przykład wpisz **21** jako kod transakcji używanej do wykonania zwrotu.</span><span class="sxs-lookup"><span data-stu-id="882cd-161">For example, enter **21** for the transaction code used as return.</span></span>  
4. <span data-ttu-id="882cd-162">W polu **Nazwa** wpisz nazwę kodu transakcji.</span><span class="sxs-lookup"><span data-stu-id="882cd-162">In the **Name** field, type the name of transaction code.</span></span> <span data-ttu-id="882cd-163">Na przykład wpisz **Zwrot**.</span><span class="sxs-lookup"><span data-stu-id="882cd-163">For example, enter **Return**.</span></span>  
5. <span data-ttu-id="882cd-164">W polu **Kwota statystyczna** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="882cd-164">In the **Statistical amount** field, select an option.</span></span> <span data-ttu-id="882cd-165">Na przykład zaznacz opcję **Puste**, co wskaże, że wartości statystyczna, która ma być raportowana dla transakcji o kodzie transakcji **21**, zawsze będzie równa zero.</span><span class="sxs-lookup"><span data-stu-id="882cd-165">For example, select **Empty** which indicates that the Statistical value to be reported for transactions with Transaction code of **21** will always be zero.</span></span>  
6. <span data-ttu-id="882cd-166">W okienku nawigacji otwórz **Moduły > Podatek > Ustawienia > Handel zagraniczny > Parametry handlu zagranicznego**.</span><span class="sxs-lookup"><span data-stu-id="882cd-166">In the Navigation pane, go to **Modules > Tax > Setup > Foreign trade > Foreign trade parameters**.</span></span>
7. <span data-ttu-id="882cd-167">W polu **Kod transakcji** wpisz lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-167">In the **Transaction code** field, enter or select a value.</span></span> <span data-ttu-id="882cd-168">Na przykład zaznacz **11**.</span><span class="sxs-lookup"><span data-stu-id="882cd-168">For example, select **11**.</span></span>  
8. <span data-ttu-id="882cd-169">W polu **Faktura korygująca** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-169">In the **Credit note** field, enter or select a value.</span></span> <span data-ttu-id="882cd-170">Ta wartość określa również fizyczny zwrot.</span><span class="sxs-lookup"><span data-stu-id="882cd-170">This value also identifies the physical return.</span></span> <span data-ttu-id="882cd-171">Faktura korygująca na fizyczny zwrot zostanie przesłana do dziennika systemu Intrastat z zastosowaniem przeciwnego kierunku.</span><span class="sxs-lookup"><span data-stu-id="882cd-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="882cd-172">Na przykład zwrot przyjęcia jest przenoszony jako wysyłka.</span><span class="sxs-lookup"><span data-stu-id="882cd-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="882cd-173">Natomiast faktura korygująca jest traktowana jako korekta i przenoszona z zastosowaniem tego samego kierunku, ale przeciwnego znaku.</span><span class="sxs-lookup"><span data-stu-id="882cd-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="882cd-174">Na przykład korekta przyjęcia jest przenoszona jako przyjęcie z kwotą ujemną, a flaga aktywności jest ustawiana na **Korekta**.</span><span class="sxs-lookup"><span data-stu-id="882cd-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to **Correction**.</span></span>  
9. <span data-ttu-id="882cd-175">Rozwiń skróconą kartę **Przenoszenie**.</span><span class="sxs-lookup"><span data-stu-id="882cd-175">Expand the **Transfer** fastTab.</span></span>
10. <span data-ttu-id="882cd-176">W polu **Pozycje z kodem asortymentu** zaznacz opcję **Tak**.</span><span class="sxs-lookup"><span data-stu-id="882cd-176">Select **Yes** in the **Items with commodity code** field.</span></span> <span data-ttu-id="882cd-177">Wybierz tę opcję, aby przenieść tylko transakcje z przypisanym kodem asortymentu.</span><span class="sxs-lookup"><span data-stu-id="882cd-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="882cd-178">Transakcje bez kodu asortymentu nie będą przenoszone do systemu Intrastat.</span><span class="sxs-lookup"><span data-stu-id="882cd-178">Transactions without a commodity code won\*\*t be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="882cd-179">W polu **Przenieś, jeśli spełnione kryterium dla** wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="882cd-179">In the **Transfer when meeting criterion for** field, select an option.</span></span> <span data-ttu-id="882cd-180">Na przykład wybierz wartość **Jeden z wybranych**.</span><span class="sxs-lookup"><span data-stu-id="882cd-180">For example, select **One of the selected**.</span></span>  
12. <span data-ttu-id="882cd-181">Rozwiń sekcję **Hierarchia kodów asortymentu**.</span><span class="sxs-lookup"><span data-stu-id="882cd-181">Expand the **Commodity code hierarchy** section.</span></span>
13. <span data-ttu-id="882cd-182">Kliknij kartę **Właściwości kraju/regionu**.</span><span class="sxs-lookup"><span data-stu-id="882cd-182">Click the **Country/region properties** tab.</span></span>
14. <span data-ttu-id="882cd-183">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-183">Click **New**.</span></span>
15. <span data-ttu-id="882cd-184">W polu **Kraj/region** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-184">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="882cd-185">Na przykład wybierz wartość **FRA**.</span><span class="sxs-lookup"><span data-stu-id="882cd-185">For example, select the value **FRA**.</span></span>  
16. <span data-ttu-id="882cd-186">W polu **Kod Intrastat** wprowadź kod ISO kraju.</span><span class="sxs-lookup"><span data-stu-id="882cd-186">In the **Intrastat code** field, enter the ISO code for the country.</span></span>  <span data-ttu-id="882cd-187">Na przykład wpisz **FR**.</span><span class="sxs-lookup"><span data-stu-id="882cd-187">For example, type **FR**.</span></span>  
17. <span data-ttu-id="882cd-188">W polu **Typ kraju/regionu** wybierz opcję **UE**.</span><span class="sxs-lookup"><span data-stu-id="882cd-188">In the **Country/region type** field, select **EU**.</span></span>
18. <span data-ttu-id="882cd-189">Kliknij kartę Sekwencje numerów.</span><span class="sxs-lookup"><span data-stu-id="882cd-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="882cd-190">Konfigurowanie metod dostawy i reguł uwzględniania opłat w raportowaniu Intrastat</span><span class="sxs-lookup"><span data-stu-id="882cd-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="882cd-191">W okienku nawigacji otwórz **Moduły > Sprzedaż i Marketing > Ustawienia > Dystrybucja > Tryby dostawy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-191">In the Navigation pane, go to **Modules > Sales and marketing > Setup > Distribution > Modes of delivery**.</span></span>
2. <span data-ttu-id="882cd-192">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="882cd-192">In the list, find and select the desired record.</span></span> <span data-ttu-id="882cd-193">Na przykład wybierz wartość **20 Lotniczy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-193">For example, select **20 Air**.</span></span>  
3. <span data-ttu-id="882cd-194">Rozwiń skróconą kartę **Handel zagraniczny**.</span><span class="sxs-lookup"><span data-stu-id="882cd-194">Expand the **Foreign trade** fastTab.</span></span>
4. <span data-ttu-id="882cd-195">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-195">Click **Edit**.</span></span>
5. <span data-ttu-id="882cd-196">W polu **Transport** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-196">In the **Transport** field, enter or select a value.</span></span> <span data-ttu-id="882cd-197">Na przykład zaznacz **02**.</span><span class="sxs-lookup"><span data-stu-id="882cd-197">For example, select **02**.</span></span>  
6. <span data-ttu-id="882cd-198">W okienku nawigacji otwórz **Moduły > Rozrachunki z odbiorcami > Ustawienia opłat > Kod opłat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-198">In the Navigation pane, go to **Modules > Accounts receivable > Charges setup > Charges code**.</span></span>
7. <span data-ttu-id="882cd-199">Skorzystaj z opcji szybkiego filtrowania, aby znaleźć rekordy.</span><span class="sxs-lookup"><span data-stu-id="882cd-199">Use the quick filter to find records.</span></span> <span data-ttu-id="882cd-200">Na przykład wyfiltruj według pola Kod opłat z wartością **fracht**.</span><span class="sxs-lookup"><span data-stu-id="882cd-200">For example, filter on the Charges code field with a value of **freight**.</span></span>
8. <span data-ttu-id="882cd-201">Rozwiń skróconą kartę **Handel zagraniczny**.</span><span class="sxs-lookup"><span data-stu-id="882cd-201">Expand the **Foreign trade** fastTab.</span></span>
9. <span data-ttu-id="882cd-202">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-202">Click **Edit**.</span></span>
10. <span data-ttu-id="882cd-203">W polu **Wartość faktury dla Intrastat** zaznacz opcję **Tak**.</span><span class="sxs-lookup"><span data-stu-id="882cd-203">Select **Yes** in the **Intrastat invoice value** field.</span></span> <span data-ttu-id="882cd-204">Kwota zostanie przeniesiona do pola **Opłaty faktury** i zsumowana z kwotą przeniesioną do pola Kwota faktury.</span><span class="sxs-lookup"><span data-stu-id="882cd-204">The amount will be transferred to the **Invoice charges** field and will be summarized with the amount transferred in the Invoice amount field.</span></span> <span data-ttu-id="882cd-205">W polu **Wartość statystyczna Intrastat** wybierz opcję **Tak**, jeśli kwota opłat musi zostać przeniesiona do pola **Opłaty statystyczne** i zsumowana z wartością pola **Kwota statystyczna**.</span><span class="sxs-lookup"><span data-stu-id="882cd-205">Select **Yes** in the **Intrastat statistical value** field if the amount of changes need to be transferred to the **Statistical charges** field and summarized with **Statistical amount** field.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="882cd-206">Sprzedaż produktów do odbiorców w UE</span><span class="sxs-lookup"><span data-stu-id="882cd-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="882cd-207">W okienku nawigacji otwórz **Moduły > Rozrachunki z odbiorcami > Zamówienia > Wszystkie zamówienia zakupu**.</span><span class="sxs-lookup"><span data-stu-id="882cd-207">In the Navigation pane, go to **Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="882cd-208">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-208">Click **New**.</span></span>
3. <span data-ttu-id="882cd-209">W polu **Konto odbiorcy** zaznacz odbiorcę z UE.</span><span class="sxs-lookup"><span data-stu-id="882cd-209">In the **Customer account** field, select an EU customer.</span></span> <span data-ttu-id="882cd-210">Na przykład wybierz wartość **DE 012 Litware Retail**.</span><span class="sxs-lookup"><span data-stu-id="882cd-210">For example, select **DE-012 Litware Retail**.</span></span>  
4. <span data-ttu-id="882cd-211">Rozwiń skróconą kartę **Dostawa**.</span><span class="sxs-lookup"><span data-stu-id="882cd-211">Expand the **Delivery** fastTab.</span></span>
5. <span data-ttu-id="882cd-212">W polu **Metoda dostawy** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-212">In the **Mode of delivery** field, enter or select a value.</span></span> <span data-ttu-id="882cd-213">Na przykład wybierz wartość **20 Lotniczy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-213">For example, select **20 Air**.</span></span>  
6. <span data-ttu-id="882cd-214">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-214">Click **OK**.</span></span>
7. <span data-ttu-id="882cd-215">Wybierz pierwszy wiersz wierszy zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="882cd-215">Select the first row of sales order lines.</span></span>
8. <span data-ttu-id="882cd-216">W polu **Kod towaru** wpisz lub wprowadź wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-216">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="882cd-217">Na przykład zaznacz **D001**.</span><span class="sxs-lookup"><span data-stu-id="882cd-217">For example, select **D001**.</span></span>  
9. <span data-ttu-id="882cd-218">Rozwiń skróconą kartę **Szczegóły wiersza**.</span><span class="sxs-lookup"><span data-stu-id="882cd-218">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="882cd-219">Kliknij kartę **Handel zagraniczny**. Pole transportu jest wypełniane automatycznie na podstawie wybranej metody dostawy.</span><span class="sxs-lookup"><span data-stu-id="882cd-219">Click the **Foreign trade** tab. The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="882cd-220">W polu **Port** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-220">In the **Port** field, enter or select a value.</span></span>
12. <span data-ttu-id="882cd-221">Kliknij opcję **Finanse**.</span><span class="sxs-lookup"><span data-stu-id="882cd-221">Click **Financials**.</span></span> <span data-ttu-id="882cd-222">Zgodnie z ustawieniami ta kwota będzie dodana do pola **Wartość faktury dla Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-222">As per the settings, this amount will be included in **Intrastat invoice value**.</span></span>  
13. <span data-ttu-id="882cd-223">Kliknij opcję **Obsługuj opłaty**.</span><span class="sxs-lookup"><span data-stu-id="882cd-223">Click **Maintain charges**.</span></span>
14. <span data-ttu-id="882cd-224">W polu **Kod opłat** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-224">In the **Charges code** field, enter or select a value.</span></span> <span data-ttu-id="882cd-225">Na przykład wybierz wartość **FRACHT**.</span><span class="sxs-lookup"><span data-stu-id="882cd-225">For example, select **FREIGHT**.</span></span>  
15. <span data-ttu-id="882cd-226">Zaznacz pole wyboru **Zachowaj**.</span><span class="sxs-lookup"><span data-stu-id="882cd-226">Select the **Keep** check box.</span></span>
16. <span data-ttu-id="882cd-227">W polu **Wartość opłat** wprowadź liczbę.</span><span class="sxs-lookup"><span data-stu-id="882cd-227">In the **Charges value** field, enter a number.</span></span> <span data-ttu-id="882cd-228">Na przykład wpisz **10**.</span><span class="sxs-lookup"><span data-stu-id="882cd-228">For example, enter **10**.</span></span>  
17. <span data-ttu-id="882cd-229">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="882cd-229">Click **Save**.</span></span>
18. <span data-ttu-id="882cd-230">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="882cd-230">Close the page.</span></span>
19. <span data-ttu-id="882cd-231">W okienku akcji kliknij pozycję **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="882cd-231">On the Action Pane, click **Invoice**.</span></span>
20. <span data-ttu-id="882cd-232">Kliknij opcję **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="882cd-232">Click **Invoice**.</span></span>
21. <span data-ttu-id="882cd-233">Rozwiń sekcję **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="882cd-233">Expand the **Parameters** section.</span></span>
22. <span data-ttu-id="882cd-234">W polu **Ilość** zaznacz opcję **Wszystko**.</span><span class="sxs-lookup"><span data-stu-id="882cd-234">In the **Quantity** field, select **All**.</span></span>
23. <span data-ttu-id="882cd-235">Rozwiń skróconą kartę **Konfiguracja**.</span><span class="sxs-lookup"><span data-stu-id="882cd-235">Expand the **Setup** fastTab.</span></span>
24. <span data-ttu-id="882cd-236">W polu **Data faktury** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="882cd-236">In the **Invoice date** field, enter a date.</span></span> <span data-ttu-id="882cd-237">Na przykład wpisz **2015-01-31**.</span><span class="sxs-lookup"><span data-stu-id="882cd-237">For example, enter **2015-01-31**.</span></span>  
25. <span data-ttu-id="882cd-238">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-238">Click **OK**.</span></span>
26. <span data-ttu-id="882cd-239">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-239">Click **OK**.</span></span>
27. <span data-ttu-id="882cd-240">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="882cd-240">Close the page.</span></span>
28. <span data-ttu-id="882cd-241">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="882cd-241">Click **New**.</span></span>
29. <span data-ttu-id="882cd-242">W polu **Konto odbiorcy** zaznacz odbiorcę z UE.</span><span class="sxs-lookup"><span data-stu-id="882cd-242">In the **Customer account** field, select an EU customer.</span></span> <span data-ttu-id="882cd-243">Na przykład wybierz wartość **DE-013 Trey Wholesales**.</span><span class="sxs-lookup"><span data-stu-id="882cd-243">For example, select **DE-013 Trey Wholesales**.</span></span>
30. <span data-ttu-id="882cd-244">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-244">Click **OK**.</span></span>
31. <span data-ttu-id="882cd-245">W polu **Kod towaru** wpisz lub wprowadź wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-245">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="882cd-246">Na przykład zaznacz **D0001**.</span><span class="sxs-lookup"><span data-stu-id="882cd-246">For example, select **D0001**.</span></span>  
32. <span data-ttu-id="882cd-247">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="882cd-247">Click **Save**.</span></span>
33. <span data-ttu-id="882cd-248">Kliknij opcję **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="882cd-248">Click **Invoice**.</span></span>
34. <span data-ttu-id="882cd-249">W polu **Data faktury** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="882cd-249">In the **Invoice date** field, enter a date.</span></span> <span data-ttu-id="882cd-250">Na przykład wpisz datę **2015-01-31**.</span><span class="sxs-lookup"><span data-stu-id="882cd-250">For example, enter the date **2015-01-31**.</span></span>  
35. <span data-ttu-id="882cd-251">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-251">Click **OK**.</span></span>
36. <span data-ttu-id="882cd-252">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-252">Click **OK**.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="882cd-253">Przesyłanie transakcji do systemu Intrastat</span><span class="sxs-lookup"><span data-stu-id="882cd-253">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="882cd-254">W okienku nawigacji otwórz **Moduły > Podatek > Deklaracje > Handel zagraniczny > Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="882cd-254">In the Navigation pane, go to **Modules > Tax > Declarations > Foreign trade > Intrastat**.</span></span>
2. <span data-ttu-id="882cd-255">Kliknij przycisk **Przeniesienie**.</span><span class="sxs-lookup"><span data-stu-id="882cd-255">Click **Transfer**.</span></span>
3. <span data-ttu-id="882cd-256">W polu **Faktura dla odbiorcy** zaznacz opcję **Tak**.</span><span class="sxs-lookup"><span data-stu-id="882cd-256">Select **Yes** in the **Customer invoice** field.</span></span>
4. <span data-ttu-id="882cd-257">Kliknij przycisk **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="882cd-257">Click **Filter**.</span></span>
5. <span data-ttu-id="882cd-258">Na liście zaznacz wiersz z **datą**.</span><span class="sxs-lookup"><span data-stu-id="882cd-258">In the list, mark the row with **Date**.</span></span>
6. <span data-ttu-id="882cd-259">W polu **Kryteria** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="882cd-259">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="882cd-260">Na przykład wprowadzić filtru na okres stycznia 2015 r. (dokładna wartość zależy od formatu daty): 1.1.2015..31.1.2015</span><span class="sxs-lookup"><span data-stu-id="882cd-260">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="882cd-261">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-261">Click **OK**.</span></span>
8. <span data-ttu-id="882cd-262">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="882cd-262">Click **OK**.</span></span>
9. <span data-ttu-id="882cd-263">Na liście znajdź i zaznacz przeniesiony rekord.</span><span class="sxs-lookup"><span data-stu-id="882cd-263">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="882cd-264">Kliknij kartę **Ogólne**.</span><span class="sxs-lookup"><span data-stu-id="882cd-264">Click the **General** tab.</span></span>
    
<span data-ttu-id="882cd-265">Przejrzyj przeniesione dane, w tym kraj/region miejsca docelowego/wysyłki, kraj pochodzenia, wagę, ilość, ilość w jednostkach dodatkowych, oznaczenie asortymentu, kod transakcji, kwoty na fakturach i kwoty statystyczne.</span><span class="sxs-lookup"><span data-stu-id="882cd-265">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span> <span data-ttu-id="882cd-266">W razie potrzeby można zmodyfikować te dane.</span><span class="sxs-lookup"><span data-stu-id="882cd-266">You can modify data if necessary.</span></span>  
