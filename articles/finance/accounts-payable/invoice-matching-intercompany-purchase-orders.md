---
title: Uzgadnianie faktur i międzyfirmowe zamówienia zakupu
description: Firmę kupującą, która uczestniczy w transakcjach handlu międzyfirmowego, można skonfigurować tak, aby używała uzgadniania faktur w rozrachunkach z dostawcami. W takim przypadku muszą być spełnione równocześnie wymagania dotyczące księgowania dla handlu międzyfirmowego i uzgadniania faktur w rozrachunkach z dostawcami, aby było można zaksięgować faktury od dostawcy międzyfirmowego.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aaa4a08f65e4a3452782cf2b928464dff27ed59b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189667"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a><span data-ttu-id="889c7-104">Uzgadnianie faktur i międzyfirmowe zamówienia zakupu</span><span class="sxs-lookup"><span data-stu-id="889c7-104">Invoice matching and intercompany purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="889c7-105">Firmę kupującą, która uczestniczy w transakcjach handlu międzyfirmowego, można skonfigurować tak, aby używała uzgadniania faktur w rozrachunkach z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="889c7-105">The purchasing legal entity that is involved in an intercompany trade transaction might be set up to use accounts payable invoice matching.</span></span> <span data-ttu-id="889c7-106">Gdy pole **Księguj fakturę z rozbieżnościami** w formularzu **Parametry modułu rozrachunków z dostawcami** jest ustawione na**Wymagaj zatwierdzania**, zostanie przeprowadzona weryfikacja uzgadniania faktur.</span><span class="sxs-lookup"><span data-stu-id="889c7-106">When the **Post invoice with discrepancies** field in the **Accounts payable parameters** form is set to **Require approval**, invoice matching validation will be performed.</span></span> <span data-ttu-id="889c7-107">W takim przypadku muszą być spełnione równocześnie wymagania dotyczące księgowania dla handlu międzyfirmowego i uzgadniania faktur w rozrachunkach z dostawcami, aby było można zaksięgować faktury od dostawcy międzyfirmowego.</span><span class="sxs-lookup"><span data-stu-id="889c7-107">In this case, the posting requirements for both intercompany trade and accounts payable invoice matching must be met before intercompany vendor invoices can be posted.</span></span>

<span data-ttu-id="889c7-108">Przykłady w tym temacie używają następującej konfiguracji handlu międzyfirmowego:</span><span class="sxs-lookup"><span data-stu-id="889c7-108">The examples in this topic use the following setup for intercompany trade:</span></span>
-   <span data-ttu-id="889c7-109">Fabrikam-Zakup jest firmą kupującą.</span><span class="sxs-lookup"><span data-stu-id="889c7-109">Fabrikam Purchase is the purchasing legal entity.</span></span>
-   <span data-ttu-id="889c7-110">Fabrikam-Sprzedaż jest firmą sprzedającą.</span><span class="sxs-lookup"><span data-stu-id="889c7-110">Fabrikam Sales is the selling legal entity.</span></span>
-   <span data-ttu-id="889c7-111">Odbiorca 4020 jest zarejestrowany w firmie Fabrikam-Sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="889c7-111">Customer 4020 exists in Fabrikam Sales.</span></span>
-   <span data-ttu-id="889c7-112">Dostawca 3024 jest zarejestrowany w firmie Fabrikam-Zakup.</span><span class="sxs-lookup"><span data-stu-id="889c7-112">Vendor 3024 exists in Fabrikam Purchase.</span></span>
-   <span data-ttu-id="889c7-113">W firmie Fabrikam-Zakup określono informacje międzyfirmowe dla dostawcy 3024.</span><span class="sxs-lookup"><span data-stu-id="889c7-113">In Fabrikam Purchase, intercompany information is specified for vendor 3024.</span></span> <span data-ttu-id="889c7-114">Firma Fabrikam-Sprzedaż jest określona jako odbiorca, a odbiorca 4020 jest określony jako konto odbiorcy odpowiadająca firmie Fabrikam-Zakup.</span><span class="sxs-lookup"><span data-stu-id="889c7-114">Fabrikam Sales is specified as the customer company, and customer 4020 is specified as the customer account that corresponds to the Fabrikam Purchase legal entity.</span></span>
-   <span data-ttu-id="889c7-115">W firmie Fabrikam-Sprzedaż określono informacje międzyfirmowe dla odbiorcy 4020.</span><span class="sxs-lookup"><span data-stu-id="889c7-115">In Fabrikam Sales, intercompany information is specified for customer 4020.</span></span> <span data-ttu-id="889c7-116">Firma Fabrikam-Zakup jest określona jako odbiorca, a dostawca 3024 jest określony jako konto dostawcy odpowiadające firmie Fabrikam-Sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="889c7-116">Fabrikam Purchase is specified as the vendor company, and vendor 3024 is specified as the vendor account that corresponds to the Fabrikam Sales legal entity.</span></span>

