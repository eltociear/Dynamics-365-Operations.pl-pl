---
title: Omówienie zestawu początkowego
description: W tym temacie omówiono zestaw początkowy Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 73af7fc8845fe08bc4aa014abe4d8c6dcf7ccb7d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785267"
---
# <a name="starter-kit-overview"></a><span data-ttu-id="f267b-103">Omówienie zestawu początkowego</span><span class="sxs-lookup"><span data-stu-id="f267b-103">Starter kit overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f267b-104">W tym temacie omówiono zestaw początkowy Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f267b-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce starter kit.</span></span>

## <a name="overview"></a><span data-ttu-id="f267b-105">Omówienie</span><span class="sxs-lookup"><span data-stu-id="f267b-105">Overview</span></span>

<span data-ttu-id="f267b-106">Zestaw początkowy Dynamics 365 Commerce to zbiór modułów, za pomocą których można utworzyć witrynę sieci Web e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="f267b-106">The Dynamics 365 Commerce starter kit is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="f267b-107">Moduły mają aspekty interfejsu użytkownika (UI) i aspekty zachowania funkcjonalnego.</span><span class="sxs-lookup"><span data-stu-id="f267b-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="f267b-108">Motywy mogą być stosowane do modułów w początkowym zestawie, aby zmieniać ich wygląd i działanie.</span><span class="sxs-lookup"><span data-stu-id="f267b-108">Themes can be applied to the modules in the starter kit to change their look and feel.</span></span> <span data-ttu-id="f267b-109">W motywach używane są kaskadowe arkusze stylów (CSS).</span><span class="sxs-lookup"><span data-stu-id="f267b-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="f267b-110">Motyw fikcyjnej witryny e-Commerce o nazwie „Fabrikam” jest dostarczany jako część zestawu początkowego i może być używany jako odwołanie.</span><span class="sxs-lookup"><span data-stu-id="f267b-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the starter kit and can be used as a reference.</span></span>

## <a name="starter-kit-modules"></a><span data-ttu-id="f267b-111">Moduły zestawu początkowego</span><span class="sxs-lookup"><span data-stu-id="f267b-111">Starter kit modules</span></span>

<span data-ttu-id="f267b-112">W początkowym zestawie są dostępne następujące typy modułów:</span><span class="sxs-lookup"><span data-stu-id="f267b-112">The following types of modules are provided in the starter kit:</span></span>

