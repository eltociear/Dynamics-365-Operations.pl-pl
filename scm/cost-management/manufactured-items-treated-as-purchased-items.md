---
title: "Konfigurowanie produktów, które mogą być produkowane lub zamawiane"
description: "Produkty można pozyskiwać na różne sposoby — mogą być produkowane (wytwarzane) lub zamawiane (kupowane). W tym artykule opisano niektóre typowe kwestie do rozważenia podczas konfigurowania dla produktów obsługi pozyskiwania z wielu źródeł."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4a2eb04a7cd788914aa461047e20b7b9cbad5e1
ms.contentlocale: pl-pl
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Konfigurowanie produktów, które mogą być produkowane lub zamawiane

[!include[banner](../includes/banner.md)]


Produkty można pozyskiwać na różne sposoby — mogą być produkowane (wytwarzane) lub zamawiane (kupowane). W tym artykule opisano niektóre typowe kwestie do rozważenia podczas konfigurowania dla produktów obsługi pozyskiwania z wielu źródeł. 

Model wielu źródeł jest zwykle używany do kupowania towarów, które są wytwarzane od czasu do czasu, lub gdy jakiś towar, który był głównie towarem wytwarzanym, zmienił się i teraz jest głównie towarem kupowanym. Towar jest początkowo określany jako towar wytwarzany w celu zdefiniowania informacji o BOM i marszrucie oraz umożliwienia tworzenia zleceń produkcyjnych dla tego towaru. Typ produkcji powinien być ustawiony na **BOM** (lub dla procesu wytwarzania na **Formuła** lub **Produkt towarzyszący**).

Jeśli używasz kosztu standardowego, rekord kosztu towaru można obliczyć dla towaru wytwarzanego. Jednak rekord kosztu towaru nie może pokrywać się z kosztem standardowym, który ma być stosowany dla celów zakupów. W takim przypadku koszt standardowy należy wprowadzić i aktywować dla rekordu kosztu towaru. Do obliczania kosztów należy wziąć pod uwagę specjalną listę BOM i marszrutę, odzwierciedlające kombinację dostaw produktu w okresie obrachunkowym, aby zminimalizować odchylenia w czasie. Ponadto towar wytwarzany w jednym oddziale może zostać przeniesiony do innego oddziału. W związku z tym koszt towaru musi być ręcznie wprowadzony i aktywowany dla oddziału, do którego jest przenoszony. Jeśli towar wytwarzany jest składnikiem produktu wyższego poziomu, koszt składnika powinien być traktowany jak koszt towaru kupowanego. Niniejsze wytyczne obowiązują niezależnie od tego, czy koszty składników zostały obliczone czy wprowadzone ręcznie. Innymi słowy, w przypadku obliczania BOM koszty towaru powinny być traktowane jako koszty składnika kupowanego, zamiast używać informacji dotyczących BOM i marszruty dla towaru w celu obliczenia kosztów. Aby zablokować takie obliczenia, wybierz flagę **Zatrzymanie rozłożenia** znajdującą się w grupie obliczania BOM przypisanej do towaru. Aby w przypadku obliczeń w procesie planowania głównego uniemożliwić rozłożenie kosztów towaru, ustaw horyzont rozłożenia na 0 (zero) dni w zapotrzebowaniu na towary lub w grupie zapotrzebowania. W obliczaniu planowania głównego towar będzie traktowany jako kupowany i nie zostaną przeprowadzone dodatkowe obliczenia dla informacji dotyczących BOM i marszruty towaru.





