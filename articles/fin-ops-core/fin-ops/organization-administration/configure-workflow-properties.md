---
title: Konfigurowanie właściwości przepływu pracy
description: W tym temacie wyjaśniono sposób konfigurowania różnych właściwości przepływu pracy.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190127"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="948c2-103">Konfigurowanie właściwości przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="948c2-104">W tym temacie wyjaśniono sposób konfigurowania różnych właściwości przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="948c2-105">Aby skonfigurować właściwości przepływu pracy, otwórz przepływ pracy w edytorze przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="948c2-106">Kliknij w obszarze roboczym edytora przepływu pracy, a następnie kliknij przycisk **Właściwości**, aby otworzyć stronę **Właściwości**.</span><span class="sxs-lookup"><span data-stu-id="948c2-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="948c2-107">Można użyć poniższych procedur, aby skonfigurować różne właściwości przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="948c2-108">Nadawanie nazwy przepływowi pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-108">Name the workflow</span></span>

<span data-ttu-id="948c2-109">Należy wykonać następujące kroki, aby wprowadzić nazwę przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="948c2-110">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="948c2-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="948c2-111">W polu **Nazwa** wprowadź unikatową nazwę przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="948c2-112">Na przykład jeśli tworzysz przepływ pracy zapotrzebowania na zakup dla każdego kraju lub regionu, w którym działa firma, można nazwać przepływy **Zapotrzebowania na zakup — Dania** lub **Zapotrzebowania na zakup — Hiszpania**.</span><span class="sxs-lookup"><span data-stu-id="948c2-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="948c2-113">Określanie właściciela przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-113">Specify the workflow owner</span></span>

<span data-ttu-id="948c2-114">Właściciel przepływu pracy jest osobą, która zarządza przepływem pracy i obsługuje go.</span><span class="sxs-lookup"><span data-stu-id="948c2-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="948c2-115">Aby określić właściciela przepływu pracy, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="948c2-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="948c2-116">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="948c2-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="948c2-117">Na liście **Właściciel** zaznacz nazwę osoby, która będzie zarządzać przepływem pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="948c2-118">Wybór szablonu wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="948c2-118">Select an email template</span></span>

<span data-ttu-id="948c2-119">Wykonaj następujące kroki, aby wybrać szablon wiadomości e-mail, który będzie używany do generowania komunikatów powiadomień dotyczących przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="948c2-120">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="948c2-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="948c2-121">Na liście **Szablon wiadomości e-mail dla powiadomień o przepływie pracy** zaznacz szablon.</span><span class="sxs-lookup"><span data-stu-id="948c2-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="948c2-122">Wprowadzanie instrukcji dla użytkowników</span><span class="sxs-lookup"><span data-stu-id="948c2-122">Enter instructions for users</span></span>

<span data-ttu-id="948c2-123">Istnieje możliwość udostępniania instrukcji użytkownikom, którzy będą przesyłać dokumenty do przetwarzania i zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="948c2-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="948c2-124">Ci użytkownicy są również zwani *inicjatorami*.</span><span class="sxs-lookup"><span data-stu-id="948c2-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="948c2-125">Na przykład tworzysz przepływ pracy zapotrzebowania na zakup i wprowadzasz instrukcje.</span><span class="sxs-lookup"><span data-stu-id="948c2-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="948c2-126">Te instrukcje mogą być wyświetlane przez użytkowników wprowadzających zapotrzebowania na zakup na stronie **Zapotrzebowania na zakup**.</span><span class="sxs-lookup"><span data-stu-id="948c2-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="948c2-127">Aby wyświetlić instrukcje, inicjator klika ikonę na pasku komunikatów przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="948c2-128">Aby wprowadzić instrukcje dla użytkowników, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="948c2-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="948c2-129">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="948c2-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="948c2-130">W polu **Instrukcje przesyłania** wprowadź instrukcje.</span><span class="sxs-lookup"><span data-stu-id="948c2-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="948c2-131">Aby spersonalizować instrukcje, możesz wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="948c2-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="948c2-132">Podczas wyświetlania instrukcji użytkownikom symbole zastępcze są zastępowane odpowiednimi danymi.</span><span class="sxs-lookup"><span data-stu-id="948c2-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="948c2-133">Aby wstawić symbol zastępczy, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="948c2-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="948c2-134">Kliknij w polu **Instrukcje przesyłania**, aby określić miejsce wyświetlania symbolu zastępczego.</span><span class="sxs-lookup"><span data-stu-id="948c2-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="948c2-135">Kliknij opcję **Wstaw symbol zastępczy**.</span><span class="sxs-lookup"><span data-stu-id="948c2-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="948c2-136">Na wyświetlonej liście wybierz symbol zastępczy, który chcesz wstawić.</span><span class="sxs-lookup"><span data-stu-id="948c2-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="948c2-137">Kliknij przycisk **Wstaw**.</span><span class="sxs-lookup"><span data-stu-id="948c2-137">Click **Insert**.</span></span>

