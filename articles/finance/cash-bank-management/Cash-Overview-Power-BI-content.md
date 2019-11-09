---
title: Pakiet zawartości Przegląd środków pieniężnych dla usługi Power BI
description: W tym temacie opisano pakiet zawartość Przegląd środków pieniężnych dostępny dla usługi Power BI. Wyjaśniono, jak uzyskać dostęp do raportów oferowanych w pakiecie, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.
author: saraschi2
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7621ca961288af81966e0ac883c6525f89960654
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553147"
---
# <a name="cash-overview-power-bi-content"></a><span data-ttu-id="786e6-104">Pakiet zawartości Przegląd środków pieniężnych dla usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="786e6-104">Cash overview Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="786e6-105">W tym temacie opisano pakiet zawartości **Przegląd środków pieniężnych** dostępny dla usługi Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="786e6-105">This topic describes the **Cash overview** Microsoft Power BI content.</span></span> <span data-ttu-id="786e6-106">Wyjaśniono, jak uzyskać dostęp do raportów oferowanych w pakiecie, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.</span><span class="sxs-lookup"><span data-stu-id="786e6-106">It explains how to access the reports that are included in the content, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="786e6-107">Przegląd</span><span class="sxs-lookup"><span data-stu-id="786e6-107">Overview</span></span>

<span data-ttu-id="786e6-108">Pakiet zawartości **Przegląd środków pieniężnych** dla usługi Power BI jest przeznaczony dla osób odpowiedzialnych za zarządzanie gotówką w swoich organizacjach.</span><span class="sxs-lookup"><span data-stu-id="786e6-108">The **Cash overview** Power BI content was created for individuals who are responsible for cash in their organization.</span></span> <span data-ttu-id="786e6-109">Pakiet zawartości **Przegląd środków pieniężnych** dla usługi Power BI zapewnia wgląd w przepływy środków pieniężnych w firmie.</span><span class="sxs-lookup"><span data-stu-id="786e6-109">The **Cash overview** Power BI content provides visibility into your cash flow.</span></span> <span data-ttu-id="786e6-110">Dostarcza również prognoz, które mogą pomóc podejmować lepsze decyzje i w efekcie optymalizować przepływ środków pieniężnych.</span><span class="sxs-lookup"><span data-stu-id="786e6-110">It also provides forecasts that can help you make better decisions and therefore improve the health of your cash flow.</span></span> <span data-ttu-id="786e6-111">Można analizować środki pieniężne według firm, walut i rachunków bankowych, aby lepiej zrozumieć przyczyny nadwyżek i niedoborów.</span><span class="sxs-lookup"><span data-stu-id="786e6-111">You can analyze cash by legal entity, currency, and bank account to get a better understanding of surpluses and shortfalls.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="786e6-112">Konfiguracja potrzebna do wyświetlenia zawartości Power BI.</span><span class="sxs-lookup"><span data-stu-id="786e6-112">Setup needed to view Power BI content</span></span>

<span data-ttu-id="786e6-113">Aby dane były wyświetlane w przeglądach Power BI **środków pieniężnych** i **zarządzania bankami**, należy zastosować następującą konfigurację.</span><span class="sxs-lookup"><span data-stu-id="786e6-113">The following setup needs to be completed in order for data to display in **Cash overview** and **Bank management** Power BI visuals.</span></span>

