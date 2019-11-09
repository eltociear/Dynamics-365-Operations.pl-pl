---
title: Definiowanie procesu związanego z wynagrodzeniem i obliczanie wyników
description: Procesy wynagrodzeń służą do określania nowych kwot wynagrodzeń i nagród dla pracowników objętych planami wynagrodzeń stałych i o zmiennej wysokości.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0825c80e43baf0803552f7051dca5ee79dbe521e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179513"
---
# <a name="define-compensation-process-and-calculate-results"></a><span data-ttu-id="736ea-103">Definiowanie procesu związanego z wynagrodzeniem i obliczanie wyników</span><span class="sxs-lookup"><span data-stu-id="736ea-103">Define compensation process and calculate results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="736ea-104">Procesy wynagrodzeń służą do określania nowych kwot wynagrodzeń i nagród dla pracowników objętych planami wynagrodzeń stałych i o zmiennej wysokości.</span><span class="sxs-lookup"><span data-stu-id="736ea-104">Compensation processes are used to determine new compensation amounts and awards for employees enrolled in fixed and variable compensation plans.</span></span> <span data-ttu-id="736ea-105">Procesy wynagrodzeń można uruchamiać wiele razy w celu przeprowadzenia analizy „co, jeśli” i zweryfikowania, czy wszystkie zmiany i ustawienia są poprawne.</span><span class="sxs-lookup"><span data-stu-id="736ea-105">Compensation processes can be run multiple times to perform "what-if" analysis, to verify all changes and settings are correct.</span></span> <span data-ttu-id="736ea-106">Ta procedura spowoduje utworzenie procesu wynagrodzenia, wykonanie go i wyświetlenie wyników.</span><span class="sxs-lookup"><span data-stu-id="736ea-106">This procedure will create a compensation process, run the process, and view the results.</span></span> <span data-ttu-id="736ea-107">Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej USMF.</span><span class="sxs-lookup"><span data-stu-id="736ea-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-compensation-process"></a><span data-ttu-id="736ea-108">Tworzenie procesu wynagrodzenia</span><span class="sxs-lookup"><span data-stu-id="736ea-108">Create a compensation process</span></span>
1. <span data-ttu-id="736ea-109">Wybierz kolejno opcje Zasoby ludzkie > Wynagrodzenia > Proces > Procesy związane z wynagrodzeniami.</span><span class="sxs-lookup"><span data-stu-id="736ea-109">Go to Human resources > Compensation > Process > Compensation processes.</span></span>
2. <span data-ttu-id="736ea-110">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="736ea-110">Click New.</span></span>
3. <span data-ttu-id="736ea-111">W polu Proces wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="736ea-111">In the Process field, type a value.</span></span>
4. <span data-ttu-id="736ea-112">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="736ea-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="736ea-113">W polu Typ procesu wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="736ea-113">In the Process type field, select an option.</span></span>
    * <span data-ttu-id="736ea-114">Cykl definiuje okres oceniany w celu określenia wynagrodzenia.</span><span class="sxs-lookup"><span data-stu-id="736ea-114">A cycle specifies the time period evaluated to determine compensation.</span></span> <span data-ttu-id="736ea-115">Ocena bierze pod uwagę, jakie stanowiska zajmowali pracownicy, które oceny wydajności mają zostać uwzględnione, obliczenia wartości procentowej czasu, przez który pracownik był zatrudniony podczas cyklu, itd.</span><span class="sxs-lookup"><span data-stu-id="736ea-115">The evaluation considers which positions were held by employees, which performance ratings to include, calculation of the percentage of time the employee was employed during the cycle, and more.</span></span> <span data-ttu-id="736ea-116">Przykładem data rozpoczęcia cyklu może być pierwszy dzień minionego roku obrachunkowego.</span><span class="sxs-lookup"><span data-stu-id="736ea-116">An example of a cycle start date might be the first day of the past fiscal year.</span></span>  
