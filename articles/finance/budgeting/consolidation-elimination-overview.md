---
title: Omówienie konsolidacji i eliminacji
description: Ten artykuł zawiera ogólne informacje o procesie konsolidacji i eliminacji. Znajdują się w nim również odpowiedzi na wybrane często zadawane pytania.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 266c594fda1609e4efdc8cdcd79767d94b755187
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188540"
---
# <a name="consolidation-and-elimination-overview"></a><span data-ttu-id="8f6ed-104">Omówienie konsolidacji i eliminacji</span><span class="sxs-lookup"><span data-stu-id="8f6ed-104">Consolidation and elimination overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f6ed-105">Ten artykuł zawiera ogólne informacje o procesie konsolidacji i eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-105">This article provides general information about the consolidation and elimination process.</span></span> <span data-ttu-id="8f6ed-106">Znajdują się w nim również odpowiedzi na wybrane często zadawane pytania.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-106">It includes answers to some frequently asked questions.</span></span>

<span data-ttu-id="8f6ed-107">Gdy konsolidujesz dane, wyniki finansowe dla wielu oddziałów firmy są łączone w wyniki dla jednej, skonsolidowanej firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-107">When you consolidate data, the financial results for multiple subsidiary companies are combined into results for a single, consolidated company.</span></span> <span data-ttu-id="8f6ed-108">Oddziały mogą znajdować się na różnych wersjach lub systemach, mogą nie być w pełni posiadane i mogą używać różnych walut.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-108">Subsidiaries might be on different versions or systems, they might not be fully owned, and they might use different currencies.</span></span> <span data-ttu-id="8f6ed-109">Istnieje wiele opcji do konsolidacji danych:</span><span class="sxs-lookup"><span data-stu-id="8f6ed-109">There are multiple options for consolidating data:</span></span>

-   <span data-ttu-id="8f6ed-110">**Konsolidacja online** — ta opcja konsoliduje salda dzienne według wybranych kontach i wymiarów i przechowuje je w konsolidowanej firmie.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-110">**Consolidate online** – This option consolidates daily balances by the selected accounts and dimensions, and stores them in a consolidation company.</span></span>
-   <span data-ttu-id="8f6ed-111">**Raporty finansowe** — ta opcja umożliwia konsolidację transakcji i sald i można z niej skorzystać w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-111">**Financial reporting** – This option enables consolidation of transactions and balances, and can be generated at any time.</span></span> <span data-ttu-id="8f6ed-112">Można utworzyć wiele poziomów hierarchii i można wyświetlić wiele walut raportowania</span><span class="sxs-lookup"><span data-stu-id="8f6ed-112">Multiple levels of hierarchies can be created, and multiple reporting currencies can be viewed.</span></span>
-   <span data-ttu-id="8f6ed-113">**Konsolidacja z importem** — to opcja importuje salda do konsolidowanej firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-113">**Consolidate with import** – This option imports balances into a consolidation company.</span></span>
-   <span data-ttu-id="8f6ed-114">**Eksportowanie sald firmy** — ta opcja pozwala uzyskać plik eksportu sald firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-114">**Export company balances** – This option provides an export file of company balances.</span></span> <span data-ttu-id="8f6ed-115">Plik można następnie zaimportować do innych instancji lub systemów.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-115">The file can then be imported into other instances or systems.</span></span> <span data-ttu-id="8f6ed-116">Raporty finansowe mogą być również używane do eksportu sald do pliku programu Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-116">Financial reporting can also be used to export the balances to a Microsoft Excel file.</span></span>

<span data-ttu-id="8f6ed-117">Eliminacje można raportować na wiele sposobów:</span><span class="sxs-lookup"><span data-stu-id="8f6ed-117">Eliminations can be reported in multiple ways:</span></span>

