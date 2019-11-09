---
title: Ustawianie opisów domyślnych dla automatycznego księgowania
description: W tym temacie opisano sposób ustawiania domyślnego tekstu, który opisuje wpisów, które są księgowane automatycznie w księdze głównej. Można skonfigurować domyślny tekst opisu, używając tekstu dowolnego kształtu lub wybrać sztywno określone zmienne.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622696"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="846b5-104">Ustawianie opisów domyślnych dla automatycznego księgowania</span><span class="sxs-lookup"><span data-stu-id="846b5-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="846b5-105">W tym temacie opisano sposób ustawiania domyślnego tekstu, który opisuje wpisów, które są księgowane automatycznie w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="846b5-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="846b5-106">Można skonfigurować domyślny tekst opisu, używając tekstu dowolnego kształtu lub wybrać sztywno określone zmienne.</span><span class="sxs-lookup"><span data-stu-id="846b5-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="846b5-107">W przypadku niektórych typów transakcji w niektórych krajach lub regionach, możesz również uwzględnić tekst z pól w bazie danych Microsoft Dynamics AX, które są związane z tymi rodzajami transakcji.</span><span class="sxs-lookup"><span data-stu-id="846b5-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="846b5-108">Aby zapoznać się z listą typów transakcji oraz krajami i regionami, zobacz sekcję [Opcjonalnie: Dodaj inny tekst do opisów domyślnych](#optional-add-other-text-to-default-descriptions) w dalszej części tego tematu.</span><span class="sxs-lookup"><span data-stu-id="846b5-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="846b5-109">Ustawianie opisów domyślnych</span><span class="sxs-lookup"><span data-stu-id="846b5-109">Set up default descriptions</span></span>

1. <span data-ttu-id="846b5-110">Wybierz kolejno opcje **Administrowanie organizacją** \> **Ustawienia** \> **Opisy domyślne**.</span><span class="sxs-lookup"><span data-stu-id="846b5-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="846b5-111">W okienku akcji wybierz opcję **Nowy**.</span><span class="sxs-lookup"><span data-stu-id="846b5-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="846b5-112">W polu **Opis** wybierz typ transakcji, aby utworzyć domyślny opis.</span><span class="sxs-lookup"><span data-stu-id="846b5-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="846b5-113">W polu **Język** wybierz język, który ma zostać uwzględniony do opisu.</span><span class="sxs-lookup"><span data-stu-id="846b5-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="846b5-114">W polu **Tekst** wprowadź opis domyślny.</span><span class="sxs-lookup"><span data-stu-id="846b5-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="846b5-115">Możesz dowolnie wpisać tekst w polu lub użyć jednej lub więcej z następujących niezależnych zmiennych:</span><span class="sxs-lookup"><span data-stu-id="846b5-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="846b5-116">**%1** — dodaj datę transakcji.</span><span class="sxs-lookup"><span data-stu-id="846b5-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="846b5-117">**%2** — dodaj identyfikator, który odnosi się do typu dokumentu, który jest księgowany w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="846b5-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="846b5-118">Na przykład w przypadku kopii przeznaczonej dla typów transakcji, które są powiązane z fakturą, zmienna **%2** dodaje numer faktury.</span><span class="sxs-lookup"><span data-stu-id="846b5-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="846b5-119">**%3**— dodaj identyfikator, który odnosi się do typu dokumentu, który jest księgowany w księdze głównej.</span><span class="sxs-lookup"><span data-stu-id="846b5-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="846b5-120">Na przykład w przypadku kopii przeznaczonej dla typów transakcji, które są powiązane z fakturą, zmienna **%3** dodaje numer konta odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="846b5-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="846b5-121">Opcjonalnie: Dodaj inny tekst do opisów domyślnych</span><span class="sxs-lookup"><span data-stu-id="846b5-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="846b5-122">W przypadku niektórych typów transakcji w niektórych krajach lub regionach, domyślne opisy moga zawierać tekst pochodzący z pół w twoich danych, które są związane z tymi rodzajami transakcji.</span><span class="sxs-lookup"><span data-stu-id="846b5-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="846b5-123">Poniższa lista zawiera typy transakcji i kraje oraz regiony, dla których ta opcja jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="846b5-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="846b5-124">**Typy transakcji**</span><span class="sxs-lookup"><span data-stu-id="846b5-124">**Transaction types**</span></span>

