---
title: Zaawansowane uzgadnianie konta bankowego, import dla formatu MT940 — uaktualnianie złożonej jednostki danych
description: Aby zapewnić obsługę formatu MT940, trzeba dodać numer kolejny do importowanej jednostki wyciągu bankowego.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188471"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="f5e3c-103">Zaawansowane uzgadnianie konta bankowego, import dla formatu MT940 — uaktualnianie złożonej jednostki danych</span><span class="sxs-lookup"><span data-stu-id="f5e3c-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5e3c-104">Aby zapewnić obsługę formatu MT940, trzeba dodać numer kolejny do importowanej jednostki wyciągu bankowego.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="f5e3c-105">Poniższa procedura umożliwia dodanie importowanej jednostki wyciągu bankowego w celu obsługi formatu MT940.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="f5e3c-106">Skompiluj i zsynchronizuj następujące elementy:</span><span class="sxs-lookup"><span data-stu-id="f5e3c-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="f5e3c-107">Jednostka złożona\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="f5e3c-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="f5e3c-108">Jednostka\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="f5e3c-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="f5e3c-109">Jednostka\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="f5e3c-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="f5e3c-110">Jednostka\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="f5e3c-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="f5e3c-111">Jednostka\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="f5e3c-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="f5e3c-112">Tabele\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="f5e3c-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="f5e3c-113">Zarządzanie danymi\\projekty danych.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="f5e3c-114">Załaduj projekty importu dla formatu MT940</span><span class="sxs-lookup"><span data-stu-id="f5e3c-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="f5e3c-115">Zmodyfikuj arkusz stylów XSLT.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-115">Change XSLT.</span></span>
            -   <span data-ttu-id="f5e3c-116">Kliknij opcję **Wyświetl mapę**.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-116">Click **View map**.</span></span>
            -   <span data-ttu-id="f5e3c-117">Na dokumencie wyciągu bankowego kliknij opcję **Wyświetl mapę**.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="f5e3c-118">Kliknij opcję **Przekształcenia**.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="f5e3c-119">Usuń plik BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="f5e3c-120">Dodaj nową wersję pliku BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="f5e3c-121">Udostępnij ustawienie **Numer sekwencyjny** w układzie **Dane źródłowe**.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="f5e3c-122">Format danych źródłowych = Element XML.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="f5e3c-123">Nazwa jednostki = Wyciągi bankowe.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="f5e3c-124">Przekaż plik danych = nowa wersja pliku SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="f5e3c-125">Kliknij przycisk **Tak**, aby zastąpić istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="f5e3c-126">Kliknij przycisk **Tak**, aby wygenerować nowe mapowanie.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="f5e3c-127">Upewnij się, że element **SequenceNumber** jest mapowany.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="f5e3c-128">W jednostce wyciągu kliknij opcję **Wyświetl mapę**.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="f5e3c-129">Upewnij się, że element **SequenceNumber** jest mapowany z obszaru Źródło do obszaru Tymczasowy.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="f5e3c-130">Zaimportuj nowy wyciąg.</span><span class="sxs-lookup"><span data-stu-id="f5e3c-130">Import the new statement.</span></span>



