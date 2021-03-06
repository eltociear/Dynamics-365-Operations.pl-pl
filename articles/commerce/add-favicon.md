---
title: Dodawanie ikony favicon
description: W tym temacie opisano sposób dodawania ikony favicon do witryny.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001551"
---
# <a name="add-a-favicon"></a>Dodawanie ikony favicon


[!include [banner](includes/banner.md)]

W tym temacie opisano sposób dodawania ikony favicon do witryny.

## <a name="overview"></a>Omówienie

Favicon jest małym plikiem graficznym wyświetlanym na karcie przeglądarki sieci Web, na pasku adresu, w historii przeglądania oraz w zakładkach lub ulubionych i w innych miejscach. Zaleca się dodanie favicon do witryny, ponieważ reprezentuje ona i wzmacnia daną markę oraz pomaga odróżnić witrynę od innych odwiedzanych przez odbiorców witryn sieci Web.

Chociaż do witryny można dodać wiele favicons różnych rozmiarów i typów plików, w tym temacie przedstawiono sposób dodawania jednego favicon. Jednak ten sam proces i lokalizacja są używane do dodawania kolejnych favicons.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Przekaż favicon do kolekcji składników majątku w witrynie

Aby przekazać favicon do kolekcji składników majątku w witrynie wykonaj procedurę opisaną w następujących krokach:

1. Przejdź do **Składniki majątku \> Przekaż \> Przekaż składniki majątku**.
1. Znajdź i wybierz favicon w lokalnym systemie plików.
1. Wprowadź tytuł, a następnie kliknij przycisk **OK**. 
1. W okienku właściwości po prawej stronie Skopiuj publiczny adres URL favicon.

> [!NOTE]
> Jeśli nie zaznaczysz opcji **Publikuj zasoby po przekazaniu**, musisz wrócić do strony **Składniki majątku** i ręcznie opublikować favicon później.

## <a name="create-the-html-for-the-favicon"></a>Utwórz kod HTML dla favicon

Aby utworzyć kod HTML dla favicon, należy skorzystać z poniższego urywka kodu HTML. W przypadku atrybutu **href** zamień wartość **„Publiczny\_URL\_dla\_twojej\_favicon”** na publiczny adres URL, który został wcześniej skopiowany.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>Dodaj kod HTML favicon do elementu stron \<head\>.

Aby dodać favicon do witryny, należy użyć tej samej procedury, która służy do dodawania dowolnego typu kodu HTML lub skryptu do elementu **\<head\>** stron witryny.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Dodawanie logo](add-logo.md)

[Wybór motywu witryny](select-site-theme.md)

[Praca z plikami zastępowania CSS](css-override-files.md)

[Dodawanie wiadomości powitalnej](add-welcome-message.md)

[Dodawanie powiadomienia o prawach autorskich](add-copyright-notice.md)

[Dodawanie języków do witryny](add-languages-to-site.md)

[Dodawanie kodu skryptu do stron witryny w celu obsługi telemetrii](add-telemetry.md)

