---
title: Importowanie plików ISO20022
description: W tym temacie wyjaśniono, jak importować pliki płatności w formatach ISO 20022 camt.054 i pain.002 do Microsoft Dynamics 365 Finance.
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, CustBankAccounts, VendPaymMode, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4ef97d30ca2d8a9c27ce656c82d2a415682ce075
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551228"
---
# <a name="import-iso20022-files"></a><span data-ttu-id="b7bfa-103">Importowanie plików ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-103">Import ISO20022 files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7bfa-104">Można importować pliki płatności mające następujące formaty:</span><span class="sxs-lookup"><span data-stu-id="b7bfa-104">You can import payment files that have the following formats:</span></span>

 - <span data-ttu-id="b7bfa-105">**Zawiadomienie kredytowe ISO20022 camt.054** — importowanie płatności przychodzących z pliku w tym formacie do arkusza płatności odbiorców.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-105">**ISO20022 camt.054 credit advice** – Import incoming payments from a file in this format into the Customer payment journal.</span></span>
 - <span data-ttu-id="b7bfa-106">**Informacja zwrotna o stanie ISO20022 pain.002** i **zawiadomienie debetowe ISO20022 camt.054** — importowanie plików zwrotnych w tych formatach do arkusza przelewów w module Rozrachunki z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-106">**ISO20022 pain.002 status return** and **ISO20022 camt.054 debit advice** – Import return files in these formats into the AP Payment transfer journal.</span></span>

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a><span data-ttu-id="b7bfa-107">Wymagania wstępne dotyczące importowania pliku zawiadomienia kredytowego camt.054</span><span class="sxs-lookup"><span data-stu-id="b7bfa-107">Prerequisites for importing the camt.054 credit advice file</span></span>
<span data-ttu-id="b7bfa-108">Należy wykonać poniższe wymagania wstępne, aby importować komunikaty powiadomień bankowych w formacie camt.054.001.002 do arkusza płatności odbiorców.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-108">You must complete the following prerequisites to import bank notification messages in the camt.054.001.002 format into the Customer payment journal.</span></span>

1. <span data-ttu-id="b7bfa-109">Zaimportuj konfigurację **ISO20022 camt.054** modułu Raportowanie elektroniczne (ER) z usługi Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b7bfa-109">Import the **ISO20022 camt.054** Electronic reporting (ER) configuration from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b7bfa-110">Następnie na stronie **Metoda płatności odbiorcy** w polu **Konfiguracja formatu importu** zaznacz tę konfigurację.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-110">Then, on the **Customer method of payment** page, in the **Import format configuration** field, select that configuration.</span></span> <span data-ttu-id="b7bfa-111">Aby uzyskać więcej informacji, zobacz [Formaty plików metod płatności](emea-select-file-formats-for-the-method-of-payments.md).</span><span class="sxs-lookup"><span data-stu-id="b7bfa-111">For more information, see [File formats for methods of payment](emea-select-file-formats-for-the-method-of-payments.md).</span></span>
2. <span data-ttu-id="b7bfa-112">Na stronie **Wszyscy odbiorcy** wprowadź nazwę i numer organizacji dla każdego odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-112">On the **All customers** page, enter a name and organization number for each customer.</span></span>
3. <span data-ttu-id="b7bfa-113">Na stronie **Konto bankowe odbiorcy** skonfiguruj rekord konta bankowego odbiorcy przez wprowadzenie następujących informacji: numer IBAN lub numer konta bankowego oraz kod SWIFT lub kod banku.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-113">On the **Customer bank account** page, set up a customer bank account record by entering the following information: IBAN or bank account number, and SWIFT code or routing number.</span></span>
4. <span data-ttu-id="b7bfa-114">Na stronie **Konta bankowe** skonfiguruj konta bankowe firmy przez wprowadzenie następujących informacji: numer IBAN lub numer konta bankowego, kod SWIFT lub kod banku, waluta i adres.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-114">On the **Bank accounts** page, set up legal entity bank accounts by entering the following information: IBAN or bank account number, SWIFT code or routing number, currency, and address.</span></span>

   > [!NOTE]
   > <span data-ttu-id="b7bfa-115">Jeśli zamierzasz używać funkcji Zaawansowane uzgadnianie konta bankowego, na skróconej karcie **Uzgodnienie** w opcji **Zaawansowane uzgadnianie konta bankowego** ustaw wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-115">If you plan to use Advanced bank reconciliation, on the **Reconciliation** FastTab, set the **Advanced bank reconciliation** option to **Yes**.</span></span> <span data-ttu-id="b7bfa-116">Jeśli zamierzasz uzgadniać niezaksięgowane importowane płatności, w opcji **Uznaj wyciągi bankowe jako potwierdzenia płatności elektronicznych** ustaw wartość **Tak**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-116">If you plan to reconcile unposted imported payments, set the **Use bank statements as confirmation of electronic payments** option to **Yes**.</span></span>

