---
title: Raporty finansowe bilansu próbnego
description: W tym artykule opisano domyślne raporty o bilansach próbnych. Omówiono również bloki konstrukcyjne skojarzone z tymi raportami oraz sposoby modyfikowania raportów w celu dostosowania ich do wymagań biznesowych.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175575"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="f1678-104">Raporty finansowe bilansu próbnego</span><span class="sxs-lookup"><span data-stu-id="f1678-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1678-105">W tym artykule opisano domyślne raporty o bilansach próbnych.</span><span class="sxs-lookup"><span data-stu-id="f1678-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="f1678-106">Omówiono również bloki konstrukcyjne skojarzone z tymi raportami oraz sposoby modyfikowania raportów w celu dostosowania ich do wymagań biznesowych.</span><span class="sxs-lookup"><span data-stu-id="f1678-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="f1678-107">Domyślne raporty finansowe bilansu próbnego</span><span class="sxs-lookup"><span data-stu-id="f1678-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="f1678-108">W module Raporty finansowe są dostępne trzy raporty bilansu próbnego.</span><span class="sxs-lookup"><span data-stu-id="f1678-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="f1678-109">Raport domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-109">Default report</span></span>                                 | <span data-ttu-id="f1678-110">Działanie</span><span class="sxs-lookup"><span data-stu-id="f1678-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1678-111">Szczegółowy bilans próbny — domyślne</span><span class="sxs-lookup"><span data-stu-id="f1678-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f1678-112">Oferuje informacje dla wszystkich kont i obejmuje wszystkie salda po stronie debetowej i kredytowej, oraz ich wartości netto, wraz z datą transakcji, załącznikiem i opisem arkusza.</span><span class="sxs-lookup"><span data-stu-id="f1678-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="f1678-113">Sumaryczny bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f1678-114">Oferuje informacje o saldzie dla wszystkich kont i zawiera salda otwarcia i zamknięcia oraz salda po stronie debetowej i kredytowej razem z ich różnicą netto.</span><span class="sxs-lookup"><span data-stu-id="f1678-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="f1678-115">Sumaryczny bilans próbny rok do roku — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f1678-116">Oferuje informacje o saldzie dla wszystkich kont i zawiera salda otwarcia i zamknięcia oraz salda po stronie debetowej i kredytowej razem z ich różnicą netto dla bieżącego roku i roku ubiegłego.</span><span class="sxs-lookup"><span data-stu-id="f1678-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="f1678-117">Podstawowe elementy</span><span class="sxs-lookup"><span data-stu-id="f1678-117">Building blocks</span></span>
<span data-ttu-id="f1678-118">Raporty finansowe bilansu próbnego wykorzystują następujące podstawowe elementy.</span><span class="sxs-lookup"><span data-stu-id="f1678-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="f1678-119">Raport domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-119">Default report</span></span>                                 | <span data-ttu-id="f1678-120">Definicja wiersza</span><span class="sxs-lookup"><span data-stu-id="f1678-120">Row definition</span></span>          | <span data-ttu-id="f1678-121">Definicja kolumny</span><span class="sxs-lookup"><span data-stu-id="f1678-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="f1678-122">Szczegółowy bilans próbny — domyślne</span><span class="sxs-lookup"><span data-stu-id="f1678-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f1678-123">Bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-123">Trial Balance - Default</span></span> | <span data-ttu-id="f1678-124">Szczegółowy bilans próbny — domyślne</span><span class="sxs-lookup"><span data-stu-id="f1678-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="f1678-125">Sumaryczny bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f1678-126">Bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-126">Trial Balance - Default</span></span> | <span data-ttu-id="f1678-127">Sumaryczny bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="f1678-128">Sumaryczny bilans próbny rok do roku — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f1678-129">Bilans próbny — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-129">Trial Balance - Default</span></span> | <span data-ttu-id="f1678-130">Sumaryczny bilans próbny rok do roku — domyślny</span><span class="sxs-lookup"><span data-stu-id="f1678-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="f1678-131">Definicja wiersza</span><span class="sxs-lookup"><span data-stu-id="f1678-131">Row definition</span></span>

<span data-ttu-id="f1678-132">Definicja wiersza Bilans próbny — domyślny zawiera pojedynczy wiersz, który pobiera informacje ze wszystkich kont głównych.</span><span class="sxs-lookup"><span data-stu-id="f1678-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="f1678-133">Dlatego każdy może wygenerować raport bez konieczności wprowadzania żadnych zmian.</span><span class="sxs-lookup"><span data-stu-id="f1678-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="f1678-134">Podczas przeglądania raportu można przejść do pojedynczego wiersza, aby wyświetlić szczegóły dotyczące poszczególnych kont.</span><span class="sxs-lookup"><span data-stu-id="f1678-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="f1678-135">Można zmodyfikować definicję wiersza, tak aby zawierała więcej szczegółów.</span><span class="sxs-lookup"><span data-stu-id="f1678-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="f1678-136">Aby zmodyfikować definicję wiersza Bilans próbny — domyślny, by zawierał wiesze dla wszystkich kont, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="f1678-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="f1678-137">Kliknij **Edycja**, a następnie kliknij **Wstaw wiersze z wymiarów**.</span><span class="sxs-lookup"><span data-stu-id="f1678-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="f1678-138">Polecenie **Wstaw wiersze z wymiarów** pozwala wybrać wymiary, które mają znaleźć się w definicji wiersza.</span><span class="sxs-lookup"><span data-stu-id="f1678-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="f1678-139">Dla tej definicji wiersza użyjesz **Konta głównego**.</span><span class="sxs-lookup"><span data-stu-id="f1678-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="f1678-140">Upewnij się, że **Konto główne** zawiera wszystkie znaki „&”, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1678-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="f1678-141">Teraz definicja wiersza zawiera wszystkie konta główne dla Twojej domyślnej firmy.</span><span class="sxs-lookup"><span data-stu-id="f1678-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="f1678-142">Definicja kolumny</span><span class="sxs-lookup"><span data-stu-id="f1678-142">Column definition</span></span>