<span data-ttu-id="846b5-125">Można dodać inny tekst do opisów domyślnych dla typów transakcji, które są powiązane z następującymi typami dokumentów:</span><span class="sxs-lookup"><span data-stu-id="846b5-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="846b5-126">Faktury dla odbiorcy</span><span class="sxs-lookup"><span data-stu-id="846b5-126">Customer invoices</span></span>
- <span data-ttu-id="846b5-127">Odbiorca faktury korygującej</span><span class="sxs-lookup"><span data-stu-id="846b5-127">Customer credit notes</span></span>
- <span data-ttu-id="846b5-128">Płatność odbiorcy gotówką</span><span class="sxs-lookup"><span data-stu-id="846b5-128">Customer cash payments</span></span>
- <span data-ttu-id="846b5-129">Płatności dostawcy</span><span class="sxs-lookup"><span data-stu-id="846b5-129">Vendor payments</span></span>
- <span data-ttu-id="846b5-130">Zamówienia sprzedaży</span><span class="sxs-lookup"><span data-stu-id="846b5-130">Sales orders</span></span>
- <span data-ttu-id="846b5-131">Zamówienia zakupu</span><span class="sxs-lookup"><span data-stu-id="846b5-131">Purchase orders</span></span>
- <span data-ttu-id="846b5-132">Arkusze magazynowe</span><span class="sxs-lookup"><span data-stu-id="846b5-132">Inventory journals</span></span>
- <span data-ttu-id="846b5-133">Planowanie główne (MRP)</span><span class="sxs-lookup"><span data-stu-id="846b5-133">Master planning (MRP)</span></span>
- <span data-ttu-id="846b5-134">Środki trwałe</span><span class="sxs-lookup"><span data-stu-id="846b5-134">Fixed assets</span></span>

<span data-ttu-id="846b5-135">**Kraje i regiony**</span><span class="sxs-lookup"><span data-stu-id="846b5-135">**Countries and regions**</span></span>

<span data-ttu-id="846b5-136">Ta opcja jest dostępna dla następujących krajów i regionów:</span><span class="sxs-lookup"><span data-stu-id="846b5-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="846b5-137">Brazylia</span><span class="sxs-lookup"><span data-stu-id="846b5-137">Brazil</span></span>
- <span data-ttu-id="846b5-138">Chiny</span><span class="sxs-lookup"><span data-stu-id="846b5-138">China</span></span>
- <span data-ttu-id="846b5-139">Czechy</span><span class="sxs-lookup"><span data-stu-id="846b5-139">Czech Republic</span></span>
- <span data-ttu-id="846b5-140">Europa Wschodnia</span><span class="sxs-lookup"><span data-stu-id="846b5-140">Eastern Europe</span></span>
- <span data-ttu-id="846b5-141">Węgry</span><span class="sxs-lookup"><span data-stu-id="846b5-141">Hungary</span></span>
- <span data-ttu-id="846b5-142">Indie</span><span class="sxs-lookup"><span data-stu-id="846b5-142">India</span></span>
- <span data-ttu-id="846b5-143">Japonia</span><span class="sxs-lookup"><span data-stu-id="846b5-143">Japan</span></span>
- <span data-ttu-id="846b5-144">Litwa</span><span class="sxs-lookup"><span data-stu-id="846b5-144">Lithuania</span></span>
- <span data-ttu-id="846b5-145">Łotwa</span><span class="sxs-lookup"><span data-stu-id="846b5-145">Latvia</span></span>
- <span data-ttu-id="846b5-146">Polska</span><span class="sxs-lookup"><span data-stu-id="846b5-146">Poland</span></span>
- <span data-ttu-id="846b5-147">Rosja</span><span class="sxs-lookup"><span data-stu-id="846b5-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="846b5-148">Dodaj tekst do opisów domyślnych</span><span class="sxs-lookup"><span data-stu-id="846b5-148">Add text to default descriptions</span></span>

<span data-ttu-id="846b5-149">Po wykonaniu kroków w procedurze [Ustawianie opisów domyślnych](#set-up-default-descriptions) , opisanej we wcześniejszej sekcji tego tematu, należy wykonać następujące kroki, aby dodać inny tekst do opisu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="846b5-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="846b5-150">Na skróconej karcie **Parametry** wybierz pozycję **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="846b5-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="846b5-151">W polu **Tabela odwołań** zaznacz tabelę bazy danych, z której chcesz dodać do opisu dane parametru.</span><span class="sxs-lookup"><span data-stu-id="846b5-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="846b5-152">W polu **Pole odwołania** zaznacz pole, z którego chcesz dodać do opisu dane parametru.</span><span class="sxs-lookup"><span data-stu-id="846b5-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="846b5-153">Powtórz kroki od 1 do 3, aby dodać więcej parametrów.</span><span class="sxs-lookup"><span data-stu-id="846b5-153">Repeat steps 1 through 3 to add more parameters.</span></span>