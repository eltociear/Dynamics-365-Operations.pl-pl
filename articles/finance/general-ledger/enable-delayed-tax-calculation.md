---
title: Włączanie opóźnionego obliczania podatku w arkuszach
description: W tym temacie objaśniono sposób włączania funkcji opóźnionego obliczania podatku w celu zwiększenia wydajności obliczeń podatku, gdy liczba wierszy arkusza jest duża.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: e336be5468106007e1f5adf26bf272c88b8b413b
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2623528"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="68588-103">Włączanie opóźnionego obliczania podatku w arkuszach</span><span class="sxs-lookup"><span data-stu-id="68588-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="68588-104">W tym temacie wyjaśniono, w jaki sposób można opóźnić obliczanie podatku w arkuszach.</span><span class="sxs-lookup"><span data-stu-id="68588-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="68588-105">Dzięki tej funkcji można poprawić wydajność obliczeń podatku, gdy istnieje wiele wierszy arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="68588-106">Domyślnie kwoty podatku w wierszach arkusza są obliczane po każdej aktualizacji pól związanych z podatkiem.</span><span class="sxs-lookup"><span data-stu-id="68588-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="68588-107">Pola te obejmują pola dotyczące grup podatków i grup podatków dla pozycji.</span><span class="sxs-lookup"><span data-stu-id="68588-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="68588-108">Każda aktualizacja wiersza arkusza powoduje ponowne obliczenie kwot podatku dla wszystkich wierszy arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="68588-109">Chociaż to zachowanie pomaga użytkownikowi widzieć kwoty podatku obliczone w czasie rzeczywistym, może również wpływać na wydajność, jeśli liczba wierszy arkusza jest bardzo duża.</span><span class="sxs-lookup"><span data-stu-id="68588-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="68588-110">Funkcja opóźnionego obliczania podatku pozwala opóźnić obliczanie podatku w arkuszach, co ułatwia rozwiązywanie problemów z wydajnością.</span><span class="sxs-lookup"><span data-stu-id="68588-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="68588-111">Gdy ta funkcja jest włączona, kwoty podatku będą obliczane tylko wtedy, gdy użytkownik wybierze pozycję **Podatek** lub zaksięguje arkusz.</span><span class="sxs-lookup"><span data-stu-id="68588-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="68588-112">Obliczanie podatku można opóźnić na trzech poziomach:</span><span class="sxs-lookup"><span data-stu-id="68588-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="68588-113">Firma</span><span class="sxs-lookup"><span data-stu-id="68588-113">Legal entity</span></span>
- <span data-ttu-id="68588-114">Nazwa arkusza</span><span class="sxs-lookup"><span data-stu-id="68588-114">Journal name</span></span>
- <span data-ttu-id="68588-115">Nagłówek arkusza</span><span class="sxs-lookup"><span data-stu-id="68588-115">Journal header</span></span>

<span data-ttu-id="68588-116">System nadaje priorytet ustawieniu dla nagłówka arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="68588-117">Domyślnie to ustawienie jest pobierane z nazwy arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="68588-118">Domyślnie ustawienie dla nazwy arkusza jest pobierane z ustawienia na stronie **Parametry księgi głównej** podczas tworzenia nazwy arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="68588-119">W poniższych sekcjach przedstawiono sposób włączania opóźnionego obliczania podatku dla firm, nazw arkuszy i nagłówków arkuszy.</span><span class="sxs-lookup"><span data-stu-id="68588-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="68588-120">Włączanie opóźnionego obliczania podatku na poziomie firmy</span><span class="sxs-lookup"><span data-stu-id="68588-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="68588-121">Przejdź do pozycji **Księga główna \> Ustawienia księgi \> Parametry księgi głównej**.</span><span class="sxs-lookup"><span data-stu-id="68588-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="68588-122">Na karcie **Podatek**, na skróconej karcie **Ogólne** ustaw opcję **Obliczanie podatku opóźnionego** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="68588-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obraz parametrów księgi głównej](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="68588-124">Włączanie opóźnionego obliczania podatku na poziomie nazwy arkusza</span><span class="sxs-lookup"><span data-stu-id="68588-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="68588-125">Przejdź do pozycji **Księga główna \> Konfiguracja arkusza \> Nazwy arkuszy**.</span><span class="sxs-lookup"><span data-stu-id="68588-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="68588-126">Na skróconej karcie **Ogólne**, w sekcji **Podatek** ustaw opcję **Obliczanie podatku opóźnionego** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="68588-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obraz nazw arkusza](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="68588-128">Włączanie opóźnionego obliczania podatku na poziomie nagłówka arkusza</span><span class="sxs-lookup"><span data-stu-id="68588-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="68588-129">Przejdź do pozycji **Księga główna \> Wpisy w arkuszu \> Arkusze finansowe**.</span><span class="sxs-lookup"><span data-stu-id="68588-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="68588-130">Wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="68588-130">Select **New**.</span></span>
3. <span data-ttu-id="68588-131">Wybierz nazwę arkusza.</span><span class="sxs-lookup"><span data-stu-id="68588-131">Select a journal name.</span></span>
4. <span data-ttu-id="68588-132">Na karcie **Ustawienia** ustaw opcję **Obliczanie podatku opóźnionego** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="68588-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obraz strony arkusza finansowego](media/delayed-tax-calculation-journal-header.png)