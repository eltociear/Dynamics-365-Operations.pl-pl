---
title: Rekomendacje produktów w punkcie sprzedaży
description: W tym temacie opisano sposób korzystania z rekomendacji dotyczących produktów na urządzeniu punktu sprzedaży (POS).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278394"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="c51ee-103">Rekomendacje produktów w punkcie sprzedaży</span><span class="sxs-lookup"><span data-stu-id="c51ee-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c51ee-104">Istotnie, rekomendacje produktów są aplikacją zmieniającą biznes obejmującą wszystkie obszary sprzedaży detalicznej w celu tworzenia bogatych, atrakcyjnych i dostosowanych rozwiązań do wykrywania produktów.</span><span class="sxs-lookup"><span data-stu-id="c51ee-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="c51ee-105">Aby zaimplementować tę funkcję w punkcie sprzedaży, należy wykonać kroki [procedury dodawania zaleceń do urządzeń punktu sprzedaży.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="c51ee-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="c51ee-106">Aby uzyskać więcej informacji na temat zaleceń dotyczących funkcji rekomendacji, zapoznaj się z [przeglądem rekomendacji produktu.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="c51ee-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="c51ee-107">Scenariusze</span><span class="sxs-lookup"><span data-stu-id="c51ee-107">Scenarios</span></span>

<span data-ttu-id="c51ee-108">Rekomendacje produktów działają w opisanych niżej scenariuszach w punkcie sprzedaż.</span><span class="sxs-lookup"><span data-stu-id="c51ee-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="c51ee-109">Są dostępne dla aplikacji Cloud POS i Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="c51ee-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="c51ee-110">Na stronie **Szczegóły produktu**:</span><span class="sxs-lookup"><span data-stu-id="c51ee-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="c51ee-111">• Jeśli pracownik sklepu otworzy stronę **Szczegóły produktu** podczas oglądania wcześniejszych transakcji w różnych kanałach, usługa rekomendacji proponuje dodatkowe towary, które inni odbiorcy często kupowali razem z analizowanym produktem.</span><span class="sxs-lookup"><span data-stu-id="c51ee-111">• If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="c51ee-112">[![Rekomendacje na stronie Szczegóły produktu](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="c51ee-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="c51ee-113">Na stronie **Transakcja**:</span><span class="sxs-lookup"><span data-stu-id="c51ee-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="c51ee-114">• Zalecane jest, aby aparat rekomendacji sugerował pozycje na podstawie całej listy towarów w koszyku, które są często kupowane razem</span><span class="sxs-lookup"><span data-stu-id="c51ee-114">• The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c51ee-115">Aby rekomendacje były wyświetlane na stronie **Transakcja**, sprzedawca detaliczny musi zaktualizować układ ekranu w programie Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c51ee-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="c51ee-116">Formant **Zalecenia** należy upuścić na stronę **Transakcja**.</span><span class="sxs-lookup"><span data-stu-id="c51ee-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="c51ee-117">[![Rekomendacje na stronie Transakcja](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="c51ee-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="c51ee-118">Konfigurowanie Dynamics 365 Retail do obsługi rekomendacji POS</span><span class="sxs-lookup"><span data-stu-id="c51ee-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="c51ee-119">Aby skonfigurować rekomendacje produktu, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="c51ee-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="c51ee-120">Upewnij się, że usługa została zaktualizowana do **kompilacji 10.0.6.**</span><span class="sxs-lookup"><span data-stu-id="c51ee-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="c51ee-121">Postępuj zgodnie z instrukcjami dotyczącymi sposobu [włączania rekomendacji produktu](../commerce/enable-product-recommendations.md) w firmie.</span><span class="sxs-lookup"><span data-stu-id="c51ee-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="c51ee-122">Opcjonalnie: Aby wyświetlać rekomendacje na ekranie transakcji, przejdź do okna **Układ ekranu**, wybierz układ ekranu, uruchom narzędzie **Projektant układu ekranu**, a następnie upuść formant **rekomendacji** w żądanym miejscu.</span><span class="sxs-lookup"><span data-stu-id="c51ee-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="c51ee-123">Przejdź do okna **Parametry sieci sprzedaży**, wybierz opcję **Uczenie maszynowe** i w ustawieniu **Włącz rekomendacje w punkcie sprzedaży** wybierz wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="c51ee-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="c51ee-124">Aby rekomendacje były wyświetlane w punkcie sprzedaży, uruchom zadanie konfiguracji globalnej **1110**.</span><span class="sxs-lookup"><span data-stu-id="c51ee-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="c51ee-125">Aby pokazywać zmiany wprowadzone w projektancie układu ekranu punktu sprzedaży, uruchom zadanie konfiguracji kanału **1070**.</span><span class="sxs-lookup"><span data-stu-id="c51ee-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="c51ee-126">Rozwiązywanie problemów, jeśli już włączono funkcję Rekomendacje produktów</span><span class="sxs-lookup"><span data-stu-id="c51ee-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="c51ee-127">Wybierz kolejno opcje **Parametry sieci sprzedaży** \> **Listy rekomendacji** \> **Wyłącz rekomendacje produktów** i uruchom **Żądanie konfiguracji globalnej \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="c51ee-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="c51ee-128">Jeśli za pomocą **Projektanta układu ekranu** dodano **kontrolkę rekomendacji** do ekranu transakcji, usuń również ją.</span><span class="sxs-lookup"><span data-stu-id="c51ee-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="c51ee-129">Jeśli masz dodatkowe pytania, zapoznaj się z [Rekomendacje - Często zadawane pytania](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c51ee-129">If you have additional questions, check out the [Recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c51ee-130">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="c51ee-130">Additional resources</span></span>

<span data-ttu-id="c51ee-131">[Dodawanie formantu rekomendacji na stronę transakcji urządzenia POS](add-recommendations-control-pos-screen.md)
[Przegląd rekomendacji produktu](../commerce/product-recommendations.md)
[Włączanie rekomendacji dotyczących produktów](../commerce/enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="c51ee-131">[Add a recommendations control to the transaction page on a POS device](add-recommendations-control-pos-screen.md)
[Product recommendations overview](../commerce/product-recommendations.md)
[Enable product recommendations](../commerce/enable-product-recommendations.md)</span></span> 