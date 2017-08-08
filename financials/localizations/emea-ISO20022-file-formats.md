---
title: "Importowanie plików ISO20022"
description: "W tym temacie wyjaśniono, jak importować pliki płatności w formatach ISO 20022 camt.054 i pain.002 do programu Microsoft Dynamics 365 for Finance and Operations Enterprise Edition."
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: pl-pl
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>Importowanie plików ISO20022

## <a name="overview"></a>Przegląd
Można importować pliki płatności mające następujące formaty:

 - **Zawiadomienie kredytowe ISO20022 camt.054** — importowanie płatności przychodzących z pliku w tym formacie do arkusza płatności odbiorców.
 - **Informacja zwrotna o stanie ISO20022 pain.002** i **zawiadomienie debetowe ISO20022 camt.054** — importowanie plików zwrotnych w tych formatach do arkusza przelewów w module Rozrachunki z dostawcami.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Wymagania wstępne dotyczące importowania pliku zawiadomienia kredytowego camt.054
Należy wykonać poniższe wymagania wstępne, aby importować komunikaty powiadomień bankowych w formacie camt.054.001.002 do arkusza płatności odbiorców.

1. Zaimportuj konfigurację **ISO20022 camt.054** modułu Raportowanie elektroniczne (ER) z usługi Microsoft Dynamics Lifecycle Services (LCS). Następnie na stronie **Metoda płatności odbiorcy** w polu **Konfiguracja formatu importu** zaznacz tę konfigurację. Aby uzyskać więcej informacji, zobacz [Formaty plików metod płatności](emea-select-file-formats-for-the-method-of-payments.md).
2. Na stronie **Wszyscy odbiorcy** wprowadź nazwę i numer organizacji dla każdego odbiorcy.
3. Na stronie **Konto bankowe odbiorcy** skonfiguruj rekord konta bankowego odbiorcy przez wprowadzenie następujących informacji: numer IBAN lub numer konta bankowego oraz kod SWIFT lub kod banku.
4. Na stronie **Konta bankowe** skonfiguruj konta bankowe firmy przez wprowadzenie następujących informacji: numer IBAN lub numer konta bankowego, kod SWIFT lub kod banku, waluta i adres.

    > [!NOTE]
    > Jeśli zamierzasz używać funkcji Zaawansowane uzgadnianie konta bankowego, na skróconej karcie **Uzgodnienie** w opcji **Zaawansowane uzgadnianie konta bankowego** ustaw wartość **Tak**. Jeśli zamierzasz uzgadniać niezaksięgowane importowane płatności, w opcji **Uznaj wyciągi bankowe jako potwierdzenia płatności elektronicznych** ustaw wartość **Tak**.

5. Opcjonalnie: Na stronie **Mapowanie kodu transakcji** skonfiguruj mapowanie między kodami transakcji bankowych w pliku a typami transakcji bankowych.
6. Jeżeli plik zawiera opłaty za transakcje, które chcesz zaksięgować razem z przychodzącą płatnością, otwórz opłatę od płatności na stronie **Opłata od płatności odbiorcy**. Następnie na stronie **Metody płatności** skojarz opłatę od płatności z kontem bankowym w ustawieniach opłat od płatności.
7. Jeśli będą importowane płatności ESR zawierające odniesienia do dokumentów płatności ISR (dotyczy firm w Szwajcarii), należy wykonać następującą konfigurację:

    - W polu **Płatności odbiorcy, długość konta** wprowadź długość kodu odbiorcy, który będzie używany w odniesieniach do dokumentu płatności ISR lub do automatycznej identyfikacji odbiorcy.
    - Upewnij się, że numer odbiorcy i numer faktury (numeracje) zawierają tylko cyfry. Nie może w nich być żadnych innych znaków. Numer faktury nie może zawierać zer na początku.
    - Wprowadź numery ESR i BESR oraz kod banku dla rachunku bankowego firmy. Aby uzyskać więcej informacji, zobacz [Starsza funkcja ESR](emea-che-esr-customer-payments-import.md), ponieważ są wymagane podobne ustawienia.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Importowanie pliku zawiadomienia kredytowego camt.054 do arkusza płatności odbiorców
