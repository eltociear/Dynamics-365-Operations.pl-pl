---
title: "Konfigurowanie zarządzania ofertami"
description: "W tym temacie opisano sposób konfigurowania zarządzania ofertami w aplikacji Talent."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: pl-pl
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="7fd8c-103">Konfigurowanie zarządzania ofertami</span><span class="sxs-lookup"><span data-stu-id="7fd8c-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fd8c-104">Gdy kandydat jest przenoszony do etapu oferty w aplikacji Dynamics 365 for Talent Attract, trzeba mieć możliwość szybkiego tworzenia ofert dla kandydata, ich niezbędnego zatwierdzania i wysyłania do kandydata.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="7fd8c-105">Ponieważ większość ofert jest standardowych, można je tworzyć na podstawie szablonów wielokrotnego użytku.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="7fd8c-106">W aplikacji Attract wszystkie oferty są łączone w pakiet oferty, który jest kolekcją jednego lub większej dokumentów oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="7fd8c-107">Ten temat zawiera listę wszystkich czynności, jakie powinien wykonać administrator aplikacji Attract w celu skonfigurowania różnych szablonów pakietów ofert w ramach funkcji zarządzania ofertami w aplikacji Attract.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="7fd8c-108">Użytkownicy nieposiadający ról administratorów nie mają dostępu do tych funkcji.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="7fd8c-109">Funkcje zarządzania ofertami są dostępne w ramach dodatku kompleksowej obsługi rekrutacji.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="7fd8c-110">Dane oferty</span><span class="sxs-lookup"><span data-stu-id="7fd8c-110">Offer data</span></span> 

<span data-ttu-id="7fd8c-111">Dane oferty to najmniejsza jednostka wewnątrz szablonu pakietu oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="7fd8c-112">Typowa oferta składa się z tekstu standardowego i zestawu wartości.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="7fd8c-113">Zestawy wartości to jedyne elementy, które mogą się zmieniać między ofertami.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="7fd8c-114">Podczas tworzenia oferty najważniejszym aspektem, na którym może się skoncentrować twórca oferty, jest lista symboli zastępczych danych oferty znajdujących się w szablonie pakietu oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="7fd8c-115">Aby skonfigurować dane oferty, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="7fd8c-116">Przejdź do okna **Zarządzanie ofertami**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7fd8c-117">Rozwiń sekcję **Biblioteka** w lewym okienku nawigacji, a następnie przejdź do strony **Dane oferty**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="7fd8c-118">Na stronie **Dane oferty** znajdują się sekcje **Szczegóły kandydata** i **Szczegóły funkcji**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="7fd8c-119">Aplikacja Attract oferuje kilka gotowych symboli zastępczych danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="7fd8c-120">Na stronie znajdują się sekcje porządkujące różne symbole zastępcze danych oferty w logiczne grupy.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="7fd8c-121">Te sekcje mogą pomóc zarządzać danymi oferty i wprowadzać dane podczas tworzenia oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="7fd8c-122">Aby utworzyć nową sekcję danych oferty, kliknij opcję **Dodaj sekcję** i nadaj sekcji unikatową nazwę.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="7fd8c-123">Aby dodać symbole zastępcze danych oferty do dowolnej sekcji, kliknij przycisk **Dodaj dane oferty** i nadaj unikatową nazwę symbolowi zastępczemu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="7fd8c-124">Aby zmienić nazwę dowolnej sekcji, umieść wskaźnik myszy nad nazwą sekcji i zaktualizuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="7fd8c-125">Aby edytować nazwę dowolnego istniejącego symbolu zastępczego danych oferty, najpierw upewnij się, że symbol zastępczy nie jest częścią żadnego szablonu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="7fd8c-126">Następnie umieść wskaźnik myszy nad nazwą symbolu zastępczego danych oferty i zaktualizuj nazwę stosownie do potrzeb.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="7fd8c-127">Aby usunąć nazwę istniejącego symbolu zastępczego danych oferty, najpierw upewnij się, że symbol zastępczy nie jest częścią żadnego innego szablonu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="7fd8c-128">Następnie umieść wskaźnik myszy nad symbolem zastępczym, a po wyświetleniu ikony kosza kliknij ją. Wtedy symbol zastępczy danych oferty zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="7fd8c-129">Wskaźnik liczbowy obok każdego elementu danych oferty pokazuje, w ilu szablonach jest używany symbol zastępczy danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="7fd8c-130">Aby usunąć którąkolwiek sekcji, umieść wskaźnik myszy nad jej nazwą.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="7fd8c-131">Jeśli żaden symbol zastępczy danych oferty wewnątrz sekcji nie występuje w żadnym szablonie, można kliknąć ikonę kosza, aby usunąć sekcję.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="7fd8c-132">Usunięcie sekcji spowoduje również usunięcie wszystkich symboli zastępczych danych oferty znajdujących się w tej sekcji.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="7fd8c-133">Po skonfigurowaniu symboli zastępczych danych oferty można ich używać we wszystkich szablonach dokumentów.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="7fd8c-134">Symbole zastępcze danych oferty nie są ograniczone do określonego szablonu — tego samego zestawu można używać we wszystkich szablonach.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="7fd8c-135">Reguły danych oferty</span><span class="sxs-lookup"><span data-stu-id="7fd8c-135">Offer data rules</span></span>

