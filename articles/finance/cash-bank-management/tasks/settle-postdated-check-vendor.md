---
title: Rozliczanie czeku postdatowanego dla dostawcy
description: Rozlicz czek postdatowany wystawiony dostawcy, gdy bank rozliczył transakcję czekiem, który były zaległy, ale został zaakceptowany przez bank.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d935ec24d97ca76a088cbe41d57c12c6e8a6689
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188057"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="f039c-103">Rozliczanie czeku postdatowanego dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="f039c-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f039c-104">Rozlicz czek postdatowany wystawiony dostawcy, gdy bank rozliczył transakcję czekiem, który były zaległy, ale został zaakceptowany przez bank.</span><span class="sxs-lookup"><span data-stu-id="f039c-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="f039c-105">Przed rozpoczęciem tej procedury wykonaj następujące procedury.</span><span class="sxs-lookup"><span data-stu-id="f039c-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="f039c-106">Konfigurowanie czeków postdatowanych</span><span class="sxs-lookup"><span data-stu-id="f039c-106">Set up postdated checks</span></span>

2) <span data-ttu-id="f039c-107">Rejestrowanie i księgowanie czeku postdatowanego dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="f039c-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="f039c-108">Rolą w tej procedurze jest Skarbnik.</span><span class="sxs-lookup"><span data-stu-id="f039c-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="f039c-109">Ta procedura wykorzystuje firmę demonstracyjną USMF.</span><span class="sxs-lookup"><span data-stu-id="f039c-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="f039c-110">Wybierz kolejno opcje Rozrachunki z dostawcami > Płatności > Czeki postdatowane odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="f039c-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="f039c-111">Kliknij opcję Rozlicz.</span><span class="sxs-lookup"><span data-stu-id="f039c-111">Click Settle.</span></span>
3. <span data-ttu-id="f039c-112">Kliknij opcję Rozlicz wpisy rozrachunkowe.</span><span class="sxs-lookup"><span data-stu-id="f039c-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="f039c-113">Rozlicz konto dostawcy dla transakcji czekowej.</span><span class="sxs-lookup"><span data-stu-id="f039c-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="f039c-114">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="f039c-114">Close the page.</span></span>
5. <span data-ttu-id="f039c-115">Wybierz kolejno opcje Księga główna > Wpisy w arkuszu > Arkusze finansowe.</span><span class="sxs-lookup"><span data-stu-id="f039c-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="f039c-116">W polu Pokaż wybierz opcję „Wszystko”.</span><span class="sxs-lookup"><span data-stu-id="f039c-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="f039c-117">Zaznacz lub wyczyść pole wyboru Pokaż tylko utworzone przez użytkowników.</span><span class="sxs-lookup"><span data-stu-id="f039c-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="f039c-118">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="f039c-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f039c-119">Kliknij przycisk Wiersze.</span><span class="sxs-lookup"><span data-stu-id="f039c-119">Click Lines.</span></span>
10. <span data-ttu-id="f039c-120">Kliknij opcję Załącznik.</span><span class="sxs-lookup"><span data-stu-id="f039c-120">Click Voucher.</span></span>
11. <span data-ttu-id="f039c-121">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="f039c-121">Close the page.</span></span>
