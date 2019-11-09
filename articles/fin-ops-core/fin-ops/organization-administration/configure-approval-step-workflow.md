---
title: Konfigurowanie kroków zatwierdzania w przepływie pracy
description: W tym temacie wyjaśniono sposób konfigurowania właściwości kroku zatwierdzania.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5bd5300a061e12ccabdea83c20863c95e15fe19
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179500"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="1e49e-103">Konfigurowanie kroków zatwierdzania w przepływie pracy</span><span class="sxs-lookup"><span data-stu-id="1e49e-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e49e-104">W tym temacie wyjaśniono sposób konfigurowania właściwości kroku zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="1e49e-105">Aby skonfigurować krok zatwierdzania, w edytorze przepływu pracy kliknij krok zatwierdzania prawym przyciskiem myszy i wybierz polecenie **Właściwości**, a zostanie otwarta strona **Właściwości**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="1e49e-106">Następnie za pomocą procedur zamieszczonych niżej skonfiguruj właściwości kroku zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="1e49e-107">Nadawanie nazwy krokowi</span><span class="sxs-lookup"><span data-stu-id="1e49e-107">Name the step</span></span>
<span data-ttu-id="1e49e-108">Wykonaj następujące kroki, aby wprowadzić nazwę kroku zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="1e49e-109">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1e49e-110">W polu **Nazwa** wprowadź unikatową nazwę kroku zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="1e49e-111">Wprowadzanie wiersza tematu i instrukcji</span><span class="sxs-lookup"><span data-stu-id="1e49e-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="1e49e-112">Należy wprowadzić wiersz tematu i instrukcje dla użytkowników przypisanych do kroku zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="1e49e-113">Na przykład jeśli konfigurujesz krok zatwierdzania dla zapotrzebowań na zakup, użytkownik przypisany do kroku zobaczy wiersz tematu i instrukcje na stronie **Zapotrzebowania na zakup**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="1e49e-114">Wiersz tematu pojawia się na pasku komunikatów na stronie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="1e49e-115">Może wtedy kliknąć ikonę na pasku komunikatów i obejrzeć instrukcje.</span><span class="sxs-lookup"><span data-stu-id="1e49e-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="1e49e-116">Aby wprowadzić wiersz tematu i instrukcje, należy wykonać poniższe kroki.</span><span class="sxs-lookup"><span data-stu-id="1e49e-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="1e49e-117">W lewym okienku kliknij przycisk **Ustawienia podstawowe**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1e49e-118">W polu **Temat elementu pracy** wprowadź wiersz tematu.</span><span class="sxs-lookup"><span data-stu-id="1e49e-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="1e49e-119">Aby spersonalizować wiersz tematu, można wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="1e49e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="1e49e-120">Podczas wyświetlania wiersza tematu użytkownikom symbole zastępcze są zastępowane odpowiednimi danymi.</span><span class="sxs-lookup"><span data-stu-id="1e49e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="1e49e-121">Wykonaj następujące czynności, aby wstawić symbol zastępczy:</span><span class="sxs-lookup"><span data-stu-id="1e49e-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1e49e-122">W polu tekstowym kliknij miejsce, gdzie symbol zastępczy ma być wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="1e49e-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1e49e-123">Kliknij opcję **Wstaw symbol zastępczy**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1e49e-124">Na wyświetlonej liście wybierz symbol zastępczy, który chcesz wstawić.</span><span class="sxs-lookup"><span data-stu-id="1e49e-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1e49e-125">Kliknij przycisk **Wstaw**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-125">Click **Insert**.</span></span>

4. <span data-ttu-id="1e49e-126">Aby dodać tłumaczenia wiersza tematu, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="1e49e-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="1e49e-127">Kliknij opcję **Tłumaczenia**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="1e49e-128">Na wyświetlonej stronie kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1e49e-129">Z wyświetlonej listy wybierz język, w którym wprowadzasz tekst.</span><span class="sxs-lookup"><span data-stu-id="1e49e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1e49e-130">W polu **Przetłumaczony tekst** wprowadź tekst.</span><span class="sxs-lookup"><span data-stu-id="1e49e-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1e49e-131">Aby spersonalizować tekst, możesz wstawić symbole zastępcze, jak opisano w kroku 3.</span><span class="sxs-lookup"><span data-stu-id="1e49e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="1e49e-132">Kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-132">Click **Close**.</span></span>

