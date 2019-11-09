---
title: Konfigurowanie grup księgowania dla podatku
description: Podatek jest obliczany i księgowany na kontach głównych określonych w grupach księgowania.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cab2f427ed4f90021ed74da07527bc4b9378d97
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186033"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a><span data-ttu-id="9a126-103">Konfigurowanie grup księgowania dla podatku</span><span class="sxs-lookup"><span data-stu-id="9a126-103">Set up Ledger posting groups for sales tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a126-104">Podatek jest obliczany i księgowany na kontach głównych określonych w grupach księgowania.</span><span class="sxs-lookup"><span data-stu-id="9a126-104">Sales tax is calculated and posted to main accounts that are specified in the Ledger posting groups.</span></span> <span data-ttu-id="9a126-105">Grupy księgowania są dołączane do każdego kodu podatku.</span><span class="sxs-lookup"><span data-stu-id="9a126-105">Ledger posting groups are attached to each sales tax code.</span></span> <span data-ttu-id="9a126-106">Można skonfigurować osobne grupy księgowania dla każdego kodu podatku, użyć jednej grupy księgowania dla wszystkich kodów podatku lub przypisać wiele grup księgowania do kodów podatków.</span><span class="sxs-lookup"><span data-stu-id="9a126-106">You can set up individual ledger posting groups for each sales tax code, use one ledger posting group for all sales tax codes or assign multiple ledger posting groups to the sales tax codes.</span></span> <span data-ttu-id="9a126-107">To nagranie wykorzystuje firmę demonstracyjną DEMF.</span><span class="sxs-lookup"><span data-stu-id="9a126-107">This recording uses the DEMF demo company.</span></span> 