1. <span data-ttu-id="786e6-114">Otwórz **Administracja Systemu > Konfiguracja > Parametry Systemu** i ustaw **Walutę systemu** oraz **Kurs wymiany systemu**.</span><span class="sxs-lookup"><span data-stu-id="786e6-114">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="786e6-115">Otwórz **Księga ogólna > Konfiguracja > Księga** i ustaw **Waluta księgowa** oraz **Typ kursu wymiany**.</span><span class="sxs-lookup"><span data-stu-id="786e6-115">Go to **General Ledger > Setup > Ledger** to set **Accounting Currency** and **Exchange Rate Type**.</span></span>
2. <span data-ttu-id="786e6-116">Zdefiniuj kursy wymiany między walutami Transakcji a Walutą księgową, Walutą księgową a Walutą systemu oraz Walutą księgową oraz Walutami banku.</span><span class="sxs-lookup"><span data-stu-id="786e6-116">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency, and Accounting currency and Bank currencies.</span></span> <span data-ttu-id="786e6-117">Żeby to zrobić, otwórz **Księga Ogólna > Waluty > Kursy wymiany walut**.</span><span class="sxs-lookup"><span data-stu-id="786e6-117">To do this, go **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="786e6-118">Skonfiguruj i uruchom proces Prognozy Przepływów Pieniężnych.</span><span class="sxs-lookup"><span data-stu-id="786e6-118">Configure and run Cash Flow Forecasting.</span></span> <span data-ttu-id="786e6-119">Więcej informacji na temat uruchamiania Prognozy przepływów pieniężnych znajdziesz: [Prognozy przepływów pieniężnych](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="786e6-119">For more information about how to set up Cash flow forecasting, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span> 
4. <span data-ttu-id="786e6-120">Otwórz **Administracja Systemu > Konfiguracja > Sklep podmiotu** i odśwież łączny wskaźnik **CustCollectionsBIMeasurements**.</span><span class="sxs-lookup"><span data-stu-id="786e6-120">Go to **System administration > Setup > Entity Store** to refresh the **LedgerCovLiquidityMeasurement** aggregate measurement.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="786e6-121">Przechodzenie do pakietu zawartości usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="786e6-121">Accessing the Power BI content</span></span>

<span data-ttu-id="786e6-122">Raporty z zawartości **Przegląd środków pieniężnych** dla usługi Power BI są wyświetlane w obszarach roboczych **Przegląd środków pieniężnych** i **Zarządzanie rachunkami bankowymi**.</span><span class="sxs-lookup"><span data-stu-id="786e6-122">Reports from the **Cash overview** Power BI content are displayed in the **Cash overview** and **Bank management** workspaces.</span></span>

<span data-ttu-id="786e6-123">Aby wyświetlić raporty prognozowania przepływów pieniężnych z danymi, najpierw należy uruchomić proces obliczania prognozy za pomocą funkcji **Oblicz prognozy przepływów pieniężnych** z obszaru Zarządzanie gotówką i bankami.</span><span class="sxs-lookup"><span data-stu-id="786e6-123">To view the Cash flow forecasting reports with data, you must first run the forecast calculation process using the **Calculate cash flow forecasts** function from the Cash and bank management area.</span></span> <span data-ttu-id="786e6-124">Należy to zrobić dla każdej firmy uwzględnionej w prognozie.</span><span class="sxs-lookup"><span data-stu-id="786e6-124">This needs to be completed for each company included in the forecast.</span></span>  <span data-ttu-id="786e6-125">Następnie należy odświeżyć zagregowaną miarę LedgerCovLiquidityMeasurement na stronie **Magazyn jednostek**.</span><span class="sxs-lookup"><span data-stu-id="786e6-125">You then need to refresh the LedgerCovLiquidityMeasurement aggregate measurement on the **Entity Store** page.</span></span>  

<span data-ttu-id="786e6-126">Dla celów demonstracyjnych można za pomocą strony **Generuj dane** dodać dane demonstracyjne prognozowania przepływów pieniężnych z modułu Dane demonstracyjne.</span><span class="sxs-lookup"><span data-stu-id="786e6-126">For demonstration purposes, you can add cash flow forecasting demo data using the **Generate data** page from the Demo data module.</span></span>  <span data-ttu-id="786e6-127">Ten skrypt spowoduje wstawienie danych do tabel prognozowania przepływów pieniężnych, tak aby szybko wypełnić pola informacji niezbędnych dla raportów.</span><span class="sxs-lookup"><span data-stu-id="786e6-127">This script will insert data into the cash flow forecasting tables to quickly populate information necessary for reports.</span></span>  <span data-ttu-id="786e6-128">Ten moduł jest dostępny tylko wtedy, gdy w środowisku masz wdrożony model pakietu danych demonstracyjnych.</span><span class="sxs-lookup"><span data-stu-id="786e6-128">This module is only available if you have the Demo data suite model deployed on the environment.</span></span> 

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="786e6-129">Raporty dostępne w pakiecie zawartości dla usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="786e6-129">Reports that are included in the Power BI content</span></span>

<span data-ttu-id="786e6-130">W poniższej tabeli przedstawiono szczegóły dotyczące mierników, które znajdują się na każdej stronie raportu w pakiecie zawartości **Przegląd środków pieniężnych** dla usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="786e6-130">The following table provides details about the metrics that are found on each report page in the **Cash overview** Power BI content.</span></span>

| <span data-ttu-id="786e6-131">Raport</span><span class="sxs-lookup"><span data-stu-id="786e6-131">Report</span></span>                                | <span data-ttu-id="786e6-132">Zawartość</span><span class="sxs-lookup"><span data-stu-id="786e6-132">Contents</span></span> |
|---------------------------------------|----------|
| <span data-ttu-id="786e6-133">Przegląd środków pieniężnych — wszystkie firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-133">Cash overview – all companies</span></span>         | <ul><li><span data-ttu-id="786e6-134">Przychody i rozchody w walucie systemowej</span><span class="sxs-lookup"><span data-stu-id="786e6-134">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="786e6-135">Prognozowane salda w walutach</span><span class="sxs-lookup"><span data-stu-id="786e6-135">Forecasted currency balances</span></span></li><li><span data-ttu-id="786e6-136">Łączne saldo rachunków bankowych w walucie systemowej</span><span class="sxs-lookup"><span data-stu-id="786e6-136">Total bank balance in system currency</span></span></li><li><span data-ttu-id="786e6-137">Saldo wg firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-137">Balance by legal entity</span></span></li><li><span data-ttu-id="786e6-138">Dzisiejsze saldo rzeczywiste w porównaniu z prognozowanym w walucie konta bankowego</span><span class="sxs-lookup"><span data-stu-id="786e6-138">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="786e6-139">Przegląd środków pieniężnych — bieżąca firma</span><span class="sxs-lookup"><span data-stu-id="786e6-139">Cash overview – current company</span></span>       | <ul><li><span data-ttu-id="786e6-140">Przychody i rozchody w walucie rozliczeniowej</span><span class="sxs-lookup"><span data-stu-id="786e6-140">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="786e6-141">Prognozowane salda w walutach</span><span class="sxs-lookup"><span data-stu-id="786e6-141">Forecasted currency balances</span></span></li><li><span data-ttu-id="786e6-142">Łączne saldo rachunków bankowych w walucie rozliczeniowej</span><span class="sxs-lookup"><span data-stu-id="786e6-142">Total bank balance in accounting currency</span></span></li><li><span data-ttu-id="786e6-143">Dzisiejsze saldo rzeczywiste w porównaniu z prognozowanym w walucie konta bankowego</span><span class="sxs-lookup"><span data-stu-id="786e6-143">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="786e6-144">Prognoza przepływów pieniężnych — wszystkie firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-144">Cash flow forecast – all companies</span></span>    | <ul><li><span data-ttu-id="786e6-145">Przychody i rozchody w walucie systemowej</span><span class="sxs-lookup"><span data-stu-id="786e6-145">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="786e6-146">Dzienne podsumowanie prognoz</span><span class="sxs-lookup"><span data-stu-id="786e6-146">Daily forecast summary</span></span></li><li><span data-ttu-id="786e6-147">Szczegóły prognozy</span><span class="sxs-lookup"><span data-stu-id="786e6-147">Forecast details</span></span></li></ul> |
| <span data-ttu-id="786e6-148">Prognoza przepływów pieniężnych — waluta firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-148">Cash flow forecast – currency company</span></span> | <ul><li><span data-ttu-id="786e6-149">Przychody i rozchody w walucie rozliczeniowej</span><span class="sxs-lookup"><span data-stu-id="786e6-149">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="786e6-150">Dzienne podsumowanie prognoz</span><span class="sxs-lookup"><span data-stu-id="786e6-150">Daily forecast summary</span></span></li><li><span data-ttu-id="786e6-151">Szczegóły prognozy</span><span class="sxs-lookup"><span data-stu-id="786e6-151">Forecast details</span></span></li></ul> |
| <span data-ttu-id="786e6-152">Prognoza dla waluty</span><span class="sxs-lookup"><span data-stu-id="786e6-152">Currency forecast</span></span>                     | <ul><li><span data-ttu-id="786e6-153">Prognozowane salda w walutach</span><span class="sxs-lookup"><span data-stu-id="786e6-153">Forecasted currency balances</span></span></li><li><span data-ttu-id="786e6-154">Dzienne podsumowanie waluty</span><span class="sxs-lookup"><span data-stu-id="786e6-154">Daily currency summary</span></span></li><li><span data-ttu-id="786e6-155">Szczegóły prognozy</span><span class="sxs-lookup"><span data-stu-id="786e6-155">Forecast details</span></span></li></ul> |
| <span data-ttu-id="786e6-156">Salda rachunków bankowych</span><span class="sxs-lookup"><span data-stu-id="786e6-156">Bank balances</span></span>                         | <ul><li><span data-ttu-id="786e6-157">Łączne saldo rachunków bankowych w walucie systemowej</span><span class="sxs-lookup"><span data-stu-id="786e6-157">Total bank balance in system currency</span></span></li><li><span data-ttu-id="786e6-158">Saldo wg firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-158">Balance by legal entity</span></span></li><li><span data-ttu-id="786e6-159">Dzisiejsze saldo rzeczywiste w porównaniu z prognozowanym w walucie konta bankowego</span><span class="sxs-lookup"><span data-stu-id="786e6-159">Today’s actual vs forecasted balance in bank account currency</span></span></li><li><span data-ttu-id="786e6-160">Saldo wg konta bankowego</span><span class="sxs-lookup"><span data-stu-id="786e6-160">Balance by bank account</span></span></li><li><span data-ttu-id="786e6-161">Saldo wg waluty</span><span class="sxs-lookup"><span data-stu-id="786e6-161">Balance by currency</span></span></li></ul> |


## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="786e6-162">Opis modelu danych i jednostek</span><span class="sxs-lookup"><span data-stu-id="786e6-162">Understanding the data model and entities</span></span>

<span data-ttu-id="786e6-163">W poniższej tabeli przedstawiono jednostki, na których bazuje pakiet zawartości **Przegląd środków pieniężnych** dostępny dla usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="786e6-163">The following table shows the entities that the **Cash overview** Power BI content is based on.</span></span>

| <span data-ttu-id="786e6-164">Jednostka</span><span class="sxs-lookup"><span data-stu-id="786e6-164">Entity</span></span>                                                                          | <span data-ttu-id="786e6-165">Zawartość</span><span class="sxs-lookup"><span data-stu-id="786e6-165">Contents</span></span> |
|---------------------------------------------------------------------------------|----------|
| <span data-ttu-id="786e6-166">LedgerCovLiquidityMeasurement\_Company</span><span class="sxs-lookup"><span data-stu-id="786e6-166">LedgerCovLiquidityMeasurement\_Company</span></span>                                          | <span data-ttu-id="786e6-167">Firmy, według których będą filtrowane raporty</span><span class="sxs-lookup"><span data-stu-id="786e6-167">Companies to filter reports by</span></span> |
| <span data-ttu-id="786e6-168">LedgerCovLiquidityMeasurement\_Date</span><span class="sxs-lookup"><span data-stu-id="786e6-168">LedgerCovLiquidityMeasurement\_Date</span></span>                                             | <span data-ttu-id="786e6-169">Daty, według których będą filtrowane raporty</span><span class="sxs-lookup"><span data-stu-id="786e6-169">Dates to filter reports by</span></span> |
| <span data-ttu-id="786e6-170">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span><span class="sxs-lookup"><span data-stu-id="786e6-170">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span></span>                          | <span data-ttu-id="786e6-171">Rzeczywiste saldo rachunków bankowych w porównaniu z ostatnim prognozowanym saldem rachunków bankowych</span><span class="sxs-lookup"><span data-stu-id="786e6-171">Actual bank balance vs last forecasted bank balance</span></span> |
| <span data-ttu-id="786e6-172">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span><span class="sxs-lookup"><span data-stu-id="786e6-172">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span></span>                               | <span data-ttu-id="786e6-173">Szczegóły prognozowanej transakcji</span><span class="sxs-lookup"><span data-stu-id="786e6-173">Forecasted transaction details</span></span> |
| <span data-ttu-id="786e6-174">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span><span class="sxs-lookup"><span data-stu-id="786e6-174">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span></span>    | <span data-ttu-id="786e6-175">Zsumowane przychody, rozchody i salda środków pieniężnych w walucie rozliczeniowej każdej firmy</span><span class="sxs-lookup"><span data-stu-id="786e6-175">Summarized cash inflows, outflows, and balance using each company’s accounting currency</span></span> |
| <span data-ttu-id="786e6-176">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span><span class="sxs-lookup"><span data-stu-id="786e6-176">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span></span> | <span data-ttu-id="786e6-177">Zsumowane przychody, rozchody i salda środków pieniężnych w walucie systemowej dla wszystkich firm</span><span class="sxs-lookup"><span data-stu-id="786e6-177">Summarized cash inflows, outflows, and balance using the system currency for all companies</span></span> |
| <span data-ttu-id="786e6-178">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span><span class="sxs-lookup"><span data-stu-id="786e6-178">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span></span>            | <span data-ttu-id="786e6-179">Zsumowana kwota netto transakcji oraz salda walut w walutach transakcji</span><span class="sxs-lookup"><span data-stu-id="786e6-179">Summarized net transaction amount and balance of currencies using the transaction currency</span></span> |