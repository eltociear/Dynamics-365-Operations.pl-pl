---
title: Tworzenie szablonu faktury niezależnej
description: W tej procedurze przedstawiono tworzenie szablonu faktury niezależnej.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8281de3cb336d9392a6a97f98e51a2a139a384c5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189138"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="3b80b-103">Tworzenie szablonu faktury niezależnej</span><span class="sxs-lookup"><span data-stu-id="3b80b-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b80b-104">Ten przewodnik wykorzystuje firmę demonstracyjną USMF.</span><span class="sxs-lookup"><span data-stu-id="3b80b-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="3b80b-105">Ta procedura jest przeznaczona dla użytkownika, który odpowiada za zarządzanie i przetwarzanie faktur dla odbiorców.</span><span class="sxs-lookup"><span data-stu-id="3b80b-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="3b80b-106">Utwórz szablon</span><span class="sxs-lookup"><span data-stu-id="3b80b-106">Create a template</span></span>

1. <span data-ttu-id="3b80b-107">Wybierz kolejno opcje Rozrachunki z odbiorcami > Faktury > Faktury cykliczne > Szablon faktury niezależnej.</span><span class="sxs-lookup"><span data-stu-id="3b80b-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="3b80b-108">Ten formularz służy do tworzenia szablonów faktur niezależnych, które mogą zawierać wiersze faktur, opłaty, szablon zasad podziału księgowań oraz informacje o koncie księgowym.</span><span class="sxs-lookup"><span data-stu-id="3b80b-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="3b80b-109">Kliknij przycisk „Nowy”, aby utworzyć nowy szablon faktury niezależnej.</span><span class="sxs-lookup"><span data-stu-id="3b80b-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="3b80b-110">W polu Nazwa szablonu wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="3b80b-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="3b80b-111">Pole „Nazwa szablonu” w sposób unikatowy identyfikuje szablon faktury niezależnej.</span><span class="sxs-lookup"><span data-stu-id="3b80b-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="3b80b-112">Żadne dwa szablony nie mogą mieć takiej samej wartości „Nazwa szablonu”.</span><span class="sxs-lookup"><span data-stu-id="3b80b-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="3b80b-113">W polu Opis wprowadź opis szablonu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="3b80b-114">Rozwiń kartę Wiersze faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="3b80b-115">W polu Opis wprowadź opis wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="3b80b-116">W polu Konto główne wybierz konto przychodów.</span><span class="sxs-lookup"><span data-stu-id="3b80b-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="3b80b-117">Na stronie Profile księgowania odbiorców można wybrać konto transakcji przeciwstawnej dla księgowania łącznej kwoty faktury po stronie kredytowej odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="3b80b-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="3b80b-118">W polu Grupa podatków kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="3b80b-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3b80b-119">Grupa podatków dla bieżącego wiersza faktury jest domyślną grupą podatków dla konta odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="3b80b-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="3b80b-120">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3b80b-121">W polu Grupa podatków dla towaru wybierz grupę podatków od towaru dla bieżącego wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="3b80b-122">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3b80b-123">W polu Cena jednostkowa wpisz lub wyświetl cenę za jednostkę towaru w wierszu faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="3b80b-124">Ta kwota jest mnożona przez wartość w polu Ilość w celu ustalenia kwoty wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="3b80b-125">Dodaj nowy wiersz do szablonu faktury niezależnej.</span><span class="sxs-lookup"><span data-stu-id="3b80b-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="3b80b-126">W polu Opis wprowadź opis wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="3b80b-127">W polu Konto główne wybierz konto przychodów.</span><span class="sxs-lookup"><span data-stu-id="3b80b-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="3b80b-128">Na stronie Profile księgowania odbiorców można wybrać konto transakcji przeciwstawnej dla księgowania łącznej kwoty faktury po stronie kredytowej odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="3b80b-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="3b80b-129">W polu Grupa podatków kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="3b80b-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3b80b-130">Grupa podatków dla bieżącego wiersza faktury jest domyślną grupą podatków dla konta odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="3b80b-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="3b80b-131">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="3b80b-132">W polu Grupa podatków dla towaru kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="3b80b-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3b80b-133">Grupa podatków dla towaru dla bieżącego wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="3b80b-134">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="3b80b-135">Wprowadź lub wyświetl liczbę jednostek w wierszu faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="3b80b-136">Ta liczba jest mnożona przez wartość w polu Cena jednostkowa w celu ustalenia kwoty wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="3b80b-137">Wprowadź lub wyświetl cenę jednostkową dla wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="3b80b-138">Ta kwota jest mnożona przez wartość w polu Ilość w celu ustalenia kwoty wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="3b80b-139">Wyświetl i zmodyfikuj zasady podziału księgowań dla określonego wiersza i jego wierszy podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="3b80b-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="3b80b-140">Zasady podziału księgowań określają sposób księgowania kwot, czyli przychodów, podatków lub opłat, na fakturze niezależnej.</span><span class="sxs-lookup"><span data-stu-id="3b80b-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="3b80b-141">Zaktualizuj zasady podziału księgowań dla wybranego wiersza faktury.</span><span class="sxs-lookup"><span data-stu-id="3b80b-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="3b80b-142">Kliknij przycisk Zamknij.</span><span class="sxs-lookup"><span data-stu-id="3b80b-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="3b80b-143">Zapisywanie faktury niezależnej jako szablonu</span><span class="sxs-lookup"><span data-stu-id="3b80b-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="3b80b-144">Istniejącą fakturę niezależną można również zapisać jako szablon.</span><span class="sxs-lookup"><span data-stu-id="3b80b-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="3b80b-145">Gdy na karcie Faktura wybierzesz opcję Zapisz do szablonu, wprowadź nazwę i opis szablonu.</span><span class="sxs-lookup"><span data-stu-id="3b80b-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="3b80b-146">Jeśli szablon o tej nazwie już istnieje, zobaczysz o tym powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="3b80b-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="3b80b-147">Nadal można kliknąć przycisk OK, aby zastąpić istniejący szablon.</span><span class="sxs-lookup"><span data-stu-id="3b80b-147">You can still click on Ok to replace it.</span></span> 