---
title: Rozwiązanie PowerBI.com Wyniki finansowe
description: W tym temacie opisano pakiet zawartość Wyniki finansowe dostępny dla rozwiązania PowerBI.com.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35db2b51274afa6dae4cb5f75b4ba5390b167a49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181756"
---
# <a name="financial-performance-powerbicom-solution"></a><span data-ttu-id="b8757-103">Rozwiązanie PowerBI.com Wyniki finansowe</span><span class="sxs-lookup"><span data-stu-id="b8757-103">Financial performance PowerBI.com solution</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b8757-104">To rozwiązanie PowerBI.com zostało wycofane zgodnie z opisem w temacie [Pakiety zawartości usługi Power BI dostępne w usłudze AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span><span class="sxs-lookup"><span data-stu-id="b8757-104">This PowerBI.com solution has been deprecated as documented in [Power BI content packs available on AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span></span>

<span data-ttu-id="b8757-105">W tym temacie opisano pakiet zawartość **Wyniki finansowe** dostępny dla rozwiązania PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="b8757-105">This topic describes the **Financial performance** PowerBI.com solution.</span></span> <span data-ttu-id="b8757-106">Omówiono dostępny pulpit nawigacyjny i raporty oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="b8757-106">It describes the dashboard and reports that are included, and provides information about the data model and entities that were used to build the solution.</span></span>

## <a name="main-account-setup"></a><span data-ttu-id="b8757-107">Konfiguracja konta głównego</span><span class="sxs-lookup"><span data-stu-id="b8757-107">Main account setup</span></span>
<span data-ttu-id="b8757-108">Ponieważ organizacje chcą, aby kwoty zobowiązań i przychodów były wyświetlane jako kwoty dodatnie w raportach, ważne jest odpowiednie skonfigurowanie kont głównych.</span><span class="sxs-lookup"><span data-stu-id="b8757-108">Because organizations want liabilities and revenue amounts to appear as positive amounts on reports, the setup of the main accounts is important.</span></span> <span data-ttu-id="b8757-109">Aby kwoty na tych kontach głównych były wyświetlane jako dodatnie, typ konta głównego musi być ustawiony jako **Pasywa** lub **Przychód**.</span><span class="sxs-lookup"><span data-stu-id="b8757-109">For these main accounts to appear as positive amounts, the main account type must be set to **Liability** or **Revenue**.</span></span> <span data-ttu-id="b8757-110">Gdy są używane te typy kont, sprawozdawczość za pośrednictwem usługi Power BI będzie powodowała odwracanie znaków i wyświetlanie kwot jako dodatnich.</span><span class="sxs-lookup"><span data-stu-id="b8757-110">When these account types are used, reporting through Power BI will reverse the signs and show the amounts as positive.</span></span>

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a><span data-ttu-id="b8757-111">Pulpit nawigacyjny i raporty dostępne w rozwiązaniu PowerBI.com</span><span class="sxs-lookup"><span data-stu-id="b8757-111">Dashboard and reports that are included in the PowerBI.com solution</span></span>
<span data-ttu-id="b8757-112">Pulpit nawigacyjny zawiera kafelki podsumowań danych oparte na źródłowych raportach.</span><span class="sxs-lookup"><span data-stu-id="b8757-112">The dashboard contains summarized tiles of data that are based on underlying reports.</span></span> <span data-ttu-id="b8757-113">Każdy kafelek zawiera podsumowanie informacji o bieżącym roku dla wszystkich firm w organizacji.</span><span class="sxs-lookup"><span data-stu-id="b8757-113">Each tile contains summarized information for the current year across all companies in an organization.</span></span> <span data-ttu-id="b8757-114">Oto kilka dostępnych kafelków:</span><span class="sxs-lookup"><span data-stu-id="b8757-114">Here are some of the tiles:</span></span>