1. <span data-ttu-id="9a126-108">Wybierz kolejno opcje **Okienko nawigacji > Moduły > Podatek > Ustawienia > Podatek > Grupy księgowania**.</span><span class="sxs-lookup"><span data-stu-id="9a126-108">Go to **Navigation pane > Modules > Tax > Setup > Sales tax > Ledger posting groups**.</span></span>
2. <span data-ttu-id="9a126-109">Kliknij przycisk **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="9a126-109">Click **New**.</span></span>
3. <span data-ttu-id="9a126-110">W polu **Grupa księgowania** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="9a126-110">In the **Ledger posting group** field, type a value.</span></span>
4. <span data-ttu-id="9a126-111">W polu **Opis** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="9a126-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9a126-112">W polu **Podatek należny** wybierz konto główne dla wychodzących podatków, które są płatne na rzecz urzędu skarbowego.</span><span class="sxs-lookup"><span data-stu-id="9a126-112">In the **Sales tax payable** field, select the main account for outgoing sales taxes that are payable to the tax authority.</span></span> <span data-ttu-id="9a126-113">Podatki są zbierane w imieniu urzędu skarbowego przy sprzedaży opodatkowanych towarów i usług.</span><span class="sxs-lookup"><span data-stu-id="9a126-113">Sales taxes are collected on behalf of the tax authority when you sell taxable goods and services.</span></span>  
6. <span data-ttu-id="9a126-114">W polu **Podatek naliczony** wybierz konto główne dla przychodzących podatków, które otrzymuje się z urzędu skarbowego.</span><span class="sxs-lookup"><span data-stu-id="9a126-114">In the **Sales tax receivable** field, select the main account for incoming taxes that are received from the tax authority.</span></span> <span data-ttu-id="9a126-115">Dostawcy pobierają podatki w imieniu urzędu skarbowego, kiedy kupujesz opodatkowane towary i usługi.</span><span class="sxs-lookup"><span data-stu-id="9a126-115">Vendors collect taxes on behalf of the tax authority when you buy taxable goods and services.</span></span> <span data-ttu-id="9a126-116">To pole jest niedostępne, gdy na stronie Parametry księgi głównej zaznaczono opcję **Zastosuj zasady opodatkowania dla podatku**.</span><span class="sxs-lookup"><span data-stu-id="9a126-116">This field is not available if the Apply sales tax taxation rules option is selected in the **General ledger parameters** page.</span></span> <span data-ttu-id="9a126-117">Zamiast tego podatki płacone dostawcom są księgowane po stronie debetowej na tym samym koncie, co zakupy.</span><span class="sxs-lookup"><span data-stu-id="9a126-117">Instead, sales taxes that are paid to vendors are debited to the same account as the purchase.</span></span>   
7. <span data-ttu-id="9a126-118">W polu **Wydatki podatku nienaliczonego** wybierz konto główne dla księgowania podatków konsumpcyjnych podlegających odliczeniu, które nie zostały pobrane ani zgłoszone do urzędu skarbowego przez dostawców w ramach systemu odwróconego podatku PTU/HST stosowanego w UE.</span><span class="sxs-lookup"><span data-stu-id="9a126-118">In the **Use tax expense** field, select  the main account for posting deductible Use taxes that are not claimed or reported to the tax authority by vendors as part of EU reverse charge GST/HST.</span></span> <span data-ttu-id="9a126-119">Opcja **Podatek nienaliczony** musi zostać wybrana dla **kodu podatku** w **grupie podatków**, która jest używana w transakcji.</span><span class="sxs-lookup"><span data-stu-id="9a126-119">The **Use tax** option needs to be selected for the **Sales tax code** in the **Sales tax group** that is used in the transaction.</span></span> <span data-ttu-id="9a126-120">To pole jest niedostępne, gdy na stronie **Parametry księgi głównej** zaznaczono opcję **Zastosuj zasady opodatkowania** dla podatku.</span><span class="sxs-lookup"><span data-stu-id="9a126-120">This field is not be available if the **Apply sales tax taxation rules** option is selected in the **General ledger parameters** page.</span></span>   
8. <span data-ttu-id="9a126-121">W polu **Podatek nienaliczony** należny wybierz konto główne do księgowania przychodzących podatków konsumpcyjnych, które są płatne na rzecz urzędu skarbowego.</span><span class="sxs-lookup"><span data-stu-id="9a126-121">In the **Use tax payable** field, select the main account for posting incoming Use taxes that are payable to tax authorities.</span></span> <span data-ttu-id="9a126-122">Opcja **Podatek nienaliczony** musi zostać wybrana dla **kodu podatku** w **grupie podatków**, aby można było zaksięgować **Podatek nienaliczony**.</span><span class="sxs-lookup"><span data-stu-id="9a126-122">The **Use tax** option needs to be selected in the **Sales tax code** in the **Sales tax group** to post **Use tax**.</span></span> <span data-ttu-id="9a126-123">Jeśli w oknie **Parametry księgi głównej** zaznaczono opcję **Zastosuj zasady opodatkowania dla podatku**, kompensacja jest księgowana na koncie wydatków transakcji.</span><span class="sxs-lookup"><span data-stu-id="9a126-123">If **Apply sales tax taxation rules** option is selected in **General ledger parameters** page, the offset is posted to the transaction’s expense account.</span></span>   
9. <span data-ttu-id="9a126-124">W polu **Konto rozliczeniowe** wybierz konto główne, na którym będzie księgowane saldo netto kont księgowych określonych w polach **Podatek nienaliczony należny** i **Podatek naliczony**.</span><span class="sxs-lookup"><span data-stu-id="9a126-124">In the **Settlement account** field, select the main account that the net balance of the ledger accounts specified in the **Use tax payable** and **Sales tax receivable** fields will be posted.</span></span> <span data-ttu-id="9a126-125">Saldo zostanie utworzone podczas rozliczania podatku i wykonywania zadania księgowania.</span><span class="sxs-lookup"><span data-stu-id="9a126-125">The balance will be created when the sales tax settle and post job is ran.</span></span>  <span data-ttu-id="9a126-126">Jeśli urząd skarbowy za okres rozliczeniowy jest skojarzony z kontem dostawcy, saldo jest zamiast tego księgowane na koncie dostawcy.</span><span class="sxs-lookup"><span data-stu-id="9a126-126">If the tax authority for the settlement period is associated with a vendor account, the balance is posted to the vendor account instead.</span></span>
10. <span data-ttu-id="9a126-127">W polu **Rabat gotówkowy dostawcy** wybierz konto główne do księgowania rabatów gotówkowych dla kodów podatków skojarzonych z tą grupą księgowania.</span><span class="sxs-lookup"><span data-stu-id="9a126-127">In the **Vendor cash discount** field, select the main account to post cash discount for Sales tax codes associated with this Ledger posting group.</span></span> <span data-ttu-id="9a126-128">To ustawienie jest opcjonalne i jeśli konto nie zostanie wprowadzone, będzie używane konto główne z **kodów rabatów gotówkowych**.</span><span class="sxs-lookup"><span data-stu-id="9a126-128">This is optional and if no account is entered,  the main account on **Cash discount codes** will be used.</span></span> <span data-ttu-id="9a126-129">Może być korzystne używanie różnych kont dla poszczególnych **grup księgowania**, jeśli w oknie Grupy podatków zaznaczono opcję Cofnij podatek od rabatu gotówkowego.</span><span class="sxs-lookup"><span data-stu-id="9a126-129">It can be useful to use different accounts per **Ledger posting group** if using the reverse sales tax on cash discount option on Sales tax groups.</span></span>  
11. <span data-ttu-id="9a126-130">W polu **Rabat gotówkowy odbiorcy** wybierz konto główne do księgowania rabatów gotówkowych dla **kodów podatków** skojarzonych z tą **grupą księgowania**.</span><span class="sxs-lookup"><span data-stu-id="9a126-130">In the **Customer case discount** field, select the main account to post cash discount for **Sales tax codes** associated with this **Ledger posting group**.</span></span> <span data-ttu-id="9a126-131">To ustawienie jest opcjonalne i jeśli konto nie zostanie wprowadzone, będzie używane konto główne z **kodów rabatów gotówkowych**.</span><span class="sxs-lookup"><span data-stu-id="9a126-131">This is optional and if no account is entered, the main account on the **Cash discount codes** will be used.</span></span> <span data-ttu-id="9a126-132">Może być korzystne używanie różnych kont dla poszczególnych **grup księgowania**, jeśli w oknie **Grupy podatków** zaznaczono opcję Cofnij podatek od rabatu gotówkowego.</span><span class="sxs-lookup"><span data-stu-id="9a126-132">It can be useful to use different accounts per **Ledger posting group** if using the reverse sales tax on cash discount option on **Sales tax groups**.</span></span>  
12. <span data-ttu-id="9a126-133">Kliknij przycisk **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="9a126-133">Click **Save**.</span></span>