5. <span data-ttu-id="1e49e-133">W polu **Instrukcje dotyczące elementu produkcyjnego** wprowadź instrukcje.</span><span class="sxs-lookup"><span data-stu-id="1e49e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="1e49e-134">Aby spersonalizować instrukcje, możesz wstawić symbole zastępcze.</span><span class="sxs-lookup"><span data-stu-id="1e49e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="1e49e-135">Podczas wyświetlania instrukcji użytkownikom symbole zastępcze są zastępowane odpowiednimi danymi.</span><span class="sxs-lookup"><span data-stu-id="1e49e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="1e49e-136">Wykonaj następujące czynności, aby wstawić symbol zastępczy:</span><span class="sxs-lookup"><span data-stu-id="1e49e-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1e49e-137">W polu tekstowym kliknij miejsce, gdzie symbol zastępczy ma być wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="1e49e-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1e49e-138">Kliknij opcję **Wstaw symbol zastępczy**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1e49e-139">Na wyświetlonej liście wybierz symbol zastępczy, który chcesz wstawić.</span><span class="sxs-lookup"><span data-stu-id="1e49e-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1e49e-140">Kliknij przycisk **Wstaw**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-140">Click **Insert**.</span></span>

7. <span data-ttu-id="1e49e-141">Aby dodać tłumaczenia instrukcji, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="1e49e-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="1e49e-142">Kliknij opcję **Tłumaczenia**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="1e49e-143">Na wyświetlonej stronie kliknij przycisk **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1e49e-144">Z wyświetlonej listy wybierz język, w którym wprowadzasz tekst.</span><span class="sxs-lookup"><span data-stu-id="1e49e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1e49e-145">W polu **Przetłumaczony tekst** wprowadź tekst.</span><span class="sxs-lookup"><span data-stu-id="1e49e-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1e49e-146">Aby spersonalizować tekst, możesz wstawić symbole zastępcze, jak opisano w kroku 6.</span><span class="sxs-lookup"><span data-stu-id="1e49e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="1e49e-147">Kliknij przycisk **Zamknij**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="1e49e-148">Przypisywanie kroku zatwierdzania</span><span class="sxs-lookup"><span data-stu-id="1e49e-148">Assign the approval step</span></span>

