---
title: "Płatności dodatnie — omówienie"
description: "Ten artykuł zawiera informacje o aparacie płatności dodatnich. Umożliwia on generowania elektronicznej listy czeków, które można okazywać bankowi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c5a9f3f2a5c456b4ec515b912bb7470b549684a5
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="positive-pay-overview"></a>Płatności dodatnie — omówienie

[!include[banner](../includes/banner.md)]


Ten artykuł zawiera informacje o aparacie płatności dodatnich. Umożliwia on generowania elektronicznej listy czeków, które można okazywać bankowi. 

Płatności dodatnie służą do generowania elektronicznej listy czeków, które można okazywać bankowi. Pliki płatności dodatnich ułatwiają bankom zapobieganie oszustwom związanym z czekami. Administrator konfiguruje płatności dodatnie w celu generowania elektronicznej listy czeków za każdym razem, gdy czeki są drukowane. Następnie gdy czek jest przedstawiany bankowi, bank porównuje go z wcześniej wysłaną listą czeków. Jeśli czek pasuje do czeku na liście, wówczas bank rozlicza czek. Jeśli czek nie pasuje do czeku na liście, bank wstrzymuje czek w celu sprawdzenia.

Płatność dodatnia jest też nazywana SafePay. 

Pliki płatności dodatnich mogą zawierać poufne informacje na temat odbiorców płatności i kwot czeków. W związku z tym musisz podjąć odpowiednie środki bezpieczeństwa od momentu wygenerowania plików aż do ich odbioru przez bank. Pliki płatności dodatnich są pobierane zgodnie z instrukcjami pobierania odpowiednimi dla przeglądarki internetowej. 

Pliki płatności dodatnich tworzy się za pomocą jednostek danych. Aby można było wygenerować pliku płatności dodatnich, należy skonfigurować formaty przekształceń kodu XML, które dokonują translacji danych do formatu czytelnego dla banku. 

Dla każdego konta bankowego, dla którego chcesz wygenerować informacje o płatnościach dodatnich, należy przypisać format płatności dodatnich. Po wygenerowaniu płatności można wygenerować plik płatności dodatnich dla pojedynczej firmy i pojedynczego konta bankowego. Alternatywnie można generować pliki płatności dodatnich dla wielu firm i kont bankowych równocześnie. 

Po zapłaceniu czeków wymienionych w pliku płatności dodatnich, otrzymasz numer potwierdzenia z banku. Następnie można potwierdzić plik płatności dodatnich w programie Microsoft Dynamics 365 for Operations. 

Jeśli trzeba zmodyfikować plik płatności dodatnich, można go wycofać. Wtedy dla każdego czeku w pliku płatności dodatnich jest resetowane pole wskazujące, czy czek jest uwzględniony w pliku płatności dodatnich.

Aby uzyskać więcej informacji, zobacz [Konfigurowanie i generowanie plików płatności dodatnich](set-up-generate-positive-pay-files.md).