5. <span data-ttu-id="b7bfa-117">Opcjonalnie: Na stronie **Mapowanie kodu transakcji** skonfiguruj mapowanie między kodami transakcji bankowych w pliku a typami transakcji bankowych.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-117">Optional: On the **Transaction code mapping** page, set up the mapping between bank transaction codes in the file and bank transaction types.</span></span>
6. <span data-ttu-id="b7bfa-118">Jeżeli plik zawiera opłaty za transakcje, które chcesz zaksięgować razem z przychodzącą płatnością, otwórz opłatę od płatności na stronie **Opłata od płatności odbiorcy**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-118">If the file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the **Customer payment fee** page.</span></span> <span data-ttu-id="b7bfa-119">Następnie na stronie **Metody płatności** skojarz opłatę od płatności z kontem bankowym w ustawieniach opłat od płatności.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-119">Then, on the **Methods of payment** page, associate the payment fee with the bank account in the payment fee setup.</span></span>
7. <span data-ttu-id="b7bfa-120">Jeśli będą importowane płatności ESR zawierające odniesienia do dokumentów płatności ISR (dotyczy firm w Szwajcarii), należy wykonać następującą konfigurację:</span><span class="sxs-lookup"><span data-stu-id="b7bfa-120">If ESR payments will be imported and will contain ISR references (applicable for legal entities in Switzerland), complete the following setup:</span></span>

    - <span data-ttu-id="b7bfa-121">W polu **Płatności odbiorcy, długość konta** wprowadź długość kodu odbiorcy, który będzie używany w odniesieniach do dokumentu płatności ISR lub do automatycznej identyfikacji odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-121">In the **Customer payments, account lengths** field, enter the length of the customer code that is used in ISR references or for automatic identification of the customer.</span></span>
    - <span data-ttu-id="b7bfa-122">Upewnij się, że numer odbiorcy i numer faktury (numeracje) zawierają tylko cyfry.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-122">Make sure that the customer number and invoice number (number sequences) contain only digits.</span></span> <span data-ttu-id="b7bfa-123">Nie może w nich być żadnych innych znaków.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-123">They must contain no other characters.</span></span> <span data-ttu-id="b7bfa-124">Numer faktury nie może zawierać zer na początku.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-124">The invoice number must not have leading zeros.</span></span>
    - <span data-ttu-id="b7bfa-125">Wprowadź numery ESR i BESR oraz kod banku dla rachunku bankowego firmy.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-125">Enter the ESR, BESR, and routing number for the legal entity bank account.</span></span> <span data-ttu-id="b7bfa-126">Aby uzyskać więcej informacji, zobacz [Starsza funkcja ESR](emea-che-esr-customer-payments-import.md), ponieważ są wymagane podobne ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-126">For more information, see [legacy ESR feature](emea-che-esr-customer-payments-import.md), because similar settings are required.</span></span>
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a><span data-ttu-id="b7bfa-127">Importowanie pliku zawiadomienia kredytowego camt.054 do arkusza płatności odbiorców</span><span class="sxs-lookup"><span data-stu-id="b7bfa-127">Import the camt.054 credit advice file into the Customer payment journal</span></span>
1. <span data-ttu-id="b7bfa-128">Na stronie **Wiersze arkusza płatności odbiorców** kliknij kolejno opcje **Funkcje** > **Import płatności**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-128">On the **Customer payment journal lines** page, click **Functions** > **Import payments**.</span></span>
2. <span data-ttu-id="b7bfa-129">Wybierz metodę płatności, która ma wymagane ustawienia formatu camt.054 ISO20022.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-129">Select the method of payment that has the required settings for the ISO20022 camt.054 format.</span></span>
3. <span data-ttu-id="b7bfa-130">Określ wymagane parametry i ścieżkę pliku, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-130">Specify the required parameters and the path of the file, and then click **OK**.</span></span> <span data-ttu-id="b7bfa-131">Plik zostanie zaimportowany.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-131">The file is imported.</span></span>

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a><span data-ttu-id="b7bfa-132">Warunki wstępne importowania plików informacji zwrotnej o stanie w formacie ISO20022 pain.002 i zawiadomienia debetowego w formacie ISO20022 camt.054 do arkusza przelewów w module Rozrachunki z dostawcami</span><span class="sxs-lookup"><span data-stu-id="b7bfa-132">Prerequisites for importing files in the pain.002 status return and camt.054 debit advice formats into the AP Payment transfer journal</span></span>
<span data-ttu-id="b7bfa-133">Należy spełnić poniższe warunki wstępne, aby importować komunikaty bankowe w następujących formatach ISO20022 do strony **Przelew do dostawcy**: komunikaty zwrotne o stanie pain.002.001.003 i zawiadomienia debetowe camt.054.001.002.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-133">You must complete the following prerequisites to import bank messages in the following ISO20022 formats to the **Vendor payment transfer** page: pain.002.001.003 status return messages and camt.054.001.002 debit advice.</span></span>

