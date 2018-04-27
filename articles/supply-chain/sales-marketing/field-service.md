---
title: Integracja z programem Microsoft Dynamics 365 for Field Service
description: "Ten temat zawiera omówienie integracji z programem Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: pl-pl
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integracja z programem Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Program Microsoft Dynamics 365 for Finance and Operations umożliwia synchronizowanie procesów biznesowych między programami Finance and Operations a Microsoft Dynamics 365 for Field Service. Scenariusze integracji konfiguruje się przy użyciu rozszerzalnych szablonów integratora danych oraz usługi Common Data Service (CDS), co umożliwia synchronizowanie procesów biznesowych.

[![Synchronizacja procesów biznesowych między aplikacjami Finance and Operations i Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Pierwsza faza integracji między programami Field Service i Finance and Operations skupia się na umożliwieniu fakturowania zleceń pracy i umów z programu Field Service w programie Finance and Operations. Obsługiwany przepływ rozpoczyna się w programie Field Service, gdzie informacje ze zleceń pracy są synchronizowane z programem Finance and Operations jako zamówienia sprzedaży. W programie Finance and Operations zamówienia sprzedaży są fakturowane w celu wygenerowania dokumentów faktur. Ponadto informacje z faktur za umowy w programie Field Service są synchronizowane z programem Finance and Operations. Integrator danych programu Microsoft Dynamics 365 synchronizuje dane przy użyciu konfigurowalnych projektów. Można używać standardowych szablonów do tworzenia niestandardowych projektów integracji, gdzie dodatkowe pola standardowe i niestandardowe, a także jednostki, mogą być mapowane w celu skorygowania integracji i spełnienia określonych wymagań.

Pierwsza faza integracji między programami Field Service i Finance and Operations umożliwia synchronizowanie następujących elementów:

- [Produkty w programie Finance and Operations z produktami w programie Field Service zawierającymi informacje o typach produktów](field-service-product.md)
- [Zlecenia pracy w rozwiązaniu Field Service z zamówieniami sprzedaży w rozwiązaniu Finance and Operations](field-service-work-order.md)
- [Faktury w programie Field Service z fakturami niezależnymi w programie Finance and Operations](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a>Wymagania systemowe dla rozwiązania Finance and Operations
Program Field Service można integrować z następującymi wersjami:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations w wersji 8.0 (kwiecień 2018) i nowszych

- Program Dynamics 365 for Finance and Operations w wersji 8.0 (kwiecień 2018) został wydany w kwietniu 2018 r. i ma numer kompilacji aplikacji 8.0.30.8020 oraz aktualizację Platform Update 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Wymagania systemowe programu Field Service
Aby korzystać z rozwiązania integracyjnego Field Service, należy zainstalować następujące składniki:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 lub nowszy

- Dynamics 365 for Field Service wersja 1612 (9.0.1.733) (DB 9.0.1.733) online lub nowsza.
- Rozwiązanie Prospekt na gotówkę (P2C) dla programu Dynamics 365, wersja 1.15.0.1 lub nowsza. To rozwiązanie jest dostępne do pobrania z usługi [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Rozwiązanie integracyjne Field Service dla programu Dynamics 365, wersja 1.0.0.0 lub nowsza. To rozwiązanie jest dostępne do pobrania z usługi AppSource. **(OCZEKUJĄ NA WYDANIE)**
