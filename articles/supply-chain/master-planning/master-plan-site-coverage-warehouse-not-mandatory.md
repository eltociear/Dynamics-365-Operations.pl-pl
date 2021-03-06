---
title: Planowanie główne dla zapotrzebowania oddziału, magazyn niewymagany
description: W tym temacie opisano sposób planowania towaru, który ma wymiar zapotrzebowania „oddział”.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43989f95764a60dc7f5662ef74c005c5fddaa275
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813738"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Planowanie główne dla zapotrzebowania oddziału, magazyn niewymagany

[!include [banner](../includes/banner.md)]

W tym temacie opisano sposób planowania towaru, który ma wymiar zapotrzebowania „oddział”.

Niniejszy scenariusz planowania głównego wymaga spełnienia następujących warunków:

-   Wymiar lokalizacji jest ustawiony jako wymagany i musi być wprowadzony w transakcji popytu.
-   Wymiar magazynowy nie jest skonfigurowany jako obowiązkowy. Magazyn może być znany, ale nie jest uwzględniany w obliczeniach planowania głównego.
-   Wymiar oddziału jest ustawiony dla planowania zapotrzebowania.
-   Wymiar magazynu nie jest ustawiony dla planowania zapotrzebowania. Dlatego podaż i popyt są agregowane według oddziałów oraz ewentualnie według innych wymiarów z planowaniem zapotrzebowania.

Na poniższej ilustracji przedstawiono przebieg planowania głównego. Parametry wymienione na ilustracji i ich lokalizacje są następujące:
-   Jest zdefiniowane zapotrzebowanie na dany towar. Kliknij kolejno opcje **Zarządzanie informacjami o produktach &gt; Produkty&gt; Zwolnione produkty**. Zaznacz towar i kliknij kolejno opcje **Plan &gt; Zapotrzebowanie na towary**.
-   Dla magazynu są zdefiniowane relacje uzupełniania. Kliknij kolejno opcje **Zarządzanie zapasami &gt; Ustawienia &gt; Podział magazynu &gt; Magazyny**. Na karcie **Planowanie główne** zobacz grupę pól **Magazyn główny**.
-   Domyślny typ zamówienia to Produkcja, Zamówienie zakupu lub Kanban. Kliknij kolejno opcje **Zarządzanie informacjami o produktach &gt; Produkty&gt; Zwolnione produkty**. Wybierz odpowiedni towar i kliknij kolejno opcje **Plan &gt; Ustawienia domyślne zamówień**. W formularzu **Ustawienia domyślne zamówień** zobacz pole **Domyślny typ zamówienia**.

![Popyt dla zapotrzebowania oddziału, magazyn niewymagany    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Dodatkowe zasoby
--------

[Omówienie planowania głównego i funkcjonalności wielooddziałowości](master-plan-multisite-functionality.md)

[Planowanie główne dla zapotrzebowania oddziału i magazynu, magazyn wymagany](master-plan-site-coverage-warehouse-mandatory.md)

[Planowanie główne dla zapotrzebowania oddziału, magazyn wymagany](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Planowanie główne dla zapotrzebowania oddziału, magazyn niewymagany](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Ustalanie wersji BOM](master-plan-bom-version-determined.md)



