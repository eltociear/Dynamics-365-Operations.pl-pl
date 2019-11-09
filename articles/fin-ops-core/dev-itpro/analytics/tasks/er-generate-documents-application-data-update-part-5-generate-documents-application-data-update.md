---
title: Generowanie dokumentów zawierających dane aplikacji
description: Aby wykonać kroki opisane w tej procedurze, należy najpierw wykonać procedurę „ER Generowanie dokumentów z aktualizacją danych aplikacji (Część 4 — Modyfikowanie formatu)”.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d95feb3395c36f9cf8a23770dc3173377067d9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184883"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="9c18f-103">Generowanie dokumentów zawierających dane aplikacji</span><span class="sxs-lookup"><span data-stu-id="9c18f-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c18f-104">Aby wykonać kroki opisane w tej procedurze, należy najpierw wykonać procedurę „ER Generowanie dokumentów z aktualizacją danych aplikacji (Część 4: Modyfikowanie formatu)”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="9c18f-105">Etapy w tej procedurze wyjaśniają sposób projektowania konfiguracji raportowania elektronicznego (ER) do generowania dokumentu elektronicznego i aktualizowania danych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9c18f-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="9c18f-106">W tej procedurze uruchomisz konfigurację formatu ER, aby wygenerować raport Intrastat i zaktualizować dane aplikacji w celu zarchiwizowania szczegółów procesu raportowania.</span><span class="sxs-lookup"><span data-stu-id="9c18f-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="9c18f-107">Ta procedura została utworzona dla użytkowników z przypisaną rola administratora systemu lub dewelopera raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="9c18f-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="9c18f-108">Kroki można wykonać przy użyciu zestawu danych firmy DEMF.</span><span class="sxs-lookup"><span data-stu-id="9c18f-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="9c18f-109">Przed rozpoczęciem upewnij się, że kontekstem kraju firmy DEMF jest BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="9c18f-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="9c18f-110">Konfigurowanie parametrów handlu zagranicznego</span><span class="sxs-lookup"><span data-stu-id="9c18f-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="9c18f-111">Wybierz kolejno opcje Podatek > Ustawienia > Handel zagraniczny > Parametry handlu zagranicznego.</span><span class="sxs-lookup"><span data-stu-id="9c18f-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="9c18f-112">Kliknij kartę Sekwencje numerów.</span><span class="sxs-lookup"><span data-stu-id="9c18f-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="9c18f-113">Archiwizując szczegóły procesu raportowania Intrastat, musimy identyfikować rekordy każdego tworzonego archiwum.</span><span class="sxs-lookup"><span data-stu-id="9c18f-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="9c18f-114">Do tego celu należy skonfigurować specjalną numerację.</span><span class="sxs-lookup"><span data-stu-id="9c18f-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="9c18f-115">Wybierz odwołanie „Identyfikator archiwum Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="9c18f-116">W polu Kod sekwencji numerów wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="9c18f-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="9c18f-117">W polu „Kod sekwencji numerów” wprowadź lub wybierz wartość „Fore_2”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="9c18f-118">Rozstrzygnij zmiany w kodzie numeracji.</span><span class="sxs-lookup"><span data-stu-id="9c18f-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="9c18f-119">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9c18f-119">Click Save.</span></span>
7. <span data-ttu-id="9c18f-120">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9c18f-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="9c18f-121">Uruchamianie zmodyfikowanego formatu ER</span><span class="sxs-lookup"><span data-stu-id="9c18f-121">Run modified ER format</span></span>
1. <span data-ttu-id="9c18f-122">Wybierz kolejno opcje Administrowanie organizacją > Raportowanie elektroniczne > Konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="9c18f-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9c18f-123">W drzewie rozwiń węzeł „Intrastat (model)”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="9c18f-124">W drzewie zaznacz element „Intrastat (model)\Intrastat (format)”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="9c18f-125">Kliknij przycisk Uruchom.</span><span class="sxs-lookup"><span data-stu-id="9c18f-125">Click Run.</span></span>
5. <span data-ttu-id="9c18f-126">W polu Wprowadź nazwę pliku wpisz „intrastat2.xml”.</span><span class="sxs-lookup"><span data-stu-id="9c18f-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="9c18f-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="9c18f-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="9c18f-128">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="9c18f-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="9c18f-129">Przejrzenie wyników wykonania formatu ER</span><span class="sxs-lookup"><span data-stu-id="9c18f-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="9c18f-130">Przejrzyj wygenerowany plik XML.</span><span class="sxs-lookup"><span data-stu-id="9c18f-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="9c18f-131">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9c18f-131">Close the page.</span></span>
2. <span data-ttu-id="9c18f-132">Wybierz kolejno opcje Podatek > Deklaracje > Handel zagraniczny > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="9c18f-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="9c18f-133">Otwórz ten formularz zawierający transakcje Intrastat, które uwzględniono w wygenerowanym dokumencie elektronicznym.</span><span class="sxs-lookup"><span data-stu-id="9c18f-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="9c18f-134">Kliknij opcję Archiwum Intrastat.</span><span class="sxs-lookup"><span data-stu-id="9c18f-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="9c18f-135">Ponieważ wykonany format raportowania elektronicznego zawiera teraz ustawienia aktualizacji danych aplikacji, szczegóły gotowego raportu Intrastat zostały zarchiwizowane.</span><span class="sxs-lookup"><span data-stu-id="9c18f-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="9c18f-136">W tym formularzu widać rekord nagłówka utworzonego archiwum.</span><span class="sxs-lookup"><span data-stu-id="9c18f-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="9c18f-137">Kliknij przycisk Szczegóły.</span><span class="sxs-lookup"><span data-stu-id="9c18f-137">Click Details.</span></span>
    * <span data-ttu-id="9c18f-138">W tym formularzu widać szczegóły utworzonego archiwum.</span><span class="sxs-lookup"><span data-stu-id="9c18f-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="9c18f-139">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9c18f-139">Close the page.</span></span>
6. <span data-ttu-id="9c18f-140">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9c18f-140">Close the page.</span></span>
7. <span data-ttu-id="9c18f-141">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9c18f-141">Close the page.</span></span>
