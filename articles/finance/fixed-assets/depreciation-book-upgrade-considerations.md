---
title: Omówienie uaktualniania księgi amortyzacji
description: 'W poprzednich wersjach istniały dwie koncepcje wyceny środków trwałych: modele ewidencji i księgi amortyzacji.'
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efa1b492fec085cc8bac5a786af4aaba854899e5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249662"
---
# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="875d9-103">Omówienie uaktualnienia księgi amortyzacji</span><span class="sxs-lookup"><span data-stu-id="875d9-103">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="875d9-104">W poprzednich wersjach istniały dwie koncepcje wyceny środków trwałych: modele ewidencji i księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="875d9-104">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="875d9-105">W programie Microsoft Dynamics 365 for Operations (wydanie 1611) funkcje modeli ewidencji i ksiąg amortyzacji zostały scalone w pojedynczy obiekt zwany księgą.</span><span class="sxs-lookup"><span data-stu-id="875d9-105">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="875d9-106">Ten temat porusza kilka zagadnień, które należy wziąć pod uwagę przy uaktualnianiu.</span><span class="sxs-lookup"><span data-stu-id="875d9-106">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="875d9-107">Proces uaktualniania spowoduje przeniesienie istniejących ustawień i wszystkich istniejących transakcji do nowej struktury księgi.</span><span class="sxs-lookup"><span data-stu-id="875d9-107">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="875d9-108">Modele ewidencji pozostaną w swoim obecnym kształcie, jako księgi powodujące księgowanie w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="875d9-108">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="875d9-109">Księgi amortyzacji zostaną przeniesione do księgi, która w opcji **Księguj w księdze głównej** ma wartość **Nie**.</span><span class="sxs-lookup"><span data-stu-id="875d9-109">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="875d9-110">Arkusze ksiąg amortyzacji zostaną przeniesiona do arkusza księgi głównej, w której ustawiono warstwę księgowania **Brak**.</span><span class="sxs-lookup"><span data-stu-id="875d9-110">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="875d9-111">Transakcje księgi amortyzacji zostaną przeniesione do transakcji na środkach trwałych.</span><span class="sxs-lookup"><span data-stu-id="875d9-111">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="875d9-112">Przed uruchomieniem uaktualniania danych zapoznaj się z dwoma opcjami służącymi do uaktualniania wierszy arkuszy księgi amortyzacji do załączników transakcji oraz do uaktualniania numeracji, która będzie używana dla serii załączników.</span><span class="sxs-lookup"><span data-stu-id="875d9-112">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="875d9-113">Opcja 1: **Numeracja systemowa** — Jest to opcja domyślna, która optymalizuje przebieg uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="875d9-113">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="875d9-114">Uaktualnianie nie będzie używać struktury numeracji, ale zamiast tego przydzieli załącznikom numery w oparciu o zestawy.</span><span class="sxs-lookup"><span data-stu-id="875d9-114">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="875d9-115">Po uaktualnieniu nowa numeracja zostanie utworzona z ustawieniem **Następny zestaw numerów** odpowiednio opartym na uaktualnionych transakcjach.</span><span class="sxs-lookup"><span data-stu-id="875d9-115">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="875d9-116">Domyślnie używana numeracja będzie w formacie FADBUpgr\#\#\#\#\#\#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="875d9-116">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="875d9-117">Podczas korzystania z tej metody jest dostępnych kilka parametrów umożliwiających korygowanie tego formatu:</span><span class="sxs-lookup"><span data-stu-id="875d9-117">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="875d9-118">**Kod sekwencji numerów** — Kod identyfikujący numerację.</span><span class="sxs-lookup"><span data-stu-id="875d9-118">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="875d9-119">Ten kod nie może istnieć, ponieważ zostanie utworzony przez uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="875d9-119">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="875d9-120">Nazwa stałej: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="875d9-120">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="875d9-121">Wartość domyślna: „FADBUpgr”</span><span class="sxs-lookup"><span data-stu-id="875d9-121">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="875d9-122">**Prefiks** — Wartość w postaci stałego ciągu tekstowego, który będzie używany jako prefiks numerów załącznika.</span><span class="sxs-lookup"><span data-stu-id="875d9-122">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="875d9-123">Nazwa stałej: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="875d9-123">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="875d9-124">Wartość domyślna: „FADBUpgr”</span><span class="sxs-lookup"><span data-stu-id="875d9-124">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="875d9-125">**Długość alfanumeryczna** — Długość segmentu alfanumerycznego w numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-125">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="875d9-126">Nazwa stałej: **NumberSequenceDefaultParameterAlpanumericLength**</span><span class="sxs-lookup"><span data-stu-id="875d9-126">Constant name: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span></span>
    -   <span data-ttu-id="875d9-127">Wartość domyślna: 9</span><span class="sxs-lookup"><span data-stu-id="875d9-127">Default value: 9</span></span>
-   <span data-ttu-id="875d9-128">**Numer początkowy** — Pierwszy numer, który ma zostać użyty w numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-128">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="875d9-129">Nazwa stałej: **NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="875d9-129">Constant name: \*\*NumberSequenceDefaultParameterStartNumber  \*\*</span></span>
    -   <span data-ttu-id="875d9-130">Wartość domyślna: 1</span><span class="sxs-lookup"><span data-stu-id="875d9-130">Default value: 1</span></span>