- <span data-ttu-id="f267b-113">**Moduł kontenerów** — moduł kontenerowy jest prostym modułem działającym jako host dla innych modułów.</span><span class="sxs-lookup"><span data-stu-id="f267b-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="f267b-114">Steruje on układem modułów znajdujących się wewnątrz tego modułu.</span><span class="sxs-lookup"><span data-stu-id="f267b-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="f267b-115">**Moduły marketingowe** — moduły marketingowe: Hero, funkcja, Umieszczanie zawartości, przebudowana zawartość, odtwarzacz wideo i moduły karuzeli.</span><span class="sxs-lookup"><span data-stu-id="f267b-115">**Marketing modules** – Marketing modules include hero, feature, content placement, content rich block, video player, and carousel modules.</span></span> <span data-ttu-id="f267b-116">Wszystkie te moduły mogą być używane do poprezentacji zawartości.</span><span class="sxs-lookup"><span data-stu-id="f267b-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="f267b-117">Można je umieścić na dowolnej stronie i są sterowane danymi z systemu zarządzania treścią (CMS).</span><span class="sxs-lookup"><span data-stu-id="f267b-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="f267b-118">**Moduły nagłówka i stopki** — moduły nagłówka i stopki są wyświetlane w nagłówku i stopce wszystkich stron witryny.</span><span class="sxs-lookup"><span data-stu-id="f267b-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="f267b-119">Moduły te można skonfigurować zgodnie z wymaganiami właściwości.</span><span class="sxs-lookup"><span data-stu-id="f267b-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="f267b-120">**Moduły wyszukiwania** — produkty można wykrywać za pomocą modułu wyszukiwania w nagłówku.</span><span class="sxs-lookup"><span data-stu-id="f267b-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="f267b-121">Wyniki wyszukiwania zostaną wyświetlone na stronie wyników wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="f267b-121">Search results appear on the search results page.</span></span> <span data-ttu-id="f267b-122">Produkty można również wykryty na stronach kategorii, które są dedykowanymi stronami dla każdej kategorii obsługiwanej w hierarchii nawigacji kanału.</span><span class="sxs-lookup"><span data-stu-id="f267b-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="f267b-123">Ponadto moduły elementów uściślających mogą służyć do dalszego filtrowania wyników wyszukiwania i stron kategorii.</span><span class="sxs-lookup"><span data-stu-id="f267b-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="f267b-124">**Moduły strony Szczegóły produktu** — strony z informacjami o produktach używają kilku modułów do wyświetlania informacji o produktach.</span><span class="sxs-lookup"><span data-stu-id="f267b-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="f267b-125">Odbiorca modułu pola zakupu dla odbiorców umożliwia wyświetlenie produktów i dodanie ich do koszyka.</span><span class="sxs-lookup"><span data-stu-id="f267b-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="f267b-126">Inne moduły, takie jak moduł specyfikacji technicznej, zawierają szczegóły dotyczące produktu.</span><span class="sxs-lookup"><span data-stu-id="f267b-126">Other modules such, as the tech specs module, show the product details.</span></span> <span data-ttu-id="f267b-127">Moduł oceny i recenzje może służyć do wyświetlania i udostępniania recenzji.</span><span class="sxs-lookup"><span data-stu-id="f267b-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="f267b-128">**Kupowanie w trybie online w module sklep** — funkcja kupowania w trybie online w module sklep jest zintegrowana z mapami Bing.</span><span class="sxs-lookup"><span data-stu-id="f267b-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="f267b-129">Może służyć do wyszukiwania pobliskich sklepów, w których klienci mogą odbierać produkty nabyte przez nich.</span><span class="sxs-lookup"><span data-stu-id="f267b-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="f267b-130">**Moduły zakupu** — moduły zakupów zawierają moduł koszyka, który może być używany do dodawania towarów do koszyka.</span><span class="sxs-lookup"><span data-stu-id="f267b-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="f267b-131">Moduł realizacji transakcji zawiera adres wysyłkowy, opcje dostarczania oraz informacje o kartach upominkowych, programie lojalnościowym i karcie kredytowej, dzięki czemu można je przetwarzać.</span><span class="sxs-lookup"><span data-stu-id="f267b-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="f267b-132">Po złożeniu zamówienia moduł potwierdzający zamówienie może być używany do wyświetlania szczegółów potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="f267b-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="f267b-133">**Moduły zarządzania kontami** — odbiorcy mogą zalogować się do istniejącego konta, a moduł zapisywania się pozwala im utworzyć nowe konto.</span><span class="sxs-lookup"><span data-stu-id="f267b-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="f267b-134">Po utworzeniu konta można użyć modułu historii zamówień w celu wyświetlenia ostatnich zamówień, a moduł szczegóły zamówienia może służyć do wyświetlania szczegółów zamówienia.</span><span class="sxs-lookup"><span data-stu-id="f267b-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="f267b-135">**Moduł rekomendacji** — rekomendacje są wyświetlane za pomocą modułu umieszczanie produktu.</span><span class="sxs-lookup"><span data-stu-id="f267b-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="f267b-136">Moduł ten obsługuje listy algorytmowe i redakcyjne, które można prezentować na dowolnej stronie.</span><span class="sxs-lookup"><span data-stu-id="f267b-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f267b-137">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="f267b-137">Additional resources</span></span>

[<span data-ttu-id="f267b-138">Moduł kontenera</span><span class="sxs-lookup"><span data-stu-id="f267b-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f267b-139">Moduł pola zakupu</span><span class="sxs-lookup"><span data-stu-id="f267b-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f267b-140">Moduł koszyka</span><span class="sxs-lookup"><span data-stu-id="f267b-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f267b-141">Moduł realizacji transakcji</span><span class="sxs-lookup"><span data-stu-id="f267b-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f267b-142">Moduł potwierdzenia zamówienia</span><span class="sxs-lookup"><span data-stu-id="f267b-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f267b-143">Moduł nagłówka</span><span class="sxs-lookup"><span data-stu-id="f267b-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f267b-144">Moduł stopki</span><span class="sxs-lookup"><span data-stu-id="f267b-144">Footer module</span></span>](author-footer-module.md)