1. <span data-ttu-id="b7bfa-134">Zaimportuj konfiguracje ER **ISO20022 camt.054** i **ISO20022 pain.002** z usługi LCS.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-134">Import the **ISO20022 camt.054** and **ISO20022 pain.002** ER configurations from LCS.</span></span>
2. <span data-ttu-id="b7bfa-135">Na stronie **Metoda płatności dostawcy** w polach **Konfiguracja formatu zwrotnego** i **Pomocnicza konfiguracja formatu zwrotnego** zaznacz zaimportowane konfiguracje modułu ER.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-135">On the **Vendor method of payment** page, in the **Return format configuration** and **Return format secondary configuration** fields, select the ER configurations that you imported.</span></span> <span data-ttu-id="b7bfa-136">Trzeba będzie aktywować standardowy format elektroniczny informacji zwrotnych dla wybranej metody płatności.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-136">You will have to activate the generic electronic return format for the selected method of payment.</span></span>
3. <span data-ttu-id="b7bfa-137">Na stronie **Mapowanie stanu formatu zwrotnego** skonfiguruj mapowanie kodów stanu między stanami formatu pain.002 a stanami arkusza płatności dostawców.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-137">On the **Return format status mapping** page, set up the mapping of status codes between pain.002 statuses and Vendor payment journal statuses.</span></span>

    <span data-ttu-id="b7bfa-138">Oto przykład konfiguracji stanów.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-138">Here is an example of a status setup.</span></span>

    <span data-ttu-id="b7bfa-139">Stan zwrotu</span><span class="sxs-lookup"><span data-stu-id="b7bfa-139">Return status</span></span> | <span data-ttu-id="b7bfa-140">Stan płatności</span><span class="sxs-lookup"><span data-stu-id="b7bfa-140">Payment status</span></span>
    --------------|---------------
    <span data-ttu-id="b7bfa-141">RJCT</span><span class="sxs-lookup"><span data-stu-id="b7bfa-141">RJCT</span></span>          | <span data-ttu-id="b7bfa-142">Odrzucona</span><span class="sxs-lookup"><span data-stu-id="b7bfa-142">Rejected</span></span>
    <span data-ttu-id="b7bfa-143">ACCP</span><span class="sxs-lookup"><span data-stu-id="b7bfa-143">ACCP</span></span>          | <span data-ttu-id="b7bfa-144">Zaakceptowany</span><span class="sxs-lookup"><span data-stu-id="b7bfa-144">Accepted</span></span>
    <span data-ttu-id="b7bfa-145">ACSP</span><span class="sxs-lookup"><span data-stu-id="b7bfa-145">ACSP</span></span>          | <span data-ttu-id="b7bfa-146">Odebrane</span><span class="sxs-lookup"><span data-stu-id="b7bfa-146">Received</span></span>

