---
title: Konfigurowanie potrąconych zaliczek na podatek
description: W tym temacie wyjaśniono sposób konfigurowania potrąconej zaliczki na podatek.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185964"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="ace5b-103">Konfigurowanie potrąconych zaliczek na podatek</span><span class="sxs-lookup"><span data-stu-id="ace5b-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ace5b-104">W tym temacie wyjaśniono sposób konfigurowania potrąconej zaliczki na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="ace5b-105">*Potrącona zaliczka na podatek* to podatek nałożony na dostawców, który nie powoduje utworzenia transakcji podatkowej.</span><span class="sxs-lookup"><span data-stu-id="ace5b-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="ace5b-106">Potrącona zaliczka na podatek obliczana dla płatności dostawców jest zobowiązaniem.</span><span class="sxs-lookup"><span data-stu-id="ace5b-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="ace5b-107">Z tego względu tylko konta bilansowe lub konta pasywów są odpowiednimi miejscami do księgowania potrąconych zaliczek na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="ace5b-108">W tym przewodniku po zadaniach przedstawiono sposób konfigurowania zaliczek na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="ace5b-109">Otwórz **Okienko nawigacji > Moduły > Podatek > Podatki pośrednie > Potrącona zaliczka na podatek > Kody potrąconych zaliczek na podatek**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="ace5b-110">Wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-110">Select **New**.</span></span>
3. <span data-ttu-id="ace5b-111">W polu **Kod potrąconej zaliczki na podatek** wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="ace5b-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="ace5b-112">W polu **Nazwa potrąconej zaliczki na podatek** nadaj nazwę kodowi zaliczki na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="ace5b-113">W polu **Konto główne** wybierz główne konto do księgowania zobowiązań z tytułu zaliczek na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="ace5b-114">Wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-114">Select **Save**.</span></span>
7. <span data-ttu-id="ace5b-115">Wybierz **Wartości** i oznacz odpowiedni rekord na liście.</span><span class="sxs-lookup"><span data-stu-id="ace5b-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="ace5b-116">W polu **Wartość** wprowadź wartość procentową używaną do obliczania zaliczki na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="ace5b-117">Wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-117">Select **Save**.</span></span>
10. <span data-ttu-id="ace5b-118">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="ace5b-118">Close the page.</span></span>
11. <span data-ttu-id="ace5b-119">Wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-119">Select **Save**.</span></span>
12. <span data-ttu-id="ace5b-120">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="ace5b-120">Close the page.</span></span>
13. <span data-ttu-id="ace5b-121">Otwórz **Okienko nawigacji > Moduły > Podatek > Podatki pośrednie > Potrącona zaliczka na podatek > Grupy potrąconych zaliczek na podatek**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="ace5b-122">Wybierz pozycję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-122">Select **New**.</span></span>
15. <span data-ttu-id="ace5b-123">W polu **Grupa potrąconej zaliczki na podatek** nadaj identyfikator grupie zaliczek na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="ace5b-124">W polu **Opis** nadaj nazwę grupie zaliczek na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="ace5b-125">W polu **Kod potrąconej zaliczki na podatek** wybierz kod zaliczki na podatek.</span><span class="sxs-lookup"><span data-stu-id="ace5b-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="ace5b-126">Wybierz opcję **Zapisz**.</span><span class="sxs-lookup"><span data-stu-id="ace5b-126">Select **Save**.</span></span>
19. <span data-ttu-id="ace5b-127">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="ace5b-127">Close the page.</span></span>