<span data-ttu-id="1e49e-149">Wykonaj poniższe kroki, aby określić, komu ma zostać przypisany ten krok zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="1e49e-150">W lewym okienku kliknij opcję **Przypisanie**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="1e49e-151">Na karcie **Typ przypisania** wybierz jedną z opcji w tabeli poniżej, a następnie wykonaj dodatkowe kroki dla tej opcji, zanim przejdziesz do kroku 3.</span><span class="sxs-lookup"><span data-stu-id="1e49e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1e49e-152">Opcja</span><span class="sxs-lookup"><span data-stu-id="1e49e-152">Option</span></span></th>
    <th><span data-ttu-id="1e49e-153">Użytkownicy, którym jest przypisany krok zatwierdzania</span><span class="sxs-lookup"><span data-stu-id="1e49e-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="1e49e-154">Dodatkowe kroki</span><span class="sxs-lookup"><span data-stu-id="1e49e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1e49e-155">Uczestnik</span><span class="sxs-lookup"><span data-stu-id="1e49e-155">Participant</span></span></td>
    <td><span data-ttu-id="1e49e-156">Użytkownicy, którzy są przypisani do określonej grupy lub roli</span><span class="sxs-lookup"><span data-stu-id="1e49e-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1e49e-157">Gdy wybierzesz wartość w polu <strong>Uczestnik</strong>, na karcie <strong>Oparte na roli</strong> na liście <strong>Typ uczestnika</strong> wybierz typ grupy lub roli, do której ma zostać przypisany krok.</span><span class="sxs-lookup"><span data-stu-id="1e49e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="1e49e-158">Na liście <strong>Uczestnik</strong> wybierz grupę lub rolę, do której ma zostać przypisany krok.</span><span class="sxs-lookup"><span data-stu-id="1e49e-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1e49e-159">Hierarchia</span><span class="sxs-lookup"><span data-stu-id="1e49e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="1e49e-160">Użytkownicy w określonej hierarchii organizacyjnej</span><span class="sxs-lookup"><span data-stu-id="1e49e-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1e49e-161">Gdy wybierzesz wartość w polu <strong>Hierarchia</strong>, na karcie <strong>Wybór hierarchii</strong> na liście <strong>Typ hierarchii</strong> wybierz typ hierarchii, do której ma zostać przypisany krok.</span><span class="sxs-lookup"><span data-stu-id="1e49e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="1e49e-162">System musi pobrać zakres nazwisk użytkowników z hierarchii.</span><span class="sxs-lookup"><span data-stu-id="1e49e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1e49e-163">Te nazwy reprezentują użytkowników, którym można przypisać krok.</span><span class="sxs-lookup"><span data-stu-id="1e49e-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="1e49e-164">Wykonaj poniższe kroki, aby określić początek i koniec zakresu nazw użytkowników pobieranych przez system:</span><span class="sxs-lookup"><span data-stu-id="1e49e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1e49e-165">Aby określić początek zakresu, zaznacz osobę na liście <strong>Rozpocznij od</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1e49e-166">Aby określić koniec zakresu, kliknij opcję <strong>Dodaj warunek</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1e49e-167">Następnie wprowadź warunek określający miejsce w hierarchii, w którym system ma zakończyć pobieranie nazwisk.</span><span class="sxs-lookup"><span data-stu-id="1e49e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1e49e-168">Na karcie <strong>Opcje hierarchii</strong> określ, którym użytkownikom w zakresie należy przypisać krok:</span><span class="sxs-lookup"><span data-stu-id="1e49e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="1e49e-169"><strong>Przypisz do wszystkich pobranych użytkowników</strong> — krok zostanie przypisany do wszystkich użytkowników w zakresie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="1e49e-170"><strong>Przypisz tylko do ostatnio pobranego użytkownika</strong> — krok zostanie przypisany tylko do ostatniego użytkownika w zakresie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1e49e-171"><strong>Nie uwzględniaj użytkowników spełniających następujący warunek</strong> — krok nie zostanie przypisany żadnym użytkownikom w zakresie, którzy spełniają określony warunek.</span><span class="sxs-lookup"><span data-stu-id="1e49e-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1e49e-172">Kliknij przycisk <strong>Dodaj warunek</strong>, aby określić warunek.</span><span class="sxs-lookup"><span data-stu-id="1e49e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1e49e-173">Użytkownik przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="1e49e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="1e49e-174">Użytkownicy w bieżącym przepływie pracy</span><span class="sxs-lookup"><span data-stu-id="1e49e-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1e49e-175">Po wybraniu wartości w polu <strong>Użytkownik przepływu pracy</strong> przejdź do karty <strong>Użytkownik przepływu pracy</strong> i na liście <strong>Użytkownik przepływu pracy</strong> wybierz użytkownika, który uczestniczy w przepływie pracy.</span><span class="sxs-lookup"><span data-stu-id="1e49e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1e49e-176">Użytkownik</span><span class="sxs-lookup"><span data-stu-id="1e49e-176">User</span></span></td>
    <td><span data-ttu-id="1e49e-177">Określeni użytkownicy</span><span class="sxs-lookup"><span data-stu-id="1e49e-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1e49e-178">Po wybraniu wartości w polu <strong>Użytkownik</strong> kliknij kartę <strong>Użytkownik</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1e49e-179">Lista <strong>Dostępni użytkownicy</strong> zawiera wszystkich użytkowników systemu.</span><span class="sxs-lookup"><span data-stu-id="1e49e-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="1e49e-180">Wybierz użytkowników, którym chcesz przypisać krok, a następnie przenieś tych użytkowników do listy <strong>Wybrani użytkownicy</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="1e49e-181">Na karcie **Limit czasu** w polu **Czas trwania** określ, ile czasu ma użytkownik, aby podjąć akcję lub zareagować na dokumenty, które dotrą do etapu zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="1e49e-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="1e49e-182">Umożliwia wybranie jednej z następujących opcji:</span><span class="sxs-lookup"><span data-stu-id="1e49e-182">Select one of the following options:</span></span>

    - <span data-ttu-id="1e49e-183">**Godziny** — Wprowadź liczbę godzin, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="1e49e-184">Następnie wybierz kalendarz używany przez organizację i wprowadź informacje o tygodniu roboczym obowiązującym w organizacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1e49e-185">**Dni** — Wprowadź liczbę dni, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="1e49e-186">Następnie wybierz kalendarz używany przez organizację i wprowadź informacje o tygodniu roboczym obowiązującym w organizacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1e49e-187">**Tygodnie** — Wprowadź liczbę tygodni, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="1e49e-188">**Miesiące** — Wybierz dzień i tydzień, do kiedy użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="1e49e-189">Na przykład można określić, że użytkownik ma odpowiedzieć do piątku w trzecim tygodniu miesiąca.</span><span class="sxs-lookup"><span data-stu-id="1e49e-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1e49e-190">**Lata** — Wybierz dzień, tydzień i miesiąc, do kiedy użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="1e49e-191">Na przykład można określić, że użytkownik ma odpowiedzieć do piątku w trzecim tygodniu grudnia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="1e49e-192">Jeśli użytkownik nie podejmie działania wobec dokumentu w wyznaczonym czasie, dokument staje się zaległy.</span><span class="sxs-lookup"><span data-stu-id="1e49e-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="1e49e-193">Dokument zaległy można eskalować na podstawie opcji wybranych na stronie w obszarze **Eskalacja**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="1e49e-194">Jeśli krok zatwierdzania został przypisany do wielu użytkowników lub do grupy użytkowników, na karcie **Zasady ukończenia** wybierz jedną z następujących opcji:</span><span class="sxs-lookup"><span data-stu-id="1e49e-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="1e49e-195">**Pojedyncza osoba zatwierdzająca** — Akcja stosowana do dokumentu jest określona przez pierwszą osobę, która odpowiada.</span><span class="sxs-lookup"><span data-stu-id="1e49e-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="1e49e-196">Na przykład Tomasz przesłał raport z wydatków na 15 000 zł.</span><span class="sxs-lookup"><span data-stu-id="1e49e-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1e49e-197">Raport z wydatków jest obecnie przypisany do Magdy, Ewy i Bartka.</span><span class="sxs-lookup"><span data-stu-id="1e49e-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1e49e-198">Jeśli pierwszą osobą, która odpowie na dokument, jest Magda, wybrana przez nią akcja zostanie zastosowana do dokumentu.</span><span class="sxs-lookup"><span data-stu-id="1e49e-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="1e49e-199">Jeśli Magda odrzuci dokument, zostanie on odrzucony i wysłany z powrotem do Tomasza.</span><span class="sxs-lookup"><span data-stu-id="1e49e-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="1e49e-200">Po zatwierdzeniu przez Magdę dokument zostanie przesłany do Anny w celu zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Przepływ pracy z procesem zatwierdzania](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="1e49e-202">**Większość osób zatwierdzających** — Akcja stosowana do dokumentu jest określana po uzyskaniu odpowiedzi od większości osób zatwierdzających.</span><span class="sxs-lookup"><span data-stu-id="1e49e-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="1e49e-203">Na przykład Tomasz przesłał raport z wydatków na 15 000 zł.</span><span class="sxs-lookup"><span data-stu-id="1e49e-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1e49e-204">Raport z wydatków jest obecnie przypisany do Magdy, Ewy i Bartka.</span><span class="sxs-lookup"><span data-stu-id="1e49e-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1e49e-205">Jeżeli dwoma pierwszym osobami zatwierdzającymi, które zareagowały, są Magda i Ewa, ich operacje są stosowane do dokumentu.</span><span class="sxs-lookup"><span data-stu-id="1e49e-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="1e49e-206">Jeśli Magda zatwierdzi dokument, ale Ewa go odrzuci, dokument zostanie odrzucony i wysłany z powrotem do Tomasza.</span><span class="sxs-lookup"><span data-stu-id="1e49e-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="1e49e-207">Jeśli Magda i Ewa zatwierdzą dokument, zostanie on wysłany do Anny do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="1e49e-208">**Odsetek obiektów zatwierdzających** — Akcja dotycząca dokumentu zostanie określona po uzyskaniu odpowiedzi określonego procentu osób zatwierdzających.</span><span class="sxs-lookup"><span data-stu-id="1e49e-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="1e49e-209">Na przykład Tomasz przesłał raport z wydatków na 15 000 zł.</span><span class="sxs-lookup"><span data-stu-id="1e49e-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1e49e-210">Raport z wydatków jest obecnie przypisany do Magdy, Ewy i Bartka, a jako wartość procentową wprowadzono **50**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="1e49e-211">Jeśli Magda i Ewa są dwiema pierwszymi osobami zatwierdzającymi, które odpowiedziały, ich czynności są stosowane do dokumentu, ponieważ obie razem spełniają wymóg 50 procent osób zatwierdzających.</span><span class="sxs-lookup"><span data-stu-id="1e49e-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="1e49e-212">Jeśli Magda zatwierdzi dokument, ale Ewa go odrzuci, dokument zostanie odrzucony i wysłany z powrotem do Tomasza.</span><span class="sxs-lookup"><span data-stu-id="1e49e-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="1e49e-213">Jeśli Magda i Ewa zatwierdzą dokument, zostanie on wysłany do Anny do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="1e49e-214">**Wszystkie osoby zatwierdzające** — Wszystkie osoby zatwierdzające muszą zatwierdzić dokument.</span><span class="sxs-lookup"><span data-stu-id="1e49e-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="1e49e-215">W przeciwnym razie nie można kontynuować przepływu pracy.</span><span class="sxs-lookup"><span data-stu-id="1e49e-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="1e49e-216">Na przykład Tomasz przesłał raport z wydatków na 15 000 zł.</span><span class="sxs-lookup"><span data-stu-id="1e49e-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="1e49e-217">Raport z wydatków jest obecnie przypisany do Magdy, Ewy i Bartka.</span><span class="sxs-lookup"><span data-stu-id="1e49e-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="1e49e-218">Jeśli Magda i Ewa zatwierdzą dokument, ale Bartek go odrzuci, dokument zostanie odrzucony i wysłany z powrotem do Tomasza.</span><span class="sxs-lookup"><span data-stu-id="1e49e-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="1e49e-219">Jeśli Magda, Ewa i Bartek zatwierdzą dokument, zostanie wysłany do Anny do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="1e49e-220">Określanie, kiedy krok zatwierdzania jest wymagany</span><span class="sxs-lookup"><span data-stu-id="1e49e-220">Specify when the approval step is required</span></span>

