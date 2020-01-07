---
title: Moduł umieszczania zawartości
description: W tym temacie omówiono moduły rozmieszczania treści i elementów umieszczania treści oraz opisano sposób dodawania ich do stron witryny w Microsoft Dynamics 365 Commerce.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785307"
---
# <a name="content-placement-module"></a><span data-ttu-id="4c054-103">Moduł umieszczania zawartości</span><span class="sxs-lookup"><span data-stu-id="4c054-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4c054-104">W tym temacie omówiono moduły rozmieszczania treści i elementów umieszczania treści oraz opisano sposób dodawania ich do stron witryny w Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c054-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4c054-105">Omówienie</span><span class="sxs-lookup"><span data-stu-id="4c054-105">Overview</span></span>

<span data-ttu-id="4c054-106">Moduł umieszczania zawartości to specjalny kontener, w którym inne moduły mogą być umieszczone wewnątrz określonego układu.</span><span class="sxs-lookup"><span data-stu-id="4c054-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="4c054-107">Moduły umieszczania zawartości obsługują następujące typy modułów jako moduły podrzędne: element umieszczania zawartości, pozycja powitalna konta, pozycja zamówienia konta, pozycja listy życzeń konta oraz pozycja profilu konta.</span><span class="sxs-lookup"><span data-stu-id="4c054-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="4c054-108">Moduły umieszczania zawartości pobierają dane z obsługiwanych przez nie modułów podrzędnych.</span><span class="sxs-lookup"><span data-stu-id="4c054-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="4c054-109">Z tego względu moduły umieszczania zawartości mogą być używane na różne sposoby, w zależności od dodawanych do niej modułów.</span><span class="sxs-lookup"><span data-stu-id="4c054-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="4c054-110">Moduły elementów umieszczania treści używają zarówno obrazów, jak i tekstu do prezentacji promocji, zasad i funkcji produktu.</span><span class="sxs-lookup"><span data-stu-id="4c054-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="4c054-111">Na przykład na stronie głównej można użyć modułu elementów umieszczania zawartości, aby wyświetlić zasady sklepu lub informacje o wysyłce.</span><span class="sxs-lookup"><span data-stu-id="4c054-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="4c054-112">Moduły umieszczania zawartości są sterowane danymi z systemu zarządzania zawartością (CMS) i mogą być umieszczane na dowolnej stronie.</span><span class="sxs-lookup"><span data-stu-id="4c054-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="4c054-113">Można je jednak używać tylko wewnątrz modułu umieszczania zawartości.</span><span class="sxs-lookup"><span data-stu-id="4c054-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="4c054-114">Przykłady modułów umieszczania zawartości w e-Commerce</span><span class="sxs-lookup"><span data-stu-id="4c054-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="4c054-115">Moduły umieszczania zawartości, które zawierają moduły elementów do umieszczania zawartości, mogą być używane na stronach głównych lub marketingowych w celu zaprezentowania funkcji produktu, promocji, zasad sklepu, informacji o wysyłce oraz innych informacji za pośrednictwem obu obrazów i tekstu.</span><span class="sxs-lookup"><span data-stu-id="4c054-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="4c054-116">Moduły umieszczania zawartości, które zawierają moduły elementów do umieszczania zawartości, mogą być używane na stronach szczegółów produktu w celu zaprezentowania funkcji produktu.</span><span class="sxs-lookup"><span data-stu-id="4c054-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="4c054-117">Na stronach zarządzania kontami można używać modułów umieszczania zawartości zawierających elementy powitalne konta lub moduły towarów z zamówieniami konta.</span><span class="sxs-lookup"><span data-stu-id="4c054-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="4c054-118">Właściwości modułu rozmieszczania treści</span><span class="sxs-lookup"><span data-stu-id="4c054-118">Content placement module properties</span></span>