4. <span data-ttu-id="b7bfa-147">Na stronie **Kody błędów formatu zwrotnego** skonfiguruj kody błędów i opisy formatu pain.002 kody zgodnie z zewnętrznymi kodami przyczyn stanu w standardzie ISO20022.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-147">On the **Return format error codes** page, set up pain.002 error codes and descriptions in accordance with external ISO20022 status reason codes.</span></span>

    <span data-ttu-id="b7bfa-148">Poniżej przedstawiono przykład częściowej konfiguracji kodów błędów.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-148">Here is an example of part of an error code setup.</span></span>

    <span data-ttu-id="b7bfa-149">Kod</span><span class="sxs-lookup"><span data-stu-id="b7bfa-149">Code</span></span> | <span data-ttu-id="b7bfa-150">Nazwisko</span><span class="sxs-lookup"><span data-stu-id="b7bfa-150">Name</span></span>
    -----|-----
    <span data-ttu-id="b7bfa-151">AC01</span><span class="sxs-lookup"><span data-stu-id="b7bfa-151">AC01</span></span> | <span data-ttu-id="b7bfa-152">IncorrectAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7bfa-152">IncorrectAccountNumber</span></span>
    <span data-ttu-id="b7bfa-153">AC02</span><span class="sxs-lookup"><span data-stu-id="b7bfa-153">AC02</span></span> | <span data-ttu-id="b7bfa-154">InvalidDebtorAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7bfa-154">InvalidDebtorAccountNumber</span></span>
    <span data-ttu-id="b7bfa-155">AC03</span><span class="sxs-lookup"><span data-stu-id="b7bfa-155">AC03</span></span> | <span data-ttu-id="b7bfa-156">InvalidCreditorAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7bfa-156">InvalidCreditorAccountNumber</span></span>
    <span data-ttu-id="b7bfa-157">AC04</span><span class="sxs-lookup"><span data-stu-id="b7bfa-157">AC04</span></span> | <span data-ttu-id="b7bfa-158">ClosedAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7bfa-158">ClosedAccountNumber</span></span>
    <span data-ttu-id="b7bfa-159">AC05</span><span class="sxs-lookup"><span data-stu-id="b7bfa-159">AC05</span></span> | <span data-ttu-id="b7bfa-160">ClosedDebtorAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b7bfa-160">ClosedDebtorAccountNumber</span></span>
    <span data-ttu-id="b7bfa-161">AC06</span><span class="sxs-lookup"><span data-stu-id="b7bfa-161">AC06</span></span> | <span data-ttu-id="b7bfa-162">BlockedAccount</span><span class="sxs-lookup"><span data-stu-id="b7bfa-162">BlockedAccount</span></span>

