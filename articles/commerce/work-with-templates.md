---
title: Praca z szablonami
description: W tym temacie opisano, jak pracować z szablonami w Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: f7f7e2d3dddc35a43adff8d186cf755eba854313
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697734"
---
# <a name="work-with-templates"></a><span data-ttu-id="b0257-103">Praca z szablonami</span><span class="sxs-lookup"><span data-stu-id="b0257-103">Work with templates</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b0257-104">W tym temacie opisano, jak pracować z szablonami w Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0257-104">This topic describes how to work with templates in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b0257-105">Omówienie</span><span class="sxs-lookup"><span data-stu-id="b0257-105">Overview</span></span>

<span data-ttu-id="b0257-106">Zgodnie z tematem [Omówienie szablonów i układów](templates-layouts-overview.md), szablony definiują zbiór opcji dostępnych dla autorów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="b0257-106">As was discussed in [Templates and layouts overview](templates-layouts-overview.md), templates define the set of options that is available to downstream authors.</span></span> <span data-ttu-id="b0257-107">Szablony są przydatne dla zespołu tworzenia sieci Web w przedsiębiorstwie z kilku powodów, a strukturalne dobre szablony mogą pomóc we wszystkich następujących celach:</span><span class="sxs-lookup"><span data-stu-id="b0257-107">Templates are useful to an enterprise's web authoring team for several reasons, and well-structured templates can help with all the following goals:</span></span>

- <span data-ttu-id="b0257-108">Uprość tworzenie treści dzięki codziennym rolom edytora treści.</span><span class="sxs-lookup"><span data-stu-id="b0257-108">Simplify the authoring experience for day-to-day content editor roles.</span></span>

    - <span data-ttu-id="b0257-109">Filtrowanie opcji modułu, tak aby były pokazywane tylko odpowiednie moduły dla konkretnej sekcji strony.</span><span class="sxs-lookup"><span data-stu-id="b0257-109">Filter module options so that only relevant modules are shown for a specific page section.</span></span> <span data-ttu-id="b0257-110">(Na przykład sekcja marketingowa szablonu może być skonfigurowana do odfiltrowywania nieistotnych modułów, których nigdy nie należy używać w tym kontekście, a to tylko skomplikuje zadania tworzenia treści, jeśli zostaną wyświetlone).</span><span class="sxs-lookup"><span data-stu-id="b0257-110">(For example, a marketing section of a template can be configured to filter out irrelevant modules that should never be used in that context, and that will just complicate content authoring tasks if they are shown.)</span></span>
    - <span data-ttu-id="b0257-111">Skonfiguruj domyślne ustawienie modułu, aby zwiększyć efektywność tworzenia.</span><span class="sxs-lookup"><span data-stu-id="b0257-111">Configure default module setting to help improve authoring efficiency.</span></span>
    - <span data-ttu-id="b0257-112">Definiowanie domyślnych fragmentów stron w celu zwiększenia wydajności tworzenia.</span><span class="sxs-lookup"><span data-stu-id="b0257-112">Define default page fragments to help improve authoring efficiency.</span></span> <span data-ttu-id="b0257-113">(Na przykład fragmenty nagłówka i stopki w szablonie będą automatycznie wyświetlane na każdej stronie podrzędnej.)</span><span class="sxs-lookup"><span data-stu-id="b0257-113">(For example, header and footer fragments in a template will automatically appear on every downstream page.)</span></span>

- <span data-ttu-id="b0257-114">Umożliwia zachowanie marki dla witryn w przedsiębiorstwie przez zdefiniowanie zatwierdzonego zbioru rozmieszczenia modułów oraz opcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b0257-114">Keep enterprise sites on-brand by defining an approved set of module arrangement and configuration options.</span></span>

    > [!TIP] 
    > <span data-ttu-id="b0257-115">Pomyślne witryny e-Commerce umożliwiają klientom korzystanie z znanych, powtarzalnych i nieoznakowanych wzorców projektowania użytkowników (UX).</span><span class="sxs-lookup"><span data-stu-id="b0257-115">Successful e-Commerce sites provide customers with familiar, repeatable, and on-brand user experience (UX) design patterns.</span></span> <span data-ttu-id="b0257-116">Użycie szablonów ułatwia kontrolowanie spójności w witrynie.</span><span class="sxs-lookup"><span data-stu-id="b0257-116">By using templates, you help control consistency across your site.</span></span>