- <span data-ttu-id="b8757-115">Kasa</span><span class="sxs-lookup"><span data-stu-id="b8757-115">Cash</span></span>
- <span data-ttu-id="b8757-116">Łączne przychody w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-116">Total Revenue this year</span></span>
- <span data-ttu-id="b8757-117">Łączne wydatki w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-117">Total Expenses this year</span></span>
- <span data-ttu-id="b8757-118">Dochód netto w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-118">Net Income this year</span></span>
- <span data-ttu-id="b8757-119">Wskaźnik szybkiej płynności</span><span class="sxs-lookup"><span data-stu-id="b8757-119">Quick Ratio</span></span>
- <span data-ttu-id="b8757-120">Łączne wydatki w roku według kategorii kont</span><span class="sxs-lookup"><span data-stu-id="b8757-120">Total Expenses this year by account category</span></span>
- <span data-ttu-id="b8757-121">Wskaźnik bieżącej płynności</span><span class="sxs-lookup"><span data-stu-id="b8757-121">Current Ratio</span></span>
- <span data-ttu-id="b8757-122">Zadłużenie aktywów łącznie</span><span class="sxs-lookup"><span data-stu-id="b8757-122">Debt to Total Assets</span></span>
- <span data-ttu-id="b8757-123">Przychody rzeczywiste a prognozowane</span><span class="sxs-lookup"><span data-stu-id="b8757-123">Actual vs Forecasted Revenue</span></span>
- <span data-ttu-id="b8757-124">Zafakturowane przychody w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-124">Billed Revenue this Year</span></span>
- <span data-ttu-id="b8757-125">Wskaźnik wydatków operacyjnych w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-125">Operating expenses Ratio this year</span></span>
- <span data-ttu-id="b8757-126">Marża zysku w roku</span><span class="sxs-lookup"><span data-stu-id="b8757-126">Profit Margin this year</span></span>
- <span data-ttu-id="b8757-127">Wydatki rzeczywiste a zabudżetowane — wszystkie firmy</span><span class="sxs-lookup"><span data-stu-id="b8757-127">Actual vs Budget Expenses – All companies</span></span>

<span data-ttu-id="b8757-128">Każdy kafelek wykorzystuje pomocniczy raport.</span><span class="sxs-lookup"><span data-stu-id="b8757-128">Each tile is backed by a supporting report.</span></span> <span data-ttu-id="b8757-129">Raporty zawierają wykresy i tabele dostarczające więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="b8757-129">These reports contain both charts and tables that provide more information.</span></span> <span data-ttu-id="b8757-130">W poniższej tabeli opisano dostępne raporty.</span><span class="sxs-lookup"><span data-stu-id="b8757-130">The following table describes the reports.</span></span>