5. <span data-ttu-id="b7bfa-163">Jeżeli plik camt.054 zawiera opłaty za transakcje, które chcesz zaksięgować razem z przychodzącą płatnością, otwórz opłatę od płatności na stronie **Opłata od płatności dostawcy**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-163">If the camt.054 file contains transaction charges that you want to post together with the incoming payment, create a payment fee on the **Vendor payment fee** page.</span></span> <span data-ttu-id="b7bfa-164">Następnie na stronie **Metody płatności** skojarz opłatę od płatności z kontem bankowym w ustawieniach opłat od płatności.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-164">Then, on the **Methods of payment** page, associate the payment fee with the bank account in the payment fee setup.</span></span>

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a><span data-ttu-id="b7bfa-165">Importowanie plików informacji zwrotnej o stanie pain.002 lub zawiadomienia debetowego camt.054 do arkusza płatności dostawców</span><span class="sxs-lookup"><span data-stu-id="b7bfa-165">Import the pain.002 status return or camt.054 debit advice files into the Vendor payment journal</span></span>
1. <span data-ttu-id="b7bfa-166">Otwórz stronę **Przelewy** stronę w menu modułu Rozrachunki z dostawcami.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-166">Open the **Payment transfers** page in Accounts Payable menu.</span></span>
2. <span data-ttu-id="b7bfa-167">Na stronie **Przelewy** kliknij opcję **Plik zwrotny — Dostawca**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-167">On the **Payment transfers** page, click **Return file - vendor**.</span></span>
3. <span data-ttu-id="b7bfa-168">Wybierz metodę płatności, która ma wymagane ustawienia plików formatu ISO20022, i kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-168">Select the method of payment that has the required settings for ISO20022 files, and then click **OK**.</span></span>
4. <span data-ttu-id="b7bfa-169">Zaznacz format pliku, który chcesz zaimportować, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-169">Select the file format that you plan to import, and then click **OK**.</span></span>
5. <span data-ttu-id="b7bfa-170">Określ wymagane parametry i ścieżkę pliku, a następnie kliknij przycisk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-170">Specify the required parameters and the path of the file, and then click **OK**.</span></span>

<span data-ttu-id="b7bfa-171">Jeśli importujesz plik pain.002, stan wierszy płatności do dostawców zostanie zaktualizowany zgodnie z informacjami w importowanym pliku.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-171">If you're importing the pain.002 file, the status of vendor payment lines is updated, based the information in the imported file.</span></span>

<span data-ttu-id="b7bfa-172">W przypadku importowania pliku camt.054 należy określić następujące dodatkowe parametry:</span><span class="sxs-lookup"><span data-stu-id="b7bfa-172">If you're importing the camt.054 file, you should specify the following additional parameters:</span></span>

- <span data-ttu-id="b7bfa-173">**Identyfikator opłaty** — wprowadź identyfikator opłaty, który będzie definiował nowe wiersze opłat od płatności tworzone w wierszu arkusza płatności dostawców w przypadku, gdy plik camt.054 zawiera kwotę opłaty.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-173">**Fee ID** – Enter the Fee ID which will define new payment fee lines, which will be created on the Vendor payment journal line if a charge amount is present in the camt.054 file.</span></span>
- <span data-ttu-id="b7bfa-174">**Nazwa nowego arkusza** i **Opis nowego arkusza** — wprowadź nazwę i opis arkusza, do którego będą przenoszone przetworzone transakcje.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-174">**New journal name** and **New journal description** – Enter the name and description of the journal that processed transactions will be transferred to.</span></span> <span data-ttu-id="b7bfa-175">Po przeniesieniu w nowym arkuszu powinny zostać przypisane nowe numery załączników.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-175">After the transfer, new voucher numbers should be assigned in the new journal.</span></span>
- <span data-ttu-id="b7bfa-176">**Importuj transakcje poleceń zapłaty** — ustaw w tej opcji wartość **Tak**, jeśli wychodzące polecenia zapłaty muszą być importowane do arkusza płatności dostawców.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-176">**Import direct debit transactions** – Set this option to **Yes** if outgoing direct debits must be imported into the Vendor payment journal.</span></span>
- <span data-ttu-id="b7bfa-177">**Nazwa arkusza** — podaj nazwę nowego arkusza na importowane transakcje polecenia zapłaty.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-177">**Journal name** – Define a new journal name for the imported direct debit transactions.</span></span>
- <span data-ttu-id="b7bfa-178">**Rozlicz transakcje** — ustaw w tej opcji wartość **Tak**, jeśli importowane płatności do dostawców muszą być rozliczane względem faktur znajdujących się w systemie.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-178">**Settle transactions** – Set this option to **Yes** if imported vendor payments must be settled with invoices that are found in the system.</span></span>

<span data-ttu-id="b7bfa-179">Zaimportowane informacje można przejrzeć na stronie **Przelewy**.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-179">You can view the imported information on the **Payment transfers** page.</span></span> 

