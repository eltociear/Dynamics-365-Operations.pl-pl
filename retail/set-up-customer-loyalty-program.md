---
title: "Konfigurowanie programu lojalnościowego"
description: "W tym artykule opisano sposób konfigurowania programu lojalnościowego. Programy lojalnościowe mogą pomóc zwiększyć lojalność odbiorców poprzez wynagradzanie ich za zakup produktów w sklepach sieci sprzedaży. W programie Microsoft Dynamics 365 for Operations można skonfigurować proste lub złożone programy lojalnościowe, które mają zastosowanie w firmach w dowolnym kanale sprzedaży detalicznej."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 04521c20ddeca1154b134b23c1db69f45c554ed3
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-a-customer-loyalty-program"></a>Konfigurowanie programu lojalnościowego

[!include[banner](includes/banner.md)]


W tym artykule opisano sposób konfigurowania programu lojalnościowego. Programy lojalnościowe mogą pomóc zwiększyć lojalność odbiorców poprzez wynagradzanie ich za zakup produktów w sklepach sieci sprzedaży. W programie Microsoft Dynamics 365 for Operations można skonfigurować proste lub złożone programy lojalnościowe, które mają zastosowanie w firmach w dowolnym kanale sprzedaży detalicznej.

<a name="loyalty-features"></a>Funkcje lojalnościowe
----------------

Program lojalnościowy można skonfigurować w taki sposób, żeby zawierał następujące opcje:

-   Konfigurowanie wielu typów nagród ofertowanych w programach lojalnościowych, a następnie śledzenie uczestnictwa w programach lojalnościowych.
-   Konfigurowanie programów lojalnościowych reprezentujących różne oferowane premie nagród. Można dołączyć warstwy programu lojalnościowego, aby oferować większe premie i nagrody dla klientów, którzy często kupują zakupów lub wydają więcej pieniędzy w sklepach.
-   Określanienie reguł dochodów w celu identyfikacji działań, jakie odbiorca musi wykonać, aby zdobyć nagrody. Można także zdefiniować reguły realizacji, określające, kiedy i jak odbiorca może odebrać nagrody.
-   Wystawianie kart lojalnościowych z dowolnego kanału sprzedaży detalicznej, który bierze udział w programach lojalnościowych, i łączenie kart lojalnościowych z jednym lub kilkoma programami lojalnościowymi, w których odbiorcy mogą brać udział. Można też połączyć rekord odbiorcy z kartą lojalnościową, aby umożliwić odbiorcy gromadzenie puli punktów lojalnościowych z wielu kart oraz ich wykorzystywanie.
-   Ręczne dopasowanie kart lojalnościowych lub przeniesienie salda nagród w programie lojalnościowym z jednej karty do drugiej w celu dostosowania lub nagrodzenia odbiorcy.

## <a name="setting-up-loyalty-programs"></a>Konfigurowanie programów lojalnościowych
Należy skonfigurować kilka składników, aby włączyć funkcję lojalnościową w module Dynamics 365 for Operations — Handel detaliczny. Na poniższym diagramie przedstawiono składniki lojalnościowe i ich relacje względem siebie. ![Przebieg procesu konfigurowania systemu lojalności](./media/loyaltyprocess.gif)

## <a name="loyalty-components"></a>Składniki lojalnościowe
W poniższej tabeli opisano każdy składnik i miejsce, w którym jest on używany w konfiguracji lojalnościowej.