6. <span data-ttu-id="736ea-117">W polu Rozpoczęcie cyklu wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="736ea-117">In the Cycle start field, enter a date.</span></span>
    * <span data-ttu-id="736ea-118">Data zakończenia cyklu jest ważna, ponieważ jest to data używana do określania, którzy pracownicy byli aktywnie zatrudnieni i zarejestrowany w co najmniej jednym planem wynagrodzeń.</span><span class="sxs-lookup"><span data-stu-id="736ea-118">The cycle end date is  important because it is the date used to determine which employees were actively employed and enrolled in one or more compensation plans.</span></span>  
7. <span data-ttu-id="736ea-119">W polu Zakończenie cyklu wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="736ea-119">In the Cycle end field, enter a date.</span></span>
    * <span data-ttu-id="736ea-120">Datą aktywacji transakcji jest dzień, od którego nowe stawki wynagrodzeń mają zacząć obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="736ea-120">The transaction active date is the date the new compensation rates should take effect.</span></span> <span data-ttu-id="736ea-121">Wiele firm stosuje kilka miesięcy przerwy między końcem cyklu a czasem, kiedy nowe stawki wynagrodzeń zaczynają obowiązywać.</span><span class="sxs-lookup"><span data-stu-id="736ea-121">Many companies include a few months between their end of a cycle and the time the new compensation rates go into effect.</span></span> <span data-ttu-id="736ea-122">Dodatkowy czas jest używany do przetwarzania i przeglądania nowych wynagrodzeń.</span><span class="sxs-lookup"><span data-stu-id="736ea-122">The additional time is used for processing and reviewing the new compensation.</span></span>  
8. <span data-ttu-id="736ea-123">W polu Data aktywacji transakcji wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="736ea-123">In the Transaction active date field, enter a date.</span></span>
    * <span data-ttu-id="736ea-124">Data stałego punktu odniesienia jest używana w planach wynagrodzeń o zmiennej wysokości, które określają kwotę nagrody dla pracownika na podstawie jego stawki wynagrodzenia w tym momencie.</span><span class="sxs-lookup"><span data-stu-id="736ea-124">The point-in-time date is used for variable compensation plans that determine an employee's award amount based on their compensation rate at this point in time.</span></span>  
    * <span data-ttu-id="736ea-125">Data określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia jest używana w planach stałych wynagrodzeń z regułą zatrudnienia Procent.</span><span class="sxs-lookup"><span data-stu-id="736ea-125">The fixed pay pro rated hire date is used with fixed compensation plans with a hire rule of Percent.</span></span>  <span data-ttu-id="736ea-126">Pracownicy, którzy zostali zatrudnieni między rozpoczęciem cyklu a datą określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia, otrzymają 100% obliczonego wzrostu wynagrodzenia zamiast proporcjonalnego procentu.</span><span class="sxs-lookup"><span data-stu-id="736ea-126">Employees who are hired between the cycle start and the fixed pay pro rated hire date will receive 100% of their calculated compensation increase, instead of pro-rated percentage.</span></span>  
9. <span data-ttu-id="736ea-127">W polu Data określenia stałego wynagrodzenia proporcjonalnie do zatrudnienia wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="736ea-127">In the Fixed pay pro rated hire date field, enter a date.</span></span>
    * <span data-ttu-id="736ea-128">Termin przeglądu to dzień, do którego wszystkie wyniki procesów powinny zostać przejrzane, tak aby można było je załadować do rekordu wynagrodzenia pracownika przed datą aktywacji transakcji.</span><span class="sxs-lookup"><span data-stu-id="736ea-128">The review deadline is the date by which all process results should be reviewed so that they can be loaded into an employee's compensation record before the transaction active date.</span></span> <span data-ttu-id="736ea-129">To pole służy wyłącznie do celów informacyjnych.</span><span class="sxs-lookup"><span data-stu-id="736ea-129">This field is informational only.</span></span>  
