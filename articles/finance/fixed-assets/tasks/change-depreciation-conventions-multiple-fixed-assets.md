---
title: Zmiana konwencji amortyzacji dla wielu środków trwałych
description: To zadanie aktualizuje konwencję amortyzacji dla wybranej grupy środków trwałych.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179382"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="4ba3a-103">Zmiana konwencji amortyzacji dla wielu środków trwałych</span><span class="sxs-lookup"><span data-stu-id="4ba3a-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ba3a-104">To zadanie aktualizuje konwencję amortyzacji dla wybranej grupy środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="4ba3a-105">W tym przewodniku po zadaniach jest wykorzystywana firma demonstracyjna USMF.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="4ba3a-106">Wybierz kolejno opcje Środki trwałe > Zadania okresowe > Aktualizacja grupowa.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="4ba3a-107">W polu Księga amortyzacji kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4ba3a-108">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4ba3a-109">W polu Rozpoczęcie eksploatacji wpisz datę.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="4ba3a-110">W polu Zakończenie eksploatacji wpisz datę.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="4ba3a-111">Aktualizacji podlegają tylko składniki aktywów, które są częścią wybranej księgi amortyzacji i zostały włączone do eksploatacji w okresie wyznaczonym tymi datami.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="4ba3a-112">W polu Bieżąca konwencja amortyzacji wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="4ba3a-113">Aktualizacja obejmie tylko składniki aktywów, które mają bieżącą konwencję amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="4ba3a-114">W polu Nowa konwencja amortyzacji wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="4ba3a-115">Sprawdź, czy raport będzie drukowany w żądanym miejscu docelowym.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="4ba3a-116">Rozwiń sekcję Rekordy do uwzględnienia.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="4ba3a-117">Kliknij przycisk Filtr.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-117">Click Filter.</span></span>
10. <span data-ttu-id="4ba3a-118">Na liście zaznacz grupę środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="4ba3a-119">W polu Kryteria kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4ba3a-120">Zaznacz żądaną grupę środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="4ba3a-121">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4ba3a-122">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-122">Click OK.</span></span>
15. <span data-ttu-id="4ba3a-123">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-123">Click OK.</span></span>
    *  <span data-ttu-id="4ba3a-124">Wyniki procesu są wyświetlane w raporcie Aktualizacja grupowa.</span><span class="sxs-lookup"><span data-stu-id="4ba3a-124">Results of the process are shown on the Mass update report.</span></span>     
