---
title: Konwencje amortyzacji środków trwałych
description: Ten temat zawiera omówienie konwencji amortyzacji środków trwałych.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179394"
---
# <a name="fixed-asset-depreciation-conventions"></a>Konwencje amortyzacji środków trwałych

[!include [banner](../includes/banner.md)]

Konwencje amortyzacji są używane do określenia, kiedy i jak amortyzacja jest obliczana dla roku nabycia środka trwałego i roku likwidacji środka trwałego.

Konwencje amortyzacji można przypisać do konfiguracji księgi grupy środków trwałych. Aby wyświetlić lub przypisać konwencję amortyzacji, w obszarze konfiguracji środków trwałych, należy wybrać grupy **środka trwałego**. Wybierz przycisk **Księgi**. W takim przypadku przypisane konwencje amortyzacji są używane jako wartości domyślne podczas tworzenia księgi środków trwałych. Konwencje amortyzacji można również ustawiać dla poszczególnych ksiąg środków trwałych. Aby to zrobić, wybierz **Księgi** w obszarze konfiguracji środków trwałych, a następnie wybierz przycisk **grup środków trwałych**.


|  Konwencja amortyzacji  |   Opis  |
|---------------------------|-----------------|
|           Brak            |  Środki trwałe zaczynają być amortyzowane w dniu <strong>Rozpoczęcie eksploatacji</strong>.|
|         Pół roku         |  Odejmujesz po pół roku amortyzacji w pierwszym roku i w ostatnim roku amortyzowania składnika majątku. Odejmujesz cały rok amortyzacji za każdy pozostały rok w okresie amortyzacji. |
|        Pełny miesiąc         | Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> przypadającą w dowolnym dniu w miesiącu, zaczynają się amortyzować w pierwszym dniu tego miesiąca. Środki trwałe, które zostaną wycofane w dowolnym dniu miesiąca, na potrzeby amortyzacji są traktowane jako wycofane w ostatnim dniu poprzedniego miesiąca.  |
|        Kwartał środkowy        | W celu obliczenia odpisu amortyzacyjnego za rok, w którym środek wprowadzono do eksploatacji, należy pomnożyć amortyzację za cały rok przez procent kwartału, w którym składnik majątku był w eksploatacji, jak pokazano w tabeli poniżej.<table><thead><tr><th>Kwartał</th><th>Wartość procentowa</th></tr></thead><tbody><tr><td>Pierwszy</td><td>87.5</td></tr><tr><td>Drugi</td><td>62.5</td></tr><tr><td>Trzeci</td><td>37.5</td></tr><tr><td>Czwarty</td><td>12.5</td></tr></tbody></table>Amortyzacja za pół kwartału jest uwzględniana w kwartale likwidacji (lub całkowitej amortyzacji). |
| Miesiąc środkowy (1. dzień miesiąca)  | Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w pierwszej połowie miesiąca (dni od 1 do 15), zaczynają się amortyzować w pierwszym dniu miesiąca zawierającego datę <strong>Rozpoczęcie eksploatacji</strong>. Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w drugiej połowie miesiąca (dni od 16 do końca miesiąca), zaczynają się amortyzować w pierwszym dniu miesiąca po dacie <strong>Rozpoczęcie eksploatacji</strong>. Środki trwałe, które zostaną wycofane w pierwszej połowie miesiąca (dni od 1 do 15), na potrzeby amortyzacji są traktowane jako wycofane w ostatnim dniu poprzedniego miesiąca. Środki trwałe, które zostaną wycofane w drugiej połowie miesiąca (dni od 16 do końca miesiąca), na potrzeby amortyzacji są traktowane jako wycofane w ostatnim dniu miesiąca, w którym nastąpiło wycofanie. |
| Miesiąc środkowy (15. dzień miesiąca) |  W celu obliczenia odpisu amortyzacyjnego za rok, w którym środek wprowadzono do eksploatacji, należy pomnożyć amortyzację całoroczną przez odpowiedni ułamek. Licznik (górna liczba) ułamka jest liczbą pełnych miesięcy w roku, gdy składnik majątku znajdował się w eksploatacji, powiększoną o 1/2 (0,5). Dzielnik (dolna liczba) wynosi 12. Jeśli zlikwidujesz składnik majątku przed końcem okresu amortyzacji, użyj tej samej metody do obliczenia odpisu amortyzacyjnego za rok likwidacji.   |
| Pół roku (początek roku) | Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w pierwszej połowie roku, zaczynają się amortyzować w pierwszym dniu roku (cały rok). Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w drugiej połowie roku, zaczynają się amortyzować w połowie roku.|
|   Pół roku (następny rok)   |   Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w pierwszej połowie roku, zaczynają się amortyzować w pierwszym dniu roku (cały rok). Środki trwałe, które mają datę <strong>Rozpoczęcie eksploatacji</strong> w drugiej połowie roku, zaczynają się amortyzować w pierwszym dniu następnego roku. Środki trwałe, które zostaną wycofane w pierwszej połowie roku, na potrzeby amortyzacji są traktowane jako wycofane w ostatnim dniu poprzedniego roku. Każda amortyzacja zaksięgowana w bieżącym roku musi zostać wycofana (skorygowana). Środki trwałe, które zostaną wycofane w drugiej połowie roku, na potrzeby amortyzacji są traktowane jako wycofane w ostatnim dniu roku, w którym nastąpiło wycofanie.|

