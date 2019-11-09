---
title: Generowanie raportów w formatach pakietu Office z osadzonymi obrazami
description: W poniższych krokach wyjaśniono, jak użytkownik odtwarzający rolę „Administrator systemu” lub „Deweloper raportowania elektronicznego” może projektować konfiguracje raportowania elektronicznego (ER) w celu generowania dokumentów elektronicznych w formatach dokumentów pakietu MS Office (Excel i Word) zawierających osadzone obrazy.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 64fade6578e9cd4f8a51c524e4f6ebbf63b93f20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184768"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="41579-103">Generowanie raportów w formatach pakietu Office z osadzonymi obrazami</span><span class="sxs-lookup"><span data-stu-id="41579-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41579-104">W poniższych krokach wyjaśniono, jak użytkownik odtwarzający rolę „Administrator systemu” lub „Deweloper raportowania elektronicznego” może projektować konfiguracje raportowania elektronicznego (ER) w celu generowania dokumentów elektronicznych w formatach dokumentów pakietu MS Office (Excel i Word) zawierających osadzone obrazy.</span><span class="sxs-lookup"><span data-stu-id="41579-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="41579-105">W tym przykładzie użyjesz utworzonych konfiguracji ER dla przykładowej firmy „Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="41579-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="41579-106">Aby wykonać te kroki, należy najpierw wykonać kroki z przewodnika po zadaniu „ER Tworzenie raportów w formatach programu MS Office z osadzonymi obrazami (Część 2: Przegląd konfiguracji)”.</span><span class="sxs-lookup"><span data-stu-id="41579-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="41579-107">Kroki można wykonać na danych firmy „USMF”.</span><span class="sxs-lookup"><span data-stu-id="41579-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="41579-108">Uruchamianie formatu z początkowym mapowaniem modelu</span><span class="sxs-lookup"><span data-stu-id="41579-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="41579-109">Kliknij kolejno opcje Zarządzanie gotówką i bankami > Konta bankowe > Konta bankowe.</span><span class="sxs-lookup"><span data-stu-id="41579-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="41579-110">Użyj szybkiego filtru, aby wyfiltrować pole Konto bankowe według wartości „USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="41579-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="41579-111">W okienku akcji kliknij pozycję Konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="41579-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="41579-112">Kliknij przycisk Sprawdź.</span><span class="sxs-lookup"><span data-stu-id="41579-112">Click Check.</span></span>
5. <span data-ttu-id="41579-113">Kliknij opcję Drukowanie testu.</span><span class="sxs-lookup"><span data-stu-id="41579-113">Click Print test.</span></span>
    * <span data-ttu-id="41579-114">Uruchom format do celów testowych.</span><span class="sxs-lookup"><span data-stu-id="41579-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="41579-115">W polu Format czeku zbywalnego wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="41579-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="41579-116">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="41579-116">Click OK.</span></span>
    * <span data-ttu-id="41579-117">Przejrzyj produkt wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="41579-117">Review the created output.</span></span> <span data-ttu-id="41579-118">Należy zauważyć, że w raporcie jest przedstawiane logo firmy oraz podpis osoby upoważnionej.</span><span class="sxs-lookup"><span data-stu-id="41579-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="41579-119">Obraz podpisu jest pobierany z pola danych typu „Kontener” w rekordzie układu czeku skojarzonym z wybranym kontem bankowym.</span><span class="sxs-lookup"><span data-stu-id="41579-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="41579-120">Rozwiń sekcję Kopie.</span><span class="sxs-lookup"><span data-stu-id="41579-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="41579-121">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="41579-121">Click Edit.</span></span>
10. <span data-ttu-id="41579-122">W polu Znak wodny wprowadź tekst „Drukuj znak wodny jako unieważniony”.</span><span class="sxs-lookup"><span data-stu-id="41579-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="41579-123">Zmień ustawienie znaku wodnego, aby był pokazywany tekst znaku wodnego podczas generowania dokumentu w elemencie kształtu programu Excel.</span><span class="sxs-lookup"><span data-stu-id="41579-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="41579-124">Kliknij opcję Drukowanie testu.</span><span class="sxs-lookup"><span data-stu-id="41579-124">Click Print test.</span></span>
12. <span data-ttu-id="41579-125">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="41579-125">Click OK.</span></span>
    * <span data-ttu-id="41579-126">Przejrzyj produkt wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="41579-126">Review the created output.</span></span> <span data-ttu-id="41579-127">Należy zauważyć, że znak wodny jest widoczny w utworzonym raporcie zgodnie z wybraną opcją.</span><span class="sxs-lookup"><span data-stu-id="41579-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="41579-128">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-128">Close the page.</span></span>
