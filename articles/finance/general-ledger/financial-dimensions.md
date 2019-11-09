---
title: Wymiary finansowe
description: W tym temacie opisano różne typy wymiarów finansowych oraz sposoby ich konfigurowania.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0715d3e4e4cb167c55d9c7d98cdf599187bf3b43
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179365"
---
# <a name="financial-dimensions"></a><span data-ttu-id="ab0c0-103">Wymiary finansowe</span><span class="sxs-lookup"><span data-stu-id="ab0c0-103">Financial dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab0c0-104">W tym temacie omówiono różne typy wymiarów finansowych oraz sposoby ich konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="ab0c0-105">Strona **Wymiary finansowe** umożliwia tworzenie wymiarów finansowych, które mogą być używane jako segmenty kont w planach kont.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="ab0c0-106">Istnieją dwa typy wymiarów finansowych: wymiary niestandardowe i wymiary oparte na jednostce.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="ab0c0-107">Niestandardowe wymiary są współużytkowane przez podmioty prawne i wartości są wprowadzane i obsługiwane przez użytkowników.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="ab0c0-108">W wymiarach opartych na jednostce wartości są zdefiniowane w innych miejscach w systemie, takich jak jednostki Odbiorcy lub Sklepy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as in Customers or Stores entities.</span></span> <span data-ttu-id="ab0c0-109">Niektóre wymiary oparte na jednostce są współużytkowane przez podmioty prawne, podczas gdy inne są przypisane do określonej firmy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span>

<span data-ttu-id="ab0c0-110">Po utworzeniu wymiarów finansowych na stronie **Wartości wymiarów finansowych** przypisz dodatkowe właściwości do każdego wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span>

<span data-ttu-id="ab0c0-111">Wymiary finansowe mogą służyć do reprezentowania firm.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="ab0c0-112">Nie trzeba tworzyć podmiotów prawnych w Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-112">You don't have to create the legal entities in Dynamics 365 Finance.</span></span> <span data-ttu-id="ab0c0-113">Jednak wymiary finansowe nie są zaprojektowane do zaspokajania wymagań operacyjnych ani biznesowych firmy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-113">However, financial dimensions aren't designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="ab0c0-114">Funkcję księgowania międzyjednostkowego w Finance zaprojektowano tylko z myślą o zapisach księgowych, które są tworzone przy każdej transakcji.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-114">The interunit accounting functionality in Finance is designed to address only the accounting entries that are created by each transaction.</span></span>

<span data-ttu-id="ab0c0-115">Przed skonfigurowaniem wymiarów finansowych jako firmy oceń swoje procesy biznesowe w następujących obszarach, aby ustalić, czy ta konfiguracja będzie działać w Twojej organizacji:</span><span class="sxs-lookup"><span data-stu-id="ab0c0-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="ab0c0-116">Zapasy</span><span class="sxs-lookup"><span data-stu-id="ab0c0-116">Inventory</span></span>
- <span data-ttu-id="ab0c0-117">Sprzedaż i zakupy między wymiarami finansowymi i firmami</span><span class="sxs-lookup"><span data-stu-id="ab0c0-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="ab0c0-118">Obliczanie i raportowanie podatku</span><span class="sxs-lookup"><span data-stu-id="ab0c0-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="ab0c0-119">Raportowanie operacyjne</span><span class="sxs-lookup"><span data-stu-id="ab0c0-119">Operational reporting</span></span>

<span data-ttu-id="ab0c0-120">Poniżej przedstawiono wybrane ograniczenia:</span><span class="sxs-lookup"><span data-stu-id="ab0c0-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="ab0c0-121">Można używać funkcji podatkowych tylko z firmami, a nie z wymiarami finansowymi.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="ab0c0-122">Niektóre raporty nie zawierają wymiarów finansowych.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="ab0c0-123">W związku z tym w celu raportowania według wymiarów finansowych może być konieczne modyfikowanie raportów.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="ab0c0-124">Wymiary niestandardowe</span><span class="sxs-lookup"><span data-stu-id="ab0c0-124">Custom dimensions</span></span>

