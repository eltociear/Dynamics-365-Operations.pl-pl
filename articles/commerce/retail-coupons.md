---
title: Konfigurowanie kuponów dla sprzedaży detalicznej
description: Ten temat zawiera omówienie koncepcji kuponów oraz wyjaśnienie, jak je konfigurować.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4c580e40ae1f0398ab9f8437d42ddcb2979558c3
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057378"
---
# <a name="set-up-coupons-for-retail-sales"></a>Konfigurowanie kuponów dla sprzedaży detalicznej

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Ogólne informacje o kuponach

Kupony to kody i kody kreskowe używane w celu dodawania rabatów do transakcji. Każdy kupon może mieć wiele kodów, a każdy kod może mieć własną datę wejścia w życie.

Każdy kupon jest powiązany z jednym rabatem. Grupy cenowe skojarzone z rabatem określają odbiorców, którzy mogą używać kuponu, lub kanały, w których kupon obowiązuje.

Zasadniczo kupony są dodatkową weryfikacją nad rabatami. Kupon zawiera wymagane kody kuponu i kody kreskowe oraz zakresy dat dla tych kodów. Kupon określa również opcjonalne limity wykorzystania oraz wymagane właściwości odbiorcy. Rabat określa zbiór produktów, dla których kupon jest ważny. Grupy cenowe rabatu określają zbiór odbiorców, kanały lub katalogi, dla których kupon jest ważny.

Aby utworzyć kuponu, należy utworzyć oddzielnie rabat i kupon. Następnie trzeba połączyć te elementy, zaznaczając rabat na stronie kuponu w Commerce.

> [!NOTE]
> Po połączeniu kuponu z rabatem kilka pól na stronie rabatu w Commerce staje się tylko do odczytu, ponieważ są one zarządzane przez ustawienia kuponu. Są to m.in. pola stanu i standardowych zakresów dat.

### <a name="limited-use-coupons"></a>Kupony o ograniczonym użyciu

Kupony można skonfigurować jako kupony o ograniczonym użyciu. Limit użycia można zdefiniować dla klienta lub kanału lub jako limit globalny. Ten limit jest wymuszany podczas wprowadzania lub skanowania kodu lub kodu kreskowego w punkcie sprzedaży albo podczas wprowadzania zamówienia sprzedaży.

Limit jest wymuszany dla kodu kuponu na kuponie. Na przykład kupon jednorazowego użytku, który zawiera dwa kody kuponu, może zostać wykorzystany dwukrotnie, po jednym razie dla każdego kodu kuponu. Każdy kod na kuponie można niezależnie ustawić jako aktywny.

> [!NOTE]
> Gdy kod kuponu osiągnie limit wykorzystania, system *nie* zmienia automatycznie stanu kod kuponu na „Wykorzystane”. Jednak system nie pozwala na dalsze używanie kodu kuponu, który osiągnął limit wykorzystania. Jeśli stan kodu kuponu zostanie ręcznie ustawiony na wartość inną niż „Aktywne”, to kodu kuponu nie można użyć w żadnym kanale.

## <a name="managing-coupons"></a>Zarządzanie kuponami

Rabat i kupon należy utworzyć oddzielnie. Następnie trzeba połączyć te elementy, zaznaczając rabat na stronie kuponu. Po połączeniu kuponu z rabatem kilka pól na stronie rabatu staje się tylko do odczytu, ponieważ są one zarządzane przez ustawienia kuponu. Są to m.in. pola stanu i standardowych zakresów dat.

Zasadniczo kupony są teraz dodatkową weryfikacją nad rabatami. Kupon zawiera kody kuponu i kody kreskowe, zakresy dat dla tych kodów, limity użycia oraz wymagane właściwości odbiorcy. Rabat określa zbiór produktów, dla których kupon jest ważny. Grupy cenowe rabatu określają zbiór odbiorców, kanały lub katalogi, dla których kupon jest ważny.

## <a name="system-setup-for-coupons"></a>Konfiguracja systemu dla kuponów

Zanim będzie można utworzyć kupon, należy skonfigurować kod kreskowy kuponu i dwie numeracje kuponu.

1. Na stronie **Znaki maski** utwórz nowy znak maski dla kodu kuponu. Można wybrać dowolny nieużywany znak.
2. Na stronie **Ustawienia maski kodów kreskowych** utwórz nową maskę kodów kreskowych. W polu **Typ** ustaw wartość **Kupon**.
3. Na stronie **Ustawienia kodów kreskowych** utwórz nowy kod kreskowy, który wykorzystuje utworzoną maskę kodów kreskowych.
4. Na stronie **Sekwencje identyfikatorów** utwórz dwie nowe numeracje. Jedna numeracja jest przeznaczona dla identyfikatora kod kuponu, a druga dla numeru kuponu. Identyfikator kodu kuponu jest unikatowym identyfikatorem każdego kodu kuponu na kuponie. Numer kuponu to jego unikatowy identyfikator. Każdy kupon może zawierać wiele kodów i kodów kreskowych, które inicjują realizację kuponu.

    > [!NOTE]
    > Dla obu numeracji należy w polu **Zakres** ustawić wartość **Firma**. W większości przypadków numery w obu numeracjach powinny być generowane automatycznie.

5. Na stronie **Parametry handlu** na karcie **Kody kreskowe** zaznacz utworzony wcześniej kod kreskowy.
6. Na stronie **Wspólne parametry handlu** na karcie **Sekwencje numerów** zaznacz utworzone przez siebie numeracje numeru kuponu i identyfikatora kod kuponu.
7. Teraz można otworzyć stronę **Kupony** i utworzyć nowe kupony.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Wpływ częściowych aktualizacji na kupony

Funkcjonalność kuponów obejmuje wiele odrębnych funkcji. Program Commerce Headquarters (HQ) i kanał mogą być częściowo aktualizowane w różnych składnikach. Dlatego trzeba dokładnie rozumieć, jak częściowe aktualizuje wpływają na całą funkcjonalność kuponów.

- **Program HQ jest częściowo zaktualizowany, ale aplikacje Commerce Scale Unit i POS nie są zaktualizowane.** W aktualizacji programu HQ są aktualizowane strony kuponu i rabatu oraz aparat ustalania cen. Jeśli tylko jeden z tych dwóch składników zostanie zaktualizowany, niektóre strony w module Commerce będą zawierały niezgodne dane obliczania cen. W związku z tym podczas obliczania rabatów mogą się pojawić nieoczekiwane obliczenia rabatów lub błędy.
- **Program HQ jest zaktualizowany, ale aplikacje Commerce Scale Unit i POS nie są zaktualizowane (N-1).** Ponieważ nie wszystkie sklepy mogą zostać zaktualizowane w tym samym czasie, zaleca się, aby przed zaktualizowaniem sklepów zaktualizować aplikację HQ. W scenariuszu N-1 nowe funkcje dotyczące kuponów nie będą dostępne w sklepach, które nie zostały jeszcze zaktualizowane. Na przykład funkcjonalność kuponów wprowadza wiersze wykluczenia. Użycie opcji wykluczenia do wierszy rabatu spowoduje, że nie będą one stosowane w sklepie, który korzysta ze starszej wersji.
- **Program HQ nie jest zaktualizowany, ale aplikacje Commerce Scale Unit i POS są zaktualizowane (N+1).** Ponieważ zaktualizowany aparat kalkulacji cen w aplikacji Commerce Scale Unit może obsługiwać starsze kody rabatów podczas obliczania cen, aktualizacja nie powinna mieć żadnego funkcjonalnego wpływu w tym scenariuszu.