14. <span data-ttu-id="41579-129">W okienku akcji kliknij pozycję Zarządzanie płatnościami.</span><span class="sxs-lookup"><span data-stu-id="41579-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="41579-130">Kliknij przycisk Czeki.</span><span class="sxs-lookup"><span data-stu-id="41579-130">Click Checks.</span></span>
16. <span data-ttu-id="41579-131">Kliknij przycisk Pokaż filtry.</span><span class="sxs-lookup"><span data-stu-id="41579-131">Click Show filters.</span></span>
17. <span data-ttu-id="41579-132">Zastosuj następujące filtry: wprowadź wartość filtru „381”,„385”,„389” w polu „Numer czeku”, stosując operator filtru „jest jednym z”.</span><span class="sxs-lookup"><span data-stu-id="41579-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="41579-133">Na liście zaznacz wszystkie wiersze.</span><span class="sxs-lookup"><span data-stu-id="41579-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="41579-134">Kliknij opcję Drukuj kopię czeku.</span><span class="sxs-lookup"><span data-stu-id="41579-134">Click Print check copy.</span></span>
    * <span data-ttu-id="41579-135">Uruchom format, aby ponownie wydrukować wybrane czeki.</span><span class="sxs-lookup"><span data-stu-id="41579-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="41579-136">Przejrzyj produkt wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="41579-136">Review the created output.</span></span> <span data-ttu-id="41579-137">Należy zauważyć, że wybrane czeki zostały ponownie wydrukowane.</span><span class="sxs-lookup"><span data-stu-id="41579-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="41579-138">Logo firmy i etykiety nie są drukowane, ponieważ znajdują się na formularzu z nadrukiem.</span><span class="sxs-lookup"><span data-stu-id="41579-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="41579-139">Modyfikowanie mapowania zaimportowanego modelu danych</span><span class="sxs-lookup"><span data-stu-id="41579-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="41579-140">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-140">Close the page.</span></span>
2. <span data-ttu-id="41579-141">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-141">Close the page.</span></span>
3. <span data-ttu-id="41579-142">Wybierz kolejno opcje Administrowanie organizacją > Raportowanie elektroniczne > Konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="41579-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="41579-143">W drzewie zaznacz element „Model czeków”.</span><span class="sxs-lookup"><span data-stu-id="41579-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="41579-144">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="41579-144">Click Designer.</span></span>
6. <span data-ttu-id="41579-145">Kliknij opcję Mapuj model na źródło danych.</span><span class="sxs-lookup"><span data-stu-id="41579-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="41579-146">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="41579-146">Click Designer.</span></span>
    * <span data-ttu-id="41579-147">Zmienimy powiązanie elementu podpisu modelu danych, tak aby obraz podpisu był pobierany z pliku dołączonego do rekordu układu czeku skojarzonego z wybranym kontem bankowym.</span><span class="sxs-lookup"><span data-stu-id="41579-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="41579-148">Wyłącz opcję Pokaż szczegóły.</span><span class="sxs-lookup"><span data-stu-id="41579-148">Turn Show details off.</span></span>
9. <span data-ttu-id="41579-149">W drzewie rozwiń węzeł „układ”.</span><span class="sxs-lookup"><span data-stu-id="41579-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="41579-150">W drzewie rozwiń węzeł „układ\podpis”.</span><span class="sxs-lookup"><span data-stu-id="41579-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="41579-151">W drzewie zaznacz element „układ\podpis\obraz = chequesaccount.'<Relacje'.BankChequeLayout.Signature1Bmp”.</span><span class="sxs-lookup"><span data-stu-id="41579-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="41579-152">W drzewie rozwiń węzeł „chequesaccount”.</span><span class="sxs-lookup"><span data-stu-id="41579-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="41579-153">W drzewie rozwiń węzeł „chequesaccount\<Relacje”.</span><span class="sxs-lookup"><span data-stu-id="41579-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="41579-154">W drzewie rozwiń węzeł „chequesaccount\<Relacje\BankChequeLayout”.</span><span class="sxs-lookup"><span data-stu-id="41579-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="41579-155">W drzewie rozwiń węzeł „chequesaccount\<Relacje\BankChequeLayout\<Relacje”.</span><span class="sxs-lookup"><span data-stu-id="41579-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="41579-156">W drzewie rozwiń węzeł „chequesaccount\<Relacje\BankChequeLayout\<Relacje\<Dokumenty”.</span><span class="sxs-lookup"><span data-stu-id="41579-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="41579-157">W drzewie zaznacz element „chequesaccount\<Relacje\BankChequeLayout\<Relacje\<Dokumenty\getFileContentAsContainer()”.</span><span class="sxs-lookup"><span data-stu-id="41579-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="41579-158">Kliknij opcję Powiąż.</span><span class="sxs-lookup"><span data-stu-id="41579-158">Click Bind.</span></span>
19. <span data-ttu-id="41579-159">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="41579-159">Click Save.</span></span>
20. <span data-ttu-id="41579-160">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-160">Close the page.</span></span>
21. <span data-ttu-id="41579-161">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-161">Close the page.</span></span>
22. <span data-ttu-id="41579-162">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-162">Close the page.</span></span>
23. <span data-ttu-id="41579-163">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="41579-164">Uruchamianie formatu przy użyciu skorygowanego mapowania modelu</span><span class="sxs-lookup"><span data-stu-id="41579-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="41579-165">Kliknij kolejno opcje Zarządzanie gotówką i bankami > Konta bankowe > Konta bankowe.</span><span class="sxs-lookup"><span data-stu-id="41579-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="41579-166">Skorzystaj z opcji szybkiego filtrowania, aby znaleźć rekordy.</span><span class="sxs-lookup"><span data-stu-id="41579-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="41579-167">Na przykład wyfiltruj według pola Konto bankowe z wartością „USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="41579-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="41579-168">W okienku akcji kliknij pozycję Konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="41579-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="41579-169">Kliknij przycisk Sprawdź.</span><span class="sxs-lookup"><span data-stu-id="41579-169">Click Check.</span></span>
5. <span data-ttu-id="41579-170">Kliknij opcję Drukowanie testu.</span><span class="sxs-lookup"><span data-stu-id="41579-170">Click Print test.</span></span>
6. <span data-ttu-id="41579-171">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="41579-171">Click OK.</span></span>
    * <span data-ttu-id="41579-172">Przejrzyj produkt wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="41579-172">Review the created output.</span></span> <span data-ttu-id="41579-173">Należy zauważyć, że obraz z załącznika funkcji zarządzania dokumentami jest wyświetlany jako podpis osoby upoważnionej.</span><span class="sxs-lookup"><span data-stu-id="41579-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="41579-174">Używanie dokumentu programu MS Word jako szablonu w zaimportowanym formacie</span><span class="sxs-lookup"><span data-stu-id="41579-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="41579-175">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-175">Close the page.</span></span>
