---
title: Klucze konfiguracji a jednostki danych
description: W tym temacie opisano relację między kluczami konfiguracji i jednostkami danych.
author: Sunil-Garg
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b951c1da298689ea82f8c0abb868bea7c8c22487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182078"
---
# <a name="configuration-keys-and-data-entities"></a><span data-ttu-id="c78e5-103">Klucze konfiguracji i jednostki danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-103">Configuration keys and data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c78e5-104">Zanim zaczniesz używać jednostek danych do importowania lub eksportowania danych, zalecamy ustalenie wpływu kluczy konfiguracji na jednostki danych, których zamierzasz używać.</span><span class="sxs-lookup"><span data-stu-id="c78e5-104">Before you use data entities to import or export data, we recommended that you first determine the impact of configuration keys on the data entities that you are planning to use.</span></span>

<span data-ttu-id="c78e5-105">Aby dowiedzieć się więcej o kluczach konfiguracji, zobacz [Raport kodów licencji i kluczy konfiguracji](../sysadmin/license-codes-configuration-keys-report.md).</span><span class="sxs-lookup"><span data-stu-id="c78e5-105">To learn more about configuration keys, see the [License codes and configuration keys report](../sysadmin/license-codes-configuration-keys-report.md).</span></span>

### <a name="configuration-key-assignments"></a><span data-ttu-id="c78e5-106">Przypisania kluczy konfiguracji</span><span class="sxs-lookup"><span data-stu-id="c78e5-106">Configuration key assignments</span></span>
<span data-ttu-id="c78e5-107">Klucze konfiguracji można przypisywać do jednego lub wszystkich poniższych artefaktów.</span><span class="sxs-lookup"><span data-stu-id="c78e5-107">Configuration keys can be assigned to one or all of the following artifacts.</span></span>

- <span data-ttu-id="c78e5-108">Jednostki danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-108">Data entities</span></span>
- <span data-ttu-id="c78e5-109">Tabele używane jako źródła danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-109">Tables used as data sources</span></span>
- <span data-ttu-id="c78e5-110">Pola tabeli</span><span class="sxs-lookup"><span data-stu-id="c78e5-110">Table fields</span></span>
- <span data-ttu-id="c78e5-111">Pola jednostki danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-111">Data entity fields</span></span>

<span data-ttu-id="c78e5-112">W tabeli poniżej podsumowano, jak wartości kluczy konfiguracji w różnych artefaktach stanowiących bazę obiektu zmieniają oczekiwane zachowanie obiektu.</span><span class="sxs-lookup"><span data-stu-id="c78e5-112">The following table summarizes how configuration key values on the different artifacts that underlie an object change the expected behavior of the object.</span></span>

