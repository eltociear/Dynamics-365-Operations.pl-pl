---
title: Synchronizowanie zadań projektu bezpośrednio z programu Project Service Automation do programu Finance and Operations
description: W tym temacie omówiono szablon i podstawowe zadanie, które są używane do synchronizowania zadań projektu bezpośrednio z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 977037f0e2b313ebf05a3e1616d34567f82e82d7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250399"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1be7a-103">Synchronizowanie zadań projektu bezpośrednio z programu Project Service Automation do programu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1be7a-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1be7a-104">W tym temacie omówiono szablon i podstawowe zadanie, które są używane do synchronizowania zadań projektu bezpośrednio z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1be7a-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1be7a-105">Mechanizmy integracji zadań projektu, kategorii transakcji wydatkowych, szacunków godzin, szacunków wydatków i blokowania funkcji są dostępne w wersji 8.0.</span><span class="sxs-lookup"><span data-stu-id="1be7a-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="1be7a-106">Jeśli używasz Enterprise Edition 7.3.0, po zainstalowaniu aktualizacji KB 4132657 i 4132660 możesz używać szablonów, aby integrować zadania projektu, kategorie transakcji wydatkowych, szacunki godzin, szacunki wydatków i wartości rzeczywiste oraz konfigurować blokowanie funkcji.</span><span class="sxs-lookup"><span data-stu-id="1be7a-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="1be7a-107">Jeśli należy zresetować zasady podziału księgowań, zalecamy dodatkowo zainstalować aktualizację KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="1be7a-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="1be7a-108">Funkcja integrowania wartości rzeczywistych jest dostępna wersji 8.01 i nowszych.</span><span class="sxs-lookup"><span data-stu-id="1be7a-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1be7a-109">Przepływ danych z programu Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="1be7a-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1be7a-110">Rozwiązanie integracji rozwiązania Project Service Automation dp Finance korzysta z funkcji integracji danych do synchronizowania danych między wystąpieniami rozwiązania Project Service Automation oraz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1be7a-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1be7a-111">Szablon integracji, który jest dostępny z funkcji integracji danych, umożliwia przepływ danych dotyczących zadań projektu z rozwiązania Project Service Automation do rozwiązania Finance.</span><span class="sxs-lookup"><span data-stu-id="1be7a-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1be7a-112">Na poniższej ilustracji przedstawiono, w jaki sposób dane są synchronizowane pomiędzy rozwiązaniami Project Service Automation oraz Finance.</span><span class="sxs-lookup"><span data-stu-id="1be7a-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1be7a-113">[![Przepływ danych w integracji programu Project Service Automation z programem Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1be7a-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="1be7a-114">Szablon i zadanie</span><span class="sxs-lookup"><span data-stu-id="1be7a-114">Template and task</span></span>

<span data-ttu-id="1be7a-115">Aby uzyskać dostęp do szablonu, w centrum administracyjnym usługi Microsoft PowerApps wybierz opcję **Projekty** i w prawym górnym rogu wybierz opcję **Nowy projekt**, aby wybrać spośród szablonów publicznych.</span><span class="sxs-lookup"><span data-stu-id="1be7a-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1be7a-116">Następujący szablon i podstawowe zadanie służą do synchronizowania zadań projektu z rozwiązania Project Service Automation do rozwiązania Finance:</span><span class="sxs-lookup"><span data-stu-id="1be7a-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1be7a-117">**Nazwa szablonu w narzędziu Integracja danych:** Zadania w projekcie (PSA do Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1be7a-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1be7a-118">**Nazwa zadania w projekcie:** Zadania w projekcie</span><span class="sxs-lookup"><span data-stu-id="1be7a-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="1be7a-119">Zanim będzie możliwa synchronizacja zadań w projektach, należy zsynchronizować umowy na projekty i projekty.</span><span class="sxs-lookup"><span data-stu-id="1be7a-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="1be7a-120">Zestaw jednostek</span><span class="sxs-lookup"><span data-stu-id="1be7a-120">Entity set</span></span>

| <span data-ttu-id="1be7a-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1be7a-121">Project Service Automation</span></span> | <span data-ttu-id="1be7a-122">Finanse</span><span class="sxs-lookup"><span data-stu-id="1be7a-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="1be7a-123">Zadania w projekcie</span><span class="sxs-lookup"><span data-stu-id="1be7a-123">Project Tasks</span></span>              | <span data-ttu-id="1be7a-124">Jednostka integracji zadania projektu</span><span class="sxs-lookup"><span data-stu-id="1be7a-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="1be7a-125">Przepływ jednostek</span><span class="sxs-lookup"><span data-stu-id="1be7a-125">Entity flow</span></span>

<span data-ttu-id="1be7a-126">Zarządzanie zadaniami w projekcie odbywa się w aplikacji Project Service Automation i są one synchronizowane z programem Finance jako działania w projekcie.</span><span class="sxs-lookup"><span data-stu-id="1be7a-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1be7a-127">Wymagania wstępne i ustawienia mapowania</span><span class="sxs-lookup"><span data-stu-id="1be7a-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="1be7a-128">Zanim będzie możliwa synchronizacja zadań w projektach, należy zsynchronizować umowy na projekty i projekty.</span><span class="sxs-lookup"><span data-stu-id="1be7a-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="1be7a-129">Zapytanie zaawansowane</span><span class="sxs-lookup"><span data-stu-id="1be7a-129">Power Query</span></span>

<span data-ttu-id="1be7a-130">Należy użyć dodatku Microsoft Power Query dla programu Excel do odfiltrowania danych, jeśli jest spełniony następujący warunek:</span><span class="sxs-lookup"><span data-stu-id="1be7a-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="1be7a-131">Masz rekordy przypisane do zasobów w zadaniu w projekcie.</span><span class="sxs-lookup"><span data-stu-id="1be7a-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="1be7a-132">Jeśli musisz używać narzędzia Power Query, przestrzegaj następującej wytycznej:</span><span class="sxs-lookup"><span data-stu-id="1be7a-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="1be7a-133">Szablon Zadania w projekcie (PSA do Fin and Ops) ma domyślny filtr, który wyklucza rekordy określonego zasobu z zadania w projekcie przez ustawienie filtru **IsLineTask** na wartość **False**.</span><span class="sxs-lookup"><span data-stu-id="1be7a-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="1be7a-134">Jeśli tworzysz własny szablon, musisz dodać ten filtr.</span><span class="sxs-lookup"><span data-stu-id="1be7a-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1be7a-135">Mapowanie szablonu w integracji danych</span><span class="sxs-lookup"><span data-stu-id="1be7a-135">Template mapping in Data integration</span></span>

<span data-ttu-id="1be7a-136">Poniższa ilustracja przedstawia przykład mapowań zadań szablonu w integracji danych.</span><span class="sxs-lookup"><span data-stu-id="1be7a-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="1be7a-137">Mapowanie pokazuje informacje z pola, które zostanie zsynchronizowane z rozwiązania Finance do rozwiązania Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1be7a-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1be7a-138">[![Mapowanie szablonu](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="1be7a-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>