| <span data-ttu-id="b8757-131">Raport</span><span class="sxs-lookup"><span data-stu-id="b8757-131">Report</span></span>                      | <span data-ttu-id="b8757-132">Informacje zawarte w raporcie</span><span class="sxs-lookup"><span data-stu-id="b8757-132">Information that the report contains</span></span> |
|-----------------------------|--------------------------------------|
| <span data-ttu-id="b8757-133">Analiza środków pieniężnych</span><span class="sxs-lookup"><span data-stu-id="b8757-133">Cash Analysis</span></span>               | <span data-ttu-id="b8757-134">Gotówka z podziałem na firmy, gotówka według kwartałów, łączna gotówka oraz gotówka z podziałem na konta</span><span class="sxs-lookup"><span data-stu-id="b8757-134">Cash by legal entity, cash by quarter, total cash, and cash by account</span></span><blockquote>[!NOTE] <span data-ttu-id="b8757-135">Informacje o gotówce według kwartałów nie obejmują sald początkowych w sumie za pierwszy kwartał.</span><span class="sxs-lookup"><span data-stu-id="b8757-135">The cash by quarter information doesn't include beginning balances in the total for the first quarter.</span></span> <span data-ttu-id="b8757-136">Suma jest pokazywana dla nowych transakcji księgowanych w każdym kwartale.</span><span class="sxs-lookup"><span data-stu-id="b8757-136">It shows the total of new transactions that are posted in each quarter.</span></span></blockquote> |
| <span data-ttu-id="b8757-137">Analiza wskaźnika bieżącej płynności</span><span class="sxs-lookup"><span data-stu-id="b8757-137">Current Ratio Analysis</span></span>      | <span data-ttu-id="b8757-138">Wskaźnik bieżącej płynności z podziałem na firmy, wskaźnik bieżącej płynności według kwartałów oraz salda bieżących aktywów i pasywów</span><span class="sxs-lookup"><span data-stu-id="b8757-138">Current ratio by legal entity, current ratio by quarter, and balances for current assets and current liabilities</span></span> |
| <span data-ttu-id="b8757-139">Analiza wskaźnika szybkiej płynności</span><span class="sxs-lookup"><span data-stu-id="b8757-139">Quick Ratio Analysis</span></span>        | <span data-ttu-id="b8757-140">Wskaźnik szybkiej płynności z podziałem na firmy, wskaźnik szybkiej płynności według kwartałów oraz bieżące salda gotówki, należności i zobowiązań</span><span class="sxs-lookup"><span data-stu-id="b8757-140">Quick ratio by legal entity, quick ratio by quarter, and balances for cash, accounts receivable, and current liabilities</span></span> |
| <span data-ttu-id="b8757-141">Analiza kosztów własnych sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b8757-141">Cost of Goods Sold Analysis</span></span> | <span data-ttu-id="b8757-142">Koszt własny sprzedaży (KWS) z podziałem na firmy, KWS w tym i poprzednim roku według kwartałów, KWS według firm, łączny KWS oraz stosunek procentowy KWS do sprzedaży</span><span class="sxs-lookup"><span data-stu-id="b8757-142">Cost of goods sold (COGS) by legal entity, COGS this year and last year by quarter, COGS to sales by legal entity, total COGS, and COGS to sales percentage</span></span> |
| <span data-ttu-id="b8757-143">Analiza kapitału obrotowego</span><span class="sxs-lookup"><span data-stu-id="b8757-143">Working Capital Analysis</span></span>    | <span data-ttu-id="b8757-144">Kapitał obrotowy z podziałem na firmy, kapitał obrotowy według kwartałów, bieżące aktywa, bieżące pasywa i całkowity kapitał obrotowy</span><span class="sxs-lookup"><span data-stu-id="b8757-144">Working capital by legal entity, working capital by quarter, current assets, current liabilities, and total working capital</span></span> |
| <span data-ttu-id="b8757-145">Analiza aktywów i zadłużenia</span><span class="sxs-lookup"><span data-stu-id="b8757-145">Asset and Debt Analysis</span></span>     | <span data-ttu-id="b8757-146">Zwrot z całkowitych aktywów i zadłużenie do sumy aktywów z podziałem na firmy, zadłużenie do sumy aktywów i zwrot z całkowitych aktywów od początku kwartału, aktywa i pasywa</span><span class="sxs-lookup"><span data-stu-id="b8757-146">Return on total assets and debt to total assets by legal entity, debt to total assets and return on total assets quarter to date, assets, and liabilities</span></span> |
| <span data-ttu-id="b8757-147">Analiza marży zysku</span><span class="sxs-lookup"><span data-stu-id="b8757-147">Profit Margin Analysis</span></span>      | <span data-ttu-id="b8757-148">Marża zysku rzeczywista i zabudżetowana z podziałem na firmy, marża zysku według kwartałów, procent marży zysku i marża zysku</span><span class="sxs-lookup"><span data-stu-id="b8757-148">Actual and budget profit margin by legal entity, profit marking by quarter, profit margin percentage, and profit margin</span></span> |
| <span data-ttu-id="b8757-149">Analiza dochodu netto</span><span class="sxs-lookup"><span data-stu-id="b8757-149">Net Income Analysis</span></span>         | <span data-ttu-id="b8757-150">Dochód netto rzeczywisty i zabudżetowany z podziałem na firmy, dochód netto w tym i poprzednim roku oraz stosunek procentowy wydatków do dochodu netto</span><span class="sxs-lookup"><span data-stu-id="b8757-150">Actual and budget net income by legal entity, net income this year and last year, and expenses to net income percentage</span></span> |
| <span data-ttu-id="b8757-151">Analiza dochodów</span><span class="sxs-lookup"><span data-stu-id="b8757-151">Earnings Analysis</span></span>           | <span data-ttu-id="b8757-152">Dochody rzeczywiste i zabudżetowane przed potrąceniem odsetek i podatków (EBIT) z podziałem na firmy, EBIT z tym i poprzednim roku, stosunek procentowy wydatków do przychodów oraz stosunek wydatków rzeczywistych i zabudżetowanych do przychodów</span><span class="sxs-lookup"><span data-stu-id="b8757-152">Actual and budget earnings before interest and taxes (EBIT) by legal entity, EBIT this year and last year, expenses to revenue percentage, and actual and budget expenses to revenue</span></span> |
| <span data-ttu-id="b8757-153">Analiza przychodów</span><span class="sxs-lookup"><span data-stu-id="b8757-153">Revenue Analysis</span></span>            | <span data-ttu-id="b8757-154">Suma przychodów, suma przychodów rzeczywistych a zabudżetowanych z podziałem na firmy, suma przychodów w tym i poprzednim roku, różnica zabudżetowanych przychodów z podziałem na firmy oraz i suma przychodów w tym i poprzednim okresie</span><span class="sxs-lookup"><span data-stu-id="b8757-154">Total revenue, actual and budget total revenue by legal entity, total revenue this year and last year, revenue budget variance by legal entity, and total revenue this period and last period</span></span> |
| <span data-ttu-id="b8757-155">Analiza wydatków</span><span class="sxs-lookup"><span data-stu-id="b8757-155">Expense Analysis</span></span>            | <span data-ttu-id="b8757-156">Suma wydatków, suma wydatków rzeczywistych a zabudżetowanych z podziałem na firmy, suma wydatków rzeczywistych a zabudżetowanych według kwartałów, suma wydatków według kategorii kont oraz wskaźnik wydatków operacyjnych</span><span class="sxs-lookup"><span data-stu-id="b8757-156">Total expenses, actual to budget total expenses by legal entity, actual and budget total expense by quarter, total expenses by account category, and operating expenses ratio</span></span> |
| <span data-ttu-id="b8757-157">Analiza zafakturowanych przychodów</span><span class="sxs-lookup"><span data-stu-id="b8757-157">Billed Revenue Analysis</span></span>     | <span data-ttu-id="b8757-158">Suma rozrachunków z odbiorcami, suma rozrachunków z odbiorcami z podziałem na firmy, suma rozrachunków z odbiorcami według kwartałów oraz salda kont rozrachunków z odbiorcami</span><span class="sxs-lookup"><span data-stu-id="b8757-158">Total accounts receivable, total accounts receivable by legal entity, total accounts receivable by quarter, and balances for accounts receivable accounts</span></span><blockquote>[!NOTE] <span data-ttu-id="b8757-159">Informacje nie obejmują sald początkowych kont księgowych rozrachunków z odbiorcami.</span><span class="sxs-lookup"><span data-stu-id="b8757-159">The information doesn't include beginning balances for the accounts receivable ledger accounts.</span></span> <span data-ttu-id="b8757-160">Pokazują sumę dla nowych transakcji księgowanych w module Rozrachunki z odbiorcami.</span><span class="sxs-lookup"><span data-stu-id="b8757-160">It shows the total of new transactions that are posted to Accounts receivable.</span></span></blockquote> |