4. <span data-ttu-id="948c2-138">Aby dodać tłumaczenia instrukcji, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="948c2-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="948c2-139">Kliknij opcję **Tłumaczenia**.</span><span class="sxs-lookup"><span data-stu-id="948c2-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="948c2-140">Na wyświetlonej stronie kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="948c2-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="948c2-141">Z wyświetlonej listy wybierz język, w którym będziesz wprowadzać tekst.</span><span class="sxs-lookup"><span data-stu-id="948c2-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="948c2-142">W polu **Przetłumaczony tekst** wprowadź tekst.</span><span class="sxs-lookup"><span data-stu-id="948c2-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="948c2-143">Aby spersonalizować tekst, możesz wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="948c2-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="948c2-144">Aby uzyskać instrukcje dotyczące sposobu wprowadzania symbolu zastępczego, zobacz krok 3.</span><span class="sxs-lookup"><span data-stu-id="948c2-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="948c2-145">Kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="948c2-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="948c2-146">Określanie, kiedy jest używany ten przepływ pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-146">Specify when this workflow is used</span></span>

<span data-ttu-id="948c2-147">Można utworzyć wiele przepływów pracy opartych na tym samym typie.</span><span class="sxs-lookup"><span data-stu-id="948c2-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="948c2-148">Na przykład można utworzyć przepływ pracy zapotrzebowania na zakup dla każdego kraju lub regionu, w którym działa firma, na przykład Zapotrzebowania na zakup — Dania lub Zapotrzebowania na zakup — Hiszpania.</span><span class="sxs-lookup"><span data-stu-id="948c2-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="948c2-149">Jeśli istnieje wiele przepływów pracy opartych na tym samym typie, trzeba określić warunki używania poszczególnych przepływów pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="948c2-150">Dla poprzedniego przykładu należałoby określić następujące warunki:</span><span class="sxs-lookup"><span data-stu-id="948c2-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="948c2-151">Zapotrzebowania na zakup — Dania jest używany, gdy krajem/regionem jest DK.</span><span class="sxs-lookup"><span data-stu-id="948c2-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="948c2-152">Zapotrzebowania na zakup — Hiszpania jest używany, gdy krajem/regionem jest ES.</span><span class="sxs-lookup"><span data-stu-id="948c2-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="948c2-153">Aby określić, kiedy ma być używany konfigurowany przepływ pracy, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="948c2-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="948c2-154">W lewym okienku kliknij opcję **Aktywacja**.</span><span class="sxs-lookup"><span data-stu-id="948c2-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="948c2-155">Zaznacz pole wyboru **Ustaw warunki uruchamiania tego przepływu pracy**.</span><span class="sxs-lookup"><span data-stu-id="948c2-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="948c2-156">Kliknij opcję **Dodaj warunek**.</span><span class="sxs-lookup"><span data-stu-id="948c2-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="948c2-157">Służy do wprowadzania warunku.</span><span class="sxs-lookup"><span data-stu-id="948c2-157">Enter a condition.</span></span>
5. <span data-ttu-id="948c2-158">Wprowadź wszelkie wymagane dodatkowe warunki.</span><span class="sxs-lookup"><span data-stu-id="948c2-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="948c2-159">Aby sprawdzić, czy wprowadzone warunki są poprawnie ustawione, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="948c2-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="948c2-160">Kliknij przycisk **Test**.</span><span class="sxs-lookup"><span data-stu-id="948c2-160">Click **Test**.</span></span>
    2. <span data-ttu-id="948c2-161">Na stronie **Warunek testowy przepływu pracy** w obszarze **Sprawdź poprawność warunku** wybierz rekord.</span><span class="sxs-lookup"><span data-stu-id="948c2-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="948c2-162">Kliknij przycisk **Test**.</span><span class="sxs-lookup"><span data-stu-id="948c2-162">Click **Test**.</span></span> <span data-ttu-id="948c2-163">System oszacuje rekord i określi, czy rekord spełnia określone warunki.</span><span class="sxs-lookup"><span data-stu-id="948c2-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="948c2-164">Na przykład jeśli tworzysz przepływ pracy zapotrzebowania na zakup dla Hiszpanii, obszar **Sprawdź poprawność warunku** na stronie zawiera listę zapotrzebowań na zakup.</span><span class="sxs-lookup"><span data-stu-id="948c2-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="948c2-165">Kliknięcie przycisku **Test** spowoduje uruchomienie systemowego szacowania wybranego zapotrzebowania na zakup w celu sprawdzenia, czy krajem/regionem jest ES.</span><span class="sxs-lookup"><span data-stu-id="948c2-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="948c2-166">Kliknij przycisk **OK** lub **Anuluj**, aby powrócić do strony **Właściwości**.</span><span class="sxs-lookup"><span data-stu-id="948c2-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="948c2-167">Określanie, kiedy są wysyłane powiadomienia</span><span class="sxs-lookup"><span data-stu-id="948c2-167">Specify when notifications are sent</span></span>

