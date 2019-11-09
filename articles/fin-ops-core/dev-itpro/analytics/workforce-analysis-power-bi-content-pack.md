---
title: Pakiet zawartości usługi Power BI Metryki pracowników
description: W tym temacie opisano pakiet zawartość Metryki pracowników dostępny dla usługi Power BI. Wyjaśniono, jak uzyskać dostęp do raportów, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkforceWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Talent
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 868b0781a84d345297ab40b1a423272e47d50ec5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249165"
---
# <a name="workforce-metrics-power-bi-content"></a><span data-ttu-id="37db6-104">Pakiet zawartości usługi Power BI Metryki pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-104">Workforce metrics Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37db6-105">W tym temacie opisano pakiet zawartość **Metryki pracowników** dostępny dla usługi Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="37db6-105">This topic describes the **Workforce metrics** Microsoft Power BI content.</span></span> <span data-ttu-id="37db6-106">Wyjaśniono, jak uzyskać dostęp do raportów programu Power BI, oraz zamieszczono informacje o modelu danych i jednostkach użytych do zbudowania pakietu.</span><span class="sxs-lookup"><span data-stu-id="37db6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="37db6-107">Przechodzenie do pakietu zawartości usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="37db6-107">Accessing the Power BI content</span></span>
<span data-ttu-id="37db6-108">Pakiet zawartości usługi Power BI zatytułowany **Metryki pracowników** jest wyświetlany w obszarze roboczym **Zarządzanie pracownikami**, jeśli używasz jednego z następujących produktów:</span><span class="sxs-lookup"><span data-stu-id="37db6-108">The **Workforce metrics** Power BI content appears in the **Personnel management** workspace if you use one of these products:</span></span>

- <span data-ttu-id="37db6-109">Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="37db6-109">Microsoft Dynamics 365 Finance</span></span>
- <span data-ttu-id="37db6-110">Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="37db6-110">Microsoft Dynamics 365 Talent</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="37db6-111">Wskaźniki umieszczone w pakiecie zawartości usługi Power BI</span><span class="sxs-lookup"><span data-stu-id="37db6-111">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="37db6-112">W poniższej tabeli pokazano mierniki dostępne na każdej stronie raportu.</span><span class="sxs-lookup"><span data-stu-id="37db6-112">The following table lists the metrics that are shown on each report.</span></span>

