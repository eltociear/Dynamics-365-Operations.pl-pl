---
title: Anuluj planowanie pracy
description: W tym temacie wyjaśniono, jak usunąć aktywne planowanie pracy, gdy używana jest funkcja optymalizacji planowania.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774032"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="ea7b8-103">Anuluj planowanie pracy</span><span class="sxs-lookup"><span data-stu-id="ea7b8-103">Cancel a planning job</span></span>

<span data-ttu-id="ea7b8-104">W Microsoft Dynamics 365 Supply Chain Management, można usunąć aktywne planowanie pracy, gdy używana jest funkcja optymalizacji planowania.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="ea7b8-105">Aby anulować aktywne zadanie planowania, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ea7b8-106">Tylko aktywna praca może być usunięta.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="ea7b8-107">Przejdź do **Planowanie główne \> Ustawień \> Plany**.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="ea7b8-108">Umożliwia wybór odpowiedniego planu dla przebiegu planowania.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="ea7b8-109">Wybierz **Historia**.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-109">Select **History**.</span></span>
4. <span data-ttu-id="ea7b8-110">Wybierz planowaną pracę do anulowania.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="ea7b8-111">Wybierz **Anuluj**.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-111">Select **Cancel**.</span></span>

<span data-ttu-id="ea7b8-112">Stan zadania będzie **anulowany** do momentu potwierdzenia przez usługę optymalizacji planowania, że zadanie zostało anulowane.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="ea7b8-113">Status zostanie wówczas zaktualizowany do stanu **Anulowane**.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="ea7b8-114">Aby wyświetlić zmiany stanu, należy odświeżyć stronę, wybierając przycisk **Odśwież**.</span><span class="sxs-lookup"><span data-stu-id="ea7b8-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="ea7b8-115">Powiązane zasoby</span><span class="sxs-lookup"><span data-stu-id="ea7b8-115">Related resources</span></span>

[<span data-ttu-id="ea7b8-116">Omówienie planowania optymalizacji</span><span class="sxs-lookup"><span data-stu-id="ea7b8-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="ea7b8-117">Rozpocznij pracę z optymalizacją planowania</span><span class="sxs-lookup"><span data-stu-id="ea7b8-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="ea7b8-118">Analiza dopasowywania optymalizacją planowania</span><span class="sxs-lookup"><span data-stu-id="ea7b8-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ea7b8-119">Wyświetlanie dzienników historii i planowania planów</span><span class="sxs-lookup"><span data-stu-id="ea7b8-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ea7b8-120">Stosowanie filtrów do planu</span><span class="sxs-lookup"><span data-stu-id="ea7b8-120">Apply filters to a plan</span></span>](plan-filters.md)