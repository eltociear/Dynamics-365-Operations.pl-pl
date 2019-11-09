---
title: Optymalizowanie wydajności za pomocą zadań automatycznego czyszczenia
description: W tym temacie wyjaśniono, jak rozwiązywać pewne problemy z wydajnością w Microsoft Dynamics 365 Talent, czyszcząc historię zadań wsadowych.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 1e9d237817024800ad9880ec58db3505ac1c493f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027091"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="5d232-103">Optymalizowanie wydajności za pomocą zadań automatycznego czyszczenia</span><span class="sxs-lookup"><span data-stu-id="5d232-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d232-104">**Wystawienie**</span><span class="sxs-lookup"><span data-stu-id="5d232-104">**Issue**</span></span>

<span data-ttu-id="5d232-105">Microsoft Dynamics 365 Talent może napotkać problemy z wydajnością, jeśli historia zadania wsadowego rozrasta się zbyt dużą.</span><span class="sxs-lookup"><span data-stu-id="5d232-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="5d232-106">**Powód**</span><span class="sxs-lookup"><span data-stu-id="5d232-106">**Cause**</span></span>

<span data-ttu-id="5d232-107">Często wykonywane zadania wsadowe mogą prowadzić do nietrwałego wzrostu historii zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="5d232-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="5d232-108">Może to spowodować problemy z wydajnością.</span><span class="sxs-lookup"><span data-stu-id="5d232-108">This can cause performance issues.</span></span> 

<span data-ttu-id="5d232-109">**Rozdzielczość**</span><span class="sxs-lookup"><span data-stu-id="5d232-109">**Resolution**</span></span>

<span data-ttu-id="5d232-110">Umożliwia zaplanowanie automatycznego zadania w celu oczyszczenia historii zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5d232-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="5d232-111">Zalecamy skonfigurowanie zadania, aby było uruchamiane co tydzień, ale może być konieczne ręczne uruchomienie procesu oczyszczania w zależności od używanego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5d232-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="5d232-112">Poniższa procedura zawiera zalecane ustawienia, ale można je zmienić zgodnie z potrzebami użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5d232-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="5d232-113">W talentów wybierz opcję **Administracja systemu**.</span><span class="sxs-lookup"><span data-stu-id="5d232-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="5d232-114">Na pasku **wyszukiwania** wprowadź **oczyszczanie historii zadań wsadowych**.</span><span class="sxs-lookup"><span data-stu-id="5d232-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Wyszukaj okresowe oczyszczanie historii zadań wsadowych](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="5d232-116">W polu **Limit historii (dni)** wprowadź **30**.</span><span class="sxs-lookup"><span data-stu-id="5d232-116">In **History limit (days)**, enter **30**.</span></span>

   ![Ustaw limit historii 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="5d232-118">Wybierz **Uruchom w tle**, a następnie **Cykl**.</span><span class="sxs-lookup"><span data-stu-id="5d232-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Ustaw cykl](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="5d232-120">W obszarze **Zdefiniujcykl** ustaw **datę rozpoczęcia** i **godzinę rozpoczęcia** w godzinach poza godziną lub weekendu, a następnie wybierz opcję **brak daty zakończenia**.</span><span class="sxs-lookup"><span data-stu-id="5d232-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definiowanie daty i godziny rozpoczęcia](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="5d232-122">W **wzorzec cyklu** wybierz **dni**, a następnie ustaw opcję **Powtarzaj po określonym przedziale** na **7**.</span><span class="sxs-lookup"><span data-stu-id="5d232-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Ustawienie oczyszczania powoduje powtarzanie tygodnia](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="5d232-124">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d232-124">Select **OK**.</span></span>

8. <span data-ttu-id="5d232-125">W razie potrzeby zmień dowolne inne parametry w obszarze **Uruchom w tle**, a następnie wybierz przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d232-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>
