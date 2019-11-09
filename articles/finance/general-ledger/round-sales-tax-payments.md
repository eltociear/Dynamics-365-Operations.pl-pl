---
title: Reguły płatności podatkowych i zaokrąglania
description: W tym artykule wyjaśniono działanie konfiguracji reguły zaokrąglania w ustawieniach urzędu skarbowego oraz sposób zaokrąglania salda podatku podczas zadania rozliczania i księgowania podatku.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186332"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="6e883-103">Reguły płatności podatkowych i zaokrąglania</span><span class="sxs-lookup"><span data-stu-id="6e883-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e883-104">W tym artykule wyjaśniono działanie konfiguracji reguły zaokrąglania w ustawieniach urzędu skarbowego oraz sposób zaokrąglania salda podatku podczas zadania rozliczania i księgowania podatku.</span><span class="sxs-lookup"><span data-stu-id="6e883-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="6e883-105">Okresowo należy zgłaszać i płacić podatek w urzędzie skarbowym.</span><span class="sxs-lookup"><span data-stu-id="6e883-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="6e883-106">Można to zrobić, uruchamiając proces rozliczenia i księgowania podatku na stronie Podatek.</span><span class="sxs-lookup"><span data-stu-id="6e883-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="6e883-107">Podatek od sprzedaży w danym okresie zostanie rozliczony dla kont podatku, a saldo podatku zostanie zaksięgowane na koncie rozliczenia podatku.</span><span class="sxs-lookup"><span data-stu-id="6e883-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="6e883-108">Saldo podatku, który jest księgowany na koncie rozliczenie podatku, może być zaokrąglane zgodnie z wymogami urzędu skarbowego przez skonfigurowanie reguły zaokrąglania na stronie podatku od sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="6e883-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="6e883-109">Różnica wynikająca z zaokrąglenia jest księgowana na koncie zaokrąglania podatku wybranym w polu Konta do transakcji automatycznych w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="6e883-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="6e883-110">Poniższy przykład pokazuje mechanizm działania reguły zaokrąglania na potrzeby urzędu skarbowego.</span><span class="sxs-lookup"><span data-stu-id="6e883-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="6e883-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e883-111">Examples</span></span>

