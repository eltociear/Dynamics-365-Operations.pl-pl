---
title: Wybieranie definicji modeli danych podczas tworzenia formatów
description: Aby wykonać kroki podane w tej procedurze, należy najpierw wykonać procedurę ER Tworzenie dostawcy konfiguracji i oznaczanie go jako aktywnego.
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
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184722"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="94556-103">Wybieranie definicji modeli danych podczas tworzenia formatów</span><span class="sxs-lookup"><span data-stu-id="94556-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94556-104">Aby wykonać kroki podane w tej procedurze, należy najpierw wykonać procedurę ER Tworzenie dostawcy konfiguracji i oznaczanie go jako aktywnego.</span><span class="sxs-lookup"><span data-stu-id="94556-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="94556-105">W tej procedurze pokazano, jak można wybrać pozycję główną modelu jako definicję modelu danych w celu wstawienia konfiguracji formatu raportowania elektronicznego (ER) przeznaczonej do generowania dokumentów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="94556-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="94556-106">W tej procedurze dodasz nową konfigurację formatu ER dla przykładowej firmy „Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="94556-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="94556-107">Ta procedura jest przeznaczona dla użytkowników z przypisaną rola Administrator systemu lub Deweloper raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="94556-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="94556-108">Kroki można wykonać przy użyciu dowolnego zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="94556-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="94556-109">Wybierz kolejno opcje Administrowanie organizacją > Obszary robocze > Raportowanie elektroniczne.</span><span class="sxs-lookup"><span data-stu-id="94556-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="94556-110">Upewnij się, że dostawca konfiguracji przykładowej firmy Litware, Inc. jest dostępny i oznaczony jako Aktywny.</span><span class="sxs-lookup"><span data-stu-id="94556-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="94556-111">Jeśli ten dostawca konfiguracji nie jest widoczny, wykonaj procedurę Tworzenie dostawcy konfiguracji i oznaczanie go jako aktywnego.</span><span class="sxs-lookup"><span data-stu-id="94556-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="94556-112">Kliknij opcję Konfiguracje raportowania.</span><span class="sxs-lookup"><span data-stu-id="94556-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="94556-113">Dodawanie nowej konfiguracji modelu danych ER</span><span class="sxs-lookup"><span data-stu-id="94556-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="94556-114">Kliknij przycisk Utwórz konfigurację, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="94556-115">Dodaliśmy nową konfigurację modelu raportowania elektronicznego zawierającą model danych, który jest przeznaczony do używania jako źródło danych do generowania raportów ER.</span><span class="sxs-lookup"><span data-stu-id="94556-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="94556-116">W polu Nazwa wpisz „Model płatności (fikcyjny)”.</span><span class="sxs-lookup"><span data-stu-id="94556-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="94556-117">Model płatności (fikcyjny)</span><span class="sxs-lookup"><span data-stu-id="94556-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="94556-118">Kliknij przycisk Utwórz konfigurację.</span><span class="sxs-lookup"><span data-stu-id="94556-118">Click Create configuration.</span></span>
4. <span data-ttu-id="94556-119">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="94556-119">Click Designer.</span></span>
    * <span data-ttu-id="94556-120">Otwórz projektanta ER w celu określenia struktury modelu danych tej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="94556-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="94556-121">Załóżmy, że projektujemy model danych dla dziedziny płatności biznesowych do obsługi 2 metod płatności — polecenia przelewu i polecenia zapłaty.</span><span class="sxs-lookup"><span data-stu-id="94556-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="94556-122">Kliknij przycisk Nowy, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="94556-123">W polu Nazwa wpisz „Płatności — polecenie przelewu”.</span><span class="sxs-lookup"><span data-stu-id="94556-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="94556-124">Płatności — polecenie przelewu</span><span class="sxs-lookup"><span data-stu-id="94556-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="94556-125">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="94556-125">Click Add.</span></span>
8. <span data-ttu-id="94556-126">Kliknij przycisk Nowy, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="94556-127">W polu Nowy węzeł jako wpisz „Element główny modelu”.</span><span class="sxs-lookup"><span data-stu-id="94556-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="94556-128">W polu Nazwa wpisz „Płatności — polecenie zapłaty”.</span><span class="sxs-lookup"><span data-stu-id="94556-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="94556-129">Płatności — polecenie zapłaty</span><span class="sxs-lookup"><span data-stu-id="94556-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="94556-130">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="94556-130">Click Add.</span></span>
12. <span data-ttu-id="94556-131">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="94556-131">Click Save.</span></span>
13. <span data-ttu-id="94556-132">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="94556-132">Close the page.</span></span>
14. <span data-ttu-id="94556-133">Kliknij przycisk Zmień stan.</span><span class="sxs-lookup"><span data-stu-id="94556-133">Click Change status.</span></span>
    * <span data-ttu-id="94556-134">Wykonaj wersję roboczą modelu, tak aby była dostępna w mapowaniach i formatach nowego modelu.</span><span class="sxs-lookup"><span data-stu-id="94556-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="94556-135">Kliknij przycisk Wykonaj.</span><span class="sxs-lookup"><span data-stu-id="94556-135">Click Complete.</span></span>
