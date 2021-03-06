---
title: Łączenie z systemem Pomocy
description: W tym temacie opisano składniki systemu Pomocy dla aplikacji Finance and Operations i sposoby ich łączenia oraz podstawowe zasady tworzenia pomocy niestandardowej.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006179"
---
# <a name="connect-the-help-system"></a>Łączenie z systemem Pomocy

[!include [banner](../includes/banner.md)]

W tym temacie opisano składniki systemu pomocy dla aplikacji Finance and Operations, takie jak Dynamics 365 Finance, Supply Chain Management, Commerce, oraz Human Resources. Omówiono sposoby podłączania tych składników oraz podstawowe zasady tworzenia pomocy niestandardowej.

## <a name="help-architecture"></a>Architektura modułu Pomoc

Poniższa ilustracja pokazuje części Pomocy systemu. Wewnętrzny system Pomocy ściąga artykuły z witryny pod adresem https://docs.microsoft.com oraz przewodniki po zadaniach przechowywane w narzędziu do modelowania procesów biznesowych w usłudze Lifecycle Services (LCS).

> [!NOTE]
> Funkcje oznaczone w diagramie gwiazdką (\*) są planowane, ale jeszcze niedostępne.

[![Architektura modułu Pomoc](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Łączenie z systemem Pomocy

> [!NOTE]
> Karta **Przewodniki po zadaniach** jest obecnie niedostępna w programach Dynamics 365 Human Resources lub Commerce. Obecnie pracujemy nad włączeniem tej funkcjonalności w przyszłym wydaniu. Przewodniki po zadaniach w sekcji Rozpoczęcie pracy w module Human Resources pozostają dostępne i oferują podstawowe funkcje. Pomoc dotycząca procedur jest również dostępna w witrynie docs.microsoft.com w odniesieniu do Human Resources oraz Commerce.

Za pomocą strony **Parametry systemowe** administratorzy łączą elementy systemu Pomocy i je implementują.

[![Formularz Parametry systemu z ustawieniami Pomocy](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Na stronie **Parametry systemu** wykonaj następujące kroki:

> [!IMPORTANT]
> Podczas pierwszego otwierania karty **Pomoc** należy utworzyć połączenie z usługą Lifecycle Services. Kliknij łącze na środku formularza, poczekaj na nawiązanie połączenia, zamknij okno dialogowe i kliknij przycisk **OK**, co spowoduje przejście do formularza **Parametry systemu**.
>
> [![Nawiązywanie połączenia z usługą LCS](./media/connect-to-lcs-crop-1024x365.png "Nawiązywanie połączenia z usługą LCS")](./media/connect-to-lcs-crop.png)

1. Wybierz projekt Lifecycle Services, z którym chcesz się połączyć.
2. Wybierz biblioteki BPM (w ramach wybranego projektu), z których będą pobierane nagrania zadań.
3. Ustaw kolejność wyświetlania bibliotek BPM. Określa kolejność wyświetlania nagrań z bibliotek w okienku **pomocy**.

Po wykonaniu tych kroków można utworzyć okienko **Pomoc** i kliknąć kartę **Przewodniki zadań**. Zobaczysz przewodniki zadań mające zastosowanie do strony aktualnie wyświetlonej w programie Finance and Operations. Jeśli nie zostaną znalezione żadne przewodniki po zadaniach, możesz wprowadzić słowa kluczowe, aby doprecyzować wyszukiwanie.

### <a name="showing-translated-task-guides"></a>Wyświetlanie przetłumaczonych przewodników po zadaniach

Przetłumaczone przewodniki po zadaniach po raz pierwszy umieszczono w ujednoliconej bibliotece APQC w wydaniu z maja 2016 r. oraz w bibliotece ułatwiającej rozpoczęcie pracy. Aby wyświetlić przetłumaczone przewodniki po zadaniach w pomocy w aplikacji Finance and Operations, upewnij się, że masz połączenie z biblioteką z maja. Język wyświetlania przetłumaczonego przewodnika po zadaniu jest kontrolowany przez każdego użytkownika w ustawieniach języka w oknie **Opcje** &gt; **Preferencje**.

> [!NOTE]
> Mimo że przetłumaczono wiele przewodników po zadaniach, obecnie klient nie pokazuje nazw przetłumaczonych przewodników. Ponadto w majowej bibliotece są dostępne tłumaczenia tylko przewodników po zadaniach opublikowanych w lutym 2016 r. Opublikujemy zaktualizowaną bibliotekę z dodatkowymi tłumaczeniami.
>
> - Jeśli przewodnik po zadaniu został przetłumaczony, po otwarciu przewodnika jego cały tekst będzie wyświetlany w wybranym języku.
> - Jeśli przewodnik po zadaniu nie został jeszcze przetłumaczony, po otwarciu przewodnika tylko część tekstu (formanty) będzie wyświetlana w wybranym języku.

## <a name="creating-custom-help"></a>Tworzenie pomocy niestandardowej

Można przewodników po zadaniach do tworzenia pomocy niestandardowej lub połączenia witryny sieci Web z okienkiem pomocy.

### <a name="create-custom-help-with-task-guides"></a>Tworzenie Pomocy niestandardowej przy użyciu przewodników po zadaniach

W Finance, Supply Chain Management i aplikacji Commercezadanie można utworzyć pomoc niestandardową poprzez utworzenie nagrań zadań odpowiadających konkretnemu wdrożeniu i zapisanie ich w bibliotece procesów biznesowych LCS. Nie można tworzyć niestandardowych przewodników po zadaniach dla modułu Human Resources.

W przypadku partnerów: jeśli zostanie podniesiony poziom biblioteki do firmowej i zostanie ona uwzględniona w rozwiązaniu, będzie dostępna dla klientów. Można również utworzyć kopię ujednoliconej globalnej biblioteki APQC, a następnie otworzyć tę kopię, otwierać z niej nagrania zadań, modyfikować je i zapisywać nagrania z wprowadzonymi zmianami. Więcej informacji można znaleźć w see [Zasoby Rejestratora zadań](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Łączenie z niestandardową witryną

Firma Microsoft oferuje wytyczne i przykładowy kod opisujące tworzenie oraz łączenie witryny Pomocy niestandardowej do okienka Pomocy. Aby uzyskać więcej informacji, zobacz:

- [Utwórz Pomoc niestandardową dla aplikacji Finance and Operations (oficjalny dokument)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Repozytorium GitHub Pomocy niestandardowej](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Dodatkowe zasoby

[System Pomocy](help-overview.md)

[Zasoby rejestratora zadań](../../dev-itpro/user-interface/task-recorder.md)

[Tworzenie dokumentacji lub szkolenia za pomocą Rejestratora zadań](../../dev-itpro/user-interface/task-recorder-training-docs.md)
