---
title: Pakiet zawartości usługi Power BI Analiza wydatków zakupowych
description: W tym temacie opisano, co się znajduje w pakiecie zawartości usługi Power BI Analiza wydatków zakupowych. Wyjaśniono, jak uzyskać dostęp do raportów oferowanych w pakiecie, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d25bacc2ec1f8e13376b96e188b099a184f7f8c6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569139"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="03cb9-104">Pakiet zawartości usługi Power BI Analiza wydatków zakupowych</span><span class="sxs-lookup"><span data-stu-id="03cb9-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03cb9-105">W tym temacie opisano, co się znajduje w pakiecie zawartości usługi Microsoft Power BI **Analiza wydatków zakupowych**.</span><span class="sxs-lookup"><span data-stu-id="03cb9-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="03cb9-106">Wyjaśniono, jak uzyskać dostęp do raportów programu Power BI, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.</span><span class="sxs-lookup"><span data-stu-id="03cb9-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="03cb9-107">Przegląd</span><span class="sxs-lookup"><span data-stu-id="03cb9-107">Overview</span></span>

<span data-ttu-id="03cb9-108">Pakiet zawartości usługi Power BI **Analiza wydatków zakupowych** został zaprojektowany, aby pomóc kierownikom ds. zakupów i menedżerom odpowiedzialnym za budżety monitorować wydatki zakupowe.</span><span class="sxs-lookup"><span data-stu-id="03cb9-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="03cb9-109">Menedżerowie mogą analizować wydatki zakupowe w następujące sposoby:</span><span class="sxs-lookup"><span data-stu-id="03cb9-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="03cb9-110">Zakupy od początku roku (według grupy dostawców i indywidualnych dostawców, kategorii zaopatrzenia, poszczególnych produktów i lokalizacji dostawców)</span><span class="sxs-lookup"><span data-stu-id="03cb9-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="03cb9-111">Zmiany wydatków zakupowych rok do roku (według grup dostawców i kategorii zaopatrzenia)</span><span class="sxs-lookup"><span data-stu-id="03cb9-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="03cb9-112">Pakiet zawartości wykorzystuje dane transakcyjne zakupów i przedstawia zarówno zagregowany widok danych zakupowych w całej firmie, jak i podział wydatków zakupowych na dostawców i produkty.</span><span class="sxs-lookup"><span data-stu-id="03cb9-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="03cb9-113">Raporty eksponują zmiany wydatków zakupowych w horyzoncie czasowym.</span><span class="sxs-lookup"><span data-stu-id="03cb9-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="03cb9-114">W związku z tym raporty mogą służyć do ostrzegania menedżerów o pozytywnych i negatywnych trendach wydatków dla poszczególnych dostawców i produktów.</span><span class="sxs-lookup"><span data-stu-id="03cb9-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="03cb9-115">Dodatkowo wykresy pokazują wydatki zakupowe dla różnych kategorii zaopatrzenia i grup dostawców.</span><span class="sxs-lookup"><span data-stu-id="03cb9-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="03cb9-116">W związku z tym menedżerowie kategorii i kierownicy regionalni mogą używać tych wykresów do identyfikowania zmian w zachowaniach wydatkowych.</span><span class="sxs-lookup"><span data-stu-id="03cb9-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="03cb9-117">Przechodzenie do pakietu zawartości usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="03cb9-117">Accessing the Power BI content</span></span>
<span data-ttu-id="03cb9-118">Pakiet zawartości usługi Power BI **Analiza wydatków związanych z zakupami** jest wyświetlany na stronie **Analiza wydatków i zakupów** (**Zaopatrzenie i sourcing** \> **Zapytania i raporty** \> **Analiza wydajności zakupów** \> **Analiza wydatków i zakupów**).</span><span class="sxs-lookup"><span data-stu-id="03cb9-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="03cb9-119">Wskaźniki umieszczone w pakiecie zawartości usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="03cb9-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="03cb9-120">Pakiet zawartości usługi Power BI **Analiza wydatków zakupowych** obejmuje raport zawierający zestaw wskaźników.</span><span class="sxs-lookup"><span data-stu-id="03cb9-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="03cb9-121">Te wskaźniki są wizualizowane jako wykresy, kafelki i tabele.</span><span class="sxs-lookup"><span data-stu-id="03cb9-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="03cb9-122">Następująca sekcja zawiera przegląd dostępnych wizualizacji.</span><span class="sxs-lookup"><span data-stu-id="03cb9-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="03cb9-123">Strona raportu o zakupach wg dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-123">Purchase by vendor report page</span></span>
<span data-ttu-id="03cb9-124">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-124">**Charts**</span></span>
- <span data-ttu-id="03cb9-125">10 najważniejszych dostawców wg wartości zakupów (wykres skumulowany słupkowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="03cb9-126">Łączne zakupy wg grupy dostawców/kraju/nazwy (wykres kołowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="03cb9-127">Zakupy wg grupy dostawców/kraju/nazwy (wykres kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="03cb9-128">Średnie zakupy wg grupy dostawców/kraju/nazwy (wykres kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="03cb9-129">**Kafelki**</span><span class="sxs-lookup"><span data-stu-id="03cb9-129">**Tiles**</span></span>
- <span data-ttu-id="03cb9-130">Suma zakupów</span><span class="sxs-lookup"><span data-stu-id="03cb9-130">Total purchase</span></span>
- <span data-ttu-id="03cb9-131">Wzrost zakupów r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-131">YOY purchase growth</span></span>
- <span data-ttu-id="03cb9-132">Łączna liczba dostawców</span><span class="sxs-lookup"><span data-stu-id="03cb9-132">Total # vendors</span></span>
- <span data-ttu-id="03cb9-133">Łączna liczba aktywnych dostawców</span><span class="sxs-lookup"><span data-stu-id="03cb9-133">Total # of active vendors</span></span>

<span data-ttu-id="03cb9-134">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="03cb9-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="03cb9-135">Strona raportu o produktach wg dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-135">Purchase by product report page</span></span>

<span data-ttu-id="03cb9-136">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-136">**Charts**</span></span>
- <span data-ttu-id="03cb9-137">Zakupy wg kategorii zaopatrzenia/nazwy produktu (wykres kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="03cb9-138">Łączne zakupy wg kategorii zaopatrzenia/nazwy produktu (wykres kołowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="03cb9-139">10 najważniejszych produktów wg wartości zakupów (wykres skumulowany słupkowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="03cb9-140">**Kafelki**</span><span class="sxs-lookup"><span data-stu-id="03cb9-140">**Tiles**</span></span>
- <span data-ttu-id="03cb9-141">Łączna liczba produktów</span><span class="sxs-lookup"><span data-stu-id="03cb9-141">Total # of products</span></span></li>
- <span data-ttu-id="03cb9-142">Procent aktywnych produktów w łącznej liczbie produktów</span><span class="sxs-lookup"><span data-stu-id="03cb9-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="03cb9-143">Liczba produktów odpowiedzialnych za 80% zakupów</span><span class="sxs-lookup"><span data-stu-id="03cb9-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="03cb9-144">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="03cb9-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="03cb9-145">Strona raportu o okresie wg dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-145">Purchase by period report page</span></span>
<span data-ttu-id="03cb9-146">Ta strona pokazuje zakupy w tym i ubiegłym roku oraz wzrost według kategorii zaopatrzenia.</span><span class="sxs-lookup"><span data-stu-id="03cb9-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="03cb9-147">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-147">**Charts**</span></span> 
- <span data-ttu-id="03cb9-148">Zakupy wg miesiąca/dnia (wykres kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="03cb9-149">Odchylenie łącznych zakupów r/r (wykres kaskadowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="03cb9-150">Wzrost łącznych zakupów r/r (wykres kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="03cb9-151">Zestawienie zaopatrzenia (macierz)</span><span class="sxs-lookup"><span data-stu-id="03cb9-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="03cb9-152">**Kafelki**</span><span class="sxs-lookup"><span data-stu-id="03cb9-152">**Tiles**</span></span>
- <span data-ttu-id="03cb9-153">Wzrost zakupów r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-153">YOY purchase growth</span></span>
- <span data-ttu-id="03cb9-154">% wzrostu zakupów r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-154">YOY purchase growth %</span></span>

<span data-ttu-id="03cb9-155">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="03cb9-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="03cb9-156">Strona raportu o zakupach wg lokalizacji dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="03cb9-157">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-157">**Charts**</span></span>
- <span data-ttu-id="03cb9-158">Zakupy wg miejscowości</span><span class="sxs-lookup"><span data-stu-id="03cb9-158">Purchase by city</span></span>
- <span data-ttu-id="03cb9-159">% wzrostu zakupów r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="03cb9-160">Zakupy wg krajów</span><span class="sxs-lookup"><span data-stu-id="03cb9-160">Purchase by country</span></span>

<span data-ttu-id="03cb9-161">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="03cb9-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="03cb9-162">Analiza wydatków zakupowych wg strony raportu</span><span class="sxs-lookup"><span data-stu-id="03cb9-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="03cb9-163">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-163">**Charts**</span></span> 
- <span data-ttu-id="03cb9-164">Zakupy w bieżącym roku wg miesiąca/dnia (wykres liniowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="03cb9-165">Zakupy w bieżącym i ubiegłym roku (wykres liniowy i kolumnowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="03cb9-166">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="03cb9-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="03cb9-167">Analiza wydatków zakupowych wg strony raportu dot. dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="03cb9-168">**Wykresy**</span><span class="sxs-lookup"><span data-stu-id="03cb9-168">**Charts**</span></span> 
- <span data-ttu-id="03cb9-169">% udziału 10 najważniejszych dostawców w zakupach (wykres lejkowy)</span><span class="sxs-lookup"><span data-stu-id="03cb9-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="03cb9-170">10 dostawców z największym wzrostem wydatków r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="03cb9-171">10 dostawców z największym spadkiem wydatków r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="03cb9-172">**Przykład** 
</span><span class="sxs-lookup"><span data-stu-id="03cb9-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="03cb9-173">Model i jednostki danych</span><span class="sxs-lookup"><span data-stu-id="03cb9-173">Data model and entities</span></span>
<span data-ttu-id="03cb9-174">Następujące dane są używane do wypełniania stron raportów w pakiecie zawartości **Analiza wydatków zakupowych** dla usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="03cb9-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="03cb9-175">Te dane są reprezentowane jako zagregowane miary umieszczone w magazynie jednostek.</span><span class="sxs-lookup"><span data-stu-id="03cb9-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="03cb9-176">Magazyn jednostek to baza danych programu Microsoft SQL Server zoptymalizowana pod kątem analiz.</span><span class="sxs-lookup"><span data-stu-id="03cb9-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="03cb9-177">Aby uzyskać więcej informacji, zobacz [Omówienie integracji usługi Power BI z magazynem jednostek](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="03cb9-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="03cb9-178">Zagregowane miary w tym pakiecie zawartości są podzbiorem zagregowanych miar, które były dostępne w module Zakupy w programach Microsoft Dynamics AX 2012 i Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="03cb9-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="03cb9-179">Aby zagregowane miary modułu można było umieścić w magazynie jednostek, trzeba ustawić te miary jako wdrażalne.</span><span class="sxs-lookup"><span data-stu-id="03cb9-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="03cb9-180">Aby uzyskać więcej informacji, zobacz procedurę umieszczania zagregowanych miar w magazynie jednostek w temacie [Omówienie integracji usługi Power BI z magazynem jednostek](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="03cb9-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="03cb9-181">Następujące najważniejsze zagregowane miary są dostępne bezpośrednio w jednostce Wiersze faktury i używane jako podstawa w pakiecie zawartości:</span><span class="sxs-lookup"><span data-stu-id="03cb9-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="03cb9-182">Jednostka</span><span class="sxs-lookup"><span data-stu-id="03cb9-182">Entity</span></span>        | <span data-ttu-id="03cb9-183">Najważniejsze zagregowane miary</span><span class="sxs-lookup"><span data-stu-id="03cb9-183">Key aggregate measurements</span></span> | <span data-ttu-id="03cb9-184">Źródło danych</span><span class="sxs-lookup"><span data-stu-id="03cb9-184">Data source</span></span>                                 | <span data-ttu-id="03cb9-185">Pole</span><span class="sxs-lookup"><span data-stu-id="03cb9-185">Field</span></span>              | <span data-ttu-id="03cb9-186">opis</span><span class="sxs-lookup"><span data-stu-id="03cb9-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="03cb9-187">Wiersze faktury</span><span class="sxs-lookup"><span data-stu-id="03cb9-187">Invoice lines</span></span> | <span data-ttu-id="03cb9-188">Zakup</span><span class="sxs-lookup"><span data-stu-id="03cb9-188">Purchase</span></span>                   | <span data-ttu-id="03cb9-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="03cb9-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="03cb9-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="03cb9-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="03cb9-191">Kwota w walucie rozliczeniowej.</span><span class="sxs-lookup"><span data-stu-id="03cb9-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="03cb9-192">W poniższej tabeli przedstawiono najważniejsze miary w pakiecie zawartości, które są obliczane na podstawie jednostki Wiersze faktury.</span><span class="sxs-lookup"><span data-stu-id="03cb9-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="03cb9-193">Pomiar</span><span class="sxs-lookup"><span data-stu-id="03cb9-193">Measure</span></span>               | <span data-ttu-id="03cb9-194">Obliczenie</span><span class="sxs-lookup"><span data-stu-id="03cb9-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03cb9-195">Zakupy w bieżącym roku</span><span class="sxs-lookup"><span data-stu-id="03cb9-195">Purchase current year</span></span> | <span data-ttu-id="03cb9-196">Zakupy w bieżącym roku = SUM('Wiersze faktury'\[Zakupy\])</span><span class="sxs-lookup"><span data-stu-id="03cb9-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="03cb9-197">Zakupy w ubiegłym roku</span><span class="sxs-lookup"><span data-stu-id="03cb9-197">Purchase last year</span></span>    | <span data-ttu-id="03cb9-198">Zakupy w ubiegłym roku = CALCULATE(SUM('Wiersze faktury'\[Zakupy\]), SAMEPERIODLASTYEAR(Daty\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="03cb9-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="03cb9-199">Wzrost zakupów r/r</span><span class="sxs-lookup"><span data-stu-id="03cb9-199">YOY purchase growth</span></span>   | <span data-ttu-id="03cb9-200">Wzrost zakupów r/r = \[Zakupy w bieżącym roku\] – \[Zakupy w ubiegłym roku\]</span><span class="sxs-lookup"><span data-stu-id="03cb9-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="03cb9-201">Następujące najważniejsze wymiary w pakiecie zawartości są używane jako filtry do dzielenia zagregowanych miar w celu uzyskania większej szczegółowości i lepszego wglądu analitycznego.</span><span class="sxs-lookup"><span data-stu-id="03cb9-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="03cb9-202">Jednostka</span><span class="sxs-lookup"><span data-stu-id="03cb9-202">Entity</span></span>                 | <span data-ttu-id="03cb9-203">Przykłady atrybutów</span><span class="sxs-lookup"><span data-stu-id="03cb9-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="03cb9-204">Dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-204">Vendors</span></span>                | <span data-ttu-id="03cb9-205">Grupa dostawców, Kraj/region dostawcy, Nazwa dostawcy</span><span class="sxs-lookup"><span data-stu-id="03cb9-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="03cb9-206">Produkty</span><span class="sxs-lookup"><span data-stu-id="03cb9-206">Products</span></span>               | <span data-ttu-id="03cb9-207">Numer produktu, Nazwa produktu, Nazwa grupy pozycji</span><span class="sxs-lookup"><span data-stu-id="03cb9-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="03cb9-208">Kategorie zaopatrzenia</span><span class="sxs-lookup"><span data-stu-id="03cb9-208">Procurement categories</span></span> | <span data-ttu-id="03cb9-209">Kategoria zaopatrzenia, Nazwa kategorii zaopatrzenia</span><span class="sxs-lookup"><span data-stu-id="03cb9-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="03cb9-210">Firmy</span><span class="sxs-lookup"><span data-stu-id="03cb9-210">Legal entities</span></span>         | <span data-ttu-id="03cb9-211">Nazwa firmy</span><span class="sxs-lookup"><span data-stu-id="03cb9-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="03cb9-212">Daty</span><span class="sxs-lookup"><span data-stu-id="03cb9-212">Dates</span></span>                  | <span data-ttu-id="03cb9-213">Daty, Przesunięcie roku</span><span class="sxs-lookup"><span data-stu-id="03cb9-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="03cb9-214">Domyślnie pakiet zawartości przestawia dane bieżącego roku kalendarzowego.</span><span class="sxs-lookup"><span data-stu-id="03cb9-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="03cb9-215">Można jednak zmienić wartość filtra dat w sekcji filtrów raportu.</span><span class="sxs-lookup"><span data-stu-id="03cb9-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="03cb9-216">Można również zmienić wartość filtra firm.</span><span class="sxs-lookup"><span data-stu-id="03cb9-216">You can also change the company filter.</span></span>