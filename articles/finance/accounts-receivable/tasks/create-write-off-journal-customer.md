---
title: Tworzenie arkusza odpisów dla odbiorcy
description: W tym przewodniku po zadaniach zostanie pokazany sposób konfigurowania parametrów odpisów i następnie transakcji odpisu ze stron Windykacja, Otwarte faktury odbiorcy i Odbiorca.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188839"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="c955e-103">Tworzenie arkusza odpisów dla odbiorcy</span><span class="sxs-lookup"><span data-stu-id="c955e-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c955e-104">W tym przewodniku po zadaniach zostanie pokazany sposób konfigurowania parametrów odpisów i następnie transakcji odpisu ze stron Windykacja, Otwarte faktury odbiorcy i Odbiorca.</span><span class="sxs-lookup"><span data-stu-id="c955e-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="c955e-105">W zadaniu wykorzystano firmę demonstracyjną USMF.</span><span class="sxs-lookup"><span data-stu-id="c955e-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="c955e-106">Konfigurowanie parametrów odpisów</span><span class="sxs-lookup"><span data-stu-id="c955e-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="c955e-107">Przejdź do **Okienko nawigacji > Moduły > Kredyty i windykacja > Ustawienia > Parametry modułu rozrachunków z odbiorcami**.</span><span class="sxs-lookup"><span data-stu-id="c955e-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="c955e-108">Kliknij kartę **Windykacja**.</span><span class="sxs-lookup"><span data-stu-id="c955e-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="c955e-109">Rozwiń lub zwiń sekcję **Odpisz**.</span><span class="sxs-lookup"><span data-stu-id="c955e-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="c955e-110">**Arkusz odpisów** jest arkuszem finansowym, który będzie zawierał transakcje odpisu utworzone przez Ciebie.</span><span class="sxs-lookup"><span data-stu-id="c955e-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="c955e-111">Do każdego odpisu można dołączyć kod przyczyny.</span><span class="sxs-lookup"><span data-stu-id="c955e-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="c955e-112">To domyślne ustawienie można zastąpić podczas dokonywania odpisu.</span><span class="sxs-lookup"><span data-stu-id="c955e-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="c955e-113">Ustaw wartość Tak w **Oddziel podatek**, aby w odpisie oddzielić podatek od oryginalnej transakcji.</span><span class="sxs-lookup"><span data-stu-id="c955e-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="c955e-114">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-114">Close the page.</span></span>
5. <span data-ttu-id="c955e-115">Wybierz kolejno opcje **Kredyty i windykacja > Ustawienia > Profile księgowania odbiorców**.</span><span class="sxs-lookup"><span data-stu-id="c955e-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="c955e-116">Konto odpisu będzie używane jako konto wydatków lub rezerwacji korekt w arkuszu finansowym.</span><span class="sxs-lookup"><span data-stu-id="c955e-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="c955e-117">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="c955e-118">Odpisywanie salda odbiorcy ze strony wiekowanych sald</span><span class="sxs-lookup"><span data-stu-id="c955e-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="c955e-119">Wybierz kolejno opcje **Kredyty i windykacja > Windykacja > Wiekowane salda**.</span><span class="sxs-lookup"><span data-stu-id="c955e-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="c955e-120">Zaznacz wiersz odbiorcy, dla którego ma zostać dokonany odpis.</span><span class="sxs-lookup"><span data-stu-id="c955e-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="c955e-121">Na przykład zaznacz wiersz z firmą Birch Company.</span><span class="sxs-lookup"><span data-stu-id="c955e-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="c955e-122">W **okienku akcji** kliknij pozycję **Windykacja**.</span><span class="sxs-lookup"><span data-stu-id="c955e-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="c955e-123">Kliknij opcję **Odpisz**.</span><span class="sxs-lookup"><span data-stu-id="c955e-123">Click **Write off**.</span></span>
5. <span data-ttu-id="c955e-124">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c955e-124">Click **OK**.</span></span>
6. <span data-ttu-id="c955e-125">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-125">Close the page.</span></span>
7. <span data-ttu-id="c955e-126">Otwórz **Okienko nawigacji > Moduły > Księga główna > Wpisy w arkuszu > Arkusze finansowe**.</span><span class="sxs-lookup"><span data-stu-id="c955e-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="c955e-127">Wybierz numer partii arkuszy z arkuszem, który zawiera odpis.</span><span class="sxs-lookup"><span data-stu-id="c955e-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="c955e-128">Jest tworzony jeden wiersz w celu wystornowania salda odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="c955e-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="c955e-129">Jeden lub więcej wierszy jest tworzonych w celu zaksięgowania odpisu na koncie odpisów.</span><span class="sxs-lookup"><span data-stu-id="c955e-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="c955e-130">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-130">Close the page.</span></span>
10. <span data-ttu-id="c955e-131">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="c955e-132">Odpisywanie transakcji z formularza windykacji</span><span class="sxs-lookup"><span data-stu-id="c955e-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="c955e-133">Wybierz kolejno opcje **Kredyty i windykacja > Windykacja > Wiekowane salda**.</span><span class="sxs-lookup"><span data-stu-id="c955e-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="c955e-134">Zaznacz nazwę odbiorcy mającego transakcje, które chcesz odpisać.</span><span class="sxs-lookup"><span data-stu-id="c955e-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="c955e-135">Na przykład wybierz Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="c955e-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="c955e-136">Zaznacz wiersz pierwszej transakcji.</span><span class="sxs-lookup"><span data-stu-id="c955e-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="c955e-137">Zaznacz wiersz drugiej transakcji.</span><span class="sxs-lookup"><span data-stu-id="c955e-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="c955e-138">Kliknij opcję **Odpisz**.</span><span class="sxs-lookup"><span data-stu-id="c955e-138">Click **Write off**.</span></span>
6. <span data-ttu-id="c955e-139">W polu **Komentarz dotyczący przyczyny** wpisz „Prawdopodobnie nieściągalne długi”.</span><span class="sxs-lookup"><span data-stu-id="c955e-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="c955e-140">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c955e-140">Click **OK**.</span></span>
8. <span data-ttu-id="c955e-141">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-141">Close the page.</span></span>
9. <span data-ttu-id="c955e-142">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-142">Close the page.</span></span>
10. <span data-ttu-id="c955e-143">Wybierz kolejno opcje **Księga główna > Wpisy w arkuszu > Arkusze finansowe**.</span><span class="sxs-lookup"><span data-stu-id="c955e-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="c955e-144">Wybierz numer partii arkuszy z arkuszem, który zawiera odpis.</span><span class="sxs-lookup"><span data-stu-id="c955e-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="c955e-145">Jest tworzony jeden wiersz w celu wystornowania salda odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="c955e-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="c955e-146">Jeden lub więcej wierszy jest tworzonych w celu zaksięgowania odpisu na koncie odpisów.</span><span class="sxs-lookup"><span data-stu-id="c955e-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="c955e-147">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-147">Close the page.</span></span>
13. <span data-ttu-id="c955e-148">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="c955e-149">Odpisywanie faktury ze strony Otwarte faktury odbiorców</span><span class="sxs-lookup"><span data-stu-id="c955e-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="c955e-150">W okienku nawigacji otwórz **Moduły > Rozrachunki z odbiorcami > Faktury > Otwarte faktury dla odbiorców**.</span><span class="sxs-lookup"><span data-stu-id="c955e-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="c955e-151">Zaznacz wiersz faktury.</span><span class="sxs-lookup"><span data-stu-id="c955e-151">Mark the line for an invoice.</span></span> <span data-ttu-id="c955e-152">Na przykład zaznacz wiersz faktury CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="c955e-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="c955e-153">W **okienku akcji** kliknij pozycję **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c955e-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="c955e-154">Kliknij opcję **Odpisz**.</span><span class="sxs-lookup"><span data-stu-id="c955e-154">Click **Write off**.</span></span>
5. <span data-ttu-id="c955e-155">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c955e-155">Click **OK**.</span></span>
6. <span data-ttu-id="c955e-156">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="c955e-157">Odpisywanie salda odbiorcy ze strony odbiorcy</span><span class="sxs-lookup"><span data-stu-id="c955e-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="c955e-158">Wybierz kolejno opcje **Rozrachunki z odbiorcami > Odbiorcy > Wszyscy odbiorcy**.</span><span class="sxs-lookup"><span data-stu-id="c955e-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="c955e-159">Umożliwia wybór konta odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="c955e-159">Select a customer account.</span></span> <span data-ttu-id="c955e-160">Wybierz na przykład US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="c955e-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="c955e-161">W **okienku akcji** kliknij pozycję **Windykacja**.</span><span class="sxs-lookup"><span data-stu-id="c955e-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="c955e-162">Kliknij opcję **Odpisz**.</span><span class="sxs-lookup"><span data-stu-id="c955e-162">Click **Write off**.</span></span>
5. <span data-ttu-id="c955e-163">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c955e-163">Click **OK**.</span></span>
6. <span data-ttu-id="c955e-164">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c955e-164">Close the page.</span></span>
