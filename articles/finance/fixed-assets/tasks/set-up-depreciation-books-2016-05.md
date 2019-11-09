---
title: Konfigurowanie ksiąg amortyzacji (maj 2016)
description: W tym przewodniku po zadaniach zostanie utworzona nowa księga amortyzacji i skojarzona z grupą środków trwałych.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186907"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="fa00d-103">Konfigurowanie ksiąg amortyzacji (maj 2016)</span><span class="sxs-lookup"><span data-stu-id="fa00d-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa00d-104">W tym przewodniku po zadaniach zostanie utworzona nowa księga amortyzacji i skojarzona z grupą środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="fa00d-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="fa00d-105">Przewodnik korzysta z roli Księgowy i danych firmy demonstracyjnej USMF.</span><span class="sxs-lookup"><span data-stu-id="fa00d-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="fa00d-106">Tworzenie księgi amortyzacji</span><span class="sxs-lookup"><span data-stu-id="fa00d-106">Create a depreciation book</span></span>
1. <span data-ttu-id="fa00d-107">Wybierz kolejno opcje Środki trwałe > Ustawienia > Księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="fa00d-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="fa00d-108">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="fa00d-108">Click New.</span></span>
3. <span data-ttu-id="fa00d-109">W polu Księga amortyzacji wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="fa00d-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="fa00d-110">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="fa00d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa00d-111">Zaznacz pole wyboru Oblicz amortyzację lub usuń jego zaznaczenie.</span><span class="sxs-lookup"><span data-stu-id="fa00d-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="fa00d-112">W polu Profil amortyzacji kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="fa00d-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fa00d-113">Na liście znajdź i zaznacz odpowiedni profil amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="fa00d-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="fa00d-114">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="fa00d-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fa00d-115">W polu Amortyzacja alternatywna kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="fa00d-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fa00d-116">Na liście zaznacz odpowiedni profil amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="fa00d-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="fa00d-117">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="fa00d-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fa00d-118">Profil Amortyzacja dodatkowa będzie używany na potrzeby dodatkowej amortyzacji składnika aktywów w nadzwyczajnych okolicznościach.</span><span class="sxs-lookup"><span data-stu-id="fa00d-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="fa00d-119">Na przykład może to służy do zarejestrowania amortyzacji powstałej w wyniku klęski żywiołowej.</span><span class="sxs-lookup"><span data-stu-id="fa00d-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="fa00d-120">Zaznacz lub wyczyść pole wyboru Tworzenie korekt amortyzacji przy korektach podstawy.</span><span class="sxs-lookup"><span data-stu-id="fa00d-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="fa00d-121">W polu Kalendarz kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="fa00d-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="fa00d-122">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="fa00d-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="fa00d-123">Kojarzenie księgi amortyzacji z grupą środków trwałych</span><span class="sxs-lookup"><span data-stu-id="fa00d-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="fa00d-124">Kliknij opcję Grupy środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="fa00d-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="fa00d-125">W polu Grupa środków trwałych kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="fa00d-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fa00d-126">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="fa00d-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="fa00d-127">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="fa00d-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fa00d-128">W polu Konwencja amortyzacji wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="fa00d-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="fa00d-129">W polu Okres użytkowania wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="fa00d-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="fa00d-130">Należy zauważyć, że wartość pola Okresy amortyzacji jest obliczana po ustawieniu okresu użytkowania.</span><span class="sxs-lookup"><span data-stu-id="fa00d-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  