| <span data-ttu-id="37db6-113">Raport</span><span class="sxs-lookup"><span data-stu-id="37db6-113">Report</span></span>                                           | <span data-ttu-id="37db6-114">Metryki</span><span class="sxs-lookup"><span data-stu-id="37db6-114">Metrics</span></span> |
|--------------------------------------------------|---------|
| <span data-ttu-id="37db6-115">Mierniki osób</span><span class="sxs-lookup"><span data-stu-id="37db6-115">People Metrics</span></span>                                   | <span data-ttu-id="37db6-116">Podsumowanie innych raportów</span><span class="sxs-lookup"><span data-stu-id="37db6-116">Summary of other reports</span></span> |
| <span data-ttu-id="37db6-117">Analiza stanu osobowego według firmy, działu, lokalizacji</span><span class="sxs-lookup"><span data-stu-id="37db6-117">Headcount Analysis Company, Department, Location</span></span> | <span data-ttu-id="37db6-118">Stan osobowy według firmy, stan osobowy według działu, stan osobowy według lokalizacji i łączny stan osobowy</span><span class="sxs-lookup"><span data-stu-id="37db6-118">Headcount by company, headcount by department, headcount by location, and total headcount</span></span> |
| <span data-ttu-id="37db6-119">Analiza stanu osobowego według zadania, kroku i menedżera</span><span class="sxs-lookup"><span data-stu-id="37db6-119">Headcount Analysis Job, Step, Manager</span></span>            | <span data-ttu-id="37db6-120">Stan osobowy według zadania, stan osobowy według kroku, stan osobowy według menedżera i łączny stan osobowy</span><span class="sxs-lookup"><span data-stu-id="37db6-120">Headcount by job, headcount by step, headcount by manager, and total headcount</span></span> |
| <span data-ttu-id="37db6-121">Analiza trendu stanu osobowego</span><span class="sxs-lookup"><span data-stu-id="37db6-121">Headcount Trend Analysis</span></span>                         | <span data-ttu-id="37db6-122">Stan osobowy w tym roku w porównaniu z zeszłym rokiem z podziałem na firmy oraz skumulowany stan osobowy w ciągu ostatnich 12 miesięcy</span><span class="sxs-lookup"><span data-stu-id="37db6-122">Headcount this year versus last year by company and rolling headcount for the last 12 months</span></span> |
| <span data-ttu-id="37db6-123">Analiza FTE</span><span class="sxs-lookup"><span data-stu-id="37db6-123">FTE Analysis</span></span>                                     | <span data-ttu-id="37db6-124">Suma etatów przeliczeniowych (przeliczeniu na pełne etaty), suma przypisanych etatów przeliczeniowych, etaty przeliczeniowe według działów, etaty przeliczeniowe w ciągu ostatnich 12 miesięcy oraz etaty przeliczeniowe według zadań</span><span class="sxs-lookup"><span data-stu-id="37db6-124">Total full-time equivalent (FTE), total assigned FTE, FTE by department, FTE for the last 12 months, and FTE by job</span></span> |
| <span data-ttu-id="37db6-125">Dane demograficzne pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-125">Workforce Demographics</span></span>                           | <span data-ttu-id="37db6-126">Stan osobowy według wieku i płci, stan osobowy według pochodzenia etnicznego, stan osobowy według statusu weterana wojennego, stan osobowy według stanu cywilnego, liczba studentów na studiach dziennych, średni staż pracy, średni wiek, stosunek liczby kobiet do liczby mężczyzn oraz języki używane przez pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-126">Headcount by age and gender, headcount by ethnic origin, headcount by veteran status, headcount by marital status, number of full-time students, average tenure, average age, ratio of female to male employees, and languages spoken by employees</span></span> |
| <span data-ttu-id="37db6-127">Analiza stanowisk</span><span class="sxs-lookup"><span data-stu-id="37db6-127">Position Analysis</span></span>                                | <span data-ttu-id="37db6-128">Wolne stanowiska według działu, stanowiska wolne do obsadzenia, stosunek liczby stanowisk aktywnych do nieaktywnych oraz stanowiska według działów</span><span class="sxs-lookup"><span data-stu-id="37db6-128">Open positions by department, open-to-filled positions, active-to-inactive positions, and positions by department</span></span> |
| <span data-ttu-id="37db6-129">Analiza rotacji</span><span class="sxs-lookup"><span data-stu-id="37db6-129">Attrition Analysis</span></span>                               | <span data-ttu-id="37db6-130">Rotacja w tym roku w porównaniu do ubiegłego, rotacja, odchodzący pracownicy według wieku i płci, średni staż pracy odchodzących pracowników, pracownicy odchodzący w tym miesiącu oraz odejścia pracowników z podziałem na przyczyny</span><span class="sxs-lookup"><span data-stu-id="37db6-130">Attrition this year versus last year, attrition, exiting employees by age and gender, average tenure of employees leaving, employees exiting this month, and employees leaving by reason</span></span> |
| <span data-ttu-id="37db6-131">Pracownicy wg działów</span><span class="sxs-lookup"><span data-stu-id="37db6-131">People by department</span></span>                             | <span data-ttu-id="37db6-132">Pracownicy z numerami pracowniczymi według działów, stanowisk oraz dat rozpoczęcia i zakończenia przypisania do stanowiska</span><span class="sxs-lookup"><span data-stu-id="37db6-132">Employees with a personnel number by department, position, and assignment start and end dates</span></span> |
| <span data-ttu-id="37db6-133">Analiza stażu pracy</span><span class="sxs-lookup"><span data-stu-id="37db6-133">Seniority Analysis</span></span>                               | <span data-ttu-id="37db6-134">Średni staż pracy, średni staż pracy według firmy, lista stażu pracy</span><span class="sxs-lookup"><span data-stu-id="37db6-134">Average tenure, average years of service by company, and seniority list</span></span> |
| <span data-ttu-id="37db6-135">Rocznice pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-135">Employee Anniversaries</span></span>                           | <span data-ttu-id="37db6-136">Rocznice w tym miesiącu, rocznice w przyszłym miesiącu, pracownicy według stażu pracy i rocznic, staż pracy według działów</span><span class="sxs-lookup"><span data-stu-id="37db6-136">Anniversaries this month, anniversaries next month, employees by years of service, and anniversaries, years of service by department</span></span> |
| <span data-ttu-id="37db6-137">Urodziny pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-137">Employee Birthdays</span></span>                               | <span data-ttu-id="37db6-138">Urodziny w tym miesiącu, urodziny w następnym miesiącu, urodziny pracowników oraz urodziny według miesięcy i działów</span><span class="sxs-lookup"><span data-stu-id="37db6-138">Birthdays this month, birthdays next month, employee birthdays, and birthdays by month and department</span></span> |
| <span data-ttu-id="37db6-139">Projekty zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-139">Mass Hire Projects</span></span>                               | <span data-ttu-id="37db6-140">Projekty zatrudnienia grupowego razem, projekty zatrudnienia grupowego według stanów, projekty zatrudnienia grupowego według działów i właścicieli, projektów zatrudnienia grupowego według zadań oraz projekty zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-140">Total mass hire projects, mass hire projects by status, mass hire projects by department and owner, mass hire projects by job, and mass hire projects</span></span> |

