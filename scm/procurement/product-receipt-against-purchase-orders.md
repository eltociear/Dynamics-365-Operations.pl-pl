---
title: "Przyjęcie produktów względem zamówień zakupu"
description: "W tym artykule opisano różne opcje rejestrowania produktów jako przyjętych."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5d1b063344d4191facf2ddace5f5c9d592fb0942
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="product-receipt-against-purchase-orders"></a>Przyjęcie produktów względem zamówień zakupu

[!include[banner](../includes/banner.md)]


W tym artykule opisano różne opcje rejestrowania produktów jako przyjętych.

Przyjęcie produktów to proces rejestrowania, że zamówione produkty zostały odebrane, wskutek czego wiersze zamówienia zakupu mogą być przetwarzane na potrzeby fakturowania. W niektórych przypadkach produkty są poddawane wstępnej rejestracji, w której przed przyjęciem produktów są odnotowywane dodatkowe informacje od dostawcy. Po przybyciu produktów są one najpierw oznaczane jako **Zarejestrowane**. Produkty mogą następnie przejść przez dodatkowe procesy, takie jak zarządzanie jakością, zanim ostatecznie są oznaczone jako **Otrzymane**.

## <a name="preregistration-asn"></a>Wstępna rejestracja (WPW)
Dostawcy mogą udostępniać informacje o produktach, które zostaną wysłane. W takim przypadku można wstępnie zarejestrować produkty, aby odnotować te informacje, zanim produkty zostaną odebrane. Wstępna rejestracja produktów zmniejsza ilość pracy wymaganej podczas rejestracji i przyjęcia. Dostawcy mogą udostępniać informacje o produktach elektronicznie za pośrednictwem wcześniejszego powiadomienia o wysyłce (WPW), który jest następnie automatycznie rejestrowane w systemie. Informacje w WPW obejmują ilość produktów, które zostaną wydane, oraz datę wysyłki. WPW może również zawierać informacje takie jak dane partii lub numery seryjne. Rejestracja WPW następuje w module **Zarządzanie transportem**.

## <a name="registration"></a>Rejestracja
Rejestrowanie przyjęcia produktów często następuje w dokach rozładunkowych w magazynie. Wykonuje się je przy użyciu ręcznego urządzenia albo za pomocą arkuszy przyjęć. Alternatywnie można ręcznie zarejestrować przyjęcie produktów za pomocą operacji **Rejestracja** na stronie **Zamówienie zakupu**. W obu przypadkach produkty są oznaczone jako **Zarejestrowane**. Należy zauważyć, że produkty nie są jeszcze oznaczone jako **Otrzymane**.  

Produkty przyjęte do magazynu mogą przechodzić kontrolę jakości, zanim zostaną odłożone do zapasów. Do wykonywania kontroli jakości mogą być używane zlecenia kontroli jakości lub zlecenia kwarantanny. Jeśli są używane zlecenia kontroli jakości, można skonfigurować proces tymczasowego blokowania produktów za pomocą rezerwacji na okres, gdy są kontrolowane. Jeśli są używane zlecenia kwarantanny, produkty są przenoszone do innego magazynu w celu kontroli. Ten magazyn jest nazywany magazynem kwarantanny. W obu procesach kontroli jakości niektóre towary mogą zostać uznane za odpadki, ponieważ nie spełniają oczekiwań jakościowych albo kontrola jakości obejmuje badania niszczące próbki produktu.

## <a name="product-receipt"></a>Dokument przyjęcia produktów
Najczęściej do oznaczania produktów z zamówienia zakupu jako **Otrzymane** jest używana operacja **Dokument przyjęcia produktów** znajdująca się na karcie **Zamówienie zakupu**. Strona **Księgowanie dokumentu przyjęcia produktów** zawiera różne opcje dotyczące ilości ujmowanej jako przyjęta. Na przykład w polu **Ilość** można ustawić wartość **Ilość zamówiona** lub **Ilość dostarczana teraz**. Alternatywnie w przypadku używania procesu przybycia do magazynu często w tym polu ustawia się wartość **Ilość zarejestrowana**. Można zmodyfikować ilości w każdym wierszu zamówienia, który ma zostać oznaczony jako **Otrzymane**, aby uwzględnić wszelkie rozbieżności, takie jak niedobór w dostawie i nadwyżka w dostawie. Podczas przyjęcia produktów należy podać identyfikator przyjęcia produktów, którym zazwyczaj jest odwołanie do dokumentu dostawy od dostawcy. Ten identyfikator jest wymagany przez księgowość, ponieważ umożliwia sprawdzanie lub inspekcję dokumentów dostawy od dostawcy względem faktycznie otrzymanych towarów oraz względem zaksięgowanych zapasów lub wydatków.  