## <a name="additional-details"></a><span data-ttu-id="b7bfa-180">Dodatkowe szczegóły</span><span class="sxs-lookup"><span data-stu-id="b7bfa-180">Additional details</span></span>

<span data-ttu-id="b7bfa-181">Podczas importowania konfiguracji formatu z usługi LCS importujesz całe drzewo konfiguracja, a więc również konfiguracje modelu i mapowania modelu.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-181">When you import a format configuration from LCS, you import the whole configuration tree which means that the Model and Model mapping configurations are included.</span></span> <span data-ttu-id="b7bfa-182">W modelu płatności począwszy od wersji 8 mapowania znajdują się w oddzielnych konfiguracjach raportowania elektronicznego w drzewie rozwiązania (Mapowanie modelu płatności 1611, Mapowanie modelu płatności do lokalizacji docelowej ISO20022 itp.).</span><span class="sxs-lookup"><span data-stu-id="b7bfa-182">In the Payment model starting from version 8, the mappings are located in separate ER configurations in the solution tree (Payment model mapping 1611, Payment model mapping to destination ISO20022, etc).</span></span> <span data-ttu-id="b7bfa-183">W jednym modelu (modelu płatności) istnieje wiele różnych formatów płatności, dlatego oddzielna obsługa mapowań jest kluczowa dla łatwego zarządzania rozwiązaniem.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-183">There are many different payment formats under one model (Payment model), thus separate mapping handling is a key for easy solution maintenance.</span></span> <span data-ttu-id="b7bfa-184">Rozważmy na przykład następujący scenariusz: używasz płatności ISO20022 do generowania plików poleceń przelewu, a następnie importujesz komunikaty zwrotne z banku.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-184">For example, consider this scenario: you use ISO20022 payments to generate credit transfer files and then you import the return messages from the bank.</span></span> <span data-ttu-id="b7bfa-185">W tym scenariuszu należy korzystać z następujących konfiguracji:</span><span class="sxs-lookup"><span data-stu-id="b7bfa-185">In this scenario, you should use the following configurations:</span></span>

 - <span data-ttu-id="b7bfa-186">**Model płatności**</span><span class="sxs-lookup"><span data-stu-id="b7bfa-186">**Payment model**</span></span>
 - <span data-ttu-id="b7bfa-187">**Mapowanie modelu płatności 1611** — to mapowanie będzie używane do generowania pliku eksportu</span><span class="sxs-lookup"><span data-stu-id="b7bfa-187">**Payment model mapping 1611** – this mapping will be used to generate the export file</span></span>
 - <span data-ttu-id="b7bfa-188">**Mapowanie modelu płatności do lokalizacji docelowej ISO20022** — ta konfiguracja zawiera wszystkie mapowania, które będą używane do importowania danych (kierunek mapowania „do lokalizacji docelowej”)</span><span class="sxs-lookup"><span data-stu-id="b7bfa-188">**Payment model mapping to destination ISO20022** – this configuration includes all mappings which will be used to import the data (“to destination” mapping direction)</span></span>
 - <span data-ttu-id="b7bfa-189">**Polecenie przelewu ISO20022** — ta konfiguracja zawiera składnik formatu odpowiedzialny za generowanie pliku eksportu (pain.001) na podstawie konfiguracji Mapowanie modelu płatności 1611, a także format do modelowania składnika mapowania, który będzie używany razem z konfiguracją Mapowanie modelu płatności do lokalizacji docelowej ISO20022 w celu rejestrowania wyeksportowanych płatności w systemie na potrzeby dalszego importu (import w tabeli technicznej CustVendProcessedPayments)</span><span class="sxs-lookup"><span data-stu-id="b7bfa-189">**ISO20022 Credit transfer** – this configuration includes a format component that is responsible for export file generation (pain.001) based on the Payment model mapping 1611, as well as a format to model mapping component which will be used together with Payment model mapping to destination ISO20022 to register exported payments in the system for further import purposes (import in CustVendProcessedPayments technical table)</span></span>
 - <span data-ttu-id="b7bfa-190">**Polecenie przelewu ISO20022 (CE)**, gdzie CE odpowiada rozszerzeniu kraju — format pochodny od formatu Polecenie przelewu ISO20022 z taką samą strukturą i pewnymi różnicami specyficznymi dla krajów</span><span class="sxs-lookup"><span data-stu-id="b7bfa-190">**ISO20022 Credit transfer (CE)**, where CE correspond to country extension – derived format to the ISO20022 Credit transfer with the same structure and with certain country-specific differences</span></span>
 - <span data-ttu-id="b7bfa-191">**Pain.002** — ten format zostanie użyty wraz z konfiguracją Mapowanie modelu płatności do lokalizacji docelowej ISO20022 w celu zaimportowania pliku pain.002 do arkusza przeniesień płatności dostawców</span><span class="sxs-lookup"><span data-stu-id="b7bfa-191">**Pain.002** – this format will be used together with the Payment model mapping to destination ISO20022 in order to import the pain.002 file into vendor payments transfers journal</span></span>
 - <span data-ttu-id="b7bfa-192">**Camt.054** — ten format zostanie użyty wraz z konfiguracją Mapowanie modelu płatności do lokalizacji docelowej ISO20022 w celu zaimportowania pliku camt.054 do arkusza przeniesień płatności dostawców</span><span class="sxs-lookup"><span data-stu-id="b7bfa-192">**Camt.054** – this format will be used together with the Payment model mapping to destination ISO20022 to import the camt.054 file into vendor payments transfers journal.</span></span> <span data-ttu-id="b7bfa-193">Ta sama konfiguracja formatu będzie używana w funkcji importowania płatności odbiorców, ale inne mapowanie będzie używane w konfiguracji Mapowanie modelu płatności do lokalizacji docelowej ISO20022.</span><span class="sxs-lookup"><span data-stu-id="b7bfa-193">The same format configuration will be used in customer payments import functionality, but the different mapping will be used in the Payment model mapping to destination ISO20022 configuration.</span></span>

