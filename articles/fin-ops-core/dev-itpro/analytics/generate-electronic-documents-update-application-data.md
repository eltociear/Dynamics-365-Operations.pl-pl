---
title: Generowanie dokumentów elektronicznych i aktualizowanie danych aplikacji przy użyciu modułu ER
description: Można projektować formaty raportowania elektronicznego (ER), które będą używane w aplikacji do generowania wychodzących dokumentów elektronicznych. Można także zaprojektować formaty ER, które analizują składnię przychodzących dokumentów elektronicznych i używają zawartości tych dokumentów do aktualizowania danych aplikacji.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 333f91cef12b6564ca9bc668732b4cc038f0fa7e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181871"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="d908b-104">Generowanie dokumentów elektronicznych i aktualizowanie danych aplikacji przy użyciu modułu ER</span><span class="sxs-lookup"><span data-stu-id="d908b-104">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d908b-105">Można projektować formaty raportowania elektronicznego (ER), które będą używane w aplikacji do generowania wychodzących dokumentów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="d908b-105">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="d908b-106">Można także zaprojektować formaty ER, które analizują składnię przychodzących dokumentów elektronicznych i używają zawartości tych dokumentów do aktualizowania danych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d908b-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="d908b-107">Dzięki tej funkcjonalności jeden format ER może służyć do generowania wychodzących dokumentów elektronicznych, a następnie aktualizowania danych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d908b-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="d908b-108">Tej funkcji można używać w następujących scenariuszach:</span><span class="sxs-lookup"><span data-stu-id="d908b-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="d908b-109">Aby uniknąć wielokrotnego wykorzystywania danych aplikacji w kolejnych procesach, można oznaczyć dane aplikacje bezpośrednio po ich użyciu do wygenerowania dokumentów elektronicznych.</span><span class="sxs-lookup"><span data-stu-id="d908b-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="d908b-110">Na przykład można oznaczyć transakcje płatności jako już przetworzone natychmiast po ich umieszczeniu w wygenerowanym komunikacie płatniczym.</span><span class="sxs-lookup"><span data-stu-id="d908b-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="d908b-111">Aby zapisać szczegóły przetwarzania dokumentów elektronicznych, które zostały wygenerowane za pomocą logiki modułu ER.</span><span class="sxs-lookup"><span data-stu-id="d908b-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="d908b-112">Na przykład unikatowy identyfikator komunikatu płatniczego wygenerowanego za pomocą wyrażenia ER.</span><span class="sxs-lookup"><span data-stu-id="d908b-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="d908b-113">Wyrażenie bazuje na informacjach wprowadzonych w oknie dialogowym modułu ER po uruchomieniu formatu ER w celu wygenerowania dokumentów.</span><span class="sxs-lookup"><span data-stu-id="d908b-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="d908b-114">Aby dowiedzieć się więcej o tej funkcji, odtwórz przewodniki po zadaniach ER Generowanie dokumentów z aktualizacją danych aplikacji (część 7.5.4.3 procesu biznesowego Nabywanie/opracowywanie składników usług/rozwiązań informatycznych (10677)), które prowadzą przez kolejne etapy procesu sprawozdawczości i archiwizacji Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d908b-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="d908b-115">Następujące pliki są wymagane do wykonania pewnych kroków w tych przewodnikach po zadaniach.</span><span class="sxs-lookup"><span data-stu-id="d908b-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="d908b-116">Pobierz i zapisz te pliki na swoim lokalnym komputerze.</span><span class="sxs-lookup"><span data-stu-id="d908b-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="d908b-117">Konfiguracja modelu danych ER: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="d908b-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="d908b-118">Konfiguracja mapowania modelu ER: Intrastat (mapowanie)</span><span class="sxs-lookup"><span data-stu-id="d908b-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="d908b-119">Konfiguracja formatu ER: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="d908b-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)