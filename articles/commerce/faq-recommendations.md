---
title: Rekomendacje produktów — często zadawane pytania
description: Ten temat zawiera informacje o procesach i narzędziach, których można wykorzystywać do rozwiązywania problemów związanych z zaleceniami dotyczącymi produktów lub ich wynikami.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7951f92ef68a7a782f2874d7b73d7e45eba0afba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003034"
---
# <a name="product-recommendations-faq"></a>Rekomendacje produktów — często zadawane pytania


[!include [banner](includes/banner.md)]

Ten temat zawiera informacje o procesach i narzędziach, których można wykorzystywać do rozwiązywania problemów związanych z [rekomendacjami produktów](product-recommendations.md) lub ich wynikami.

## <a name="best-practices"></a>Najlepsze praktyki
Bardzo ważne jest wykorzystanie pojęcia produktów głównych i wariantów produktu. Rozsądne grupowanie wariantów dla nadrzędnego produktu głównego pomaga algorytmom list i usłudze w tworzeniu lepszych modeli. Ponadto usługa może obsługiwać tylko jedno wystąpienie produktu, a nie wszystkie ściśle powiązane warianty z listy. Jeśli wszystkie ściśle powiązane warianty są umieszczone na liście, mogą wystąpić błędne lub zduplikowane wyniki.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Dlaczego na moich listach rekomendacji nie ma produktów?

Zazwyczaj, jeśli brakuje pozycji z listy rekomendacji produktów, może to być błąd konfiguracji produktu. Na przykład może to być niepoprawna data rozpoczęcia lub zakończenia produktu, wymiar może być niepoprawnie skonfigurowany lub produkt może nie znajdować się w poprawnym asortymentzie kanału itp.

Jeśli brakuje pozycji z listy rekomendacji opartej na sztucznej analizie maszyn (AI-ML), pozycja może nie pasować do kryteriów listy rekomendacji lub może nie mieć wystarczającej liczby transakcji zakupu, aby wyświetlić listę rekomendacji.

Zalecane jest sprawdzenie następujących czynności:
1. **Upewnij się, że włączono rekomendacje dotyczące produktu w HQ.** Aby uzyskać informacje o włączaniu tej usłudze, zobacz [Włączanie rekomendacji produktów](enable-product-recommendations.md).
1. **Upewnij się, że są ustawione kluczowe właściwości produktu.** Na przykład asortymenty produktów muszą mieć wartość **Uwzględnij**.
1. **W przypadku nowych produktów w asortymentach może upłynąć nawet do 3 godzin, zanim produkt zostanie uruchomiony na nowej liście.**
1. **Jeśli produkt nadal nie jest wyświetlany na liście trendy, bestsellery, klientom podoba się również lub często kupowane razem, może to oznaczać, że ten produkt nie ma wystarczającej liczby transakcji.** W takim przypadku można poczekać na więcej transakcji, zaktualizować domyślne parametry listy rekomendacji lub skorzystać z ręcznej interwencji w celu zmodyfikowania wyników listy produktów rekomendacji. Aby uzyskać więcej informacji o parametrach rekomendacji, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).
1. **Upewnij się, że produkt spełnia kryteria rekomendacji dla listy.** Aby uzyskać więcej informacji o parametrach rekomendacji produktów, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Jak można zapobiec zwracaniu złych wyników rekomendacji?

Listy rekomendacji wymagają dużej ilości transakcji do wygenerowania wyników. Dlatego ważne jest, aby użytkownicy dostarczali pełne historyczne dane o transakcjach.

Ponadto produkty, które nie mają transakcji lub kilku transakcji zwykle nie mają **Klientom podoba się również** lub **często kupowane razem**, a nie pojawiają się na listach **Trendy** lub **Bestsellery**. Taka sytuacja może często występować w przypadku bardzo nowych produktów lub starych produktów, które mają małą liczbę zakupów. Popularne nowe elementy umożliwią łatwe pokonanie tego zagadnienia.

Zalecane jest wykonanie następujących czynności:
1. **Upewnij się, że produkt spełnia kryteria rekomendacji dla tej listy.** Aby uzyskać więcej informacji o parametrach rekomendacji produktów, zapoznaj się z tematem Modyfikuj wyniki rekomendacji produktów na podstawie plików AI-ML.
1. **Jeśli produkt jest nowy, rozważ zmodyfikowanie listy rekomendacji, dopóki produkt nie będzie już miał dalszych transakcji.** Aby uzyskać więcej informacji o modyfikacji wyników list rekomendacji produktów, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).


- **Upewnij się, że produkt spełnia kryteria rekomendacji dla tej listy.** Aby uzyskać więcej informacji o parametrach rekomendacji produktów, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).
- **Jeśli produkt jest nowy, rozważ zmodyfikowanie listy rekomendacji, dopóki produkt nie będzie już miał dalszych transakcji**. Aby uzyskać więcej informacji o modyfikacji wyników list rekomendacji produktów, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Czy można usunąć produkt, ale nadal jest on widoczny w sklepie?

Istnieje możliwość korygowania list algorithmically generowanych w razie potrzeby biznesowego. Jeśli jednak produkt zostanie usunięty z listy zaleceń, produkt pozostanie wykrywalny w sklepie. Aby uzyskać więcej informacji o modyfikacji wyników rekomendacji produktów, zapoznaj się z tematem [Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md).

Jeśli w sklepie ma być zablokowane wykrycie towaru, należy zmienić wartość **Asortymentów towarów** na **Wykluczenie**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Jak dodać listę do strony e-Commerce?

Aby uzyskać informacje dotyczące sposobu dodawania stron rekomendacji produktów do witryny e-Commerce, zapoznaj się z tematem [Dodawanie list rekomendacji produktów do stron](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Jak włączyć rekomendacje w punkcie sprzedaży?

Po włączeniu zaleceń dotyczących produktu należy dodać Panel rekomendacji do ekranu kontrolki punktu sprzedaży. Więcej informacji na temat sposobu dodawania panelu rekomendacji do układu urządzenia punktu sprzedaży można znaleźć w [dokumentacji tej funkcji](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen).

## <a name="additional-resources"></a>Dodatkowe zasoby

[Omówienie rekomendacji produktów](product-recommendations.md)

[Włączanie rekomendacji produktów](enable-product-recommendations.md)

[Zarządzanie wynikami rekomendacji produktów na podstawie plików AI-ML](modify-product-recommendation-results.md)