- <span data-ttu-id="b0257-117">Wyniki optymalizacji aparatu wyszukiwania (SEO) można ulepszyć przez zapewnienie powtarzalnych i programowo zdefiniowanych definicji stron i metadanych.</span><span class="sxs-lookup"><span data-stu-id="b0257-117">Improve search engine optimization (SEO) scores by ensuring repeatable and programmatically defined page definitions and metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="b0257-118">Chociaż szablony są zaprojektowane pod kątem kontroli spójności w witrynie, można je teoretycznie konfigurować, aby nie wymuszać spójności.</span><span class="sxs-lookup"><span data-stu-id="b0257-118">Although templates are designed to control consistency across a site, they can theoretically be configured so that they don't enforce any consistency.</span></span> <span data-ttu-id="b0257-119">Marki i administratorzy witryn mogą definiować dowolny poziom zmienności stron w ich oddziale.</span><span class="sxs-lookup"><span data-stu-id="b0257-119">Brand and site administrators can define any level of variability for the pages on their site.</span></span> <span data-ttu-id="b0257-120">Na przykład szablon może pozostać całkowicie otwarty, dzięki czemu autorzy zawartości mogą utworzyć dowolny projekt strony.</span><span class="sxs-lookup"><span data-stu-id="b0257-120">For example, a template can be left entirely open, so that content authors can create any page design that they choose.</span></span> <span data-ttu-id="b0257-121">W takim przypadku nie są dostępne żadne świadczenia z poprzedniej listy.</span><span class="sxs-lookup"><span data-stu-id="b0257-121">In this case, none of the benefits in the preceding list are applicable.</span></span>

## <a name="modify-a-template"></a><span data-ttu-id="b0257-122">Modyfikowanie szablonu</span><span class="sxs-lookup"><span data-stu-id="b0257-122">Modify a template</span></span>

<span data-ttu-id="b0257-123">Szablony są modyfikowane za pomocą edytora szablonów.</span><span class="sxs-lookup"><span data-stu-id="b0257-123">Templates are modified by using the template editor.</span></span>

<span data-ttu-id="b0257-124">Aby otworzyć Edytor szablonów, należy wykonać następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="b0257-124">To open the template editor, follow one of these steps:</span></span>

- <span data-ttu-id="b0257-125">W okienku nawigacji w witrynie wybierz pozycję **Szablony**, a następnie wybierz szablon do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="b0257-125">In the navigation pane of your site, select **Templates**, and then select the template to modify.</span></span>
- <span data-ttu-id="b0257-126">W edytorze stron dla istniejącej strony wybierz węzeł górny w drzewie konspektu z lewej strony.</span><span class="sxs-lookup"><span data-stu-id="b0257-126">In the page editor for an existing page, select the top node in the outline tree on the left.</span></span> <span data-ttu-id="b0257-127">Następnie w okienku właściwości po prawej stronie wybierz opcję **Edytuj szablon**.</span><span class="sxs-lookup"><span data-stu-id="b0257-127">Then, in the property pane on the right, select **Edit Template**.</span></span>

