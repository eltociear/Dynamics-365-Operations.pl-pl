---
title: GETCURRENTCOMPANY, funkcja ER
description: Ten temat zawiera ogólne informacje o używaniu funkcji GETCURRENTCOMPANY w module Raportowanie elektroniczne (ER).
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041430"
---
# <a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY, funkcja ER</a>

[!include [banner](../includes/banner.md)]

Funkcja `GETCURRENTCOMPANY` zwraca wartość *Ciąg* reprezentującą kod firmy (jednostki prawnej), do której użytkownik jest aktualnie zalogowany.

## <a name="syntax"></a>Składnia

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Wartości zwracane

*Ciąg*

Wynikowa wartość tekstowa.

## <a name="example"></a>Przykład

Funkcja `GETCURRENTCOMPANY ()` zwraca wartość **USMF** dla użytkownika zalogowanego do firmy **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Inne funkcje (specyficzne dla domeny biznesowej)](er-functions-category-other.md)
