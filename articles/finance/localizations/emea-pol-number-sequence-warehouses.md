---
title: Konfigurowanie numeracji według magazynów
description: W tym temacie omówiono konfigurowanie numeracji dokumentów przyjęcia produktów dla zakupu i dokumentów dostawy dla sprzedaży z podziałem na magazyny dla Polski.
author: ShylaThompson
manager: AnnBe
ms.date: 09/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Poland
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2a05f61c53db4fa5b90c5bc67aef9f80438f7c7b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183841"
---
# <a name="set-up-number-sequences-by-warehouse"></a><span data-ttu-id="80b0a-103">Konfigurowanie numeracji według magazynów</span><span class="sxs-lookup"><span data-stu-id="80b0a-103">Set up number sequences by warehouse</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="80b0a-104">W tym temacie omówiono konfigurowanie numeracji dokumentów przyjęcia produktów dla zakupu i dokumentów dostawy dla sprzedaży z podziałem na magazyny dla Polski.</span><span class="sxs-lookup"><span data-stu-id="80b0a-104">This topic walks you through setting up number sequences for purchase product receipts and sales packing slips by warehouse for Poland.</span></span>

## <a name="set-up-a-number-sequence-for-purchase-product-receipts-by-warehouse"></a><span data-ttu-id="80b0a-105">Konfigurowanie sekwencji numerów dla dokumentów przyjęcia produktów zakupionych według magazynu</span><span class="sxs-lookup"><span data-stu-id="80b0a-105">Set up a number sequence for purchase product receipts by warehouse</span></span>

<span data-ttu-id="80b0a-106">Istnieje możliwość skonfigurowania sekwencji numerów dla dokumentów przyjęcia produktów zakupionych według magazynu na stronie **Parametry modułu rozrachunków z dostawcami**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-106">You can set up a number sequence for purchase product receipts by warehouse on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="80b0a-107">Dokumenty dostawy można ponumerować oddzielnie dla każdego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-107">You can number delivery documents separately for each warehouse.</span></span> 

1. <span data-ttu-id="80b0a-108">Kliknij kolejno opcje **Rozrachunki z dostawcami > Ustawienia > Parametry modułu rozrachunków z dostawcami**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-108">Click **Accounts payable > Setup > Accounts payable parameters**.</span></span> 
2. <span data-ttu-id="80b0a-109">Na stronie **Parametry modułu rozrachunków z dostawcami** w lewym okienku kliknij opcję **Numery kolejne**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-109">On the **Accounts payable parameters** page, in the left pane, click **Number sequences**.</span></span> 
3. <span data-ttu-id="80b0a-110">W polu **Kod sekwencji numerów** wybierz numerację dla typu odwołania Wewnętrzny dokument przyjęcia produktów.</span><span class="sxs-lookup"><span data-stu-id="80b0a-110">In the **Number sequence code** field, select a number sequence for the Internal product receipt reference type.</span></span> 
4. <span data-ttu-id="80b0a-111">Kliknij przycisk **Magazyny**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-111">Click **Warehouses**.</span></span> 
5. <span data-ttu-id="80b0a-112">Na stronie **Zakup — numerowanie dokumentów dostawy** w polu **Magazyn** wybierz magazyn.</span><span class="sxs-lookup"><span data-stu-id="80b0a-112">On the **Purchase – delivery note numbering** page, in the **Warehouse** field, select a warehouse.</span></span> 
6. <span data-ttu-id="80b0a-113">W polu **Kod sekwencji numerów** wprowadź kod sekwencji numerów dokumentów przyjęcia produktów dla wybranego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-113">In the **Number sequence code** field, enter a product receipt number sequence code for the selected warehouse.</span></span> 
7. <span data-ttu-id="80b0a-114">Powtórz krok 6 dla każdego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-114">Repeat step 6 for each warehouse.</span></span> 

> [!NOTE]
> <span data-ttu-id="80b0a-115">Można również skonfigurować numerację dokumentów dostawy według magazynu dla zamówienia zakupu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-115">You can also set up delivery document numbering by warehouse for a purchase order.</span></span> <span data-ttu-id="80b0a-116">W tym celu należy wybrać określony magazyn na stronie **Księgowanie dokumentu przyjęcia produktów**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-116">To do this, select a specific warehouse on the **Posting product receipt** page.</span></span> <span data-ttu-id="80b0a-117">Po zaksięgowaniu dokumentu przyjęcia produktów stan wiersza zamówienia zakupu nie zmieni się na **Dostarczone** lub **Otrzymano**, dopóki wszystkie wiersze zakupu dla wszystkich magazynów nie zostaną zaksięgowane dla tego zamówienia zakupu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-117">After you post a product receipt, the order status of the purchase order line will not change to **Delivered** or **Received** until all purchase lines for all warehouses are posted for the purchase order.</span></span> 

