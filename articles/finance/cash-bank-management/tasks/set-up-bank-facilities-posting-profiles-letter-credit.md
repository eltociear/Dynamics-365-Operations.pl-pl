---
title: Konfigurowanie instrumentów bankowych i profilów księgowania dla akredytyw
description: Ta procedura prowadzi przez proces tworzenia instrumentu bankowego i profilu księgowania wymaganych do przetwarzania akredytyw.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3d35bd265ad31da083d2437fae886569766085
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188080"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="9e2de-103">Konfigurowanie instrumentów bankowych i profilów księgowania dla akredytyw</span><span class="sxs-lookup"><span data-stu-id="9e2de-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e2de-104">Ta procedura prowadzi przez proces tworzenia instrumentu bankowego i profilu księgowania wymaganych do przetwarzania akredytyw.</span><span class="sxs-lookup"><span data-stu-id="9e2de-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="9e2de-105">Zadania wykorzystują firmę demonstracyjną „USMF”.</span><span class="sxs-lookup"><span data-stu-id="9e2de-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="9e2de-106">Parametr księgi głównej</span><span class="sxs-lookup"><span data-stu-id="9e2de-106">General ledger parameter</span></span>
1. <span data-ttu-id="9e2de-107">Wybierz kolejno opcje Zarządzanie gotówką i bankami > Ustawienia > Parametry modułu Zarządzanie gotówką i bankami.</span><span class="sxs-lookup"><span data-stu-id="9e2de-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="9e2de-108">Rozwiń sekcję Dokument bankowy.</span><span class="sxs-lookup"><span data-stu-id="9e2de-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="9e2de-109">Zaznacz opcję Włączenie akredytywy importowej.</span><span class="sxs-lookup"><span data-stu-id="9e2de-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="9e2de-110">Zaznacz opcję Włączenie akredytywy eksportowej.</span><span class="sxs-lookup"><span data-stu-id="9e2de-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="9e2de-111">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9e2de-111">Click Save.</span></span>
6. <span data-ttu-id="9e2de-112">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9e2de-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="9e2de-113">Tworzenie instrumentu bankowego</span><span class="sxs-lookup"><span data-stu-id="9e2de-113">Create Bank facility</span></span>
1. <span data-ttu-id="9e2de-114">Wybierz kolejno opcje Zarządzanie gotówką i bankami > Ustawienia > Instrumenty bankowe.</span><span class="sxs-lookup"><span data-stu-id="9e2de-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="9e2de-115">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="9e2de-115">Click New.</span></span>
3. <span data-ttu-id="9e2de-116">W polu Grupa instrumentów nadaj nazwę grupie instrumentów bankowych.</span><span class="sxs-lookup"><span data-stu-id="9e2de-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="9e2de-117">W polu Opis wprowadź opis grupy instrumentów bankowych.</span><span class="sxs-lookup"><span data-stu-id="9e2de-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="9e2de-118">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9e2de-118">Click Save.</span></span>
6. <span data-ttu-id="9e2de-119">Kliknij kartę Typy instrumentu.</span><span class="sxs-lookup"><span data-stu-id="9e2de-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="9e2de-120">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="9e2de-120">Click New.</span></span>
8. <span data-ttu-id="9e2de-121">W polu Typ instrumentu wprowadź unikatowy kod.</span><span class="sxs-lookup"><span data-stu-id="9e2de-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="9e2de-122">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="9e2de-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="9e2de-123">W polu Grupa instrumentów kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="9e2de-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9e2de-124">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="9e2de-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9e2de-125">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="9e2de-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="9e2de-126">W polu Charakter instrumentu zaznacz charakter instrumentu bankowego.</span><span class="sxs-lookup"><span data-stu-id="9e2de-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="9e2de-127">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9e2de-127">Click Save.</span></span>
15. <span data-ttu-id="9e2de-128">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="9e2de-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="9e2de-129">Profil księgowania na koncie bankowym</span><span class="sxs-lookup"><span data-stu-id="9e2de-129">Bank posting profile</span></span>
1. <span data-ttu-id="9e2de-130">Wybierz kolejno opcje Zarządzanie gotówką i bankami > Ustawienia > Profil księgowania dokumentów bankowych.</span><span class="sxs-lookup"><span data-stu-id="9e2de-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="9e2de-131">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="9e2de-131">Click New.</span></span>
3. <span data-ttu-id="9e2de-132">W polu Numer konta/grupy kliknij przycisk rozwijany, aby otworzyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="9e2de-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9e2de-133">Na liście znajdź i zaznacz odpowiedni rekord.</span><span class="sxs-lookup"><span data-stu-id="9e2de-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9e2de-134">Na liście kliknij łącze w wybranym wierszu.</span><span class="sxs-lookup"><span data-stu-id="9e2de-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9e2de-135">Wybierz konto główne do rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="9e2de-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="9e2de-136">To konto będzie używane podczas obliczania prognoz przepływów pieniężnych.</span><span class="sxs-lookup"><span data-stu-id="9e2de-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="9e2de-137">W polu Konto opłaty wybierz konto dla transakcji wydatkowych.</span><span class="sxs-lookup"><span data-stu-id="9e2de-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="9e2de-138">W polu Konto marży wybierz konto dla transakcji dotyczących marży.</span><span class="sxs-lookup"><span data-stu-id="9e2de-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="9e2de-139">To konto będzie obciążane podczas księgowania marży początkowej, a uznawane podczas księgowania płatności.</span><span class="sxs-lookup"><span data-stu-id="9e2de-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="9e2de-140">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9e2de-140">Click Save.</span></span>
