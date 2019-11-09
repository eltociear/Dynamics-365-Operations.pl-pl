---
title: ER Konfigurowanie miejsc docelowych
description: Ta procedura przedstawia sposób konfigurowania i używania różnych miejsc docelowych dla składników wyjściowych raportowania elektronicznego (ER), takich jak folder lub plik.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbef5410d0e6f15fbb5025f3831486d55cd06216
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185067"
---
# <a name="er-configure-destinations"></a><span data-ttu-id="cf903-103">ER Konfigurowanie miejsc docelowych</span><span class="sxs-lookup"><span data-stu-id="cf903-103">ER Configure destinations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf903-104">Ta procedura przedstawia sposób konfigurowania i używania różnych miejsc docelowych dla składników wyjściowych raportowania elektronicznego (ER), takich jak folder lub plik.</span><span class="sxs-lookup"><span data-stu-id="cf903-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="cf903-105">Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej DEMF.</span><span class="sxs-lookup"><span data-stu-id="cf903-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="cf903-106">Niemcy to kraj\region podstawowego adresu firmy, jednak w tej procedurze można użyć dowolnej firmy.</span><span class="sxs-lookup"><span data-stu-id="cf903-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="cf903-107">Formatem używanym w tym przykładzie jest Polecenie przelewu ISO20022, ale można użyć dowolnego innego formatu, który został już zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="cf903-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="cf903-108">Należy zauważyć, że ta procedura jest przykładem konfiguracji z jednym plikiem i jednym miejscem docelowym.</span><span class="sxs-lookup"><span data-stu-id="cf903-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="cf903-109">Więcej informacji na temat zarządzania miejscami docelowymi raportowania elektronicznego można znaleźć na stronach Pomocy systemu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cf903-109">More information about Electronic reporting destination management can be found in the Dynamics 365 Finance Help.</span></span>