-   <span data-ttu-id="8f6ed-118">Reguły eliminacji można ustawić w systemie, a następnie przetwarzać w trakcie procesu konsolidacji lub za pomocą propozycji eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-118">Elimination rules can be set up in the system, and then processed during the consolidation process or through an elimination proposal.</span></span> <span data-ttu-id="8f6ed-119">Reguły mogą być księgowane dla każdej firmy, która ma wybraną opcję **Użyj na potrzeby procesu eliminacji finansowej** w ustawieniach firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-119">The rules can be posted to any company that has **Use for financial elimination process** selected in the legal entity setup.</span></span>
-   <span data-ttu-id="8f6ed-120">Można tworzyć oddzielną firmę i można jej używać do ręcznego określania i księgowania transakcji eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-120">A separate company can be created and used to manually determine and post elimination transactions.</span></span> <span data-ttu-id="8f6ed-121">Ta firma może być używana w procesie konsolidacji lub w raportach finansowych.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-121">This company can be used in the consolidation process or in financial reporting.</span></span>
-   <span data-ttu-id="8f6ed-122">Konta i wymiary finansowe, które są używane do określania działania międzyfirmowego można filtrować w definicji wiersza lub definicji kolumny w raporcie finansowym i dostępne są opcje wyświetlania wszystkich szczegółów.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-122">The accounts and financial dimensions that are used to determine intercompany activity can be filtered on a row definition or column definition in Financial reporting, and full drill-down capabilities can be used.</span></span> <span data-ttu-id="8f6ed-123">Obliczona kolumna lub wiersz może być następnie użyta do usuwania kont i wymiarów finansowych ze skonsolidowanej sumy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-123">A calculated column or row can then be used to remove the accounts and financial dimensions from the consolidated total.</span></span>

<span data-ttu-id="8f6ed-124">Istnieje wiele scenariuszy konsolidacji, a każda z tych metod może obsługiwać scenariusze na różne sposoby.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-124">There are many consolidation scenarios, and each method can handle the scenarios in different ways.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8f6ed-125">Często zadawane pytania</span><span class="sxs-lookup"><span data-stu-id="8f6ed-125">Frequently asked questions</span></span>
1.  <span data-ttu-id="8f6ed-126">Wolę księgować eliminacje w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-126">I prefer to post eliminations in a database.</span></span> <span data-ttu-id="8f6ed-127">Jakie mam dostępne opcje?</span><span class="sxs-lookup"><span data-stu-id="8f6ed-127">What are my options?</span></span>

<span data-ttu-id="8f6ed-128">Masz do wyboru kilka opcji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-128">You have multiple options.</span></span> <span data-ttu-id="8f6ed-129">Możesz użyć opcji **Konsolidacja online** i uwzględniać eliminacje podczas procesu lub jako propozycję.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-129">You can use the **Consolidate online** option, and include eliminations during the process or as a proposal.</span></span> <span data-ttu-id="8f6ed-130">Transakcje będą księgowane w konsolidowanej firmie.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-130">The transactions will be posted in the consolidation company.</span></span> <span data-ttu-id="8f6ed-131">Alternatywnie możesz mieć oddzielną firmę, w której ręcznie tworzysz eliminacje, a następnie używasz jej w raporcie finansowym lub procesie konsolidacji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-131">Alternatively, you can have a separate company that you manually create the eliminations in, and then use that company in Financial reporting or in the consolidation process.</span></span>

2.  <span data-ttu-id="8f6ed-132">Musimy mieć wyniki skonsolidowane w wielu walutach raportowania.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-132">We need our consolidated results in multiple reporting currencies.</span></span>

<span data-ttu-id="8f6ed-133">Opcja **Raport finansowy** oferuje obsługę nieograniczonej liczby walut raportowania.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-133">The **Financial reporting** option has unlimited reporting currencies.</span></span> <span data-ttu-id="8f6ed-134">Dane są przeliczane podczas generowania raportu na podstawie kursu wymiany i metody przeliczania waluty ustawionych na koncie głównym.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-134">The data is translated during report generation, based on the exchange rate type and currency translation method that are set on the main account.</span></span> <span data-ttu-id="8f6ed-135">Jednak ponieważ opcja **Konsolidacja online** obsługuje tylko jedną walutę raportowania, konsolidowana firma jest wymagana dla każdej waluty raportowania, jeśli używasz tej opcji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-135">However, because the **Consolidate online** option has only one reporting currency, a consolidated company is required for each reporting currency if you use that option.</span></span> <span data-ttu-id="8f6ed-136">Opcja **Raport finansowy** jest metodą zalecaną.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-136">The **Financial reporting** option is the recommended method.</span></span>

3.  <span data-ttu-id="8f6ed-137">Chcę wyświetlić szczegóły na poziomie transakcji dla każdej firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-137">I want to see transaction-level detail for each company.</span></span>

