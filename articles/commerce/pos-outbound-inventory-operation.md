---
title: Wychodząca operacja magazynowa w punkcie sprzedaży
description: W tym temacie opisano możliwości wychodzących operacji magazynowych w punkcie sprzedaży (POS).
author: hhaines
manager: annbe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c3e50d20162340c599fb6719ae6f45654dba990a
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071888"
---
# <a name="outbound-inventory-operation-in-pos"></a>Wychodząca operacja magazynowa w punkcie sprzedaży

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

W systemie Microsoft Dynamics 365 Commerce w wersji 10.0.10 lub późniejszych operacje przychodzące i wychodzące w punkcie sprzedaży (POS) zastępują operację pobrania i przyjęcia.

> [!NOTE]
> W wersji 10.0.10 lub nowszej każda nowa funkcja w punkcie sprzedaży, która jest związana z odbieraniem zapasów sklepu z zamówieniami zakupu i zamówieniami przeniesienia, zostanie dodana do operacji przychodzących. Jeśli obecnie jest używana operacja pobrania i przyjęcia w punkcie sprzedaży, zaleca się opracowanie strategii przenoszenia z tej operacji do nowych operacji przychodzących i wychodzących. Mimo że operacja pobrania i przyjęcia nie zostanie usunięta z produktu, nie będzie już można w niej zainwestować, z perspektywy funkcjonalnej lub wydajności po wersji 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Wymaganie wstępne: Skonfiguruj strukturę dokumentów asynchronicznych

Operacja wychodząca obejmuje udoskonalenia wydajności zapewniające, że użytkownicy, którzy mają wysokie ilości księgowania przyjęć w wielu sklepach lub firmach, oraz duże dokumenty dot. zapasów, mogą przetwarzać te dokumenty w module Centrali Commerce bez kłopotów z limitami czasu oraz bez błędów. Te udoskonalenia wymagają użycia struktury dokumentów asynchronicznych.

Gdy jest używana struktura dokumentów asynchronicznych, można przekazać zmiany dokumentów wychodzących z puktu sprzedaży do Centrali Commerce, a następnie przenieść je do innych zadań, gdy przetwarzanie w Centrali Commerce odbywa się w tle. Stan dokumentu można sprawdzić na stronie listy dokumentów **Operacji wychodzących** w punkcie sprzedaży, aby upewnić się, że Księgowanie zakończyło się pomyślnie. W aplikacji punktu sprzedaży można również skorzystać z listy dokumentów aktywnej dla operacji wychodzącej, aby wyświetlić dokumenty, których nie można było zaksięgować w Centrali Commerce. Jeśli dokument nie powiedzie się, użytkownicy punktu sprzedaży będą mogli wprowadzać poprawki, a następnie ponownie próbować przetworzyć go w Centrali Commerce.

> [!IMPORTANT]
> Należy skonfigurować strukturę dokumentów asynchronicznych, zanim firma podejmie próbę użycia operacji wychodzącej w punkcie sprzedaży.

Aby skonfigurować strukturę dokumentów asynchronicznych, należy wykonać następujące procedury:

### <a name="create-and-configure-a-number-sequence"></a>Utwórz i skonfiguruj sekwencję numerów

1. Wybierz kolejno opcje **Administrowanie organizacją \> Numery kolejne \> Numery kolejne**.
2. Na stronie **Numery kolejne** utwórz dwie nowe sekwencje numerów.
3. W polach **Kod sekwencji numerów** i **nazwa** wprowadź wartości zdefiniowane przez użytkownika.
4. Na skróconej karcie **Referencje** wybierz pozycję **Dodaj**.
5. W polu **Obszar** wybierz **Parametry rozwiązania Commerce**.
6. W polu **referencje** wybierz **Identyfikator operacji dokumentu sieci sprzedaży**.
7. Na skróconej karcie **Ogólne** w sekcji **Konfiguracja** ustaw opcję **Ciągłe** na wartość **Nie**, aby upewnić się, że nie występują żadne problemy z wydajnością.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Utwórz i Zaplanuj dwa zadania wsadowe dla zadań przetwarzania dokumentów i monitorowania

Tworzone zadania wsadowe będą używane do przetwarzania dokumentów, które nie powiodą się lub przekroczą limit czasu. Będą one również używane, gdy liczba aktywnych dokumentów magazynowych, które są przetwarzane z punktu sprzedaży, przekracza wartość skonfigurowaną przez system.