<span data-ttu-id="948c2-168">Podczas przesyłania dokumentu do przetwarzania tworzone jest wystąpienie przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="948c2-169">Można wysyłać powiadomienia do użytkowników, gdy wystąpienia przepływu pracy oparte na przepływie pracy są uruchamiane, kończone, przerywane lub zatrzymane z powodu błędu.</span><span class="sxs-lookup"><span data-stu-id="948c2-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="948c2-170">Aby określić, kiedy są wysyłane powiadomienia, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="948c2-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="948c2-171">W lewym okienku kliknij opcję **Powiadomienia**.</span><span class="sxs-lookup"><span data-stu-id="948c2-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="948c2-172">Zaznacz pole wyboru dla każdego zdarzenia, które powinno uruchamiać powiadomienia:</span><span class="sxs-lookup"><span data-stu-id="948c2-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="948c2-173">**Rozpoczęte** — wysyłanie powiadomień po uruchomieniu wystąpienia przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="948c2-174">**Zatrzymane** — wysyłanie powiadomień, gdy wystąpienie przepływu pracy zostało zatrzymane z powodu błędu.</span><span class="sxs-lookup"><span data-stu-id="948c2-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="948c2-175">**Ukończono** — wysyłanie powiadomień po zakończeniu wystąpienia przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="948c2-176">**Nieodwracalne** — wysyłanie powiadomień, gdy wystąpienie przepływu pracy zostało zatrzymane z powodu nieodwracalnego błędu.</span><span class="sxs-lookup"><span data-stu-id="948c2-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="948c2-177">**Przerwane** — wysyłanie powiadomień po przerwaniu wystąpienia przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="948c2-178">Zaznacz wiersz zdarzenia wybranego w kroku 2.</span><span class="sxs-lookup"><span data-stu-id="948c2-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="948c2-179">Na karcie **Tekst powiadomienia** wprowadź tekst powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="948c2-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="948c2-180">Aby spersonalizować tekst, możesz wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="948c2-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="948c2-181">Podczas wyświetlania tekstu użytkownikom symbole zastępcze są zastępowane odpowiednimi danymi.</span><span class="sxs-lookup"><span data-stu-id="948c2-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="948c2-182">Aby wstawić symbol zastępczy, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="948c2-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="948c2-183">Kliknij w polu, aby określić miejsce wyświetlania symbolu zastępczego.</span><span class="sxs-lookup"><span data-stu-id="948c2-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="948c2-184">Kliknij opcję **Wstaw symbol zastępczy**.</span><span class="sxs-lookup"><span data-stu-id="948c2-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="948c2-185">Na wyświetlonej liście wybierz symbol zastępczy, który chcesz wstawić.</span><span class="sxs-lookup"><span data-stu-id="948c2-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="948c2-186">Kliknij przycisk **Wstaw**.</span><span class="sxs-lookup"><span data-stu-id="948c2-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="948c2-187">Popularnym dołączanym elementem zastępczym **Tekst powiadomienia** jest „Ostatnie uwagi: %Workflow.Last note%”, który pokazuje wszystkie komentarze z poprzedniego kroku.</span><span class="sxs-lookup"><span data-stu-id="948c2-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="948c2-188">Aby dodać tłumaczenia tekstu, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="948c2-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="948c2-189">Kliknij opcję **Tłumaczenia**.</span><span class="sxs-lookup"><span data-stu-id="948c2-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="948c2-190">Na wyświetlonej stronie kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="948c2-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="948c2-191">Z wyświetlonej listy wybierz język, w którym będziesz wprowadzać tekst.</span><span class="sxs-lookup"><span data-stu-id="948c2-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="948c2-192">W polu **Przetłumaczony tekst** wprowadź tekst.</span><span class="sxs-lookup"><span data-stu-id="948c2-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="948c2-193">Aby spersonalizować tekst, możesz wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="948c2-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="948c2-194">Aby uzyskać instrukcje dotyczące sposobu wprowadzania symbolu zastępczego, zobacz krok 5.</span><span class="sxs-lookup"><span data-stu-id="948c2-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="948c2-195">Kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="948c2-195">Click **Close**.</span></span>