10. <span data-ttu-id="736ea-130">W polu Termin przeglądu wprowadź datę.</span><span class="sxs-lookup"><span data-stu-id="736ea-130">In the Review deadline field, enter a date.</span></span>
11. <span data-ttu-id="736ea-131">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="736ea-131">Click Save.</span></span>

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a><span data-ttu-id="736ea-132">Konfigurowanie planów i działań wynagrodzenia dla procesu wynagrodzenia</span><span class="sxs-lookup"><span data-stu-id="736ea-132">Setup the compensation plans and actions for a compensation process</span></span>
1. <span data-ttu-id="736ea-133">Kliknij przycisk Ustawienia.</span><span class="sxs-lookup"><span data-stu-id="736ea-133">Click Setup.</span></span>
    * <span data-ttu-id="736ea-134">Strona Ustawienia służy do wybrania, które plany mają być przetwarzane w ramach tego procesu wynagrodzenia, a także które akcje mają zostać wykonane dla każdego planu.</span><span class="sxs-lookup"><span data-stu-id="736ea-134">The Setup page is used to select which plans to process as part of this compensation process, as well as which actions should be taken against each plan.</span></span>  
2. <span data-ttu-id="736ea-135">W polu Plan wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="736ea-135">In the Plan field, enter or select a value.</span></span>
3. <span data-ttu-id="736ea-136">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="736ea-136">Click Save.</span></span>
4. <span data-ttu-id="736ea-137">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-137">Click Add.</span></span>
5. <span data-ttu-id="736ea-138">W polu Akcja wybierz akcję typu Kapitał własny.</span><span class="sxs-lookup"><span data-stu-id="736ea-138">In the Action field, select an Equity type of action.</span></span>
6. <span data-ttu-id="736ea-139">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-139">Click Add.</span></span>
7. <span data-ttu-id="736ea-140">W polu Akcja wybierz akcję typu Wartość.</span><span class="sxs-lookup"><span data-stu-id="736ea-140">In the Action field, select a Merit type of action.</span></span>
    * <span data-ttu-id="736ea-141">Akcje dotyczące wynagrodzeń mogą być „łączone” z sobą przy użyciu pola Użyj poprzedniego wyniku, aby wskazać, czy wybrana akcja powinna używać podstawowego wynagrodzenia pracowników czy też wyniku poprzedniej akcji jako punktu wyjścia dla obliczeń w tej akcji.</span><span class="sxs-lookup"><span data-stu-id="736ea-141">Compensation actions can be "chained" together using the Use previous result field to indicate whether the selected action should use the employees base pay or the result of the previous action as the starting point for this action's calculation.</span></span>  
8. <span data-ttu-id="736ea-142">W polu Użyj poprzedniego wyniku zaznacz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="736ea-142">Select Yes in the Use previous result field.</span></span>
9. <span data-ttu-id="736ea-143">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-143">Click Add.</span></span>
10. <span data-ttu-id="736ea-144">W polu Akcja wybierz akcję typu Ogólne.</span><span class="sxs-lookup"><span data-stu-id="736ea-144">In the Action field, select a General type of Action.</span></span>
    * <span data-ttu-id="736ea-145">Różne typy akcji dotyczących wynagrodzeń włączają różne pola.</span><span class="sxs-lookup"><span data-stu-id="736ea-145">Different compensation action types enable different fields.</span></span> <span data-ttu-id="736ea-146">Dla typu akcji Ogólne można określić procent podwyżki lub kwotę podwyżki.</span><span class="sxs-lookup"><span data-stu-id="736ea-146">For a General compensation action type, an increase percent or increase amount can be specified.</span></span>  
