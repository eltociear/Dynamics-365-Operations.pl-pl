---
title: Konfigurowanie wyświetlania starszych partii w magazynie na urządzeniu przenośnym
description: W tym temacie opisano sposób konfigurowania urządzenia przenośnego do wyświetlania listy lokalizacji z partiami starszymi niż partie w bieżącej lokalizacji w wierszu pracy.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569435"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Konfigurowanie wyświetlania starszych partii w magazynie na urządzeniu przenośnym

[!include [banner](../includes/banner.md)]

Ustawienie **Wyświetl starsze partie w magazynie** pozwala wyświetlić listę lokalizacji zawierających partie starsze niż partie w bieżącej lokalizacji w wierszu pracy. Wyświetlona lista lokalizacji zawiera informacje o starszych partiach w lokalizacji z datami ważności oraz fizycznie zapasy każdej partii. Można wybrać pobieranie z nowej lokalizacji albo kontynuować pobieranie z bieżącej lokalizacji. 
- Pobieranie z nowej lokalizacji — Po zaznaczeniu nowej lokalizacji, z której ma być wykonywane pobieranie, bieżący wiersz pracy zostanie zaktualizowany, tak aby używał nowej lokalizacji, a praca będzie kontynuowana w zwykły sposób, ale przy użyciu nowej lokalizacji. Aby nowa lokalizacja działała, musi mieć dostępną ilość wystarczającą dla całego wiersza pracy. Jeśli wymagana ilość nie jest dostępna, wiersz pracy nie zostanie zaktualizowany i pojawi się lista. 
- Kontynuowanie pobierania z bieżącej lokalizacji — W przypadku dalszego używania bieżącej lokalizacji wiersza pracy ilości dla wiersza pracy będą w dalszym ciągu pobierane z oryginalnej lokalizacji.

## <a name="where-it-applies"></a>Zastosowanie
Funkcjonalność wyświetlania starszych partii w magazynie jest konfigurowana w menu urządzenia przenośnego i wpływa na pobieranie towarów w partiach poniżej.

## <a name="set-up-display-older-batches-within-warehouse"></a>Konfigurowanie wyświetlania starszych partii w magazynie
Ustawienie **Wyświetl starsze partie w magazynie** jest dostępne w elementach menu urządzenia przenośnego, gdy w opcji **Pobierz z najstarszej partii** ustawiono wartość **Ostrzegaj**.

- W oknie **Zarządzanie magazynem** > **Ustawienia** > **Urządzenie przenośne** > **Elementy menu urządzenia przenośnego** w opcji **Użyj istniejącej pracy** ustaw wartość **Tak**, a następnie w polu **Pobierz z najstarszej partii** ustaw wartość **Ostrzegaj**. 