<span data-ttu-id="1e49e-221">Można określić, kiedy krok zatwierdzania jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1e49e-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="1e49e-222">Krok zatwierdzenia może być wymagany zawsze lub tylko wtedy, gdy są spełnione określone warunki.</span><span class="sxs-lookup"><span data-stu-id="1e49e-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="1e49e-223">Krok zatwierdzania jest zawsze wymagany</span><span class="sxs-lookup"><span data-stu-id="1e49e-223">The approval step is always required</span></span>

<span data-ttu-id="1e49e-224">Jeśli krok zatwierdzania jest zawsze wymagany, wykonaj następujące czynności.</span><span class="sxs-lookup"><span data-stu-id="1e49e-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="1e49e-225">W lewym okienku kliknij opcję **Warunek**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="1e49e-226">Wybierz opcję **Zawsze wykonuj ten krok**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="1e49e-227">Krok zatwierdzania jest wymagany w określonych warunkach</span><span class="sxs-lookup"><span data-stu-id="1e49e-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="1e49e-228">Konfigurowany krok zatwierdzania może być wymagany tylko w określonych warunkach.</span><span class="sxs-lookup"><span data-stu-id="1e49e-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="1e49e-229">Na przykład jeśli konfigurujesz krok zatwierdzania przepływu pracy zapotrzebowania na zakup, można określić, aby krok następował tylko wtedy, gdy kwota zapotrzebowania na zakup jest większa niż 10 000 zł.</span><span class="sxs-lookup"><span data-stu-id="1e49e-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="1e49e-230">Wykonaj następujące czynności, aby określić, kiedy krok zatwierdzania jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1e49e-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="1e49e-231">W lewym okienku kliknij opcję **Warunek**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="1e49e-232">Wybierz opcję **Wykonaj ten krok, tylko jeśli zostanie spełniony następujący warunek**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="1e49e-233">Służy do wprowadzania warunku.</span><span class="sxs-lookup"><span data-stu-id="1e49e-233">Enter a condition.</span></span>
4. <span data-ttu-id="1e49e-234">Wprowadź wszelkie wymagane dodatkowe warunki.</span><span class="sxs-lookup"><span data-stu-id="1e49e-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="1e49e-235">Aby sprawdzić, czy wprowadzone warunki są poprawnie skonfigurowane, wykonaj następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="1e49e-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="1e49e-236">Kliknij przycisk **Test**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-236">Click **Test**.</span></span>
    2. <span data-ttu-id="1e49e-237">Na stronie **Warunek testowy przepływu pracy** w obszarze **Sprawdź poprawność warunku** wybierz rekord.</span><span class="sxs-lookup"><span data-stu-id="1e49e-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="1e49e-238">Kliknij przycisk **Test**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-238">Click **Test**.</span></span> <span data-ttu-id="1e49e-239">System oszacuje rekord i określi, czy rekord spełnia określone warunki.</span><span class="sxs-lookup"><span data-stu-id="1e49e-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="1e49e-240">Kliknij przycisk **OK** lub **Anuluj**, aby powrócić do strony **Właściwości**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="1e49e-241">Określanie, co się dzieje z dokumentem zaległym</span><span class="sxs-lookup"><span data-stu-id="1e49e-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="1e49e-242">Jeśli użytkownik nie podejmie działania wobec dokumentu w wyznaczonym czasie, dokument staje się zaległy.</span><span class="sxs-lookup"><span data-stu-id="1e49e-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="1e49e-243">Dokument zaległy może być eskalowany lub automatycznie przypisywany do innego użytkownika w celu zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="1e49e-244">Wykonaj następujące kroki, aby eskalować zaległy dokument.</span><span class="sxs-lookup"><span data-stu-id="1e49e-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="1e49e-245">W lewym okienku kliknij opcję **Eskalacja**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="1e49e-246">Zaznacz pole wyboru **Użyj ścieżki eskalacji**, aby utworzyć ścieżkę eskalacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="1e49e-247">System automatycznie przypisze dokument do użytkowników wymienionych w ścieżce eskalacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="1e49e-248">Na przykład poniższa tabela przedstawia ścieżkę eskalacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="1e49e-249">Kolejność</span><span class="sxs-lookup"><span data-stu-id="1e49e-249">Sequence</span></span> | <span data-ttu-id="1e49e-250">Ścieżka eskalacji</span><span class="sxs-lookup"><span data-stu-id="1e49e-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="1e49e-251">1 przypada na wpłatę z zysku na rzecz budżetu państwa</span><span class="sxs-lookup"><span data-stu-id="1e49e-251">1</span></span>        | <span data-ttu-id="1e49e-252">Przypisać do: Danuta</span><span class="sxs-lookup"><span data-stu-id="1e49e-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="1e49e-253">2</span><span class="sxs-lookup"><span data-stu-id="1e49e-253">2</span></span>        | <span data-ttu-id="1e49e-254">Przypisać do: Ireny</span><span class="sxs-lookup"><span data-stu-id="1e49e-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="1e49e-255">3</span><span class="sxs-lookup"><span data-stu-id="1e49e-255">3</span></span>        | <span data-ttu-id="1e49e-256">Działanie końcowe: Odrzucenie</span><span class="sxs-lookup"><span data-stu-id="1e49e-256">Final action: Reject</span></span> |

    <span data-ttu-id="1e49e-257">W tym przykładzie system przypisuje zaległy dokument do Danuty.</span><span class="sxs-lookup"><span data-stu-id="1e49e-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="1e49e-258">Jeśli Danuta nie odpowie w przydzielonym czasie, system przypisze dokument do Ireny.</span><span class="sxs-lookup"><span data-stu-id="1e49e-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="1e49e-259">Jeśli Irena nie odpowie w przydzielonym czasie, system odrzuci dokument.</span><span class="sxs-lookup"><span data-stu-id="1e49e-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="1e49e-260">Aby dodać użytkownika do ścieżki eskalacji, kliknij opcję **Dodaj eskalację**.</span><span class="sxs-lookup"><span data-stu-id="1e49e-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="1e49e-261">Na karcie **Typ przypisania** wybierz jedną z opcji w tabeli poniżej, a następnie wykonaj dodatkowe kroki dla tej opcji, zanim przejdziesz do kroku 4.</span><span class="sxs-lookup"><span data-stu-id="1e49e-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1e49e-262">Opcja</span><span class="sxs-lookup"><span data-stu-id="1e49e-262">Option</span></span></th>
    <th><span data-ttu-id="1e49e-263">Użytkownicy, do których dokument jest eskalowany</span><span class="sxs-lookup"><span data-stu-id="1e49e-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="1e49e-264">Dodatkowe kroki</span><span class="sxs-lookup"><span data-stu-id="1e49e-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1e49e-265">Hierarchia</span><span class="sxs-lookup"><span data-stu-id="1e49e-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="1e49e-266">Użytkownicy w określonej hierarchii organizacyjnej</span><span class="sxs-lookup"><span data-stu-id="1e49e-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1e49e-267">Gdy wybierzesz wartość w polu <strong>Hierarchia</strong>, na karcie <strong>Wybór hierarchii</strong> na liście <strong>Typ hierarchii</strong> wybierz typ hierarchii, do której ma zostać eskalowany dokument.</span><span class="sxs-lookup"><span data-stu-id="1e49e-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="1e49e-268">System musi pobrać zakres nazwisk użytkowników z hierarchii.</span><span class="sxs-lookup"><span data-stu-id="1e49e-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1e49e-269">Te nazwy reprezentują użytkowników, do których można eskalować dokument.</span><span class="sxs-lookup"><span data-stu-id="1e49e-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="1e49e-270">Wykonaj poniższe kroki, aby określić początek i koniec zakresu nazw użytkowników pobieranych przez system:</span><span class="sxs-lookup"><span data-stu-id="1e49e-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1e49e-271">Aby określić początek zakresu, zaznacz osobę na liście <strong>Rozpocznij od</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1e49e-272">Aby określić koniec zakresu, kliknij opcję <strong>Dodaj warunek</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1e49e-273">Następnie wprowadź warunek określający miejsce w hierarchii, w którym system ma zakończyć pobieranie nazwisk.</span><span class="sxs-lookup"><span data-stu-id="1e49e-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1e49e-274">Na karcie <strong>Opcje hierarchii</strong> określ, do których użytkowników w zakresie należy eskalować dokument:</span><span class="sxs-lookup"><span data-stu-id="1e49e-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="1e49e-275"><strong>Przypisz do wszystkich pobranych użytkowników</strong> — dokument zostanie eskalowany do wszystkich użytkowników w zakresie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="1e49e-276"><strong>Przypisz tylko do ostatnio pobranego użytkownika</strong> — dokument zostanie eskalowany tylko do ostatniego użytkownika w zakresie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1e49e-277"><strong>Nie uwzględniaj użytkowników spełniających następujący warunek</strong> — dokument nie będzie eskalowany do żadnych użytkowników w zakresie, którzy spełniają określony warunek.</span><span class="sxs-lookup"><span data-stu-id="1e49e-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1e49e-278">Kliknij przycisk <strong>Dodaj warunek</strong>, aby określić warunek.</span><span class="sxs-lookup"><span data-stu-id="1e49e-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1e49e-279">Użytkownik przepływu pracy</span><span class="sxs-lookup"><span data-stu-id="1e49e-279">Workflow user</span></span></td>
    <td><span data-ttu-id="1e49e-280">Użytkownicy w bieżącym przepływie pracy</span><span class="sxs-lookup"><span data-stu-id="1e49e-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1e49e-281">Po wybraniu wartości w polu <strong>Użytkownik przepływu pracy</strong> przejdź do karty <strong>Użytkownik przepływu pracy</strong> i na liście <strong>Użytkownik przepływu pracy</strong> wybierz użytkownika, który uczestniczy w przepływie pracy.</span><span class="sxs-lookup"><span data-stu-id="1e49e-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1e49e-282">Użytkownik</span><span class="sxs-lookup"><span data-stu-id="1e49e-282">User</span></span></td>
    <td><span data-ttu-id="1e49e-283">Określeni użytkownicy</span><span class="sxs-lookup"><span data-stu-id="1e49e-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1e49e-284">Po wybraniu wartości w polu <strong>Użytkownik</strong> kliknij kartę <strong>Użytkownik</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1e49e-285">Lista <strong>Dostępni użytkownicy</strong> zawiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1e49e-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="1e49e-286">Wybierz użytkowników, do których chcesz eskalować dokument, a następnie przenieś tych użytkowników do listy <strong>Wybrani użytkownicy</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e49e-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="1e49e-287">Na karcie **Limit czasu** w polu **Czas trwania** określ, ile czasu ma użytkownik, aby podjąć akcję lub zareagować na dokumenty.</span><span class="sxs-lookup"><span data-stu-id="1e49e-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="1e49e-288">Umożliwia wybranie jednej z następujących opcji:</span><span class="sxs-lookup"><span data-stu-id="1e49e-288">Select one of the following options:</span></span>

    - <span data-ttu-id="1e49e-289">**Godziny** — Wprowadź liczbę godzin, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="1e49e-290">Następnie wybierz kalendarz używany przez organizację i wprowadź informacje o tygodniu roboczym obowiązującym w organizacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1e49e-291">**Dni** — Wprowadź liczbę dni, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="1e49e-292">Następnie wybierz kalendarz używany przez organizację i wprowadź informacje o tygodniu roboczym obowiązującym w organizacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1e49e-293">**Tygodnie** — Wprowadź liczbę tygodni, w ciągu których użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="1e49e-294">**Miesiące** — Wybierz dzień i tydzień, do kiedy użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="1e49e-295">Na przykład można określić, że użytkownik ma odpowiedzieć do piątku w trzecim tygodniu miesiąca.</span><span class="sxs-lookup"><span data-stu-id="1e49e-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1e49e-296">**Lata** — Wybierz dzień, tydzień i miesiąc, do kiedy użytkownik musi zareagować.</span><span class="sxs-lookup"><span data-stu-id="1e49e-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="1e49e-297">Na przykład można określić, że użytkownik ma odpowiedzieć do piątku w trzecim tygodniu grudnia.</span><span class="sxs-lookup"><span data-stu-id="1e49e-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="1e49e-298">Powtórz kroki od 3 do 4 dla każdego użytkownika, który powinien zostać dodany do ścieżki eskalacji.</span><span class="sxs-lookup"><span data-stu-id="1e49e-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="1e49e-299">Można zmienić kolejność użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1e49e-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="1e49e-300">Jeśli użytkownicy wymienieni w ścieżce eskalacji nie odpowiedzą w wyznaczonym czasie, system automatycznie wykona operację na dokumencie.</span><span class="sxs-lookup"><span data-stu-id="1e49e-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="1e49e-301">Aby określić akcję podejmowaną przez system, wybierz wiersz **Akcja**, a następnie na karcie **Zakończ działanie** wybierz akcję.</span><span class="sxs-lookup"><span data-stu-id="1e49e-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>