<span data-ttu-id="b0257-128">Widok drzewa konspektu po lewej stronie zawiera opcje i struktury modułu dostępne dla podrzędnych układów i stron.</span><span class="sxs-lookup"><span data-stu-id="b0257-128">The outline tree view on the left shows the module options and structures that are available to child layouts and pages.</span></span> <span data-ttu-id="b0257-129">Po wybraniu modułu w drzewie konspektu można wyświetlić właściwości szablonu dla wybranego modułu w okienku właściwości po prawej stronie.</span><span class="sxs-lookup"><span data-stu-id="b0257-129">When you select a module in the outline tree, you can view the template properties for the selected module in the property pane on the right.</span></span> <span data-ttu-id="b0257-130">Niektóre z tych właściwości są unikatowe dla edycji szablonów.</span><span class="sxs-lookup"><span data-stu-id="b0257-130">Some of these properties are unique to template editing.</span></span> <span data-ttu-id="b0257-131">W poniższej tabeli opisano te właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0257-131">The following table describes these properties.</span></span>

| <span data-ttu-id="b0257-132">Nazwa właściwości</span><span class="sxs-lookup"><span data-stu-id="b0257-132">Property name</span></span> | <span data-ttu-id="b0257-133">Opis</span><span class="sxs-lookup"><span data-stu-id="b0257-133">Description</span></span> |
|---|---|
| <span data-ttu-id="b0257-134">Minimalna liczba wystąpień</span><span class="sxs-lookup"><span data-stu-id="b0257-134">Min Occurs</span></span> | <span data-ttu-id="b0257-135">Ta właściwość określa minimalną liczbę wystąpień wybranego modułu.</span><span class="sxs-lookup"><span data-stu-id="b0257-135">This property defines the minimum number of occurrences for the selected module.</span></span> <span data-ttu-id="b0257-136">Jeśli na przykład wartość jest ustawiona na **1**, moduł jest wymagany dla autorów podrzędnych, natomiast jeśli wartość jest ustawiona na **0** (zero), moduł jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b0257-136">For example, if the value is set to **1**, the module is required for downstream authors, whereas if the value is set to **0** (zero), the module is optional.</span></span> |
| <span data-ttu-id="b0257-137">Maksymalna liczba wystąpień</span><span class="sxs-lookup"><span data-stu-id="b0257-137">Max Occurs</span></span> | <span data-ttu-id="b0257-138">Ta właściwość określa maksymalną liczbę wystąpień wybranego modułu.</span><span class="sxs-lookup"><span data-stu-id="b0257-138">This property defines the maximum number of occurrences for the selected module.</span></span> <span data-ttu-id="b0257-139">Jeśli na przykład wartość jest ustawiona na **1**, moduł można dodać tylko jeden raz.</span><span class="sxs-lookup"><span data-stu-id="b0257-139">For example, if the value is set to **1**, the module can be added only one time.</span></span> |
| <span data-ttu-id="b0257-140">Min. moduły (Kontenery)</span><span class="sxs-lookup"><span data-stu-id="b0257-140">Min Modules (Containers)</span></span> | <span data-ttu-id="b0257-141">W przypadku modułów, które zawierają inne moduły (czyli dla *modułów kontenerów*), ta właściwość definiuje minimalną liczbę modułów, które powinny zostać dodane jako elementy podrzędne.</span><span class="sxs-lookup"><span data-stu-id="b0257-141">For modules that contain other modules (that is, for *containers modules*), this property defines the minimum number of total modules that should be added as children.</span></span> <span data-ttu-id="b0257-142">Na przykład dla modułu karuzeli wartość może być ustawiona na liczbę większą niż 1.</span><span class="sxs-lookup"><span data-stu-id="b0257-142">For example, for a carousel module, the value might be set to a number that is more than 1.</span></span> |
| <span data-ttu-id="b0257-143">Max. moduły (Kontenery)</span><span class="sxs-lookup"><span data-stu-id="b0257-143">Max Modules (Containers)</span></span> | <span data-ttu-id="b0257-144">W przypadku modułów kontenera ta właściwość definiuje maksymalną liczbę modułów, które powinny zostać dodane jako elementy podrzędne.</span><span class="sxs-lookup"><span data-stu-id="b0257-144">For container modules, this property defines the maximum number of total modules that should be added as children.</span></span> <span data-ttu-id="b0257-145">Na przykład dla modułu karuzeli wartość może być ustawiona na liczbę mniejszą niż 10.</span><span class="sxs-lookup"><span data-stu-id="b0257-145">For example, for a carousel module, the value might be set to a number that is less than 10.</span></span> |
| <span data-ttu-id="b0257-146">Zablokowano</span><span class="sxs-lookup"><span data-stu-id="b0257-146">Locked</span></span> | <span data-ttu-id="b0257-147">Obok wszystkich właściwości modułu podstawowego zostanie wyświetlona **zablokowana** kontrola logiczna.</span><span class="sxs-lookup"><span data-stu-id="b0257-147">A **Locked** Boolean control appears next to all core module properties.</span></span> <span data-ttu-id="b0257-148">Pozwala to autorowi szablonów na zablokowanie ustawienia modułu w szablonie.</span><span class="sxs-lookup"><span data-stu-id="b0257-148">It lets the template author lock a module setting in the template.</span></span> <span data-ttu-id="b0257-149">Zablokowane ustawienie modułu nie może być zastąpione przez żadną inną podrzędną układu lub strony.</span><span class="sxs-lookup"><span data-stu-id="b0257-149">A module setting that is locked can't be overridden by any child layouts or pages.</span></span> <span data-ttu-id="b0257-150">Staje się centralnie edytowalną wartością właściwości dla wszystkich układów i stron korzystających z szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-150">It becomes a centrally editable property value for all layouts and pages that use the template.</span></span> |

