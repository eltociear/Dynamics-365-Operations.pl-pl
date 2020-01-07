---
title: Dodawanie nowej strony witryny
description: W tym temacie opisano, jak dodać nową stronę witryny w Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d5ab90343220e427a80cc4dde17c628ba64ac69e
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696745"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="70340-103">Dodawanie nowej strony witryny</span><span class="sxs-lookup"><span data-stu-id="70340-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="70340-104">W tym temacie opisano, jak dodać nową stronę witryny w Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70340-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="70340-105">Omówienie</span><span class="sxs-lookup"><span data-stu-id="70340-105">Overview</span></span>

<span data-ttu-id="70340-106">Po utworzeniu szablonów i fragmentów dla witryny następnym krokiem jest rozpoczęcie tworzenia stron, które ich używają.</span><span class="sxs-lookup"><span data-stu-id="70340-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="70340-107">Aby rozpocząć, musisz wybrać szablon lub układ, nazwę strony oraz adres URL strony.</span><span class="sxs-lookup"><span data-stu-id="70340-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="70340-108">Szablon lub układ</span><span class="sxs-lookup"><span data-stu-id="70340-108">Template or layout</span></span>

<span data-ttu-id="70340-109">Dla nowej strony można zastosować szablon lub układ.</span><span class="sxs-lookup"><span data-stu-id="70340-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="70340-110">Aby uzyskać więcej informacji, zobacz [Omówienie szablonów i układów](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="70340-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="70340-111">Nazwa strony</span><span class="sxs-lookup"><span data-stu-id="70340-111">Page name</span></span>

<span data-ttu-id="70340-112">Nazwa strony musi być unikatowa dla danej strony.</span><span class="sxs-lookup"><span data-stu-id="70340-112">The page name must be unique to your page.</span></span> <span data-ttu-id="70340-113">Powinna ona być opisowa, aby można było łatwo ją odnaleźć i inne osoby wiedziały, że jest przeznaczona dla strony.</span><span class="sxs-lookup"><span data-stu-id="70340-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="70340-114">Należy uważnie wybrać nazwę strony, ponieważ nie można jej później zmienić.</span><span class="sxs-lookup"><span data-stu-id="70340-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="70340-115">Adres URL strony</span><span class="sxs-lookup"><span data-stu-id="70340-115">Page URL</span></span>

<span data-ttu-id="70340-116">Można wybrać opcję wprowadzania adresu URL dla nowej strony.</span><span class="sxs-lookup"><span data-stu-id="70340-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="70340-117">Podczas tworzenia strony można wprowadzić ciąg, który będzie używany do tworzenia pełnego adresu URL.</span><span class="sxs-lookup"><span data-stu-id="70340-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="70340-118">Ten ciąg określany jest jako względny adres URL lub do informacji o adresie URL.</span><span class="sxs-lookup"><span data-stu-id="70340-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="70340-119">Cały adres URL jest następnie generowany na podstawie informacji o adresach URL, a nowa strona jest przypisana do niej.</span><span class="sxs-lookup"><span data-stu-id="70340-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="70340-120">Przed opublikowaniem strony można później zmienić jej adres URL.</span><span class="sxs-lookup"><span data-stu-id="70340-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="70340-121">Aby uzyskać więcej informacji, zobacz temat [Tworzenie adresu URL strony](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="70340-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="70340-122">Dynamics 365 Commerce rozdziela adresy URL i zawartość.</span><span class="sxs-lookup"><span data-stu-id="70340-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="70340-123">Innymi słowy, można utworzyć stronę, która nie jest skojarzona z adresem URL i utworzyć adres URL, który nie jest skojarzony ze stroną.</span><span class="sxs-lookup"><span data-stu-id="70340-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="70340-124">W związku z tym może nastąpić założenie zawartości adresu URL i nie wymaga przestoju, a przekierowywanie jest łatwiejsze do zarządzania.</span><span class="sxs-lookup"><span data-stu-id="70340-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="70340-125">Dodawanie nowej strony</span><span class="sxs-lookup"><span data-stu-id="70340-125">Add a new page</span></span>