<span data-ttu-id="889c7-117">W poniższych przykładach zastosowano następujące ustawienia dotyczące uzgadniania faktur od dostawców dla firmy Fabrikam-Zakup:</span><span class="sxs-lookup"><span data-stu-id="889c7-117">The examples use the following setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="889c7-118">Na stronie Parametry modułu rozrachunków z dostawcami wybrana jest opcja Włącz weryfikację uzgadniania faktur.</span><span class="sxs-lookup"><span data-stu-id="889c7-118">On the Accounts payable parameters page, the Enable invoice matching validation option is selected.</span></span>
-   <span data-ttu-id="889c7-119">Na stronie Parametry modułu rozrachunków z dostawcami pole Księguj fakturę z rozbieżnościami ma wartość Wymagaj zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="889c7-119">On the Accounts payable parameters page, the Post invoice with discrepancies field is set to Require approval.</span></span>
-   <span data-ttu-id="889c7-120">Wartość procentowa ceny jednostkowej dla firmy wynosi 2 procent.</span><span class="sxs-lookup"><span data-stu-id="889c7-120">The price tolerance percentage for the legal entity is 2 percent.</span></span>

## <a name="example-price-matching-and-intercompany-trade"></a><span data-ttu-id="889c7-121"> Przykład: Uzgadnianie cen i handel międzyfirmowy</span><span class="sxs-lookup"><span data-stu-id="889c7-121">Example: Price matching and intercompany trade</span></span>
<span data-ttu-id="889c7-122">Kwoty netto dla faktury z międzyfirmowej faktury od dostawcy i międzyfirmowej faktury dla odbiorcy muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="889c7-122">The net amounts for the intercompany vendor invoice and the intercompany customer invoice must be equal.</span></span> <span data-ttu-id="889c7-123">Wymaganie to ma charakter nadrzędny wobec wszelkich dozwolonych możliwości dokonywania akceptacji lub wartości procentowych rozbieżności cen w procesie uzgadniania faktur.</span><span class="sxs-lookup"><span data-stu-id="889c7-123">This requirement overrides any invoice matching approvals or price tolerance percentages that apply.</span></span> <span data-ttu-id="889c7-124">Można na przykład wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="889c7-124">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="889c7-125">W firmie Fabrikam-Zakup utwórz zamówienie sprzedaży ZS888 dla odbiorcy 4020.</span><span class="sxs-lookup"><span data-stu-id="889c7-125">In Fabrikam Purchase, create sales order SO888 for customer 4020.</span></span> <span data-ttu-id="889c7-126">Międzyfirmowe zamówienia zakupu MZZ222 jest tworzone automatycznie dla dostawcy 3024 w firmie Fabrikam-Zakup, a międzyfirmowe zamówienie sprzedaży MZS888 jest automatycznie tworzone w firmie Fabrikam-Sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="889c7-126">Intercompany purchase order ICPO222 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO888 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="889c7-127">W Fabrikam-Sprzedaż zarejestruj, że towary zostały otrzymane i zaksięguj dokument dostawy.</span><span class="sxs-lookup"><span data-stu-id="889c7-127">In Fabrikam Sales, register that the items have been received, and post a packing slip.</span></span> <span data-ttu-id="889c7-128">Stan dokumentu MZS888 zostaje zmieniony na Dostarczone.</span><span class="sxs-lookup"><span data-stu-id="889c7-128">The status of ICSO888 changes to Delivered.</span></span> <span data-ttu-id="889c7-129">Stan dokumentu MZZ222 zostaje zmieniony na Otrzymane.</span><span class="sxs-lookup"><span data-stu-id="889c7-129">The status of ICPO222 changes to Received.</span></span>
3.  <span data-ttu-id="889c7-130">W Fabrikam-Sprzedaż wykonaj aktualizację faktury dla MZS888.</span><span class="sxs-lookup"><span data-stu-id="889c7-130">In Fabrikam Sales, perform an invoice update for ICSO888.</span></span> <span data-ttu-id="889c7-131">Cena jednostkowa wynosi 0,45 i aktualizowanych jest 100 jednostek.</span><span class="sxs-lookup"><span data-stu-id="889c7-131">The unit price is 0.45, and 100 items are updated.</span></span>
4.  <span data-ttu-id="889c7-132">W firmie Fabrikam-Zakup utwórz fakturę dla MZZ222.</span><span class="sxs-lookup"><span data-stu-id="889c7-132">In Fabrikam Purchase, create an invoice for ICPO222.</span></span> <span data-ttu-id="889c7-133">Przypadkowo zmieniasz cenę netto z 45,00 na 54,00.</span><span class="sxs-lookup"><span data-stu-id="889c7-133">You accidentally change the net price from 45.00 to 54.00.</span></span> <span data-ttu-id="889c7-134">Pojawia się ikona wskazująca, że cena przekracza dozwoloną wartość procentową rozbieżności cen (dozwolona rozbieżność to 2%).</span><span class="sxs-lookup"><span data-stu-id="889c7-134">An icon is displayed to indicate that the price exceeds the allowable price tolerance of 2 percent.</span></span>
5.  <span data-ttu-id="889c7-135">Na stronie Szczegóły uzgadniania faktur zaznacz opcję zatwierdzania księgowania z rozbieżnościami w uzgadnianiu.</span><span class="sxs-lookup"><span data-stu-id="889c7-135">On the Invoice matching details page, select the option to approve posting with matching discrepancies.</span></span> <span data-ttu-id="889c7-136">Na stronie Faktura dostawcy kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="889c7-136">On the Vendor invoice page, click OK.</span></span> <span data-ttu-id="889c7-137">Jeśli faktura od dostawcy nie była międzyfirmową fakturą od dostawcy, księgowanie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="889c7-137">If the vendor invoice was not an intercompany vendor invoice, posting would be successful.</span></span> <span data-ttu-id="889c7-138">Ponieważ jednak chodzi o międzyfirmową fakturę od dostawcy księgowanie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="889c7-138">However, because you are working with an intercompany vendor invoice, posting is unsuccessful.</span></span> <span data-ttu-id="889c7-139">W handlu międzyfirmowym sumy faktur międzyfirmowych na międzyfirmowym zamówieniu sprzedaży muszą być równe z sumami na odpowiednim międzyfirmowym zamówieniu zakupu.</span><span class="sxs-lookup"><span data-stu-id="889c7-139">For intercompany trade, the invoice totals on the intercompany sales order must equal the invoice totals on the corresponding intercompany purchase order.</span></span> <span data-ttu-id="889c7-140">Aby rozwiązać ten problem, popraw cenę netto na fakturze z powrotem na wartość domyślną 45,00.</span><span class="sxs-lookup"><span data-stu-id="889c7-140">To resolve this issue, you must correct the net price on the invoice by changing the net price back to the default amount, 45.00.</span></span>

