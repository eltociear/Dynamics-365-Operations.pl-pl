---
title: Moduł baneru promocyjnego
description: W tym temacie opisano moduł baneru promocyjnego i sposób ich dodawania do stron witryny w Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025627"
---
# <a name="promo-banner-module"></a>Moduł baneru promocyjnego


[!include [banner](includes/banner.md)]

W tym temacie opisano moduł baneru promocyjnego i sposób ich dodawania do stron witryny w Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Omówienie

Moduły baneru promocyjnego służą do wyświetlania wbudowanych komunikatów informacyjnych na stronie. Można ich używać do wyświetlania promocji na poziomie całej witryny wyświetlanych na wszystkich stronach witryny e-Commerce. 

Moduły baneru promocyjnego obsługują wiadomość SMS i łącze. Jeśli do modułu baneru promocyjnego jest dodawanych wiele wiadomości, staje się on wiodącym banerem karuzeli, który pozwoli klientom przechodzić między wszystkimi wiadomościami. 

Moduły baneru promocyjnego są sterowane danymi z systemu zarządzania zawartością (CMS) i mogą być umieszczane na dowolnej stronie.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Przykłady użycia banerów promocyjnych w e-Commerce

W nagłówku witryny można używać banerów promocyjnych do wyświetlania promocji lub komunikatów w całej witrynie, tak jak w poniższych przykładach.

„Roczna wyprzedaż kończy się za 10 dni”

„Zaoszczędź na zakupach do szkoły. Kup teraz.”

## <a name="promo-banner-module-properties"></a>Właściwości modułu baneru promocyjnego

| Nazwa właściwości             | Value                              | Opis |
|---------------------------|------------------------------------|-------------|
| Wiadomości transparentu           | Tekst i łącza                     | Szeroki wybór tekstu i łączy. |
| Autoodtwarzanie                  | **Prawda** lub **Fałsz**              | Wartość wskazująca, czy komunikaty są automatycznie przetwarzane, jeśli skonfigurowano wiele wiadomości. |
| Interwał przejścia slajdu | Liczba milisekund (ms)      | Interwał używany do cyklicznego przechodzenia między wiadomościami. |
| Zezwól na odrzucanie             | **Prawda** lub **Fałsz**              | Jeśli wartość jest ustawiona na **Prawda**, odbiorcy mogą anulować alert. |
| Pokazuj flipper karuzeli     | **Prawda** lub **Fałsz**              | Wartość wskazująca, czy mają być pokazywane flippery karuzeli, dzięki czemu odbiorcy mogą ręcznie przechodzić między różnymi elementami baneru. |
| Wyrównanie tekstu            | **Prawo**, **Lewo** lub **Środek** | Wyrównanie tekstu w module baner promocyjny. |
| Link                      | Adres URL                              | Adres URL opcjonalnego linku. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Dodawanie modułu baneru promocyjnego do nowej strony 

Aby dodać moduł baneru promocyjnego do nowej strony i ustawić wymagane właściwości, wykonaj następujące kroki.

1. Utwórz szablon strony o nazwie nazwa **Szablon baneru promocyjnego**.
1. W obszarze **Konspekt strony** dodaj moduł **Domyślna strona** do gniazda **Treść**. 
1. Zaewidencjonuj szablon i opublikuj go. 
1. Za pomocą utworzonego właśnie szblonu alertu utwórz stronę o nazwie **Strona baneru promocyjnego**. 
1. W **Głównym** gnieździe na nowej stronie dodaj moduł kontenera. 
1. W okienku po prawej stronie określ wartość **Szerokości** jako **Wypełnij kontener**.
1. W obszarze **Konspekt strony** dodaj moduł baneru promocyjnego do modułu kontenerów.
1. W ustawieniach modułu banery promocyjnego dodaj co najmniej jedną wiadomość baneru. Każda wiadomość może zawierać tekst razem z łączem. Inne właściwości można edytować, jeśli moduł ma być dostosowany dalej.
1. Zapisz i zobacz podgląd strony. W górnej części strony powinien pojawić się alert z dodanym tekstem.
1. Zakończ edytowanie strony i opublikuj go. 

> [!NOTE]
> Baner jest zazwyczaj używany w gnieździe nagłówka strony lub w gnieździe podnagłówków.


## <a name="additional-resources"></a>Dodatkowe zasoby

[Omówienie zestawu początkowego](starter-kit-overview.md)

[Moduł karuzeli](add-carousel.md)

[Moduł bloku zaawansowanej zawartości](add-content-rich-block.md)

[Moduł bloku zawartości](add-hero-module.md)

[Moduł odtwarzacza wideo](add-video-player.md)
