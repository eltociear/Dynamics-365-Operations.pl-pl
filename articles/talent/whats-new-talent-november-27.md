---
title: "Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (27 listopada 2018 r.)"
description: "W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: 6bd049bfe4639136276ab2f14e6310e45d1254f2
ms.contentlocale: pl-pl
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="122ae-103">Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (27 listopada 2018 r.)</span><span class="sxs-lookup"><span data-stu-id="122ae-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="122ae-104">**Kompilacja 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="122ae-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="122ae-105">W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Core HR.</span><span class="sxs-lookup"><span data-stu-id="122ae-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="122ae-106">Zmiany</span><span class="sxs-lookup"><span data-stu-id="122ae-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="122ae-107">Nie można utworzyć notatki w Zarządzaniu sprawami</span><span class="sxs-lookup"><span data-stu-id="122ae-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="122ae-108">Wprowadzono zmiany, aby rozwiązać problem występujący podczas próby edytowania lub tworzenia notatki w dzienniku spraw w Zarządzaniu sprawami.</span><span class="sxs-lookup"><span data-stu-id="122ae-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="122ae-109">Nieprawidłowo napisane słowo na karcie analityki w obszarze roboczym wynagrodzeń</span><span class="sxs-lookup"><span data-stu-id="122ae-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="122ae-110">Poprawiono pisownię pochodzenia etnicznego na wykresie analiz wynagrodzeń w obszarze roboczym wynagrodzeń.</span><span class="sxs-lookup"><span data-stu-id="122ae-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="122ae-111">Obszar roboczy samoobsługi pracownika nie wyświetla się, jeśli użytkownik nie jest przypisany do pracownika</span><span class="sxs-lookup"><span data-stu-id="122ae-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="122ae-112">Wprowadzono zmiany, gdy obszar roboczy **samoobsługa pracownika** jest wybrany jako strona początkowa przy rozruchu dla użytkownika, który nie jest przypisany do pracownika.</span><span class="sxs-lookup"><span data-stu-id="122ae-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="122ae-113">W takiej sytuacji jest wyświetlany domyślny pulpit nawigacyjny.</span><span class="sxs-lookup"><span data-stu-id="122ae-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="122ae-114">Błąd urlopów i nieobecności: obiekt odwołania nie jest ustawiony na wystąpienie obiektu</span><span class="sxs-lookup"><span data-stu-id="122ae-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="122ae-115">Wprowadzono zmiany do urlopów i nieobecności, aby rozwiązać ten problem po zatwierdzeniu rekordów urlopów i nieobecności na liście **elementy pracy przypisane do mnie**.</span><span class="sxs-lookup"><span data-stu-id="122ae-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="122ae-116">Nie można wznowić przepływu pracy obrazu</span><span class="sxs-lookup"><span data-stu-id="122ae-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="122ae-117">Po wznowieniu przepływ pracy obrazu, przepływ pracy zostanie ustawiony jako „anulowany” i istniejące żądanie można usunąć w obszarze roboczym samoobsługi pracowników.</span><span class="sxs-lookup"><span data-stu-id="122ae-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="122ae-118">Ponownie zatrudnieni pracownicy lub zleceniobiorcy pokazują się wiele razy po zakończeniu umowy</span><span class="sxs-lookup"><span data-stu-id="122ae-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="122ae-119">Ta aktualizacja sprawia, że zwolnieni i ponownie zatrudnieni pracownicy będą wyświetlani tylko raz na liście „odeszli”.</span><span class="sxs-lookup"><span data-stu-id="122ae-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="122ae-120">Znany problem</span><span class="sxs-lookup"><span data-stu-id="122ae-120">Known issue</span></span>

- <span data-ttu-id="122ae-121">**Problem**: Podczas dodawania nowego załącznika do pracownika przyciski **Nowy** i **Edytuj** są wyszarzone.</span><span class="sxs-lookup"><span data-stu-id="122ae-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="122ae-122">**Obejście:** Przed otwarciem strony załącznika upewnij się, że pola informacji na stronie **Pracownik** są zamknięte.</span><span class="sxs-lookup"><span data-stu-id="122ae-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="122ae-123">Jeśli pola informacji są zamknięte podczas wczytywania strony **Pracownik**, przyciski złączników będą włączone.</span><span class="sxs-lookup"><span data-stu-id="122ae-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="122ae-124">(Ten problem zostanie rozwiązany w następnej aktualizacji platformy).</span><span class="sxs-lookup"><span data-stu-id="122ae-124">(This issue will be fixed in the next platform update.)</span></span>