## <a name="example-quantity-matching-with-intercompany-trade"></a><span data-ttu-id="889c7-141"> Przykład: Uzgadnianie ilości w handlu międzyfirmowym.</span><span class="sxs-lookup"><span data-stu-id="889c7-141">Example: Quantity matching with intercompany trade</span></span>
<span data-ttu-id="889c7-142">Ilości na międzyfirmowym zamówieniu zakupu i międzyfirmowym zamówieniu sprzedaży muszą być równe.</span><span class="sxs-lookup"><span data-stu-id="889c7-142">The quantities on the intercompany purchase order and the intercompany sales order must be equal.</span></span> <span data-ttu-id="889c7-143">Wymaganie to ma charakter nadrzędny wobec wszelkich dozwolonych możliwości dokonywania akceptacji.</span><span class="sxs-lookup"><span data-stu-id="889c7-143">This requirement overrides any invoice matching approvals that apply.</span></span> <span data-ttu-id="889c7-144">W poniższym przykładzie zastosowano następującą konfigurację dla handlu międzyfirmowego:</span><span class="sxs-lookup"><span data-stu-id="889c7-144">This example uses the following additional setup for intercompany trade:</span></span>
-   <span data-ttu-id="889c7-145">W firmie Fabrikam-Zakup zasada działania w przypadku zamówienia zakupu dla dostawcy 3024 została ustawiona na automatyczne księgowanie zarówno oryginalnej faktury dla odbiorcy, jak i międzyfirmowej faktury od dostawcy.</span><span class="sxs-lookup"><span data-stu-id="889c7-145">In Fabrikam Purchase, the purchase order action policy for vendor 3024 is set up to automatically post both the original customer invoice and the intercompany vendor invoice.</span></span>