## <a name="create-a-new-template"></a><span data-ttu-id="b0257-151">Utwórz nowy szablon</span><span class="sxs-lookup"><span data-stu-id="b0257-151">Create a new template</span></span>

<span data-ttu-id="b0257-152">Aby utworzyć nowy szablon, należy wykonać poniższe kroki.</span><span class="sxs-lookup"><span data-stu-id="b0257-152">To create a new template, follow these steps.</span></span>

1. <span data-ttu-id="b0257-153">W okienku nawigacji w witrynie wybierz pozycję **Szablony**, a następnie otwórz szablon w widoku inspekcji.</span><span class="sxs-lookup"><span data-stu-id="b0257-153">In the navigation pane of your site, select **Templates** to open the template inspector view.</span></span>
1. <span data-ttu-id="b0257-154">Wybierz **Nowy szablon**.</span><span class="sxs-lookup"><span data-stu-id="b0257-154">Select **New Template**.</span></span>
1. <span data-ttu-id="b0257-155">W oknie dialogowym tworzenia szablonu wprowadź nazwę i opis szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-155">In the template creation dialog box, enter a name and description for the template.</span></span> <span data-ttu-id="b0257-156">Wprowadzone wartości będą widoczne dla autorów podczas tworzenia nowych stron.</span><span class="sxs-lookup"><span data-stu-id="b0257-156">The values that you enter will be shown to authors when they create new pages.</span></span> <span data-ttu-id="b0257-157">Dlatego należy wprowadzić metadane, które będą przydatne autorom stron.</span><span class="sxs-lookup"><span data-stu-id="b0257-157">Therefore, enter metadata that will be useful to page authors.</span></span> <span data-ttu-id="b0257-158">Na przykład wprowadź **Ten szablon służy do tworzenia ogólnych stron marketingowych** jako opis.</span><span class="sxs-lookup"><span data-stu-id="b0257-158">For example, enter **Use this template to create general marketing pages** as the description.</span></span> <span data-ttu-id="b0257-159">Te metadane można później edytować.</span><span class="sxs-lookup"><span data-stu-id="b0257-159">This metadata can be edited later.</span></span>
1. <span data-ttu-id="b0257-160">Wybierz przycisk **OK**, aby utworzyć nowy szablon i otworzyć edytor szablonów.</span><span class="sxs-lookup"><span data-stu-id="b0257-160">Select **OK** to create the new template and open the template editor.</span></span> <span data-ttu-id="b0257-161">Edytor szablonów pokazuje drzewo konspektu po lewej stronie i okienko właściwości po prawej stronie.</span><span class="sxs-lookup"><span data-stu-id="b0257-161">The template editor shows an outline tree on the left and a property pane on the right.</span></span>
1. <span data-ttu-id="b0257-162">W drzewie konspektu rozwiń węzły i wybierz gniazdo **nagłówka HTML**.</span><span class="sxs-lookup"><span data-stu-id="b0257-162">In the outline tree, expand the nodes, and select the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b0257-163">Jeśli w tym gnieździe nie ma jeszcze żadnych modułów, należy wybrać przycisk wielokropka (**...**), a następnie wybierz pozycję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="b0257-163">If there aren't yet any modules in this slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b0257-164">W oknie dialogowym **Dodaj moduł** wybierz **Podsumowanie domyslnej strony** i wybierz przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0257-164">In the **Add Module** dialog box, select **Default page summary**, and then select **OK**.</span></span>
1. <span data-ttu-id="b0257-165">W drzewie konspektu wybierz nowy moduł, a następnie w okienku właściwości wprowadź wszystkie ustawienia domyślne, które powinny być konfigurowane automatycznie dla wszystkich stron podrzędnych szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-165">In the outline tree, select the new module, and then, in the property pane, enter any default settings that should be automatically configured for all child pages of the template.</span></span> <span data-ttu-id="b0257-166">Jeśli nie chcesz dodawaj żadnych ustawień domyślnych, pozostaw te wartości puste.</span><span class="sxs-lookup"><span data-stu-id="b0257-166">If you don't want any default settings, leave the values blank.</span></span>
1. <span data-ttu-id="b0257-167">W drzewie konspektu wybierz **Treść**, następnie wybierz przycisk wielokropka, a następnie wybierz pozycję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="b0257-167">In the outline tree, select the **Body** slot, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b0257-168">Wybierz moduł kontenera strony (może być tylko jedna opcja), a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0257-168">Select a page container module (there might be only one option), and then select **OK**.</span></span>