## <a name="set-up-a-number-sequence-for-sales-packing-slips-by-warehouse"></a><span data-ttu-id="80b0a-118">Ustaw sekwencję identyfikatorów dokumentów dostawy sprzedaży według magazynu</span><span class="sxs-lookup"><span data-stu-id="80b0a-118">Set up a number sequence for sales packing slips by warehouse</span></span>

<span data-ttu-id="80b0a-119">Istnieje możliwość skonfigurowania sekwencji numerów dla dokumentów dostawy sprzedaży według magazynu na stronie **Parametry modułu rozrachunków z odbiorcami**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-119">You can set up a number sequence for sales packing slips by warehouse on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="80b0a-120">Dokumenty dostawy można ponumerować oddzielnie dla każdego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-120">You can number delivery documents separately for each warehouse.</span></span> 

1. <span data-ttu-id="80b0a-121">Kliknij kolejno opcje **Rozrachunki z dostawcami > Ustawienia > Parametry modułu rozrachunków z odbiorcami**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-121">Click **Accounts receivable > Setup > Accounts receivable parameters**.</span></span> 
2. <span data-ttu-id="80b0a-122">W lewym okienku kliknij opcję **Aktualizacje**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-122">In the left pane, click **Updates**.</span></span> <span data-ttu-id="80b0a-123">Zaznacz pole wyboru **Oddzielna numeracja dokumentów dostawy**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-123">Select the **Independent delivery note numbering** check box.</span></span> 
3. <span data-ttu-id="80b0a-124">W lewym okienku kliknij opcję **Sekwencje identyfikatorów**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-124">In the left pane, click **Number sequences**.</span></span> <span data-ttu-id="80b0a-125">Wybierz sekwencję numerów arkuszy dla typu odwołania Dokument dostawy.</span><span class="sxs-lookup"><span data-stu-id="80b0a-125">Select a number sequence for the Packing slip reference type.</span></span> 
4. <span data-ttu-id="80b0a-126">Kliknij przycisk **Magazyny**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-126">Click **Warehouses**.</span></span> 
5. <span data-ttu-id="80b0a-127">Na stronie **Sprzedaż — numerowanie dokumentów dostawy** w polu **Magazyn** wybierz magazyn.</span><span class="sxs-lookup"><span data-stu-id="80b0a-127">On the **Sales - delivery note numbering** page, in the **Warehouse** field, select a warehouse.</span></span> 
6. <span data-ttu-id="80b0a-128">W polu **Kod sekwencji numerów** wprowadź kod numeracji dokumentów dostawy dla wybranego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-128">In the **Number sequence code** field, enter a packing slip number sequence code for the selected warehouse.</span></span> 
7. <span data-ttu-id="80b0a-129">Powtórz krok 6 dla każdego magazynu.</span><span class="sxs-lookup"><span data-stu-id="80b0a-129">Repeat step 6 for each warehouse.</span></span> 

> [!NOTE]
> <span data-ttu-id="80b0a-130">Można również skonfigurować numerację dokumentów dostawy według magazynu dla zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="80b0a-130">You can also set up delivery document numbering by warehouse for a sales order.</span></span> <span data-ttu-id="80b0a-131">W tym celu należy wybrać określony magazyn na stronie **Dokument dostawy**.</span><span class="sxs-lookup"><span data-stu-id="80b0a-131">To do this, select a specific warehouse on the **Packing slip** page.</span></span> <span data-ttu-id="80b0a-132">Po zaksięgowaniu dokumentu dostawy stan zamówienia nie zmieni się na **Dostarczone** lub **Otrzymano** w zamówieniu sprzedaży, dopóki wszystkie wiersze sprzedaży dla wszystkich magazynów nie zostaną zaksięgowane dla tego zamówienia sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="80b0a-132">After you post a packing slip, the order status will not change to **Delivered** or **Received** in the sales order until all sales lines for all warehouses are posted for the sales order.</span></span> 