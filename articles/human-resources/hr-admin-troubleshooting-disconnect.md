---
title: Klient aplikacji rozłącza się
description: W tym artykule wyjaśniono, co należy zrobić, jeśli klient zostaje odłączony od własnego środowiska i nie może ustalić, dlaczego.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010174"
---
# <a name="client-disconnects"></a>Klient aplikacji rozłącza się

**Szczegóły środowiska** 

Ten problem może występować we wszystkich środowiskach.
 
**Objaw** 

Odbiorca zostaje odłączony od własnego środowiska i nie może ustalić, dlaczego. Na komputerze odbiorcy jest wyświetlany jeden z następujących komunikatów o błędach:

- Twoje połączenie zostało utracone Kliknij przycisk Zamknij, aby kontynuować pracę.
- Prawdopodobnie doszło do utraty łączności sieciowej. Kliknij przycisk Ponów próbę, aby spróbować ponownie.

**Czerwona flaga**

Ten problem występuje często, gdy użytkownicy są w fazie implementacji, porównują informacje między środowiskami produkcyjnymi i testowymi i zapominają, że poruszają się między sesjami. Jeśli użytkownicy są na tym etapie, prawdopodobnie wystąpi ten problem.

**Wystawienie** 

**Typy przeglądarek:** Google Chrome, Internet Explorer oraz Microsoft Edge

Microsoft Dynamics 365 Human Resources rozłącza użytkowników, gdy są otwarte dwie różne sesje jednocześnie dla tego samego użytkownika i tego samego typu przeglądarki. (Na przykład użytkownik A wyświetla środowisko 1 i 2 środowiska w Chrome.) Nie ma znaczenia, czy użytkownik otworzy inne okna przeglądarki lub różne karty. Jeśli te same poświadczenia użytkownika są używane do logowania się zarówno w środowisku 1, jak i środowisku 2 w tym samym czasie w tym samym typie przeglądarki, moduł Human Resources rozłączy jedną z sesji.

**Rozwiązanie**

Upewnij się, że tylko jedno środowisko jest otwarte w danej chwili dla danego typu przeglądarki. Użytkownicy mogą otwierać wiele sesji w tym samym środowisku (to znaczy wiele kart w tej samej przeglądarce).

Użytkownicy, którzy chcą do przechodzić między dwiema środowiskami w tym samym czasie powinni otwierać każde środowisko w innym typie przeglądarki. (Na przykład użytkownik A może wyświetlić środowisko 1 w przeglądarce Chrome i środowisko 2 w Microsoft Edge).