| <span data-ttu-id="c78e5-113">Ustawienie klucza konfiguracji w jednostce danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-113">Configuration key setting on data entity</span></span> | <span data-ttu-id="c78e5-114">Ustawienie klucza konfiguracji w tabeli</span><span class="sxs-lookup"><span data-stu-id="c78e5-114">Configuration key setting on table</span></span> | <span data-ttu-id="c78e5-115">Ustawienie klucza konfiguracji w polu tabeli</span><span class="sxs-lookup"><span data-stu-id="c78e5-115">Configuration key setting on table field</span></span> | <span data-ttu-id="c78e5-116">Klucz konfiguracji w polu jednostki danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-116">Configuration key on data entity field</span></span> | <span data-ttu-id="c78e5-117">Oczekiwane zachowanie</span><span class="sxs-lookup"><span data-stu-id="c78e5-117">Expected behavior</span></span> |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| <span data-ttu-id="c78e5-118">Wyłączony</span><span class="sxs-lookup"><span data-stu-id="c78e5-118">Disabled</span></span>                                | <span data-ttu-id="c78e5-119">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-119">Not evaluated</span></span>                      | <span data-ttu-id="c78e5-120">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-120">Not evaluated</span></span>                            | <span data-ttu-id="c78e5-121">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-121">Not evaluated</span></span>                          | <span data-ttu-id="c78e5-122">Jeśli klucz konfiguracji jednostki danych jest wyłączony, jednostka danych nie będzie działać.</span><span class="sxs-lookup"><span data-stu-id="c78e5-122">If the configuration key for the data entity is disabled, the data entity will not be functional.</span></span> <span data-ttu-id="c78e5-123">Nie ma znaczenia, czy klucze konfiguracji w źródłowych tabelach i polach są włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="c78e5-123">It does not matter whether the configuration keys in the underlying tables and fields are enabled or disabled.</span></span> |
| <span data-ttu-id="c78e5-124">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-124">Enabled</span></span>                                 | <span data-ttu-id="c78e5-125">Wyłączony</span><span class="sxs-lookup"><span data-stu-id="c78e5-125">Disabled</span></span>                           | <span data-ttu-id="c78e5-126">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-126">Not evaluated</span></span>                            | <span data-ttu-id="c78e5-127">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-127">Not evaluated</span></span>                          | <span data-ttu-id="c78e5-128">Jeśli klucz konfiguracji jednostki danych jest włączony, struktura zarządzania danymi sprawdza klucz konfiguracji w każdej tabeli źródłowej.</span><span class="sxs-lookup"><span data-stu-id="c78e5-128">If the configuration key for a data entity is enabled, the data management framework checks the configuration key on each of the underlying tables.</span></span> <span data-ttu-id="c78e5-129">Jeśli klucz konfiguracji tabeli jest wyłączony, tabela nie będzie dostępna do użytku w jednostce danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-129">If the configuration key for a table is disabled, that table will not be available in the data entity for functional use.</span></span> <span data-ttu-id="c78e5-130">Jeśli klucz konfiguracji tabeli jest wyłączony, ustawienia kluczy konfiguracji tabeli i jednostki danych nie są oceniane.</span><span class="sxs-lookup"><span data-stu-id="c78e5-130">If a table's configuration key is disabled, the table and data entity configuration key settings are not evaluated.</span></span> <span data-ttu-id="c78e5-131">Jeżeli tabela podstawowa w jednostce ma wyłączony klucz konfiguracji, system będzie działał tak, jakby został wyłączony klucz konfiguracji jednostki.</span><span class="sxs-lookup"><span data-stu-id="c78e5-131">If the primary table in the entity has its configuration key disabled, then the system will act as though the entity's configuration key were disabled.</span></span> |
| <span data-ttu-id="c78e5-132">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-132">Enabled</span></span>                                 | <span data-ttu-id="c78e5-133">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-133">Enabled</span></span>                            | <span data-ttu-id="c78e5-134">Wyłączony</span><span class="sxs-lookup"><span data-stu-id="c78e5-134">Disabled</span></span>                                 | <span data-ttu-id="c78e5-135">Nie oceniane</span><span class="sxs-lookup"><span data-stu-id="c78e5-135">Not evaluated</span></span>                          | <span data-ttu-id="c78e5-136">Jeśli włączono klucz konfiguracji w jednostce danych, a są włączone klucze konfiguracji źródłowych tabel, struktura zarządzania danymi będzie sprawdzać klucz konfiguracji w polach w tabelach.</span><span class="sxs-lookup"><span data-stu-id="c78e5-136">If the configuration key for a data entity is enabled, and the underlying tables configuration keys are enabled, the data management framework will check the configuration key on of the fields in the tables.</span></span> <span data-ttu-id="c78e5-137">Jeśli klucz konfiguracji pola jest wyłączony, to pole nie będzie dostępne do użytku w jednostce danych, nawet gdy odnośne pole jednostki danych ma włączony klucz konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="c78e5-137">If the configuration key for a field is disabled, that field will not be available in the data entity for functional use even if the corresponding data entity field has the configuration key enabled.</span></span> |
| <span data-ttu-id="c78e5-138">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-138">Enabled</span></span>                                 | <span data-ttu-id="c78e5-139">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-139">Enabled</span></span>                            | <span data-ttu-id="c78e5-140">Włączone</span><span class="sxs-lookup"><span data-stu-id="c78e5-140">Enabled</span></span>                                  | <span data-ttu-id="c78e5-141">Wyłączony</span><span class="sxs-lookup"><span data-stu-id="c78e5-141">Disabled</span></span>                               | <span data-ttu-id="c78e5-142">Jeśli klucz konfiguracji jest włączony na wszystkich innych poziomach, ale klucz konfiguracji pola jednostki nie jest włączony, to pole nie będzie dostępne do użytku w jednostki danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-142">If the configuration key is enabled at all other levels, but the entity field configuration key is not enabled, then the field will not be available for use in the data entity.</span></span> |

