---
title: Obszar roboczy fakturowania w portalu współpracy z dostawcami
description: W tym temacie wyjaśniono, jak wyświetlić faktury od dostawców i przesyłać faktury z obszaru roboczego Fakturowanie w portalu współpracy z dostawcami.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 626607814d6c747d74a13de284db097f0efd8a0c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179464"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="00e14-103">Obszar roboczy fakturowania w portalu współpracy z dostawcami</span><span class="sxs-lookup"><span data-stu-id="00e14-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00e14-104">W tym temacie wyjaśniono, jak wyświetlić faktury od dostawców i przesyłać faktury z obszaru roboczego Fakturowanie w portalu współpracy z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="00e14-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="00e14-105">Obszar roboczy **Fakturowanie w portalu współpracy dostawcy** może służyć do przeglądania informacji o fakturach od dostawców i przesyłania faktur do systemu za pomocą funkcji przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="00e14-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="00e14-106">Obszar roboczy fakturowania w portalu współpracy z dostawcami</span><span class="sxs-lookup"><span data-stu-id="00e14-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="00e14-107">Kafelki podsumowania</span><span class="sxs-lookup"><span data-stu-id="00e14-107">Summary tiles</span></span>

<span data-ttu-id="00e14-108">Kafelki **Podsumowanie** prezentują przegląd faktur od wybranego dostawcy.</span><span class="sxs-lookup"><span data-stu-id="00e14-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="00e14-109">Istnieje możliwość wyświetlania faktur według ich stanu.</span><span class="sxs-lookup"><span data-stu-id="00e14-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="00e14-110">Wersje robocze faktur nie zostały przesłane do przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="00e14-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="00e14-111">Przesłane niezatwierdzone faktury to takie faktury, które dostawca przesłał, ale nie zostały one jeszcze zaksięgowane w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="00e14-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="00e14-112">Zatwierdzone niezapłacone faktury to takie faktury, które zostały zaksięgowane, ale ich jeszcze w całości nie opłacono.</span><span class="sxs-lookup"><span data-stu-id="00e14-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="00e14-113">Zapłacone faktury to takie faktury, które zostały w całości zapłacone w aplikacji.</span><span class="sxs-lookup"><span data-stu-id="00e14-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="00e14-114">Kliknięcie kafelka otwiera przefiltrowany widok strony **Lista faktur**.</span><span class="sxs-lookup"><span data-stu-id="00e14-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="00e14-115">Listy tabelaryczne</span><span class="sxs-lookup"><span data-stu-id="00e14-115">Tabular lists</span></span>

<span data-ttu-id="00e14-116">W sekcji **Listy tabelaryczne** stan fakturowania dzieli się w podobny sposób, jak w kafelkach podsumowania: listy wersji roboczych i przesłanych niezatwierdzonych.</span><span class="sxs-lookup"><span data-stu-id="00e14-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="00e14-117">W stanie Wersja robocza fakturę można przesłać do przepływu pracy lub usunąć.</span><span class="sxs-lookup"><span data-stu-id="00e14-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="00e14-118">Ostatnia lista tabelaryczna to opcja pozwalająca odnaleźć faktury.</span><span class="sxs-lookup"><span data-stu-id="00e14-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="00e14-119">Można filtrować podczas wyszukiwania, aby przyspieszyć wyszukiwanie.</span><span class="sxs-lookup"><span data-stu-id="00e14-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="00e14-120">Strona listy Wszystkie faktury od dostawcy</span><span class="sxs-lookup"><span data-stu-id="00e14-120">All vendor invoices list page</span></span>

<span data-ttu-id="00e14-121">Na stronie listy **Faktury w portalu współpracy z dostawcami** można wyświetlić wszystkie zaksięgowane i niezaksięgowane faktury od dostawcy.</span><span class="sxs-lookup"><span data-stu-id="00e14-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="00e14-122">Ta strona listy służy do wyświetlania stanu płatności faktur.</span><span class="sxs-lookup"><span data-stu-id="00e14-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="00e14-123">Istnieją następujące stany płatności: niezaksięgowane, niezapłacone, częściowo zapłacone i w pełni zapłacone.</span><span class="sxs-lookup"><span data-stu-id="00e14-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="00e14-124">Tworzenie nowej faktury na podstawie zamówienia zakupu</span><span class="sxs-lookup"><span data-stu-id="00e14-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="00e14-125">Nową fakturę od dostawcy można utworzyć, wybierając akcję **Nowy** w obszarze roboczym **Fakturowanie w portalu współpracy z dostawcami**.</span><span class="sxs-lookup"><span data-stu-id="00e14-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="00e14-126">Dostawca musi podać numer zamówienia zakupu i numer faktury.</span><span class="sxs-lookup"><span data-stu-id="00e14-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="00e14-127">Domyślnie wszystkie wiersze z zamówienia zakupu dostawcy będą widoczne w nowej fakturze.</span><span class="sxs-lookup"><span data-stu-id="00e14-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="00e14-128">Informacje dotyczące ilości i kosztu można edytować przed przesłaniem faktury dostawcy do przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="00e14-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="00e14-129">Przed przesłaniem faktury można do niej dołączyć pliki, obrazy, notatki i adresy URL.</span><span class="sxs-lookup"><span data-stu-id="00e14-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="00e14-130">Aby uzyskać więcej informacji, zobacz [Współpraca z zewnętrznymi dostawcami](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="00e14-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>


