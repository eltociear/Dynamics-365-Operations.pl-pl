---
title: Mobilny obszar roboczy Mój zespół
description: Ten temat zawiera informacje o komórkowym obszarze roboczym Mój zespół, który umożliwia kierownikom wyświetlanie informacji o bezpośrednich podwładnych i pracownikach na dalszych szczeblach podwładności. Użytkownicy mogą również wysyłać pochwały osobom w swoich łańcuchach relacji służbowych.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 272cf991301fa5c2df8a6de3354588fc372fa92f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248740"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="651a7-104">Mobilny obszar roboczy Mój zespół</span><span class="sxs-lookup"><span data-stu-id="651a7-104">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="651a7-105">Ten temat zawiera informacje o komórkowym obszarze roboczym **Mój zespół**.</span><span class="sxs-lookup"><span data-stu-id="651a7-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="651a7-106">Ten obszar roboczy umożliwia kierownikom wyświetlanie informacji o bezpośrednich podwładnych i pracownikach na dalszych szczeblach podwładności.</span><span class="sxs-lookup"><span data-stu-id="651a7-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="651a7-107">Mogą oni również wysyłać pochwały osobom w swoich łańcuchach relacji służbowych.</span><span class="sxs-lookup"><span data-stu-id="651a7-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="651a7-108">Ten mobilny obszar roboczy jest przeznaczony do używania w aplikacji mobilnej Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="651a7-108">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="651a7-109">Przegląd</span><span class="sxs-lookup"><span data-stu-id="651a7-109">Overview</span></span> 
<span data-ttu-id="651a7-110">Mobilny obszar roboczy **Mój zespół** pozwala kierownikom wykonywać następujące zadania:</span><span class="sxs-lookup"><span data-stu-id="651a7-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="651a7-111">Wyświetlanie listy bezpośrednich podwładnych menedżera.</span><span class="sxs-lookup"><span data-stu-id="651a7-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="651a7-112">Wyświetlanie listy pośrednich podwładnych menedżera.</span><span class="sxs-lookup"><span data-stu-id="651a7-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="651a7-113">Wyświetlanie szczegółowych informacji o każdym członka zespołu, takich jak data urodzenia, data stażu pracy, staż pracy, wynagrodzenie i osiągane wyniki.</span><span class="sxs-lookup"><span data-stu-id="651a7-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="651a7-114">Wysyłanie pochwał osobom na dalszych szczeblach podwładności wobec menedżera.</span><span class="sxs-lookup"><span data-stu-id="651a7-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="651a7-115">Wymagania wstępne</span><span class="sxs-lookup"><span data-stu-id="651a7-115">Prerequisites</span></span>
<span data-ttu-id="651a7-116">Aby można było używać tego mobilnego obszaru roboczego, muszą być spełnione następujące wymagania wstępne.</span><span class="sxs-lookup"><span data-stu-id="651a7-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="651a7-117">Wymaganie wstępne</span><span class="sxs-lookup"><span data-stu-id="651a7-117">Prerequisite</span></span></th>
<th><span data-ttu-id="651a7-118">Rola</span><span class="sxs-lookup"><span data-stu-id="651a7-118">Role</span></span></th>
<th><span data-ttu-id="651a7-119">opis</span><span class="sxs-lookup"><span data-stu-id="651a7-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="651a7-120">W organizacji musi być wdrożony jeden z następujących produktów:</span><span class="sxs-lookup"><span data-stu-id="651a7-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="651a7-121">Aplikacja Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="651a7-121">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="651a7-122">Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="651a7-122">Microsoft Dynamics 365 Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="651a7-123">Administrator systemu</span><span class="sxs-lookup"><span data-stu-id="651a7-123">System administrator</span></span></td>
<td><span data-ttu-id="651a7-124">Jeśli w organizacji jeszcze wdrożono aplikacji Finance and Operations, zobacz <a href="../deployment/deploy-demo-environment.md">Wdrażanie środowiska demonstracyjnego</a>.</span><span class="sxs-lookup"><span data-stu-id="651a7-124">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="651a7-125">Jeśli w organizacji jeszcze nie wdrożono oprogramowania Talent, administrator systemu ma dostęp do wersji próbnej z <a href="https://www.microsoft.com/dynamics365/talent">witryny internetowej modułu Talent</a>.</span><span class="sxs-lookup"><span data-stu-id="651a7-125">If you don&#39;t already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="651a7-126">Mobilny obszar roboczy <strong>Mój zespół</strong> musi być opublikowany.</span><span class="sxs-lookup"><span data-stu-id="651a7-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="651a7-127">Administrator systemu</span><span class="sxs-lookup"><span data-stu-id="651a7-127">System administrator</span></span></td>
<td><span data-ttu-id="651a7-128">Zobacz <a href="publish-mobile-workspace.md">Publikowanie mobilnego obszaru roboczego</a>.</span><span class="sxs-lookup"><span data-stu-id="651a7-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="651a7-129">Pobieranie i instalowanie aplikacji mobilnej</span><span class="sxs-lookup"><span data-stu-id="651a7-129">Download and install the mobile app</span></span>

