---
title: INT64VALUE, funkcja ER
description: Ten temat zawiera ogólne informacje o używaniu funkcji INT64VALUE w module Raportowanie elektroniczne (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042695"
---
# <a name="INT64VALUE">INT64VALUE, funkcja ER</a>

[!include [banner](../includes/banner.md)]

Funkcja `INT64VALUE` zwraca wartość *Int64*, która reprezentuje określony ciąg.

## <a name="syntax-1"></a>Składnia 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Składnia 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenty

`text`: *Ciąg*

Wartość tekstowa, która musi zostać przekonwertowana na liczbę typu *Int64*.

`number`: *Liczba rzeczywista* lub *Liczba całkowita*

Liczbowa wartość *rzeczywista* lub *całkowita*, która musi zostać przekonwertowana na liczbę typu *Int64*.

## <a name="return-values"></a>Wartości zwracane

*Int64*

Wynikowa wartość numeryczna.

## <a name="usage-notes"></a>Uwagi dotyczące użytkowania

Wszystkie miejsca dziesiętne są obcinane.

## <a name="example-1"></a>Przykład 1

Funkcja `INT64VALUE ("22565422744")` zwraca wartość *Int64* wynoszącą **22565422744**.

## <a name="example-2"></a>Przykład 2

Funkcja `INT64VALUE ( VALUE("22565422744.77"))` zwraca wartość *Int64* wynoszącą **22565422744**.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Funkcje konwersji typu](er-functions-category-type-conversion.md)
