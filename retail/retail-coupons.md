---
title: "Tworzenie kuponów dla sieci sprzedaży"
description: "Ten temat zawiera omówienie koncepcji kuponów handlu detalicznego oraz wyjaśnienie, jak je konfigurować."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: cebd1b6f041e18c2e016142aba7447bf813f570b
ms.openlocfilehash: fb013d3695870cb3b69ac41ff488f0865a648be4
ms.contentlocale: pl-pl
ms.lasthandoff: 06/19/2017


---

# Tworzenie kuponów dla sieci sprzedaży
<a id="create-coupons-for-retail-sales" class="xliff"></a>

[!include[banner](includes/banner.md)]


## Ogólne informacje o kuponach
<a id="overview-of-coupons" class="xliff"></a>

Kupony to kody i kody kreskowe używane w celu dodawania rabatów detalicznych do transakcji. Każdy kupon może mieć wiele kodów, a każdy kod może mieć własną datę wejścia w życie. 

Każdy kupon jest powiązany z jednym rabatem detalicznym. Grupy cenowe skojarzone z rabatem określają odbiorców, którzy mogą używać kuponu, lub kanały, w których kupon obowiązuje. 

Zasadniczo kupony są dodatkową weryfikacją nad rabatami detalicznymi. Kupon zawiera wymagane kody kuponu i kody kreskowe oraz zakresy dat dla tych kodów. Kupon określa również opcjonalne limity wykorzystania oraz wymagane właściwości odbiorcy. Rabat określa zbiór produktów, dla których kupon jest ważny. Grupy cenowe rabatu określają zbiór odbiorców, kanały lub katalogi, dla których kupon jest ważny.

Aby utworzyć kuponu, należy utworzyć oddzielnie rabat i kupon. Następnie trzeba połączyć te elementy, zaznaczając rabat na stronie kuponu w programie Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Po połączeniu kuponu z rabatem kilka pól na stronie rabatu w programie Microsoft Dynamics 365 for Retail staje się tylko do odczytu, ponieważ są one zarządzane przez ustawienia kuponu. Są to m.in. pola stanu i standardowych zakresów dat.

### Kupony o ograniczonym użyciu
<a id="limited-use-coupons" class="xliff"></a>

Kupony można skonfigurować jako kupony o ograniczonym użyciu. Limit użycia można zdefiniować dla klienta lub kanału lub jako limit globalny. Ten limit jest wymuszany podczas wprowadzania lub skanowania kodu lub kodu kreskowego w punkcie sprzedaży albo podczas wprowadzania zamówienia sprzedaży. Kupon jest rejestrowany jako użyty po sfinalizowaniu zamówienia, z którym jest skojarzony kupon.

Limit jest wymuszany dla kodu kuponu na kuponie. Na przykład kupon jednorazowego użytku, który zawiera dwa kody kuponu, może zostać wykorzystany dwukrotnie, po jednym razie dla każdego kodu kuponu. Każdy kod na kuponie można niezależnie ustawić jako aktywny.

## Zarządzanie kuponami
<a id="managing-coupons" class="xliff"></a>

Rabat i kupon należy utworzyć oddzielnie. Następnie trzeba połączyć te elementy, zaznaczając rabat na stronie kuponu. Po połączeniu kuponu z rabatem kilka pól na stronie rabatu staje się tylko do odczytu, ponieważ są one zarządzane przez ustawienia kuponu. Są to m.in. pola stanu i standardowych zakresów dat.  

Zasadniczo kupony są dodatkową weryfikacją nad rabatami detalicznymi. Kupon zawiera kody kuponu i kody kreskowe, zakresy dat dla tych kodów, limity użycia oraz wymagane właściwości odbiorcy. Rabat określa zbiór produktów, dla których kupon jest ważny. Grupy cenowe rabatu określają zbiór odbiorców, kanały lub katalogi, dla których kupon jest ważny.

## Konfiguracja systemu dla kuponów
<a id="system-setup-for-coupons" class="xliff"></a> 

