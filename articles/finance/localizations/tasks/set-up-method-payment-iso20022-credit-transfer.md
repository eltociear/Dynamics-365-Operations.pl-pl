---
title: Konfigurowanie metody płatności przelewu ISO20022
description: W tej procedurze pokazano, jak skonfigurować metodę płatności dla dostawcy poleceniem przelewu ISO20022 lub za pomocą innego typu płatności, używając raportowania elektronicznego do wygenerowania pliku.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174999"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="9cec6-103">Konfigurowanie metody płatności przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="9cec6-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cec6-104">W tej procedurze pokazano, jak skonfigurować metodę płatności dla dostawcy poleceniem przelewu ISO20022 lub za pomocą innego typu płatności, używając raportowania elektronicznego do wygenerowania pliku.</span><span class="sxs-lookup"><span data-stu-id="9cec6-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="9cec6-105">Przed wykonaniem tego zadania trzeba utworzyć konfiguracje formatów eksportu i konta płatności.</span><span class="sxs-lookup"><span data-stu-id="9cec6-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="9cec6-106">Zadanie utworzono przy użyciu danych firmy demonstracyjnej DEMF.</span><span class="sxs-lookup"><span data-stu-id="9cec6-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="9cec6-107">Jest to trzecia z pięciu procedur, które razem ilustrują proces płatności dostawcom przy użyciu konfiguracji raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="9cec6-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="9cec6-108">Procedura dotyczy funkcji dodanej w programie Dynamics 365 for Operations w wersji 1611.</span><span class="sxs-lookup"><span data-stu-id="9cec6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="9cec6-109">Wybierz kolejno opcje Rozrachunki z dostawcami > Ustawienia płatności > Metody płatności.</span><span class="sxs-lookup"><span data-stu-id="9cec6-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="9cec6-110">Skorzystaj z opcji szybkiego filtrowania, aby znaleźć rekordy.</span><span class="sxs-lookup"><span data-stu-id="9cec6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9cec6-111">Na przykład wyfiltruj według pola Metoda płatności z wartością „SEPA CT”.</span><span class="sxs-lookup"><span data-stu-id="9cec6-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="9cec6-112">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="9cec6-112">Click Edit.</span></span>
4. <span data-ttu-id="9cec6-113">W polu Okres wybierz opcję „Razem”.</span><span class="sxs-lookup"><span data-stu-id="9cec6-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="9cec6-114">W polu Typ płatności wybierz opcję „Płatność elektroniczna”.</span><span class="sxs-lookup"><span data-stu-id="9cec6-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="9cec6-115">Rozwiń sekcję Formaty plików.</span><span class="sxs-lookup"><span data-stu-id="9cec6-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="9cec6-116">W polu Ogólne raportowanie elektroniczne wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="9cec6-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="9cec6-117">W polu Konfiguracja formatu eksportu wpisz lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="9cec6-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="9cec6-118">Na liście zaznacz wartość Polecenie przelewu ISO20022 (DE).</span><span class="sxs-lookup"><span data-stu-id="9cec6-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="9cec6-119">Jeśli lista jest pusta, nie istnieje żadna zaimportowana i aktywna konfiguracja formatu eksportu płatności dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="9cec6-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="9cec6-120">W polu Typ konta wybierz opcję „Bank”.</span><span class="sxs-lookup"><span data-stu-id="9cec6-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="9cec6-121">W polu Konto płatności wpisz wartość „DEMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="9cec6-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="9cec6-122">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="9cec6-122">Click Save.</span></span>