<span data-ttu-id="7fd8c-136">Większość organizacji ma reguły określające sposób tworzenia ofert.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="7fd8c-137">Na przykład organizacja może wymagać, aby oferta maksymalnego rocznego wynagrodzenia dla określonej kombinacji lokalizacji i poziomu stażu pracy mieściła się w pewnym zakresie albo żeby poziom oferty dla nowo zatrudnianej osoby mógł przybierać tylko klika ściśle określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="7fd8c-138">Obecnie aplikacja Attract obsługuje wszystkie reguły danych za pomocą pliku CSV.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="7fd8c-139">Aby przygotować plik CSV reguł danych, należy wykonać następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="7fd8c-140">Ustal symbol zastępczy danych oferty dla zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="7fd8c-141">Na przykład **Wynagrodzenie roczne**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="7fd8c-142">Zidentyfikuj zależne wartości symbolu zastępczego danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="7fd8c-143">Na przykład **Lokalizacja funkcji** i **Poziom**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="7fd8c-144">Nazwij kolumny 1 i 2 **Lokalizacja funkcji** i **Poziom**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="7fd8c-145">Aby przekazać zakres wartości, zatytułuj kolumny 3 i 4 **Wynagrodzenie roczne**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="7fd8c-146">Aby przekazywać tylko określoną wartość zamiast zakresu, nazwij tylko kolumnę 3 **Wynagrodzenie roczne**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="7fd8c-147">Wypełnij pliku programu Microsoft Excel zgodnie z wymaganymi rolami.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="7fd8c-148">Upewnij się, że każdy wiersz zawiera unikatową kombinację wszystkich wartości.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="7fd8c-149">Zapisz plik w formacie CSV.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="7fd8c-150">Aby przekazać plik reguł danych oferty, należy wykonać następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="7fd8c-151">Przejdź do okna **Zarządzanie ofertami**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7fd8c-152">Rozwiń sekcję **Biblioteka** w lewym panelu nawigacji, a następnie przejdź do strony **Reguły danych oferty**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="7fd8c-153">Kliknij przycisk **Nowy zestaw danych**, aby wyświetlić okno dialogowe **Przekaż**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="7fd8c-154">Nadaj unikatową nazwę zestawowi reguł, a następnie przekaż zapisany plik CSV.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="7fd8c-155">Kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-155">Click **Add**.</span></span>
    <span data-ttu-id="7fd8c-156">Zestaw reguł będzie przetwarzany w tle, a po zakończeniu przetwarzania otrzymasz powiadomienie w aplikacji i pocztą e-mail.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="7fd8c-157">Otrzymasz powiadomienie, jeśli wystąpią błędy w trakcie przetwarzania przekazanego pliku.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="7fd8c-158">Wtedy możesz pobrać dziennik błędów, naprawić plik i przekazać go ponownie.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="7fd8c-159">Użyj przycisku wielokropka (**...**), jeśli chcesz pobrać zestaw reguł i zaktualizować zestaw wartości.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="7fd8c-160">Po aktualizacji możesz ponownie przekazać plik.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="7fd8c-161">Można usunąć istniejący przekazany zestaw reguł, jeśli definiowany symbol zastępczy nie jest używany w innym szablonie dokumentu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!UWAGI]
