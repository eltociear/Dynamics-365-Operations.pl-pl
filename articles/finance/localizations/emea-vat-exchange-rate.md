---
title: Podstawowe informacje o kursie wymiany dla podatku VAT
description: Ten temat zawiera informacje dotyczące kursów wymiany dla obliczania podatku VAT. Kurs wymiany używany do obliczania podatku VAT może się różnić od kursu wymiany używanego w funkcjach księgowania w firmie. Po zaksięgowaniu dokumentu w walucie obcej wszelkie występujące różnice kursowe są księgowane na określonych kontach księgowych.
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateCurrencyPairCalculationRules, LedgerParameters, SalesTaxExchangeRateType, TaxTmpWorkTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 272703
ms.assetid: 2d1fad67-8234-49cc-b009-0f3cc29f5886
ms.search.region: Czech Republic, Hungary, Poland
ms.author: mrolecki
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7e23581c73c3eb62e21dc3a53b5730c7c7cb0e62
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175165"
---
# <a name="vat-exchange-rate-overview"></a><span data-ttu-id="cd989-105">Podstawowe informacje o kursie wymiany dla podatku VAT</span><span class="sxs-lookup"><span data-stu-id="cd989-105">VAT exchange rate overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd989-106">Ten temat zawiera informacje dotyczące kursów wymiany dla obliczania podatku VAT.</span><span class="sxs-lookup"><span data-stu-id="cd989-106">This topic provides information about exchange rates for the VAT calculation.</span></span> <span data-ttu-id="cd989-107">Kurs wymiany używany do obliczania podatku VAT może się różnić od kursu wymiany używanego w funkcjach księgowania w firmie.</span><span class="sxs-lookup"><span data-stu-id="cd989-107">The exchange rate that is used for VAT calculation can differ from the exchange rate that is used for company accounting functions.</span></span> <span data-ttu-id="cd989-108">Po zaksięgowaniu dokumentu w walucie obcej wszelkie występujące różnice kursowe są księgowane na określonych kontach księgowych.</span><span class="sxs-lookup"><span data-stu-id="cd989-108">When a document in a foreign currency is posted, any exchange rate differences that occur are posted to specific ledger accounts.</span></span>

<span data-ttu-id="cd989-109">Organizacja może wybrać kurs wymiany, który służy do obliczania podatku od towarów i usług (VAT) dla deklaracji VAT.</span><span class="sxs-lookup"><span data-stu-id="cd989-109">Your organization can select the exchange rate that it uses to calculate value-added tax (VAT) for VAT statements.</span></span> <span data-ttu-id="cd989-110">Ten kurs wymiany może się różnić od kursu wymiany używanego w funkcjach księgowania w firmie.</span><span class="sxs-lookup"><span data-stu-id="cd989-110">This exchange rate can differ from the exchange rate that your organization uses for company accounting functions.</span></span> <span data-ttu-id="cd989-111">Funkcje księgowania obejmują m.in. przygotowywanie następujących dokumentów związanych z podatkami:</span><span class="sxs-lookup"><span data-stu-id="cd989-111">Accounting functions include the preparation of the following tax-related documents:</span></span>

-   <span data-ttu-id="cd989-112">Faktury</span><span class="sxs-lookup"><span data-stu-id="cd989-112">Invoices</span></span>
-   <span data-ttu-id="cd989-113">Faktury niezależne</span><span class="sxs-lookup"><span data-stu-id="cd989-113">Free text invoices</span></span>
-   <span data-ttu-id="cd989-114">Zamówienia zakupu</span><span class="sxs-lookup"><span data-stu-id="cd989-114">Purchase orders</span></span>
-   <span data-ttu-id="cd989-115">Faktury projektu</span><span class="sxs-lookup"><span data-stu-id="cd989-115">Project invoices</span></span>
-   <span data-ttu-id="cd989-116">Faktury korygujące</span><span class="sxs-lookup"><span data-stu-id="cd989-116">Credit notes</span></span>
-   <span data-ttu-id="cd989-117">Faktury korygujące</span><span class="sxs-lookup"><span data-stu-id="cd989-117">Corrective invoices</span></span>

<span data-ttu-id="cd989-118">Po zaksięgowaniu dokumentu w walucie obcej wszelkie występujące różnice kursowe są księgowane na określonych kontach księgowych.</span><span class="sxs-lookup"><span data-stu-id="cd989-118">When you post a document that uses a foreign currency, any exchange rate differences that occur are posted to specific ledger accounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd989-119">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="cd989-119">Prerequisites</span></span>

<span data-ttu-id="cd989-120">Aby korzystać z ten funkcjonalności, należy odpowiednio skonfigurować system.</span><span class="sxs-lookup"><span data-stu-id="cd989-120">Before you can use this functionality, you must configure the system.</span></span>