| Składnik                                        | Opis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Miejsce użycia                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurowanie rabatów (wymaganie wstępne)                  | Konfigurowanie rabatów, które możesz zaoferować odbiorcom lojalnościowych. Możesz na przykład zaoferować 5 procent mniej za wszystkie produkty odzieżowe.                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Rabaty muszą zostać dodane do grup cenowych, aby zostały uwzględnione w programie lojalnościowym. Grupy cenowe są przypisywane do warstwy lojalnościowej i programów lojalnościowych.                                                                                                                                                                                                                      |
| Konfigurowanie grup cenowych (wstępne wymaganie)               | Grupy cenowe są używane do tworzenia i obsługi cen i rabatów dla produktów sieci sprzedaży. Konfigurowanie grup cenowych, zawierających rabaty, które mają zastosowanie do programów lojalnościowych.                                                                                                                                                                                                                                                                                                                                                                                                             | Grupy cenowe są przypisywane do warstwy lojalnościowej i programów lojalnościowych.                                                                                                                                                                                                                                                                                                        |
| Konfigurowanie kanałów (wymaganie wstępne)                   | Kanały sprzedaży detalicznej to sklepy uczestniczące w programach lojalnościowych, takie jak sklepy tradycyjne, sklepy internetowe i biura obsługi. Przed przypisaniem programów lojalnościowych do nich, należy skonfigurować kanały sprzedaży detalicznej.                                                                                                                                                                                                                                                                                                                                                      | Kanały sprzedaży detalicznej należy przypisać do programu lojalnościowego w przypadku, gdy kanał sprzedaży detalicznej bierze udział w programie lojalnościowym.                                                                                                                                                                                                                                                                  |
| Konfigurowanie metody płatności w programie lojalnościowym (wymaganie wstępne) | Należy skonfigurować metodę płatności, zanim będzie można użyć karty lojalnościowej przy kasie i zanim będzie można zrealizować punkty lojalnościowe jako część programu lojalnościowego. Metodę płatności w programie lojalnościowym należy również dodać do kanału sprzedaży detalicznej, aby odbiorcy mogli realizować ich punkty lojalnościowe jako płatność dla produktów.                                                                                                                                                                                                                                                                                           | Konfiguracja metody typu płatności w programie lojalnościowym, a następnie przypisanie metody płatności w programie lojalnościowym w kanałach sprzedaży detalicznej, uczestniczących w programie lojalnościowym.                                                                                                                                                                                                                          |
| Konfigurowanie zakresów dat                            | Zakresy dat umożliwiają elastyczne ustawianie odstępów czasu dla warstw lojalnościowych. Użyj zakresów dat do określenia, jak długo klient może zostać w warstwie lub ile czasu klient ma na ukończenie aktywności, by spełnić wymagania warstwy.                                                                                                                                                                                                                                                                                                                                            | Zakresy dat mają zastosowanie tylko w przypadku korzystania z warstw w programach lojalnościowych. Można wybrać zakres dat, ktory ma zastosowanie do warstwy programu, a także zakresy dat, które dotyczą reguł warstwy programu.                                                                                                                                                                                  |
| Konfigurowanie punktów lojalnościowych                             | Punkty lojalnościowe to typy nagród oferowane odbiorcom. Punkty lojalnościowe mogą być wymienialne lub nie. Wymienialne punkty lojalnościowe mogą zostać wymienione na produkty. Niewymienialne punkty lojalnościowe są używane do celów śledzenia lub do przeniesienia odbiorcy do następnej warstwy w programie lojalnościowym.                                                                                                                                                                                                                                                                          | Punkty lojalnościowe znajdują odwołanie w regułach warstwy i są używane do kwalifikowania odbiorcy dla określonej warstwy. Punkty lojalnościowe znajdują też odwołanie w programach lojalnościowych w regułach zdobywania i realizacji punktów. W regułach zdobywania, można określić nagrody, które odbiorcy mogą uzyskać dla określonego działania. W regułach wykorzystywania określa się nagrody, które odbiorca może zrealizować.                  |
| Konfigurowanie programów lojalnościowych                          | Programy lojalnościowe to podstawowa jednostka lojalnościowa, jaką oferujesz. Każdy program lojalnościowy może mieć przypisane warstwy lojalnościowe. Grupy cen i rabatów są przypisywane do programów lojalnościowych na poziomie programu lub poziomie warstwy.                                                                                                                                                                                                                                                                                                                                             | Dla programów programów lojalnościowych tworzy się schematy lojalnościowe. Karty lojalnościowe przypisuje się do programów lojalnościowych, karty lojalnościowe można przypisać do odbiorcy. Kanały sprzedaży detalicznej uczestniczą w programach lojalnościowych, które są przypisane do schematów lojalnościowych. Wszyscy odbiorcy, którzy mają kartę lojalnościową, mogą uczestniczyć w programach lojalnościowych, które są przypisane do karty.            |
| Konfigurowanie warstw lojalności i reguł warstwy              | Warstwy lojalnościowe to opcjonalne poziomy, które można zdefiniować dla programów lojalnościowych. Można skonfigurować podstawowe rabaty i nagrody dla wszystkich odbiorców, którzy biorą udział w programie lojalnościowym; można skonfigurować dodatkowe rabaty i nagrody dla odbiorców, którzy zdobywają różne poziomy w programie. Dla każdej definiowanej warstwy lojalnościowej można skonfigurować reguły, które kwalifikują odbiorcę dla każdej warstwy. Można także zdefiniować, jak długo klient może pozostawać w tej warstwie po jej osiągnięciu.                                                                                  | Warstwy lojalnościowe i zasady dotyczące warstwy lojalnościowej są definiowane w programach lojalnościowych. Jeśli nie zdefiniowano żadnych warstw lojalnościowych, wszyscy odbiorcy, którzy uczestniczą w programie lojalnościowym, kwalifikują się do rabatów, które można przypisać w grupie cenowej programu lojalnościowego. Po zdefiniowaniu warstw lojalnościowych można skonfigurować reguły zdobywania i reguły realizacji dla warstw lojalnościowych w programie lojalnościowym. |
| Konfigurowanie programów lojalnościowych                           | Schematy lojalnościowe określają reguły zdobywania i realizacji, które dotyczą wybranego programu lojalnościowego. Kanały sprzedaży detalicznej są przypisywane do schematu lojalnościowego, aby określić, który program lojalnościowy, reguły zdobywania i reguły realizacji stosuje się do sklepu sieci sprzedaży.                                                                                                                                                                                                                                                                                                                                  | Schemat lojalnościowy jest przypisany do programu lojalnościowego oraz do kanałów sprzedaży detalicznej. Do tego samego programu lojalnościowego można przypisać wiele schematów lojalnościowych; wiele schematów lojalnościowych można przypisać do wielu kanałów sprzedaży detalicznej.                                                                                                                                                                        |
| Konfigurowanie kart lojalnościowych                             | Karta lojalnościowa upoważnia posiadacza karty do uczestnictwa w programach lojalnościowych, które są przypisane do karty. Można wystawiać karty lojalnościowe anonimowo lub mogą być przypisane do określonego odbiorcy. Możliwe jest przeglądanie transakcji w programie lojalnościowym dla określonej karty; można wyświetlić podsumowanie punktów lojalnościowych, które zostały zgromadzone na karcie. Można wystawiać karty lojalnościowe z dowolnego kanału sprzedaży detalicznej. Można również ręcznie zmienić kartę lojalnościową, aby uaktualnić odbiorcę do innej warstwy, dodać punkty lojalnościowe lub przenieść saldo punktów lojalnościowych z jednej karty na inną. | Programy lojalnościowe są przypisywane do karty lojalnościowej.                                                                                                                                                                                                                                                                                                                                  |