> [!NOTE]
> <span data-ttu-id="c78e5-143">Jeśli jednostka ma inną jednostkę jako źródło danych, powyższa semantyka jest stosowana w sposób cykliczny.</span><span class="sxs-lookup"><span data-stu-id="c78e5-143">If an entity has another entity as a data source then, the above semantics are applied in a recursive manner.</span></span>

### <a name="entity-list-refresh"></a><span data-ttu-id="c78e5-144">Odświeżanie listy jednostek</span><span class="sxs-lookup"><span data-stu-id="c78e5-144">Entity list refresh</span></span>
<span data-ttu-id="c78e5-145">Po odświeżeniu listy jednostek struktura zarządzania danymi tworzy metadane klucza konfiguracji do użytku w czasie wykonywania.</span><span class="sxs-lookup"><span data-stu-id="c78e5-145">When the entity list is refreshed, the data management framework builds the configuration key metadata for runtime use.</span></span> <span data-ttu-id="c78e5-146">Te metadane są generowane przy użyciu logiki opisanej powyżej.</span><span class="sxs-lookup"><span data-stu-id="c78e5-146">This metadata is built using the logic described above.</span></span> <span data-ttu-id="c78e5-147">Stanowczo zalecamy poczekać na zakończenie odświeżania listy jednostek, zanim zaczniesz używać zadań i jednostek strukturze zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="c78e5-147">We strongly recommend that you wait for the entity list refresh to complete before using jobs and entities in the data management framework.</span></span> <span data-ttu-id="c78e5-148">Jeśli nie zaczekasz, metadane kluczy konfiguracji mogą być nieaktualne i w efekcie powodować nieoczekiwane rezultaty.</span><span class="sxs-lookup"><span data-stu-id="c78e5-148">If you don't wait, the configuration key metadata may not be up to date and could result in unexpected outcomes.</span></span> <span data-ttu-id="c78e5-149">Podczas odświeżania listy jednostek jest wyświetlany następujący komunikat na stronie listy jednostek.</span><span class="sxs-lookup"><span data-stu-id="c78e5-149">When the entity list is being refreshed, the following message is shown in the entity list page.</span></span>

