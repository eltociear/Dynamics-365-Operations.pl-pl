---
title: Tworzenie i nabywanie środków trwałych z modułu Rozrachunki z dostawcami
description: Ten przewodnik po zadaniach zawiera instruktaż tworzenia i nabywania środka trwałego za pomocą procesu zakupów.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179381"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="9fe39-103">Tworzenie i nabywanie środków trwałych z modułu Rozrachunki z dostawcami</span><span class="sxs-lookup"><span data-stu-id="9fe39-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fe39-104">Ten przewodnik po zadaniach zawiera instruktaż tworzenia i nabywania środka trwałego za pomocą procesu zakupów.</span><span class="sxs-lookup"><span data-stu-id="9fe39-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="9fe39-105">Wykorzystuje role Księgowy i Pracownik ds. rozrachunków z dostawcami oraz firmę demonstracyjną USMF.</span><span class="sxs-lookup"><span data-stu-id="9fe39-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="9fe39-106">Konfigurowanie parametrów środków trwałych</span><span class="sxs-lookup"><span data-stu-id="9fe39-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="9fe39-107">W **okienku nawigacji** przejdź do **Moduły > Środki trwałe > Ustawienia > Parametry środków trwałych**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="9fe39-108">Rozwiń skróconą kartę **Zamówienia zakupu**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="9fe39-109">Zaznacz pole wyboru **Zezwalaj na nabywanie środków trwałych z zakupów**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="9fe39-110">Zaznacz pole wyboru **Utwórz środek trwały podczas księgowania dokumentu przyjęcia produktów lub faktury**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="9fe39-111">Tworzenie nowej faktury od dostawcy</span><span class="sxs-lookup"><span data-stu-id="9fe39-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="9fe39-112">W **okienku nawigacji** przejdź do **Moduły > Rozrachunki z dostawcami > Obszary robocze > Wprowadzanie faktur od dostawcy**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="9fe39-113">Kliknij przycisk **Nowa faktura od dostawcy**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="9fe39-114">W polu **Konto płatnika** kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="9fe39-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9fe39-115">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="9fe39-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9fe39-116">W polu **Numer** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="9fe39-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="9fe39-117">W polu **Data księgowania** wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="9fe39-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="9fe39-118">Kliknij przycisk **Dodaj wiersz.**</span><span class="sxs-lookup"><span data-stu-id="9fe39-118">Click **Add line**.</span></span>
8. <span data-ttu-id="9fe39-119">W polu **Numer towaru** kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="9fe39-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="9fe39-120">Do nabywania środków trwałych mogą służyć towary niemagazynowe lub kategorie zaopatrzenia.</span><span class="sxs-lookup"><span data-stu-id="9fe39-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="9fe39-121">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="9fe39-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9fe39-122">W polu **Ilość** wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="9fe39-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="9fe39-123">Jeden wiersz faktury spowoduje utworzenie tylko jednego środka trwałego, niezależnie od ilości.</span><span class="sxs-lookup"><span data-stu-id="9fe39-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="9fe39-124">Wartość pola ilości fakturowanej zostanie przeniesiona do ilości środka trwałego.</span><span class="sxs-lookup"><span data-stu-id="9fe39-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="9fe39-125">W polu **Cena jednostkowa** wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="9fe39-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="9fe39-126">Rozwiń skróconą kartę **Szczegóły wiersza**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="9fe39-127">Kliknij kartę **Środki trwałe**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="9fe39-128">Zaznacz pole wyboru **Utwórz nowy środek trwały**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="9fe39-129">W polu **Grupa środków trwałych** kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="9fe39-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="9fe39-130">Na liście wybierz grupę środków trwałych, która ma być używana podczas tworzenia nowego środka trwałego.</span><span class="sxs-lookup"><span data-stu-id="9fe39-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="9fe39-131">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="9fe39-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9fe39-132">Kliknij przycisk **Księguj**.</span><span class="sxs-lookup"><span data-stu-id="9fe39-132">Click **Post**.</span></span> <span data-ttu-id="9fe39-133">Środek trwały zostanie utworzony i nabyty podczas księgowania faktury.</span><span class="sxs-lookup"><span data-stu-id="9fe39-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  
