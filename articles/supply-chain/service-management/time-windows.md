---
title: Okna czasu
description: "Okna czasu umożliwiają optymalizowanie planowania wierszy zleceń serwisowych."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: b7268870aa9065e4e52d936e819107094bad3663
ms.contentlocale: pl-pl
ms.lasthandoff: 02/20/2018

---

# <a name="time-windows"></a>Okna czasu  

[!include[banner](../includes/banner.md)]

Okna czasu umożliwiają optymalizowanie planowania wierszy zleceń serwisowych. Istnieje możliwość takiego skonfigurowania systemu, aby automatycznie tworzył zlecenia serwisowe. Na podstawie kryteriów określonych przez okno czasu można połączyć jak największą liczbę wierszy zleceń serwisowych z jak najmniejszą liczbą zleceń serwisowych.

Okna czasu określają, jak daleko może zostać przesunięty wiersz zlecenia serwisowego względem obliczonej daty. Obliczona data określa, kiedy według harmonogramu ma zostać wykonany wiersz zlecenia serwisowego. Data bazuje na ustawieniu interwału i okresie serwisu podanym na stronie **Tworzenie zleceń serwisowych**. Okno czasu definiuje się za pomocą wartości z poniższej tabeli.

| Metoda | opis                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tydzień   | Dowolny otwarty dzień w tym samym tygodniu, w którym wypada początkowa obliczona data, do którego można przenieść wiersz zlecenia serwisowego.                                                                                                                                                                                    |
| Miesiąc  | Dowolny otwarty dzień w tym samym miesiącu, w którym wypada początkowa obliczona data, do którego można przenieść wiersz zlecenia serwisowego. Na przykład obliczoną datą wiersza zlecenia serwisowego jest 15 lutego 2017 r. Wiersz zlecenia serwisowego można zaplanować na dowolny dzień roboczy między 1 lutego a 28 lutego 2017 r. |
| Ręczny | Należy określić maksymalną liczbę dni przed początkową obliczoną datą i po niej, o jaką może zostać przesunięty wiersz zlecenia serwisowego.                                                                                                                                                                           |

Jeśli nie określisz okna czasu dla wiersza umowy serwisowej, wiersz zlecenia serwisowego wygenerowany na podstawie tej umowy serwisowej musi zostać wykonany dokładnie w dniu, na który został pierwotnie zaplanowany.

## <a name="related-topics"></a>Powiązane tematy

[Tworzenie okien czasowych](create-time-windows.md)

