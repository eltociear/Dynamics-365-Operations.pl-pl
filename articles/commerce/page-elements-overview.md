---
title: Słownik terminów dotyczących modelu strony
description: W tym temacie opisano różne elementy, które są używane na stronach witryny Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c7b79e8b3bd68ba6246fe24916c60f476a26605
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697964"
---
# <a name="page-model-glossary"></a><span data-ttu-id="840b4-103">Słownik terminów dotyczących modelu strony</span><span class="sxs-lookup"><span data-stu-id="840b4-103">Page model glossary</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="840b4-104">W tym temacie opisano różne elementy, które są używane na stronach witryny Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="840b4-104">This topic describes the various elements that are used on the pages of a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="page-element-definitions"></a><span data-ttu-id="840b4-105">Definicje elementów strony</span><span class="sxs-lookup"><span data-stu-id="840b4-105">Page element definitions</span></span>

<span data-ttu-id="840b4-106">Poniższa tabela przedstawia podsumowanie pojęć, które powinny być znane, gdy zmieniasz wygląd, działanie i zawartość witryny.</span><span class="sxs-lookup"><span data-stu-id="840b4-106">The following table provides a summary of terms that you should be familiar with when you change the look, feel, and content of your site.</span></span> <span data-ttu-id="840b4-107">Aby uzyskać dokładniejsze wyjaśnienia i procedury, należy skorzystać z łączy.</span><span class="sxs-lookup"><span data-stu-id="840b4-107">For more thorough explanations and procedures, follow the links.</span></span>