16. <span data-ttu-id="94556-136">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="94556-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="94556-137">Rozpoczynanie wprowadzania nowej konfiguracji formatu ER</span><span class="sxs-lookup"><span data-stu-id="94556-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="94556-138">Kliknij przycisk Utwórz konfigurację, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="94556-139">W polu Nowy wpisz „Format oparty na modelu danych Model płatności (fikcyjny)”.</span><span class="sxs-lookup"><span data-stu-id="94556-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="94556-140">W polu Definicja modelu danych wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="94556-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="94556-141">Należy zwrócić uwagę, że wszystkie pozycje główne wybranego modelu danych są obecnie dostępne do wyboru jako definicja modelu danych.</span><span class="sxs-lookup"><span data-stu-id="94556-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="94556-142">Można kontynuować projektowanie formatu przy użyciu dowolnych potrzebnych pozycji głównych modelu danych.</span><span class="sxs-lookup"><span data-stu-id="94556-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="94556-143">Brak mapowania modelu dla wybranej pozycji głównej nie uniemożliwia kontynuowania.</span><span class="sxs-lookup"><span data-stu-id="94556-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="94556-144">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="94556-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="94556-145">Dodawanie nowej konfiguracji mapowania modelu ER</span><span class="sxs-lookup"><span data-stu-id="94556-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="94556-146">Kliknij przycisk Utwórz konfigurację, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="94556-147">W polu Nowy wpisz „Mapowanie modelu oparte na modelu danych Model płatności (fikcyjny)”.</span><span class="sxs-lookup"><span data-stu-id="94556-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="94556-148">W polu Nazwa wpisz „Mapowania modelu płatności (fikcyjnego)”.</span><span class="sxs-lookup"><span data-stu-id="94556-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="94556-149">Mapowania modelu płatności (fikcyjnego)</span><span class="sxs-lookup"><span data-stu-id="94556-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="94556-150">W polu Definicja modelu danych wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="94556-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="94556-151">Kliknij przycisk Utwórz konfigurację.</span><span class="sxs-lookup"><span data-stu-id="94556-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="94556-152">Projektowanie mapowań modeli ER</span><span class="sxs-lookup"><span data-stu-id="94556-152">Design ER model mappings</span></span>
1. <span data-ttu-id="94556-153">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="94556-153">Click Designer.</span></span>
    * <span data-ttu-id="94556-154">Za pomocą projektanta ER określ mapowania modelu dla wymaganych pozycji głównych.</span><span class="sxs-lookup"><span data-stu-id="94556-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="94556-155">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="94556-155">Click Designer.</span></span>
    * <span data-ttu-id="94556-156">Wykonaj symulację skonfigurowania mapowania wybranego modelu na pozycję główną wybranego modelu.</span><span class="sxs-lookup"><span data-stu-id="94556-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="94556-157">W drzewie zaznacz element „Dynamics 365 for Operations\Rekordy w tabeli”.</span><span class="sxs-lookup"><span data-stu-id="94556-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="94556-158">Kliknij opcję Dodaj element główny.</span><span class="sxs-lookup"><span data-stu-id="94556-158">Click Add root.</span></span>
5. <span data-ttu-id="94556-159">W polu Nazwa wprowadź „Księga”.</span><span class="sxs-lookup"><span data-stu-id="94556-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="94556-160">W polu Tabela wpisz „LedgerJournalTrans”.</span><span class="sxs-lookup"><span data-stu-id="94556-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="94556-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="94556-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="94556-162">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="94556-162">Click OK.</span></span>
8. <span data-ttu-id="94556-163">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="94556-163">Click Save.</span></span>
9. <span data-ttu-id="94556-164">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="94556-164">Close the page.</span></span>
10. <span data-ttu-id="94556-165">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="94556-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="94556-166">Rozpoczynanie wprowadzania następnej nowej konfiguracji formatu ER</span><span class="sxs-lookup"><span data-stu-id="94556-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="94556-167">W drzewie zaznacz element „Model płatności (fikcyjny)”.</span><span class="sxs-lookup"><span data-stu-id="94556-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="94556-168">Kliknij przycisk Utwórz konfigurację, aby otworzyć rozwijane okno dialogowe.</span><span class="sxs-lookup"><span data-stu-id="94556-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="94556-169">W polu Nowy wpisz „Format oparty na modelu danych Model płatności (fikcyjny)”.</span><span class="sxs-lookup"><span data-stu-id="94556-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="94556-170">W polu Definicja modelu danych wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="94556-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="94556-171">Należy zauważyć, że teraz tylko jedna pozycja główna jest dostępna do mapowania źródeł danych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="94556-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="94556-172">Podczas wprowadzania jednego lub więcej mapowań modeli tylko pozycje głównego modelu, które są mapowane na źródła danych aplikacji, mogą być wybierane jako definicja modelu podczas dodawania formatu raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="94556-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="94556-173">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="94556-173">Close the page.</span></span>
