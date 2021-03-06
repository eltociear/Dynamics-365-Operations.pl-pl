---
title: Konfigurowanie kategorii konta głównego
description: W tym temacie wyjaśniono sposób konfigurowania kategorii konta głównego w Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e2ba1d900f5d87a76fa93bf53f2970320e7d84c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186010"
---
# <a name="set-up-main-account-categories"></a>Konfigurowanie kategorii konta głównego

[!include [task guide banner](../../includes/task-guide-banner.md)]

W tym temacie wyjaśniono sposób konfigurowania kategorii konta głównego. Kategorie kont głównych są używane dla domyślnych raportów w sprawozdawczości finansowej i programie Power BI. Kategoriom kont głównych, które są tworzone domyślnie, można zmienić nazwy, ale nie można ich usunąć. Można tworzyć dodatkowe kategorie kont i używać ich na potrzeby raportowania i analizy. Ten temat wykorzystuje firmę demonstracyjną „USMF”.

## <a name="create-a-main-account-category"></a>Tworzenie kategorii konta głównego
1. W okienku nawigacji wybierz kolejno **Moduły > Księga główna > Plan kont > Konta > Kategorie kont głównych**.
2. Wybierz pozycję **Nowy**.
3. W polu **Kategoria konta głównego** wprowadź unikatową nazwę.
4. W **polu Opis** wprowadź opis kategorii kont głównych.
5. W polu **Typ konta głównego** zaznacz typ konta głównego, który zostanie powiązany z kategorią.

## <a name="link-main-accounts-to-account-category"></a>Łączenie kont głównych z kategorią konta
1. Kliknij opcję **Połącz konta główne**.
2. Z listy wybierz konta główne, które mają zostać przypisane do kategorii konta głównego, zaznaczając odpowiednie pola w **Połączonej** kolumnie. Przypisanie kont głównych do kategorii konta głównego spowoduje agregację sald kont, gdy ta kategoria jest używana do sprawozdawczości finansowej i analizy.  
3. Zaznacz lub wyczyść pole wyboru **Połączone**, aby wybrać konta główne.
4. Kliknij przycisk **OK**.
5. Wybierz opcję **Tak**.