1.  <span data-ttu-id="cd989-121">Utwórz typy kursów wymiany i ustaw kursy wymiany dla podatku w oknie **Księga główna** &gt; **Waluty** &gt; **Typy kursu wymiany**.</span><span class="sxs-lookup"><span data-stu-id="cd989-121">Create exchange rate types and set up exchange rates for the sales tax at **General ledger** &gt; **Currencies** &gt; **Exchange rate types**.</span></span> <span data-ttu-id="cd989-122">Można zdefiniować dowolną liczbę typów kursu wymiany i dowolną liczbę kursów wymiany dla par walut.</span><span class="sxs-lookup"><span data-stu-id="cd989-122">You can define as many exchange rate types and as many exchange rates for pairs of currencies as you require.</span></span>
2.  <span data-ttu-id="cd989-123">Włącz obliczanie kursów wymiany dla podatku VAT, włączając parametr **Kurs banku** oraz definiując typy kursów wymiany dla podatków naliczonego i należnego w oknie **Księga główna** &gt; **Ustawienia księgi** &gt; **Parametry księgi głównej**.</span><span class="sxs-lookup"><span data-stu-id="cd989-123">Enable the calculation of VAT exchange rates by turning on the **Bank exchange rate** parameter, and by defining sales tax receivable and sales tax payable exchange rate types, at **General ledger** &gt; **Ledger setup** &gt; **General ledger parameters**.</span></span>
3.  <span data-ttu-id="cd989-124">Skonfiguruj typy kursów wymiany walut dla określonych typów transakcji sprzedaży i zakupu w oknie **Księga główna** &gt; **Waluty** &gt; **Typy kursów wymiany walut dla podatku**.</span><span class="sxs-lookup"><span data-stu-id="cd989-124">Set up currency exchange rate types for specific sales and purchase transaction types at **General ledger** &gt; **Currencies** &gt; **Currency exchange rate types for sales tax**.</span></span>
4.  <span data-ttu-id="cd989-125">Skonfiguruj konta różnic podatków naliczonego i należnego oraz konta przeciwstawne tych różnic w grupach księgowania w księdze w oknie **Podatek** &gt; **Ustawienia** &gt; **Podatek** &gt; **Grupy księgowania**.</span><span class="sxs-lookup"><span data-stu-id="cd989-125">Set up sales tax receivable and sales tax payable difference and difference offset accounts in the ledger posting groups at **Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Ledger posting groups**.</span></span>
5.  <span data-ttu-id="cd989-126">Opcjonalnie: Skonfiguruj regułę obliczania kursu wymiany dla pary walut w oknie **Księga główna** &gt; **Waluty** &gt; **Zasady obliczania kursu wymiany dla par walut**.</span><span class="sxs-lookup"><span data-stu-id="cd989-126">Optional: Set up an exchange rate calculation rule for a currency pair at **General ledger** &gt; **Currencies** &gt; **Exchange rate calculation rules for currency pairs**.</span></span> <span data-ttu-id="cd989-127">Zasady obliczania kursu wymiany są używane do przeliczania kwot podatku VAT na fakturach sprzedaży w walucie obcej na kwoty podatku VAT w walucie docelowej.</span><span class="sxs-lookup"><span data-stu-id="cd989-127">The exchange rate calculation rules are used to convert VAT amounts for foreign currency sales invoices to VAT amounts in a destination currency.</span></span>

## <a name="overview"></a><span data-ttu-id="cd989-128">Przegląd</span><span class="sxs-lookup"><span data-stu-id="cd989-128">Overview</span></span>

<span data-ttu-id="cd989-129">Jeśli po skonfigurowaniu w systemie używania kursów wymiany dla podatku VAT trzeba wprowadzić dokument lub utworzyć zamówienie wykorzystujące walutę obcą, można użyć strony **Transakcje podatkowe**, aby ustawić wartość **Data rejestru VAT**, która będzie powodowała pobieranie i ustawianie domyślnej wartości **Kurs wymiany podatku**.</span><span class="sxs-lookup"><span data-stu-id="cd989-129">After you've configured the system to use VAT exchange rates, if you must enter a document or create an order that uses a foreign currency, you can use **Sales tax transactions** page to set the **Date of VAT register** value to pick up and set the default **Sales tax exchange rate** value.</span></span> <span data-ttu-id="cd989-130">Oba pola można edytować.</span><span class="sxs-lookup"><span data-stu-id="cd989-130">You can edit both fields.</span></span> <span data-ttu-id="cd989-131">Można również użyć pola **Podstawa po korekcie (kurs wymiany dla podatku VAT)** lub **Skorygowana kwota podatku (kurs wymiany dla podatku VAT)**, aby wprowadzić rzeczywiste kwoty podatku VAT w walucie lokalnej określonej w dokumencie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="cd989-131">You can also use the **Adjusted amount origin (VAT exchange rate)** or **Adjusted sales tax amount (VAT exchange rate)** field to enter actual VAT amounts in the local currency that is stated in an external document.</span></span> <span data-ttu-id="cd989-132">Przeglądając zapisy rachunkowe, można wyświetlać różnice kwot podatku na stronie **Arkusz księgi podrzędnej**.</span><span class="sxs-lookup"><span data-stu-id="cd989-132">When you review the accounting, you can view sales tax difference amounts on the **Subledger journal** page.</span></span> <span data-ttu-id="cd989-133">Gdy dokument jest księgowany, dla transakcji księgowanych na skonfigurowanych przez Ciebie kontach księgi głównej możesz przeglądać wszelkie różnice w kwotach podatku spowodowane różnicami między kursem wymiany waluty dla podatku VAT a kursem wymiany waluty rozliczeniowej używanej w organizacji.</span><span class="sxs-lookup"><span data-stu-id="cd989-133">When a document is posted, for transactions that are posted to the general ledger accounts that you've configured, you can view any differences in sales tax amounts that are caused by the difference between the VAT currency exchange rate and the accounting currency exchange rate for your organization.</span></span>



