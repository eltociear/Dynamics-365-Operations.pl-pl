---
title: Dokumenty składnika majątku
description: W tym temacie objaśniono dokumenty w module Zarządzanie składnikami majątku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783505"
---
# <a name="asset-documents"></a>Dokumenty składnika majątku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

W tym temacie objaśniono dokumenty w module Zarządzanie składnikami majątku.

W module Zarządzanie składnikami majątku można skonfigurować dokumenty w taki sposób, aby były one automatycznie powiązane na przykład z typami zadań, producentami składników majątku, typami składników majątku lub składnikami majątku. Ta funkcja jest przydatna, kiedy zwalniane są zaktualizowane wersje dokumentów. W takim przypadku wystarczy umieścić zaktualizowany dokument w standardowej lokalizacji, której używasz dla dokumentów Microsoft Dynamics 365 for Finance and Operations, i dołączyć dokument do utworzonego rekordu dokumentu składnika majątku. Do zaktualizowanego dokument można następnie uzyskać dostęp z menu **Wszystkie składniki majątku**, **Aktywne składniki majątku**, **Moje aktywne składniki majątku**, **Wszystkie zlecenia pracy** oraz **Aktywne zadania zleceń pracy**. Proces dołączania dokumentów do rekordu dokumentu zasobów używa standardowego systemu obsługi dokumentów w programie Finance and Operations.

**Przykład 1:** dokument, który jest powiązany z typem zadania może opisywać procedurę dla tego typu zadania.

**Przykład 2:** dokument powiązany z kombinacją typu składnika majątku, producenta i modelu może być standardowym podręcznikiem dla wybranego modelu producenta składnika majątku.

## <a name="create-asset-document-relation"></a>Tworzenie relacji dokumentu składnika majątku

1. Wybierz kolejno **Zarządzanie składnikami majątku** \> **Ustawienia** \> **Dokumenty składnika majątku**.
2. Wybierz **Nowy**, aby utworzyć rekord dokumentu składnika majątku.
3. W zależności od tego, jak szczegółowa ma być relacja dokumentu, dokonaj odpowiednich selekcji w jednym lub kilku z następujących pól: **Typ składnika majątku**, **Producent**, **Model**, **Składnik majątku**, **Kategoria typy zadania**, **Typ zadania**, **Wariant typu zadania** oraz **Kryterium doboru** Opcje, które są dostępne w polach **Wariant typu zadania** i **Kryterium doboru** zależą od opcji wybranych w polu **Typ zadania**.

    > [!NOTE]
    > Gdy system wyszukuje dokumenty, które powinny być powiązane ze składnikami majątku lub zleceniem pracy, moduł Zarządzanie składnikami majątku przechodzi przez wszystkie rekordy dokumentu składnika majątku w celu sprawdzenia możliwego dopasowania. W pierwszej kolejności sprawdza zawsze kombinację najbardziej szczegółową. Innymi słowy, moduł Zarządzanie składnikami majątku najpierw sprawdza dopasowanie dla pola **Kryterium doboru**. Jeśli nie znaleziono dopasowania, sprawdza dopasowanie dla pola **Wariant typu zadania**. Jeśli nie znaleziono dopasowania, sprawdza dopasowanie dla pola **Typ zadania** itd. Jak widać w układzie strony **Dokumenty składnika majątku** to zachowanie oznacza, że aby znaleźć najbardziej konkretną kombinację, moduł Zarządzanie składnikami majątku sprawdza każdy rekord od prawej do lewej pod kątem dopasowania. Kilka dokumentów może być związanych ze składnikiem majątku lub zleceniem pracy. Zależnie od potrzeb można edytować poziom usługi na żądaniu konserwacji lub zleceniu pracy.

4. Wybierz **Załączniki**. W programie Finance and Operations zostanie wyświetlona strona **Obsługa dokumentów**.
5. Skonfiguruj dokumenty lub notatki, które powinny być dołączone do rekordu dokumentu składnika majątku. Po dołączeniu dokumentów w polu **Załączniki** pokazuje się liczba dokumentów powiązanych z rekordem.