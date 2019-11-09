---
title: Tworzenie składników kosztu
description: Istnieje kilka sposobów tworzenia składników kosztów w module Rachunek kosztów.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187804"
---
# <a name="create-cost-elements"></a><span data-ttu-id="d9ca7-103">Tworzenie składników kosztu</span><span class="sxs-lookup"><span data-stu-id="d9ca7-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9ca7-104">Istnieje kilka sposobów tworzenia składników kosztów w module Rachunek kosztów.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="d9ca7-105">W tej procedurze pokazano, jak utworzyć składniki kosztów, importując konta główne za pośrednictwem łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="d9ca7-106">Dane wykorzystane do utworzenia tej procedury pochodzą z firmy demonstracyjnej USMF.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="d9ca7-107">Procedura dotyczy funkcji Rachunek kosztów dodanej w programie Dynamics 365 for Operations w wersji 1611.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="d9ca7-108">Tworzenie nowych składników kosztów</span><span class="sxs-lookup"><span data-stu-id="d9ca7-108">Create new cost elements</span></span>
1. <span data-ttu-id="d9ca7-109">Wybierz kolejno opcje Rachunek kosztów > Wymiary > Wymiary składników kosztów.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="d9ca7-110">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-110">Click New.</span></span>
3. <span data-ttu-id="d9ca7-111">W polu Nazwa wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d9ca7-112">W polu Łącznik danych dla elementów członkowskich wymiarów wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="d9ca7-113">Wypełnij pole Opis.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d9ca7-114">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="d9ca7-115">Konfigurowanie łącznika danych</span><span class="sxs-lookup"><span data-stu-id="d9ca7-115">Configure the data connector</span></span>
1. <span data-ttu-id="d9ca7-116">Kliknij opcję Konfiguruj dostawcę elementów członkowskich wymiarów.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="d9ca7-117">W polu Plan kont wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="d9ca7-118">Wybierz opcję Współdzielony, aby używać wspólnego planu kont.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="d9ca7-119">Kliknij przycisk Nowy.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-119">Click New.</span></span>
4. <span data-ttu-id="d9ca7-120">Na liście oznacz wybrany wiersz.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d9ca7-121">Do kont można zastosować filtry, aby zostały spełnione żądane kryteria.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="d9ca7-122">W polu Z konta głównego wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="d9ca7-123">W polu Do konta głównego wprowadź lub wybierz wartość.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="d9ca7-124">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="d9ca7-125">Importuj konta główne</span><span class="sxs-lookup"><span data-stu-id="d9ca7-125">Import main accounts</span></span>
1. <span data-ttu-id="d9ca7-126">Kliknij opcję Importuj elementy członkowskie wymiaru.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="d9ca7-127">Konta główne zostaną zaimportowane do modułu Rachunek kosztów i będą używane jako składniki kosztu.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="d9ca7-128">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="d9ca7-129">Wyświetlanie zaimportowanych kont jako składników kosztów</span><span class="sxs-lookup"><span data-stu-id="d9ca7-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="d9ca7-130">Kliknij opcję Wyświetl elementy członkowskie wymiaru.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-130">Click View dimension members.</span></span>
    * <span data-ttu-id="d9ca7-131">Umożliwia wyświetlanie zaimportowanych kont księgowych jako składników kosztów w firmie, do których mogą spływać koszty.</span><span class="sxs-lookup"><span data-stu-id="d9ca7-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  
