---
title: ER Importowanie konfiguracji z usługi Lifecycle Services
description: W poniższych krokach wyjaśniono, jak użytkownik w roli Administrator systemu lub Deweloper raportowania elektronicznego może zaimportować nową wersję konfiguracji raportowania elektronicznego (ER) z usługi Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184837"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="124f6-103">ER Importowanie konfiguracji z usługi Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="124f6-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="124f6-104">W poniższych krokach wyjaśniono, jak użytkownik w roli Administrator systemu lub Deweloper raportowania elektronicznego może zaimportować nową wersję konfiguracji raportowania elektronicznego (ER) z usługi Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="124f6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="124f6-105">W tym przykładzie wybierzesz żądaną wersję konfiguracji raportowania elektronicznego dla przykładowej firmy Litware, Inc. i zaimportujesz ją. Podane kroki można wykonać w dowolnej firmie, ponieważ konfiguracje ER są współużytkowane przez wszystkie firmy.</span><span class="sxs-lookup"><span data-stu-id="124f6-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="124f6-106">Aby wykonać te kroki, należy najpierw wykonać kroki w procedurze „Przekazywanie konfiguracji ER do usługi Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="124f6-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="124f6-107">W celu wykonania tych kroków jest również wymagany dostęp do usługi LCS.</span><span class="sxs-lookup"><span data-stu-id="124f6-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="124f6-108">Wybierz kolejno opcje Administrowanie organizacją > Obszary robocze > Raportowanie elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="124f6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="124f6-109">Kliknij opcję Konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="124f6-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="124f6-110">Usuwanie udostępnionej wersji konfiguracji modelu danych</span><span class="sxs-lookup"><span data-stu-id="124f6-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="124f6-111">W drzewie zaznacz element „Konfiguracja przykładowego modelu”.</span><span class="sxs-lookup"><span data-stu-id="124f6-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="124f6-112">Pierwsza wersja konfiguracji przykładowego modelu danych została utworzona i opublikowana w usłudze LCS podczas procedury „Przekazywanie konfiguracji ER do usługi Lifecycle Services”.</span><span class="sxs-lookup"><span data-stu-id="124f6-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="124f6-113">W tej procedurze usuniesz tę wersję konfiguracji raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="124f6-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="124f6-114">Ta wersja konfiguracji przykładowego modelu danych zostanie zaimportowana później z usługi LCS.</span><span class="sxs-lookup"><span data-stu-id="124f6-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="124f6-115">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="124f6-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="124f6-116">Zaznacz wersję tej konfiguracji mającą stan „Udostępniono”.</span><span class="sxs-lookup"><span data-stu-id="124f6-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="124f6-117">Ten stan wskazuje, że konfiguracja została opublikowana w usłudze LCS.</span><span class="sxs-lookup"><span data-stu-id="124f6-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="124f6-118">Kliknij przycisk Zmień stan.</span><span class="sxs-lookup"><span data-stu-id="124f6-118">Click Change status.</span></span>
4. <span data-ttu-id="124f6-119">Kliknij opcję Nie kontynuuj.</span><span class="sxs-lookup"><span data-stu-id="124f6-119">Click Discontinue.</span></span>
    * <span data-ttu-id="124f6-120">Zmień stan wybranej wersji z „Udostępniono” na „Zaprzestano”, aby ją udostępnić do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="124f6-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="124f6-121">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="124f6-121">Click OK.</span></span>
6. <span data-ttu-id="124f6-122">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="124f6-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="124f6-123">Zaznacz wersję tej konfiguracji mającą stan „Zaprzestano”.</span><span class="sxs-lookup"><span data-stu-id="124f6-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="124f6-124">Kliknij przycisk Usuń.</span><span class="sxs-lookup"><span data-stu-id="124f6-124">Click Delete.</span></span>
8. <span data-ttu-id="124f6-125">Kliknij przycisk Tak.</span><span class="sxs-lookup"><span data-stu-id="124f6-125">Click Yes.</span></span>
    * <span data-ttu-id="124f6-126">Należy zauważyć, że jest dostępna tylko wersja robocza 2 wybranej konfiguracji przykładowego modelu danych.</span><span class="sxs-lookup"><span data-stu-id="124f6-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="124f6-127">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="124f6-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="124f6-128">Importowanie udostępnionej wersji konfiguracji modelu danych z usługi LCS</span><span class="sxs-lookup"><span data-stu-id="124f6-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="124f6-129">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="124f6-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="124f6-130">Otwórz listę repozytoriów dostawcy konfiguracji, czyli firmy</span><span class="sxs-lookup"><span data-stu-id="124f6-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="124f6-131">firmy Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="124f6-131">configuration provider.</span></span>  
2. <span data-ttu-id="124f6-132">Kliknij Repozytoria.</span><span class="sxs-lookup"><span data-stu-id="124f6-132">Click Repositories.</span></span>
3. <span data-ttu-id="124f6-133">Kliknij przycisk Otwórz.</span><span class="sxs-lookup"><span data-stu-id="124f6-133">Click Open.</span></span>
    * <span data-ttu-id="124f6-134">Zaznacz repozytorium usługi LCS i je otwórz.</span><span class="sxs-lookup"><span data-stu-id="124f6-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="124f6-135">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="124f6-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="124f6-136">Na liście wersji zaznacz pierwszą wersję konfiguracji przykładowego modelu.</span><span class="sxs-lookup"><span data-stu-id="124f6-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="124f6-137">Kliknij przycisk Importuj.</span><span class="sxs-lookup"><span data-stu-id="124f6-137">Click Import.</span></span>
6. <span data-ttu-id="124f6-138">Kliknij przycisk Tak.</span><span class="sxs-lookup"><span data-stu-id="124f6-138">Click Yes.</span></span>
    * <span data-ttu-id="124f6-139">Potwierdź import wybranej wersji z usługi LCS.</span><span class="sxs-lookup"><span data-stu-id="124f6-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="124f6-140">Należy zauważyć, że komunikat informacyjny (nad formularzem) potwierdza pomyślne ukończenia importu wybranej wersji.</span><span class="sxs-lookup"><span data-stu-id="124f6-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="124f6-141">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="124f6-141">Close the page.</span></span>
8. <span data-ttu-id="124f6-142">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="124f6-142">Close the page.</span></span>
9. <span data-ttu-id="124f6-143">Kliknij opcję Konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="124f6-143">Click Configurations.</span></span>
10. <span data-ttu-id="124f6-144">W drzewie zaznacz element „Konfiguracja przykładowego modelu”.</span><span class="sxs-lookup"><span data-stu-id="124f6-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="124f6-145">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="124f6-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="124f6-146">Zaznacz wersję tej konfiguracji mającą stan „Udostępniono”.</span><span class="sxs-lookup"><span data-stu-id="124f6-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="124f6-147">Należy zauważyć, że teraz jest również dostępna udostępniona wersja 1 wybranej konfiguracji przykładowego modelu danych.</span><span class="sxs-lookup"><span data-stu-id="124f6-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  
