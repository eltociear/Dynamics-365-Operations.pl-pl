---
title: Tworzenie wstępnie zdefiniowanych wariantów produktu
description: Ta procedura prowadzi przez proces tworzenia wariantów produktu dla produktu głównego przy użyciu kombinacji wymiarów produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf1e41d0071a4c78d2a0f43548e44ae9d426580
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844784"
---
# <a name="create-predefined-product-variants"></a>Tworzenie wstępnie zdefiniowanych wariantów produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ta procedura prowadzi przez proces tworzenia wariantów produktu dla produktu głównego przy użyciu kombinacji wymiarów produktu. Do stworzenia tej procedury wykorzystano firmę demonstracyjną USMF.


## <a name="create-a-product-master"></a>Tworzenie produktu głównego
1. Wybierz kolejno opcje Zarządzanie informacjami o produktach > Produkty > Produkty główne.
2. Kliknij przycisk Nowy.
3. W polu Numer produktu wpisz wartość.
    * Ręczne wprowadzenie numeru produktu jest konieczne tylko wtedy, jeśli dla pola numeru produktu nie skonfigurowano sekwencji identyfikatorów. Innymi słowy pomiń ten krok, jeśli pole ma ustawioną sekwencję identyfikatorów.  
4. W polu Nazwa produktu wpisz wartość.
5. W polu Grupa wymiarów produktu wpisz lub wprowadź wartość.
    * Wybierz grupę wymiarów produkt SizeCol (rozmiar i kolor).  
6. Kliknij przycisk OK.

## <a name="add-product-dimensions"></a>Dodawanie wymiarów produktu
1. Kliknij opcję Wymiary produktu.
    * W tym przykładzie pokazano, jak ręcznie wprowadzić wymiary produktu. Można także wybrać grupę rozmiaru, koloru lub stylu zawierającą wartości wymiarów produktu, których chcesz używać.  
2. Kliknij przycisk Nowy.
3. Na liście oznacz wybrany wiersz.
4. W polu Rozmiar wprowadź lub wybierz wartość.
5. W polu Nazwa wpisz wartość.
6. Kliknij przycisk Nowy.
7. Na liście oznacz wybrany wiersz.
8. W polu Rozmiar wprowadź lub wybierz wartość.
9. W polu Nazwa wpisz wartość.
10. Kliknij kartę Kolory.
11. Kliknij przycisk Nowy.
12. Na liście oznacz wybrany wiersz.
13. W polu Kolor wprowadź lub wybierz wartość.
14. W polu Nazwa wpisz wartość.
15. Kliknij przycisk Nowy.
16. Na liście oznacz wybrany wiersz.
17. W polu Kolor wprowadź lub wybierz wartość.
18. W polu Nazwa wpisz wartość.
19. Kliknij przycisk Zapisz.
20. Zamknij stronę.

## <a name="generate-product-variants"></a>Generowanie wariantów produktu
1. Kliknij opcję Warianty produktu.
2. Kliknij opcję Sugestie dotyczące wariantów.
3. Kliknij opcję Zaznacz wszystko.
    * W tym przykładzie są zaznaczone wszystkie możliwe warianty. Jeśli do tworzenia wariantów będzie używany tylko podzbiór możliwych kombinacji wymiarów produktu, można wybrać poszczególne elementy.  
4. Kliknij przycisk Utwórz.
    * Opisy wszystkich wariantów można wygenerować na podstawie kombinacji wartości wymiarów produktu. Opisy są opcjonalne.  
5. Kliknij przycisk Zapisz.