<span data-ttu-id="70340-126">Aby dodać nową stronę do swojej witryny, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="70340-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="70340-127">W obszarze **Witryny** wybierz **Fabrikam** (lub nazwę witryny).</span><span class="sxs-lookup"><span data-stu-id="70340-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="70340-128">Wybierz **Nowa strona**.</span><span class="sxs-lookup"><span data-stu-id="70340-128">Select **New Page**.</span></span>
1. <span data-ttu-id="70340-129">W oknie dialogowym **Nowa strona** wybierz szablon i wybierz przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="70340-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="70340-130">W polu **Nazwa strony** wprowadź nazwę strony (na przykład **Nowa strona**).</span><span class="sxs-lookup"><span data-stu-id="70340-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="70340-131">W polu **adres URL** wprowadź ciąg (adres URL), aby dokończyć adres URL (na przykład **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="70340-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="70340-132">Kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="70340-132">Select **OK**.</span></span> <span data-ttu-id="70340-133">Zostanie wyświetlona strona edytora.</span><span class="sxs-lookup"><span data-stu-id="70340-133">The page editor appears.</span></span> <span data-ttu-id="70340-134">Zauważ, że nagłówek i stopka są automatycznie dodawane do strony na podstawie wybranego szablonu.</span><span class="sxs-lookup"><span data-stu-id="70340-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="70340-135">W konspekcie strony wybierz gniazdo **Główne**, następnie wybierz przycisk wielokropka (**...**), a następnie wybierz pozycję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="70340-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="70340-136">Zaznacz element **Kontener** i kliknij przycisk **OK**</span><span class="sxs-lookup"><span data-stu-id="70340-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="70340-137">Wybierz **Kontener płynny**, a następnie wybierz przycisk wielokropka i opcję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="70340-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="70340-138">Zaznacz **Blok zawartości sformatowanej**, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="70340-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="70340-139">Wybierz **Blok zawartości sformatowanej**, a następnie wybierz przycisk wielokropka i opcję **Dodaj moduł**.</span><span class="sxs-lookup"><span data-stu-id="70340-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="70340-140">Zaznacz **Element bloku zawartości sformatowanej**, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="70340-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="70340-141">W okienku właściwości po prawej stronie wybierz pozycję **Akapit**, a następnie w polu wprowadź **Tekst testowy**.</span><span class="sxs-lookup"><span data-stu-id="70340-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="70340-142">Wybierz **Zapisz** i następnie wybierz **Zaewidencjonuj**.</span><span class="sxs-lookup"><span data-stu-id="70340-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="70340-143">W polu **Komentarze** wprowadź **Dodawanie nowej strony**, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="70340-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="70340-144">Wybierz opcję **Podgląd**, aby wyświetlić podgląd strony.</span><span class="sxs-lookup"><span data-stu-id="70340-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="70340-145">Po zakończeniu Zamknij kartę podglądu, aby powrócić do narzędzia autorskiego.</span><span class="sxs-lookup"><span data-stu-id="70340-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="70340-146">Wybierz opcję **Publikuj**.</span><span class="sxs-lookup"><span data-stu-id="70340-146">Select **Publish**.</span></span>
1. <span data-ttu-id="70340-147">W ścieżce nawigacji (struktura nawigacyjna) wybierz firmę **Fabrikam** (lub nazwę witryny).</span><span class="sxs-lookup"><span data-stu-id="70340-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="70340-148">W okienku nawigacji po lewej stronie zaznacz **adresy URL**.</span><span class="sxs-lookup"><span data-stu-id="70340-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="70340-149">Na liście znajdź i zaznacz URL (**mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="70340-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="70340-150">Wybierz opcję **Publikuj**.</span><span class="sxs-lookup"><span data-stu-id="70340-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70340-151">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="70340-151">Additional resources</span></span>

[<span data-ttu-id="70340-152">Modyfikacja istniejącej strony witryny</span><span class="sxs-lookup"><span data-stu-id="70340-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="70340-153">Wybieranie układów stron</span><span class="sxs-lookup"><span data-stu-id="70340-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="70340-154">Zarządzanie metadanymi funkcji optymalizacji aparatu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="70340-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="70340-155">Zapisywanie, pogląd i publikowanie strony</span><span class="sxs-lookup"><span data-stu-id="70340-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="70340-156">Wzbogacanie strony produktu</span><span class="sxs-lookup"><span data-stu-id="70340-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="70340-157">Wzbogacanie strony docelowej kategorii</span><span class="sxs-lookup"><span data-stu-id="70340-157">Enrich a category landing page</span></span>](enrich-category-page.md)