7. <span data-ttu-id="948c2-196">Na karcie **Adresat** użyj poniższych opcji do określenia, kto ma otrzymywać powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="948c2-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="948c2-197">Opcja</span><span class="sxs-lookup"><span data-stu-id="948c2-197">Option</span></span></th>
    <th><span data-ttu-id="948c2-198">Powiadomienia są tym użytkownikom</span><span class="sxs-lookup"><span data-stu-id="948c2-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="948c2-199">Aby wysyłać powiadomienia, należy wykonać następujące czynności</span><span class="sxs-lookup"><span data-stu-id="948c2-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="948c2-200">Uczestnik</span><span class="sxs-lookup"><span data-stu-id="948c2-200">Participant</span></span></td>
    <td><span data-ttu-id="948c2-201">Użytkownicy, którzy są przypisani do określonej grupy lub roli</span><span class="sxs-lookup"><span data-stu-id="948c2-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="948c2-202">Na karcie <strong>Odbiorcy</strong> kliknij przycisk <strong>Uczestnik</strong>.</span><span class="sxs-lookup"><span data-stu-id="948c2-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="948c2-203">Na karcie <strong>Oparte na</strong> na liście <strong>Typ uczestnika</strong> wybierz typ grupy lub roli, do której mają być wysyłane powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="948c2-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="948c2-204">Na liście <strong>Uczestnik</strong> wybierz grupę lub rolę, do której mają być wysyłane powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="948c2-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="948c2-205">Użytkownik przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-205">Workflow user</span></span></td>
    <td><span data-ttu-id="948c2-206">Użytkownicy będący uczestnikami tego przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="948c2-207">Na karcie <strong>Odbiorcy</strong> kliknij przycisk <strong>Użytkownik przepływu pracy</strong>.</span><span class="sxs-lookup"><span data-stu-id="948c2-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="948c2-208">Na karcie <strong>Użytkownik przepływu pracy</strong> na liście <strong>Użytkownik przepływu pracy</strong> wybierz uczestnika w tym przepływie pracy.</span><span class="sxs-lookup"><span data-stu-id="948c2-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="948c2-209">Użytkownik</span><span class="sxs-lookup"><span data-stu-id="948c2-209">User</span></span></td>
    <td><span data-ttu-id="948c2-210">Określeni użytkownicy</span><span class="sxs-lookup"><span data-stu-id="948c2-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="948c2-211">Na karcie <strong>Odbiorcy</strong> kliknij przycisk <strong>Użytkownik</strong>.</span><span class="sxs-lookup"><span data-stu-id="948c2-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="948c2-212">Na karcie <strong>Użytkownik</strong> lista <strong>Dostępni użytkownicy</strong> zawiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="948c2-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="948c2-213">Wybierz użytkowników, którym chcesz wysyłać powiadomienia, a następnie przenieś tych użytkowników do listy <strong>Wybrani użytkownicy</strong>.</span><span class="sxs-lookup"><span data-stu-id="948c2-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="948c2-214">Powtórz kroki od 3 do 7 dla każdego zdarzenia wybranego w kroku 2.</span><span class="sxs-lookup"><span data-stu-id="948c2-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="948c2-215">Wprowadzanie komentarzy dotyczących zmian zastosowanych w przepływie pracy</span><span class="sxs-lookup"><span data-stu-id="948c2-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="948c2-216">Aby wprowadzić komentarze dotyczące zmian zastosowanych w przepływie pracy, należy wykonać następujące kroki.</span><span class="sxs-lookup"><span data-stu-id="948c2-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="948c2-217">W lewym okienku kliknij opcję **Uwagi**.</span><span class="sxs-lookup"><span data-stu-id="948c2-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="948c2-218">W polu **Wprowadź komentarze dotyczące przepływu pracy** wprowadź komentarze.</span><span class="sxs-lookup"><span data-stu-id="948c2-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="948c2-219">Przejrzyj wprowadzone komentarze.</span><span class="sxs-lookup"><span data-stu-id="948c2-219">Review your comments.</span></span> <span data-ttu-id="948c2-220">Po dodaniu komentarzy nie można ich modyfikować.</span><span class="sxs-lookup"><span data-stu-id="948c2-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="948c2-221">Kliknij przycisk **Dodaj**, aby dodać komentarze do obszaru **Historia komentarzy**.</span><span class="sxs-lookup"><span data-stu-id="948c2-221">Click **Add** to add your comments to the **Comment history** area.</span></span>