<span data-ttu-id="b8757-161">Wykresy i kafelki we wszystkich tych raportach można filtrować i przypinać do pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b8757-161">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="b8757-162">Aby uzyskać więcej informacji na temat filtrowania i przypinania w usłudze Power BI, zobacz [Tworzenie i konfigurowanie pulpitu nawigacyjnego](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span><span class="sxs-lookup"><span data-stu-id="b8757-162">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="b8757-163">Opis modelu danych i jednostek</span><span class="sxs-lookup"><span data-stu-id="b8757-163">Understanding the data model and entities</span></span>
<span data-ttu-id="b8757-164">Następujące jednostki zostały użyte jako podstawa w pakiecie zawartości rozwiązania PowerBI.com **Wyniki finansowe**:</span><span class="sxs-lookup"><span data-stu-id="b8757-164">The following entities were used as the basis of the **Financial performance** PowerBI.com solution:</span></span>

<span data-ttu-id="b8757-165">**Jednostki zagregowanych danych**</span><span class="sxs-lookup"><span data-stu-id="b8757-165">**Aggregate data entities**</span></span>

- <span data-ttu-id="b8757-166">**GeneralLedgerActivities** — ta jednostka agreguje salda księgi głównej według kategorii kont.</span><span class="sxs-lookup"><span data-stu-id="b8757-166">**GeneralLedgerActivities** – This entity aggregates general ledger balances by account category.</span></span>
- <span data-ttu-id="b8757-167">**BudgetActivities** — ta jednostka agreguje salda budżetu według kategorii kont.</span><span class="sxs-lookup"><span data-stu-id="b8757-167">**BudgetActivities** – This entity aggregates budget balances by account category.</span></span>