> - <span data-ttu-id="7fd8c-163">Pod każdym symbolem zastępczym można umieścić tylko jeden unikatowy zestaw kolumn, od których zależy symbol.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="7fd8c-164">Na przykład jeśli symbol zastępczy **Wynagrodzenie roczne** zależy od kolumn **Lokalizacja funkcji** i **Poziom**, nie można przekazać innego zestawu reguł, w którym symbol zastępczy **Wynagrodzenie roczne** zależy od innego zestawu kolumn.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="7fd8c-165">Przykładowe zestawy reguł danych oferty można pobierać na karcie **Przykłady** na stronie **Reguły danych oferty**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="7fd8c-166">Gdy twórca oferty zastąpi wartości zalecane przez reguły danych oferty, oferta jest oznaczana jako niestandardowa i wtedy zostanie wymuszony przepływu pracy zatwierdzania oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="7fd8c-167">Szablony dokumentów</span><span class="sxs-lookup"><span data-stu-id="7fd8c-167">Document templates</span></span>

<span data-ttu-id="7fd8c-168">Szablon dokumentu oferty może pomóc administratorom tworzyć listy z ofertą.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="7fd8c-169">Szablon dokumentu oferty jest kombinacją tekstu, który będzie częścią oferty, i zdefiniowanych symboli zastępczych danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="7fd8c-170">Aby utworzyć szablon dokumentu oferty, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="7fd8c-171">Przejdź do okna **Zarządzanie ofertami**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7fd8c-172">Rozwiń sekcję **Biblioteka** w lewym okienku nawigacji, a następnie przejdź do strony **Szablony**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="7fd8c-173">Strona **Szablony** zawiera listę szablonów dokumentów, które zostały już zdefiniowane.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="7fd8c-174">Aby utworzyć nowy szablon dokumentu, kliknij przycisk **Nowy szablon**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="7fd8c-175">Nadaj szablonowi unikatową nazwę i kliknij przycisk **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="7fd8c-176">Za pomocą edytora tekstu sformatowanego wstaw lub zmodyfikuj zawartość dokumentu oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="7fd8c-177">Możesz wstawić tabele, obrazy i hiperłącza, korzystając z opcji dostępnych w górnej części edytora tekstu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="7fd8c-178">Symbole zastępcze danych oferty można wstawić w dokumencie szablonu oferty następującymi metodami:</span><span class="sxs-lookup"><span data-stu-id="7fd8c-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="7fd8c-179">Przeciągnięcie z prawego okienka i upuszczenie.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="7fd8c-180">Umieszczenie hasztagu symbolu zastępczego danych oferty bezpośrednio w odpowiednim miejscu.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="7fd8c-181">Wpisz znak **\#**, a następnie rozpocznij wpisywanie nazwy symbolu zastępczego danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="7fd8c-182">Pojawi się lista rozwijana z opcjami.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="7fd8c-183">Kliknij opcję lub naciśnij klawisz **Enter**, aby wstawić symbol zastępczy danych oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!UWAGI]
    > - <span data-ttu-id="7fd8c-185">Aby skojarzyć symbol zastępczy z szablonem dokumentu oferty bez pokazywania wartości symbolu kandydatowi, umieść wskaźnik myszy nad symbolem zastępczym danych oferty i kliknij ikonę **Przypnij**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="7fd8c-186">Spowoduje to przesunięcie symbolu zastępczego do sekcji **Przypięte dane oferty** w szablonie dokumentu oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="7fd8c-187">Aby odpiąć, wykonaj te same czynności, ale na liście symboli zastępczych danych oferty kliknij pozycję **Odepnij**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="7fd8c-188">Aby wyświetlić listę aktywnych symboli zastępczych danych oferty, przejdź do karty **Aktywne** w prawym okienku.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="7fd8c-189">Jeśli wstawisz symbol zastępczy sterowany przez zestaw reguł danych oferty, możesz obejrzeć zależność tego symbolu zastępczego danych oferty od innych wartości.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="7fd8c-190">Alternatywnie możesz **zaimportować** zawartość z pliku .docx na lokalnym komputerze i edytować ją zgodnie z wymaganiami.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="7fd8c-191">Dzięki temu nie trzeba wpisywać całej zawartości w edytorze.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="7fd8c-192">Aby wyświetlić podgląd dokumentu oferty, użyj opcji **Podgląd** w górnej części strony.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="7fd8c-193">Aby określić, czy twórca oferty może edytować zawartość dokumentu oferty, użyj opcji **Zarządzaj uprawnieniami** w górnej części strony.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="7fd8c-194">Jeśli chcesz, aby twórca oferty mógł tylko wstawiać wartości symboli zastępczych, a nie edytować tekst, ustaw wartość uprawnienia na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="7fd8c-195">Kliknij przycisk **Zapisz**, aby zapisać swoją pracę.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="7fd8c-196">Szablon zostanie zapisany w stanie Wersja robocza.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="7fd8c-197">Aby sfinalizować dokument i oznaczyć go jako opublikowany, kliknij przycisk **Zakończ**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="7fd8c-198">Możesz zobaczyć, które szablony dokumentów są obecnie aktywne, w trybie roboczym oraz zostały zarchiwizowane i nie są już używane na stronie docelowej biblioteki szablonów dokumentów.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="7fd8c-199">Można usunąć każdy szablon dokumentu oferty, który nie są częścią istniejącego szablonu pakietu oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="7fd8c-200">Szablony pakietów ofert</span><span class="sxs-lookup"><span data-stu-id="7fd8c-200">Offer package templates</span></span>