11. <span data-ttu-id="736ea-147">Zaznacz opcję Wybierz kwotę podwyżki.</span><span class="sxs-lookup"><span data-stu-id="736ea-147">Select the Select increase amount option.</span></span>
12. <span data-ttu-id="736ea-148">W polu Kwota podwyżki wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="736ea-148">In the Increase amount field, enter a number.</span></span>
13. <span data-ttu-id="736ea-149">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-149">Click Add.</span></span>
14. <span data-ttu-id="736ea-150">W polu Akcja wybierz akcję typu Promocja.</span><span class="sxs-lookup"><span data-stu-id="736ea-150">In the Action field, select a Promotion type of Action.</span></span>
    * <span data-ttu-id="736ea-151">Typy akcji Promocja i Inna zmiana poziomu umożliwiają użytkownikom wprowadzanie ręcznych korekt wynagrodzeń pracowników.</span><span class="sxs-lookup"><span data-stu-id="736ea-151">Promotion and Other level change action types enable users to make manual adjustments to employee compensation.</span></span> <span data-ttu-id="736ea-152">Dla tych typów akcji można włączyć zalecenia, a także inne typy akcji umożliwiających wprowadzenie nowej rekomendowanej wartości wynagrodzenia dla pracownika.</span><span class="sxs-lookup"><span data-stu-id="736ea-152">Recommendations can be enabled for these action types, as well as other action types to enable you to enter a new recommended compensation value for an employee.</span></span>  
15. <span data-ttu-id="736ea-153">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-153">Click Add.</span></span>
16. <span data-ttu-id="736ea-154">W polu Typ wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="736ea-154">In the Type field, select an option.</span></span>
    * <span data-ttu-id="736ea-155">Plany wynagrodzeń stałe i o zmiennej wysokości można przetwarzać w tym samym procesie wynagrodzenia.</span><span class="sxs-lookup"><span data-stu-id="736ea-155">Fixed and variable compensation plans can be run in the same compensation process.</span></span>  
17. <span data-ttu-id="736ea-156">W polu Plan wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="736ea-156">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="736ea-157">Zaznacz pole wyboru Włącz wynagrodzenie za wyniki, aby określić, czy stałe i zmienne kwoty wynagrodzeń mają być korygowane zależnie od oceny wydajności pracownika.</span><span class="sxs-lookup"><span data-stu-id="736ea-157">Use the Enable pay for performance check box to determined whether fixed and variable compensation amounts should be adjusted based on the employee's performance rating.</span></span>  
    * <span data-ttu-id="736ea-158">Dźwignia finansowa może być zastępowana w planach wynagrodzeń o zmiennej wysokości.</span><span class="sxs-lookup"><span data-stu-id="736ea-158">Leverage can be overridden on variable compensation plans.</span></span>  
18. <span data-ttu-id="736ea-159">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="736ea-159">Click Save.</span></span>
19. <span data-ttu-id="736ea-160">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="736ea-160">Click Add.</span></span>
20. <span data-ttu-id="736ea-161">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="736ea-161">Close the page.</span></span>

## <a name="run-the-compensation-process"></a><span data-ttu-id="736ea-162">Wykonywanie procesu wynagrodzenia</span><span class="sxs-lookup"><span data-stu-id="736ea-162">Run the compensation process</span></span>
1. <span data-ttu-id="736ea-163">Kliknij opcję Uruchom proces.</span><span class="sxs-lookup"><span data-stu-id="736ea-163">Click Run process.</span></span>
    * <span data-ttu-id="736ea-164">Formant Pokaż wyniki przetwarzania umożliwia przeglądanie komunikatów o przetwarzaniu dla całego procesu wynagrodzenia po zakończeniu przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="736ea-164">The Show processing results control lets you view processing messages for the complete compensation process when processing has finished.</span></span>  
2. <span data-ttu-id="736ea-165">W polu Pokaż wyniki przetwarzania zaznacz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="736ea-165">Select Yes in the Show processing results field.</span></span>
3. <span data-ttu-id="736ea-166">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="736ea-166">Click OK.</span></span>

