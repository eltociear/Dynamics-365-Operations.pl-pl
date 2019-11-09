---
title: Tworzenie pozwolenia na polecenie zapłaty dla odbiorcy
description: W tym przewodniku po zadaniach pokazano, jak utworzyć zgodę na polecenie zapłaty, a następnie używać go na fakturze.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179450"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="c6c22-103">Tworzenie pozwolenia na polecenie zapłaty dla odbiorcy</span><span class="sxs-lookup"><span data-stu-id="c6c22-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6c22-104">W tym przewodniku po zadaniach pokazano, jak utworzyć zgodę na polecenie zapłaty, a następnie używać go na fakturze.</span><span class="sxs-lookup"><span data-stu-id="c6c22-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="c6c22-105">Tworzenie konta bankowego</span><span class="sxs-lookup"><span data-stu-id="c6c22-105">Create a bank account</span></span>
1. <span data-ttu-id="c6c22-106">W **okienku nawigacji** otwórz **Moduły > Rozrachunki z odbiorcami > Odbiorcy > Wszyscy odbiorcy**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="c6c22-107">Na liście wybierz rekord.</span><span class="sxs-lookup"><span data-stu-id="c6c22-107">In the list, select a record.</span></span> <span data-ttu-id="c6c22-108">Na przykład zaznacz US-001.</span><span class="sxs-lookup"><span data-stu-id="c6c22-108">For example, select US-001</span></span>
3. <span data-ttu-id="c6c22-109">W okienku akcji kliknij pozycję **Odbiorca**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="c6c22-110">Kliknij przycisk **konta bankowe**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="c6c22-111">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-111">Click **New**.</span></span>
6. <span data-ttu-id="c6c22-112">W polu **Konto bankowe** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="c6c22-113">W polu **Nazwa** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="c6c22-114">W polu **IBAN** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="c6c22-115">W polu **Waluta** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="c6c22-116">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-116">Click **Save**.</span></span>
11. <span data-ttu-id="c6c22-117">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-117">Close the page.</span></span>
12. <span data-ttu-id="c6c22-118">W **okienkun awigacji** przejdź do **Moduły > Zarządzanie gotówką i bankami > Konta bankowe > Konta bankowe**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="c6c22-119">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="c6c22-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c6c22-120">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="c6c22-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c6c22-121">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-121">Click **Edit**.</span></span>
16. <span data-ttu-id="c6c22-122">Rozwiń kartę skróconą **Dodatkowa identyfikacja**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="c6c22-123">W polu **Identyfikator polecenia zapłaty** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="c6c22-124">W polu **IBAN** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="c6c22-125">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-125">Close the page.</span></span>
20. <span data-ttu-id="c6c22-126">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="c6c22-127">Konfigurowanie elektronicznej metody płatności</span><span class="sxs-lookup"><span data-stu-id="c6c22-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="c6c22-128">W **okienku nawigacji** przejdź do **Moduły > Rozrachunki z odbiorcami > Ustawienia płatności > Metody płatności**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="c6c22-129">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-129">Click **New**.</span></span>
3. <span data-ttu-id="c6c22-130">W polu **Metoda płatności** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="c6c22-131">W polu **Opis** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c6c22-132">W polu **Typ płatności** wybierz opcję „Płatność elektroniczna”.</span><span class="sxs-lookup"><span data-stu-id="c6c22-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="c6c22-133">Typem płatności dla zgody na płacenie poleceniem zapłaty musi być płatność elektroniczna.</span><span class="sxs-lookup"><span data-stu-id="c6c22-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="c6c22-134">W polu **Wymaga zgody** wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="c6c22-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="c6c22-135">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="c6c22-136">Dodawanie zgody na polecenie zapłaty do odbiorcy</span><span class="sxs-lookup"><span data-stu-id="c6c22-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="c6c22-137">W **okienku nawigacji** otwórz **Moduły > Rozrachunki z odbiorcami > Odbiorcy > Wszyscy odbiorcy**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="c6c22-138">Na liście wybierz rekord.</span><span class="sxs-lookup"><span data-stu-id="c6c22-138">In the list, select a record.</span></span> <span data-ttu-id="c6c22-139">Na przykład zaznacz US-001.</span><span class="sxs-lookup"><span data-stu-id="c6c22-139">For example, select US-001</span></span>
3. <span data-ttu-id="c6c22-140">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-140">Click **Edit**.</span></span>
4. <span data-ttu-id="c6c22-141">Rozwiń skróconą kartę **Ustawienia domyślne płatności**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="c6c22-142">W polu **Metoda płatności** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="c6c22-143">Rozwiń skróconą kartę **Ustawienia domyślne płatności**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="c6c22-144">Rozwiń skróconą kartę **Pozwolenia na polecenie zapłaty**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="c6c22-145">Kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-145">Click **Add**.</span></span>
9. <span data-ttu-id="c6c22-146">W polu **Konto bankowe** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="c6c22-147">W polu **Konto bankowe wierzyciela** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="c6c22-148">W polu **Częstość płatności** wprowadź liczbę płatności, jaką oczekujesz przetwarzać w ramach tej zgody.</span><span class="sxs-lookup"><span data-stu-id="c6c22-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="c6c22-149">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-149">Click **OK**.</span></span>
13. <span data-ttu-id="c6c22-150">Kliknij przycisk **Drukuj**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-150">Click **Print**.</span></span>
14. <span data-ttu-id="c6c22-151">Kliknij opcję **Raport dotyczący zgody**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="c6c22-152">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-152">Close the page.</span></span>
16. <span data-ttu-id="c6c22-153">Kliknij przycisk **Edytuj**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-153">Click **Edit**.</span></span>
17. <span data-ttu-id="c6c22-154">W polu **Data podpisania** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="c6c22-155">Kliknij przycisk **Tak**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-155">Click **Yes**.</span></span>
19. <span data-ttu-id="c6c22-156">Wpisz miejsce, w którym zgoda została podpisana.</span><span class="sxs-lookup"><span data-stu-id="c6c22-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="c6c22-157">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-157">Click **OK**.</span></span>
21. <span data-ttu-id="c6c22-158">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="c6c22-159">Tworzenie faktury niezależnej ze zgodą</span><span class="sxs-lookup"><span data-stu-id="c6c22-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="c6c22-160">W **okienku nawigacji** otwórz **Moduły > Rozrachunki z odbiorcami > Faktury > Wszystkie faktury niezależne**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="c6c22-161">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="c6c22-161">Click **New**.</span></span>
3. <span data-ttu-id="c6c22-162">Zaznacz odbiorcę, dla którego dodano zgodę.</span><span class="sxs-lookup"><span data-stu-id="c6c22-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="c6c22-163">W polu **Identyfikator zgody na polecenie zapłaty** wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="c6c22-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>
