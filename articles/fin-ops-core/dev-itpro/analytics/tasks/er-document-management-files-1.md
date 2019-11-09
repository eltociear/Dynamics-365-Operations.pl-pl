---
title: ER Używanie plików zarządzania dokumentami w danych wyjściowych formatu (Część 1 — Przygotowanie modelu danych)
description: W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli administratora systemu lub dewelopera raportowania elektronicznego może tak skonfigurować format raportowania elektronicznego (ER), aby w danych wyjściowych raportowania elektronicznego używać plików zarządzania danymi (załączników).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29c13e729223a98d7f45244c5a796bca6e3baaf3
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550840"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="06162-103">ER Używanie plików zarządzania dokumentami w danych wyjściowych formatu (Część 1 — Przygotowanie modelu danych)</span><span class="sxs-lookup"><span data-stu-id="06162-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06162-104">W poniższych krokach wyjaśniono, jak użytkownik przypisany do roli administratora systemu lub dewelopera raportowania elektronicznego może tak skonfigurować format raportowania elektronicznego (ER), aby w danych wyjściowych raportowania elektronicznego używać plików zarządzania danymi (załączników).</span><span class="sxs-lookup"><span data-stu-id="06162-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="06162-105">Kroki można wykonać na danych dowolnej firmy.</span><span class="sxs-lookup"><span data-stu-id="06162-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="06162-106">Aby wykonać te kroki, należy najpierw wykonać kroki w procedurze „Tworzenie dostawcy konfiguracji i oznaczanie go jako aktywnego”.</span><span class="sxs-lookup"><span data-stu-id="06162-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="06162-107">Procedura dotyczy funkcji dodanej w programie Dynamics 365 for Operations w wersji 1611.</span><span class="sxs-lookup"><span data-stu-id="06162-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="06162-108">Uzyskiwanie dostępu do listy konfiguracji dostarczanej przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="06162-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="06162-109">Wybierz kolejno opcje Administrowanie organizacją > Obszary robocze > Raportowanie elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="06162-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="06162-110">Upewnij się, że dostawca „Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="06162-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="06162-111">jest dostępny i oznaczony jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="06162-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="06162-112">Zaznacz dostawcę „Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="06162-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="06162-113"> </span><span class="sxs-lookup"><span data-stu-id="06162-113">provider.</span></span>
3. <span data-ttu-id="06162-114">Kliknij Repozytoria.</span><span class="sxs-lookup"><span data-stu-id="06162-114">Click Repositories.</span></span>
    * <span data-ttu-id="06162-115">Jeśli repozytorium typu „Zasoby operacyjne” już istnieje, należy pominąć pozostałe kroki bieżącego zadania podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="06162-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="06162-116">Kliknij przycisk Dodaj, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="06162-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="06162-117">W polu Typ repozytorium konfiguracji wprowadź wartość „Zasoby operacyjne”.</span><span class="sxs-lookup"><span data-stu-id="06162-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="06162-118">Kliknij opcję Utwórz repozytorium.</span><span class="sxs-lookup"><span data-stu-id="06162-118">Click Create repository.</span></span>
7. <span data-ttu-id="06162-119">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="06162-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="06162-120">Pobieranie konfiguracje modelu faktur sprzedaży dostarczonych przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="06162-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="06162-121">Kliknij przycisk Pokaż filtry.</span><span class="sxs-lookup"><span data-stu-id="06162-121">Click Show filters.</span></span>
2. <span data-ttu-id="06162-122">Zastosuj następujące filtry: w polu „Nazwa” wprowadź wartość filtru „Zasoby operacyjne”, używając operatora filtru „zaczyna się od”; w polu „Opis” wprowadź wartość filtru "", używając operatora filtru „zaczyna się od”</span><span class="sxs-lookup"><span data-stu-id="06162-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="06162-123">Kliknij przycisk Pokaż filtry.</span><span class="sxs-lookup"><span data-stu-id="06162-123">Click Show filters.</span></span>
4. <span data-ttu-id="06162-124">Kliknij przycisk Otwórz.</span><span class="sxs-lookup"><span data-stu-id="06162-124">Click Open.</span></span>
5. <span data-ttu-id="06162-125">W drzewie zaznacz element „Model faktur sprzedaży”.</span><span class="sxs-lookup"><span data-stu-id="06162-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="06162-126">Zaznacz konfigurację modelu „Model faktur sprzedaży”, aby ją zaimportować.</span><span class="sxs-lookup"><span data-stu-id="06162-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="06162-127">Kliknij przycisk Importuj.</span><span class="sxs-lookup"><span data-stu-id="06162-127">Click Import.</span></span>
    * <span data-ttu-id="06162-128">Kliknij przycisk Importuj dla wersji 1 wybranej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="06162-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="06162-129">Kliknij przycisk Tak.</span><span class="sxs-lookup"><span data-stu-id="06162-129">Click Yes.</span></span>
8. <span data-ttu-id="06162-130">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="06162-130">Close the page.</span></span>
9. <span data-ttu-id="06162-131">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="06162-131">Close the page.</span></span>
10. <span data-ttu-id="06162-132">Kliknij opcję Konfiguracje raportowania.</span><span class="sxs-lookup"><span data-stu-id="06162-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="06162-133">W drzewie zaznacz element „Model faktur sprzedaży”.</span><span class="sxs-lookup"><span data-stu-id="06162-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="06162-134">Utwórz pochodny model w celu umożliwienia dostępu do plików zarządzania dokumentami.</span><span class="sxs-lookup"><span data-stu-id="06162-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="06162-135">Utworzysz własną konfigurację modelu faktur sprzedaży na podstawie konfiguracji dostarczonej przez firmę Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06162-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="06162-136">Użyjesz tej konfiguracji w celu zaimplementowania dostępu do plików zarządzania dokumentami oraz udostępnienia ich dla dokumentów elektronicznych, które zostaną utworzone na podstawie tego modelu.</span><span class="sxs-lookup"><span data-stu-id="06162-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="06162-137">Kliknij przycisk Utwórz konfigurację, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="06162-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="06162-138">W polu Nowy wprowadź wyrażenie „Pochodzi od nazwy: Model faktur sprzedaży, Microsoft”.</span><span class="sxs-lookup"><span data-stu-id="06162-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="06162-139">W polu Nazwa wpisz „Model faktur sprzedaży (niestandardowy)”.</span><span class="sxs-lookup"><span data-stu-id="06162-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="06162-140">Model faktur sprzedaży (niestandardowy)</span><span class="sxs-lookup"><span data-stu-id="06162-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="06162-141">Kliknij przycisk Utwórz konfigurację.</span><span class="sxs-lookup"><span data-stu-id="06162-141">Click Create configuration.</span></span>