1. <span data-ttu-id="cf903-110">Wybierz kolejno opcje Administrowanie organizacją > Raportowanie elektroniczne > Aplikacja docelowa raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="cf903-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="cf903-111">Kliknij przycisk Nowy, aby utworzyć nowy zbiór miejsc docelowych dla formatu.</span><span class="sxs-lookup"><span data-stu-id="cf903-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="cf903-112">W polu Odwołanie zaznacz format, dla którego chcesz skonfigurować miejsca docelowe.</span><span class="sxs-lookup"><span data-stu-id="cf903-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="cf903-113">Jeśli nie masz wartości do wybrania, oznacza to, że nie zaimportowano żadnych konfiguracji formatów raportowania elektronicznego.</span><span class="sxs-lookup"><span data-stu-id="cf903-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="cf903-114">Należy zaimportować konfigurację formatu przed skonfigurowaniem miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="cf903-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="cf903-115">Kliknij przycisk Nowy, aby utworzyć nowe miejsce docelowe dla plików.</span><span class="sxs-lookup"><span data-stu-id="cf903-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="cf903-116">Należy zauważyć, że można utworzyć jedno miejsce docelowe plików dla każdego składnika wyjściowego o takim samym formacie, takiego jak folder lub plik.</span><span class="sxs-lookup"><span data-stu-id="cf903-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="cf903-117">Miejsca docelowe będzie można osobno włączać i wyłączać w ustawieniach.</span><span class="sxs-lookup"><span data-stu-id="cf903-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="cf903-118">W polu Nazwa wprowadź przyjazną nazwę składnika wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="cf903-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="cf903-119">Zaleca się używanie sugestywnych nazw, na przykład „Plik płatności” lub „Raport z kontroli”.</span><span class="sxs-lookup"><span data-stu-id="cf903-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="cf903-120">Te nazwy będą prezentowane użytkownikom podczas konfigurowania razem z ustawieniami miejsc docelowych.</span><span class="sxs-lookup"><span data-stu-id="cf903-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="cf903-121">W polu Nazwa pliku wybierz plik lub folder specyficzny dla formatu.</span><span class="sxs-lookup"><span data-stu-id="cf903-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="cf903-122">Kliknij przycisk Ustawienia.</span><span class="sxs-lookup"><span data-stu-id="cf903-122">Click Settings.</span></span>
8. <span data-ttu-id="cf903-123">W polu Włączone wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="cf903-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="cf903-124">Pole wyboru Włączone na każdej karcie pozwala włączać i wyłączać osobno każde miejsce docelowe.</span><span class="sxs-lookup"><span data-stu-id="cf903-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="cf903-125">W tym przykładzie włączysz wysyłanie pliku wyjściowego do adresata poczty podczas generowania pliku.</span><span class="sxs-lookup"><span data-stu-id="cf903-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="cf903-126">Kliknij przycisk Edytuj, aby skonfigurować adresatów wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="cf903-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="cf903-127">Kliknij przycisk Dodaj.</span><span class="sxs-lookup"><span data-stu-id="cf903-127">Click Add.</span></span>
11. <span data-ttu-id="cf903-128">Kliknij opcję Wiadomość e-mail zarządzania drukowaniem.</span><span class="sxs-lookup"><span data-stu-id="cf903-128">Click Print Management email.</span></span>
12. <span data-ttu-id="cf903-129">W polu Źródło poczty e-mail wybierz opcję.</span><span class="sxs-lookup"><span data-stu-id="cf903-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="cf903-130">Można wybrać różne typy źródeł poczty e-mail, takie jak typ odbiorcy lub dostawcy.</span><span class="sxs-lookup"><span data-stu-id="cf903-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="cf903-131">Określa to typ argumentu, który będzie zwracany przez formułę konta źródła poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="cf903-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="cf903-132">Formuła konta źródła poczty e-mail, opisana w następnym kroku, służy do powiązania źródła wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="cf903-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="cf903-133">Wybierz opcję Dostawca, jeśli formuła będzie zwracała konto dostawcy.</span><span class="sxs-lookup"><span data-stu-id="cf903-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="cf903-134">Użyj opcji Dostawca, jeśli używasz przykładu konfiguracji przelewu bankowego ISO 20022.</span><span class="sxs-lookup"><span data-stu-id="cf903-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="cf903-135">Kliknij przycisk Powiąż źródło poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="cf903-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="cf903-136">W formule wprowadź specyficzne dla dokumentu odwołanie do wybranego wcześniej typu strony.</span><span class="sxs-lookup"><span data-stu-id="cf903-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="cf903-137">Zamiast wpisywać informacje ręcznie, można odszukać węzeł źródła danych reprezentujący konto strony, a następnie kliknąć przycisk Dodaj źródło danych, aby zaktualizować formułę.</span><span class="sxs-lookup"><span data-stu-id="cf903-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="cf903-138">Na przykład: W przypadku konfiguracji polecenia przelewu ISO 20022 węzłem reprezentującym konto dostawcy jest „$PaymentsForCoveringLetter”.Wierzyciel.Identyfikator.SourceID.</span><span class="sxs-lookup"><span data-stu-id="cf903-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="cf903-139">W przeciwnym razie wpisz dowolny ciąg tekstowy, np. „DE-001”, aby zapisać formułę.</span><span class="sxs-lookup"><span data-stu-id="cf903-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="cf903-140">Kliknij przycisk Zapisz.</span><span class="sxs-lookup"><span data-stu-id="cf903-140">Click Save.</span></span>
16. <span data-ttu-id="cf903-141">Zamknij stronę.</span><span class="sxs-lookup"><span data-stu-id="cf903-141">Close the page.</span></span>
17. <span data-ttu-id="cf903-142">Kliknij przycisk Edytuj, aby skonfigurować dane osoby kontaktowej dla strony.</span><span class="sxs-lookup"><span data-stu-id="cf903-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="cf903-143">W polu Kontakt podstawowy wybierz opcję Tak.</span><span class="sxs-lookup"><span data-stu-id="cf903-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="cf903-144">Można użyć różnych opcji w celu wskazania, jaki typ kontaktu strony powinien być używany jako adres e-mail dla tego miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="cf903-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="cf903-145">W tym przykładzie korzystamy z głównej osoby kontaktowej.</span><span class="sxs-lookup"><span data-stu-id="cf903-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="cf903-146">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="cf903-146">Click OK.</span></span>
20. <span data-ttu-id="cf903-147">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="cf903-147">Click OK.</span></span>
21. <span data-ttu-id="cf903-148">W polu Temat wpisz wartość.</span><span class="sxs-lookup"><span data-stu-id="cf903-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="cf903-149">Kliknij przycisk OK.</span><span class="sxs-lookup"><span data-stu-id="cf903-149">Click OK.</span></span>