<span data-ttu-id="b0257-169">W obszarze nowy kontener strony zostanie wyświetlony nowy zbiór gniazd (**nagłówek**, **główne** itd.).</span><span class="sxs-lookup"><span data-stu-id="b0257-169">Under the new page container module, you will see a new set of slots (**Header**, **Main**, and so on).</span></span> <span data-ttu-id="b0257-170">W tym miejscu można dodać i skonfigurować opcje modułu, które będą dostępne dla autorów podczas tworzenia stron z tego szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-170">Here, you can add and configure the module options that will be available to authors when they create pages from this template.</span></span> <span data-ttu-id="b0257-171">Domyślnie, jeśli żadne moduły nie są dodawane do gniazda, obsługiwane są wszystkie dostępne typy modułów dla tego gniazda.</span><span class="sxs-lookup"><span data-stu-id="b0257-171">By default, if you don't add any modules to a slot, all available modules types are supported for that slot.</span></span>

<span data-ttu-id="b0257-172">Szablon jest teraz technicznie prawidłowy i może być zapisany, zaewidencjonowany i używany do tworzenia nowych stron.</span><span class="sxs-lookup"><span data-stu-id="b0257-172">The template is now technically valid, and it can be saved, checked in, and used to create new pages.</span></span> <span data-ttu-id="b0257-173">Jednak następne trzy sekcje opisują niektóre inne ustawienia domyślne, które można skonfigurować jako pierwsze.</span><span class="sxs-lookup"><span data-stu-id="b0257-173">However, the next three sections describe some other default settings that you might want to configure first.</span></span>

## <a name="add-a-header-and-a-footer"></a><span data-ttu-id="b0257-174">Dodawanie nagłówka i stopki</span><span class="sxs-lookup"><span data-stu-id="b0257-174">Add a header and a footer</span></span>