<span data-ttu-id="651a7-130">Pobieranie i instalowanie aplikacji mobilnej Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="651a7-130">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="651a7-131">Telefony Android</span><span class="sxs-lookup"><span data-stu-id="651a7-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="651a7-132">Telefony iPhone</span><span class="sxs-lookup"><span data-stu-id="651a7-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="651a7-133">Logowanie do aplikacji mobilnej</span><span class="sxs-lookup"><span data-stu-id="651a7-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="651a7-134">Uruchom aplikację na urządzeniu komórkowym.</span><span class="sxs-lookup"><span data-stu-id="651a7-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="651a7-135">Wprowadź swój adres URL w usłudze Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="651a7-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="651a7-136">Podczas pierwszego logowania pojawi się monit o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="651a7-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="651a7-137">Wprowadź swoje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="651a7-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="651a7-138">Po zalogowaniu się zobaczysz obszary robocze dostępne dla firmy.</span><span class="sxs-lookup"><span data-stu-id="651a7-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="651a7-139">Należy zauważyć, że jeśli administrator systemu później opublikuje nowy obszar roboczy, trzeba odświeżyć listę komórkowych obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="651a7-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="651a7-140">[![Ściąganie w celu odświeżenia](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="651a7-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="651a7-141">Wyświetlanie informacji o członkach zespołu przy użyciu mobilnego obszaru roboczego Mój zespół</span><span class="sxs-lookup"><span data-stu-id="651a7-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="651a7-142">W aplikacji komórkowej zaznacz obszar roboczy **Mój zespół**.</span><span class="sxs-lookup"><span data-stu-id="651a7-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="651a7-143">Zostanie wyświetlona lista członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-143">A list of team members is shown.</span></span> <span data-ttu-id="651a7-144">Lista zawiera także tytuł każdego członka zespołu oraz imiona i nazwiska jego wszelkich bezpośrednich podwładnych.</span><span class="sxs-lookup"><span data-stu-id="651a7-144">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
2.  <span data-ttu-id="651a7-145">Wybierz członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-145">Select a team member.</span></span> <span data-ttu-id="651a7-146">Zostanie wyświetlona strona **Podsumowanie członka zespołu**.</span><span class="sxs-lookup"><span data-stu-id="651a7-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="651a7-147">Informacje na tej stronie obejmują datę urodzenia członka zespołu, datę stażu pracy, staż pracy, liczbę lat pracy na bieżącym stanowisku oraz informacje dotyczące wynagrodzenia.</span><span class="sxs-lookup"><span data-stu-id="651a7-147">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="651a7-148">Wyświetlanie informacji o członkach zespołu na dalszych szczeblach podwładności przy użyciu mobilnego obszaru roboczego Mój zespół</span><span class="sxs-lookup"><span data-stu-id="651a7-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="651a7-149">W aplikacji komórkowej zaznacz obszar roboczy **Mój zespół**.</span><span class="sxs-lookup"><span data-stu-id="651a7-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="651a7-150">Zostanie wyświetlona lista członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-150">A list of team members is shown.</span></span> <span data-ttu-id="651a7-151">Lista zawiera także tytuł każdego członka zespołu oraz imiona i nazwiska jego wszelkich bezpośrednich podwładnych.</span><span class="sxs-lookup"><span data-stu-id="651a7-151">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="651a7-152">Kliknij łącze **Bezpośredni podwładni**.</span><span class="sxs-lookup"><span data-stu-id="651a7-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="651a7-153">Zostanie wyświetlona lista członków zespołu na dalszych szczeblach podwładności.</span><span class="sxs-lookup"><span data-stu-id="651a7-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="651a7-154">Wybierz członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-154">Select a team member.</span></span> <span data-ttu-id="651a7-155">Zostanie wyświetlona strona **Podsumowanie członka zespołu**.</span><span class="sxs-lookup"><span data-stu-id="651a7-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="651a7-156">Informacje na tej stronie obejmują datę urodzenia członka zespołu, datę stażu pracy, staż pracy, liczbę lat pracy na bieżącym stanowisku oraz informacje dotyczące wynagrodzenia.</span><span class="sxs-lookup"><span data-stu-id="651a7-156">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="651a7-157">Wysyłanie pochwał do członków zespołu przy użyciu mobilnego obszaru roboczego Mój zespół</span><span class="sxs-lookup"><span data-stu-id="651a7-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="651a7-158">W aplikacji komórkowej zaznacz obszar roboczy **Mój zespół**.</span><span class="sxs-lookup"><span data-stu-id="651a7-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="651a7-159">Zostanie wyświetlona lista członków zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-159">A list of team members is shown.</span></span> <span data-ttu-id="651a7-160">Lista zawiera także tytuł każdego członka zespołu oraz imiona i nazwiska jego wszelkich bezpośrednich podwładnych.</span><span class="sxs-lookup"><span data-stu-id="651a7-160">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="651a7-161">Wybierz członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="651a7-161">Select a team member.</span></span> <span data-ttu-id="651a7-162">Zostanie wyświetlona strona **Podsumowanie członka zespołu**.</span><span class="sxs-lookup"><span data-stu-id="651a7-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="651a7-163">Kliknij opcję **Wyślij pochwałę**.</span><span class="sxs-lookup"><span data-stu-id="651a7-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="651a7-164">Wprowadź tekst pochwały, jaką chcesz wysłać.</span><span class="sxs-lookup"><span data-stu-id="651a7-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="651a7-165">Wybierz opcję **Gotowe**.</span><span class="sxs-lookup"><span data-stu-id="651a7-165">Select **Done**.</span></span>