<span data-ttu-id="8f6ed-138">Opcja **Raport finansowy** jest rozwiązaniem, ponieważ można wyświetlić szczegóły na poziomie transakcji dla tylu firm, ile jest w definicji drzewa raportowania.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-138">The **Financial reporting** option is the solution, because transaction-level detail can be viewed for as many companies as are included in the reporting tree definition.</span></span>

4.  <span data-ttu-id="8f6ed-139">Używamy planowania budżetu lub kontroli budżetu i dane muszą być skonsolidowane.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-139">We are using budget planning or budget control, and it must be consolidated.</span></span>
<span data-ttu-id="8f6ed-140">Opcja **Raport finansowy** jest rozwiązaniem do konsolidacji planowania budżetu lub danych kontroli budżetu.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-140">The **Financial reporting** option is the solution to consolidate any budget planning or budget control data.</span></span>

5.  <span data-ttu-id="8f6ed-141">Nasze oddziały są rozproszone po całym świece i mamy wiele planów kont.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-141">Our subsidiaries are spread throughout the world, and we have multiple charts of accounts.</span></span> <span data-ttu-id="8f6ed-142">Jaka jest najlepsza metoda do konsolidowania naszych danych?</span><span class="sxs-lookup"><span data-stu-id="8f6ed-142">What is the best method for consolidating our data?</span></span>

<span data-ttu-id="8f6ed-143">Dostępne są różne opcje do obsługi wielu planów kont.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-143">You have multiple options when you must handle multiple charts of accounts.</span></span> <span data-ttu-id="8f6ed-144">Można użyć opcji **Konsolidacja online**, a następnie użyć konta konsolidacji zdefiniowanego na koncie głównym lub w grupie kont konsolidacyjnych.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-144">You can use the **Consolidate online** option, and then choose to use either the consolidation account that is defined on the main account or a consolidation account group.</span></span> <span data-ttu-id="8f6ed-145">Można też użyć opcji **Raport finansowy**, aby uwzględnić wiele łączy w wymiarach finansowych w definicji wiersza i zmapować konta.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-145">You can also use the **Financial reporting** option, include multiple links to the financial dimensions in the row definition, and map the accounts.</span></span>

6.  <span data-ttu-id="8f6ed-146">Potrzebujemy wielu poziomów konsolidacji.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-146">We require multiple levels of consolidation.</span></span> <span data-ttu-id="8f6ed-147">Innymi słowy najpierw konsolidujemy wszystkie nasze oddziałów w Europie do funta szterlinga (GBP).</span><span class="sxs-lookup"><span data-stu-id="8f6ed-147">In other words, we first consolidate all our European subsidiaries to the British pound (GBP).</span></span> <span data-ttu-id="8f6ed-148">Następnie na podstawie tych danych przeliczamy skonsolidowane kwoty na dolary amerykańskie (USD).</span><span class="sxs-lookup"><span data-stu-id="8f6ed-148">We then take that data and translate the consolidated amount to US dollars.</span></span> <span data-ttu-id="8f6ed-149">Jak możemy to zrobić?</span><span class="sxs-lookup"><span data-stu-id="8f6ed-149">How can we do this?</span></span>

<span data-ttu-id="8f6ed-150">Gdy wymaganych jest wiele poziomów konsolidacji i różne waluty są używane na każdym poziomie, trzeba skorzystać z opcji **Konsolidacja online**.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-150">When multiple levels of consolidation are required, and different currencies are used at each level, you must use the **Consolidate online** option.</span></span> <span data-ttu-id="8f6ed-151">Należy utworzyć wiele konsolidowanych, które różnią się od siebie walutami księgowania i raportowania.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-151">Multiple consolidation companies must be created that differ in their accounting and reporting currencies.</span></span> <span data-ttu-id="8f6ed-152">Następnie należy uruchomić konsolidację wiele razy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-152">The consolidation must then be run multiple times.</span></span> <span data-ttu-id="8f6ed-153">Opcja **Raport finansowy** zawsze przelicza z waluty księgowania firmy źródłowej na walutę wybranej firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-153">The **Financial reporting** option always translates from each source company's accounting currency to the selected currency.</span></span>

