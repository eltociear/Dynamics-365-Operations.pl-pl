---
title: CN_GBT_ADDITIONALDIMENSIONID, funkcja ER
description: Ten temat zawiera ogólne informacje o używaniu funkcji CN_GBT_ADDITIONALDIMENSIONID w module Raportowanie elektroniczne (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917035"
---
# <a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID, funkcja ER</a>

[!include [banner](../includes/banner.md)]

Funkcja `CN_GBT_ADDITIONALDIMENSIONID` zwraca wartość typu *Ciąg*, która reprezentuje identyfikator pojedynczego wymiaru finansowego pobrany z określonego ciągu. Określony ciąg przedstawia wszystkie wymiary jako rozdzielaną przecinkami listę identyfikatorów.

## <a name="syntax"></a>Składnia

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumenty

`text`: *Ciąg*

Wartość typu *Ciąg* przedstawiająca wszystkie wymiary jako rozdzielaną przecinkami listę identyfikatorów.

`number`: Liczba całkowita

Wartość typu *Liczba całkowita* określa numer kolejny żądanego wymiaru w określonym ciągu.

## <a name="return-values"></a>Wartości zwracane

*Ciąg*

Wynikowa wartość tekstowa.

## <a name="example"></a>Przykład

Funkcja `CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` zwraca wartość **"CC"**.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Inne funkcje (specyficzne dla domeny biznesowej)](er-functions-category-other.md)