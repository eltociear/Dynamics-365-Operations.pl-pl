---
title: Metody amortyzacji i konwencje
description: Ten artykuł zawiera omówienie konwencji amortyzacji i metod amortyzacji obsługiwanych w Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f1320d0adaad783f856ed6404039e7954920340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187344"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="7a537-103">Metody amortyzacji i konwencje</span><span class="sxs-lookup"><span data-stu-id="7a537-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a537-104">Ten artykuł zawiera omówienie obsługiwanych konwencji amortyzacji i metod amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="7a537-105">Można wybrać różne metody i konwencje amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="7a537-106">Celem metod jest alokowanie wartości amortyzacji środka trwałego w okresach obrachunkowych.</span><span class="sxs-lookup"><span data-stu-id="7a537-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="7a537-107">Wartość środka trwałego podlegająca amortyzacji jest ceną nabycia pomniejszoną o ewentualną wartość likwidacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="7a537-108">W przypadku używania konwencji amortyzacji i modyfikowania daty ostatniego rozpoczęcia amortyzacji środka trwałego, co sprawia, że kilka amortyzacji jest pomijanych, amortyzacja za ostatni rok może być większa lub mniejsza niż oczekiwana.</span><span class="sxs-lookup"><span data-stu-id="7a537-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="7a537-109">Amortyzacja jest korygowana przez liczbę okresów amortyzacji których dotyczy modyfikacja daty ostatniego rozpoczęcia amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="7a537-110">Przykładowo, gdy przez trzy lata używana jest półroczna konwencja amortyzacji, amortyzacja zazwyczaj występuje przez 3,5 roku.</span><span class="sxs-lookup"><span data-stu-id="7a537-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="7a537-111">Jeśli w ciągu 3,5 roku zostanie zmieniona data ostatniego rozpoczęcia amortyzacji, ostatni rok amortyzacji przesunie w górę liczbę okresów, których to dotyczy.</span><span class="sxs-lookup"><span data-stu-id="7a537-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="7a537-112">Jeśli data zostanie przesunięta o trzy miesiące, ostatni rok będzie miał dziewięć miesięcy wartych amortyzacji, podczas gdy normalnie byłoby ich sześć.</span><span class="sxs-lookup"><span data-stu-id="7a537-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="7a537-113">Można wybierać spośród następujących konwencji amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="7a537-114">Pół roku</span><span class="sxs-lookup"><span data-stu-id="7a537-114">Half year</span></span>
-   <span data-ttu-id="7a537-115">Pełny miesiąc</span><span class="sxs-lookup"><span data-stu-id="7a537-115">Full month</span></span>
-   <span data-ttu-id="7a537-116">Kwartał środkowy</span><span class="sxs-lookup"><span data-stu-id="7a537-116">Mid quarter</span></span>
-   <span data-ttu-id="7a537-117">Miesiąc środkowy (1. dzień miesiąca)</span><span class="sxs-lookup"><span data-stu-id="7a537-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="7a537-118">Miesiąc środkowy (15. dzień miesiąca)</span><span class="sxs-lookup"><span data-stu-id="7a537-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="7a537-119">Pół roku (początek roku)</span><span class="sxs-lookup"><span data-stu-id="7a537-119">Half year (start of year)</span></span>
-   <span data-ttu-id="7a537-120">Pół roku (następny rok)</span><span class="sxs-lookup"><span data-stu-id="7a537-120">Half year (next year)</span></span>

<span data-ttu-id="7a537-121">Można wybrać jedną z następujących metod amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="7a537-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="7a537-122">Liniowy okres użytkowania</span><span class="sxs-lookup"><span data-stu-id="7a537-122">Straight line service life</span></span>
-   <span data-ttu-id="7a537-123">Degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-123">Reducing balance</span></span>
-   <span data-ttu-id="7a537-124">Ręczne</span><span class="sxs-lookup"><span data-stu-id="7a537-124">Manual</span></span>
-   <span data-ttu-id="7a537-125">Współczynnik</span><span class="sxs-lookup"><span data-stu-id="7a537-125">Factor</span></span>
-   <span data-ttu-id="7a537-126">Zużycie</span><span class="sxs-lookup"><span data-stu-id="7a537-126">Consumption</span></span>
-   <span data-ttu-id="7a537-127">Liniowy pozostały okres użytkowania</span><span class="sxs-lookup"><span data-stu-id="7a537-127">Straight line life remaining</span></span>
-   <span data-ttu-id="7a537-128">Degresywna 200%</span><span class="sxs-lookup"><span data-stu-id="7a537-128">200% reducing balance</span></span>
-   <span data-ttu-id="7a537-129">Degresywna 175%</span><span class="sxs-lookup"><span data-stu-id="7a537-129">175% reducing balance</span></span>
-   <span data-ttu-id="7a537-130">Degresywna 150%</span><span class="sxs-lookup"><span data-stu-id="7a537-130">150% reducing balance</span></span>
-   <span data-ttu-id="7a537-131">Degresywna 125%</span><span class="sxs-lookup"><span data-stu-id="7a537-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="7a537-132">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="7a537-132">Additional resources</span></span>
--------

[<span data-ttu-id="7a537-133">Amortyzacja środka trwałego</span><span class="sxs-lookup"><span data-stu-id="7a537-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="7a537-134">Amortyzacja liniowa za okres użytkowania</span><span class="sxs-lookup"><span data-stu-id="7a537-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="7a537-135">Amortyzacja degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="7a537-136">Amortyzacja ręczna</span><span class="sxs-lookup"><span data-stu-id="7a537-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="7a537-137">Amortyzacja czynnikowa</span><span class="sxs-lookup"><span data-stu-id="7a537-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="7a537-138">Amortyzacja według zużycia</span><span class="sxs-lookup"><span data-stu-id="7a537-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="7a537-139">Amortyzacja liniowa za pozostały okres użytkowania</span><span class="sxs-lookup"><span data-stu-id="7a537-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="7a537-140">125% amortyzacja degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="7a537-141">150% amortyzacja degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="7a537-142">175% amortyzacja degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="7a537-143">200% amortyzacja degresywna</span><span class="sxs-lookup"><span data-stu-id="7a537-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)