<span data-ttu-id="b0257-175">Jeśli witryna ma już fragment nagłówka, należy wykonać poniższe kroki w celu dodania nagłówka i stopki do szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-175">If your site already has a header fragment, follow these steps to add a header and a footer to a template.</span></span>

1. <span data-ttu-id="b0257-176">W drzewie konspektu rozwiń miejsce w **treści** i podrzędny moduł strony.</span><span class="sxs-lookup"><span data-stu-id="b0257-176">In the outline tree, expand the **Body** slot and its child page module.</span></span>
1. <span data-ttu-id="b0257-177">Wybierz gniazdo **nagłówka**.</span><span class="sxs-lookup"><span data-stu-id="b0257-177">Select the **Header** slot.</span></span>
1. <span data-ttu-id="b0257-178">Wybierz przycisk wielokropka (...) dla gniazda **Nagłówek**, a następnie wybierz opcję **Dodaj fragment**.</span><span class="sxs-lookup"><span data-stu-id="b0257-178">Select the ellipsis button for the **Header** slot, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="b0257-179">Wyszukaj i wybierz fragment nagłówka oddziału, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0257-179">Search for and select your site's header fragment, and then select **OK**.</span></span>

<span data-ttu-id="b0257-180">Wszystkie strony korzystające z szablonu będą teraz automatycznie dziedziczyły ten fragment nagłówka.</span><span class="sxs-lookup"><span data-stu-id="b0257-180">All pages that use the template will now automatically inherit this header fragment.</span></span>

