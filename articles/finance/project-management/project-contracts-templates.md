---
title: Synchronizowanie umów na projekty i projektów bezpośrednio z programu Project Service Automation do programu Finance and Operations
description: Ten temat zawiera opis szablonu i podstawowych zadań, które są używane do synchronizowania umów projektu i projektów bezpośrednio między Microsoft Dynamics 365 Project Service Automation a programem Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250468"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="226bd-103">Synchronizowanie umów na projekty i projektów bezpośrednio z programu Project Service Automation do programu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="226bd-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="226bd-104">Ten temat zawiera opis szablonu i podstawowych zadań, które są używane do synchronizowania umów projektu i projektów bezpośrednio między programem Dynamics 365 Project Service Automation a programem Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="226bd-105">Jeśli używasz programu Enterprise Edition 7.3.0, należy zainstalować poprawkę KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="226bd-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="226bd-106">Przepływ danych z programu Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="226bd-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="226bd-107">Zanim będzie można używać rozwiązania do integrowania aplikacji Project Service Automation z Finance, należy się zapoznać z funkcją Integracja danych dostępną w programie Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="226bd-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="226bd-108">Rozwiązanie integracji rozwiązania Project Service Automation dp Finance korzysta z funkcji integracji danych do synchronizowania danych między wystąpieniami rozwiązania Project Service Automation oraz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="226bd-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="226bd-109">Szablon integracji, który jest dostępny z funkcji integracji danych, umożliwia przepływ danych na temat umów dotyczących projektów, projektów, wierszy umowy dotyczącej projektu i punktów kontrolnych wiersza umowy projektu z rozwiązania Project Service Automation do rozwiązania Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="226bd-110">Na poniższej ilustracji przedstawiono, w jaki sposób dane są synchronizowane pomiędzy rozwiązaniami Project Service Automation oraz Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="226bd-111">[![Przepływ danych w integracji programu Project Service Automation z programem Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="226bd-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="226bd-112">Szablony i zadania</span><span class="sxs-lookup"><span data-stu-id="226bd-112">Templates and tasks</span></span>

<span data-ttu-id="226bd-113">Aby przejść do dostępnych szablonów, w centrum administracyjnym usługi Microsoft PowerApps wybierz opcję **Projekty** i w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać spośród szablonów publicznych.</span><span class="sxs-lookup"><span data-stu-id="226bd-113">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="226bd-114">Następujący szablon i zadania podrzędne służą do synchronizowania umów dotyczących projektu i projektów z rozwiązania Project Service Automation do rozwiązania Finance:</span><span class="sxs-lookup"><span data-stu-id="226bd-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="226bd-115">Integrowanie z Dynamics 365 Project Service Automation v2. x</span><span class="sxs-lookup"><span data-stu-id="226bd-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="226bd-116">**Nazwa szablonu w narzędziu Integracja danych:** Projekty i umowy (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="226bd-116">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="226bd-117">**Nazwa zadania w projekcie:**</span><span class="sxs-lookup"><span data-stu-id="226bd-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="226bd-118">Umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-118">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-119">Projekty z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-119">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-120">Wiersze umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-120">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-121">Punkty kontrolne wiersza umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-121">Project contract line milestones PSA to Fin and Ops</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="226bd-122">Integrowanie z Dynamics 365 Project Service Automation v3. x</span><span class="sxs-lookup"><span data-stu-id="226bd-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="226bd-123">Istnieje zmiana schematu Project Service Automation, która ma wpływ na szablon punktów kontrolnych wiersza umowy dotyczącej projektu i jest wymagane użycie wersji v2 szablonu w celu zintegrowania usługi Project Service Automation v3. x z systemem Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="226bd-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="226bd-124">**Nazwa szablonu w narzędziu Integracja danych:** Projekty i umowy (PSA 3.x do Fin and Ops) - v2</span><span class="sxs-lookup"><span data-stu-id="226bd-124">**Name of the template in Data integration:** Projects and Contracts (PSA 3.x to Fin and Ops) - v2</span></span>
- <span data-ttu-id="226bd-125">**Nazwa zadania w projekcie:**</span><span class="sxs-lookup"><span data-stu-id="226bd-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="226bd-126">Umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-126">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-127">Projekty z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-127">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-128">Wiersze umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-128">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="226bd-129">Punkty kontrolne wiersza umowy na projekt z PSA do Fin and Ops</span><span class="sxs-lookup"><span data-stu-id="226bd-129">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="226bd-130">Zanim będzie możliwa synchronizacja umów na projekty i projektów, należy zsynchronizować konta.</span><span class="sxs-lookup"><span data-stu-id="226bd-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="226bd-131">Zestaw jednostek</span><span class="sxs-lookup"><span data-stu-id="226bd-131">Entity set</span></span>

| <span data-ttu-id="226bd-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="226bd-132">Project Service Automation</span></span>       | <span data-ttu-id="226bd-133">Finanse</span><span class="sxs-lookup"><span data-stu-id="226bd-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="226bd-134">Zamówienia</span><span class="sxs-lookup"><span data-stu-id="226bd-134">Orders</span></span>                           | <span data-ttu-id="226bd-135">Jednostka integracji umowy projektu</span><span class="sxs-lookup"><span data-stu-id="226bd-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="226bd-136">Projekty</span><span class="sxs-lookup"><span data-stu-id="226bd-136">Projects</span></span>                         | <span data-ttu-id="226bd-137">Jednostka integracji dla projektu</span><span class="sxs-lookup"><span data-stu-id="226bd-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="226bd-138">Wiersze zamówienia</span><span class="sxs-lookup"><span data-stu-id="226bd-138">Order lines</span></span>                      | <span data-ttu-id="226bd-139">Jednostka integracji wiersza umowy projektu</span><span class="sxs-lookup"><span data-stu-id="226bd-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="226bd-140">Punkty kontrolne wiersza umowy na projekt</span><span class="sxs-lookup"><span data-stu-id="226bd-140">Project contract line milestones</span></span> | <span data-ttu-id="226bd-141">Jednostka integracji punktu kontrolnego wiersza umowy projektu</span><span class="sxs-lookup"><span data-stu-id="226bd-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="226bd-142">Przepływ jednostek</span><span class="sxs-lookup"><span data-stu-id="226bd-142">Entity flow</span></span>

<span data-ttu-id="226bd-143">Zarządzanie umowami na projekt odbywa się w aplikacji Project Service Automation i są one synchronizowane z programem Finance jako umowy na projekt.</span><span class="sxs-lookup"><span data-stu-id="226bd-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="226bd-144">W szablonie integracji można ustawić źródło integracji w programie Finance dla umowy na projekt.</span><span class="sxs-lookup"><span data-stu-id="226bd-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="226bd-145">Zarządzanie projektami rozliczanymi według czasu i materiałów oraz projektami ze stała ceną odbywa się w aplikacji Project Service Automation. Projekty te są synchronizowane z aplikacją Finance jako projekty.</span><span class="sxs-lookup"><span data-stu-id="226bd-145">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance as projects.</span></span> <span data-ttu-id="226bd-146">W szablonie integracji można ustawić źródło integracji w programie Finance na projekt.</span><span class="sxs-lookup"><span data-stu-id="226bd-146">As part of the template integration, you can set the integration source in Finance for the project.</span></span>

<span data-ttu-id="226bd-147">Zarządzanie wierszami umowy na projekt odbywa się w aplikacji Project Service Automation i są one synchronizowane z programem Finance jako reguły fakturowania umowy na projekt.</span><span class="sxs-lookup"><span data-stu-id="226bd-147">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="226bd-148">Jeśli metoda fakturowania różni się od domyślnej dla typu projektu, synchronizacja spowoduje zaktualizowanie typu projektu dla projektu w wierszu umowy i grupy projektów.</span><span class="sxs-lookup"><span data-stu-id="226bd-148">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="226bd-149">Zarządzanie punktami kontrolnymi wiersza umowy na projekt odbywa się w aplikacji Project Service Automation i są one synchronizowane z programem Finance jako punkty kontrolne reguł fakturowania umowy na projekt.</span><span class="sxs-lookup"><span data-stu-id="226bd-149">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="226bd-150">Rozwiązanie do integrowania aplikacji Project Service Automation z Finance</span><span class="sxs-lookup"><span data-stu-id="226bd-150">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="226bd-151">Pole **Identyfikator umowy dotyczącej projektu** jest dostępne na stronie **Umowy dotyczące projektu**.</span><span class="sxs-lookup"><span data-stu-id="226bd-151">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="226bd-152">To pole pełni rolę naturalnego i unikatowego klucza wspierającego integrację.</span><span class="sxs-lookup"><span data-stu-id="226bd-152">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="226bd-153">Jeśli podczas tworzenia nowej umowy projektu wartość **Identyfikator kontraktu projektu** jeszcze nie istnieje, jest ona generowana automatycznie przy użyciu numeracji.</span><span class="sxs-lookup"><span data-stu-id="226bd-153">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="226bd-154">Wartość składa się z prefiksu **ORD**, po którym następuje zwiększona kolejna liczba, a następnie sześcioznakowy sufiks.</span><span class="sxs-lookup"><span data-stu-id="226bd-154">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="226bd-155">Oto przykład: **ORD-01022-Z4M9Q0**.</span><span class="sxs-lookup"><span data-stu-id="226bd-155">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="226bd-156">Pole **Numeru projektu** jest dostępne na stronie **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="226bd-156">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="226bd-157">To pole pełni rolę naturalnego i unikatowego klucza wspierającego integrację.</span><span class="sxs-lookup"><span data-stu-id="226bd-157">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="226bd-158">Jeśli podczas tworzenia nowego projektu wartość **Numer projektu** jeszcze nie istnieje, jest generowana automatycznie przy użyciu numeracji.</span><span class="sxs-lookup"><span data-stu-id="226bd-158">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="226bd-159">Wartość składa się z prefiksu **PRJ**, po którym następuje zwiększona kolejna liczba, a następnie sześcioznakowy sufiks.</span><span class="sxs-lookup"><span data-stu-id="226bd-159">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="226bd-160">Oto przykład: **PRJ-01049-CCNID0**.</span><span class="sxs-lookup"><span data-stu-id="226bd-160">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="226bd-161">Gdy używane są rozwiązania integracji aplikacji Project Service Automation, skrypt uaktualniania ustawia pole **Identyfikator umowy projektu** dla istniejących umów projektów i pole **Numer projektu** dla istniejących projektów w aplikacji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="226bd-161">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="226bd-162">Wymagania wstępne i ustawienia mapowania</span><span class="sxs-lookup"><span data-stu-id="226bd-162">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="226bd-163">Zanim będzie możliwa synchronizacja umów na projekty i projektów, należy zsynchronizować konta.</span><span class="sxs-lookup"><span data-stu-id="226bd-163">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="226bd-164">W zestawie połączeń dodaj mapowanie pola klucza integracji **msdyn\_organizationalunits** do elementu **msdyn\_name \[nazwa\]**.</span><span class="sxs-lookup"><span data-stu-id="226bd-164">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="226bd-165">Najpierw trzeba będzie dodać projekt do zestawu połączenia.</span><span class="sxs-lookup"><span data-stu-id="226bd-165">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="226bd-166">Aby uzyskać więcej informacji, zobacz [Integrowanie danych na platformie Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="226bd-166">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="226bd-167">W zestawie połączeń dodaj mapowanie pola klucza integracji z **msdyn\_projects** do elementu **msdynce\_projectnumber \[numer projektu\]**.</span><span class="sxs-lookup"><span data-stu-id="226bd-167">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="226bd-168">Najpierw trzeba będzie dodać projekt do zestawu połączenia.</span><span class="sxs-lookup"><span data-stu-id="226bd-168">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="226bd-169">Aby uzyskać więcej informacji, zobacz [Integrowanie danych na platformie Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="226bd-169">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="226bd-170">Pole **SourceDataID** umów na projekty i projektów można zaktualizować na inną wartość lub usunąć z mapowania.</span><span class="sxs-lookup"><span data-stu-id="226bd-170">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="226bd-171">Domyślną wartością szablonu jest **Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="226bd-171">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="226bd-172">Mapowanie **PaymentTerms** należy zaktualizować, tak aby odzwierciedlało prawidłowe warunki płatności w aplikacji Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-172">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="226bd-173">Można również usunąć mapowanie z zadania projektu.</span><span class="sxs-lookup"><span data-stu-id="226bd-173">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="226bd-174">Mapa wartości domyślnych zawiera wartości domyślne dla danych demonstracyjnych.</span><span class="sxs-lookup"><span data-stu-id="226bd-174">The default value map has default values for demo data.</span></span> <span data-ttu-id="226bd-175">W poniższej tabeli przedstawiono wartości w rozwiązaniu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="226bd-175">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="226bd-176">Wartość</span><span class="sxs-lookup"><span data-stu-id="226bd-176">Value</span></span> | <span data-ttu-id="226bd-177">opis</span><span class="sxs-lookup"><span data-stu-id="226bd-177">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="226bd-178">1</span><span class="sxs-lookup"><span data-stu-id="226bd-178">1</span></span>     | <span data-ttu-id="226bd-179">Netto 30</span><span class="sxs-lookup"><span data-stu-id="226bd-179">Net 30</span></span>        |
    | <span data-ttu-id="226bd-180">2</span><span class="sxs-lookup"><span data-stu-id="226bd-180">2</span></span>     | <span data-ttu-id="226bd-181">2% 10, netto 30</span><span class="sxs-lookup"><span data-stu-id="226bd-181">2% 10, Net 30</span></span> |
    | <span data-ttu-id="226bd-182">3</span><span class="sxs-lookup"><span data-stu-id="226bd-182">3</span></span>     | <span data-ttu-id="226bd-183">Netto 45</span><span class="sxs-lookup"><span data-stu-id="226bd-183">Net 45</span></span>        |
    | <span data-ttu-id="226bd-184">4</span><span class="sxs-lookup"><span data-stu-id="226bd-184">4</span></span>     | <span data-ttu-id="226bd-185">Netto 60</span><span class="sxs-lookup"><span data-stu-id="226bd-185">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="226bd-186">Zapytanie zaawansowane</span><span class="sxs-lookup"><span data-stu-id="226bd-186">Power Query</span></span>

<span data-ttu-id="226bd-187">Należy użyć dodatku Microsoft Power Query dla programu Excel do odfiltrowania danych, jeśli są spełnione następujące warunki:</span><span class="sxs-lookup"><span data-stu-id="226bd-187">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="226bd-188">Masz zamówienia sprzedaży w Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="226bd-188">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="226bd-189">Istnieje wiele jednostek organizacyjnych w rozwiązaniu Project Service Automation. Jednostki te zostaną zmapowane do wielu podmiotów prawnych w rozwiązaniu Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-189">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="226bd-190">Jeśli musisz używać narzędzia Power Query, przestrzegaj następujących wytycznych:</span><span class="sxs-lookup"><span data-stu-id="226bd-190">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="226bd-191">Szablon Projekty i umowy (PSA do Fin and Ops) zawiera domyślny filtr obejmujący wyłącznie zamówienia sprzedaży typu **Element roboczy (msdyn\_ordertype = 192350001)**.</span><span class="sxs-lookup"><span data-stu-id="226bd-191">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="226bd-192">Ten filtr gwarantuje, że umowy dotyczące projektów są tworzone dla zamówień sprzedaży w programie Finance.</span><span class="sxs-lookup"><span data-stu-id="226bd-192">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="226bd-193">Jeśli tworzysz własny szablon, musisz dodać ten filtr.</span><span class="sxs-lookup"><span data-stu-id="226bd-193">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="226bd-194">Należy utworzyć filtr do narzędzia Power Query uwzględniający tylko organizacje umowy, które mają być synchronizowane z firmą integrującą zestaw połączenia.</span><span class="sxs-lookup"><span data-stu-id="226bd-194">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="226bd-195">Na przykład umowy na projekty, które masz zawarte z jednostką organizacyjną Contoso US, powinny być synchronizowane z firmą USSI, ale umowy na projekty zawarte z jednostką organizacyjną Contoso Global mają być synchronizowane z firmą USMF.</span><span class="sxs-lookup"><span data-stu-id="226bd-195">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="226bd-196">Jeśli nie dodasz tego filtra do swojego mapowania zadań, wszystkie umowy na projekty będą synchronizowane z firmą zdefiniowaną dla zestawu połączeń, bez względu na jednostkę organizacyjną umowy.</span><span class="sxs-lookup"><span data-stu-id="226bd-196">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="226bd-197">Mapowanie szablonu w integracji danych</span><span class="sxs-lookup"><span data-stu-id="226bd-197">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="226bd-198">Pola **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** i **AddressZipCode** nie są uwzględnione w domyślnym mapowaniu dla umów na projekty.</span><span class="sxs-lookup"><span data-stu-id="226bd-198">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="226bd-199">Jeśli trzeba zsynchronizować te dane dla umów dotyczących projektów, możesz dodać mapowania.</span><span class="sxs-lookup"><span data-stu-id="226bd-199">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="226bd-200">Pola **Opis**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** i **ProjectType** nie są uwzględnione w domyślnym mapowaniu dla projektów.</span><span class="sxs-lookup"><span data-stu-id="226bd-200">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="226bd-201">Jeśli trzeba zsynchronizować te dane dla projektów, możesz dodać mapowania.</span><span class="sxs-lookup"><span data-stu-id="226bd-201">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="226bd-202">Poniższa ilustracja przedstawia przykłady mapowań zadań szablonu w integracji danych.</span><span class="sxs-lookup"><span data-stu-id="226bd-202">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="226bd-203">Mapowanie pokazuje informacje z pola, które zostanie zsynchronizowane z rozwiązania Finance do rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="226bd-203">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="226bd-204">[![Mapowanie szablonu](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="226bd-204">[![Template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="226bd-205">[![Mapowanie szablonu](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="226bd-205">[![Template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="226bd-206">[![Mapowanie szablonu](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="226bd-206">[![Template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="226bd-207">[![Mapowanie szablonu](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="226bd-207">[![Template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="226bd-208">Mapowanie punktów kontrolnych wiersza umowy projektu w szablonie projekty i kontrakty (PSA 3. x to Dynamics)-v2:</span><span class="sxs-lookup"><span data-stu-id="226bd-208">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="226bd-209">[![Mapowanie szablonu](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="226bd-209">[![Template mapping](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>