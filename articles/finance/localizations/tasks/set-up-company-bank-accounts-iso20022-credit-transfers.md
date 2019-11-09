---
title: Konfigurowanie kont bankowych firmy dla poleceń przelewu ISO20022
description: Ta procedura przedstawia sposób konfigurowania danych konta bankowego specyficznych dla firmy wymaganych do generowania pliku płatności.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175000"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="a96c5-103">Konfigurowanie kont bankowych firmy dla poleceń przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="a96c5-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a96c5-104">Ta procedura przedstawia sposób konfigurowania danych konta bankowego specyficznych dla firmy wymaganych do generowania pliku płatności.</span><span class="sxs-lookup"><span data-stu-id="a96c5-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="a96c5-105">Ustawiasz informacje wymagane do wygenerowania formatu polecenia przelewu ISO 20022, ale w zależności od formatu mogą być wymagane dodatkowe informacje, takie jak identyfikator firmy lub numer rozliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="a96c5-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="a96c5-106">Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej DEMF.</span><span class="sxs-lookup"><span data-stu-id="a96c5-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="a96c5-107">Jest to druga z pięciu procedur, które razem ilustrują proces płatności dostawcom przy użyciu konfiguracji raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="a96c5-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a96c5-108">Procedura dotyczy funkcji dodanej w programie Dynamics 365 for Operations w wersji 1611.</span><span class="sxs-lookup"><span data-stu-id="a96c5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="a96c5-109">Konfigurowanie kodów IBAN i SWIFT</span><span class="sxs-lookup"><span data-stu-id="a96c5-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="a96c5-110">Wybierz kolejno opcje Zarządzanie gotówką i bankami > Konta bankowe.</span><span class="sxs-lookup"><span data-stu-id="a96c5-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="a96c5-111">Użyj szybkiego filtru, aby wyfiltrować pole Konto bankowe według wartości „DEMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="a96c5-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="a96c5-112">Kliknij pozycję DEMF OPER, aby otworzyć szczegóły konta bankowego.</span><span class="sxs-lookup"><span data-stu-id="a96c5-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="a96c5-113">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="a96c5-113">Click Edit.</span></span>
5. <span data-ttu-id="a96c5-114">Rozwiń sekcję Dodatkowa identyfikacja.</span><span class="sxs-lookup"><span data-stu-id="a96c5-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="a96c5-115">W polu IBAN wpisz wartość „DE89370400440532013000”.</span><span class="sxs-lookup"><span data-stu-id="a96c5-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="a96c5-116">W polu Kod SWIFT wpisz wartość „DEUTDEFF”.</span><span class="sxs-lookup"><span data-stu-id="a96c5-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="a96c5-117">Należy zauważyć, że kod SWIFT\BIC nie jest wymagany dla wielu formatów płatności, jednak zaleca się zarejestrowanie go dla konta bankowego.</span><span class="sxs-lookup"><span data-stu-id="a96c5-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="a96c5-118">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="a96c5-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="a96c5-119">Konfigurowanie konta bankowego firmy</span><span class="sxs-lookup"><span data-stu-id="a96c5-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="a96c5-120">Wybierz kolejno opcje Administrowanie organizacją > Organizacje > Firmy.</span><span class="sxs-lookup"><span data-stu-id="a96c5-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="a96c5-121">Kliknij przycisk Edytuj.</span><span class="sxs-lookup"><span data-stu-id="a96c5-121">Click Edit.</span></span>
3. <span data-ttu-id="a96c5-122">Rozwiń sekcję Informacje o koncie bankowym.</span><span class="sxs-lookup"><span data-stu-id="a96c5-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="a96c5-123">W polu Konto bankowe wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="a96c5-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="a96c5-124">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="a96c5-124">Click Save.</span></span>
