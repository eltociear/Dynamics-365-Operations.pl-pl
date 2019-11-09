---
title: Specyfikacja podatku wg transakcji księgi raport
description: W tym temacie objaśniono sposób używania raportu Specyfikacja podatku przez Raport transakcji księgi do wyświetlania i drukowania informacji o transakcjach księgi, dla których jest obliczany podatek
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c36d9f8fb81a0a7e7a6de3db48cebdcf9d13b2d
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/14/2019
ms.locfileid: "2591201"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="f2b1e-103">Specyfikacja podatku wg transakcji księgi raport</span><span class="sxs-lookup"><span data-stu-id="f2b1e-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2b1e-104">W tym temacie objaśniono sposób używania raportu **Specyfikacja podatku przez transakcje księgi** do wyświetlania i drukowania informacji o transakcjach księgi, dla których jest obliczany podatek</span><span class="sxs-lookup"><span data-stu-id="f2b1e-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="f2b1e-105">Konta podatkowe a konta niepodatkowe</span><span class="sxs-lookup"><span data-stu-id="f2b1e-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="f2b1e-106">W raporcie **Specyfikacja podatku wg transakcji księgi** są wyświetlane transakcje podatkowe dla kont podatkowych i kont innych niż podatki.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="f2b1e-107">Te konta są klasyfikowane w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="f2b1e-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="f2b1e-108">**Konto podatkowe** — konto jest traktowane jako konto podatkowe podczas księgowania transakcji podatkowej, a konto główne w wierszu arkusza **podatkowego** jest kontem podatkowym, takim jak konto podatku należnego lub konto podatku należnego</span><span class="sxs-lookup"><span data-stu-id="f2b1e-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="f2b1e-109">**Konto niepodatkowe** — konto jest traktowane jako konto niepodatkowe podczas księgowania transakcji podatkowej, a konto główne w wierszu arkusza podatkowego jest kontem niepodatkowym, takim jak konto przychodu lub konto wydatków.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="f2b1e-110">Dla kont podatku, kolumny **pochodzenie**, **podatek należny** i **podatek naliczony** w raporcie są wyświetlane **0** (zero)</span><span class="sxs-lookup"><span data-stu-id="f2b1e-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="f2b1e-111">W przypadku kont niepodatkowych kolumny te zawierają kwoty.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="f2b1e-112">filtrowane dane wyświetlane w raporcie,</span><span class="sxs-lookup"><span data-stu-id="f2b1e-112">Filtering the data on the report</span></span>

<span data-ttu-id="f2b1e-113">Podczas generowania tego raportu, wyświetlane są następujące pola domyślne.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="f2b1e-114">Możesz używać tych pól filtrowania danych, które będą wyświetlane w raporcie.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="f2b1e-115">Pole</span><span class="sxs-lookup"><span data-stu-id="f2b1e-115">Field</span></span>                      | <span data-ttu-id="f2b1e-116">Opis</span><span class="sxs-lookup"><span data-stu-id="f2b1e-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="f2b1e-117">Data</span><span class="sxs-lookup"><span data-stu-id="f2b1e-117">Date</span></span>                       | <span data-ttu-id="f2b1e-118">Pola w sekcji **od** i **do** służą do definiowania zakresu dat dla transakcji podatkowych.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="f2b1e-119">Konto główne</span><span class="sxs-lookup"><span data-stu-id="f2b1e-119">Main account</span></span>               | <span data-ttu-id="f2b1e-120">Pola w sekcji **od** i **do** służą do definiowania zakresu dat dla kont głównych.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="f2b1e-121">Kod podatku</span><span class="sxs-lookup"><span data-stu-id="f2b1e-121">Sales tax code</span></span>             | <span data-ttu-id="f2b1e-122">Pola w sekcji **od** i **do** służą do definiowania zakresu dat dla kodów podatków.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="f2b1e-123">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="f2b1e-123">Grouping</span></span>                   | <span data-ttu-id="f2b1e-124">Umożliwia określenie, czy raport powinien być pogrupowany według kont księgowych czy kodów podatków.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="f2b1e-125">Suma częściowa wg kodu podatku</span><span class="sxs-lookup"><span data-stu-id="f2b1e-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="f2b1e-126">Ustawienie tej opcji na **tak** powoduje wyświetlanie sum częściowych według kodu podatku.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="f2b1e-127">Tylko sumy</span><span class="sxs-lookup"><span data-stu-id="f2b1e-127">Totals only</span></span>                | <span data-ttu-id="f2b1e-128">Tę opcję należy wybrać **tak**, aby były wyświetlane tylko sumy całkowite.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="f2b1e-129">Tylko konta główne</span><span class="sxs-lookup"><span data-stu-id="f2b1e-129">Main accounts only</span></span>         | <span data-ttu-id="f2b1e-130">Ustawienie tej opcji na **tak** powoduje uwzględnienie tylko kont głównych w raporcie.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="f2b1e-131">Wyświetlanie w raporcie tylko kont niepodlegających opodatkowaniu</span><span class="sxs-lookup"><span data-stu-id="f2b1e-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="f2b1e-132">Aby w raporcie były wyświetlane tylko konta niepodatkowe, należy skonfigurować warunek filtru, taki jak gwiazdka (\*), co pokazano na poniższej ilustracji.</span><span class="sxs-lookup"><span data-stu-id="f2b1e-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Raport przedstawiający konta niepodatkowe](media/taxspecperledgertrans.png)