Jeśli pracownik zamówił towary przy użyciu zapotrzebowania na zakup, może zostać poproszony o własnoręczne potwierdzenie otrzymania produktu. To zachowanie konfiguruje się za pomocą przepływu pracy. Można skonfigurować warunki przepływu pracy tak, aby pasowały do procesu biznesowego w firmie.  

Zamówienia zakupu mogą być tworzone dla produktów, które nie są przeznaczone na zapasy, ale są uważane za koszty. Ta kategoria obejmuje wiersze zamówień, w których produkty są oznaczone jako **Niemagazynowe** przez ich grupy modeli zapasów, a także wiersze wykorzystujące kategorie zaopatrzenia. W takim przypadku pozycje mogą nie przechodzić przez rejestrację przybycia i przyjęcie do magazynu. Zamiast tego operacja **Dokument przyjęcia produktów** jest używana do rejestrowania przyjęcia bezpośrednio w zamówieniu zakupu, a przyjęcie opiera się na ilości zamówionej, nie zarejestrowanej.  

Można tworzyć wiersze zamówienia zakupu z włączoną opcją **Nowy środek trwały**. Ta opcja wskazuje, że zakup należy uznać za środek trwały, a nie zapas. W takim przypadku skonfigurowane reguły określania środków trwałych decydują, czy zakup produktu lub kategorii przekracza określone progi i w związku z tym musi zostać potraktowany jako składnik aktywów i poddany procedurze zarządzania środkami trwałymi. Mogą również dokonywać zakupów dla istniejących środków trwałych. W takim przypadku kwota jest odpowiednio korygowana.  

Można wybrać wiele zamówień i przetwarzać przyjęcia dla nich wszystkich razem. Takie podejście nie jest stosowane bardzo często, ale można go używać, jeśli dostawca skonsolidował wysyłki do Twojej firmy w jeden ładunek. Podczas przyjmowania kupionych produktów można użyć funkcji wykonywania zbiorczych aktualizacji. Aktualizacje zbiorcze pozwalają zaksięgować jeden dokument dostawy od dostawcy dla więcej niż jednego zamówienia zakupu.  

Zamówienia zakupu mogą być tworzone na podstawie zamówienia sprzedaży, jeśli zaznaczono opcję **Dostawa bezpośrednia**. W przypadku używania dostawy bezpośredniej produkty nigdy nie przybywają do magazynu, ale są wysyłane bezpośrednio od dostawcy do odbiorcy. W takim przypadku przyjęcie jest zazwyczaj rejestrowane bezpośrednio w zamówieniu zakupu. Przyjęcie może się odbywać automatycznie, np. poprzez integrację z dostawcą za pośrednictwem systemu elektronicznej wymiany danych (EDI). Alternatywnie jeśli zamówienie zakupu jest międzyfirmowe, w momencie dostawy program Microsoft Dynamics 365 for Operations automatyzuje przyjęcie względem międzyfirmowego zamówienia sprzedaży. Gdy jest używana dostawa bezpośrednia, produkty są nadal ujmowane jako zapasy, mimo iż fizycznie nie przybywają do magazynu. W związku z tym po zarejestrowaniu przyjęcia produktów w zamówieniu zakupu zamówienie sprzedaży jest automatycznie aktualizowane o dokument dostawy, dzięki czemu łączna zmiana zapasów wynosi 0 (zero). W scenariuszach dostaw bezpośrednich nie powinno się wymagać wstępnej rejestracji. Jeśli używasz magazynów, w których włączono funkcjonalność zarządzania magazynem, można obejść wymóg rejestracji numerów identyfikacyjnych poprzez określenie wirtualnego magazynu. Taki magazyn określa się w polu **Magazyn dostawy bezpośredniej** w danych produktu. 

Po przetworzeniu przyjęcia produktów w zamówieniu zakupu stan zamówienia zakupu jest ustawiany na **Otrzymane**, aby wskazać, że można przetwarzać fakturę dla zamówienia. Można przejrzeć szczegółowe informacje o produktach, które już otrzymano, używając do tego strony **Arkusze dokumentów przyjęcia produktów**.  

Do tej strony można przejść z grupy akcji **Przyjęcie** na stronie **Zamówienie zakupu**. Informacje zawarte w arkuszach obejmują szczegóły dotyczące ilości, dat i wymiarów.

<a name="see-also"></a>Informacje dodatkowe
--------

[Omówienie zamówień zakupu](purchase-order-overview.md)

[Tworzenie zamówienia zakupu](purchase-order-creation.md)

[Zatwierdzanie i potwierdzanie zamówienia zakupu](purchase-order-approval-confirmation.md)

[Przegląd faktur od dostawcy](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)