<span data-ttu-id="7fd8c-201">Pakiety ofert to drugie artefakty oferty, które są udostępniane kandydatowi. Składają się z jednego lub kombinacji wielu szablonów dokumentów oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="7fd8c-202">Aby utworzyć pakiet oferty, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="7fd8c-203">Przejdź do okna **Zarządzanie ofertami**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="7fd8c-204">Z lewego okienka nawigacji przejdź do strony **Pakiety**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="7fd8c-205">Zostanie wyświetlona lista aktywnych szablonów pakietów, które są dostępne do użytku przez twórców ofert.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="7fd8c-206">Aby utworzyć nowy pakiet oferty, kliknij przycisk **Nowy pakiet**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="7fd8c-207">Wprowadź unikatową nazwę i kliknij przycisk **Utwórz**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="7fd8c-208">Kliknij przycisk **Dodaj szablon**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-208">Click **Add template**.</span></span>

    >[!UWAGI]
    > - <span data-ttu-id="7fd8c-210">Możesz utworzyć nowy szablon albo wybrać jeden z istniejących.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="7fd8c-211">Jeśli postanowisz dodać istniejący szablon, upewnij się, że szablon dokumentu oferty został zapisany, sfinalizowany i oznaczony jako aktywny.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="7fd8c-212">Można wybrać dowolną potrzebną liczbę szablonów dokumentów.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="7fd8c-213">Kliknij przycisk **Gotowe**, aby wrócić do okna **Zarządzanie pakietami**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="7fd8c-214">Można skonfigurować kolejność dokumentów oraz wskazać, czy określone dokumenty oferty są wymagane podczas tworzenia oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="7fd8c-215">Twórca oferty będzie miał możliwość usunięcia dokumentów oznaczonych jako **Niewymagane**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="7fd8c-216">Aby zapisać szablon pakietu oferty, tak aby mogli go używać wszyscy twórcy ofert, kliknij **Zapisz i opublikuj**.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="7fd8c-217">Aby wyświetlić wersje robocze szablonów pakietów ofert, przejdź do karty **Wersje robocze**. Jeśli w szablonie pakietu oferty zostanie wprowadzona zmiana, należy zapisać szablon i ponownie go opublikować.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="7fd8c-218">Konfigurowanie procesu tworzenia oferty</span><span class="sxs-lookup"><span data-stu-id="7fd8c-218">Configure an offer process</span></span>

<span data-ttu-id="7fd8c-219">Istnieje kilka etapów procesu tworzenia oferty, które mogą być konfigurowane przez administratora aplikacji Attract.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="7fd8c-220">**Zatwierdzenia ofert** — Określ, czy zatwierdzenia ofert są wymagane, zanim ofertę można wysłać do kandydata.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="7fd8c-221">Jako administrator możesz również zdecydować, czy wszystkie zatwierdzenia ofert będą następowały kolejno, czy równolegle.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="7fd8c-222">Możesz także określić, czy osoby zatwierdzające oferty muszą dodawać komentarze do swoich zatwierdzeń ofert.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="7fd8c-223">Zatwierdzenia ofert są obowiązkowe dla wszystkich ofert niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="7fd8c-224">**Funkcje oferty dla kandydata** — Jako administrator możesz określić, czy wszystkie oferty mają datę ważności, a jeśli tak, ile powinien wynosić domyślny okres ważności oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="7fd8c-225">Można również określić, czy kandydaci mają prawo odrzucać oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="7fd8c-226">**Podpisy elektroniczne** — Obecnie jedną dostępną opcją podpisywania elektronicznego jest wpisanie przez kandydata swojego imienia i nazwiska w pakiecie oferty podczas akceptowania oferty.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="7fd8c-227">W przyszłości dodamy integrację z innymi rozwiązaniami dostawców usług podpisu elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="7fd8c-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="7fd8c-228">Aby uzyskać więcej informacji o procesie tworzenia oferty, zobacz [Tworzenie, zatwierdzanie i podpisywanie ofert](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="7fd8c-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
