---
title: "Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (sierpień 2018 r.)"
description: "W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: cdf0893835c1ee9edd89c43b3c5c842d89e6d526
ms.contentlocale: pl-pl
ms.lasthandoff: 08/29/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a>Nowości i zmiany w rozwiązaniu Dynamics 365 for Talent Core HR (sierpień 2018 r.)

[!include [banner](includes/banner.md)]

**Kompilacja 8.1.104**

W tym temacie opisano nowe i zmienione funkcje dostępne w rozwiązaniu Dynamics 365 for Talent Core HR.

## <a name="view-expiring-records-in-manager-self-service"></a>Wyświetlanie wygasających rekordów w obszarze roboczym Samoobsługa menedżera

Teraz w obszarze roboczym Samoobsługa menedżera można wyświetlać wygasające rekordy. Nowe opcje umożliwiają określenie, jakie informacje będą dostępne do wglądu dla menedżerów. Obejmuje to:

-   Certyfikaty

-   Numery identyfikacyjne

-   Okresy próbne

-   Kontrole

-   Testy

Ta funkcja daje także możliwość określenia zakresu dni, w których mają być szukane wygasające rekordy.

## <a name="configurable-transfer-actions"></a>Konfigurowalne akcje przeniesienia

Można skonfigurować opcje, które będą dostępne dla poszczególnych ról podczas wprowadzania wniosku o przeniesienie. Ta funkcja zapewnia dodatkową elastyczność posługiwania się rolami w organizacji.

Na przykład menedżerowie wnioskujący o przeniesienia pracowników mogą nie mieć uprawnień do proponowania lub wprowadzania kwot wynagrodzenia albo wybierania list zadań, które mają zostać skojarzone z wnioskiem o przeniesienie. W takim przypadku menedżerowie mogą tworzyć i przesyłać wnioski o przeniesienie, ale nie mogą wprowadzać przypisań wynagrodzeń ani list zadań. W tej samej konfiguracji dział kadr będzie mógł przypisywać nowe wartości wynagrodzeń, a także wszelkie dodatkowe listy kontrolne czynności, które należy wykonać po sfinalizowaniu przeniesienia.

Domyślnie nowe opcje konfiguracji są ustawione w taki sposób, aby nie zmieniały żadnych funkcji w wersjach sprzed tej aktualizacji.

## <a name="leave-and-absence"></a>Urlopy i nieobecności

Teraz sekcja Urlopy i nieobecności zawiera dodatkowe pola dat.

Za ich pomocą można w podstawie okresu naliczania na poziomie planu ustawić używanie konkretnych dat dotyczących pracowników etatowych. Dzięki temu w procesie naliczania urlopu można używać dat innych niż data początkowa planu. Opcje dat specyficznych dla pracownika obejmują następujące pozycje:

-   Niestandardowe (dostępna przed tą aktualizacją)

-   Rocznica

-   Pierwotna data zatrudnienia

-   Data stażu pracy

-   Skorygowana data rozpoczęcia dla pracownika

-   Data rozpoczęcia dla pracownika

Jeżeli w procesie rejestracji zostanie skonfigurowane używanie jednej z dat specyficznych dla pracownika, proces będzie używał tej daty do obliczania okresów naliczania. Podstawa okresu naliczania jest również wyświetlana w rejestracji pracownika do planu, aby pomóc zrozumieć, które informacje są używane w trakcie procesu naliczania.

## <a name="microsoft-word-integration"></a>Integracja z oprogramowaniem Microsoft Word

Obsługa szablonów dokumentów została włączona w całym rozwiązaniu Core HR. Ta funkcja umożliwia tworzenie pism i raportów na podstawie utworzonego szablonu programu Word.

Dodatkowe informacje o tej funkcji są dostępne w dokumencie [Integracja z pakietem Office — samouczek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).


## <a name="other-fixes"></a>Inne poprawki

Ta wersja zawiera również szereg poprawek błędów, nowe jednostki, poprawki istniejących jednostek oraz modyfikacje tłumaczeń etykiet.