1. Wybierz kolejno opcje **Administrowanie systemem \> Zapytania \> Zadania wsadowe**.
2. Na stronie **Zadanie wsadowe** utwórz dwa zadania wsadowe:

    - Skonfiguruj jedno zadanie do uruchamiania klasy **RetailDocumentOperationMonitorBatch**.
    - Skonfiguruj inne zadanie do uruchamiania klasy **RetailDocumentOperationProcessingBatch**.

3. Umożliwia zaplanowanie nowych zadań wsadowych, które będą uruchamiane cyklicznie. Na przykład można skonfigurować harmonogram, tak aby zadania były uruchamiane co pięć minut.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Wymaganie wstępne: Dodaj operację wychodzącą do układu ekranu punktu sprzedaży

Zanim organizacja będzie mogła skorzystać z funkcji operacji wychodzących, musi skonfigurować **operację wychodzącą** w punkcie sprzedaży w jednym lub kilku [układach ekranu punktu sprzedaży](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Przed wdrożeniem nowej operacji w środowisku produkcyjnym należy upewnić się, że została ona gruntownie przetestowana i przeszkolić użytkowników do jej używania.

## <a name="overview"></a>Omówienie

Użytkownicy punktu sprzedaży dotyczącego operacji wchodzących wykonują następujące zadania:

- Księgowanie wysyłek dla dokumentów zamówień przeniesienia, w przypadku których sklep użytkownika jest wyznaczonym magazynem wychodzącym.
- Wyświetlanie informacji o historycznych wysyłkach zamówień przeniesienia, które zostały zaksięgowane przez sklep.
- Tworzenie nowego żądania wchodzącego zamówienia przeniesienia.

Po rozpoczęciu operacji wchodzącej z poziomu aplikacji punktu sprzedaży wyświetlany jest widok strony listy. Ten widok pokazuje otwarte dokumenty zlecenia przeniesienia, które mają wiersze zapasów, które bieżący sklep użytkownika ma wysłać i zrealizować. Aby znaleźć i wybrać dokument, użytkownicy mogą przewijać listę lub skorzystać z funkcji wyszukiwania.

Lista dokumentów zapasów wchodzących zawiera trzy karty.

- **Aktywna** — na tej karcie są wyświetlane zamówienia przeniesienia ze stanem **Wnioskowane** lub **Częściowo wysłane** Zamówienia zawierają wiersze lub ilości w wierszach, które muszą zostać wysłane przez bieżący sklep użytkownika. Na tej karcie wyświetlane są również zamówienia, które mają stan **Przetwarzanie w centrali** (czyli oczekiwanie na potwierdzenie pomyślnego księgowania z Centali Commerce) lub **Przetwarzanie nie powiodło się** (to znaczy, że księgowanie w Centrali Commerce nie powiodło się, a użytkownik musi poprawić dane i ponowić próbę przesłania zamówień).
- **Wersja robocza** — na tej karcie są wyświetlane nowe żądania wychodzącego zamówienia przeniesienia, które utworzono w sklepie użytkownika. Jednak dokumenty zostały zapisane lokalnie. Nie zostały one jeszcze przesłane do Centrali Commerce w celu przetworzenia.
- **Zakończone** — na tej karcie jest wyświetlana lista dokumentów przeniesienia zakupu, które sklep w pełni wysłał w ciągu ostatnich siedmiu dni. Ta karta jest używana wyłącznie w celach informacyjnych. Wszystkie informacje o dokumentach są tylko do odczytu dla sklepu.

W przypadku wyświetlania dokumentów na dowolnej z tych kart pole **Stan** może pomóc w zrozumieniu etapu, w którym znajduje się dokument.

- **Wersja robocza** — dokument zamówienia przeniesienia został zapisany lokalnie tylko w bazie danych kanału sklepu. Żadne informacje dotyczące wniosku o zamówienie przeniesienia nie zostały jeszcze przesłane do Centrali Commerce.
- **Wnioskowane** — zamówienie zakupu lub zamówienie przeniesienia zostało utworzone w module Centrali Commerce i jest w pełni otwarte. Bieżący sklep użytkownika jeszcze przetworzył wszelkie wysyłki w odniesieniu do dokumentu.
- **Częściowo wysłano** — dokument zamówienia przeniesienia zawiera jedną lub więcej wierszy lub częściową, które zostały zaksięgowane jako wysłane przez magazyn wychodzący. Wiersze wysłane są dostępne do odebrania w ramach operacji przychodzącej.
- **W pełni wysłane** — zlecenie przesunięcia zawierało wszystkie wiersze i pełne ilości wierszy zaksięgowane jako wysłane przez magazyn wychodzący.
- **W toku** — ten stan jest używany do informowania użytkowników urządzenia, że dokument jest aktywnie opracowywany przez innego użytkownika.
- **Wstrzymana** — ten stan jest pokazywany po wybraniu opcji **Wstrzymaj przyjmowanie** w celu tymczasowego zatrzymania procesu przyjmowania.
- **Przetwarzanie w Centrali** — dokument został przesłany do Centrali Commerce z aplikacji punktu sprzedaży, ale nie został jeszcze zaksięgowany pomyślnie w Centrali Commerce. Dokument przechodzi przez proces asynchronicznego księgowania dokumentu. Po pomyślnym zaksięgowaniu dokumentu w module Commerce Headquarter jego stan powinien zostać zaktualizowany do **w pełni odebranego** lub **częściowo odebranego**.
- **Przetwarzanie nie powiodło się** — dokument został zaksięgowany w Centrali Commerce i odrzucony. W **Szczegółach** jest wyświetlana przyczyna niepowodzenia księgowania. Dokument musi być edytowany w celu usunięcia problemów z danymi, a następnie musi zostać ponownie przesłany do Centrali Commerce w celu przetworzenia.

Po wybraniu wiersza dokumentu z listy zostanie wyświetlone okienko **Szczegółów**. W tym okienku są wyświetlane dodatkowe informacje o dokumencie, takie jak informacje o wysyłce i dacie. Na pasku postępu widać, ile towarów trzeba będzie przetworzyć. Jeśli dokument nie został pomyślnie przetworzony w Centrali Commerce, w okienku **szczegółów** są wyświetlane także komunikaty o błędach związane z tym niepowodzeniem.

W widoku strony listy dokumentów możesz wybrać **Szczegóły zamówienia** na pasku aplikacji, aby wyświetlić szczegóły dokumentu. Można również uaktywnić przetwarzanie paragonów w uprawnionych wierszach dokumentu.

W widoku strony listy dokumentów można również utworzyć nowe zamówienia przeniesienia wchodzącego dla sklepu.

## <a name="transfer-order-shipping-process"></a>Proces wysyłania zamówienia przeniesienia

Po wybraniu dokumentu zamówienia przeniesienia na karcie **Aktywne** można wybrać **Szczegóły zamówienia**, aby rozpocząć proces wypełniania. Zostanie wyświetlony widok **Pełna lista zamówień**. Na tej stronie są wyświetlane wszystkie wiersze dokumentu zawierające dany towar. Zawiera także szczegóły zamówionej ilości.

Każde skanowanie kodu kreskowego aktualizuje ilość w polu **Wysyłane teraz** o jedną jednostkę. Można również wprowadzić ilość wysyłkową, wybierając **Wyślij produkt** dostarczany na pasku aplikacji, wprowadzić identyfikator towaru, a następnie wprowadzając ilość. Jeśli towar jest objęty kontrolą lokalizacji, można potwierdzić lub skonfigurować lokalizację wysyłki dla wiersza dokumentu.

W widoku **Pełna lista zamówień** można ręcznie wybrać wiersz z listy, a następnie zaktualizować ilość **Wysyłane teraz** dla wybranego wiersza w okienku **Szczegółów**.

### <a name="over-delivery-shipping-validations"></a>Sprawdzanie poprawności nadwyżki w wysyłce

Sprawdzanie poprawności nastąpiło podczas procesu odbierania dla wierszy dokumentu. Obejmują one sprawdzanie nadwyżki w dostawie. Jeśli użytkownik spróbuje uzyskać więcej zapasów niż zamówiono w zamówieniu zakupu, ale nadwyżka w dostawie nie jest skonfigurowana lub otrzymana ilość przekracza tolerancję nadwyżki w dostawie skonfigurowaną dla wiersza zamówienia zakupu, zostanie wyświetlony błąd i nie można przyjąć nadmiarowej ilości.

### <a name="shipping-location-controlled-items"></a>Towary kontrolowane w lokalizacji wysyłki

Jeśli wysyłane produkty są kontrolowane pod względem lokalizacji, użytkownicy mogą wybrać lokalizację, z której chcą wystawić zapasy podczas procesu wysyłki. Zaleca się skonfigurowanie domyślnej lokalizacji sprawy dla magazynu sklepu, aby ten proces był bardziej wydajny. Nawet w przypadku skonfigurowania lokalizacji domyślnej użytkownicy mogą zastępować lokalizację sprawy w wybranych wierszach w miarę ich obowiązywania.

Operacja uwzględnia konfigurację **Dozwolony pusty przychód** dla pozycji **lokalizacji** w wymiarze przechowywania i nie wymaga wprowadzenia wymiaru lokalizacji, jeśli jest skonfigurowany pusty przychód. Jeśli puste lokalizacje przychodu nie są dozwolone dla towaru, w aplikacji punktu sprzedaży jest wyświetlany komunikat o błędzie i wymagane jest wprowadzenie lokalizacji przed zaksięgowaniem przychodu.

### <a name="ship-all"></a>Wyślij wszystko

Jeśli jest to wymagane, można wybrać opcję **Wyślij wszystko** na pasku aplikacji, aby szybko zaktualizować ilość **Wysyłane teraz** dla wszystkich wierszy dokumentu do wartości maksymalnej, która jest dostępna do realizacji dla tych wierszy.

### <a name="cancel-fulfillment"></a>Anuluj realizację

Funkcji **Anulowanie realizacji** należy użyć na pasku aplikacji tylko wtedy, gdy chcesz wycofać się z dokumentu i nie chcesz zapisywać żadnych zmian. Na przykład początkowo zaznaczono niewłaściwy dokument i nie ma potrzeby zapisywania żadnego z poprzednich danych wysyłki.

### <a name="pause-fulfillment"></a>Wstrzymaj realizację

W przypadku realizacji zamówienia przeniesienia można użyć funkcji **Wstrzymaj realizację**, jeśli proces ma zostać podzielony od procesu. Na przykład można wykonać inną operację z punktu sprzedaży, na przykład dzwonienie do sprzedaży odbiorcy lub opóźnienie księgowania wysyłki do Centrali Commerce.

Po wybraniu opcji **Wstrzymaj realizację**stan dokumentu zostanie zmieniony na **Wstrzymany**. Dlatego użytkownick będzie wiedzieć, że wprowadzono dane do dokumentu, ale dokument nie został jeszcze zatwierdzony. Aby wznowić proces realizacji, wybierz wstrzymany dokument, a następnie wybierz **Szczegóły zamówienia**. Wszystkie **Wysyłane teraz** ilości odbieranych towarów są zachowywane i można je przeglądać z poziomu widoku **Pełna lista zamówień**.

### <a name="finish-fulfillment"></a>Zakończ realizację

Po zakończeniu wprowadzania wszystkich ilości **Wysyłane teraz** dla produktów należy wybrać opcję **Zakończ realizację** na pasku aplikacji.

Gdy jest używane przetwarzanie dokumentów asynchronicznych, paragon jest przesyłany za pośrednictwem struktury dokumentów asynchronicznych. Czas potrzebny na zaksięgowanie dokumentu jest zależny od rozmiaru dokumentu (liczby wierszy) i ogólnego ruchu przetwarzania występującego na serwerze. Zazwyczaj proces ten odbywa się w ciągu kilku sekund. Jeśli Księgowanie dokumentu nie powiedzie się, użytkownik zostanie powiadomiony za pośrednictwem listy dokumentów **Operacja wychodząca** na karcie **Aktywne**, gdzie stan dokumentu zostanie zaktualizowany jako **Proces nie powiódł się**. Użytkownik może następnie wybrać nieuszkodzony dokument w punkcie sprzedaży, aby wyświetlić komunikaty o błędach oraz przyczynę niepowodzenia w okienku **Szczegółów**. Uszkodzony dokument pozostaje niezaksięgowany i wymaga powrotu użytkownika do wierszy dokumentu przez wybranie **Szczegółów zamówienia** w punkcie sprzedaży. Użytkownik musi wówczas zaktualizować dokument, używając korekt, na podstawie błędów. Po poprawieniu dokumentu użytkownik może spróbować ponownie go przetworzyć, wybierając opcję **Zakończ realizację** na pasku aplikacji.

## <a name="create-an-outbound-transfer-order"></a>Utworzenie wychodzącego zamówienia przeniesienia

Z punktu sprzedaży użytkownicy mogą tworzyć nowe dokumenty zamówienia przeniesienia. Aby rozpocząć proces, należy wybrać opcję **Nowy** na pasku aplikacji, gdy znajdujesz się na liście głównych dokumentów **Operacji wychodzących**. Następnie zostanie wyświetlony monit o wybranie **Przeniesienia do** magazynu lub sklepu, do którego obecny sklep wyśle zapasy. Wartości są ograniczone do wyboru zdefiniowanego w konfiguracji grupy realizacji sklepu. W żądaniu przeniesienia wychodzącego bieżący sklep będzie zawsze **Przenoszony z** magazynu dla zamówienia przeniesienia. Tej wartości nie można zmienić.

W razie konieczności można wprowadzić wartości w polach **Data wysyłki**, **Data odebrania** i **Metoda dostawy**. Można również dodać notatkę, która będzie przechowywana razem z nagłówkiem zamówienia przeniesienia, jako załącznik do dokumentu w Centrali Commerce.

Po utworzeniu informacji nagłówka można dodać produkty do zamówienia przeniesienia. Aby rozpocząć proces dodawania towarów i żądanych ilości, zeskanuj kody kreskowe lub wybierz pozycję **Dodaj produkt**.

Po wprowadzeniu wierszy w zamówieniu przeniesienia wychodzącego należy wybrać opcję **Zapisz**, aby zapisać zmiany w dokumencie lokalnie lub **Przeslij żądanie**, aby przesłać szczegóły zamówienia do Centrali Commerce w celu dalszego przetwarzania. Jeśli zostanie wybrana **Zapisz**, dokument wersji roboczej zostanie zapisany w bazie danych kanału, a magazyn wychodzący nie będzie mógł uruchomić dokumentu, dopóki nie zostanie on pomyślnie przetworzony przez **Prześlij żądanie**. Opcję **Zapisz** należy wybrać tylko w przypadku, gdy nie można zatwierdzić żądania w celu przetworzenia w Centrali Commerce.

Jeśli dokument jest zapisany lokalnie, można go znaleźć na karcie **Wersje robocze** na liście dokumentów dla **Operacji przychodzących**. Gdy dokument jest w stanie **Wersji roboczej**, można go edytować, wybierając **Edytuj**. W razie konieczności można zaktualizować, dodać lub usunąć wiersze. Można również usunąć cały dokument, gdy jest on w stanie **Wersji roboczej**, zaznaczając opcję **Usuń** na karcie **Wersje robocze**.

Po pomyślnym przesłaniu wersji roboczej do modułu Commerce Headquarter zostanie ona wyświetlona na karcie **Aktywne** i stan zmieni się na **Wnioskowane**. W tym momencie tylko użytkownicy z magazynu wychodzącego mogą edytować dokument, wybierając **Operację wychodzącą** w aplikacji punktu sprzedaży. Użytkownicy w magazynie przychodzącym mogą wyświetlać zamówienie przeniesienia na karcie **Aktywne** na liście dokumentów **Operacja przychodząca**, ale nie mogą ich edytować ani usuwać. Blokada edycji zapewnia, że nie występują żadne konflikty, ponieważ przychodzący zleceniodawca zmienia zamówienie przeniesienia w tym samym czasie, gdy wychodzący spedytor będzie aktywnie pobierał i wysyłał zamówienie. Jeśli po przesłaniu zamówienia przeniesienia wymagane są zmiany z magazynu lub magazynu przychodzącego, należy skontaktować się z odbiorcą w sprawie wychodzącego spedytora i poprosić o wprowadzenie zmian.

Po zmiany stanu na **Wnioskowane** jest on gotowy do przetworzenia przez magazyn wychodzący. Ponieważ przesyłka jest przetwarzana przy użyciu operacji wychodzącej, status dokumentów zlecenia przeniesienia jest aktualizowany na z **Wnioskowany** do **Wysłane** lub **Częściowo wysłane**. Gdy dokumenty są w stanie **W pełni wysłane** lub **Częściowo wysłane**, magazyn lub magazyn przychodzący może zaksięgować przychody z nich przy użyciu procesu przyjęcia operacji przychodzącej.

W pełni wysłane zamówienia przeniesienia są przenoszone na kartę **Zakończone** na liście dokumentów **Operacji wychodzącej**. Są one widoczne dla użytkowników w magazynie lub sklepie wychodzącym, w trybie tylko do odczytu, przez siedem dni.

## <a name="related-topics"></a>Powiązane tematy

[Operacja zapasów przychodzących w punkcie sprzedaży](pos-inbound-inventory-operation.md)
