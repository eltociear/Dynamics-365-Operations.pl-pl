---
title: Reguły eliminacji
description: Ten temat zawiera informacje o różnych regułach eliminacji i opcjach raportowania eliminacji.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdcfebad5329b8ac6f3507f2bc59f26cf70aae33
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186677"
---
# <a name="elimination-rules"></a><span data-ttu-id="8bec6-103">Reguły eliminacji</span><span class="sxs-lookup"><span data-stu-id="8bec6-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bec6-104">Ten temat zawiera informacje o różnych regułach eliminacji i opcjach raportowania eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="8bec6-105">Transakcje eliminacji są wymagane, gdy firma macierzysta współpracuje z przynajmniej jednym oddziałem firmy oraz korzysta ze skonsolidowanych raportów finansowych.</span><span class="sxs-lookup"><span data-stu-id="8bec6-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="8bec6-106">Skonsolidowane sprawozdania finansowe muszą zawierać tylko transakcje między skonsolidowaną organizacją a innymi podmiotami spoza tej organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="8bec6-107">Z tego względu transakcje między firmami, które znajdują się w tej samej organizacji, należy usunąć lub wyeliminować z księgi głównej, aby nie były wyświetlane w raportach finansowych.</span><span class="sxs-lookup"><span data-stu-id="8bec6-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="8bec6-108">Istnieje wiele sposobów przygotowania raportu na temat eliminacji:</span><span class="sxs-lookup"><span data-stu-id="8bec6-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="8bec6-109">Reguły eliminacji mogą być tworzone i przetwarzane w firmie konsolidacji lub eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="8bec6-110">Raporty finansowe mogą pokazywać konta i wymiary eliminacji w określonym wierszu lub kolumnie.</span><span class="sxs-lookup"><span data-stu-id="8bec6-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="8bec6-111">Odrębna osoba prawna może służyć do księgowania transakcji ręcznej do śledzenia eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="8bec6-112">Temat poświęcony jest regułom eliminacji, które są przetwarzane w firmie konsolidacji i eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="8bec6-113">Można określić reguły eliminacji w celu utworzenia transakcji eliminacji w firmie określonej jako firma docelowa dla eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="8bec6-114">Ta firma docelowa jest znana jako firma z wpisami eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="8bec6-115">Arkusze eliminacji mogą być generowane albo podczas procesu konsolidacji, albo za pomocą propozycji arkusza eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="8bec6-116">Przed skonfigurowaniem reguł eliminacji należy zapoznać się z następującymi terminami:</span><span class="sxs-lookup"><span data-stu-id="8bec6-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="8bec6-117">**Źródłowa firma** — Firma, w której zostały zaksięgowane kwoty, które są eliminowane.</span><span class="sxs-lookup"><span data-stu-id="8bec6-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="8bec6-118">**Firma docelowa** — Firma, w której są księgowane reguły eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="8bec6-119">**Firma z wpisami eliminacji** — Firma określona jako firma docelowa dla eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="8bec6-120">**Firma skonsolidowana** — Firma utworzona na potrzeby raportowania wyników finansowych grupy firm.</span><span class="sxs-lookup"><span data-stu-id="8bec6-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="8bec6-121">Dane finansowe firm są konsolidowane w ramach tej firmy, a następnie przy użyciu połączonych danych jest tworzony raport finansowy.</span><span class="sxs-lookup"><span data-stu-id="8bec6-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="8bec6-122">W poniższej tabeli przedstawiono typy transakcji, które być może trzeba będzie wyeliminować.</span><span class="sxs-lookup"><span data-stu-id="8bec6-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bec6-123">Typ transakcji</span><span class="sxs-lookup"><span data-stu-id="8bec6-123">Transaction type</span></span></th>
<th><span data-ttu-id="8bec6-124">Przykład</span><span class="sxs-lookup"><span data-stu-id="8bec6-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bec6-125">Wprowadzanie i fakturowanie zamówień sprzedaży (przetwarzanie scentralizowane)</span><span class="sxs-lookup"><span data-stu-id="8bec6-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="8bec6-126">Sprzedaż produktu odbiorcy w imieniu innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-127">Wprowadzanie i fakturowanie zamówień sprzedaży (międzyfirmowe/wewnątrzfirmowe)</span><span class="sxs-lookup"><span data-stu-id="8bec6-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="8bec6-128">Sprzedaż produktów między firmami w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bec6-129">Zamówienia zakupu (przetwarzanie scentralizowane)</span><span class="sxs-lookup"><span data-stu-id="8bec6-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="8bec6-130">Zakup zapasów, materiałów, usług, środków trwałych i innych produktów u dostawcy w imieniu innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-131">Zarządzanie zapasami (międzyfirmowe/wewnątrzfirmowe)</span><span class="sxs-lookup"><span data-stu-id="8bec6-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="8bec6-132">Przeniesienie zapasów jednej firmy do środków trwałych innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="8bec6-133">Przeniesienie zapasów jednej firmy do zapasów innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bec6-134">Śledzenie zapasów w transporcie</span><span class="sxs-lookup"><span data-stu-id="8bec6-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="8bec6-135">Przeniesienie towarów między magazynami w tej samej firmie, ale znajdującymi się w różnych lokalizacjach geograficznych.</span><span class="sxs-lookup"><span data-stu-id="8bec6-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-136">Scentralizowane przetwarzanie faktur rozrachunków z dostawcami</span><span class="sxs-lookup"><span data-stu-id="8bec6-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="8bec6-137">Rejestrowanie faktury w imieniu innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bec6-138">Scentralizowane przetwarzanie płatności rozrachunków z dostawcami</span><span class="sxs-lookup"><span data-stu-id="8bec6-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="8bec6-139">Płacenie za fakturę w imieniu innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-140">Zarządzanie gotówką i akcjami (przetwarzanie scentralizowane)</span><span class="sxs-lookup"><span data-stu-id="8bec6-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="8bec6-141">Przetwarzanie płatności podatkowych, zwrotów podatku, należnych odsetek, pożyczek, zaliczek, wypłaconych dywidend oraz prowizji/tantiem.</span><span class="sxs-lookup"><span data-stu-id="8bec6-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="8bec6-142">Płacenie wydatków w imieniu innej firmy w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="8bec6-143">Faktura jest wprowadzana w księgach firmy docelowej, a użytkownik musi rozliczyć ją wzajemnie między firmami.</span><span class="sxs-lookup"><span data-stu-id="8bec6-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="8bec6-144">Na przykład jedna firma płaci raport z wydatków pracownika w innej firmie.</span><span class="sxs-lookup"><span data-stu-id="8bec6-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="8bec6-145">W tym przypadku raport z wydatków pracownika ma wydatki związane z inną firmą.</span><span class="sxs-lookup"><span data-stu-id="8bec6-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="8bec6-146">Przekazywanie gotówki z jednej firmy do innej w organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bec6-147">Rozrachunki z odbiorcami (przetwarzanie scentralizowane)</span><span class="sxs-lookup"><span data-stu-id="8bec6-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="8bec6-148">Przyjmowanie gotówki na podstawie faktury odbiorcy innej firmy i składanie czeku na konto bankowe tej firmy.</span><span class="sxs-lookup"><span data-stu-id="8bec6-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-149">Lista płac (przetwarzanie scentralizowane, międzyfirmowe/wewnątrzfirmowe)</span><span class="sxs-lookup"><span data-stu-id="8bec6-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="8bec6-150">Dokonywanie płatności listy płac innej firmy.</span><span class="sxs-lookup"><span data-stu-id="8bec6-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="8bec6-151">Na przykład firma wypłaca pensje według listy płac swoim pracownikom, ale realizuje zwrot kosztów dla pracowników innej firmy w tym przebiegu płatności.</span><span class="sxs-lookup"><span data-stu-id="8bec6-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="8bec6-152">Lub jeśli pracownik jest zatrudniony na pół etatu w firmie A oraz na pół etatu w firmie B i otrzymuje w obu miejscach pracy inne świadczenia.</span><span class="sxs-lookup"><span data-stu-id="8bec6-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="8bec6-153">W takich przypadkach płaca pracownika obejmuje płatności z obu firm.</span><span class="sxs-lookup"><span data-stu-id="8bec6-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="8bec6-154">Oprócz wynagrodzeń mogą być także księgowane podatki, świadczenia, potrącenia i naliczenia związane z wynagrodzeniami.</span><span class="sxs-lookup"><span data-stu-id="8bec6-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="8bec6-155">Przenoszenie robocizny między działami lub oddziałami.</span><span class="sxs-lookup"><span data-stu-id="8bec6-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bec6-156">Środki trwałe (międzyfirmowe/wewnątrzfirmowe)</span><span class="sxs-lookup"><span data-stu-id="8bec6-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="8bec6-157">Przenoszenie środków trwałych do środków trwałych lub zapasów innej firmy.</span><span class="sxs-lookup"><span data-stu-id="8bec6-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bec6-158">Alokacje (międzyfirmowe/wewnątrzfirmowe)</span><span class="sxs-lookup"><span data-stu-id="8bec6-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="8bec6-159">Przetwarzanie alokacji firmowych.</span><span class="sxs-lookup"><span data-stu-id="8bec6-159">You process corporate allocations.</span></span> <span data-ttu-id="8bec6-160">Alokacje to działania dotyczące dowolnego konta podlegającego alokacji, niezależnie od modułu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="8bec6-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="8bec6-161">Przykład</span><span class="sxs-lookup"><span data-stu-id="8bec6-161">Example</span></span>
<span data-ttu-id="8bec6-162">Twoja firma, czyli firma A, sprzedaje gadżety innej firmie w twojej organizacji, czyli firmie B. W poniższym przykładzie pokazano sposób, w jaki być może trzeba będzie wyeliminować transakcje między dwiema firmami:</span><span class="sxs-lookup"><span data-stu-id="8bec6-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="8bec6-163">Firma A sprzedaje gadżet, który kosztuje 10,00, firmie B za 10,00.</span><span class="sxs-lookup"><span data-stu-id="8bec6-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="8bec6-164">Firma A sprzedaje gadżet, który kosztuje 10,00, firmie B za 10,00 + 2,00 rzeczywistych kosztów wysyłki.</span><span class="sxs-lookup"><span data-stu-id="8bec6-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="8bec6-165">Firma A sprzedaje firmie B gadżet o wartości 10,00 w cenie 15,00 i otrzymuje marżę z tej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="8bec6-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="8bec6-166">Firma A sprzedaje firmie B gadżet o wartości 10,00 w cenie 15,00 i otrzymuje połowę marży z tej sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="8bec6-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="8bec6-167">Firma B otrzymuje drugą połowę marży ze sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="8bec6-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="8bec6-168">Zatem przychód jest podzielony.</span><span class="sxs-lookup"><span data-stu-id="8bec6-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="8bec6-169">Podział przychodu stanowi zachętę do zamówienia z innej firmy w organizacji, a nie z zewnętrznej organizacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="8bec6-170">Wszystkie te transakcje tworzą transakcje międzyfirmowe, księgowane na kontach zobowiązań i należności.</span><span class="sxs-lookup"><span data-stu-id="8bec6-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="8bec6-171">Ponadto w tych transakcjach mogą być uwzględniane kwoty podwyżek i obniżek, gdy kwota sprzedaży międzyfirmowej nie jest równa kosztowi sprzedanych towarów.</span><span class="sxs-lookup"><span data-stu-id="8bec6-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="8bec6-172">Konfigurowanie reguł eliminacji</span><span class="sxs-lookup"><span data-stu-id="8bec6-172">Set up elimination rules</span></span>
<span data-ttu-id="8bec6-173">Podczas konfigurowania reguł eliminacji zalecamy utworzenie wymiaru finansowego specjalnie do celów eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-173">When setting up elimination rules, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="8bec6-174">Większość klientów nazywa ten wymiar Partner handlowy lub podobnie.</span><span class="sxs-lookup"><span data-stu-id="8bec6-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="8bec6-175">Jeśli postanowisz nie używać wymiaru finansowego, to upewnij się, że masz konta główne przeznaczone tylko do transakcji międzyfirmowych.</span><span class="sxs-lookup"><span data-stu-id="8bec6-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="8bec6-176">Ta konfiguracja eliminacji znajduje się w obszarze Ustawienia w module Konsolidacje.</span><span class="sxs-lookup"><span data-stu-id="8bec6-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="8bec6-177">Po wprowadzeniu opisu reguły trzeba wybrać firmę, w której arkusza eliminacji będzie księgowany.</span><span class="sxs-lookup"><span data-stu-id="8bec6-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="8bec6-178">Powinna to być firma, która ma wybraną opcję **Użyj na potrzeby procesu eliminacji finansowej** w ustawieniach firmy.</span><span class="sxs-lookup"><span data-stu-id="8bec6-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="8bec6-179">W razie potrzeby można ustawić daty początku i końca obowiązywania reguły eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="8bec6-180">Należy ustawić opcję **Aktywne** na **Tak**, jeśli reguła ma być dostępna w procesie propozycji eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="8bec6-181">Wybierz arkusz, który ma typ **Eliminacja**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="8bec6-182">Po określeniu podstawowych ustawień można zdefiniować faktyczne reguły przetwarzanego przez kliknięcie przycisku **Wiersze**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="8bec6-183">Możliwe są dwie opcje dla eliminacji: eliminowanie kwoty zmiany netto lub definiowanie stałej kwoty.</span><span class="sxs-lookup"><span data-stu-id="8bec6-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="8bec6-184">Wybierz konto źródłowe.</span><span class="sxs-lookup"><span data-stu-id="8bec6-184">Select your source account.</span></span> <span data-ttu-id="8bec6-185">Można użyć gwiazdki (\*) jako symbolu wieloznacznego.</span><span class="sxs-lookup"><span data-stu-id="8bec6-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="8bec6-186">Na przykład wartość 1\* spowodowałaby używanie jako źródła danych alokacji wszystkich kont rozpoczynających się od 1.</span><span class="sxs-lookup"><span data-stu-id="8bec6-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="8bec6-187">Po wybraniu kont źródłowych ustawienie **Specyfikacja konta** określa konto z używanej firmy docelowej.</span><span class="sxs-lookup"><span data-stu-id="8bec6-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="8bec6-188">Wybierz opcję **Źródło**, jeśli chcesz używać tego samego konta głównego zdefiniowanego w ustawieniu **Źródło**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="8bec6-189">Jeśli wybierzesz opcję **Zdefiniowany przez użytkownika**, należy określić konto docelowe.</span><span class="sxs-lookup"><span data-stu-id="8bec6-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="8bec6-190">Specyfikacja wymiaru działa w ten sam sposób.</span><span class="sxs-lookup"><span data-stu-id="8bec6-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="8bec6-191">Jeśli wybierzesz opcję **Źródło**, w firmie docelowej będą używane te same wymiary, jak w firmie źródłowej.</span><span class="sxs-lookup"><span data-stu-id="8bec6-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="8bec6-192">Jeśli wybierzesz opcję **Zdefiniowany przez użytkownika**, będzie trzeba określić wymiary w firmie docelowej, klikając elementu menu **Docelowe wymiary**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="8bec6-193">Wybierz wymiary źródłowe i wymiary finansowe oraz wartości, które będą używane jako źródło eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="8bec6-194">Przetwarzanie transakcje eliminacji</span><span class="sxs-lookup"><span data-stu-id="8bec6-194">Process elimination transactions</span></span>
<span data-ttu-id="8bec6-195">Istnieją dwa sposoby przetwarzania transakcji eliminacji: w procesie konsolidacji online lub poprzez utworzenie arkusza eliminacji i uruchomienie procesu propozycji eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="8bec6-196">W tej sekcji skupiono się na tworzeniu arkusza i wykonywaniu procesu eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="8bec6-197">W firmie zdefiniowanej jako firma eliminacji wybierz opcję **Arkusz eliminacji** w module Konsolidacje.</span><span class="sxs-lookup"><span data-stu-id="8bec6-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="8bec6-198">Po wybraniu arkusza kliknij przycisk **Wiersze**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="8bec6-199">Propozycję można wygenerować, wybierając menu **Propozycje**, a następnie wybierając opcję **Propozycja eliminacji**.</span><span class="sxs-lookup"><span data-stu-id="8bec6-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="8bec6-200">Wybierz firmę będącą źródłem skonsolidowanych danych, a następnie wybierz regułę, którą chcesz przetwarzać.</span><span class="sxs-lookup"><span data-stu-id="8bec6-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="8bec6-201">Wprowadź daty początkową i końcową określające, kiedy ma się zaczynać i kończyć wyszukiwanie kwot eliminacji.</span><span class="sxs-lookup"><span data-stu-id="8bec6-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="8bec6-202">Pole **Data księgowania w księdze głównej** zawiera datę zaksięgowania arkusza w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="8bec6-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="8bec6-203">Po kliknięciu przycisku **OK** można przejrzeć kwoty i zaksięgować arkusz.</span><span class="sxs-lookup"><span data-stu-id="8bec6-203">After you click **OK**, you can review the amounts and post the journal.</span></span>