Zanim będzie można utworzyć kupon, należy skonfigurować kod kreskowy kuponu i dwie numeracje kuponu. 

1.  Na stronie **Znaki maski** utwórz nowy znak maski dla kodu kuponu. Można wybrać dowolny nieużywany znak.
2.  Na stronie **Ustawienia maski kodów kreskowych** utwórz nową maskę kodów kreskowych. W polu **Typ** ustaw wartość **Kupon**.
3.  Na stronie **Ustawienia kodów kreskowych** utwórz nowy kod kreskowy, który wykorzystuje utworzoną maskę kodów kreskowych.
4.  Na stronie **Sekwencje identyfikatorów** utwórz dwie nowe numeracje. Jedna numeracja jest przeznaczona dla identyfikatora kod kuponu, a druga dla numeru kuponu. Identyfikator kodu kuponu jest unikatowym identyfikatorem każdego kodu kuponu na kuponie. Numer kuponu to jego unikatowy identyfikator. Każdy kupon może zawierać wiele kodów i kodów kreskowych, które inicjują realizację kuponu.

    > [!NOTE]
    > Dla obu numeracji należy w polu **Zakres** ustawić wartość **Firma**. W większości przypadków numery w obu numeracjach powinny być generowane automatycznie.

5.  Na stronie **Wspólne parametry sieci sprzedaży** na karcie **Kody kreskowe** zaznacz utworzony wcześniej kod kreskowy.
6.  Na stronie **Parametry sieci sprzedaży** na karcie **Sekwencje identyfikatorów** zaznacz utworzone przez siebie numeracje numeru kuponu i identyfikatora kod kuponu.
7.  Teraz można otworzyć stronę **Kupony** i utworzyć nowe kupony.

## Wpływ częściowych aktualizacji na kupony
<a id="the-effect-of-partial-updates-on-coupons" class="xliff"></a>

Funkcjonalność kuponów obejmuje wiele odrębnych funkcji w programie Dynamics 365 for Retail. Program Microsoft Dynamics 365 for Retail Headquarters (HQ) i kanał mogą być częściowo aktualizowane w różnych składnikach. Dlatego trzeba dokładnie rozumieć, jak częściowe aktualizuje wpływają na całą funkcjonalność kuponów.

- **Program HQ jest częściowo zaktualizowany, ale aplikacje Retail Server i POS nie są zaktualizowane.** W aktualizacji programu HQ są aktualizowane strony kuponu i rabatu oraz aparat ustalania cen detalicznych. Jeśli tylko jeden z tych dwóch składników zostanie zaktualizowany, niektóre strony w module Retail będą zawierały niezgodne dane obliczania cen. W związku z tym podczas obliczania rabatów mogą się pojawić nieoczekiwane obliczenia rabatów lub błędy.
- **Program HQ jest zaktualizowany, ale aplikacje Retail Server i POS nie są zaktualizowane (N-1).** Ponieważ nie wszystkie sklepy detaliczne mogą zostać zaktualizowane w tym samym czasie, zaleca się, aby przed zaktualizowaniem sklepów detalicznych zaktualizować aplikację HQ. W scenariuszu N-1 nowe funkcje dotyczące kuponów nie będą dostępne w sklepach, które nie zostały jeszcze zaktualizowane. Na przykład funkcjonalność kuponów wprowadza wiersze wykluczenia. Użycie opcji wykluczenia do wierszy rabatu spowoduje, że nie będą one stosowane w sklepie detalicznym, który korzysta ze starszej wersji.
- **Program HQ nie jest zaktualizowany, ale aplikacje Retail Server i POS są zaktualizowane (N+1).** Ponieważ zaktualizowany aparat kalkulacji cen w aplikacji Retail Server może obsługiwać starsze kody rabatów podczas obliczania cen, aktualizacja nie powinna mieć żadnego funkcjonalnego wpływu w tym scenariuszu.
