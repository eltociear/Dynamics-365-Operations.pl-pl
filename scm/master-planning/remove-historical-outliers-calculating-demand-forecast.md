---
title: "Usuwanie wartości odstających z danych transakcji historycznych podczas obliczania prognozy popytu"
description: "W tym artykule opisano sposób wykluczania wartości odstających z historycznych danych, które są używane do obliczania prognozy popytu. Poprzez wykluczenie wartości odstających, można zwiększyć dokładność prognozy."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72735c9e3fb4291076f0b577f45384dec319b2a7
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Usuwanie wartości odstających z danych transakcji historycznych podczas obliczania prognozy popytu

[!include[banner](../includes/banner.md)]


W tym artykule opisano sposób wykluczania wartości odstających z historycznych danych, które są używane do obliczania prognozy popytu. Poprzez wykluczenie wartości odstających, można zwiększyć dokładność prognozy.

Można wykluczyć wartości odstające, aby zwiększyć dokładność prognozy. To zadanie jest opcjonalne. Poniżej znajduje się omówienie procesu:

1.  Kliknij kolejno opcje **Planowanie główne** &gt; **Ustawienia** &gt; **Prognozowanie popytu** &gt; **Usuwanie wartości odstających**, aby otworzyć stronę **Usuwanie wartości odstających**, na której przy użyciu zapytania można wybrać transakcje do wykluczenia.
2.  Wybierz firmę, do której odnosi się kwerenda, a następnie wprowadź nazwę i opis. W polu **Data kwerendy** zostanie automatycznie ustawiona bieżąca data.
3.  Wybierz pole wyboru **Aktywna**, aby wykluczyć transakcje znalezione w wyniku kwerendy z danych historycznych. To ustawienie zostanie wprowadzone dopiero po utworzeniu prognozy podstawowej.
4.  Na stronie **Kwerenda usuwania wartości odstających** istnieje możliwość dodawania, usuwania i wybierania kryteriów określających, które transakcje zostaną wykluczone podczas obliczania bazowej prognozy. Na przykład wybierz dany towar lub transakcję zamówienia, które chcesz wykluczyć.
5.  Kliknij opcję **Wyświetl transakcje**. Na stronie **Transakcje wartości odstających** wyświetlane są transakcje, które spełniają kryteria określone w kwerendzie i które mają być wykluczone z historycznych danych podczas obliczania prognozy popytu.

**Uwaga:** można także tworzyć kwerendy na podstawie istniejącej kwerendy. Wybierz kwerendę do skopiowania i kliknij przycisk **Duplikuj**. Pole **Data kwerendy** identyfikuje wersję. Można użyć kwerendy w istniejącej formie lub kliknąć opcję **Edytuj kwerendę** w celu zmodyfikowania kryteriów. Opcjonalnie można zmodyfikować nazwę i opis nowej kwerendy.

<a name="see-also"></a>Informacje dodatkowe
--------

[Wprowadzenie do prognozowania popytu](introduction-demand-forecasting.md)

[Monitorowanie dokładności prognozy](monitor-forecast-accuracy.md)



