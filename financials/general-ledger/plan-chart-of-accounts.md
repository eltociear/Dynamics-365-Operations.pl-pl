---
title: Planowanie planu kont
description: "Ten artykuł zawiera informacje, które pomogą zaprojektować plan kont w organizacji."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c57c4fe8cc66228062f7b64c88efe255657d016
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="plan-your-chart-of-accounts"></a>Planowanie planu kont

[!include[banner](../includes/banner.md)]


Ten artykuł zawiera informacje, które pomogą zaprojektować plan kont w organizacji.

Do śledzenia i obsługi informacji finansowych w organizacji można skonfigurować plan kont. Plan kont jest to zbiór kont, które definiują ramy finansowe. Aby jeszcze dokładniej śledzić transakcje na tych kontach, można dodawać segmenty nazywane wymiarami finansowymi. Na przykład, konto wydatków może zawierać wymiary finansowe o nazwie Dział, MPK oraz Cel. Zdefiniowane przez użytkownika reguły, nazywane strukturami kont i regułami zaawansowanymi, decydują o tym, jak te wymiary finansowe są dołączane do kont głównych i innych wymiarów finansowych, i jak wprowadzane są transakcje. 

Plan kont jest to ustrukturalizowana lista kont księgi głównej firmy. Lista służy do przygotowywania raportów finansowych dla urzędów i właścicieli. Konta są pogrupowane w typy i połączone w większe kategorie. Na poziomie najbardziej ogólnym, konta są pogrupowane jako przychody i koszty (konta operacyjne) oraz jako aktywa i pasywa (konta bilansowe). 

Plan kont może być udostępniany i używany przez dowolną firmę w organizacji. Plan kont używany przez firmę definiuje się na stronie **Księga**. 

Oto kilka czynników, które należy uwzględnić podczas planowania struktury planu kont w organizacji:

-   Wymagania dotyczące raportowania w kraju/regionie, w którym mieści się organizacja
-   Wymagania dotyczące raportowania firmy
-   Poziom wymaganej specyfikacji zarówno dla zewnętrznych organizacji, jak i dla Twojej organizacji

Plan kont tworzy się na stronie **Plan kont**. Konta główne można tworzyć na stronie **Plan kont** lub na stronie **Konta główne**. Na kontach głównych nie należy używać żadnych znaków specjalnych, które są używane jako separatory planów kont. Jeśli masz znak specjalny, który jest taki sam jak separator planu kont, może wystąpić niestabilność systemu, albo do wprowadzania konta w połączeniu z wymiarem będzie trzeba zawsze używać wyszukiwania lub okna wysuwanego. 

Dobrze jest połączyć konta główne z kategoriami konta głównego, by móc korzystać z domyślnych raportów finansowych bez konieczności wprowadzania żadnych zmian. Dzięki temu tworzenie i obsługa raportów staje się łatwiejsza. 

Strona **Skonfiguruj strukturę konta** służy do tworzenia struktur kont. Struktury kont definiują prawidłowe kombinacje. Kombinacje, łącznie z kontami głównymi, tworzą plan kont. 

**Firma zastępuje** 

Nie wszystkie konta są prawidłowe dla wszystkich firm, a niektóre mogą być dostępne tylko w określonym przedziale czasu. W tym scenariuszu sekcja Firma zastępuje może służyć do identyfikowania firm, dla których konto główne powinno być zawieszone, właściciela oraz okresu aktywności wymiaru. Zastąpienia na poziomie wspólnym nie mogą być bardziej restrykcyjne niż zastąpienia na poziomie firmy.

Aby uzyskać więcej informacji, zobacz [Wymiary finansowe](financial-dimensions.md).