<span data-ttu-id="ab0c0-125">Aby utworzyć wymiar finansowy zdefiniowany przez użytkownika, w polu **Użyj wartości z** wybierz opcję **Wymiar niestandardowy**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-125">To create a user-defined financial dimension, in the **Use values from** field, select **Custom dimension**.</span></span>

<span data-ttu-id="ab0c0-126">Można również określić maskę konta, aby ograniczyć typ i ilość informacji, które można wprowadzić dla wartości wymiarów,.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-126">You can also specify an account mask to limit the amount and type of information that can be entered for dimension values.</span></span> <span data-ttu-id="ab0c0-127">Można wprowadzić znaki, które pozostają takie same dla każdej wartości wymiaru, na przykład litery lub łącznik (-).</span><span class="sxs-lookup"><span data-stu-id="ab0c0-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="ab0c0-128">Można także wprowadzić znaki cyfr (\#) oraz handlowego „i” (&) jako symbole zastępcze znaków, które zmieniają się za każdym razem, gdy wartość wymiaru jest tworzona.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-128">You can also enter number signs (\#) and ampersands (&) as placeholders for characters that will change every time that a dimension value is created.</span></span> <span data-ttu-id="ab0c0-129">Znak cyfry (\#) służy jako symbol zastępczy dla cyfr, a znak handlowe „i” jako symbol zastępczy dla liter.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="ab0c0-130">Pole maski formatu jest dostępne tylko w przypadku zaznaczenia opcji **Wymiar niestandardowy** w polu **Użyj wartości z**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-130">The field for the format mask is available only when you select **Custom dimension** in the **Use values from** field.</span></span>

<span data-ttu-id="ab0c0-131">**Przykład**</span><span class="sxs-lookup"><span data-stu-id="ab0c0-131">**Example**</span></span>

<span data-ttu-id="ab0c0-132">Aby ograniczyć wartość wymiaru do liter „CC” i trzech cyfr, należy wprowadzić **CC-\#\#\#** jako maskę formatu.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="ab0c0-133">Wymiary oparte na jednostce</span><span class="sxs-lookup"><span data-stu-id="ab0c0-133">Entity-backed dimensions</span></span>

<span data-ttu-id="ab0c0-134">Aby utworzyć wymiary oparte na jednostce, w polu **Użyj wartości z** wybierz jednostkę zdefiniowaną przez system, która będzie podstawą wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="ab0c0-135">Wartości wymiarów finansowych będą wtedy tworzone na bazie tej jednostki.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="ab0c0-136">Na przykład aby utworzyć wartości wymiarów dla projektów, wybierz opcję **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="ab0c0-137">Wartość wymiaru zostanie wtedy utworzona dla każdej nazwy projektu.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="ab0c0-138">Strona **Wartości wymiarów finansowych** pokazuje wartości jednostki.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="ab0c0-139">Jeśli te wartości są związane z konkretną firmą, na stronie widać również firmę.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="ab0c0-140">Aktywowanie wymiaru</span><span class="sxs-lookup"><span data-stu-id="ab0c0-140">Activating dimensions</span></span>

<span data-ttu-id="ab0c0-141">Po uaktywnieniu wymiaru finansowego tabela zostanie zaktualizowana, tak aby zawierała nazwę wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="ab0c0-142">Usunięte wymiary zostaną wykasowane.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="ab0c0-143">Wartości wymiaru finansowego można wprowadzić przed jego uaktywnieniem.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="ab0c0-144">Jednak wymiar finansowy będzie mógł być zużywany dopiero po uaktywnieniu.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="ab0c0-145">Na przykład, nie można dodać wymiaru finansowego do struktury konta przed aktywowaniem wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="ab0c0-146">Po kliknięciu przycisku **Uaktywnij** wszystkie wymiary są aktualizowane i pokazują zmianę stanu.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-146">When you select **Activate**, all dimensions are updated and show status changes.</span></span>

## <a name="translations"></a><span data-ttu-id="ab0c0-147">Tłumaczenia</span><span class="sxs-lookup"><span data-stu-id="ab0c0-147">Translations</span></span>

<span data-ttu-id="ab0c0-148">Na stronie **Tłumaczenie tekstu** można wprowadzić tekst dla wybranego wymiaru finansowego w różnych językach.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="ab0c0-149">Na stronie **Tłumaczenie konta głównego** można wprowadzić tekst dla konta głównego w różnych językach.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="ab0c0-150">Firma zastępuje</span><span class="sxs-lookup"><span data-stu-id="ab0c0-150">Legal entity overrides</span></span>

<span data-ttu-id="ab0c0-151">Nie wszystkie wymiary mogą być używane we wszystkich firmach.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="ab0c0-152">Ponadto niektóre wymiary mogą mieć zastosowanie tylko do wybranych okresów.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="ab0c0-153">W takich przypadkach można w sekcji **Firma zastępuje** określić firmy, dla których wymiar powinien być zawieszony, właściciela oraz okres aktywności wymiaru.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="ab0c0-154">Usuwanie wymiarów finansowych</span><span class="sxs-lookup"><span data-stu-id="ab0c0-154">Deleting financial dimensions</span></span>

<span data-ttu-id="ab0c0-155">Aby pomóc utrzymać więzy integralności danych, w wyjątkowych sytuacjach można usuwać wymiary finansowe.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="ab0c0-156">Jeśli zostanie podjęta próba usunięcia wymiaru finansowego, sprawdzane są następujące kryteria:</span><span class="sxs-lookup"><span data-stu-id="ab0c0-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="ab0c0-157">Czy wymiar finansowy został użyty w jakiejkolwiek zaksięgowanej lub niezaksięgowanej transakcji albo w jakimkolwiek rodzaju kombinacja wartości wymiarów?</span><span class="sxs-lookup"><span data-stu-id="ab0c0-157">Has the financial dimension been used on any posted or unposted transactions, or in any type of dimension value combination?</span></span>
- <span data-ttu-id="ab0c0-158">Czy wymiar finansowy jest używany w jakiejkolwiek aktywnej strukturze konta, strukturze reguły zaawansowanej lub zestawie wymiarów finansowych?</span><span class="sxs-lookup"><span data-stu-id="ab0c0-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="ab0c0-159">Czy wymiar finansowy wchodzi w skład domyślnego formatu integracji wymiarów finansowych?</span><span class="sxs-lookup"><span data-stu-id="ab0c0-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="ab0c0-160">Czy wymiar finansowy ustawiono jako wymiar domyślny?</span><span class="sxs-lookup"><span data-stu-id="ab0c0-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="ab0c0-161">Jeśli którekolwiek z tych kryteriów jest spełnione, nie można usunąć wymiaru finansowego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>

## <a name="default-dimension-values"></a><span data-ttu-id="ab0c0-162">Wartości domyślne wymiarów</span><span class="sxs-lookup"><span data-stu-id="ab0c0-162">Default dimension values</span></span>

<span data-ttu-id="ab0c0-163">Wartości z rekordów głównych, takich jak rekordy odbiorców i dostawców, można używać jako wartości domyślnych w nowych wymiarach.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-163">You can use values from master records, such as customer and vendor, as default values in new dimensions.</span></span> <span data-ttu-id="ab0c0-164">Podczas tworzenia nowych wymiarów identyfikator rekordu głównego wprowadza się w wartościach wymiarów tych rekordów głównych.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-164">When the new dimensions are created, the master record ID is entered in the dimension values for those master records.</span></span> <span data-ttu-id="ab0c0-165">Na przykład podczas tworzenia nowego odbiorcy należy w wymiarze Odbiorca wprowadzić identyfikator odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-165">For example, when you create a new customer, the customer ID is entered in the customer dimension.</span></span> <span data-ttu-id="ab0c0-166">Podczas tworzenia zamówień sprzedaży, faktur i innych dokumentów wymagających identyfikatora odbiorcy są używane istniejące zasady ustawiania wartości domyślnych, a do dokumentu jest dodawany identyfikator odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-166">When you create sales orders, invoices, or other documents that require a customer ID, the existing defaulting rules are used, and the customer ID is added to the document.</span></span>

<span data-ttu-id="ab0c0-167">Ta funkcja jest kontrolowana przez ustawienie w wymiarze.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-167">This feature is controlled by a setting in the dimension.</span></span> <span data-ttu-id="ab0c0-168">To ustawienie nosi nazwę **Kopiuj wartości do tego wymiaru dla każdej nowo tworzonej wartości DimensionName**, gdzie **DimensionName** jest nazwą wymiaru.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-168">This setting is named **Copy values to this dimension on each new DimensionName created**, where **DimensionName** is the name of the dimension.</span></span> <span data-ttu-id="ab0c0-169">Domyślnie ta funkcja jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-169">By default, the feature is turned off.</span></span> <span data-ttu-id="ab0c0-170">Jednak można ją włączyć w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-170">However, it can be turned on at any time.</span></span>

<span data-ttu-id="ab0c0-171">Jeśli już istnieją rekordy dla wymiaru, włączenie funkcji spowoduje aktualizację głównych rekordów.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-171">If records already exist for the dimension, the master records are updated when you turn the feature on.</span></span> <span data-ttu-id="ab0c0-172">Jednak istniejące dokumenty i transakcje nie zostaną zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-172">However, existing documents and transactions aren't updated.</span></span>

<span data-ttu-id="ab0c0-173">Jeśli używasz szablonu do tworzenia rekordu nadrzędnego, upewnij się, że wartość szablonu dla wymiaru głównego jest pusta.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-173">If you are using a template to create a master record, make sure that the template value for the master dimension is blank.</span></span> <span data-ttu-id="ab0c0-174">Na przykład tworząc odbiorców z szablonu, upewnij się, że wymiar odbiorcy w szablonie jest pusty.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-174">For example, if you're creating customers from a template, make sure that the customer dimension in the template is blank.</span></span> <span data-ttu-id="ab0c0-175">Wartość wymiaru odbiorcy zostanie pobrana domyślnie z nowego numeru odbiorcy podczas tworzenia odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-175">The customer dimension value will default from the new customer number when you create the new customer.</span></span>  

## <a name="derived-dimensions"></a><span data-ttu-id="ab0c0-176">Wymiary pochodne</span><span class="sxs-lookup"><span data-stu-id="ab0c0-176">Derived dimensions</span></span>

<span data-ttu-id="ab0c0-177">Wymiar można skonfigurować tak, aby informacje dla innych wymiarów były wprowadzane automatycznie podczas wprowadzania tego wymiaru w dokumencie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-177">You can configure a dimension so that information for other dimensions is automatically entered when you enter that dimension in a document.</span></span> <span data-ttu-id="ab0c0-178">Na przykład jeśli wprowadzasz centrum kosztu 10, wartość **20** może być automatycznie wprowadzana w wymiarze Dział.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-178">For example, if you enter cost center 10, a value of **20** can be automatically entered in the department dimension.</span></span>

<span data-ttu-id="ab0c0-179">Na stronie Wymiary można skonfigurować wartości pochodne.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-179">You can set up derived values on the dimensions page.</span></span>

1. <span data-ttu-id="ab0c0-180">Wybierz wymiar, a następnie wybierz opcję **Wymiary pochodne**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-180">Select a dimension and then select **Derived dimensions**.</span></span>

    <span data-ttu-id="ab0c0-181">Strona **Wymiary pochodne** zawiera siatkę.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-181">The **Derived dimensions** page includes a grid.</span></span> <span data-ttu-id="ab0c0-182">Wybrany segment wymiaru jest pierwszą kolumnę w tej siatce.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-182">The selected dimension segment is the first column in this grid.</span></span>

2. <span data-ttu-id="ab0c0-183">Dodaj segmenty, z których mają zostać utworzone obiekty pochodne.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-183">Add the segments that should be derived.</span></span> <span data-ttu-id="ab0c0-184">Każdy segment zostanie wyświetlony jako kolumna.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-184">Each segment appears as a column.</span></span>

<span data-ttu-id="ab0c0-185">Wprowadź kombinacje wymiarów, które mają zostać utworzone jako pochodne wymiaru z pierwszej kolumny.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-185">Enter the dimension combinations that should be derived from the dimension in the first column.</span></span> <span data-ttu-id="ab0c0-186">Na przykład aby używać centrum kosztu jako wymiaru, z którego mają zostać utworzone wymiary pochodne Dział i Lokalizacja, wprowadź centrum kosztu 10, dział 20 i lokalizację 30.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-186">For example, to use the cost center as the dimension that the department and location are derived from, enter cost center 10, department 20, and location 30.</span></span> <span data-ttu-id="ab0c0-187">Następnie gdy wprowadzisz centrum kosztu 10 w rekordzie głównym lub na stronie transakcji, dział 20 i lokalizacja 30 zostaną wprowadzone domyślnie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-187">Then, when you enter cost center 10 in a master record or on a transaction page, department 20 and location 30 are entered by default.</span></span>

### <a name="overriding-existing-values-with-derived-dimensions"></a><span data-ttu-id="ab0c0-188">Zastępowanie istniejących wartości wymiarami pochodnymi</span><span class="sxs-lookup"><span data-stu-id="ab0c0-188">Overriding existing values with derived dimensions</span></span>
 
<span data-ttu-id="ab0c0-189">Domyślnie w procesie tworzenia wymiarów pochodnych nie są zastępowane istniejące wartości wymiarów pochodnych.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-189">By default, the derived dimension process doesn't override existing values for derived dimensions.</span></span> <span data-ttu-id="ab0c0-190">Na przykład jeśli wprowadzisz centrum kosztu 10 i nie wprowadzisz żadnego innego wymiaru, domyślnie zostaną wprowadzone dział 20 i lokalizacja 30.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-190">For example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="ab0c0-191">Jednak jeśli zmienisz centrum kosztu, to wartości, które zostały już zdefiniowane, nie ulegną zmianie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-191">However, if you change the cost center, the values that have already been established aren't changed.</span></span> <span data-ttu-id="ab0c0-192">W związku z tym można utworzyć wymiary domyślne w rekordach głównych, a wymiary te nie będą zmieniane przez wymiary pochodne.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-192">Therefore, you can establish default dimensions on master records, and those dimensions won't be changed by derived dimensions.</span></span>

<span data-ttu-id="ab0c0-193">Można zmienić zachowanie wymiarów pochodnych tak, aby powodować zastępowanie istniejących wartości, zaznaczając pole wyboru **Zastąp istniejące wartości wymiarów wartościami pochodnymi** na stronie **Wymiary pochodne**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-193">You can change the behavior of derived dimensions to override existing values by selecting the **Replace existing dimension values with derived values** check box on the **Derived dimensions** page.</span></span> <span data-ttu-id="ab0c0-194">Jeśli to pole jest zaznaczone, można wprowadzić wymiar z pochodnymi wartościami wymiaru i te pochodne wartości wymiaru zastąpią wszelkie wartości, które już istnieją.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-194">If this field is selected, you can enter a dimension with derived dimension values and those derived dimension values will override any values that already exist.</span></span> <span data-ttu-id="ab0c0-195">W przykładzie powyżej jeśli wprowadzisz centrum kosztu 10 i nie wprowadzisz żadnego innego wymiaru, domyślnie zostaną wprowadzone dział 20 i lokalizacja 30.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-195">Using the previous example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="ab0c0-196">Jednak jeżeli już istniały wartości działu 50 i lokalizacji 60, zmienią się one na dział 20 i lokalizację 30.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-196">However, if the values were already department 50 and location 60, the values will now be changed to department 20 and location 30.</span></span>
 
<span data-ttu-id="ab0c0-197">Przy takim ustawieniu wymiary pochodne nie zastępują automatycznie istniejących domyślnych wartości wymiarów podczas ustawiania domyślnych wartości wymiarów.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-197">Derived dimensions with this setting do not automatically replace the existing default dimensions values when dimension values are defaulted.</span></span> <span data-ttu-id="ab0c0-198">Wartości wymiarów zostaną zastąpione tylko wtedy, gdy wprowadzisz nową wartość wymiaru na stronie, a już istnieją pochodne wartości tego wymiaru na stronie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-198">Dimension values will only be overridden when you enter a new dimension value on a page and there are existing derived values for that dimension on the page.</span></span>

### <a name="preventing-changes-with-derived-dimensions"></a><span data-ttu-id="ab0c0-199">Blokowanie zmian w wymiarach pochodnych</span><span class="sxs-lookup"><span data-stu-id="ab0c0-199">Preventing changes with derived dimensions</span></span>
 
<span data-ttu-id="ab0c0-200">Gdy na stronie **Wymiary pochodne** użyjesz opcji **Dodaj segment** w celu dodania segmentu jako wymiaru pochodnego, w dolnej części strony **Dodaj segment** znajdzie się opcja, który pozwala uniemożliwić wprowadzanie zmian w tym wymiarze, jeżeli stanie się wymiarem pochodnym na stronie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-200">When you use **Add segment"** on the **Derived dimensions page** to add a segment as a derived dimension, an option is provided at the bottom of the **Add segment** page that allows you to prevent changes to that dimension when it is derived on a page.</span></span> <span data-ttu-id="ab0c0-201">Ustawieniem domyślnym jest Wyłączone, tzn. nie ma blokady zastępowania wartości wymiarów pochodnych na stronie.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-201">The default setting is off so it does not prevent the derived dimension values from being changed.</span></span> <span data-ttu-id="ab0c0-202">Zmień to ustawienie na **Tak**, jeśli chcesz zapobiec modyfikowaniu wymiaru, gdy stanie się pochodny.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-202">Change the setting to **Yes** if you want prevent the dimension from being changed after it has been derived.</span></span> <span data-ttu-id="ab0c0-203">Na przykład jeśli wartość wymiaru Dział będzie pochodną wartości wymiaru Centrum kosztu, wartość wymiaru Dział nie zmieni się, jeśli opcję **Blokuj zmiany** ustawiono na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-203">For example, if the value for the Department dimension is derived from the value of the Cost center dimension, the Department value cannot be changed if the **Prevent changes** setting is **Yes**.</span></span> 
 
<span data-ttu-id="ab0c0-204">Ustawienie to nie zapobiega zmianom, jeśli wartość wymiaru jest prawidłowa, ale nie jest wymieniona na liście wymiarów pochodnych.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-204">The setting does not prevent changes if the dimension value is valid but it is not listed in the derived dimensions list.</span></span> <span data-ttu-id="ab0c0-205">Na przykład jeśli dział 20 jest pochodną centrum kosztu 10, a wprowadzisz centrum kosztu 10, nie będzie można edytować wartości działu 20.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-205">For example, if Department 20 is derived from Cost center 10 and you enter Cost center 10, then you will not be able to edit Department 20.</span></span> <span data-ttu-id="ab0c0-206">Jednak jeśli wprowadzisz centrum kosztu 20, a tej wartości nie ma na liście wymiarów pochodnych dla centrum kosztu, można edytować wartość działu.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-206">However, if you enter Cost center 20 and it is not in the list of derived dimensions for Cost center, then you can edit the Department value.</span></span> 
 
<span data-ttu-id="ab0c0-207">We wszystkich przypadkach wartość konta i wszystkie wartości wymiarów będą nadal weryfikowane względem struktur kont po zastosowaniu wartości wymiarów pochodnych.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-207">In all cases, the account value and all dimensions values will still be validated against the account structures after the derived dimensions values have been applied.</span></span> <span data-ttu-id="ab0c0-208">Jeśli używasz wymiarów pochodnych i nie przejdą one sprawdzania poprawności po umieszczeniu na stronie, należy zmienić wartości wymiarów pochodnych na stronie wymiarów pochodnych, zanim będzie można ich używać w transakcjach.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-208">If you use derived dimensions and they fail validation when used on a page, you must change the derived dimensions values on the derived dimensions page before you can use them in transactions.</span></span> 
 
<span data-ttu-id="ab0c0-209">Po zmianie wartości wymiarów na skróconej karcie **Wymiary finansowe** wymiar, dla którego ustawiono blokadę wprowadzania zmian, nie będzie edytowalny.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-209">When you change dimensions on the **Financials dimensions** FastTab, the dimension that is marked to prevent changes will not be editable.</span></span> <span data-ttu-id="ab0c0-210">W przypadku wprowadzania konta i wymiarów w formancie wpisów podzielonych na segmenty na stronie wymiary można edytować.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-210">If you are entering an account and dimensions into the segmented entry control on a page, the dimensions are editable.</span></span> <span data-ttu-id="ab0c0-211">Jednak po przeniesieniu fokusu z formantu wpisu podzielonego na segmenty i przejściu do innego pola lub wykonaniu czynności konto i wymiar zostaną zweryfikowane względem listy wymiarów pochodnych i struktur kont w celu sprawdzenia, czy wprowadzono odpowiednie wartości.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-211">However, when you move the highlight off the segmented entry control and move to another field or take an action, the account and dimensions will be validated against the derived dimensions list and the account structures to ensure that you have entered the appropriate values.</span></span> 

### <a name="derived-dimensions-and-entities"></a><span data-ttu-id="ab0c0-212">Pochodne wymiary i jednostki</span><span class="sxs-lookup"><span data-stu-id="ab0c0-212">Derived dimensions and entities</span></span>

<span data-ttu-id="ab0c0-213">Istnieje możliwość konfigurowania segmentów i wartości wymiarów pochodnych za pomocą jednostek.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-213">You can set up the derived dimensions segments and values by using entities.</span></span>

- <span data-ttu-id="ab0c0-214">Jednostka Wymiary pochodne konfiguruje wymiary sterujące oraz segmenty, które są w nich używane.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-214">The Derived dimensions entity sets up the driving dimensions and the segments that are used for those dimensions.</span></span>
- <span data-ttu-id="ab0c0-215">Jednostka Wartości wymiarów pochodnych umożliwia zaimportowanie wartości, które powinny zostać utworzone jako pochodne dla każdego wymiaru sterującego.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-215">The Derived dimensions value entity lets you import the values that should be derived for each driving dimension.</span></span>

<span data-ttu-id="ab0c0-216">Jeżeli podczas używania jednostki do importowania danych ta jednostka importuje wymiary, podczas importowania są stosowane reguły wymiarów pochodnych, chyba że jednostka jednoznacznie spowoduje zastąpienie tych wymiarów.</span><span class="sxs-lookup"><span data-stu-id="ab0c0-216">When you use an entity to import data, if that entity imports dimensions, the derived dimension rules are applied during the import unless the entity specifically overrides those dimensions.</span></span>

<span data-ttu-id="ab0c0-217">Aby uzyskać więcej informacji, zobacz następujące tematy:</span><span class="sxs-lookup"><span data-stu-id="ab0c0-217">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ab0c0-218">Definiowanie wymiarów finansowych</span><span class="sxs-lookup"><span data-stu-id="ab0c0-218">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="ab0c0-219">Obsługa domyślnych szablonów wymiaru finansowego</span><span class="sxs-lookup"><span data-stu-id="ab0c0-219">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)