---
title: Tworzenie witryny handlu elektronicznego
description: W tym temacie opisano kroki i informacje wymagane do utworzenia nowej witryny e-Commerce w konstruktorze witryn Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002020"
---
# <a name="create-an-e-commerce-site"></a>Tworzenie witryny handlu elektronicznego


[!include [banner](includes/banner.md)]

W tym temacie opisano kroki i informacje wymagane do utworzenia nowej witryny e-Commerce w konstruktorze witryn Dynamics 365 Commerce.

Przed rozpoczęciem opracowywania witryny e-Commerce, najpierw należy utworzyć nową witrynę w kreatorze witryn. 


Aby rozpocząć opracowywanie witryny e-Commerce, najpierw należy utworzyć nową witrynę w środowisku tworzenia witryn. Aby można było utworzyć nową witrynę, w Commerce musi być utworzony co najmniej jeden sklep internetowy. 


## <a name="set-up-your-site"></a>Konfigurowanie witryny

Aby skonfigurować witrynę, wykonaj następujące czynności.

1. Otwórz środowisko budowania witryn. Łącze do kreatora witryn w usłudze Microsoft Lifecycle Services (LCS) można znaleźć na stronie Funkcje środowiska w Commerce.
1. Następnie na stronie głównej dla środowiska tworzenia witryn wybierz opcję **Nowa witryna**.
1. W oknie dialogowym **Nowa witryna** wprowadź następujące informacje.

| Pole                               | Opis |
|-------------------------------------|-------------|
| Nazwa witryny                           | Umożliwia wprowadzenie nazwy wyświetlanej, która powinna być używana w odniesieniu do danej witryny w środowisku tworzenia witryn. Ta nazwa jest widoczna tylko w środowisku autorskim i nie będzie wyświetlana klientom. |
| Grupa zabezpieczeń administratora witryny | Określ grupę zabezpieczeń Microsoft Azure Active Directory (Azure AD), która zarządza użytkownikami dysponującymi rolą administratora witryny w tej witrynie. |
| Kanał domyślny (numer jednostki operacyjnej) | Wybierz sklep internetowy, który będzie pełnić tę witrynę jako sklep sieci Web. Jeśli chcesz, aby witryna e-Commerce obsługiwała wiele sklepów internetowych, musisz skojarzyć te sklepy z serwisem w **Ustawieniach witryny** po skonfigurowaniu witryny. |
| Język domyślny                            | Umożliwia określenie domyślnego języka dla tego sklepu i rynku online. Sklep internetowy może obsługiwać wiele języków. Jeśli chcesz obsługiwać wiele języków dla tego sklepu internetowego lub innego sklepu internetowego, możesz skonfigurować tę obsługę w **Ustawieniach witryny** po skonfigurowaniu witryny.  |
| Domena                              | Wybierz nazwę domeny, która będzie służyć jako domena dla tego sklepu internetowego. Jeśli nie skonfigurowano żadnych domen w usłudze LCS, to pole można pozostawić puste. Po skonfigurowaniu domeny w usługi LCS, należy ją dodać do swojego sklepu internetowego w **Ustawieniach witryny**.  |
| Ścieżka                              | Jeśli witryna obsługuje więcej niż jeden język dla danej nazwy domeny, użyj pola ścieżki, aby utworzyć unikalny adres URL witryny dla tej kombinacji domeny i języka. Jeśli język określony w polu **Język domyślny** jest jedynym językiem, który będzie obsługiwany dla tej domeny, lub będzie używany domyślny język po zlokalizowaniu witryny w dodatkowych językach, zaleca się pozostawienie tego pola pustego. |


Po utworzeniu witryny można sprawdzić, czy jest skojarzona ze swoim sklepem internetowym, wybierając kartę **Produkty**. Powinien być widoczny asortyment produktów, które zostały przypisane do sklepu internetowego. Możesz także użyć menu rozwijanego w lewym górnym rogu strony, aby uzyskać dostęp do przydzielonych produktów według kategorii.

## <a name="additional-resources"></a>Dodatkowe zasoby

[Konfigurowanie nazwy domeny](configure-your-domain-name.md)

[Wdrażanie nowej witryny handlu elektronicznego](deploy-ecommerce-site.md)

[Kojarzenie witryny online z kanałem](associate-site-online-store.md)

[Zarządzanie plikami robots.txt](manage-robots-txt-files.md)

[Konfigurowanie stron niestandardowych do logowań użytkowników](custom-pages-user-logins.md)

[Dodawanie obsługi dla sieci dostarczania zawartości (CDN)](add-cdn-support.md)

[Włączanie wykrywania sklepu na podstawie lokalizacji](enable-store-detection.md)
