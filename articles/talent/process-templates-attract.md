---
title: Tworzenie szablonu procesu w aplikacji Attract
description: Ten temat zawiera informacje o sposobie tworzenia szablonu procesu w aplikacji Attract.
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: pl-pl
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="1ff31-103">Tworzenie szablonu procesu w aplikacji Attract</span><span class="sxs-lookup"><span data-stu-id="1ff31-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ff31-104">*Szablon procesu rekrutacji* zawiera wszystkie działania, które należy wykonać w procesie rekrutacji na funkcję.</span><span class="sxs-lookup"><span data-stu-id="1ff31-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="1ff31-105">W tym temacie opisano elementy szablonu procesu w aplikacji Microsoft Dynamics 365 for Talent Attract.</span><span class="sxs-lookup"><span data-stu-id="1ff31-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="1ff31-106">Ponadto wyjaśniono, jak utworzyć szablon.</span><span class="sxs-lookup"><span data-stu-id="1ff31-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="1ff31-107">Tworzenie szablonu to funkcjonalność dostępna w dodatku kompleksowej obsługi rekrutacji dla aplikacji Attract.</span><span class="sxs-lookup"><span data-stu-id="1ff31-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="1ff31-108">Zarządzanie szablonami</span><span class="sxs-lookup"><span data-stu-id="1ff31-108">Template management</span></span>

<span data-ttu-id="1ff31-109">Organizacje mogą zdecydować, czy wszyscy członkowie zespołu czy tylko administratorzy mogą tworzyć szablony procesów w aplikacji Attract.</span><span class="sxs-lookup"><span data-stu-id="1ff31-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="1ff31-110">Aby skonfigurować funkcjonalność zarządzania szablonami, wybierz kolejno opcje **Centrum administracyjne** \> **Zarządzanie szablonami**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="1ff31-111">Aby umożliwić członkom zespołu tworzenie własnych szablonów, włącz funkcję zarządzania szablonami.</span><span class="sxs-lookup"><span data-stu-id="1ff31-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="1ff31-112">Jeśli nie włączysz funkcjonalności zarządzania szablonami, to tylko administratorzy będą mogli tworzyć szablony.</span><span class="sxs-lookup"><span data-stu-id="1ff31-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="1ff31-113">Szablon domyślny</span><span class="sxs-lookup"><span data-stu-id="1ff31-113">Default template</span></span>

<span data-ttu-id="1ff31-114">Tylko administratorzy mogą ustawić szablon domyślny.</span><span class="sxs-lookup"><span data-stu-id="1ff31-114">Only admins can set the default template.</span></span> <span data-ttu-id="1ff31-115">Szablon domyślny jest używany, jeśli nie wybrano szablonu podczas tworzenia funkcji.</span><span class="sxs-lookup"><span data-stu-id="1ff31-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="1ff31-116">Aby skonfigurować szablon domyślny, wybierz kolejno opcje **Centrum administracyjne** \> **Zarządzanie szablonami**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="1ff31-117">Na karcie szablonu, który ma być szablonem domyślnym, naciśnij przycisk wielokropka (**...**), a następnie wybierz opcję **Ustaw jako domyślny**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="1ff31-118">Tworzenie szablonu procesu</span><span class="sxs-lookup"><span data-stu-id="1ff31-118">Create a process template</span></span>

<span data-ttu-id="1ff31-119">Administratorzy, osoby rekrutujące i menedżerowie zatrudniający mogą tworzyć szablony procesów.</span><span class="sxs-lookup"><span data-stu-id="1ff31-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="1ff31-120">Szablon procesu składa się z *etapów* i *działań*.</span><span class="sxs-lookup"><span data-stu-id="1ff31-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="1ff31-121">Etapy grupują jedno lub więcej działań.</span><span class="sxs-lookup"><span data-stu-id="1ff31-121">Stages group together one or more activities.</span></span> <span data-ttu-id="1ff31-122">Domyślnie każdy szablon procesu ma działania Prospekt, Zgłoszenie i Oferta.</span><span class="sxs-lookup"><span data-stu-id="1ff31-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="1ff31-123">Można zmieniać nazwy etapów zawierających te działania.</span><span class="sxs-lookup"><span data-stu-id="1ff31-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="1ff31-124">Można dodać więcej etapów, klikając przycisk **+ Nowy etap**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="1ff31-125">W celu dodania działań do etapu można je przeciągnąć do odpowiedniego etapu albo kliknąć dwukrotnie na liście działań.</span><span class="sxs-lookup"><span data-stu-id="1ff31-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="1ff31-126">Nazwy etapów są widoczne dla kandydatów na stronie **Stan zgłoszenia**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="1ff31-127">Weź to pod uwagę, wybierając nazwy dla etapów.</span><span class="sxs-lookup"><span data-stu-id="1ff31-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="1ff31-128">Aby uzyskać więcej informacji o działaniach, zobacz [Działania w ramach procesu zatrudniania w aplikacji Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="1ff31-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="1ff31-129">Aby utworzyć szablon procesu rekrutacji, wykonaj poniższe czynności.</span><span class="sxs-lookup"><span data-stu-id="1ff31-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="1ff31-130">Przejdź do okna **Szablony**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="1ff31-131">Wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-131">Select **New**.</span></span>
3. <span data-ttu-id="1ff31-132">W polu **Nazwa szablonu** nadaj szablonowi nazwę, a następnie kliknij przycisk **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="1ff31-133">Na liście **Wybierz proces zatwierdzania** wybierz pozycję **Domyślnie**, aby wprowadzić wymóg zatwierdzenia kandydatury na funkcję.</span><span class="sxs-lookup"><span data-stu-id="1ff31-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="1ff31-134">Włącz lub wyłącz pozwolenie na istnienie prospektów.</span><span class="sxs-lookup"><span data-stu-id="1ff31-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="1ff31-135">Opcjonalnie: dodaj lub usuń etapy.</span><span class="sxs-lookup"><span data-stu-id="1ff31-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="1ff31-136">Aby dodać etap, wybierz opcję **+ Nowy etap**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="1ff31-137">Aby usunąć etap, umieść nad nim wskaźnik myszy, a następnie kliknij wyświetloną ikonę kosza.</span><span class="sxs-lookup"><span data-stu-id="1ff31-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1ff31-138">Nie można usunąć etapów Prospekt, Zgłoszenie ani Oferta, ale można zmienić ich nazwy.</span><span class="sxs-lookup"><span data-stu-id="1ff31-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="1ff31-139">Opcjonalnie: dodaj lub usuń działania.</span><span class="sxs-lookup"><span data-stu-id="1ff31-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="1ff31-140">Aby dodać działanie, przeciągnij je z listy po prawej stronie do odpowiedniego etapu.</span><span class="sxs-lookup"><span data-stu-id="1ff31-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="1ff31-141">Alternatywnie kliknij dwukrotnie działanie, a następnie wybierz etap, do którego chcesz je dodać.</span><span class="sxs-lookup"><span data-stu-id="1ff31-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="1ff31-142">Aby usunąć działanie, rozwiń je, a następnie kliknij przycisk kosza w nagłówku działania.</span><span class="sxs-lookup"><span data-stu-id="1ff31-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="1ff31-143">Wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="1ff31-143">Select **Save**.</span></span>