## <a name="loyalty-processes"></a>Procesy lojalnościowe
W poniższej tabeli opisano procesy, które należy wykonać, aby wysłać konfiguracje lojalnościowe i dane do sklepów i pobrać transakcje lojalnościowe ze sklepów.

| Nazwa procesu                         | Opis                                                                                                                                                                                                                                                                                                                                                                                                    | Nazwa strony                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| 1050 (informacje o lojalności)           | Uruchom ten proces w celu wysyłania danych lojalnościowych z programu Dynamics 365 for Operations do sklepów sieci sprzedaży. Dobrze jest zaplanować częste wykonywanie tego procesu, tak aby dane lojalnościowe były przesyłane do wszystkich sklepów.                                                                                                                                                                                               | Harmonogram dystrybucji                |
| Przetwarzanie programów lojalnościowych              | Uruchom ten proces, aby skojarzyć schematy lojalnościowe z kanałami sprzedaży detalicznej, do których jest przypisany schemat lojalnościowy. Ten proces może zostać zaplanowany do uruchamiania jako zadanie wsadowe. Należy uruchamiać ten proces przy każdej zmianie danych konfiguracji lojalności, takich jak harmonogramy, programy lojalnościowe lub punkty lojalnościowe.                                                                                               | Przetwarzanie programów lojalnościowych              |
| Przetwarzaj transakcje programu lojalnościowego w trybie offline | Uruchom ten proces, aby zaktualizować karty lojalnościowe tak, aby uwzględniały transakcje przetworzone w trybie offline. Ten proces ma zastosowanie tylko wtedy, gdy jest zaznaczone pole wyboru **Uzyskaj w trybie offline** na stronie **Wspólne parametry sieci sprzedaży**, dzięki czemu możliwie jest odbieranie nagród w trybie offline.                                                                                                                                               | Przetwarzaj transakcje programu lojalnościowego w trybie offline |
| Aktualizuj warstwy kart lojalnościowych            | Uruchom ten proces, aby ocenić aktywność zdobywania punktów odbiorcy pod kątem reguł warstwy dla programu lojalnościowego oraz zaktualizować stan warstwy odbiorcy. Ten proces jest wymagany tylko, gdy zmienisz reguły warstwy w programach lojalnościowych i chcesz wstecznie zastosować zaktualizowane reguły do kart lojalnościowych, które zostały już wystawione. Ten proces może być uruchamiany jako zadanie wsadowe lub dla poszczególnych kart. | Aktualizuj warstwy kart lojalnościowych            |





