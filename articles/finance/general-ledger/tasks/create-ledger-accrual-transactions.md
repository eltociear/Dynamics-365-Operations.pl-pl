---
title: Tworzenie transakcji naliczeń finansowych
description: Ten przewodnik po zadaniach prowadzi przez generowanie transakcji naliczeń finansowych opartych na schematach naliczania.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186194"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="c8e32-103">Tworzenie transakcji naliczeń finansowych</span><span class="sxs-lookup"><span data-stu-id="c8e32-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8e32-104">Ten przewodnik po zadaniach prowadzi przez generowanie transakcji naliczeń finansowych opartych na schematach naliczania.</span><span class="sxs-lookup"><span data-stu-id="c8e32-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="c8e32-105">Wybierz kolejno opcje Księga główna > Wpisy w arkuszu > Arkusze finansowe.</span><span class="sxs-lookup"><span data-stu-id="c8e32-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="c8e32-106">Na liście znajdź i zaznacz odpowiedni arkusz lub utwórz nowy.</span><span class="sxs-lookup"><span data-stu-id="c8e32-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="c8e32-107">Kliknij, aby otworzyć łącze znajdujące się w polu Arkusz z numerem partii.</span><span class="sxs-lookup"><span data-stu-id="c8e32-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="c8e32-108">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="c8e32-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="c8e32-109">W polu Konto podaj żądane wartości.</span><span class="sxs-lookup"><span data-stu-id="c8e32-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="c8e32-110">W tym przykładzie definiujemy wydatek na ubezpieczenie.</span><span class="sxs-lookup"><span data-stu-id="c8e32-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="c8e32-111">Stanie się on wydatkiem okresowym.</span><span class="sxs-lookup"><span data-stu-id="c8e32-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="c8e32-112">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="c8e32-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="c8e32-113">W polu Debet wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="c8e32-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="c8e32-114">W polu Konto przeciwstawne podaj żądane wartości.</span><span class="sxs-lookup"><span data-stu-id="c8e32-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="c8e32-115">Kliknij przycisk Funkcje.</span><span class="sxs-lookup"><span data-stu-id="c8e32-115">Click Functions.</span></span>
10. <span data-ttu-id="c8e32-116">Kliknij opcję Naliczenia finansowe.</span><span class="sxs-lookup"><span data-stu-id="c8e32-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="c8e32-117">W polu Identyfikacja naliczania kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="c8e32-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c8e32-118">Na liście odszukaj i zaznacz schemat naliczania, który chcesz zastosować.</span><span class="sxs-lookup"><span data-stu-id="c8e32-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="c8e32-119">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="c8e32-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c8e32-120">W polu Data początkowa wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="c8e32-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="c8e32-121">Kliknij opcję Transakcje.</span><span class="sxs-lookup"><span data-stu-id="c8e32-121">Click Transactions.</span></span>
16. <span data-ttu-id="c8e32-122">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="c8e32-122">Close the page.</span></span>
17. <span data-ttu-id="c8e32-123">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="c8e32-123">Click OK.</span></span>
18. <span data-ttu-id="c8e32-124">Kliknij przycisk Księguj.</span><span class="sxs-lookup"><span data-stu-id="c8e32-124">Click Post.</span></span>
