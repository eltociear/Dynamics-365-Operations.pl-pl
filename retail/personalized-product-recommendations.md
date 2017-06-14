---
title: "Podstawowe informacje o spersonalizowanych rekomendacjach produktów"
description: "W programie Dynamics 365 for Operations rekomendacje produktów mogą być wyświetlane na urządzenia w punkcie sprzedaży (POS). Rekomendacje to towary, którymi odbiorca może być zainteresowany w związku z wcześniej dokonywanymi zakupami, towary na liście życzeń odbiorcy oraz towary, które inni podobni odbiorcy kupowali w sklepach internetowych i tradycyjnych. U sprzedawców detalicznych z dużymi katalogami rekomendacje pomagają odbiorcom znajdować ciekawe inne produkty. Eksponując produkty ukierunkowane na zainteresowania i nawyki zakupowe odbiorców, rekomendacje produktów mogą pomóc sprzedawać powiązane i dodatkowe produkty oraz wzmacniać lojalność odbiorców. W programie Dynamics 365 for Operations funkcjonalność rekomendacji produktów bazuje na usługach Cognitive Services i aparacie uczenia maszynowego Microsoft Azure."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: edacd4cc9f9db59617bc579cb106e8e1017b8957
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="personalized-product-recommendations-overview"></a>Podstawowe informacje o spersonalizowanych rekomendacjach produktów

[!include[banner](includes/banner.md)]


W programie Dynamics 365 for Operations rekomendacje produktów mogą być wyświetlane na urządzenia w punkcie sprzedaży (POS). Rekomendacje to towary, którymi odbiorca może być zainteresowany w związku z wcześniej dokonywanymi zakupami, towary na liście życzeń odbiorcy oraz towary, które inni podobni odbiorcy kupowali w sklepach internetowych i tradycyjnych. U sprzedawców detalicznych z dużymi katalogami rekomendacje pomagają odbiorcom znajdować ciekawe inne produkty. Eksponując produkty ukierunkowane na zainteresowania i nawyki zakupowe odbiorców, rekomendacje produktów mogą pomóc sprzedawać powiązane i dodatkowe produkty oraz wzmacniać lojalność odbiorców. W programie Dynamics 365 for Operations funkcjonalność rekomendacji produktów bazuje na usługach Cognitive Services i aparacie uczenia maszynowego Microsoft Azure.

<a name="scenarios"></a>Scenariusze
---------

Rekomendacje produktów działają w opisanych niżej scenariuszach w punkcie sprzedaż. Są dostępne dla aplikacji Cloud POS i Modern POS (MPOS).

1.  Na stronie **Szczegóły produktu**:

-   Jeśli pracownik sklepu otworzy stronę **Szczegóły produktu** podczas oglądania wcześniejszych transakcji w różnych kanałach, aparat rekomendacji proponuje dodatkowe towary, które inni odbiorcy często kupowali razem z analizowanym produktem.
-   Jeśli pracownik sklepu doda odbiorcę do transakcji, a następnie otworzy stronę **Szczegóły produktu**, aparat rekomendacji przedstawi spersonalizowane zalecenia na podstawie historii transakcji odbiorcy.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Na stronie **Transakcja**:

-   Aparat rekomendacji proponuje towary na podstawie całej listy towarów w koszyku.
-   Jeśli pracownik sklepu doda odbiorcę do transakcji, aparat rekomendacji przedstawi spersonalizowane zalecenia na podstawie historii transakcji odbiorcy oraz listy towarów w koszyku.

**Uwaga**  Aby rekomendacje były wyświetlane na stronie **Transakcja**, sprzedawca detaliczny musi zaktualizować układ ekranu w programie Dynamics 365 for Operations. Formant **Zalecenia** należy upuścić na stronę **Transakcja**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Na stronie **Szczegóły odbiorcy**:
    -   Aparat rekomendacji proponuje towary na podstawie identyfikatora użytkownika oraz towarów na liście życzeń odbiorcy.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurowanie programu Dynamics 365 for Operations do wyświetlania rekomendacji w punkcie sprzedaży
Aby skonfigurować rekomendowanie produktów, należy wykonać poniższe czynności:

1.  Upewnij się, że wybrano poprawną wartość **Firmy**.
2.  Przejdź do okna **Magazyn jednostek**, wybierz opcję **Sprzedaż detaliczna**, a następnie kliknij przycisk **Odśwież**. ** **Spowoduje to użycie danych demonstracyjnych (lub faktycznych danych firmy) z operacyjnej bazy danych i przeniesienie ich do magazynu jednostek.
3.  Opcjonalnie: Aby wyświetlać rekomendacje na ekranie transakcji, przejdź do okna **Układ ekranu, **wybierz układ ekranu, uruchom narzędzie **Projektant układu ekranu**,** **a następnie upuść **formant rekomendacji** w żądanym miejscu.
4.  Przejdź do okna **Parametry sieci sprzedaży**, wybierz opcję **Uczenie maszynowe** i w ustawieniu **Włącz rekomendacje w punkcie sprzedaży** wybierz wartość **Tak**.
5.  Aby rekomendacje były wyświetlane w punkcie sprzedaży, uruchom zadanie konfiguracji globalnej **1110**. Aby pokazywać zmiany wprowadzone w projektancie układu ekranu punktu sprzedaży, uruchom zadanie konfiguracji kanału **1070**.

## <a name="how-does-it-work"></a>[]()Jak to działa?
Gdy odświeżasz jednostkę **Magazyn jednostek**, są wykonywane następujące czynności:

-   Dane w formacie wymaganym przez usługi Cognitive Services są wyodrębniane z operacyjnej bazy danych programu Dynamics 365 for Operations i wysyłane do magazynu jednostek.
-   Dane są wykorzystywane przez Fabrykę danych Azure (ADF) do czyszczenia danych przy użyciu skryptów gałęzi w ramach działań usługi ADF. Oczyszczoną dane są umieszczane w magazynie obiektów blob.
-   Dane z magazynu obiektów blob są używane przez interfejs API usług Cognitive Services do uczenia modelu rekomendacji.

Po włączeniu opcji **Włącz rekomendacje** i uruchomieniu zadań konfiguracji zostaną wykonane następujące czynności:

-   Poświadczenia i identyfikator modelu są pobierane z interfejsu API i umieszczane w operacyjnej bazie danych programu Dynamics 365 for Operations, w pliku web.config serwera AOS, a także na serwerze sieci sprzedaży.
-   Poświadczenia i identyfikator modelu są udostępniane środowisku CRT, co umożliwia obsługę wywołań o rekomendacje produktów z aplikacji Cloud POS i MPOS w trybie online.


<a name="see-also"></a>Informacje dodatkowe
--------

[Dodawanie formantu rekomendacji do strony transakcji na urządzeniu punktu sprzedaży](add-recommendations-control-pos-screen.md)