| <span data-ttu-id="4c054-119">Nazwa właściwości</span><span class="sxs-lookup"><span data-stu-id="4c054-119">Property name</span></span> | <span data-ttu-id="4c054-120">Wartość</span><span class="sxs-lookup"><span data-stu-id="4c054-120">Value</span></span> | <span data-ttu-id="4c054-121">Opis</span><span class="sxs-lookup"><span data-stu-id="4c054-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="4c054-122">Szerokość</span><span class="sxs-lookup"><span data-stu-id="4c054-122">Width</span></span>         | <span data-ttu-id="4c054-123">**Dopasuj do kontenera** lub **ekran wypełnienia**</span><span class="sxs-lookup"><span data-stu-id="4c054-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="4c054-124">Jeśli wartość jest ustawiona na **Dopasuj do kontenera**, elementy w module rozmieszczania treści są ograniczone do szerokości modułu rozmieszczania treści.</span><span class="sxs-lookup"><span data-stu-id="4c054-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="4c054-125">Jeśli wartość jest ustawiona na **wypełnienie ekranu**, elementy nie są ograniczone do szerokości modułu rozmieszczania treści, ale mogą przechodzić do trybu pełnoekranowego.</span><span class="sxs-lookup"><span data-stu-id="4c054-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="4c054-126">Właściwości modułu elementu rozmieszczania treści</span><span class="sxs-lookup"><span data-stu-id="4c054-126">Content placement item module properties</span></span>