<span data-ttu-id="875d9-131">Opcja 2: **Istniejąca numeracja zdefiniowana przez użytkownika** — Ta opcja umożliwia zdefiniowanie numeracji, która ma być stosowana do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="875d9-131">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="875d9-132">Należy wziąć pod uwagę użycie tej opcji, jeśli potrzebujesz zaawansowanej konfiguracji numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-132">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="875d9-133">Aby użyć numeracji, należy zmodyfikować klasę uaktualniania ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans o następujące informacje:</span><span class="sxs-lookup"><span data-stu-id="875d9-133">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="875d9-134">**Kod sekwencji numerów** — Kod numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-134">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="875d9-135">Nazwa stałej: **NumberSequenceExistingCode**</span><span class="sxs-lookup"><span data-stu-id="875d9-135">Constant name: \*\*NumberSequenceExistingCode \*\*</span></span>
    -   <span data-ttu-id="875d9-136">Wartość domyślna: Brak wartości domyślnej, należy tu wpisać obowiązujący kod numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-136">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="875d9-137">**Udostępnione sekwencje numerów** — Wartość logiczna identyfikująca zakres numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-137">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="875d9-138">Użyj wartości „true” dla numeracji współużytkowanej przez wszystkie firmy, a wartości „false” dla zakresu specyficznego dla firmy.</span><span class="sxs-lookup"><span data-stu-id="875d9-138">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="875d9-139">W przypadku ustawienia wartości „false” numeracja o podanej nazwie musi istnieć w każdej firmie zawierającej transakcje księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="875d9-139">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="875d9-140">Współużytkowane numeracje istnieją w każdej partycji, która zawiera transakcje księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="875d9-140">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="875d9-141">Nazwa stałej: **NumberSequenceExistingIsShared**</span><span class="sxs-lookup"><span data-stu-id="875d9-141">Constant name: \*\*NumberSequenceExistingIsShared \*\*</span></span>
    -   <span data-ttu-id="875d9-142">Wartość domyślna: true</span><span class="sxs-lookup"><span data-stu-id="875d9-142">Default value: true</span></span>

<span data-ttu-id="875d9-143">Parametry znajdują się na początku klasy ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="875d9-143">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="875d9-144">*// Określ preferowaną metodę alokacji załączników* 
 *// true, jeśli chcesz używać istniejącego kodu numeracji* 
 *// false, jeśli zamierzasz używać zdefiniowanych przez system sekwencji numerów (ustawienie domyślne)* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="875d9-144">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="875d9-145">*// Jeśli używasz numeracji systemowej, określ parametry numeracji.*
 *// Nowa numeracja zostanie utworzona z następującymi parametrami.*</span><span class="sxs-lookup"><span data-stu-id="875d9-145">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="875d9-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="875d9-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="875d9-147">*// Jeśli używasz metody z istniejącą numeracją, podaj kod istniejącej numeracji.* 
 *// Alokacja załączników zostanie dokonana kolejno wierszami przy użyciu istniejącej numeracji.*</span><span class="sxs-lookup"><span data-stu-id="875d9-147">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="875d9-148">const str NumberSequenceExistingCode = ''; *// Określ zakres kodu istniejącej numeracji* 
 *// true, jeśli podana numeracja jest współdzielona* 
 *// false, jeśli podana numeracja dotyczy konkretnej firmy* 
 *// Jeśli nie zostanie znaleziony kod numeracji o podanym zakresie, będzie używana domyślna numeracja systemowa.*</span><span class="sxs-lookup"><span data-stu-id="875d9-148">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="875d9-149">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="875d9-149">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="875d9-150">Po zmodyfikowaniu stałych odbuduj projekt zawierający klasę.</span><span class="sxs-lookup"><span data-stu-id="875d9-150">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="875d9-151">W przypadku używania metody z numeracją systemową (opcja 1) uaktualnienie będzie używać przetwarzania opartego na zestawach w celu przydzielenia numerów załączników w sposób określony w parametrach skryptu uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="875d9-151">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="875d9-152">Spowoduje to także, że po alokacji zostanie utworzona nowa numeracja z podanymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="875d9-152">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="875d9-153">W przypadku używania metody z istniejącą numeracją zdefiniowaną przez użytkownika (opcja 2) aparat uaktualnienia danych sprawdza, czy numeracja z podanym zakresem istnieje w bazie danych dla każdej partycji i firmy z transakcjami księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="875d9-153">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="875d9-154">Jeżeli tak, w uaktualnieniu będzie wykonywane przetwarzanie wiersz po wierszu w celu alokacji numerów załączników zgodnie z parametrami numeracji przy użyciu struktury numeracji.</span><span class="sxs-lookup"><span data-stu-id="875d9-154">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="875d9-155">Jeżeli numeracja z podanym zakresem nie istnieje, w uaktualnieniu do przydzielenia numerów załączników zostanie użyta numeracja systemowa, a po zakończeniu alokacji zostanie utworzona nowa numeracja z podanymi parametrami domyślnymi.</span><span class="sxs-lookup"><span data-stu-id="875d9-155">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="875d9-156">W obu metodach skrypt uaktualniania danych będzie również używał numeracji dla pola **Seria załączników** w nowych arkuszach księgi głównej utworzonych dla poprzednich arkuszy księgi amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="875d9-156">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>