![Odświeżanie listy jednostek](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a><span data-ttu-id="c78e5-151">Strona listy jednostek danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-151">Data entity list page</span></span>
<span data-ttu-id="c78e5-152">Strona listy jednostek danych w obszarze roboczym Zarządzanie danymi pokazuje ustawienia kluczy konfiguracji jednostek.</span><span class="sxs-lookup"><span data-stu-id="c78e5-152">The data entity list page in the Data management workspace shows the configuration key settings for the entities.</span></span> <span data-ttu-id="c78e5-153">Rozpoczęcie od tej strony pozwoli zrozumieć wpływ kluczy konfiguracji na jednostkę danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-153">Start from this page to understand the impact from configuration keys on the data entity.</span></span>

<span data-ttu-id="c78e5-154">Te informacje są wyświetlane przy użyciu metadanych wygenerowanych podczas odświeżania jednostki.</span><span class="sxs-lookup"><span data-stu-id="c78e5-154">This information is shown using the metadata that is built during entity refresh.</span></span> <span data-ttu-id="c78e5-155">Kolumna klucza konfiguracji zawiera nazwę klucza konfiguracji skojarzonego z jednostką danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-155">The configuration key column shows the name of the configuration key that is associated with the data entity.</span></span> <span data-ttu-id="c78e5-156">Pusta kolumna oznacza, że nie istnieje klucz konfiguracji skojarzony z jednostką danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-156">If this column is blank it means that there is no configuration key associated with the data entity.</span></span> <span data-ttu-id="c78e5-157">W kolumnie stanu klucza konfiguracji jest pokazywany stan klucza konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="c78e5-157">The configuration key status column shows the state of the configuration key.</span></span> <span data-ttu-id="c78e5-158">Jeśli znajduje się tam znacznik wyboru, oznacza to, że klucz jest włączony.</span><span class="sxs-lookup"><span data-stu-id="c78e5-158">If it has a checkmark, it means the key is enabled.</span></span> <span data-ttu-id="c78e5-159">Puste pole oznacza, że klucz jest wyłączony albo nie ma żadnego skojarzonego klucza.</span><span class="sxs-lookup"><span data-stu-id="c78e5-159">If it is blank, it means either the key is disabled or there is no key associated.</span></span>

![Strona listy jednostek](./media/Data_entity_list_page.png)

### <a name="target-fields"></a><span data-ttu-id="c78e5-161">Pola docelowe</span><span class="sxs-lookup"><span data-stu-id="c78e5-161">Target fields</span></span>
<span data-ttu-id="c78e5-162">Następnym krokiem jest przejście do bardziej szczegółowych poziomów jednostki danych w celu obejrzenia wpływu kluczy konfiguracji na tabele i pola.</span><span class="sxs-lookup"><span data-stu-id="c78e5-162">The next step is to drill into the data entity to view the impact of configuration keys on tables and fields.</span></span> <span data-ttu-id="c78e5-163">Formularz pól docelowych dla jednostki danych zawiera klucz konfiguracji oraz informacje o stanie kluczy w powiązanych tabelach i polach w jednostce danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-163">The target fields form for a data entity shows configuration key and the key status information for the related tables and fields in the data entity.</span></span> <span data-ttu-id="c78e5-164">Jeśli sama jednostka danych ma wyłączony klucz konfiguracji, jest wyświetlany komunikat ostrzegawczy informujący, że tabele i pola w formularzu pól docelowych dla tej jednostki nie będą w ogóle dostępne, niezależnie od stanów ich kluczy konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="c78e5-164">If the data entity itself has its configuration key disabled, a warning message is shown informing that the tables and fields in the target fields form for this entity will not be available at all regardless of their configuration key status.</span></span>

![Pola docelowe](./media/Target_fields_1.png)

### <a name="child-entities"></a><span data-ttu-id="c78e5-166">Jednostki podrzędne</span><span class="sxs-lookup"><span data-stu-id="c78e5-166">Child entities</span></span> 
<span data-ttu-id="c78e5-167">Niektóre jednostki używają innych jednostek jako źródeł danych lub są złożonymi jednostkami danych. Informacje o kluczach konfiguracji takich jednostek są wyświetlane w formularzu Jednostki podrzędne.</span><span class="sxs-lookup"><span data-stu-id="c78e5-167">Certain entities have other entities as data sources, or are composite data entities: configuration key information for these entities is shown in the Child entities form.</span></span> <span data-ttu-id="c78e5-168">Tego formularza używa się w sposób podobny do używania strony listy jednostek opisanej powyżej.</span><span class="sxs-lookup"><span data-stu-id="c78e5-168">Use this form in the similar way to the entities list page described above.</span></span> <span data-ttu-id="c78e5-169">Formularz pól docelowych jednostki podrzędnej również zachowuje się w sposób opisany powyżej.</span><span class="sxs-lookup"><span data-stu-id="c78e5-169">The target fields form for the child entity also behaves like what is described above.</span></span>

![Pola docelowe](./media/Target_fields_2.png)

### <a name="using-data-entities"></a><span data-ttu-id="c78e5-171">Używanie jednostek danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-171">Using data entities</span></span>
<span data-ttu-id="c78e5-172">Po rozpoznaniu całkowitego wpływu kluczy konfiguracji na jednostki danych, których chcesz używać, można rozpocząć korzystanie z jednostek danych, dodając je do projektów danych.</span><span class="sxs-lookup"><span data-stu-id="c78e5-172">After understanding the full impact, if any, of configuration keys on the data entities that you would like to use, you can now proceed to using the data entities by adding them to data projects.</span></span> 

### <a name="run-time-validations-for-configuration-keys"></a><span data-ttu-id="c78e5-173">Sprawdzanie kluczy konfiguracji podczas wykonywania</span><span class="sxs-lookup"><span data-stu-id="c78e5-173">Run time validations for configuration keys</span></span>
<span data-ttu-id="c78e5-174">Sprawdzanie podczas wykonywania jest uruchamiane przy użyciu metadanych kluczy konfiguracji wygenerowanych podczas odświeżania listy jednostek w następujących przypadkach.</span><span class="sxs-lookup"><span data-stu-id="c78e5-174">Using the configuration key metadata built during entity refresh list, run time validations are performed in the following use cases.</span></span>

- <span data-ttu-id="c78e5-175">Podczas dodawania jednostki danych do zadania</span><span class="sxs-lookup"><span data-stu-id="c78e5-175">When a data entity is added to a job</span></span>
- <span data-ttu-id="c78e5-176">Gdy użytkownik klika przycisk „Sprawdź poprawność” na liście jednostek</span><span class="sxs-lookup"><span data-stu-id="c78e5-176">When user clicks 'validate' on the entity list</span></span>
- <span data-ttu-id="c78e5-177">Gdy użytkownik ładuje pakiet danych do projektu danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-177">When the user loads a data package into a data project</span></span>
- <span data-ttu-id="c78e5-178">Gdy użytkownik ładuje szablon do projektu danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-178">When the user loads a template into a data project</span></span>
- <span data-ttu-id="c78e5-179">Podczas ładowania istniejącego projektu danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-179">When an existing data project is loaded</span></span>
- <span data-ttu-id="c78e5-180">Podczas ładowania szablonu do projektu danych</span><span class="sxs-lookup"><span data-stu-id="c78e5-180">When a template is loaded into a data project</span></span>
- <span data-ttu-id="c78e5-181">Przed wykonaniem zadania eksportu/importu (wsadowego, niewsadowego, cyklicznego, przy użyciu protokołu Odata)</span><span class="sxs-lookup"><span data-stu-id="c78e5-181">Before the export/import job is executed (batch, non-batch, recurring, OData)</span></span>
- <span data-ttu-id="c78e5-182">Gdy użytkownik generuje mapowanie</span><span class="sxs-lookup"><span data-stu-id="c78e5-182">When the user generates mapping</span></span>
- <span data-ttu-id="c78e5-183">Gdy użytkownik mapuje pola w interfejsie użytkownika mapowania</span><span class="sxs-lookup"><span data-stu-id="c78e5-183">When the user maps fields in the mapping UI</span></span>
- <span data-ttu-id="c78e5-184">Gdy użytkownik dodaje tylko pola, które można importować</span><span class="sxs-lookup"><span data-stu-id="c78e5-184">When the user adds only 'importable fields'</span></span>

### <a name="managing-configuration-key-changes"></a><span data-ttu-id="c78e5-185">Zarządzanie zmianami w kluczach konfiguracji</span><span class="sxs-lookup"><span data-stu-id="c78e5-185">Managing configuration key changes</span></span>
<span data-ttu-id="c78e5-186">Po każdym zaktualizowaniu kluczy konfiguracji na poziomie jednostki, tabeli lub pola należy odświeżyć listę jednostek w strukturze zarządzania danymi.</span><span class="sxs-lookup"><span data-stu-id="c78e5-186">Anytime that you update configuration keys at the entity, table or field level, the entity list in the data management framework must be refreshed.</span></span> <span data-ttu-id="c78e5-187">Daje to pewność, że struktura pobierze najnowsze ustawienia kluczy konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="c78e5-187">This process ensures that the framework picks up the latest configuration key settings.</span></span> <span data-ttu-id="c78e5-188">Do czasu odświeżenia listy jednostek będzie wyświetlane następujące ostrzeżenie na stronie listy jednostek.</span><span class="sxs-lookup"><span data-stu-id="c78e5-188">Until the entity list is refreshed, the following warning will be shown in the entity list page.</span></span> <span data-ttu-id="c78e5-189">Aktualizacje kluczy konfiguracji zaczną obowiązywać natychmiast po odświeżeniu listy jednostek.</span><span class="sxs-lookup"><span data-stu-id="c78e5-189">The updated configuration key changes will take effect immediately after the entity list is refreshed.</span></span> <span data-ttu-id="c78e5-190">Po wprowadzaniu modyfikacji kluczy konfiguracji zalecamy sprawdzenie poprawności istniejących projektów danych i zadań, aby mieć pewność, że działają zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="c78e5-190">We recommend that you validate existing data projects and jobs to make sure that they function as expected after the configuration keys changes are put in effect.</span></span>

![Pola docelowe](./media/Target_fields_3.png)