<span data-ttu-id="b0257-181">Jeśli witryna nie ma jeszcze fragmentu nagłówka, zapoznaj się z tematem [Tworzenie fragmentu](work-with-fragments.md#create-a-fragment), aby uzyskać informacje na temat sposobu jego utworzenia, a następnie wykonaj poprzednią procedurę.</span><span class="sxs-lookup"><span data-stu-id="b0257-181">If your site doesn't yet have a header fragment, see [Create a fragment](work-with-fragments.md#create-a-fragment) for information about how to create it, and then complete the previous procedure.</span></span>

## <a name="change-the-template-theme"></a><span data-ttu-id="b0257-182">Zmień szablon motywu</span><span class="sxs-lookup"><span data-stu-id="b0257-182">Change the template theme</span></span>

<span data-ttu-id="b0257-183">Aby określić domyślny motyw dla wszystkich stron korzystających z szablonu, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="b0257-183">To set the default theme for all pages that use a template, follow these steps.</span></span>

1. <span data-ttu-id="b0257-184">W drzewie konspektu z lewej strony rozwiń gniazdo w **treści**.</span><span class="sxs-lookup"><span data-stu-id="b0257-184">In the outline tree on the left, expand the **Body** slot.</span></span>
1. <span data-ttu-id="b0257-185">W gnieździe **treści** wybierz moduł kontenera strony (na przykład **strona domyślna**).</span><span class="sxs-lookup"><span data-stu-id="b0257-185">In the **Body** slot, select the page container module (for example, **Default Page**).</span></span>
1. <span data-ttu-id="b0257-186">W okienku właściwości po prawej stronie w polu **motyw** wybierz motyw.</span><span class="sxs-lookup"><span data-stu-id="b0257-186">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

<span data-ttu-id="b0257-187">Domyślnie wszystkie nowe strony używają teraz wybranej kompozycji.</span><span class="sxs-lookup"><span data-stu-id="b0257-187">By default, all new pages will now use the selected theme.</span></span> <span data-ttu-id="b0257-188">Aby strony nie miały zastąpienia tego ustawienia na poziomie układu lub strony, należy ustawić dla **zablokowanej** kontrolki logicznej wartość **prawda**.</span><span class="sxs-lookup"><span data-stu-id="b0257-188">To prevent pages from overriding this setting at the layout or page level, set the **Locked** Boolean control to **True**.</span></span>

## <a name="add-a-script-to-a-template"></a><span data-ttu-id="b0257-189">Dodawanie skryptu do szablonu</span><span class="sxs-lookup"><span data-stu-id="b0257-189">Add a script to a template</span></span>

<span data-ttu-id="b0257-190">Do szablonu można dodawać elementy **&lt;skryptu&gt;** HTML zawierające kod JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0257-190">You can add HTML **&lt;script&gt;** elements that contain JavaScript to your template.</span></span> <span data-ttu-id="b0257-191">W ten sposób można udostępnić domyślne zachowania skryptów w sekcjach nagłówka HTML, początku treści oraz końcowych treści stron.</span><span class="sxs-lookup"><span data-stu-id="b0257-191">In this way, you can provide default script behaviors to the HTML head, body begin, and body end sections of your pages.</span></span>

<span data-ttu-id="b0257-192">Aby dodać skrypt do szablonu pracy, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="b0257-192">To add a script to a template, follow these steps.</span></span>

1. <span data-ttu-id="b0257-193">W drzewie konspektu z lewej strony wybierz gniazdo, w którym chcesz dodać element **&lt;skryptu&gt;** (np. nagłówek HTML, początek treści lub zakończenie treści).</span><span class="sxs-lookup"><span data-stu-id="b0257-193">In the outline tree on the left, select the slot where you want to add the **&lt;script&gt;** element (for example, the HTML head, body begin, or body end).</span></span>
1. <span data-ttu-id="b0257-194">Wybierz przycisk wielokropka (...) dla gniazda, a następnie wybierz opcję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="b0257-194">Select the ellipsis button for the slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b0257-195">W oknie dialogowym **Dodaj moduł** wybierz moduł skryptu ( np. **skrypt zewnętrzny** lub **skrypt wbudowany**).</span><span class="sxs-lookup"><span data-stu-id="b0257-195">In the **Add Module** dialog box, select a script module (for example, **External Script** or **Inline Script**).</span></span>
1. <span data-ttu-id="b0257-196">W okienku właściwości po prawej stronie, w odpowiednim formancie właściwości skryptu (np. **skrypt wbudowany** lub **tagi skryptu**) wprowadź odpowiedni skrypt.</span><span class="sxs-lookup"><span data-stu-id="b0257-196">In the property pane on the right, in the appropriate script property control (for example, **Inline Script** or **Script tags**), enter your script.</span></span>
1. <span data-ttu-id="b0257-197">W okienku właściwości wprowadź inne ustawienia opcjonalne, które chcesz skonfigurować.</span><span class="sxs-lookup"><span data-stu-id="b0257-197">In the property pane, enter any other optional settings that you want to configure.</span></span>

> [!TIP]
> <span data-ttu-id="b0257-198">Jeśli chcesz ponownie użyć dowolnego z modułów skryptów dla innych szablonów, możesz przekonwertować je na fragmenty.</span><span class="sxs-lookup"><span data-stu-id="b0257-198">If you want to reuse any of your script modules for other templates, you can convert them to fragments.</span></span> <span data-ttu-id="b0257-199">W ten sposób użytkownik pomaga zwiększyć efektywność procesu tworzenia i scentralizowa proces aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="b0257-199">In this way, you help make the authoring process more efficient, and you centralize the update process.</span></span> <span data-ttu-id="b0257-200">Aby uzyskać informacje na temat konwertowania modułu skryptu na fragment, zapoznaj się z tematem [Zapisz istniejącą konfigurację modułu jako fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span><span class="sxs-lookup"><span data-stu-id="b0257-200">For information about how to convert a script module to a fragment, see [Save an existing module configuration as a fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span></span>

## <a name="save-check-in-preview-and-publish-a-template"></a><span data-ttu-id="b0257-201">Zapisywanie, zaewidencjonuj, przejrzyj i opublikuj szablon</span><span class="sxs-lookup"><span data-stu-id="b0257-201">Save, check in, preview, and publish a template</span></span>

<span data-ttu-id="b0257-202">Aby zapisać i zewidencjonować szablon, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="b0257-202">To save and check in a template, follow these steps.</span></span>

1. <span data-ttu-id="b0257-203">Wybierz opcję **Zapisz** u góry edytora szablonów.</span><span class="sxs-lookup"><span data-stu-id="b0257-203">Select **Save** at the top of the template editor.</span></span> <span data-ttu-id="b0257-204">Zapisane zmiany nie wpływają na strony podrzędne, dopóki nie zostaną zaewidencjonowane.</span><span class="sxs-lookup"><span data-stu-id="b0257-204">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="b0257-205">Wybierz **Zaewidencjonuj**.</span><span class="sxs-lookup"><span data-stu-id="b0257-205">Select **Check In**.</span></span> <span data-ttu-id="b0257-206">Twoje zmiany są teraz wykrywalne dla podrzędnych przepływów pracy.</span><span class="sxs-lookup"><span data-stu-id="b0257-206">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="b0257-207">Aby wyświetlić podgląd zmian, należy otworzyć istniejącą stronę, która używa tego szablonu, lub utworzyć nową stronę na podstawie tego szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-207">To preview your changes, either open an existing page that uses the template or create a new page from the template.</span></span>

<span data-ttu-id="b0257-208">Po przejrzeniu zmian w szablonie należy wykonać jedną z następujących czynności, aby opublikować szablon w witrynie na żywo:</span><span class="sxs-lookup"><span data-stu-id="b0257-208">After you've previewed the changes to your template, follow one of these steps to publish the template to your live site:</span></span>

* <span data-ttu-id="b0257-209">Przejdź do **Szablony**, wybierz szablon, a następnie wybierz opcję **Opublikuj**.</span><span class="sxs-lookup"><span data-stu-id="b0257-209">Go to **Templates**, select the template, and then select **Publish**.</span></span>
* <span data-ttu-id="b0257-210">W edytorze szablonów wybierz opcję **Opublikuj**.</span><span class="sxs-lookup"><span data-stu-id="b0257-210">In the template editor, select **Publish**.</span></span>
* <span data-ttu-id="b0257-211">Umożliwia opublikowanie strony, która odwołuje się do nieopublikowanego szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0257-211">Publish a page that references the unpublished template.</span></span> <span data-ttu-id="b0257-212">Szablon zostanie automatycznie opublikowany.</span><span class="sxs-lookup"><span data-stu-id="b0257-212">The template is automatically published.</span></span>

> [!WARNING]
> <span data-ttu-id="b0257-213">Po opublikowaniu szablon lub dowolny inny element systemu zarządzania zawartością (CMS) jest wykrywalny w Internecie.</span><span class="sxs-lookup"><span data-stu-id="b0257-213">When a template, or any other content management system (CMS) item, is published, it's discoverable on the internet.</span></span> <span data-ttu-id="b0257-214">Nie Publikuj dokumentów ani zasobów, dopóki nie przygotujesz ich do publicznego udostępnienia.</span><span class="sxs-lookup"><span data-stu-id="b0257-214">Don't publish documents or assets until you're ready to make them public.</span></span> <span data-ttu-id="b0257-215">Wersje dokumentów, które zostały zapisane i zaewidencjonowane, ale nie zostały opublikowane, są wykrywalne tylko dla uwierzytelnionych użytkowników systemu.</span><span class="sxs-lookup"><span data-stu-id="b0257-215">Document versions that have been saved and checked in, but that haven't been published, are discoverable only to authenticated system users.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0257-216">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="b0257-216">Additional resources</span></span>

[<span data-ttu-id="b0257-217">Omówienie szablonów i układów</span><span class="sxs-lookup"><span data-stu-id="b0257-217">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b0257-218">Praca z układami predefiniowanymi</span><span class="sxs-lookup"><span data-stu-id="b0257-218">Work with preset layouts</span></span>](work-with-layouts.md)