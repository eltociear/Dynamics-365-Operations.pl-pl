---
title: Grupowa aktualizacja środków trwałych
description: Jeśli są stosowane księgi, istnieje możliwość zmiany konwencji amortyzacji dla grup środków trwałych będących częścią tej samej księgi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b9aaaabcac09c9147c350422924a23f785c0ce
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179386"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="68923-103">Grupowa aktualizacja środków trwałych</span><span class="sxs-lookup"><span data-stu-id="68923-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68923-104">Jeśli są stosowane księgi, istnieje możliwość zmiany konwencji amortyzacji dla grup środków trwałych będących częścią tej samej księgi.</span><span class="sxs-lookup"><span data-stu-id="68923-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="68923-105">Jeśli na przykład firma znajduje się w Stanach Zjednoczonych i w czwartym kwartale roku wyeksploatowała ponad 40 procent swoich środków trwałych, musi użyć konwencji amortyzacji „w trakcie kwartału”.</span><span class="sxs-lookup"><span data-stu-id="68923-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="68923-106">W celu zmiany wszystkich środków trwałych wymagających zmiany konwencji amortyzacji można użyć procesu aktualizacji grupowej.</span><span class="sxs-lookup"><span data-stu-id="68923-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="68923-107">Podczas aktualizowania konwencji amortyzacji dla środków trwałych należy usunąć wszystkie transakcje amortyzacji, które istnieją dla tych środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="68923-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="68923-108">Ponadto należy usunąć wszystkie transakcje korekt amortyzacji, podwyższenia amortyzacji i amortyzacji dodatkowych dla tych środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="68923-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="68923-109">Aby zaktualizować konwencję amortyzacji dla środków trwałych, które zostały już zlikwidowane, najpierw trzeba usunąć istniejące transakcje likwidacji.</span><span class="sxs-lookup"><span data-stu-id="68923-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="68923-110">Należy również usunąć wszystkie transakcje, które zostały wygenerowane w wyniku procesu likwidacji.</span><span class="sxs-lookup"><span data-stu-id="68923-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="68923-111">Po zaktualizowaniu konwencji amortyzacji dla środków trwałych można przetworzyć amortyzację oraz amortyzację dodatkową dla poszczególnych środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="68923-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="68923-112">Istnieje również możliwość ręcznego tworzenia korekt amortyzacji, jeśli są wymagane zmiany.</span><span class="sxs-lookup"><span data-stu-id="68923-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>




