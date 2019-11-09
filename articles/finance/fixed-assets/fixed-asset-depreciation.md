---
title: Amortyzacja środka trwałego
description: Ten temat zawiera omówienie mechanizmu amortyzacji środków trwałych.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1056dadab4294072cc064670f5cfcda239e22e19
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179391"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="5fe62-103">Amortyzacja środka trwałego</span><span class="sxs-lookup"><span data-stu-id="5fe62-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fe62-104">Ten temat zawiera omówienie mechanizmu amortyzacji środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="5fe62-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="5fe62-105">Amortyzacja jest okresową transakcją, która zwykle zmniejsza wartość środka trwałego w bilansie i jest naliczana jako wydatek na koncie wynikowym.</span><span class="sxs-lookup"><span data-stu-id="5fe62-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="5fe62-106">Dlatego do uznawania okresowej amortyzacji w bilansie jest zazwyczaj używane konto główne.</span><span class="sxs-lookup"><span data-stu-id="5fe62-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="5fe62-107">Konto przeciwstawne to konto w części wynikowej planu kont.</span><span class="sxs-lookup"><span data-stu-id="5fe62-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="5fe62-108">Korekta amortyzacji</span><span class="sxs-lookup"><span data-stu-id="5fe62-108">Depreciation adjustment</span></span>
<span data-ttu-id="5fe62-109">Zwykle tylko korekta do już zaksięgowanej transakcji amortyzacji jest księgowana jako korekta amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fe62-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="5fe62-110">Dlatego też zarówno konto główne, jak i konto przeciwstawne są konfigurowane w ten sam sposób, co konta amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fe62-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="5fe62-111">Korekta amortyzacji może być kwotą dodatnią lub ujemną, ale funkcjonalność konta głównego (jako konta bilansowego) oraz konta przeciwstawnego (zazwyczaj jako konta wynikowego) pozostaje taka sama.</span><span class="sxs-lookup"><span data-stu-id="5fe62-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="5fe62-112">Amortyzacja dodatkowa</span><span class="sxs-lookup"><span data-stu-id="5fe62-112">Extraordinary depreciation</span></span>
<span data-ttu-id="5fe62-113">Amortyzacja dodatkowa działa jak amortyzacja podstawowa.</span><span class="sxs-lookup"><span data-stu-id="5fe62-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="5fe62-114">W związku z tym konto główne jest używane do uznawania kwoty amortyzacji w bilansie i zmniejszania wartości środka trwałego.</span><span class="sxs-lookup"><span data-stu-id="5fe62-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="5fe62-115">Konto przeciwstawne jest kontem wynikowym, na którym obliczana jest amortyzacja dla okresu obrachunkowego i jest naliczana jako wydatek.</span><span class="sxs-lookup"><span data-stu-id="5fe62-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="5fe62-116">Amortyzacja dodatkowa działa niezależnie od amortyzacji podstawowej.</span><span class="sxs-lookup"><span data-stu-id="5fe62-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="5fe62-117">Gdy amortyzacja dodatkowa jest osobnym typem transakcji, możliwe jest księgowanie i raportowanie amortyzacji dodatkowej oddzielnie od zwykłej amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fe62-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="5fe62-118">Specjalny odpis amortyzacyjny</span><span class="sxs-lookup"><span data-stu-id="5fe62-118">Special depreciation allowance</span></span>
<span data-ttu-id="5fe62-119">Specjalny odpis amortyzacyjny pozwala na uzyskiwanie większych kwot amortyzacji podczas pierwszego roku użytkowania i amortyzowania składnika aktywów.</span><span class="sxs-lookup"><span data-stu-id="5fe62-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="5fe62-120">Specjalne odpisy amortyzacyjne należy wykonać przed wszelkimi innymi obliczeniami amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fe62-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="5fe62-121">Specjalne odpisy amortyzacyjny są często znane dopiero na późniejszych etapach użytkowania środka trwałego, dlatego najlepiej używać tego typu amortyzacji z księgą, której zapisy nie są księgowane w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="5fe62-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="5fe62-122">Można użyć funkcji okresowej Usuwanie transakcji, które nie zostały zaksięgowane w księdze głównej, aby usunąć historię transakcji dla tych ksiąg.</span><span class="sxs-lookup"><span data-stu-id="5fe62-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="5fe62-123">Można wówczas usunąć historię amortyzacji dla księgi środków trwałych, zaksięgować specjalny odpis amortyzacyjny, gdy jest znany, a następnie zaksięgować pozostałe transakcje amortyzacji dla roku.</span><span class="sxs-lookup"><span data-stu-id="5fe62-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="5fe62-124">Można utworzyć nieograniczoną liczbę rekordów specjalnego odpisu amortyzacyjnego.</span><span class="sxs-lookup"><span data-stu-id="5fe62-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="5fe62-125">Po przypisaniu tych rekordów do księgi grupy środków trwałych zostaną one zastosowane do księgi środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="5fe62-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="5fe62-126">Specjalny odpis amortyzacyjny jest wprowadzany jako wartość procentowa lub jako stała kwota.</span><span class="sxs-lookup"><span data-stu-id="5fe62-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="5fe62-127">Przy księgowaniu propozycji amortyzacji transakcje specjalnego odpisu amortyzacyjnego są księgowane w księdze jako transakcje oddzielne od transakcji amortyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fe62-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="5fe62-128"> Kalendarze amortyzacji</span><span class="sxs-lookup"><span data-stu-id="5fe62-128">Depreciation calendars</span></span>
<span data-ttu-id="5fe62-129">Każda księga ma kalendarz, który jest używany podczas amortyzowania środków trwałych.</span><span class="sxs-lookup"><span data-stu-id="5fe62-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="5fe62-130">Domyślnie jeśli nie wskażesz kalendarza w księdze, będzie ona używać kalendarza obrachunkowego księgi.</span><span class="sxs-lookup"><span data-stu-id="5fe62-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="5fe62-131">Gdy profil amortyzacji skojarzony z księgą korzysta z amortyzacji w roku obrachunkowym, należy wybrać kalendarz obrachunkowy dla księgi.</span><span class="sxs-lookup"><span data-stu-id="5fe62-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="5fe62-132">Można tworzyć udostępnione kalendarze przy użyciu strony **Kalendarze obrachunkowe** w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="5fe62-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="5fe62-133">Aby uzyskać więcej informacji, zobacz [Metody i konwencje amortyzacji](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="5fe62-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>


