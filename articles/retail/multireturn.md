---
title: Zwracanie towarów z wielu zamówień i faktur
description: W tym temacie opisano funkcje obsługi zwrotów z wielu zamówień i faktur w rozwiązaniu Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2019
ms.locfileid: "373075"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Zwracanie towarów z wielu zamówień i faktur

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

W Dynamics 365 for Finance and Operations (wersja 10.0) zwroty mogą być dokonywane dla wielu zamówień i faktur, natomiast w wersjach przed 10.0 zwrotów można było dokonywać tylko dla jednej faktury jednocześnie. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurowanie modułu Retail do obsługi zwrotów z wielu zamówień i faktur

1. Przejdź do **Parametry rozwiązania Retail \> Zamówienia odbiorcy**.
1. Włącz parametr **Włącz zawroty z wielu zamówień**. 

## <a name="process-returns"></a>Przetwarzanie zwrotów

Po włączeniu tego parametru i zsynchronizowaniu zmian ze sklepami kasjer w sklepie można wybrać wiele zamówień sprzedaży dla danego odbiorcy i dokonać ich zwrotu.

Gdy zamówienia są wybrane, zostanie wyświetlona lista wszystkich produktów podlegających zwrotowi z wszystkich faktur dla tych zamówień. Kasjer może następnie wybrać produkty do zwrotu. Dla wszystkich wybranych produktów zostanie utworzone jedno zamówienie zwrotu.