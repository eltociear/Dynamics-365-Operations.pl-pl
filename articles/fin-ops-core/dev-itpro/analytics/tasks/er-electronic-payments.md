---
title: ER Generowanie dokumentów elektronicznych dla płatności przy użyciu konfiguracji formatu
description: W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli Administrator systemu lub Deweloper raportowania elektronicznego może używać nowej konfiguracji formatu raportowania elektronicznego (ER) do generowania dokumentów elektronicznych w celu przetwarzania płatności.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184998"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="b1f8f-103">ER Generowanie dokumentów elektronicznych dla płatności przy użyciu konfiguracji formatu</span><span class="sxs-lookup"><span data-stu-id="b1f8f-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1f8f-104">W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli Administrator systemu lub Deweloper raportowania elektronicznego może używać nowej konfiguracji formatu raportowania elektronicznego (ER) do generowania dokumentów elektronicznych w celu przetwarzania płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="b1f8f-105">Kroki można wykonać na danych przykładowej firmy GBSI.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="b1f8f-106">Aby wykonać te kroki, należy najpierw wykonać kroki w procedurze „Tworzenie konfiguracji z formatem dokumentu płatności”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="b1f8f-107">Zmiana konfiguracji metody płatności elektronicznych</span><span class="sxs-lookup"><span data-stu-id="b1f8f-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="b1f8f-108">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia płatności > Metody płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="b1f8f-109">W razie potrzeby przełącz sekcję Format pliku, aby ją rozwinąć.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="b1f8f-110">Skorzystaj z opcji szybkiego filtrowania, aby znaleźć rekordy.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b1f8f-111">Na przykład wyfiltruj według pola Metoda płatności z wartością „Elektroniczne”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="b1f8f-112">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-112">Click Edit.</span></span>
5. <span data-ttu-id="b1f8f-113">W polu Ogólne raportowanie elektroniczne wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="b1f8f-114">Wybierz opcję Tak, aby używać wzorca ogólnego raportowania elektronicznego do generowania plików płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="b1f8f-115">W polu Nazwa kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b1f8f-116">Wybierz konfigurację formatu BACS (fikcyjny brytyjski).</span><span class="sxs-lookup"><span data-stu-id="b1f8f-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="b1f8f-117">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-117">Click Save.</span></span>
9. <span data-ttu-id="b1f8f-118">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="b1f8f-119">Testowanie formatu wygenerowanych plików płatności</span><span class="sxs-lookup"><span data-stu-id="b1f8f-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="b1f8f-120">Wybierz kolejno opcje Rozrachunki z dostawcami > Płatności > Arkusz płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b1f8f-121">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-121">Click New.</span></span>
3. <span data-ttu-id="b1f8f-122">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b1f8f-123">W polu Nazwa kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b1f8f-124">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1f8f-125">Wybierz opcję VendPay.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-125">Select VendPay.</span></span>  
6. <span data-ttu-id="b1f8f-126">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-126">Click Save.</span></span>
7. <span data-ttu-id="b1f8f-127">Kliknij przycisk Wiersze.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-127">Click Lines.</span></span>
8. <span data-ttu-id="b1f8f-128">W polu Firma wpisz wartość „DEMF”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="b1f8f-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="b1f8f-129">DEMF</span></span>  
9. <span data-ttu-id="b1f8f-130">W polu Konto podaj wartości „DE-01001”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="b1f8f-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="b1f8f-131">DE-01001</span></span>  
10. <span data-ttu-id="b1f8f-132">W polu Opis wpisz „Płatność”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="b1f8f-133">Płatność</span><span class="sxs-lookup"><span data-stu-id="b1f8f-133">Payment</span></span>  
11. <span data-ttu-id="b1f8f-134">W polu Debet wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="b1f8f-135">1000</span><span class="sxs-lookup"><span data-stu-id="b1f8f-135">1000</span></span>  
12. <span data-ttu-id="b1f8f-136">Kliknij kartę Płatność.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="b1f8f-137">W polu Metoda płatności kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b1f8f-138">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b1f8f-139">Zaznacz wartość Elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="b1f8f-140">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b1f8f-141">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-141">Click Save.</span></span>
17. <span data-ttu-id="b1f8f-142">Kliknij opcję Generuj płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-142">Click Generate payments.</span></span>
18. <span data-ttu-id="b1f8f-143">W polu Metoda płatności kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b1f8f-144">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b1f8f-145">Zaznacz wartość Elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="b1f8f-146">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1f8f-147">Zaznacz wartość Elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="b1f8f-148">W polu Nazwa pliku wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="b1f8f-149">Na przykład wpisz „płatności”.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="b1f8f-150">W polu Konto bankowe kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="b1f8f-151">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1f8f-152">Zaznacz wartość GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="b1f8f-153">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-153">Click OK.</span></span>
25. <span data-ttu-id="b1f8f-154">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-154">Click OK.</span></span>
    * <span data-ttu-id="b1f8f-155">Przeanalizuj utworzony plik płatności w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="b1f8f-156">Porównaj go z zaprojektowanym układem dokumentu i zdefiniowanymi atrybutami transakcji płatności.</span><span class="sxs-lookup"><span data-stu-id="b1f8f-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  