<span data-ttu-id="f1678-143">Każdy raport bilansu próbnego używa innej definicji kolumny.</span><span class="sxs-lookup"><span data-stu-id="f1678-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="f1678-144">Te definicje kolumn zawierają różnego rodzaju kolumny oferujący różne poziomu szczegółowości i danych finansowych.</span><span class="sxs-lookup"><span data-stu-id="f1678-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="f1678-145">**Szczegółowy bilans próbny — domyślne typy kolumn:**</span><span class="sxs-lookup"><span data-stu-id="f1678-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="f1678-146">**DESC** — opis z definicji wiersza</span><span class="sxs-lookup"><span data-stu-id="f1678-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f1678-147">**ACCT** — kody konta</span><span class="sxs-lookup"><span data-stu-id="f1678-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f1678-148">**ATTR (3)** — atrybuty:</span><span class="sxs-lookup"><span data-stu-id="f1678-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="f1678-149">Data transakcji</span><span class="sxs-lookup"><span data-stu-id="f1678-149">Transaction Date</span></span>
        -   <span data-ttu-id="f1678-150">Załącznik</span><span class="sxs-lookup"><span data-stu-id="f1678-150">Voucher</span></span>
        -   <span data-ttu-id="f1678-151">Opis arkusza</span><span class="sxs-lookup"><span data-stu-id="f1678-151">Journal Description</span></span>
    -   <span data-ttu-id="f1678-152">**FD** — dane finansowe zawierające tylko debety</span><span class="sxs-lookup"><span data-stu-id="f1678-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f1678-153">**FD** — dane finansowe zawierające tylko kredyty</span><span class="sxs-lookup"><span data-stu-id="f1678-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f1678-154">**CALC** — różnica netto</span><span class="sxs-lookup"><span data-stu-id="f1678-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="f1678-155">**Sumaryczny bilans próbny — domyślne typy kolumn:**</span><span class="sxs-lookup"><span data-stu-id="f1678-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="f1678-156">**ACCT** — kody konta</span><span class="sxs-lookup"><span data-stu-id="f1678-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f1678-157">**DESC** — opis z definicji wiersza</span><span class="sxs-lookup"><span data-stu-id="f1678-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f1678-158">**ATTR** – atrybut:</span><span class="sxs-lookup"><span data-stu-id="f1678-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="f1678-159">Załącznik</span><span class="sxs-lookup"><span data-stu-id="f1678-159">Voucher</span></span>
    -   <span data-ttu-id="f1678-160">**FD** — dane finansowe salda początkowego</span><span class="sxs-lookup"><span data-stu-id="f1678-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="f1678-161">**FD** — dane finansowe zawierające tylko debety</span><span class="sxs-lookup"><span data-stu-id="f1678-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f1678-162">**FD** — dane finansowe zawierające tylko kredyty</span><span class="sxs-lookup"><span data-stu-id="f1678-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f1678-163">**CALC** — różnica netto</span><span class="sxs-lookup"><span data-stu-id="f1678-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f1678-164">**CALC** — saldo zamknięcia</span><span class="sxs-lookup"><span data-stu-id="f1678-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="f1678-165">**Sumaryczny bilans próbny rok do roku — domyślny:**</span><span class="sxs-lookup"><span data-stu-id="f1678-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="f1678-166">**ACCT** — kody konta</span><span class="sxs-lookup"><span data-stu-id="f1678-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f1678-167">**DESC** — opis z definicji wiersza</span><span class="sxs-lookup"><span data-stu-id="f1678-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f1678-168">**ATTR** – atrybut</span><span class="sxs-lookup"><span data-stu-id="f1678-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="f1678-169">Załącznik</span><span class="sxs-lookup"><span data-stu-id="f1678-169">Voucher</span></span>
    -   <span data-ttu-id="f1678-170">**FD** — dane finansowe salda początkowego dla bieżącego roku</span><span class="sxs-lookup"><span data-stu-id="f1678-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="f1678-171">**FD** — dane finansowe zawierające tylko debety dla bieżącego roku</span><span class="sxs-lookup"><span data-stu-id="f1678-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="f1678-172">**FD** — dane finansowe zawierające tylko kredyty dla bieżącego roku</span><span class="sxs-lookup"><span data-stu-id="f1678-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="f1678-173">**CALC** — różnica netto</span><span class="sxs-lookup"><span data-stu-id="f1678-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f1678-174">**CALC** — saldo zamknięcia</span><span class="sxs-lookup"><span data-stu-id="f1678-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="f1678-175">**FD** — dane finansowe zawierające tylko debety dla ostatniego roku</span><span class="sxs-lookup"><span data-stu-id="f1678-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="f1678-176">**FD** — dane finansowe zawierające tylko kredyty dla ostatniego roku</span><span class="sxs-lookup"><span data-stu-id="f1678-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="f1678-177">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="f1678-177">Additional resources</span></span>
--------

[<span data-ttu-id="f1678-178">Raporty finansowe</span><span class="sxs-lookup"><span data-stu-id="f1678-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="f1678-179">Wyświetlanie raportów finansowych</span><span class="sxs-lookup"><span data-stu-id="f1678-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="f1678-180">Blog o sprawozdawczości finansowej w systemie Dynamics</span><span class="sxs-lookup"><span data-stu-id="f1678-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)