| <span data-ttu-id="4c054-127">Nazwa właściwości</span><span class="sxs-lookup"><span data-stu-id="4c054-127">Property name</span></span> | <span data-ttu-id="4c054-128">Wartość</span><span class="sxs-lookup"><span data-stu-id="4c054-128">Value</span></span> | <span data-ttu-id="4c054-129">Opis</span><span class="sxs-lookup"><span data-stu-id="4c054-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="4c054-130">Nagłówek</span><span class="sxs-lookup"><span data-stu-id="4c054-130">Heading</span></span>       | <span data-ttu-id="4c054-131">Tekst nagłówka i znaczniki nagłówka (**H1**, **H2**, **H3**, **H4**, **H5** lub **H6**)</span><span class="sxs-lookup"><span data-stu-id="4c054-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4c054-132">Każdy moduł elementu rozmieszczenia zawartości może mieć nagłówek.</span><span class="sxs-lookup"><span data-stu-id="4c054-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="4c054-133">Właściwość **nagłówek** obsługuje znaczniki nagłówków.</span><span class="sxs-lookup"><span data-stu-id="4c054-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="4c054-134">Domyślnie jest używany znacznik nagłówka **H2**, ale znacznik nagłówka jest używany, ale tag nagłówka można zmienić, aby spełnić wymagania dotyczące dostępności.</span><span class="sxs-lookup"><span data-stu-id="4c054-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="4c054-135">Akapit</span><span class="sxs-lookup"><span data-stu-id="4c054-135">Paragraph</span></span>     | <span data-ttu-id="4c054-136">Tekst akapitu</span><span class="sxs-lookup"><span data-stu-id="4c054-136">Paragraph text</span></span> | <span data-ttu-id="4c054-137">Moduły elementu rozmieszczania zawartości obsługują tekst akapitu w formacie RTF.</span><span class="sxs-lookup"><span data-stu-id="4c054-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="4c054-138">Obsługiwane są pewne podstawowe funkcje tekstu sformatowanego, takie jak pogrubiony, podkreślony, kursywa i hiperłącza.</span><span class="sxs-lookup"><span data-stu-id="4c054-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="4c054-139">Niektóre z tych możliwości mogą być zastąpione przez motyw strony stosowany do modułu.</span><span class="sxs-lookup"><span data-stu-id="4c054-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="4c054-140">Wizerunek</span><span class="sxs-lookup"><span data-stu-id="4c054-140">Image</span></span>         | <span data-ttu-id="4c054-141">Plik obrazu</span><span class="sxs-lookup"><span data-stu-id="4c054-141">Image file</span></span> | <span data-ttu-id="4c054-142">Obraz może być skojarzony z tekstem.</span><span class="sxs-lookup"><span data-stu-id="4c054-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="4c054-143">Link</span><span class="sxs-lookup"><span data-stu-id="4c054-143">Link</span></span>          | <span data-ttu-id="4c054-144">Połącz adres URL i tekst łącza</span><span class="sxs-lookup"><span data-stu-id="4c054-144">Link URL and link text</span></span> | <span data-ttu-id="4c054-145">Do tekstu można dodać łącze umożliwiające przekierowanie użytkowników do konkretnej strony.</span><span class="sxs-lookup"><span data-stu-id="4c054-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="4c054-146">Rozmiar kafelka</span><span class="sxs-lookup"><span data-stu-id="4c054-146">Tile size</span></span>     | <span data-ttu-id="4c054-147">Liczba z zakresu od **1** do **12**</span><span class="sxs-lookup"><span data-stu-id="4c054-147">A number from **1** through **12**</span></span> | <span data-ttu-id="4c054-148">Dla każdego elementu umieszczania zawartości Właściwość określa liczbę gniazd, które powinny wypełnić element w module umieszczania zawartości.</span><span class="sxs-lookup"><span data-stu-id="4c054-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="4c054-149">Maksymalny rozmiar modułu umieszczania zawartości wynosi 12 gniazd.</span><span class="sxs-lookup"><span data-stu-id="4c054-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="4c054-150">Jeśli całkowity rozmiar segmentu dla pierwszych *n* elementów w module umieszczania zawartości przekracza 12 gniazd, towary są przepakowane do następnego wiersza.</span><span class="sxs-lookup"><span data-stu-id="4c054-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="4c054-151">Dodaj moduł umieszczania zawartości zawierający moduł elementu umieszczania zawartości do strony</span><span class="sxs-lookup"><span data-stu-id="4c054-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="4c054-152">Aby dodać moduł umieszczania zawartości zawierający moduł elementu umieszczania zawartości do nowej strony i określić wymagane właściwości, wykonaj następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="4c054-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4c054-153">Utwórz szablon o nazwie nazwa **szablon rozmieszczania zawartości**.</span><span class="sxs-lookup"><span data-stu-id="4c054-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="4c054-154">W **Głównym** gnieździe na stronie domyślnej dodaj moduł rozmieszczania zawartości.</span><span class="sxs-lookup"><span data-stu-id="4c054-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="4c054-155">W module umieszczania treści dodaj moduł elementu umieszczania treści.</span><span class="sxs-lookup"><span data-stu-id="4c054-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="4c054-156">Zaewidencjonuj szablon i opublikuj go.</span><span class="sxs-lookup"><span data-stu-id="4c054-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="4c054-157">Za pomocą utworzonego właśnie szblonu rozmieszcznia zawartości utwórz stronę o nazwie **strona rozmieszcznia zawartości**.</span><span class="sxs-lookup"><span data-stu-id="4c054-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="4c054-158">W **Głównym** gnieździe na nowej stronie dodaj moduł rozmieszczania zawartości.</span><span class="sxs-lookup"><span data-stu-id="4c054-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="4c054-159">W module umieszczania treści dodaj moduł elementu umieszczania treści.</span><span class="sxs-lookup"><span data-stu-id="4c054-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="4c054-160">W okienku właściwości modułu elementu rozmieszczenia zawartości wybierz obraz, dodaj nagłówek, dodaj akapit, dodaj łącze, określ adres URL łącza i określ rozmiar kafelka na **6.**</span><span class="sxs-lookup"><span data-stu-id="4c054-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="4c054-161">Powtórz kroki 7 i 8, aby dodać kolejny moduł elementu rozmieszczenia zawartości o takim samym rozmiarze kafelka.</span><span class="sxs-lookup"><span data-stu-id="4c054-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="4c054-162">Zapisz i zobacz podgląd strony.</span><span class="sxs-lookup"><span data-stu-id="4c054-162">Save and preview the page.</span></span> <span data-ttu-id="4c054-163">Powinny być widoczne dwa elementy umieszczania zawartości widoczne obok siebie.</span><span class="sxs-lookup"><span data-stu-id="4c054-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="4c054-164">Można dostosować Właściwość **rozmiaru kafelka** każdego modułu elementu rozmieszczenia zawartości lub dodać więcej modułów, aby uzyskać żądany układ.</span><span class="sxs-lookup"><span data-stu-id="4c054-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="4c054-165">Zaewidencjonuj stronę i opublikuj ją.</span><span class="sxs-lookup"><span data-stu-id="4c054-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c054-166">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="4c054-166">Additional resources</span></span>

[<span data-ttu-id="4c054-167">Omówienie zestawu początkowego</span><span class="sxs-lookup"><span data-stu-id="4c054-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4c054-168">Moduł alertów</span><span class="sxs-lookup"><span data-stu-id="4c054-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="4c054-169">Moduł karuzeli</span><span class="sxs-lookup"><span data-stu-id="4c054-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4c054-170">Moduł zaawansowanego bloku zawartości</span><span class="sxs-lookup"><span data-stu-id="4c054-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4c054-171">Moduł funkcji</span><span class="sxs-lookup"><span data-stu-id="4c054-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="4c054-172">Moduł bohatera</span><span class="sxs-lookup"><span data-stu-id="4c054-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="4c054-173">Moduł odtwarzacza wideo</span><span class="sxs-lookup"><span data-stu-id="4c054-173">Video player module</span></span>](add-video-player.md)