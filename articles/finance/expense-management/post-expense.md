---
title: Księgowanie raportu z wydatków
description: W tym temacie opisano, jak zaksięgować raport z wydatków w księdze głównej.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179398"
---
# <a name="post-an-expense-report"></a>Księgowanie raportu z wydatków

[!include [banner](../includes/banner.md)]

Po zatwierdzeniu i przekazaniu do arkusza finansowego raport z wydatków można zaksięgować w księdze głównej. Podczas księgowania raportu z wydatków są identyfikowane wydatki, które kwalifikują się do zwrotu podatku od towarów i usług (VAT). Zadanie sprawdzenia poprawności i odzyskania zapłaconego podatku VAT jest przypisywane pracownikowi, który odpowiada za weryfikowanie raportu z wydatków.

Jeśli wydatki w raporcie z wydatków obciążają firmę inną niż firma zatrudniająca pracownika, należy zweryfikować obie firmy — wierzyciela i dłużnika. Na przykład pracownik, który przesłał raport z wydatków, pracuje dla firmy DAT, ale obciążył wydatkami firmę DIR. W takim przypadku firma DAT jest wierzycielem, a firma DIR dłużnikiem. Po zweryfikowaniu tych wierszy arkusza można księgować wiersze wydatku w księdze głównej.

Aby zaksięgować raport z wydatków, na stronie **Zatwierdzone raporty z wydatków** zaznacz raport z wydatków, a następnie w okienku akcji wybierz opcję **Księguj**.

Można też zaksięgować wszystkie raporty z wydatków figurujące na liście w tym samym czasie. Zaznacz wszystkie raporty z wydatków, a następnie wybierz opcję **Księguj**.
