---
title: "Definiowanie zasad dotyczących wydatków"
description: "Można zdefiniować zasady dotyczące wydatków, których pracownicy muszą przestrzegać przy wprowadzaniu i wysyłaniu raportów z wydatków i wniosków wyjazdowych w rozwiązaniu Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: pl-pl
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a>Zasady dotyczące wydatków

[!include[banner](../includes/banner.md)]

Można zdefiniować zasady, których pracownicy muszą przestrzegać podczas wprowadzania i przesyłania raportów z wydatków i wniosków wyjazdowych. Wdrożenie zasad dotyczących wydatków może się przyczynić do efektywniejszego zarządzania wydatkami. 

Można na przykład określić zasadę dotyczącą wydatków na zakwaterowanie w Nowym Jorku, która stanowi, że wydatki nie mogą przekroczyć 250 zł za noc. Jeśli pracownik prześle raport z wydatków lub wniosek wyjazdowy, w którym ta kwota będzie przekroczona, system powiadomi pracownika, że została przekroczona kwota wydatków określona w zasadach. Podczas definiowania zasady można skonfigurować wiadomość, jaką otrzyma pracownik. 

Można zdefiniować trzy typy zasad: 

 - Ostrzeżenie — umożliwia pracownikowi przesłanie raportu z wydatków lub wniosku wyjazdowego, ale wydatek zostanie oznaczony dla wszystkich osób zatwierdzających i  
 do późniejszego raportowania. 
 - Błąd — wymaga, aby pracownik zmienił wydatek na zgodny z zasadami przed przesłaniem raportu z wydatków lub wniosku wyjazdowego. 
 - Uzasadnienie — wymaga, aby pracownik lub menedżer wprowadził uzasadnienie przekroczenia kwoty w zasadach przed przesłaniem raportu z wydatków lub wniosku wyjazdowego. 

Można również skonfigurować zakres dat, dla którego obowiązują zasady dotyczące wydatków. Na przykład bilety na loty między Warszawą a Kopenhagą mogą być drogie w sezonie turystycznym. Można określić regułę dotyczącą wydatków na bilety lotnicze, która ogranicza koszty przelotu do Kopenhagi do 500 zł, i można określić, że ta reguła obowiązuje między 15 marca a 15 września. 
