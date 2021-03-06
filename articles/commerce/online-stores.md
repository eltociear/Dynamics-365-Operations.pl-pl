---
title: Konfigurowanie kanału sklepu internetowego
description: Ten artykuł zawiera informacje o kanałach internetowych sklepów oraz o ich konfigurowaniu w Dynamics 365 Commerce.
author: kfend
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c427b0eba2120123a47f52029d70896be88b9ec0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023738"
---
# <a name="set-up-an-online-store-channel"></a>Konfigurowanie kanału sklepu internetowego

[!include [banner](includes/banner.md)]

Ten artykuł zawiera informacje o kanałach internetowych sklepów oraz o ich konfigurowaniu w Dynamics 365 Commerce.

Commerce obsługuje wiele kanałów sprzedaży detalicznej. Te kanały sprzedaży obejmują sklepy internetowe, internetowe serwisy sprzedażowe i sklepy sieci sprzedaży (nazywane także sklepami tradycyjnymi). Sklepy internetowe zapewniają sprzedawcy detalicznemu obecność w trybie online. Dzięki temu klienci sklepu mogą robić zakupy u sprzedawcy zarówno w internecie, jak i sklepie tradycyjnym. Klienci, którzy zakupią produkty ze sklepu internetowego mogą otrzymać produkty pocztą lub odebrać je z magazynu lokalnego. 

Tworzenie sklepu internetowego na kliencie usługi Commerce. Taki sklep internetowy jest następnie publikowany w zewnętrznym sklepie online zintegrowanym z usługą Commerce. Zewnętrzny sklep internetowy służy jako witryna (interfejs użytkownika) dla sklepu internetowego i pozwala wybrać system obsługi klienta (CMS) i opcje interfejsu użytkownika. Dostępnych jest kilka integracji tego typu. 

Właściwości zdefiniowane przez Ciebie dla sklepu internetowego sterują działaniem sklepu internetowego. Na przykład można zdefiniować hierarchię kategorii nawigacji i przypisać ją do sklepu internetowego. Po opublikowaniu sklepu internetowego w zewnętrznym sklepie online, hierarchia kategorii nawigacji zostanie wyświetlona w wersji online sklepu. Kupujący używają hierarchii kategorii nawigacji do przeglądania sklepu internetowego i wyszukiwania produktów. 

Aby utworzyć sklep internetowy, należy skonfigurować składniki umożliwiające transakcje, które mają być przetwarzane dla sklepu. Należy na przykład dodać asortymenty, zastosować atrybuty i ustawić metody płatności i wysyłki. Można również zdefiniować ceny, promocje, rabaty, umowy handlowe i warunki dostawy, które są właściwe dla sklepu internetowego. 

Po opublikowaniu sklepu internetowego w zewnętrznym sklepie internetowym można tworzyć katalogi produktów sprzedaży dla sklepu online. Produkty z katalogu stają się listami produktów w sklepie internetowym. Gdy kupujący nabywa produkty ze sklepu internetowego, dostępne zapasy są aktualizowane i synchronizowane w kliencie. Ponadto zamówienia sprzedaży są generowane dla zakupów i wysyłane do klienta w celu realizacji zamówienia i przetwarzania.

## <a name="set-up-an-online-store"></a>Konfigurowanie sklepu internetowego

Aby skonfigurować sklep online , należy wykonać następujące zadania:

1. Utwórz sklep internetowy.
2. Dodaj sklep internetowy do odpowiednich hierarchii organizacyjnych.
3. Dodaj asortyment, który zawiera produkty dostępne w sklepie internetowym.
4. Przypisz lub utwórz grupy cenowe dla sklepu internetowego.
5. Ustaw tryby dostawy, które są dostępne w sklepie internetowym.
6. Przypisz metody płatności zaakceptowane dla sklepu internetowego.
7. Jeśli zezwalasz kupującym zamówić produkty w trybie online i pobrać je w lokalnym sklepie, przypisz grupy lokalizatora sklepów do tego sklepu internetowego.
8. Przypisz atrybuty dla kanałów, produktów i zamówień sprzedaży do sklepu internetowego. Atrybuty kanału mają zastosowanie do całego sklepu internetowego, atrybuty produktu stosowane są do produktów oferowanych w sklepie internetowym, a atrybuty zamówienia sprzedaży do zamówień sprzedaży generowanych ze sklepu internetowego.
9. Mapuj atrybuty do ustawiania właściwości, które określają zachowanie atrybutów w sklepie internetowym. Na przykład można ustawić atrybuty tak, aby były wymagane lub wyszukiwane.
10. Opublikuj sklep internetowy, aby wygenerować wybraną strukturę zewnętrznego sklepu internetowego.

    > [!IMPORTANT]
    > Aby można było opublikować sklep internetowy, należy ustawić jego lokalizację dystrybucji.

## <a name="commerce-channel-navigation-hierarchies"></a>Hierarchie nawigacji kanału komercyjnego

Aby można było utworzyć sklep internetowy, należy określić hierarchię nawigacji kanału komercyjnego, którą chce się dla niego zastosować. Hierarchia nawigacji kanału reprezentuje hierarchię kategorii, która jest wyświetlana w sklepie internetowym po opublikowaniu sklepu. Podczas publikowania katalogów produktów sieci sprzedaży w sklepie online, produkty w katalogu są mapowane do kategorii w hierarchii nawigacji kanału. Kupujący następnie używają tej hierarchii do nawigacji w sklepie internetowym.

## <a name="organization-hierarchies"></a>Hierarchie organizacyjne

Hierarchie organizacyjne są używane do strukturyzacji kanałów komercyjnych i reprezentacji relacji między organizacjami tworzącymi firmę. Podczas konfigurowania sklepów internetowych, można je dodawać do hierarchii organizacyjnej. Sklepy następnie udostępniają dane, które są używane do asortymentów, uzupełnienia i raportów. 

Podczas tworzenia hierarchii organizacyjnej, należy przypisać do niej cel. Cel wskazuje sposób użycia hierarchii w strukturze biznesowej. Można utworzyć jedną hierarchię organizacji dla operacji sklepu i używać tej hierarchii dla asortymentów, uzupełnienia i raportowania. 

Można również utworzyć oddzielną hierarchię organizacji dla każdego celu. Można także tworzyć wiele hierarchii, które mają ten sam cel i przypisać do każdej z nich oddzielny kanał. Jeśli katalogi produktów mają zostać opublikowane w sklepie internetowym, należy co najmniej dodać sklep internetowy do hierarchii organizacyjnej dla asortymentów. Produkty w katalogu wybierane są z asortymentów przypisanych do sklepu internetowego. Podczas publikowania katalogu proces publikowania porównuje daty wejścia w życie asortymentu przypisanego do sklepu internetowego z produktami, które znajdują się w katalogu, w celu określenia produktów, które mają być dostępne w sklepie internetowym.