<span data-ttu-id="b7bfa-194">Aby uzyskać więcej informacji na temat raportowania elektronicznego, zobacz [Omówienie raportowania elektronicznego](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b7bfa-194">For more information about Electronic reporting, refer to [Electronic reporting overview](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7bfa-195">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="b7bfa-195">Additional resources</span></span>
- [<span data-ttu-id="b7bfa-196">Tworzenie i eksport płatności dla dostawcy przy użyciu formatu płatności ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-196">Create and export vendor payments using ISO20022 payment format</span></span>](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [<span data-ttu-id="b7bfa-197">Importowanie konfiguracji polecenia przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-197">Import ISO20022 credit transfer configuration</span></span>](./tasks/import-iso20022-credit-transfer-configuration.md)
- [<span data-ttu-id="b7bfa-198">Importowanie konfiguracji polecenia zapłaty ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-198">Import ISO20022 direct debit configuration</span></span>](./tasks/import-iso20022-direct-debit-configuration.md)
- [<span data-ttu-id="b7bfa-199">Konfigurowanie kont bankowych firmy dla poleceń przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-199">Set up company bank accounts for ISO20022 credit transfers</span></span>](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [<span data-ttu-id="b7bfa-200">Konfigurowanie kont bankowych firmy dla poleceń zapłaty ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-200">Set up company bank accounts for ISO20022 direct debits</span></span>](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [<span data-ttu-id="b7bfa-201">Konfigurowanie odbiorców i kont bankowych odbiorców dla poleceń zapłaty ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-201">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [<span data-ttu-id="b7bfa-202">Konfigurowanie metody płatności przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-202">Set up method of payment for ISO20022 credit transfer</span></span>](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [<span data-ttu-id="b7bfa-203">Konfigurowanie metody płatności polecenia zapłaty ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-203">Set up method of payment for ISO20022 direct debit</span></span>](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [<span data-ttu-id="b7bfa-204">Konfigurowanie dostawców i kont bankowych dostawców dla poleceń przelewu ISO20022</span><span class="sxs-lookup"><span data-stu-id="b7bfa-204">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>](./tasks/set-up-vendor-iso20022-credit-transfers.md)