---
title: TEXT, funkcja ER
description: Ten temat zawiera ogólne informacje o używaniu funkcji TEXT w module Raportowanie elektroniczne (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915563"
---
# <a name="TEXT">TEXT, funkcja ER</a>

[!include [banner](../includes/banner.md)]

Funkcja `TEXT` zwraca określoną liczbę jako wartość typu *Ciąg* po przekształceniu na ciąg tekstowy, który jest sformatowany zgodnie z ustawieniami regionalnymi serwera bieżącego wystąpienia aplikacji.

## <a name="syntax"></a>Składnia

```
TEXT (number)
```

## <a name="arguments"></a>Argumenty

`number`: *Liczba całkowita* lub *Liczba rzeczywista*

Wartość numeryczna, która musi zostać przekonwertowana na ciąg tekstowy.

## <a name="return-values"></a>Wartości zwracane

*Ciąg*

Wynikowa wartość tekstowa.

## <a name="usage-notes"></a>Uwagi dotyczące użytkowania

Dla wartości typu *Liczba rzeczywista* konwersja ciągu jest ograniczona do dwóch miejsc dziesiętnych.

## <a name="example"></a>Przykład

Jeśli ustawienia regionalne serwera wystąpienia aplikacji Microsoft Dynamics 365 Finance są określone jako **EN-US**, funkcja `TEXT (NOW ())` zwraca datę bieżącej sesji aplikacji, 17 grudnia 2015 roku, jako ciąg tekstowy **"12/17/2015 07:59:23 AM"**. Funkcja `TEXT (1/3)` zwraca wartość **"0.33"**.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Funkcje tekstowe](er-functions-category-text.md)