2. <span data-ttu-id="41579-176">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-176">Close the page.</span></span>
3. <span data-ttu-id="41579-177">Wybierz kolejno opcje Administrowanie organizacją > Raportowanie elektroniczne > Konfiguracje.</span><span class="sxs-lookup"><span data-stu-id="41579-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="41579-178">W drzewie rozwiń węzeł „Model czeków”.</span><span class="sxs-lookup"><span data-stu-id="41579-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="41579-179">W drzewie zaznacz element „Model czeków\Format drukowania czeków”.</span><span class="sxs-lookup"><span data-stu-id="41579-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="41579-180">Kliknij przycisk Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="41579-180">Click Designer.</span></span>
7. <span data-ttu-id="41579-181">Kliknij opcję Załączniki.</span><span class="sxs-lookup"><span data-stu-id="41579-181">Click Attachments.</span></span>
8. <span data-ttu-id="41579-182">Kliknij przycisk Usuń.</span><span class="sxs-lookup"><span data-stu-id="41579-182">Click Delete.</span></span>
9. <span data-ttu-id="41579-183">Kliknij przycisk Tak.</span><span class="sxs-lookup"><span data-stu-id="41579-183">Click Yes.</span></span>
10. <span data-ttu-id="41579-184">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="41579-184">Click New.</span></span>
11. <span data-ttu-id="41579-185">Kliknij opcję Plik.</span><span class="sxs-lookup"><span data-stu-id="41579-185">Click File.</span></span>
    * <span data-ttu-id="41579-186">Kliknij przycisk Przeglądaj i zaznacz pobrany wcześniej plik „Cheque template Word.docx”.</span><span class="sxs-lookup"><span data-stu-id="41579-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="41579-187">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-187">Close the page.</span></span>
13. <span data-ttu-id="41579-188">W polu Szablon wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="41579-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="41579-189">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="41579-189">Click Save.</span></span>
15. <span data-ttu-id="41579-190">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-190">Close the page.</span></span>
16. <span data-ttu-id="41579-191">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="41579-191">Click Edit.</span></span>
17. <span data-ttu-id="41579-192">W polu Uruchom wersję roboczą wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="41579-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="41579-193">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="41579-193">Close the page.</span></span>
19. <span data-ttu-id="41579-194">Kliknij kolejno opcje Zarządzanie gotówką i bankami > Konta bankowe > Konta bankowe.</span><span class="sxs-lookup"><span data-stu-id="41579-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="41579-195">Użyj szybkiego filtru, aby wyfiltrować pole Konto bankowe według wartości „USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="41579-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="41579-196">Kliknij przycisk Sprawdź.</span><span class="sxs-lookup"><span data-stu-id="41579-196">Click Check.</span></span>
22. <span data-ttu-id="41579-197">Kliknij opcję Drukowanie testu.</span><span class="sxs-lookup"><span data-stu-id="41579-197">Click Print test.</span></span>
23. <span data-ttu-id="41579-198">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="41579-198">Click OK.</span></span>
    * <span data-ttu-id="41579-199">Przejrzyj produkt wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="41579-199">Review the created output.</span></span> <span data-ttu-id="41579-200">Należy zwrócić uwagę, że dane wyjściowe zostały wygenerowane jako dokument programu MS Word z osadzonymi obrazami prezentującymi logo firmy, podpis osoby upoważnionej i wybrany tekst znaku wodnego.</span><span class="sxs-lookup"><span data-stu-id="41579-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  
