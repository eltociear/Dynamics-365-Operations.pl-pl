---
title: Wyświetlanie historii przepływu pracy
description: W tym temacie opisano wyświetlenie stanu dokumentu przesłanego do systemu przepływu pracy w celu przetworzenia i zatwierdzenia.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189805"
---
# <a name="view-workflow-history"></a>Wyświetlanie historii przepływu pracy

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tym temacie opisano wyświetlenie stanu dokumentu przesłanego do systemu przepływu pracy w celu przetworzenia i zatwierdzenia. Dane wykorzystane do stworzenia tej procedury pochodzą z firmy demonstracyjnej USMF.

1. Otwórz **Okienko nawigacji > Moduły > Wspólne > Informacje > Przepływu pracy > Historia przepływu pracy**.
    - Ten formularz umożliwia wyświetlenie stanu dokumentu przesłanego do przepływu pracy w celu przetworzenia i zatwierdzenia.  
    - Opcja **Identyfikator wystąpienia** to kod identyfikacyjny wystąpienia przepływu pracy, w ramach którego jest przetwarzany lub został przetworzony dokument.  
    - Opcja **Stan** to stan dokumentu w przepływie pracy.  
    - Opcja **Identyfikator przepływu pracy** to kod identyfikacyjny przepływu pracy, w ramach którego jest przetwarzany lub został przetworzony dokument.  
    - Opcja **Dokument** to kod identyfikacyjny dokumentu.  
    - Opcja **Typ dokumentu** to typ dokumentu przesłanego do przetwarzania.  
    - Opcja **Przepływ pracy** to nazwa przepływu pracy, w ramach którego jest przetwarzany lub został przetworzony dokument.  
    - Opcja **Wersja** to numer wersji przepływu pracy, w ramach którego jest przetwarzany lub został przetworzony dokument.  
    - Opcja **Data i godzina utworzenia** to data i godzina przesłania dokumentu.  
    - Opcja **Upłynęło czasu** to ilość czasu, jaka upłynęła od przesłania dokumentu.  
    - Przycisk **Wznów** umożliwia wznowienie procesu przepływu pracy dla wybranego dokumentu.  
    - Przycisk **Wycofaj** umożliwia wycofywanie wybranego dokumentu, tak aby nie był przetwarzany.   
2. Na liście wybierz łącze w odpowiednim wierszu.
    - Upewnij się, że jest rozwinięta sekcja **Elementy pracy**. W tej sekcji można obejrzeć elementy pracy skojarzone z wybranym dokumentem. Na przykład może być konieczne wykonanie zadania lub zatwierdzenie dokumentu.  
    - Przycisk **Przypisz** ponownie powoduje otwarcie okna dialogowego, w którym można przepisać element pracy do innego użytkownika.  
    - Upewnij się, że jest rozwinięta sekcja **Szczegóły śledzenia**. W tej sekcji można obejrzeć historię przepływu pracy dla wybranego dokumentu.  

