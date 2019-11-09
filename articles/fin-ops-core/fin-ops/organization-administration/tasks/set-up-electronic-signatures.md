---
title: Konfigurowanie podpisów elektronicznych
description: Użyj tej procedury do skonfigurowania podpisów elektronicznych.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad4ef067841511e235dcf538c720b72283d31c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179489"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="8dd60-103">Konfigurowanie podpisów elektronicznych</span><span class="sxs-lookup"><span data-stu-id="8dd60-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8dd60-104">Użyj tej procedury do skonfigurowania podpisów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="8dd60-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="8dd60-105">Podpis elektroniczny potwierdza tożsamość osoby, która ma rozpocząć lub zatwierdzić jakiś proces obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="8dd60-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="8dd60-106">Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej DAT.</span><span class="sxs-lookup"><span data-stu-id="8dd60-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="8dd60-107">Włączanie funkcji Klucz konfiguracji Podpis elektroniczny</span><span class="sxs-lookup"><span data-stu-id="8dd60-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="8dd60-108">Wybierz kolejno opcje Administrowanie systemem > Ustawienia > Konfiguracja licencji.</span><span class="sxs-lookup"><span data-stu-id="8dd60-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="8dd60-109">W drzewie rozwiń węzeł „Administracja”.</span><span class="sxs-lookup"><span data-stu-id="8dd60-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="8dd60-110">Upewnij się, że jest zaznaczone pole wyboru Podpis elektroniczny.</span><span class="sxs-lookup"><span data-stu-id="8dd60-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="8dd60-111">Jeśli nie jest zaznaczone pole wyboru Podpis elektroniczny, należy włączyć tryb konserwacji.</span><span class="sxs-lookup"><span data-stu-id="8dd60-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="8dd60-112">Tryb konserwacji można włączyć w tym środowisku, uruchamiając zadanie konserwacji z poziomu usługi Lifecycle Services albo używając lokalnie narzędzia Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="8dd60-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="8dd60-113">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="8dd60-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="8dd60-114">Konfigurowanie parametrów podpisu elektronicznego</span><span class="sxs-lookup"><span data-stu-id="8dd60-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="8dd60-115">Wybierz kolejno opcje Administrowanie organizacją > Ustawienia > Podpis elektroniczny > Parametry podpisu elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="8dd60-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="8dd60-116">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="8dd60-116">Click Edit.</span></span>
3. <span data-ttu-id="8dd60-117">W polu Powiadomienie wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="8dd60-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="8dd60-118">Wprowadź powiadomienie, które osoby podpisujące będą otrzymywać w przypadku żądania podpisu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="8dd60-119">Możesz wprowadzić dowolny tekst.</span><span class="sxs-lookup"><span data-stu-id="8dd60-119">You can enter any text.</span></span> <span data-ttu-id="8dd60-120">Zazwyczaj taki tekst wyjaśnia użytkownikowi, co to znaczy podpisać dokument elektronicznie.</span><span class="sxs-lookup"><span data-stu-id="8dd60-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="8dd60-121">Jeśli chcesz wprowadzić tekst powiadomienia w dodatkowych językach, kliknij przycisk Tłumaczenia.</span><span class="sxs-lookup"><span data-stu-id="8dd60-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="8dd60-122">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="8dd60-122">Click Save.</span></span>
5. <span data-ttu-id="8dd60-123">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="8dd60-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="8dd60-124">Konfigurowanie kodów przyczyn dla podpisów elektronicznych</span><span class="sxs-lookup"><span data-stu-id="8dd60-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="8dd60-125">Wybierz kolejno opcje Administrowanie organizacją > Ustawienia > Podpis elektroniczny > Kody przyczyn podpisu elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="8dd60-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="8dd60-126">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="8dd60-126">Click New.</span></span>
    * <span data-ttu-id="8dd60-127">Kody przyczyn trzeba skonfigurować przez rozpoczęciem korzystania z podpisów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="8dd60-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="8dd60-128">Prawidłowy kod przyczyny jest wymagany podczas podpisywania dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="8dd60-129">Osoba podpisująca wybiera kod przyczyny, aby wskazać cel podpisu elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="8dd60-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="8dd60-130">Kodu przyczyny można na przykład użyć w celu wskazania zgody prawnej.</span><span class="sxs-lookup"><span data-stu-id="8dd60-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="8dd60-131">W polu Kod przyczyny wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="8dd60-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="8dd60-132">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="8dd60-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="8dd60-133">W razie potrzeby wprowadź dodatkowe kody przyczyn.</span><span class="sxs-lookup"><span data-stu-id="8dd60-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="8dd60-134">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="8dd60-134">Click Save.</span></span>
6. <span data-ttu-id="8dd60-135">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="8dd60-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="8dd60-136">Wymaganie używania podpisów elektronicznych do istniejących procesów</span><span class="sxs-lookup"><span data-stu-id="8dd60-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="8dd60-137">Wybierz kolejno opcje Administrowanie organizacją > Ustawienia > Podpis elektroniczny > Wymagania dotyczące podpisu elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="8dd60-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="8dd60-138">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="8dd60-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8dd60-139">Wybierz proces wymagający podpisów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="8dd60-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="8dd60-140">Zaznacz lub wyczyść pole wyboru Wymagany jest podpis.</span><span class="sxs-lookup"><span data-stu-id="8dd60-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="8dd60-141">Powtórz te kroki dla każdego procesu, który wymaga podpisów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="8dd60-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="8dd60-142">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="8dd60-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="8dd60-143">Tworzenie niestandardowego wymagania dotyczącego podpisów elektronicznych</span><span class="sxs-lookup"><span data-stu-id="8dd60-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="8dd60-144">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="8dd60-144">Click New.</span></span>
2. <span data-ttu-id="8dd60-145">Zaznacz lub wyczyść pole wyboru Wymagany jest podpis.</span><span class="sxs-lookup"><span data-stu-id="8dd60-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="8dd60-146">W polu Nazwa wpisz nazwę procesu wymagającego podpisów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="8dd60-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="8dd60-147">W polu Nazwa tabeli kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="8dd60-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8dd60-148">Na liście znajdź i zaznacz tabelę, w której są przechowywane dane wymagające podpisu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="8dd60-149">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8dd60-150">W polu Nazwa pola kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="8dd60-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8dd60-151">Na liście znajdź i zaznacz pole w tabeli, które ma być monitorowane.</span><span class="sxs-lookup"><span data-stu-id="8dd60-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="8dd60-152">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8dd60-153">Określ, kiedy ma być wymagany podpis.</span><span class="sxs-lookup"><span data-stu-id="8dd60-153">Specify when a signature is required.</span></span>     <span data-ttu-id="8dd60-154">Wybierz opcję Zawsze, jeśli podpis ma być wymagany przy każdej zmianie danych pola.</span><span class="sxs-lookup"><span data-stu-id="8dd60-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="8dd60-155">Wybierz opcję Tylko, aby określić, że podpis ma być wymagany tylko pod pewnymi warunkami.</span><span class="sxs-lookup"><span data-stu-id="8dd60-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="8dd60-156">Jeśli wybierzesz opcję Tylko, należy również wybrać jedną z następujących opcji: Przy wstawianiu rekordu, Przy aktualizacji rekordu lub Przy usuwaniu rekordu.</span><span class="sxs-lookup"><span data-stu-id="8dd60-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="8dd60-157">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="8dd60-157">Click Save.</span></span>
11. <span data-ttu-id="8dd60-158">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="8dd60-158">Close the page.</span></span>
