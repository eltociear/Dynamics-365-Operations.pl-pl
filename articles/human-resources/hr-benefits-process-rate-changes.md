---
title: Przetwórz zmiany stawki
description: Przetwórz zmiany stawki świadczenia w Microsoft Dynamics 365 Human Resources, gdy nowy lub istniejący plan świadczeń ma zmianę w ustawieniach reguły uprawnienia.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010161"
---
# <a name="process-rate-changes"></a>Przetwórz zmiany stawki

[!include [banner](includes/preview-feature.md)]

Przetwórz zmiany stawki świadczenia w Microsoft Dynamics 365 Human Resources, gdy nowy lub istniejący plan świadczeń ma zmianę w ustawieniach reguły uprawnienia. Jeśli Nowa reguła uprawnienia zostanie utworzona i przypisana do planu, system wyświetli monit o ponowne przetworzenie pracownika, aby sprawdzić, czy pracownicy mogą obecnie kwalifikować się do planu na podstawie nowych opcji dotyczących uprawnień. 

1. W obszarze roboczym **Zarządzanie świadczeniami** w sekcji **Przetwarzanie** wybierz opcję **Przetwarzanie aktualizacji zmiany stawki**.

2. W oknie dialogowym **Uruchamianie procesu aktualizacji stawki świadczenia** określ wartości następujących pól:

   | Pole | Opis |
   | --- | --- |
   | Okres rejestracji | Okres rejestracji służący do przetworzenia zmian stawki. |

3. Jeśli chcesz uruchomić ten proces w tle, wybierz opcję **Uruchom w tle** i wykonaj następujące czynności:

   1. Umożliwia wprowadzanie informacji o przetwarzaniu.

   2. Aby skonfigurować zadanie cykliczne, wybierz opcję **cykl**, wprowadź informacje o cyklu i wybierz **OK**.

   3. Aby skonfigurować alert zadania, wybierz **alerty**, wybierz alerty do odebrania, a następnie kliknij przycisk **OK**.

   4. Kliknij przycisk **OK**. Proces będzie uruchamiany z parametrami określonymi przez użytkownika.

4. Kliknij przycisk **OK**.