1. Na stronie **Wiersze arkusza płatności odbiorców** kliknij kolejno opcje **Funkcje** > **Import płatności**.
2. Wybierz metodę płatności, która ma wymagane ustawienia formatu camt.054 ISO20022.
3. Określ wymagane parametry i ścieżkę pliku, a następnie kliknij przycisk **OK**.

Plik zostanie zaimportowany.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Warunki wstępne importowania plików informacji zwrotnej o stanie w formacie ISO20022 pain.002 i zawiadomienia debetowego w formacie ISO20022 camt.054 do arkusza przelewów w module Rozrachunki z dostawcami
Należy spełnić poniższe warunki wstępne, aby importować komunikaty bankowe w następujących formatach ISO20022 do strony **Przelew do dostawcy**: komunikaty zwrotne o stanie pain.002.001.003 i zawiadomienia debetowe camt.054.001.002.

1. Zaimportuj konfiguracje ER **ISO20022 camt.054** i **ISO20022 pain.002** z usługi LCS.
2. Na stronie **Metoda płatności dostawcy** w polach **Konfiguracja formatu zwrotnego** i **Pomocnicza konfiguracja formatu zwrotnego** zaznacz zaimportowane konfiguracje modułu ER. Trzeba będzie aktywować standardowy format elektroniczny informacji zwrotnych dla wybranej metody płatności.
3. Na stronie **Mapowanie stanu formatu zwrotnego** skonfiguruj mapowanie kodów stanu między stanami formatu pain.002 a stanami arkusza płatności dostawców.

    Oto przykład konfiguracji stanów.

    Stan zwrotu | Stan płatności
    --------------|---------------
    RJCT          | Odrzucona
    ACCP          | Zaakceptowany
    ACSP          | Odebrane

4. Na stronie **Kody błędów formatu zwrotnego** skonfiguruj kody błędów i opisy formatu pain.002 kody zgodnie z zewnętrznymi kodami przyczyn stanu w standardzie ISO20022.

    Poniżej przedstawiono przykład częściowej konfiguracji kodów błędów.

    Kod | Nazwisko
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Jeżeli plik camt.054 zawiera opłaty za transakcje, które chcesz zaksięgować razem z przychodzącą płatnością, otwórz opłatę od płatności na stronie **Opłata od płatności dostawcy**. Następnie na stronie **Metody płatności** skojarz opłatę od płatności z kontem bankowym w ustawieniach opłat od płatności.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Importowanie plików informacji zwrotnej o stanie pain.002 lub zawiadomienia debetowego camt.054 do arkusza płatności dostawców
1. Otwórz stronę **Przelewy** stronę w menu modułu Rozrachunki z dostawcami.
2. Na stronie **Przelewy** kliknij opcję **Plik zwrotny — Dostawca**.
3. Wybierz metodę płatności, która ma wymagane ustawienia plików formatu ISO20022, i kliknij przycisk **OK**.
4. Zaznacz format pliku, który chcesz zaimportować, a następnie kliknij przycisk **OK**.
5. Określ wymagane parametry i ścieżkę pliku, a następnie kliknij przycisk **OK**.

Jeśli importujesz plik pain.002, stan wierszy płatności do dostawców zostanie zaktualizowany zgodnie z informacjami w importowanym pliku.

W przypadku importowania pliku camt.054 należy określić następujące dodatkowe parametry:

- **Identyfikator opłaty** — wprowadź identyfikator opłaty, który będzie definiował nowe wiersze opłat od płatności tworzone w wierszu arkusza płatności dostawców w przypadku, gdy plik camt.054 zawiera kwotę opłaty.
- **Nazwa nowego arkusza** i **Opis nowego arkusza** — wprowadź nazwę i opis arkusza, do którego będą przenoszone przetworzone transakcje. Po przeniesieniu w nowym arkuszu powinny zostać przypisane nowe numery załączników.
- **Importuj transakcje poleceń zapłaty** — ustaw w tej opcji wartość **Tak**, jeśli wychodzące polecenia zapłaty muszą być importowane do arkusza płatności dostawców.
- **Nazwa arkusza** — podaj nazwę nowego arkusza na importowane transakcje polecenia zapłaty.
- **Rozlicz transakcje** — ustaw w tej opcji wartość **Tak**, jeśli importowane płatności do dostawców muszą być rozliczane względem faktur znajdujących się w systemie.

Zaimportowane informacje można przejrzeć na stronie **Przelewy**. 
