---
title: Potwierdzenie partii i numeru identyfikacyjnego
description: W tym temacie opisano sposób konfigurowania i stosowania funkcjonalności potwierdzania partii i numeru identyfikacyjnego z urządzenia przenośnego.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563925"
---
# <a name="batch-and-license-plate-confirmation"></a>Potwierdzenie partii i numeru identyfikacyjnego

[!include [banner](../includes/banner.md)]

Funkcja potwierdzania partii umożliwia potwierdzenie, że na urządzeniu komórkowym jest wybierana poprawna partia. W początkowym pobraniu pracy tylko dla towarów w partii powyżej, gdzie określenie partia powyżej wskazuje, że zakres partii sięga wyżej niż lokalizacja w hierarchii wyszukiwania, należy sprawdzić, czy pobierana partia jest taka sama, jak partia w wierszu pracy. 

Funkcja potwierdzania numeru seryjnego umożliwia potwierdzenie, że na urządzeniu komórkowym jest wybierany poprawny numer identyfikacyjny. Podczas pobierania pracy z lokalizacji pośredniej należy sprawdzić, czy pobierany numer identyfikacyjny jest taki sam, jak numer identyfikacyjny skojarzony z pracą. Jeśli praca rozpoczyna się od zeskanowania numeru identyfikacyjnego, ten krok potwierdzania zostanie pominięty.

## <a name="where-it-applies"></a>Zastosowanie
Potwierdzanie stosuje się w następujących sytuacjach:

- Potwierdzanie partii stosuje się do pierwotnych pobrań pracy dla towarów w partiach powyżej.
- Potwierdzanie numeru identyfikacyjnego stosuje się do pobrań z lokalizacji pośrednich.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Konfigurowanie potwierdzanie partii i numeru identyfikacyjnego
Funkcjonalność potwierdzania partii i numeru identyfikacyjnego można skonfigurować z menu urządzenia komórkowego.  
1.  Na urządzeniu przenośnym w menu przejdź do pozycji Konfiguracja potwierdzenia pracy.  
2.  Wybierz opcję potwierdzania partii lub numeru identyfikacyjnego. Obie opcje są dostępne dla pobrań typów pracy, w których nie włączono opcji automatycznego potwierdzania.  