7.  <span data-ttu-id="8f6ed-154">Mamy oddziały w innym systemie.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-154">We have subsidiaries on a different system.</span></span> <span data-ttu-id="8f6ed-155">Jak je skonsolidować?</span><span class="sxs-lookup"><span data-stu-id="8f6ed-155">How can we consolidate them?</span></span>

<span data-ttu-id="8f6ed-156">Należy użyć funkcji **Konsolidacja z importem**, aby przenieść salda do konsolidowanej firmy.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-156">Use the **Consolidate with import** option to bring the balances into a consolidation company.</span></span>

8.  <span data-ttu-id="8f6ed-157">Niektóre z naszych oddziałów są naszą własnością tylko częściowo.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-157">Some of our subsidiaries are not fully owned.</span></span> <span data-ttu-id="8f6ed-158">Jaka jest najlepsza metoda do ich konsolidowania?</span><span class="sxs-lookup"><span data-stu-id="8f6ed-158">What is the best method for consolidating them?</span></span>

<span data-ttu-id="8f6ed-159">Dostępnych jest wiele opcji dla oddziałów będących częściową własnością.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-159">You have multiple options for partially owned subsidiaries.</span></span> <span data-ttu-id="8f6ed-160">Za pomocą opcji **Raport finansowy** można zdefiniować definicję drzewa raportowania i własność.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-160">By using the **Financial reporting** option, you can define a reporting tree definition and the ownership.</span></span> <span data-ttu-id="8f6ed-161">Można też obliczyć wiersz lub kolumnę do reprezentowania kwoty częściowej własności.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-161">You can also use a calculated row or column to represent the partially owned amount.</span></span> <span data-ttu-id="8f6ed-162">Można nawet wyświetlać udziały mniejszościowe jako oddzielny wiersz raportu.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-162">You can even show the minority interest as its own row on a report.</span></span> <span data-ttu-id="8f6ed-163">Można również użyć opcji **Konsolidacja online**.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-163">You can also use the **Consolidate online** option.</span></span> <span data-ttu-id="8f6ed-164">Na karcie **Firmy** w kolumnie **Własność**, w której można zdefiniować procent, jaki jest w posiadaniu firmy nadrzędnej.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-164">The **Legal entities** tab has an **Ownership** column, where you can define the percentage that is owned by the parent company.</span></span>

9.  <span data-ttu-id="8f6ed-165">Nasza organizacja musi wskazywać konsolidacje według jednostki biznesowej lub chce używać hierarchii organizacyjnej.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-165">Our organization must show consolidations by business unit or wants to use the organization hierarchies.</span></span>

<span data-ttu-id="8f6ed-166">Rozwiązaniem jest opcja **Raport finansowy**.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-166">The **Financial reporting** option is the solution.</span></span> <span data-ttu-id="8f6ed-167">Hierarchie organizacji zawierające firmy lub wymiary finansowe mogą być raportowane za pomocą Raportu finansowego.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-167">Organization hierarchies that have legal entities or financial dimensions in them can be reported on in Financial reporting.</span></span> <span data-ttu-id="8f6ed-168">Można również tworzyć własne wielopoziomowe hierarchie przy użyciu definicji drzewa raportowania z kombinacją firm i wartości wymiarów.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-168">You can also create your own multilevel hierarchies by using a reporting tree definition that has a combination of legal entities and dimension values.</span></span>

10. <span data-ttu-id="8f6ed-169">Mamy więcej niż jedną instancję systemu.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-169">We have more than one instance of the system.</span></span>

<span data-ttu-id="8f6ed-170">Za pomocą opcji **Eksportuj salda firmy** można wyeksportować dane z jednej instancji, a następnie przy użyciu opcji **Konsoliduj z importu** w drugiej instancji można skonsolidować dane.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-170">By using the **Export company balances** option to export from one instance and then using the **Consolidate with import** option on the other instance, you can consolidate the data.</span></span>


<span data-ttu-id="8f6ed-171">Aby uzyskać więcej informacji, zobacz [Przeszacowanie waluty w konsolidowanej firmie](../general-ledger/currency-revaluation-consolidation-company.md).</span><span class="sxs-lookup"><span data-stu-id="8f6ed-171">For more information, see [Currency revalution in a consolidation company](../general-ledger/currency-revaluation-consolidation-company.md).</span></span>

