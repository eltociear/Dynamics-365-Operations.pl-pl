---
title: "Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (16 października 2018 r.)"
description: "W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.contentlocale: pl-pl
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="2b2db-103">Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (19 października 2018 r.)</span><span class="sxs-lookup"><span data-stu-id="2b2db-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="2b2db-104">**Kompilacja 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="2b2db-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="2b2db-105">W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Core HR.</span><span class="sxs-lookup"><span data-stu-id="2b2db-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="2b2db-106">Zezwalanie menedżerom na aktualizowanie wniosków o czas wolny</span><span class="sxs-lookup"><span data-stu-id="2b2db-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="2b2db-107">Wnioski pracowników o czas wolny mogą wymagać aktualizacji po zatwierdzeniu za pośrednictwem przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="2b2db-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="2b2db-108">W wielu przypadkach menedżer dokonuje tych aktualizacji w imieniu pracownika.</span><span class="sxs-lookup"><span data-stu-id="2b2db-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="2b2db-109">Ta nowa funkcja umożliwia menedżerom aktualizowanie lub anulowanie wniosków o czas wolny w imieniu podległych pracowników.</span><span class="sxs-lookup"><span data-stu-id="2b2db-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="2b2db-110">Ta funkcja jest kontrolowana przez parametr **Praca w imieniu**, który można ustawić na stronie **Parametry zasobów ludzkich**.</span><span class="sxs-lookup"><span data-stu-id="2b2db-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="2b2db-111">Zezwalanie działowi kadr na aktualizowanie wniosków o czas wolny</span><span class="sxs-lookup"><span data-stu-id="2b2db-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="2b2db-112">Wnioski pracowników o czas wolny mogą wymagać aktualizacji przez dział kadr, mimo iż wcześniej zostały zatwierdzone przy użyciu przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="2b2db-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="2b2db-113">Ta funkcja umożliwia użytkownikom z działu kadr aktualizowanie wniosków o czas wolny.</span><span class="sxs-lookup"><span data-stu-id="2b2db-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="2b2db-114">Funkcja jest włączana w obszarze roboczym **Osoby** oraz na stronie **Pracownik** za pomocą nowej opcji o nazwie **Wyświetl czas wolny**.</span><span class="sxs-lookup"><span data-stu-id="2b2db-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="2b2db-115">Na tych stronach użytkownicy z działu kadr mogą przeglądać wnioski i aktualizować operacje przyznania czasu wolnego, podobnie jak mogą to robić menedżerowie.</span><span class="sxs-lookup"><span data-stu-id="2b2db-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="2b2db-116">Dostęp do tej funkcjonalności jest kontrolowany przez następujący obowiązek zabezpieczeń:</span><span class="sxs-lookup"><span data-stu-id="2b2db-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="2b2db-117">Obowiązek: Obsługa procesów urlopów i nieobecności specyficznych dla pracownika.</span><span class="sxs-lookup"><span data-stu-id="2b2db-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="2b2db-118">Uprawnienie: Obsługa wniosków o urlopy i nieobecności dla wszystkich pracowników.</span><span class="sxs-lookup"><span data-stu-id="2b2db-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="2b2db-119">Inne zmiany</span><span class="sxs-lookup"><span data-stu-id="2b2db-119">Other changes</span></span>
<span data-ttu-id="2b2db-120">Następujące aktualizacje zostały wprowadzone w tej wersji:</span><span class="sxs-lookup"><span data-stu-id="2b2db-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="2b2db-121">Zmieniono czynności zatrudniania pracownika, tak aby nie „zawieszał się” w stanie **Przepływ pracy zakończony**.</span><span class="sxs-lookup"><span data-stu-id="2b2db-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="2b2db-122">Teraz można utworzyć rekord zatrudnienia bez daty rozpoczęcia zatrudnienia.</span><span class="sxs-lookup"><span data-stu-id="2b2db-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="2b2db-123">W aplikacji Dynamics 365 for Talent data rejestracji na szkolenie wyświetlane w oknie Samoobsługa pracownika etatowego teraz jest korygowana o strefę czasową.</span><span class="sxs-lookup"><span data-stu-id="2b2db-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="2b2db-124">Pliki programu Excel można importować wielokrotnie za pomocą jednostki **Pracownik etatowy** bez powodowania błędów.</span><span class="sxs-lookup"><span data-stu-id="2b2db-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="2b2db-125">Znany problem</span><span class="sxs-lookup"><span data-stu-id="2b2db-125">Known issue</span></span>

- <span data-ttu-id="2b2db-126">**Problem**: Podczas dodawania nowego załącznika do pracownika przyciski **Nowy** i **Edytuj** są wyszarzone.</span><span class="sxs-lookup"><span data-stu-id="2b2db-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="2b2db-127">**Obejście:** Przed otwarciem strony załącznika upewnij się, że pola informacji na stronie **Pracownik** są zamknięte.</span><span class="sxs-lookup"><span data-stu-id="2b2db-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="2b2db-128">Jeśli pola informacji są zamknięte podczas wczytywania strony **Pracownik**, przyciski złączników będą włączone.</span><span class="sxs-lookup"><span data-stu-id="2b2db-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="2b2db-129">(Ten problem zostanie rozwiązany w następnej aktualizacji platformy).</span><span class="sxs-lookup"><span data-stu-id="2b2db-129">(This issue will be fixed in the next platform update.)</span></span>