<span data-ttu-id="6e883-112">Łączny podatek za okres zawiera saldo faktury w wysokości -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="6e883-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="6e883-113">Podmiot prawny zebrał więcej podatku, niż zapłacił.</span><span class="sxs-lookup"><span data-stu-id="6e883-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="6e883-114">Z tego względu firma jest winna pieniądze urzędowi skarbowemu.</span><span class="sxs-lookup"><span data-stu-id="6e883-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="6e883-115">Firma chce użyć metody zaokrąglania, która zaokrągla saldo do najbliższego 1,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="6e883-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="6e883-116">Użytkownik odpowiedzialny za księgowanie podatku musi wykonać następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="6e883-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="6e883-117">Wybierz kolejno opcje Podatek &gt; Podatki pośrednie &gt; Podatek &gt; Urzędy skarbowe.</span><span class="sxs-lookup"><span data-stu-id="6e883-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="6e883-118">Na skróconej karcie Ogólne zaznacz opcję Normalne w polu Metoda zaokrąglenia.</span><span class="sxs-lookup"><span data-stu-id="6e883-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="6e883-119">W polu Zaokrąglenie wpisz 1,00.</span><span class="sxs-lookup"><span data-stu-id="6e883-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="6e883-120">Gdy przyjdzie czas zapłacenia podatku urzędowi skarbowemu, otwórz stronę Rozlicz i zaksięguj podatek.</span><span class="sxs-lookup"><span data-stu-id="6e883-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="6e883-121">(Wybierz kolejno opcje Podatek &gt; Deklaracje &gt; Podatek &gt; Rozlicz i zaksięguj podatek).</span><span class="sxs-lookup"><span data-stu-id="6e883-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="6e883-122">Na koncie rozliczenie podatku kwota zobowiązań z tytułu podatku 98 765,43 jest zaokrąglana do 98 765.</span><span class="sxs-lookup"><span data-stu-id="6e883-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="6e883-123">W poniższej tabeli przedstawiono, jak kwota 98 765,43 jest zaokrąglana przy użyciu każdej metody zaokrąglania, która jest dostępna w polu Metoda zaokrąglania na stronie urzędu skarbowego.</span><span class="sxs-lookup"><span data-stu-id="6e883-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="6e883-124">Zaokrąglanie z opcji</span><span class="sxs-lookup"><span data-stu-id="6e883-124">Rounding form option</span></span>                | <span data-ttu-id="6e883-125">Wartość zaokrąglenia = 0,01</span><span class="sxs-lookup"><span data-stu-id="6e883-125">Round-off value = 0.01</span></span> | <span data-ttu-id="6e883-126">Wartość zaokrąglenia = 0,10</span><span class="sxs-lookup"><span data-stu-id="6e883-126">Round-off value = 0.10</span></span> | <span data-ttu-id="6e883-127">Wartość zaokrąglenia = 1,00</span><span class="sxs-lookup"><span data-stu-id="6e883-127">Round-off value = 1.00</span></span> | <span data-ttu-id="6e883-128">Wartość zaokrąglenia = 100,00</span><span class="sxs-lookup"><span data-stu-id="6e883-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="6e883-129">Normalna</span><span class="sxs-lookup"><span data-stu-id="6e883-129">Normal</span></span>                              | <span data-ttu-id="6e883-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="6e883-130">98,765.43</span></span>              | <span data-ttu-id="6e883-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="6e883-131">98,765.40</span></span>              | <span data-ttu-id="6e883-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="6e883-132">98,765.00</span></span>              | <span data-ttu-id="6e883-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="6e883-133">98,800.00</span></span>                |
| <span data-ttu-id="6e883-134">W dół</span><span class="sxs-lookup"><span data-stu-id="6e883-134">Downward</span></span>                            | <span data-ttu-id="6e883-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="6e883-135">98,765.43</span></span>              | <span data-ttu-id="6e883-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="6e883-136">98,765.40</span></span>              | <span data-ttu-id="6e883-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="6e883-137">98,765.00</span></span>              | <span data-ttu-id="6e883-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="6e883-138">98,700.00</span></span>                |
| <span data-ttu-id="6e883-139">Zaokrąglenie w górę</span><span class="sxs-lookup"><span data-stu-id="6e883-139">Rounding-up</span></span>                         | <span data-ttu-id="6e883-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="6e883-140">98,765.43</span></span>              | <span data-ttu-id="6e883-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="6e883-141">98,765.50</span></span>              | <span data-ttu-id="6e883-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="6e883-142">98,766.00</span></span>              | <span data-ttu-id="6e883-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="6e883-143">98,800.00</span></span>                |
| <span data-ttu-id="6e883-144">Na korzyść firmy, salda kredytowe</span><span class="sxs-lookup"><span data-stu-id="6e883-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="6e883-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="6e883-145">98,765.43</span></span>              | <span data-ttu-id="6e883-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="6e883-146">98,765.40</span></span>              | <span data-ttu-id="6e883-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="6e883-147">98,765.00</span></span>              | <span data-ttu-id="6e883-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="6e883-148">98,700.00</span></span>                |
| <span data-ttu-id="6e883-149">Na korzyść firmy, salda debetowe</span><span class="sxs-lookup"><span data-stu-id="6e883-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="6e883-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="6e883-150">98,765.43</span></span>              | <span data-ttu-id="6e883-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="6e883-151">98,765.50</span></span>              | <span data-ttu-id="6e883-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="6e883-152">98,766.00</span></span>              | <span data-ttu-id="6e883-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="6e883-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="6e883-154">Brak zaokrąglania, ponieważ zaokrąglenie wynosi 0,00</span><span class="sxs-lookup"><span data-stu-id="6e883-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="6e883-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span><span class="sxs-lookup"><span data-stu-id="6e883-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="6e883-156">Normalne zaokrąglenie i normalna dokładność wynoszą 0,01</span><span class="sxs-lookup"><span data-stu-id="6e883-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="6e883-157">Zaokrąglanie</span><span class="sxs-lookup"><span data-stu-id="6e883-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="6e883-158">Procedury obliczania</span><span class="sxs-lookup"><span data-stu-id="6e883-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6e883-159">round(1.015, 0.01) = 1.02</span><span class="sxs-lookup"><span data-stu-id="6e883-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="6e883-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="6e883-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="6e883-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="6e883-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6e883-162">round(1.014, 0.01) = 1.01</span><span class="sxs-lookup"><span data-stu-id="6e883-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6e883-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="6e883-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="6e883-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="6e883-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6e883-165">round(1.011, 0.02) = 1.02</span><span class="sxs-lookup"><span data-stu-id="6e883-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6e883-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="6e883-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="6e883-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="6e883-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="6e883-168">round(1.009, 0.02) = 1.00</span><span class="sxs-lookup"><span data-stu-id="6e883-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="6e883-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="6e883-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="6e883-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="6e883-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="6e883-171">Jeśli wybierzesz Na korzyść firmy, zaokrąglanie jest zawsze na korzyść firmy.</span><span class="sxs-lookup"><span data-stu-id="6e883-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="6e883-172">Aby uzyskać więcej informacji, zobacz następujące tematy:</span><span class="sxs-lookup"><span data-stu-id="6e883-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="6e883-173">Omówienie podatku</span><span class="sxs-lookup"><span data-stu-id="6e883-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="6e883-174">Tworzenie płatności podatku</span><span class="sxs-lookup"><span data-stu-id="6e883-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="6e883-175">Tworzenie transakcji sprzedaży w dokumentach</span><span class="sxs-lookup"><span data-stu-id="6e883-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="6e883-176">Wyświetlanie zaksięgowanych transakcji podatkowych</span><span class="sxs-lookup"><span data-stu-id="6e883-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="6e883-177">Funkcja zaokrąglanie</span><span class="sxs-lookup"><span data-stu-id="6e883-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)