| <span data-ttu-id="840b4-108">Okres</span><span class="sxs-lookup"><span data-stu-id="840b4-108">Term</span></span> | <span data-ttu-id="840b4-109">Opis i uwagi</span><span class="sxs-lookup"><span data-stu-id="840b4-109">Description and notes</span></span> |
|------|-----------------------|
| [<span data-ttu-id="840b4-110">Moduł</span><span class="sxs-lookup"><span data-stu-id="840b4-110">Module</span></span>](work-with-modules.md) | <p><span data-ttu-id="840b4-111">**Definicja:** moduły są blokami konstrukcyjnymi, które mogą być tworzone i tworzą szkielet strony sieci Web.</span><span class="sxs-lookup"><span data-stu-id="840b4-111">**Definition:** Modules are building block that can be authored and make up the skeleton of a webpage.</span></span> <span data-ttu-id="840b4-112">Przykładem mogą być moduły nagłóweka, bohatera i karuzela.</span><span class="sxs-lookup"><span data-stu-id="840b4-112">Examples include header, hero, and carousel modules.</span></span></p><p><span data-ttu-id="840b4-113">**Gdzie jest wybrana opcja:** wdrożone moduły można wybierać i konfigurować na różnych etapach przepływu pracy tworzenia witryn, takich jak szablon, układ, strona i etapy tworzenia fragmentów.</span><span class="sxs-lookup"><span data-stu-id="840b4-113">**Where it's selected:** Deployed modules can be selected and configured in various stages of the site authoring workflow, such as the template, layout, page, and fragment authoring stages.</span></span></p><p><span data-ttu-id="840b4-114">**Gdzie jest edytowany:** moduły niestandardowe są tworzone w kodzie przy użyciu zestawu Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="840b4-114">**Where it's edited:** Custom modules are created in code by using the software development kit (SDK).</span></span> <span data-ttu-id="840b4-115">Następnie są one przekazywane do witryny, gdzie będą dostępne do wybrania.</span><span class="sxs-lookup"><span data-stu-id="840b4-115">They are then uploaded to your site, where they become available for selection.</span></span></p> |
| <span data-ttu-id="840b4-116">Właściwość modułu</span><span class="sxs-lookup"><span data-stu-id="840b4-116">Module property</span></span> | <p><span data-ttu-id="840b4-117">**Definicja:** właściwości modułu są określonymi ustawieniami zdefiniowanymi przez moduł.</span><span class="sxs-lookup"><span data-stu-id="840b4-117">**Definition:** Module properties are specific settings that are defined by the module.</span></span> <span data-ttu-id="840b4-118">Można je edytować w narzędziach autorskich e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="840b4-118">They can be edited in the e-Commerce authoring tools.</span></span> <span data-ttu-id="840b4-119">Na przykład właściwości modułu służą do ustawiania nagłówka i obrazu tła w module banera.</span><span class="sxs-lookup"><span data-stu-id="840b4-119">For example, module properties are used to set the heading and background image of a banner module.</span></span></p><p><span data-ttu-id="840b4-120">**Gdzie jest skonfigurowany:** wybrano i skonfigurowano właściwości modułu w okienku właściwości, które pojawia się w środowiskach autorskich (edytorach) dla szablonów, układów, stron, fragmentów i ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="840b4-120">**Where it's configured:** Module properties are selected and configured in the property pane that appears in the authoring environments (editors) for templates, layouts, pages, fragments, and app settings.</span></span></p> |
| [<span data-ttu-id="840b4-121">Szablon</span><span class="sxs-lookup"><span data-stu-id="840b4-121">Template</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="840b4-122">**Definicja:** szablony definiują kombinacje i opcje modułu, które powinny być używane dla kategorii stron (np. stron marketingowych, stron kategorii i stron produktów).</span><span class="sxs-lookup"><span data-stu-id="840b4-122">**Definition:** Templates define the module combinations and options that should be used for a category of pages (for example, marketing pages, category pages, and product pages).</span></span></p><p><span data-ttu-id="840b4-123">**Gdzie jest wybrany:** szablony można wybierać podczas tworzenia strony lub układu przepływów pracy.</span><span class="sxs-lookup"><span data-stu-id="840b4-123">**Where it's selected:** Templates can be selected during page or layout creation workflows.</span></span></p><p><span data-ttu-id="840b4-124">**Gdzie jest edytowany:** szablony są tworzone w edytorze szablonów.</span><span class="sxs-lookup"><span data-stu-id="840b4-124">**Where it's edited:** Templates are authored in the template editor.</span></span> <span data-ttu-id="840b4-125">Do utworzenia lub zmodyfikowania nie jest wymagany żaden kod.</span><span class="sxs-lookup"><span data-stu-id="840b4-125">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="840b4-126">Układ</span><span class="sxs-lookup"><span data-stu-id="840b4-126">Layout</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="840b4-127">**Definicja:** układy definiują ostateczne wybór i układ modułów na podstawie zbioru opcji szablonu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="840b4-127">**Definition:** Layouts define the final selection and arrangement of modules from the parent template's set of options.</span></span> <span data-ttu-id="840b4-128">Układ może być konfigurowany dla pojedynczej strony (*układ niestandardowy*) lub może być współużytkowany przez wiele stron (*układ predefiniowany*).</span><span class="sxs-lookup"><span data-stu-id="840b4-128">A layout can be configured for a single page (*custom layout*), or it can be shared by multiple pages (*preset layout*).</span></span></p><p><span data-ttu-id="840b4-129">**Gdzie jest zaznaczone:** układy można wybierać podczas tworzenia nowej strony lub gdy dla istniejącej strony wymagany jest inny układ.</span><span class="sxs-lookup"><span data-stu-id="840b4-129">**Where it's selected:** Layouts can be selected during new page creation or when a different layout is required for an existing page.</span></span></p><p><span data-ttu-id="840b4-130">**Gdzie jest edytowany:** układy są tworzone w edytorze układu.</span><span class="sxs-lookup"><span data-stu-id="840b4-130">**Where it's edited:** Layouts are authored in the layout editor.</span></span> <span data-ttu-id="840b4-131">Do utworzenia lub zmodyfikowania nie jest wymagany żaden kod.</span><span class="sxs-lookup"><span data-stu-id="840b4-131">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="840b4-132">Wystąpienie strony</span><span class="sxs-lookup"><span data-stu-id="840b4-132">Page instance</span></span> | <p><span data-ttu-id="840b4-133">**Definicja:** wystąpienia strony definiują ostateczną zawartość poddaną stronie dla pojedynczej strony.</span><span class="sxs-lookup"><span data-stu-id="840b4-133">**Definition:** Page instances define the final, page-specific localized content for a single page.</span></span> <span data-ttu-id="840b4-134">Ta zawartość pochodzi od wartości właściwości modułu.</span><span class="sxs-lookup"><span data-stu-id="840b4-134">This content is derived from the values of module properties.</span></span></p><p><span data-ttu-id="840b4-135">**Gdzie jest on wybrany:** wybierane są strony, gdy są przypisane adresy URL.</span><span class="sxs-lookup"><span data-stu-id="840b4-135">**Where it's selected:** Pages are selected when URLs are assigned.</span></span></p><p><span data-ttu-id="840b4-136">**Gdzie jest edytowany:** strony są edytowane w edytorze strony.</span><span class="sxs-lookup"><span data-stu-id="840b4-136">**Where it's edited:** Pages are edited in the page editor.</span></span> <span data-ttu-id="840b4-137">Do utworzenia lub zmodyfikowania nie jest wymagany żaden kod.</span><span class="sxs-lookup"><span data-stu-id="840b4-137">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="840b4-138">Motyw</span><span class="sxs-lookup"><span data-stu-id="840b4-138">Theme</span></span>](select-site-theme.md) | <p><span data-ttu-id="840b4-139">**Definicja:** motywy definiują arkusz stylów kaskadowych (CSS) i określają wygląd i działanie modułów renderowanych na stronie.</span><span class="sxs-lookup"><span data-stu-id="840b4-139">**Definition:** Themes define the Cascading Style Sheet (CSS), and determine the look and feel of the modules that are rendered on a page.</span></span></p><p><span data-ttu-id="840b4-140">**Gdzie jest wybrana opcja:** po przekazaniu motywu do witryny za pomocą Microsoft Dynamics Lifecycle Services (usługi LCS) można go wybrać jako właściwość modułu kontenera stron.</span><span class="sxs-lookup"><span data-stu-id="840b4-140">**Where it's selected:** After a theme is uploaded to your site by using Microsoft Dynamics Lifecycle Services (LCS), it can be selected as a property of the page container module.</span></span></p><p><span data-ttu-id="840b4-141">**Gdzie jest edytowany:** motywy są obecnie tworzone i edytowane przy użyciu zestawu SDK.</span><span class="sxs-lookup"><span data-stu-id="840b4-141">**Where it's edited:** Themes are currently created and edited by using the SDK.</span></span> <span data-ttu-id="840b4-142">Następnie są przekazywane do witryny za pomocą usługi LCS.</span><span class="sxs-lookup"><span data-stu-id="840b4-142">They are then uploaded to your site by using LCS.</span></span></p> |
| [<span data-ttu-id="840b4-143">Fragment</span><span class="sxs-lookup"><span data-stu-id="840b4-143">Fragment</span></span>](work-with-fragments.md) | <p><span data-ttu-id="840b4-144">**Definicja:** fragmenty są w pełni skonfigurowane moduły z zlokalizowaną zawartością, która może być ponownie używana i centralnie aktualizowana na wielu stronach.</span><span class="sxs-lookup"><span data-stu-id="840b4-144">**Definition:** Fragments are fully configured modules that have localized content that can be reused and centrally updated across multiple pages.</span></span> <span data-ttu-id="840b4-145">Na przykład fragment utworzony z poziomu nagłówka może być używany we wszystkich szablonach i na wszystkich stronach w witrynie, a następnie domyślnie aktualizowany w jednym miejscu.</span><span class="sxs-lookup"><span data-stu-id="840b4-145">For example, a fragment that is created from a header module can be used in all templates and on all pages across your site, and centrally updated in one place.</span></span></p><p><span data-ttu-id="840b4-146">**Gdzie jest wybrana opcja:** fragmenty można wybierać wszędzie, gdzie można wybierać moduły.</span><span class="sxs-lookup"><span data-stu-id="840b4-146">**Where it's selected:** Fragments can be selected wherever modules can be selected.</span></span> <span data-ttu-id="840b4-147">Można je zastąpić modułem, ułatwiając w ten sposób zwiększenie efektywności dzięki możliwości wielokrotnego wykorzystania i scentralizowanego tworzenia.</span><span class="sxs-lookup"><span data-stu-id="840b4-147">They can be substituted for a module to help increase efficiency through reusable and centralized authoring.</span></span></p><p><span data-ttu-id="840b4-148">**Gdzie jest edytowany:** fragmenty są edytowane w edytorze fragmentów.</span><span class="sxs-lookup"><span data-stu-id="840b4-148">**Where it's edited:** Fragments are edited in the fragment editor.</span></span> <span data-ttu-id="840b4-149">Do utworzenia lub zmodyfikowania nie jest wymagany żaden kod.</span><span class="sxs-lookup"><span data-stu-id="840b4-149">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="840b4-150">Adres URL</span><span class="sxs-lookup"><span data-stu-id="840b4-150">URL</span></span> | <p><span data-ttu-id="840b4-151">**Definicja:** adresy URL (Uniform Resource Locator) są adresami wskazującymi strony sieci Web lub inne adresy URL.</span><span class="sxs-lookup"><span data-stu-id="840b4-151">**Definition:** Uniform resource locators (URLs) are addresses that point to webpages or other URLs.</span></span></p><p><span data-ttu-id="840b4-152">**Gdzie jest on wybrany:** adresy URL są wybierane wszędzie tam, gdzie wymagane są linki między stronami.</span><span class="sxs-lookup"><span data-stu-id="840b4-152">**Where it's selected:** URLs are selected wherever links between pages are required.</span></span></p><p><span data-ttu-id="840b4-153">**Gdzie jest edytowany:** adresy URL są edytowane w edytorze URL.</span><span class="sxs-lookup"><span data-stu-id="840b4-153">**Where it's edited:** URLs are edited in the URL editor.</span></span> <span data-ttu-id="840b4-154">Do utworzenia lub zmodyfikowania nie jest wymagany żaden kod.</span><span class="sxs-lookup"><span data-stu-id="840b4-154">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="840b4-155">Składnik majątku</span><span class="sxs-lookup"><span data-stu-id="840b4-155">Asset</span></span> | <p><span data-ttu-id="840b4-156">**Definicja:** zasoby to pliki binarne, które mają rozszerzenie takie jak .jpg, .docx, .pdf lub .mpg.</span><span class="sxs-lookup"><span data-stu-id="840b4-156">**Definition:** Assets are file binaries that have an extension such as .jpg, .docx, .pdf, or .mpg.</span></span></p><p><span data-ttu-id="840b4-157">**Gdzie jest wybrana opcja:** zasoby są wybierane jako właściwości modułu dla modułów, które tego wymagają.</span><span class="sxs-lookup"><span data-stu-id="840b4-157">**Where it's selected:** Assets are selected as module properties for modules that require them.</span></span></p><p><span data-ttu-id="840b4-158">**Gdzie jest edytowany:** zasoby są przekazywane, a skojarzone z nimi metadane są edytowane w menedżerze zasobów.</span><span class="sxs-lookup"><span data-stu-id="840b4-158">**Where it's edited:** Assets are uploaded, and associated metadata is edited in the asset manager.</span></span></p> |

## <a name="additional-resources"></a><span data-ttu-id="840b4-159">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="840b4-159">Additional resources</span></span>

[<span data-ttu-id="840b4-160">Sposoby dodawania zawartości</span><span class="sxs-lookup"><span data-stu-id="840b4-160">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="840b4-161">Dokumentowanie stanów i cyklów życia</span><span class="sxs-lookup"><span data-stu-id="840b4-161">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="840b4-162">Praca z modułami</span><span class="sxs-lookup"><span data-stu-id="840b4-162">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="840b4-163">Praca z fragmentami</span><span class="sxs-lookup"><span data-stu-id="840b4-163">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="840b4-164">Omówienie szablonów i układów</span><span class="sxs-lookup"><span data-stu-id="840b4-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="840b4-165">Dostosowywanie nawigacji w witrynie</span><span class="sxs-lookup"><span data-stu-id="840b4-165">Customize site navigation</span></span>](customize-site-navigation.md)