<span data-ttu-id="37db6-141">Wykresy i kafelki w tych raportach można filtrować oraz przypinać do pulpitu nawigacyjnego.</span><span class="sxs-lookup"><span data-stu-id="37db6-141">You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard.</span></span> <span data-ttu-id="37db6-142">Aby uzyskać więcej informacji na temat filtrowania i przypinania w usłudze Power BI, zobacz [Tworzenie i konfigurowanie pulpitu nawigacyjnego](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span><span class="sxs-lookup"><span data-stu-id="37db6-142">For more information about how to filter and pin in Power BI, see [Create and configure a dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

<span data-ttu-id="37db6-143">Uważaj, aby pobrać pakiet zawartości usługi Power BI **Metryki pracowników** mający zastosowanie do używanej wersji systemu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="37db6-143">Be sure to download the **Workforce metrics** Power BI content that applies to the version of Microsoft Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="37db6-144">Pliki .pbix dostępne w usłudze Lifecycle Services dotyczą tylko aplikacji Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="37db6-144">The .pbix files available in Lifecycle Services apply to Finance and Operations apps only.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="37db6-145">Opis modelu danych i jednostek</span><span class="sxs-lookup"><span data-stu-id="37db6-145">Understanding the data model and entities</span></span>
<span data-ttu-id="37db6-146">W poniższej tabeli przedstawiono jednostki, na których bazuje pakiet.</span><span class="sxs-lookup"><span data-stu-id="37db6-146">The following table shows the entities that the content was based on.</span></span>

| <span data-ttu-id="37db6-147">Jednostka</span><span class="sxs-lookup"><span data-stu-id="37db6-147">Entity</span></span>                   | <span data-ttu-id="37db6-148">Zawartość</span><span class="sxs-lookup"><span data-stu-id="37db6-148">Contents</span></span>                                                                            | <span data-ttu-id="37db6-149">Powiązania z innymi jednostkami</span><span class="sxs-lookup"><span data-stu-id="37db6-149">Relationships with other entities</span></span> |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="37db6-150">Przesunięcie kalendarza</span><span class="sxs-lookup"><span data-stu-id="37db6-150">Calendar Offset</span></span>          | <span data-ttu-id="37db6-151">Przesunięcia kalendarzy dla raportów wycinkowych</span><span class="sxs-lookup"><span data-stu-id="37db6-151">Calendar offsets to slice reports</span></span>                                                   | <span data-ttu-id="37db6-152">Przeszłe przypisania stanowisk, Trend stanowisk, Trend pracowników, Pracownik z rozwiązanym stosunkiem pracy</span><span class="sxs-lookup"><span data-stu-id="37db6-152">Past Position Assignment, Position Trend, Employee Trend, Terminated Employee</span></span> |
| <span data-ttu-id="37db6-153">Firma</span><span class="sxs-lookup"><span data-stu-id="37db6-153">Company</span></span>                  | <span data-ttu-id="37db6-154">Firmy, według których będą filtrowane raporty</span><span class="sxs-lookup"><span data-stu-id="37db6-154">Companies to filter reports by</span></span>                                                      | <span data-ttu-id="37db6-155">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-155">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-156">Bieżące stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-156">Current Position</span></span>         | <span data-ttu-id="37db6-157">Stanowiska na obecny dzień, etat przeliczeniowy (FTE), wolne stanowiska i stanowiska wolne do obsadzenia</span><span class="sxs-lookup"><span data-stu-id="37db6-157">Positions as of the current date, FTE, open positions, and open-to-filled positions</span></span> | <span data-ttu-id="37db6-158">Zadanie, Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-158">Job, Position</span></span> |
| <span data-ttu-id="37db6-159">Bieżący pracownik etatowy</span><span class="sxs-lookup"><span data-stu-id="37db6-159">Current Employee</span></span>         | <span data-ttu-id="37db6-160">Liczba pracowników na obecny dzień, wiek i stan osobowy</span><span class="sxs-lookup"><span data-stu-id="37db6-160">Workers as of the current date, age, and headcount</span></span>                                  | <span data-ttu-id="37db6-161">Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Tytuł pracownika, Dane demograficzne, Zadanie, Zatrudnienie, Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-161">Company, Geographic Location, Employee Name, Reports To, Employee Title, Demographics, Job, Employment, Position</span></span> |
| <span data-ttu-id="37db6-162">Data</span><span class="sxs-lookup"><span data-stu-id="37db6-162">Date</span></span>                     | <span data-ttu-id="37db6-163">Dni, tygodnie, miesiące i lata</span><span class="sxs-lookup"><span data-stu-id="37db6-163">Days, weeks, months, and years</span></span>                                                      | <span data-ttu-id="37db6-164">Przeszłe przypisania stanowisk, Trend stanowisk, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-164">Past Position Assignment, Position Trend, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-165">Dane demograficzne</span><span class="sxs-lookup"><span data-stu-id="37db6-165">Demographics</span></span>             | <span data-ttu-id="37db6-166">Data urodzenia, płeć, pochodzenie etniczne i stan cywilny</span><span class="sxs-lookup"><span data-stu-id="37db6-166">Date of birth, gender, ethnic origin, and marital status</span></span>                            | <span data-ttu-id="37db6-167">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-167">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-168">Zatrudnienie</span><span class="sxs-lookup"><span data-stu-id="37db6-168">Employment</span></span>               | <span data-ttu-id="37db6-169">Data rozpoczęcia, data zakończenia i data przejścia</span><span class="sxs-lookup"><span data-stu-id="37db6-169">Start date, end date, and transition date</span></span>                                           | <span data-ttu-id="37db6-170">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-170">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-171">Położenie geograficzne</span><span class="sxs-lookup"><span data-stu-id="37db6-171">Geographic Location</span></span>      | <span data-ttu-id="37db6-172">Miejscowość, kod pocztowy i województwo</span><span class="sxs-lookup"><span data-stu-id="37db6-172">City, county, postal code, and state or province</span></span>                                    | <span data-ttu-id="37db6-173">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-173">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-174">Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-174">Job</span></span>                      | <span data-ttu-id="37db6-175">Funkcja, typ i tytuł</span><span class="sxs-lookup"><span data-stu-id="37db6-175">Function, type, and title</span></span>                                                           | <span data-ttu-id="37db6-176">Bieżące stanowisko, Bieżący pracownik etatowy</span><span class="sxs-lookup"><span data-stu-id="37db6-176">Current Position, Current Employee</span></span> |
| <span data-ttu-id="37db6-177">Przeszłe przypisania stanowisk</span><span class="sxs-lookup"><span data-stu-id="37db6-177">Past Position Assignment</span></span> | <span data-ttu-id="37db6-178">Przyczyna przypisania, data rozpoczęcia, data zakończenia i zadanie</span><span class="sxs-lookup"><span data-stu-id="37db6-178">Assignment reason, start date, end date, and job</span></span>                                    | <span data-ttu-id="37db6-179">Przesunięcie kalendarza, Data, Zadanie, Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-179">Calendar Offset, Date, Job, Position</span></span> |
| <span data-ttu-id="37db6-180">Pozycja</span><span class="sxs-lookup"><span data-stu-id="37db6-180">Position</span></span>                 | <span data-ttu-id="37db6-181">Dział, równoważnik pełnego etatu, stanowisko, typ stanowiska i tytuł</span><span class="sxs-lookup"><span data-stu-id="37db6-181">Department, FTE, position, position type, and title</span></span>                                 | <span data-ttu-id="37db6-182">Bieżące stanowisko, Bieżący pracownik etatowy</span><span class="sxs-lookup"><span data-stu-id="37db6-182">Current Position, Current Employee</span></span> |
| <span data-ttu-id="37db6-183">Trend stanowisk</span><span class="sxs-lookup"><span data-stu-id="37db6-183">Position Trend</span></span>           | <span data-ttu-id="37db6-184">Stanowiska zajmowane w okresie, równoważnik pełnego etatu i zadanie</span><span class="sxs-lookup"><span data-stu-id="37db6-184">Positions over time, FTE, and job</span></span>                                                   | <span data-ttu-id="37db6-185">Przesunięcie kalendarza, Data, Zadanie, Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-185">Calendar Offset, Date, Job, Position</span></span> |
| <span data-ttu-id="37db6-186">Przełożony</span><span class="sxs-lookup"><span data-stu-id="37db6-186">Reports To</span></span>               | <span data-ttu-id="37db6-187">Imię, drugie imię i nazwisko</span><span class="sxs-lookup"><span data-stu-id="37db6-187">First name, last name, and full name</span></span>                                                | <span data-ttu-id="37db6-188">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-188">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-189">Pracownik z rozwiązanym stosunkiem pracy</span><span class="sxs-lookup"><span data-stu-id="37db6-189">Terminated Employee</span></span>      | <span data-ttu-id="37db6-190">Zwolnieni pracownicy, data rozwiązania stosunku pracy, tytuł, stanowisko i zadanie</span><span class="sxs-lookup"><span data-stu-id="37db6-190">Terminated workers, termination date, title, position, and job</span></span>                      | <span data-ttu-id="37db6-191">Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Przesunięcie kalendarza, Data, Tytuł pracownika, Dane demograficzne, Zatrudnienie, Zadanie, Stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-191">Company, Geographic Location, Employee Name, Reports To, Calendar Offset, Date, Employee Title, Demographics, Employment, Job, Position</span></span> |
| <span data-ttu-id="37db6-192">Nazwisko pracownika etatowego</span><span class="sxs-lookup"><span data-stu-id="37db6-192">Employee Name</span></span>            | <span data-ttu-id="37db6-193">Imię, drugie imię i nazwisko</span><span class="sxs-lookup"><span data-stu-id="37db6-193">First name, last name, and full name</span></span>                                                | <span data-ttu-id="37db6-194">Bieżący pracownik, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-194">Current Worker, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-195">Tytuł pracownika</span><span class="sxs-lookup"><span data-stu-id="37db6-195">Employee Title</span></span>           | <span data-ttu-id="37db6-196">Tytuł i data ustalenia stażu pracy</span><span class="sxs-lookup"><span data-stu-id="37db6-196">Title and seniority date</span></span>                                                            | <span data-ttu-id="37db6-197">Bieżący pracownik etatowy, Pracownik z rozwiązanym stosunkiem pracy, Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-197">Current Employee, Terminated Employee, Employee Trend</span></span> |
| <span data-ttu-id="37db6-198">Trend pracowników</span><span class="sxs-lookup"><span data-stu-id="37db6-198">Employee Trend</span></span>           | <span data-ttu-id="37db6-199">Liczba pracowników w okresie, stan osobowy, firma i stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-199">Workers over time, headcount, company, and position</span></span>                                 | <span data-ttu-id="37db6-200">Firma, Położenie geograficzne, Nazwisko pracownika etatowego, Przełożony, Przesunięcie kalendarza, Data, Tytuł pracownika, Dane demograficzne, Zatrudnienie, Zadanie</span><span class="sxs-lookup"><span data-stu-id="37db6-200">Company, Geographic Location, Employee Name, Reports To, Calendar Offset, Date, Employee Title, Demographics, Employment, Job</span></span> |
| <span data-ttu-id="37db6-201">Projekt zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-201">Mass Hire Project</span></span>        | <span data-ttu-id="37db6-202">Liczba projektów zatrudnienia grupowego, właściciel projektu oraz stan projektu</span><span class="sxs-lookup"><span data-stu-id="37db6-202">Number of mass hire projects, project owner, and project status</span></span>                     | <span data-ttu-id="37db6-203">Firma, Wiersz zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-203">Company, Mass Hire Line</span></span> |
| <span data-ttu-id="37db6-204">Wiersz zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-204">Mass Hire Line</span></span>           | <span data-ttu-id="37db6-205">Dział, typ zatrudnienia i stanowisko</span><span class="sxs-lookup"><span data-stu-id="37db6-205">Department, employment type, and position</span></span>                                           | <span data-ttu-id="37db6-206">Data, Zadanie, Projekt zatrudnienia grupowego</span><span class="sxs-lookup"><span data-stu-id="37db6-206">Date, Job, Mass Hire Project</span></span> |