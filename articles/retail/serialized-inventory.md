---
title: "Ulepszenie punktu sprzedaży dla produktów seryjnych"
description: "Ten temat zawiera listę ulepszeń wprowadzonych w produktach seryjnych, aby umożliwić oszczędność czasu i zwiększenie efektywności działania."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9eb962e903ac9ee359134cae35ebd399e23cc4e1
ms.contentlocale: pl-pl
ms.lasthandoff: 11/03/2017

---

# <a name="pos-improvements-for-serialized-products"></a>Ulepszenie punktu sprzedaży dla produktów seryjnych

[!include[banner](includes/banner.md)]

## <a name="overview"></a>Przegląd 
Na podstawie ustawień w module Centrala sieci sprzedaży produkty można sklasyfikować jako seryjne lub nieseryjne. Jeżeli produkty są seryjne, do każdej pozycji można przypisać unikatowy numer ułatwiający śledzenie gwarancji, śledzenie pozycji i potwierdzenie własności. Mimo że możliwość podania numerów seryjnych dla produktów seryjnych była dostępna w aplikacji Modern/Cloud Point of Sale (POS), dodano ulepszenia zapewniające kasjerom oszczędność czasu i zwiększenie wydajności pracy.  

## <a name="pos-improvements"></a>Ulepszenia punktu sprzedaży

- **Numery seryjne nie są wymagane aż do realizacji zamówienia** — wcześniej kasjer, który dodał do transakcji produkt seryjny musiał podać numer seryjny. To wymaganie było problemem w scenariuszach obsługi relacji z klientami, jeżeli kasjerzy i sprzedawcy mieli możliwość sprzedaży dodatkowych produktów. Do momentu płatności produkty były często aktualizowane w koszyku. Dlatego za każdym razem, gdy kasjer dodał nowy produkt, system wyświetlał monit o podanie numeru seryjnego. Okno dialogowe numeru seryjnego zawiera teraz przycisk **Dodaj później**. Dlatego sprzedawcy mogą dodać pozycję do transakcji, ale podać numer seryjny później. Sprzedawcy mogą szybko dodać i zastąpić pozycje seryjne w koszyku, a następnie podać numer seryjny przed realizacją transakcji. Jeżeli numer seryjny nie zostanie podany dla żadnego produktu seryjnego, kasjer, który spróbuje dokończyć transakcję zobaczy komunikat o błędzie. Ten komunikat informuje o tym, że przed kontynuacją kasjer musi podać brakujące numery seryjne.

    Dla każdej pozycji seryjnej, dla której numer seryjny został pominięty pod wierszem transakcji wyświetlany jest komentarz. Ten komentarz informuje, że nie podano numeru seryjnego dla pozycji. Dlatego kasjer może szybko znaleźć pozycje, w których brakuje numeru seryjnego.

    Nowe operacja **Dodaj numer seryjny** także umożliwia podanie numeru seryjnego dla pozycji, dla których brakuje numeru seryjnego. Po podaniu numeru seryjnego nie można go edytować. Kasjer musi unieważnić wiersz i dodać produkt ponownie. 
    
- **Numery seryjne nie są wymagane w celu złożenia zamówień odbiorcy** — zamówienia odbiorcy można złożyć w jednym sklepie, a zrealizować w innym. Kasjer, który składa zamówienie odbiorcy nie musi podawać numeru seryjnego. Numer seryjny zostanie podany na etapie pobierania lub odbioru. Numer seryjny należy jednak podać dla wszystkich pozycji wierszy, dla których wybrano typ dostawy **Wynieś**. W przeciwnym razie nie można dokończyć transakcji.    
- **Produkty seryjne nie są agregowane na ekranie transakcji** — ustawienie **Agreguj produkty** w grupie pola **Terminal** na stronie **Profil funkcji** umożliwia agregowanie tych samych produktów nieseryjnych na ekranie transakcji. Gdy agregowane są te same produkty, łatwiej je zobaczyć w siatce transakcji. Ponieważ jednak numery seryjne są unikatowe, a sprzedawcy nie muszą wprowadzać numerów seryjnych do momentu realizacji transakcji, ustawienie **Agreguj produkty** nie dotyczy produktów seryjnych. Dlatego produkty seryjne nie będą agregowane na ekranie transakcji, jeżeli wybrano ustawienie **Agreguj produkty**.