## <a name="view-the-results"></a><span data-ttu-id="736ea-167">Wyświetlanie wyników</span><span class="sxs-lookup"><span data-stu-id="736ea-167">View the results</span></span>
1. <span data-ttu-id="736ea-168">Kliknij opcję Wyniki procesu.</span><span class="sxs-lookup"><span data-stu-id="736ea-168">Click Process results.</span></span>
2. <span data-ttu-id="736ea-169">Kliknij opcję Wyniki pracownika.</span><span class="sxs-lookup"><span data-stu-id="736ea-169">Click Employee results.</span></span>
3. <span data-ttu-id="736ea-170">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="736ea-170">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="736ea-171">Rozwiń sekcję Stałe wynagrodzenie.</span><span class="sxs-lookup"><span data-stu-id="736ea-171">Expand the Fixed compensation section.</span></span>
    * <span data-ttu-id="736ea-172">Rozwiń skrócone karty, aby wyświetlić wyniki procesu.</span><span class="sxs-lookup"><span data-stu-id="736ea-172">Expand the FastTabs to view the results of the process.</span></span> <span data-ttu-id="736ea-173">Jeśli dla akcji dotyczącej wynagrodzenia zaznaczono opcję Włącz rekomendacje, pola Propozycja płacowa będą włączone dla tej akcji.</span><span class="sxs-lookup"><span data-stu-id="736ea-173">If Enable recommendations was marked for a compensation action, the Recommendation fields will be enabled for that action.</span></span>  
5. <span data-ttu-id="736ea-174">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="736ea-174">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="736ea-175">Wyniki dla jednego pracownika można wyświetlić przez kliknięcie przycisku Wyświetl wyniki.</span><span class="sxs-lookup"><span data-stu-id="736ea-175">The results for a single employee can be viewed by clicking the View results button.</span></span>  
    * <span data-ttu-id="736ea-176">Obliczoną kwotę wynagrodzenia można zastąpić, korygując procent lub kwotę podwyżki w polach Propozycja płacowa.</span><span class="sxs-lookup"><span data-stu-id="736ea-176">You can overwrite the calculated compensation amount by adjusting the percent or the increase amount in the Recommendation fields.</span></span>  
6. <span data-ttu-id="736ea-177">W polu Proponowany procent wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="736ea-177">In the percent recommended field, enter a number.</span></span>
7. <span data-ttu-id="736ea-178">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="736ea-178">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="736ea-179">W polu Proponowany procent wpisz liczbę.</span><span class="sxs-lookup"><span data-stu-id="736ea-179">In the percent recommended field, enter a number.</span></span>
    * <span data-ttu-id="736ea-180">Ponownego obliczania można użyć w celu zignorowania wszelkich zmiany wprowadzonych w istniejącym rekordzie oraz wygenerowania nowego wyniku wynagrodzenia dla wybranego pracownika.</span><span class="sxs-lookup"><span data-stu-id="736ea-180">Recalculate can be used to ignore any changes made to the existing record and generate a new compensation result for the selected employee.</span></span>  
    * <span data-ttu-id="736ea-181">Po wprowadzeniu wszystkich zmian dla pracownika należy zmienić stan na Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="736ea-181">When all changes are complete for an employee, change the status to Approved.</span></span>  
9. <span data-ttu-id="736ea-182">Kliknij przycisk Zmień stan.</span><span class="sxs-lookup"><span data-stu-id="736ea-182">Click Change status.</span></span>
10. <span data-ttu-id="736ea-183">Kliknij przycisk Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="736ea-183">Click Approved.</span></span>
    * <span data-ttu-id="736ea-184">Po zatwierdzeniu rekordu można go załadować do oficjalnego rekordu wynagrodzenia pracownika.</span><span class="sxs-lookup"><span data-stu-id="736ea-184">After the record has been approved it can be loaded to the employee's official compensation record.</span></span> <span data-ttu-id="736ea-185">Nowe wynagrodzenie będzie obowiązywać od dnia transakcji ustawionego w procesie wynagrodzenia.</span><span class="sxs-lookup"><span data-stu-id="736ea-185">The new compensation will be effective as of the transaction date set on the compensation process.</span></span>  