<span data-ttu-id="889c7-146">W poniższym przykładzie zastosowano następujące dodatkowe ustawienia dotyczące uzgadniania faktur od dostawców dla firmy Fabrikam-Zakup:</span><span class="sxs-lookup"><span data-stu-id="889c7-146">This example uses the following additional setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="889c7-147">Na stronie Grupy modeli pozycji dla grupy modeli, która jest używana przez artykuł B-R14 wybrana jest opcja Wymagania dotyczące przyjęcia.</span><span class="sxs-lookup"><span data-stu-id="889c7-147">On the Item model groups page for the model group that is used by item B-R14, the Receiving requirements option is selected.</span></span>
-   <span data-ttu-id="889c7-148">Dostępna ilość artykułu B-R14 wynosi 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="889c7-148">The on-hand quantity for item B-R14 is 0 (zero).</span></span>

<span data-ttu-id="889c7-149">Można na przykład wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="889c7-149">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="889c7-150">W firmie Fabrikam-Zakup utwórz zamówienie sprzedaży ZS999 dla odbiorcy 4020.</span><span class="sxs-lookup"><span data-stu-id="889c7-150">In Fabrikam Purchase, create sales order SO999 for customer 4020.</span></span> <span data-ttu-id="889c7-151">Zamówienie zawiera jedną pozycję: 100 baterii (artykuł B-R14) po cenie jednostkowej 1,00.</span><span class="sxs-lookup"><span data-stu-id="889c7-151">The order contains one line item: 100 batteries (item B-R14) at a unit price of 1.00 each.</span></span> <span data-ttu-id="889c7-152">W firmie Fabrikam-Zakup zostaje automatycznie utworzone międzyfirmowe zamówienie zakupu MZZ333 dla dostawcy 3024, a w firmie Fabrikam-Sprzedaż zostaje automatycznie utworzone międzyfirmowe zamówienie sprzedaży MSZ999.</span><span class="sxs-lookup"><span data-stu-id="889c7-152">Intercompany purchase order ICPO333 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO999 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="889c7-153">W firmie Fabrikam-Sprzedaż dokonaj procedury aktualizacji faktury z MZS999.</span><span class="sxs-lookup"><span data-stu-id="889c7-153">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="889c7-154">Księgowanie nie powiodło się, ponieważ artykuł jest niedostępny w magazynie i nie został jeszcze odebrany.</span><span class="sxs-lookup"><span data-stu-id="889c7-154">Posting is unsuccessful, because the item is out of stock and has not yet been received.</span></span> <span data-ttu-id="889c7-155">Dlatego nie da się zaktualizować informacji finansowych.</span><span class="sxs-lookup"><span data-stu-id="889c7-155">Therefore, the financial information cannot be updated.</span></span>
3.  <span data-ttu-id="889c7-156">W firmie Fabrikam-Sprzedaż zarejestruj odebranie towarów i zaksięguj dokument dostawy dla MZS99.</span><span class="sxs-lookup"><span data-stu-id="889c7-156">In Fabrikam Sales, register that the items have been received, and post a packing slip for ICSO999.</span></span> <span data-ttu-id="889c7-157">Dokument przyjęcia produktów dla MZZ333 jest automatycznie księgowany w firmie Fabrikam-Zakup.</span><span class="sxs-lookup"><span data-stu-id="889c7-157">A product receipt for ICPO333 is automatically posted in Fabrikam Purchase.</span></span> <span data-ttu-id="889c7-158">W firmie Fabrikam-Zakup odebrana ilość artykułu B-R14 zostaje zmieniona na 100.</span><span class="sxs-lookup"><span data-stu-id="889c7-158">In Fabrikam Purchase, the received quantity for item B-R14 changes to 100.</span></span>
4.  <span data-ttu-id="889c7-159">W firmie Fabrikam-Sprzedaż dokonaj procedury aktualizacji faktury z MZS999.</span><span class="sxs-lookup"><span data-stu-id="889c7-159">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="889c7-160">Księgowanie powiedzie się w obu podmiotach prawnych.</span><span class="sxs-lookup"><span data-stu-id="889c7-160">Posting is successful in both legal entities.</span></span> <span data-ttu-id="889c7-161">W firmie Fabrikam-Zakup kupowana ilość artykułu B-R14 zmienia się na 100. </span><span class="sxs-lookup"><span data-stu-id="889c7-161">In Fabrikam Purchase, the quantity that is purchased for item B-R14 changes to 100.</span></span>