<span data-ttu-id="b8757-168">**Jednostki danych**</span><span class="sxs-lookup"><span data-stu-id="b8757-168">**Data entities**</span></span>

- <span data-ttu-id="b8757-169">FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="b8757-169">FiscalCalendars</span></span>
- <span data-ttu-id="b8757-170">MainAccounts</span><span class="sxs-lookup"><span data-stu-id="b8757-170">MainAccounts</span></span>
- <span data-ttu-id="b8757-171">LegalEntities</span><span class="sxs-lookup"><span data-stu-id="b8757-171">LegalEntities</span></span>
- <span data-ttu-id="b8757-172">Księgi</span><span class="sxs-lookup"><span data-stu-id="b8757-172">Ledgers</span></span>
- <span data-ttu-id="b8757-173">ChartofAccounts</span><span class="sxs-lookup"><span data-stu-id="b8757-173">ChartofAccounts</span></span>

<span data-ttu-id="b8757-174">Te jednostki zostały użyte do utworzenia obliczanych miar w modelu danych.</span><span class="sxs-lookup"><span data-stu-id="b8757-174">These entities were used to create calculated measures in the data model.</span></span> <span data-ttu-id="b8757-175">Obliczane miary są używane do obliczania kluczowych wskaźników wydajności (KPI) i generowania raportów, które są używane w pakiecie zawartości.</span><span class="sxs-lookup"><span data-stu-id="b8757-175">The calculated measures are used to calculate the key performance indicators (KPIs) and reports that are used in the content.</span></span> <span data-ttu-id="b8757-176">Domyślnie pakiet zawartości grupuje dane z trzech ostatnich lat i jednego roku przyszłego.</span><span class="sxs-lookup"><span data-stu-id="b8757-176">By default, the content brings in data for the last three years and one future year.</span></span> <span data-ttu-id="b8757-177">Aby uwzględnić dodatkowe obliczenia w raportach i pulpicie nawigacyjnym, można zmodyfikować [skoroszyt programu Microsoft Excel](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span><span class="sxs-lookup"><span data-stu-id="b8757-177">To include additional calculations on your reports and dashboard, you can modify the [Microsoft Excel workbook](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi).</span></span> <span data-ttu-id="b8757-178">Ten skoroszyt jest domyślnym modelem danych, który został użyty do utworzenia pakietu zawartości.</span><span class="sxs-lookup"><span data-stu-id="b8757-178">This workbook is the default data model that was used to create the content.</span></span>