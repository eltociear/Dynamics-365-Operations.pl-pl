---
title: Lokalizacja wyjściowa produkcji
description: W tym temacie opisano hierarchię używaną do identyfikowania lokalizacji wyjściowej produkcji.
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9445db6d78d46831ed961977d6041459f118fee9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548890"
---
# <a name="production-output-location"></a>Lokalizacja wyjściowa produkcji

[!include [banner](../includes/banner.md)]

W tym temacie opisano hierarchię używaną do identyfikowania lokalizacji wyjściowej produkcji.

Lokalizacja wyjściowa produkcji to lokalizacja, w której najpierw umieszcza się wyrób gotowy bezpośrednio po ukończeniu produkcji. Zazwyczaj znajduje się blisko miejsca wytwarzania. Lokalizacja wyjściowa produkcji jest wykorzystywana jako pośredni magazyn materiału, zanim zostanie on przeniesiony do obszaru wysyłki, miejsca składowania, lokalizacji wejściowej produkcji następnego procesu produkcji, itd. 

Domyślną lokalizację wyjściową produkcji ustawia się podczas zgłaszania wyrobów gotowych względem zlecenia produkcyjnego lub szarży produkcyjnej. Do identyfikowania tej lokalizacji wyjściowej jest używana hierarchii przedstawiona poniżej:

1. Używanie lokalizacji wyjściowej zdefiniowanej w nagłówku zlecenia produkcyjnego lub szarży produkcyjnej.
2. Jeśli lokalizacja nie zostanie tam znaleziona — używanie lokalizacji wyjściowej zdefiniowanej w zasobie wykorzystywanym przez ostatnią operację zdefiniowaną w marszrucie produkcji.
3. Jeśli lokalizacja nie zostanie tam znaleziona — używanie lokalizacji wyjściowej zdefiniowanej w grupie zasobów wykorzystywanej przez zasób w ostatniej operacji zdefiniowanej w marszrucie produkcji.
4. Jeśli lokalizacja nie zostanie tam znaleziona — używanie lokalizacji wyjściowej zdefiniowanej w magazynie zdefiniowanym dla zlecenia produkcyjnego.

Domyślna lokalizacja wyjściowa produkcji jest ustawiana tylko dla produktów skonfigurowanych przy użyciu funkcjonalności zaawansowanych procesów magazynowych. Gdy towar tego typu jest zgłaszany jako gotowy, jest tworzona praca magazynowa typu **Ukończono odkładanie wyrobów** lub **Odłożenie produktu ubocznego i produktu towarzyszącego**. W tym typie pracy lokalizacja wyjściowa produkcji jest wykorzystywana jako lokalizacja pobrania. Lokalizacja odłożenia jest określana przez dyrektywy lokalizacji.
