---
title: Zasada rezerwacji wymiarów na poziomie magazynu elastycznego
description: W tym temacie opisano zasady rezerwacji zapasów, które umożliwiają firmom sprzedaż produktów śledzonych partiami i uruchamianie ich zagadnień logistycznych w miarę operacji obsługujących WMS, rezerwując określone partie dla zamówień sprzedaży odbiorców, nawet jeśli hierarchia rezerwacji jest skojarzone z produktami nie zezwalają na rezerwację konkretnych partii.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cd6ec1013de757214db99ada02170bb6e2af96c0
ms.sourcegitcommit: f52ddcad105aac4ad2caef709751ff80caf363c0
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036936"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Zasada rezerwacji wymiarów na poziomie magazynu elastycznego

[!include [banner](../includes/banner.md)]

Jeśli hierarchia rezerwacji zapasów typu „Lokalizacja towaru\[poniżej\]” jest skojarzona z produktami, firmy, które sprzedają produkty śledzone partiami i uruchamiają ich logistykę jako operacje włączone dla systemu zarządzania Microsoft Dynamics 365 Warehouse Management System (WMS), nie mogą zarezerwować określonych partii tych produktów dla zamówień sprzedaży odbiorców. W tym temacie opisano zasady rezerwacji zapasów, które pozwalają tym firmom zarezerwować określone partie, nawet jeśli produkty są skojarzone z hierarchią rezerwacji "Lokalizacja towaru\[poniżej\].

## <a name="inventory-reservation-hierarchy"></a>Hierarchie rezerwacji zapasów

Ta sekcja podsumowuje istniejącą hierarchię rezerwacji zapasów. Koncentruje się na sposobie obsługi śledzonych i prześledzonych towarów w partii.

Hierarchia rezerwacji zapasów określa, że w zakresie, w jakim dotyczy to wymiarów przechowywania, zamówienie wymaga obowiązkowych wymiarów oddziału, magazynu i stanu zapasów, podczas gdy logika magazynu jest odpowiedzialna za przypisanie lokalizacji do wnioskowane ilości i rezerwowanie lokalizacji. Innymi słowy, w interakcjach między zamówieniem popytu a operacjami magazynowymi, oczekuje się, że zamówienie musi być wysłane z magazynu (czyli oddziału i magazynu). Następnie magazynpolega na logice, aby znaleźć wymaganą ilość miejsca w pomieszczeniu magazynowym.

Jednak w celu odzwierciedlenia modelu operacyjnego firmy, wymiary śledzenia (numery partii i numery seryjne) podlegają większej elastyczności. Hierarchia rezerwacji zapasów może uwzględniać scenariusze, w których obowiązują następujące warunki:

- Firma korzysta z operacji magazynowych w celu zarządzania pobieraniem ilości o numerach partii lub seryjnych po znalezieniu ilości w przestrzeni magazynowej. Ten model jest często określany mianem *lokalizacji towaru\[poniżej\]*. Jest zwykle używany w przypadku, gdy identyfikacja numeru partii produktu lub numeru seryjnego nie ma znaczenia dla odbiorców, którzy nakładają popyt na firmę sprzedającą.
- Jeśli numery partii lub numerów seryjnych są częścią specyfikacji zamówienia odbiorcy i są rejestrowane na zamówieniu popytu, operacje magazynowe, które wyszukują ilości w magazynie, są ograniczone przez określone żądane numery i nie mogą być zmieniane. Ten model jest często określany mianem *lokalizacji towaru\[powyżejj\]*.

W tych scenariuszach wyzwanie polega na tym, że tylko jedna hierarchia rezerwacji zapasów może być przypisana do każdego zwolnionego produktu. Dlatego w przypadku modułu WMS do obsługi śledzonych elementów, gdy przypisanie hierarchii określa, kiedy numer partii lub seryjny ma zostać zarezerwowany (gdy zamówienie jest wykonywane lub w trakcie pracy pobrania magazynowego), nie można zmienić tego chronometrażu na zasadzie ad hoc.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Rezerwacja elastyczna dla pozycji śledzonych w partii

### <a name="business-scenario"></a>Scenariusz biznesowy

W tym scenariuszu firma korzysta z strategii zapasów, w której gotowe towary są śledzone według numerów partii. Ta firma również korzysta z obciążenia pracą WMS. Ponieważ w ramach tego obciążenia istnieje dobrze wyposażona logika planowania i uruchamiania operacji pobierania i wysyłania magazynowych dla towarów z włączonym przetwarzaniem wsadowym, większość gotowych towarów jest skojarzona z hierarchią rezerwacji "zapasów poniżej\[lokalizacji\]". Zaletą tego typu konfiguracji operacyjnej jest to, że decyzje (które są skutecznymi decyzjami dotyczącymi rezerwacji), które partie do pobrania i miejsca, gdzie mają zostać umieszczone w magazynie, są odkładane do momentu rozpoczęcia operacji pobrania z magazynu. Nie zostają one wykonane, gdy zamówienie odbiorcy zostanie złożone.

Mimo że hierarchia rezerwacji "Lokalizacji towaru\[poniżej\]" obsługuje również cele biznesowe firmy, wiele odbiorców z firmy prowadzącej działalność w firmie wymaga tej samej partii, którą zostały wcześniej zakupione podczas zamawiania produktów. Z tego względu firma poszukuje elastyczności w sposobie obsługi reguł rezerwacji partii, dzięki czemu w zależności od zapotrzebowania klienta dla tego samego towaru mają miejsce następujące zachowania:

- Numer partii może zostać zarejestrowany i zarezerwowany, gdy zamówienie jest wykonywane przez przetwórcę sprzedaży, i nie można go zmienić podczas operacji magazynowych i/lub w przypadku innych zapotrzebowań. To zachowanie pomaga zagwarantować, że zamówiony numer partii jest wysyłany do odbiorcy.
- Jeśli numer partii nie jest ważny dla odbiorcy, operacje magazynowe mogą określać numer partii podczas pracy pobierania, po zakończeniu rejestracji i rezerwacji zamówienia sprzedaży.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Umożliwienie rezerwacji konkretnej partii w zamówieniu sprzedaży

Aby określić wymaganą elastyczność w zachowaniu rezerwacji partii dla towarów skojarzonych z hierarchią rezerwacji magazynowej "Lokalizacji towaru\[poniżej\], menedżerowie magazynów muszą zaznaczyć pole wyboru **Zezwalaj na rezerwację na zamówieniu** na zapotrzebowaniu dla **Numeru partii** na stronie **hierarchie rezerwacji zapasów**.

![Uczynienie hierarchii rezerwacji zapasów elastyczną](media/Flexible-inventory-reservation-hierarchy.png)

W przypadku wybrania poziomu **Numeru partii** w hierarchii wszystkie wymiary powyżej tego poziomu i na poziomie **Lokalizacji** zostaną wybrane automatycznie. (Domyślnie zaznaczone są wszystkie wymiary powyżej poziomu **Lokalizacji**). To zachowanie odzwierciedla logikę, w której wszystkie wymiary w zakresie między numerem partii i lokalizacją są również automatycznie rezerwowane po zarezerwowaniu określonego numeru partii w wierszu zamówienia.

> [!NOTE]
> Pole wyboru **Zezwalaj na rezerwację na zamówieniu popytu** dotyczy tylko poziomów hierarchii rezerwacji poniżej wymiaru lokalizacji magazynowej.
>
> **Numer partii** jest jedynym poziomem hierarchii otwartym dla elastycznych zasad rezerwacji. Innymi słowy, nie można zaznaczyć pola wyboru **Zezwalaj na rezerwację na zamówieniu popytu** dla **Lokalizacji**, **numeru identyfikacyjnego** lub **numeru seryjnego**.
>
> Jeśli hierarchia rezerwacji zawiera wymiar numeru seryjnego (który musi być zawsze poniżej poziomu **numeru partii**), a w przypadku rezerwacji specyficznej dla danej partii dla numeru partii, system będzie kontynuował obsługę rezerwacji numerów seryjnych i operacji pobrania na podstawie reguł dotyczących zasad rezerwacji „Numer poniżej\[lokalizacji\]”.

W dowolnym momencie można zezwolić na przetwarzanie specyficznego przetwarzania wsadowego istniejącej hierarchii rezerwacji „Lokalizacja towaru\[poniżej\]” w rozmieszczeniu. Ta zmiana nie wpłynie na rezerwacje i otwarte prace magazynowe, które zostały utworzone przed zmianą. Nie można jednak wyczyścić pola wyboru **Zezwalaj na rezerwację na zamówienie popytu**, jeśli dla jednego lub większej liczby towarów skojarzonych z tą hierarchią rezerwacji istnieją transakcje magazynowe typu **zamówione**, **zarezerwowane fizycznie** lub **zamówione**.

> [!NOTE]
> Jeśli istniejąca hierarchia rezerwacji dla towaru nie zezwala na specyfikację partii w zamówieniu, można ją ponownie przypisać do hierarchii rezerwacji, która pozwala na określenie partii, pod warunkiem że struktura poziomu hierarchii jest taka sama w obu hierarchiach. Aby wykonać ponowne przypisanie, należy skorzystać z funkcji **Zmień rezerwację pozycji**. Ta zmiana może być odpowiednia, jeśli chcesz zapobiec elastycznej rezerwacji wsadowej dla podzestawu pozycji śledzonych wsadowo, ale zezwól na to w pozostałej części teczki produktów.

Niezależnie od tego, czy zaznaczono pole wyboru **Zezwalaj na rezerwację na zamówieniu zapotrzebowania**, jeśli nie chcesz zarezerwować określonego numeru partii dla towaru w wierszu zamówienia, będzie nadal obowiązywała domyślna logika operacji magazynowych obowiązująca dla hierarchii rezerwacji "lokalizacja towaru \[poniżej\]”.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Rezerwacja określonego numeru partii dla zamówienia odbiorcy

Po skonfigurowaniu śledzonej partii pozycji „Lokalizacja towaru\[ poniżej\]” w hierarchii rezerwacji zapasów można zezwolić na rezerwacje określonych numerów partii w zamówieniach sprzedaży, jednak przetwórcy zamówień sprzedaży mogą przyjmować zamówienia odbiorców dla tego samego towaru w jeden z następujących sposobów, w zależności od wniosku klienta:

- **Wprowadź szczegóły zamówienia bez określania numeru partii** — to podejście należy stosować w przypadku, gdy specyfikacja partii produktu nie jest ważna dla odbiorcy. Wszystkie istniejące procesy skojarzone z obsługą zamówienia tego typu System pozostają niezmienione. Część użytkowników nie wymaga żadnych dodatkowych okoliczności.
- **Wprowadź szczegóły zamówienia i Zarezerwuj określony numer partii** — tego podejścia należy użyć w przypadku, gdy odbiorca zażąda konkretnej partii. Zazwyczaj odbiorcy zażądają konkretnej partii, gdy będą zamawiali produkty uprzednio nabyte. Ten typ rezerwacji specyficznej dla danej partii jest określany mianem *rezerwacji do zamówienia*.

Następujący zbiór reguł jest ważny podczas przetwarzania ilości, a numer partii jest zatwierdzany w określonym zamówieniu:

- Aby zezwolić na rezerwację określonego numeru partii towaru w zasadzie rezerwacji „Lokalizacja towaru \[poniżej\]”, system musi zarezerwować wszystkie wymiary w górę w lokalizacji. Ten zakres zazwyczaj zawiera wymiar numeru identyfikacyjnego.
- Dyrektywy lokalizacji nie są używane, gdy jest tworzona praca pobrania dla wiersza sprzedaży, w którym jest używana rezerwacja partii zamówienia.
- Podczas przetwarzania magazynu pracy dla partii zakontraktowanych na zamówienie ani użytkownik, ani systemow nie mogą zmieniać numeru partii. (Przetwarzanie obejmuje obsługę wyjątków)

W poniższym przykładzie pokazano przepływ typu end-to-end.

## <a name="example-scenario"></a>Przykładowy scenariusz

W tym przukładzie trzeba mieć zainstalowane dane demonstracyjne oraz musi być używana wersja demonstracyjna **USMF** danych firmy.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Skonfiguruj hierarchię rezerwacji zapasów w celu umożliwienia rezerwacji specyficznej dla partii

1. Przejdź do **Ustawień magazynu** \> **Ustawień** \> **Zapasów \> Hierarchii rezerwacji**.
2. Wybierz pozycję **Nowy**.
3. W polu **Nazwa** wprowadź nazwę (na przykład **BatchFlex**).
4. W polu **Opis** wprowadź opis (np. **Lokalizacja towaru poniżej dynamicznie**).
5. W **Zaznaczonym** polu wybierz opcję **Numer seryjny** i **Właściciel**, a następnie wybierz przycisk strzałka w lewo, aby przenieść je do **Dostępnego** pola.
6. Kliknij przycisk **OK**.
7. W wierszu dla poziomu wymiaru **numer partii** zaznacz pole wyboru **Zezwalaj na rezerwację na zamówieniu popytu**. **Numery identyfikacyjne** i **numery lokalizacji** są wybierane automatycznie i nie można wyczyścić tych pól wyboru.
8. Wybierz opcję **Zapisz**.

### <a name="create-a-new-released-product"></a>Tworzenie nowego zwolnionego produktu

1. Aby określić trzy parametry danych głównych produktu, należy użyć następujących wartości:

    - W polu **Grupa wymiarów magazynowania** wybierz **Towar**.
    - W polu **Grupę wymiarów śledzenia** wybierz **Batch-Phy**.
    - W polu **Rezerwacja hierarchi** zaznacz opcję **BatchFlex**.

2. Utwórz dwa numery partii, takie jak **B11** i **B22**.
3. Umożliwia dodawanie ilości towarów do dostępnych zapasów przy użyciu następujących wartości:

    | Magazyn | Numer partii | Lokalizacja | Numer identyfikacyjny | Ilość |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Brak          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Podawanie szczegółów zamówienia sprzedaży

1. Przejdź kolejno do pozycji **Sprzedaż i marketing** \> **Zamówienia sprzedaży** \> **Wszystkie zamówienia sprzedaży**.
2. Wybierz pozycję **Nowy**.
3. W nagłówku zamówienia sprzedaży w sekcji **Konto odbiorcy** wprowadź **US-003**.
4. Dodaj wiersz dla nowego produktu i wprowadź **10** jako ilość. Upewnij się, że pole **Magazyn** zawiera wartość **24**.
5. W skróconej karcie **Wiersz zamówienia sprzedaży** wybierz pozycję **Zapasy**, a następnie w grupie **Obsługa** wybierz opcję **Rezerwacja partii**. Na stronie **Rezerwacja partii** jest wyświetlana lista partii dostępnych do rezerwacji dla wiersza zamówienia. W tym przykładzie przedstawiono ilość **20** dla numeru partii **B11** i ilość **10** dla numeru partii **B22**. Należy pamiętać, że nie można uzyskać dostępu do strony **rezerwacja partii** z wiersza, jeśli towar w tym wierszu jest skojarzony z hierarchią rezerwacji "Lokalizacja towaru\[poniżej\], chyba że jest skonfigurowany tak, aby zezwalać na rezerwacje specyficzne dla danej partii.

    > [!NOTE]
    > Aby zarezerwować określoną partię dla zamówienia sprzedaży, należy skorzystać ze strony **Rezerwacja partii**.
    >
    > Jeśli numer partii zostanie wprowadzony bezpośrednio w wierszu zamówienia sprzedaży, system zatrzyma się, tak jakby wprowadzono określoną wartość partii towaru, która podlega zasadom rezerwacji „Lokalizacja towaru\[poniżej\]”. Po zapisaniu wiersza pojawi się komunikat ostrzegawczy. Jeśli użytkownik potwierdzi, że numer partii ma być określony bezpośrednio w wierszu zamówienia, wiersz nie będzie obsługiwany przez zwykłą logikę zarządzania magazynem.
    >
    > Jeśli zarezerwujesz ilość na stronie **Rezerwacja**, nie zostanie zarezerwowana żadna określona partia, a wykonywanie operacji magazynowych dla wiersza będzie odbywać się zgodnie z regułami dotyczącymi rezerwacji w obszarze „Lokalizacja towaru\[poniżej\]”.

    Na ogół ta strona działa i jest współdziałana w taki sam sposób, w jaki działa i jest aktywnie związana z elementami, które mają skojarzoną hierarchię rezerwacji dla typu „Lokalizacja towaru\[powyżej\]”. Obowiązują jednak następujące wyjątki:

    - Numery **Partii przekazane do wiersza źródłowego** skróconej karcie są wyświetlane zgodnie z numerami partii, które są zarezerwowane dla danego wiersza zamówienia. Wartości partii w siatce będą wyświetlane w cyklu realizacji wiersza zamówienia, w tym w etapach przetwarzania magazynu. Z drugiej strony, na **Przeglądowej** karcie skróconej, zwykła rezerwacja wiersza zamówienia (czyli rezerwacja wykonana dla wymiarów powyżej poziomu **Lokalizacji**) jest wyświetlana w siatce w górę do momentu utworzenia pracy magazynowej. Jednostka pracy przejmuje wówczas rezerwację wiersza, a rezerwacja wiersza nie jest już wyświetlana na stronie. **Numery partii przekazane do wiersza źródłowego** na skróconej karcie ułatwiają zagwarantowanie, że moduł przetwarzający zamówienia sprzedaży może wyświetlić numery partii, które zostały przekazane do zamówienia odbiorcy w dowolnym momencie, w trakcie fakturowania.
    - Oprócz rezerwowania konkretnej partii użytkownik może ręcznie wybrać lokalizację i numer identyfikacyjny danej partii, zamiast zezwalać na automatyczne wybieranie numeru identyfikacyjnego danej partii. Ta możliwość jest związana z projektem mechanizmu rezerwacji partii zakontraktowanego zamówienia. Tak jak wspomniano wcześniej, aby zezwolić na rezerwację określonego numeru partii towaru w zasadzie rezerwacji „Lokalizacja towaru\[poniżej\]”, system musi zarezerwować wszystkie wymiary w górę w lokalizacji. Z tego względu prace magazynowe będą miały te same wymiary magazynowe, które zostały zarezerwowane przez użytkowników pracujących z tymi zamówieniami i nie zawsze będą reprezentować położenie magazynu towarów, które jest wygodne, a nawet możliwe dla operacji pobierania. Jeśli przetwórcy zamówień są świadomi ograniczeń magazynowych, może zaistnieć potrzeba ręcznego wybrania konkretnych lokalizacji i numerów identyfikacyjnych podczas rezerwowania partii. W takim przypadku użytkownik musi skorzystać z funkcji **wymiarów wyświetlanych** w nagłówku strony i musi dodać lokalizację i numer identyfikacyjny w siatce w skróconej karcie **Przegląd**.

6. Na stronie **rezerwacja partii** wybierz wiersz dla **B11**wsadowego, a następnie wybierz opcję **wiersz rezerwy**. Podczas automatycznej rezerwacji nie ma żadnej wskazanej logiki do przypisywania lokalizacji i numerów identyfikacyjnych. Ilość można wprowadzić ręcznie w polu **rezerwacja**. Zwróć uwagę, że w przypadku skróconej karty **numerów partii przekazanych do wiersza źródłowego**, zestaw **B11** jest wyświetlany jako **Zatwierdzony**.

    ![Zatwierdzanie określonego numeru partii do wiersza zamówienia sprzedaży na stronie rezerwacja partii](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Rezerwacja ilości w wierszu zamówienia sprzedaży może zostać wykonana na wielu partiach. Ponadto rezerwacja tej samej partii może zostać wykonana dla wielu lokalizacji i numerów identyfikacyjnych (jeśli są włączone płytki rejestracyjne dla lokalizacji).
    >
    > Rezerwacja konkretnej partii dla ilości w wierszu zamówienia sprzedaży może być także częściowa. Na przykład całkowita ilość 100 jednostek może zostać zarezerwowana, aby określona partia była przydzielona do 20 jednostek, natomiast jednostki 80 są rezerwowane na poziomie oddziału i magazynu dla dowolnej dostępnej partii. W tym przypadku moduł WMS będzie obsługiwał operacje pobierania za pomocą dwóch oddzielnych wierszy pracy.

7. Przejdź do **Zarządzanie informacjami o produktach** \> **Produkty** \> **Zwolnione produkty**. Wybierz towar, a następnie wybierz pozycję **Zarządzaj zapasami** \> **Widok** \> **Transakcje**.

    ![Rezerwacja zamówiona jako typ transakcji magazynowej](media/Inventory-transactions-for-order-committed-reservation.png)

8. Umożliwia przejrzenie transakcji magazynowych dotyczących danego towaru, które są powiązane z rezerwacją wiersza zamówienia sprzedaży.

    - Transakcja, w której pole **Odwołania** jest ustawione na **Zamówienie** sprzedaży, a **Rozchód** ma wartość **Fizycznie zarezerwowane**, oznacza rezerwę wiersza zamówienia dla wymiarów magazynowych powyżej poziomu **lokalizacji**. Zgodnie z hierarchią rezerwacji zapasów danego towaru, wymiary te to oddział, magazyn i stan zapasów.
    - Transakcja, w której pole **Odwołania** jest ustawione na **Rezerwacja-zamówienie sprzedaży**, a pole **Wydanie** ma wartość **Fizycznie zarezerwowane**, oznacza rezerwę wiersza zamówienia dla danej partii towaru i wszystkich zapasów ponad nią. Zgodnie z hierarchią rezerwacji zapasów danego towaru, wymiary te to numer partii oraz lokalizacja. W tym przykładzie lokalizacja to **Bulk-001**.

9. W nagłówku zamówienia wybierz **Magazyn** \> **Działania** \> **Zwolnij do magazynu**. Wiersz zamówienia jest teraz waved i jest tworzony ładunek i praca.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Służy do przeglądania i przetwarzania pracy magazynowej z numerami partii zatwierdzonych dla zamówienia

1. W skróconej karcie **Kolejność zamówień sprzedaży**, wybierz opcję **Magazyn** \> **Szczegóły pracy**.

    Praca, która obsługuje operację pobrania dla ilości partii, która jest potwierdzona w wierszu zamówienia sprzedaży, ma następujące cechy:

    - Aby utworzyć pracę, system używa szablonów roboczych, ale nie zawiera dyrektyw lokalizacji. Wszystkie standardowe ustawienia zdefiniowane dla szablonów pracy, takie jak Maksymalna liczba wierszy pobrania lub określony jednostka miary, zostaną zastosowane w celu ustalenia, kiedy należy utworzyć nową pracę. Jednak reguły skojarzone z dyrektywami lokalizacji do identyfikowania lokalizacji pobrania nie są uwzględniane, ponieważ rezerwacja rezerwacji zamówień już określa wszystkie wymiary magazynowe. Te wymiary magazynowe obejmują wymiary na poziomie składowania w magazynie. Dlatego praca dziedziczy te wymiary bez konieczności konsultowania dyrektyw lokalizacji.
    - Numer partii nie jest wyświetlany w wierszu pobrania (podobnie jak w przypadku wiersza pracy utworzonego dla towaru, który ma skojarzoną hierarchię rezerwacji z lokalizacji\[powyżej\]) zamiast tego numer partii „od” i wszystkie inne wymiary magazynowe są wyświetlane w transakcji magazynowej dla wiersza pracy, do której odwołuje się skojarzone transakcje magazynowe.

        ![Transakcja magazynowa magazynu dla pracy, która pochodzi z rezerwacji zamówienia](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Po utworzeniu pracy zostanie usunięta transakcja magazynowa towaru, w której pole **odwołania** ma ustawioną rezerwację **Rezerwacja-zamówienie sprzedaży**. Transakcja magazynowa, w której pole **odwołania** ma wartość **praca**, zawiera rezerwę fizyczną dla wszystkich wymiarów magazynowych z ilością.

        Operacje magazynowe mogą być kontynuowane w celu obsługi wykonania pracy w zwykły sposób. Jednak instrukcje na urządzeniu przenośnym wykazują pracownikowi pobranie określonego numeru partii. W środowiskach magazynowych, w których lokalizacje są oznaczone numerami identyfikacyjnymi, gdy pracownik osiągnie lokalizację, w której jest przechowywana taka sama partia na wielu płytach, może pobrać z dowolnego numeru identyfikacyjnego, który nie został jeszcze zarezerwowany (np. inny zadeklarowana rezerwacja zamówienia lub praca pochodząca z rezerwacji tego typu).

        Jeśli okaże się, że nie będzie on praktyczny do pobrania z lokalizacji określonej w wierszu pracy, operatorzy magazynu mogą używać jednej z następujących akcji do przekierowywania pobierania określonej partii z bardziej wygodnej lokalizacji:

        - Standardowa akcja **zastępowania lokalizacji** na urządzeniu przenośnym (pod warunkiem, że włączone jest ustawienie **Zezwalaj na zastępowanie lokalizacji pobrania**)
        - Akcja **zmiany lokalizacji** na stronie **Szczegóły listy prac**. 

2. Na urządzeniu przenośnym Zakończ pobieranie i odkładanie pracy.

    Ilość **10** dla numeru partii **B11** jest teraz pobierana dla wiersza zamówienia sprzedaży i umieszczona w lokalizacji **Baydoor**. W tym momencie jest gotowy do załadunku na samochód i wysyłany do adresu odbiorcy.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Zarządzanie wyjątkami pracy magazynowej z numerami partii zatwierdzonych dla zamówienia

Praca w magazynie dla zamówienia pobrania — numery partii zatwierdzonej podlegają tej samej standardowej obsłudze wyjątków magazynowych oraz działaniu zwykłej pracy. Na ogół można anulować otwartą pracę lub wiersz pracy, ponieważ jest zapełniony, ponieważ lokalizacja użytkownika jest zapełniona, może być ona pobrana i można ją zaktualizować z powodu przesunięcia. Podobnie pobrana ilość pracy, która została już zakończona, może zostać zmniejszona lub praca może zostać wycofana.

Do wszystkich tych akcji obsługi wyjątków jest stosowana następująca reguła klucza: numer partii zarezerwowany dla odbiorcy nie może zostać zastąpiony innym numerem partii, ale jego wymiary przechowywania (lokalizacja i numer identyfikacyjny) można zmienić za pomocą opcji Ręczna aktualizacja użytkownika lub automatyczna aktualizacja systemu przez system. Automatyczna aktualizacja jest oparta na tym samym przypisaniu losowym wymiarów magazynowych, które mają zastosowanie w przypadku, gdy określona partia została zarezerwowana automatycznie, ale nie określono wymiarów magazynowania.

### <a name="example-scenario"></a>Przykładowy scenariusz

Przykładem tego scenariusza jest sytuacja, w której uprzednio ukończona praca jest wycofywana za pomocą funkcji **Zmniejsz ilość pobranych ilości**. W tym przykładzie jest kontynuowany poprzedni przykład w tym temacie.

1. Wybierz kolejno opcje **Zarządzanie magazynem** \> **Ładunki** \> **Aktywne ładunki**.
2. Umożliwia wybór ładunku utworzonego w związku z wysyłką zamówienia sprzedaży.
3. W skróconej karcie **wierszy zamówienia ładunku** wybierz opcję **Zmniejsz ilość pobraną**.
4. Na stronie **Zmniejsz ilość pobranych towarów** w polu **Przenieś do lokalizacji** zaznacz opcję **FL-001**.
5. W polu **Przenieś do numeru identyfikacyjnego** zaznacz opcję **LP33**.
6. W polu **ilość zapasów do cofnięcia pobrania**, wprowadź wartość **10**.
7. Kliknij przycisk **OK**.

Poniżej przedstawiono wyniki cofnięcia pobrania:

- Stan poprzednio zamkniętej pracy jest ustawiany jako **anulowany**.
- Nowa praca typu **przesunięcie zapasów** jest tworzona dla niepobranej ilości **10** dla numeru **partii B11**. Ta praca reprezentuje przesunięcie z lokalizacji **Baydoor** do numeru identyfikacyjnego **LP33** w lokalizacji **FL-001**. Stan zostanie ustawiony na **Zamknięty**.
- System ponownie rezerwuje numer partii, który został pierwotnie zamówiony, a następnie przypisuje lokalizację i identyfikatory numerów identyfikacyjnych. (Ten proces jest równoznaczny z uruchomieniem funkcji **wiersza rezerwy** dla wiersza zamówienia dla danego numeru partii). W wyniku tego partia **B11** jest pokazana jako zatwierdzona na skróconej karcie **numery partii przekazanych do wiersza źródłowego**, na stronie **rezerwacja partii**, a pole **rezerwacja** zawiera ilość **10** dla numeru partii **B11**. Ponadto pole **lokalizacji** jest ustawione na **FL-001**, a pole **numeru identyfikacyjnego** jest ustawione na **LP11**. (Jeśli te pola są niewidoczne, można je dodać do siatki)

Poniższe tabele zawierają przegląd, w jaki sposób system obsługuje zarezerwowaną rezerwację partii dla konkretnych akcji magazynowych. Aby interpretować zawartość w tabelach, należy zastanowić się, że każda akcja magazynowa jest uruchamiana w kontekście istniejącej pracy magazynowej, która pochodzi z rezerwacji partii zamówienia, lub że wykonanie każdej akcji magazynowej ma wpływ na pracę tego typu.

> [!NOTE]
> W tych tabelach kolumna „ilość partii jest dostępna” wskazuje, czy ilość partii jest dostępna oprócz ilości, która jest już zarezerwowana dla bieżącego zamówienia — zatwierdzone rezerwacje lub już zarezerwowana przez pracę magazynową, która pochodzi z rezerwacji tego typu.

#### <a name="override-the-pick-location-on-the-open-work"></a>Zastąpienie lokalizacji odbioru w otwartej pracy

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Opcja <strong>Zezwalaj na zastępowanie lokalizacji pobrania</strong> jest włączona dla pracownika.</td>
<td>Tak</td>
<td>
<ol>
<li>Umożliwia wybranie opcji <strong>Zastąp element menu lokalizacji</strong> w magazynie Mmobile App (WMA) po rozpoczęciu pracy pobrania.</li>
<li>Wybierz opcję <strong>Sugeruj</strong>.</li>
<li>Potwierdź nową lokalizację sugerowaną na podstawie dostępności ilości partii.</li>
</ol>
</td>
<td>W bieżącej pracy wykonywane są następujące akcje:
<ul>
<li>Lokalizacja w wierszu pobrania zostanie zaktualizowana do nowej lokalizacji. (Jeśli lokalizacja jest kontrolowana numerami identyfikacyjnymi, to losowy numer identyfikacyjny jest przypisany do transakcji magazynowej pracy, a pracownik może pobrać z dowolnego numeru identyfikacyjnego, który ma dostępną ilość.)</li>
<li>Jeśli ilość została znaleziona na więcej niż jednym numerze identyfikacyjnym w nowej lokalizacji, pierwotny wiersz pobrania jest podzielony na kilka wierszy w celu dopasowania do każdego numeru identyfikacyjnego.</li>
</ul>
</td>
<td>Nie dotyczy</td>
</tr>
<tr>
<td>Nie</td>
<td>
<ol>
<li>Umożliwia wybranie opcji <strong>Zastąp element menu lokalizacji</strong> w magazynie Mmobile App (WMA) po rozpoczęciu pracy pobrania.</li>
<li>Umożliwia ręczne wprowadzenie lokalizacji.</li>
</ol>
</td>
<td>Akcja <strong>zastąpienia lokalizacji</strong> nie jest możliwa. Nie powiedzie się i zostanie zgłoszony błąd.</td>
<td>Nie dotyczy</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Pełny przycisk — Podziel wiersz pracy z powodu przepełnienia w lokalizacji użytkownika

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td>Opcja <strong>Zezwalaj na dzielenie pracy</strong> jest włączona w elemencie menu urządzenia przenośnego.</td>
<td>Nie dotyczy</td>
<td>
<ol>
<li>Wybierz opcję <strong>Pełna</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu pobrania pracy.</li>
<li>W polu <strong>Ilość pobrania</strong>, wprowadź częściową ilość wymaganego pobrania, aby wskazać pełną wydajność.</li>
</ol>
</td>
<td>
<ul>
<li>W bieżącej pracy ilość jest aktualizowana na pozostałą ilość, która musi zostać pobrana.</li>
<li>Utworzono i zamknięto nową pracę dla pobranej ilości.</li>
</ul></td>
<td>Nie dotyczy</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Zmniejsz ilość pobraną ukończonej pracy (z ładunku)

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Nie dotyczy</td>
<td>Tak</td>
<td>
<ol>
<li>Otwórz stronę <strong>Zmniejsz ilość pobraną</strong> z wiersza ładunku.</li>
<li>Wprowadź ilość, która ma zostać cofnięta.</li>
<li>Wybierz pozycję „Przenieś do” w lokalizacji/numer identyfikacyjny.</li>
</ol>
</td>
<td>
<ul> 
<li>Praca skojarzona z wierszem ładunku została anulowana.</li>
<li>Nowa praca dla zarządzania zapasami jest utworzone i zamknięte.</li>
</ul>
</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii i dla tej samej lokalizacji i numeru identyfikacyjnego (jeśli lokalizacją jest karta identyfikacyjna — kontrolowana), która została wprowadzona podczas niepobierania.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Przenoszenie towaru w magazynie

> [!NOTE]
> Tę akcję magazynową można stosować tylko do przepływu typu **Procesu tworzenia pracy**, a nie do przenoszenia według szablonów.

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Dla pracownika jest włączona opcja <strong>Zezwalaj na przenoszenie zapasów ze skojarzoną pracą</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Umożliwia rozpoczęcie przepływu w module WMA.</li>
<li>Wprowadź początkową i końcową lokalizację.</li>
</ol></td>
<td>
<ul>
<li>W przypadku wszystkich istniejących pracy, których dotyczy przeniesienie, lokalizacja pobrania jest aktualizowana do nowej lokalizacji „do”.</li>
<li>Nowa praca dla zarządzania zapasami jest utworzone i zamknięte.</li>
</ul>
</td>
<td>Wszystkie istniejące rezerwacje, na które ma wpływ przesunięcie ilości z danej lokalizacji, są ponownie rezerwowane dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Wszystkie istniejące rezerwacje, na które ma wpływ przesunięcie ilości z danej lokalizacji, są ponownie rezerwowane dla tej samej partii oraz dla nowej lokalizacji „do” i numeru identyfikacyjnego (jeśli lokalizacją jest karta identyfikacyjna).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Cofnij zmniejsz ilość pobraną ukończonej pracy (z ładunku lub fali)

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Nie dotyczy</td>
<td>Tak</td>
<td>
<ol>
<li>Otwórz stronę <strong>Odwróć pracę</strong>.</li>
<li>Na stronie żądanie wybierz opcję <strong>Pozostaw towary w bieżącej lokalizacji</strong>.</li>
</ol>
</td>
<td>Cała praca skojarzona z wierszem ładunku została anulowana.</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii oraz dla lokalizacji i numeru identyfikacyjnego, gdzie ilość została pozostawiona po wycofaniu.</td>
</tr>
<tr>
<td>Tak</td>
<td>
<ol>
<li>Otwórz stronę <strong>Odwróć pracę</strong>.</li>
<li>Na stronie żądanie wybierz opcję <strong>Przypisz towary w bieżącej lokalizacji</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Bieżąca praca została anulowana.</li>
<li>Nowa praca dla zarządzania zapasami jest utworzone i zamknięte.</li>
</ul>
</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii oraz dla lokalizacji i numeru identyfikacyjnego, gdzie ilość została przypisana po odwróceniu.</td>
</tr>
<tr>
<td>Tak/nie</td>
<td>
<ol>
<li>Otwórz stronę <strong>Odwróć pracę</strong>.</li>
<li>Na stronie żądanie wybierz opcję <strong>Przenieś towary w bieżącej lokalizacji</strong>.</li>
</ol>
</td>
<td>Odwrócenie nie jest obsługiwane.</td>
<td>Nie dotyczy</td>
</tr>
<tr>
<td>Tak/nie</td>
<td>
<ol>
<li>Otwórz stronę <strong>Odwróć pracę</strong>.</li>
<li>Na stronie żądanie wybierz opcję <strong>Przenieś towary w zależności od dyrektyw lokalizacji</strong>.</li>
</ol>
</td>
<td>Odwrócenie nie jest obsługiwane. </td>
<td>Nie dotyczy</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Krótki — pobranie ilości — umożliwia zarejestrowanie ilości fizycznie nieznalezionej w numerze lokalizacji/numeru identyfikacyjnego podczas wykonywania prac pobrań

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>None</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Nie</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>Powód</strong>, wpisz <strong>Brak realokacji</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Bieżąca praca jest zamknięta, a pobrana ilość wynosi 0 (zero).</li>
<li>Zostanie utworzona transakcja magazynowa typu <strong>Inwentaryzacja</strong> oraz typ <strong>Sprzedany</strong> są wystawione w celu odzwierciedlenia korekty.</li>
</ul>
</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>
<ul>
<li>Akcja krótkiego pobrania nie powiedzie się i zostanie zgłoszony błąd.</li>
<li>Bieżąca praca pozostanie otwarta.</li>
</ul>
</td>
<td>Nie dotyczy</td>
</tr>
<tr>
<td rowspan='2'>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>None</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Tak</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>Powód</strong>, wpisz <strong>Brak realokacji</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Bieżąca praca jest zamknięta, a pobrana ilość wynosi 0 (zero).</li>
<li>Zostanie utworzona transakcja magazynowa typu <strong>Inwentaryzacja</strong> oraz typ <strong>Sprzedany</strong> są wystawione w celu odzwierciedlenia korekty.</li>
</ul>
</td>
<td>Wszystkie istniejące rezerwacje, na które ma wpływ przesunięcie ilości z danej lokalizacji krótkiego odbioru, są ponownie rezerwowane dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Wszystkie istniejące rezerwacje, na które ma wpływ przesunięcie ilości z danej lokalizacji krótkiego odbioru, są usuwane.</td>
</tr>
<tr>
<td>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>Ręcznie</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Nie/Tak</strong>. Ponadto dla pracownika jest włączona opcja <strong>Zezwalaj na ręczną zmianę alokacji pozycji</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana z krótkiego odbioru</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>przyczyna</strong> wybierz opcję <strong>krótkie pobieranie z ręczną zmianą alokacji</strong>.</li>
<li>Wybierz numer lokalizacji/numer identyfikacyjny na liście.</li>
</ol>
</td>
<td>
<ul>
<li>W bieżącej pracy wykonywane są następujące akcje:
<ul>
<li>Bieżąca linia odbioru jest zamknięta, a pobrana ilość wynosi 0 (zero).</li>
<li>Wiersz odłożenia został anulowany.</li>
<li>Zostanie utworzony nowy wiersz pobrania. Używa on numeru lokalizacji/licencji wybranego przez użytkownika.</li>
<li>Zostanie utworzony nowy linia włożenia.</li>
</ul>
</li>
<li>Zostanie utworzona transakcja magazynowa typu <strong>Inwentaryzacja</strong> oraz typ <strong>Sprzedany</strong> są wystawione w celu odzwierciedlenia korekty.</li>
</ul>
</td>
<td>Nie dotyczy</td>
</tr>
<tr>
<td>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>Ręcznie</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Nie</strong>. Ponadto dla pracownika jest włączona opcja <strong>Zezwalaj na ręczną zmianę alokacji pozycji</strong>.</td>
<td>Nie</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana z krótkiego odbioru</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>przyczyna</strong> wybierz opcję <strong>krótkie pobieranie z ręczną zmianą alokacji</strong>.</li>
</ol>
</td>
<td>Akcja krótkiego pobrania nie powiedzie się i zostanie zgłoszony błąd.</td>
<td>Nie dotyczy</td>
</tr>
<tr>
<td>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>Ręcznie</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Tak</strong>. Ponadto dla pracownika jest włączona opcja <strong>Zezwalaj na ręczną zmianę alokacji pozycji</strong>.</td>
<td>Nie</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana z krótkiego odbioru</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>przyczyna</strong> wybierz opcję <strong>krótkie pobieranie z ręczną zmianą alokacji</strong>.</li>
<li>Wybierz numer lokalizacji/numer identyfikacyjny na liście.</li>
</ol>
</td>
<td>
<ul>
<li>W bieżącej pracy wykonywane są następujące akcje:
<ul>
<li>Bieżąca linia odbioru jest zamknięta, a pobrana ilość wynosi 0 (zero).</li>
<li>Wiersz odłożenia został anulowany.</li>
</ul>
</li>
<li>Zostanie utworzona transakcja magazynowa typu <strong>Inwentaryzacja</strong> oraz typ <strong>Sprzedany</strong> są wystawione w celu odzwierciedlenia korekty.</li>
</ul>
</td>
<td>Wszystkie istniejące rezerwacje, na które ma wpływ przesunięcie ilości z danej lokalizacji krótkiego odbioru/numer identyfikacyjny, są usuwane.</td>
</tr>
<tr>
<td>Skonfigurowano wyjątek pracy dla <strong>krótkiego typu pobrania</strong>, w którym jest ustawiana <strong>Ponowna alokacja towaru</strong> = <strong>Automatycznie</strong>, <strong>Dopasuj zapasy</strong> = <strong>Tak/Nie</strong> oraz <strong>Usuń rezerwacje</strong> = <strong>Tak/Nie</strong>.</td>
<td>Nie dotyczy</td>
<td>
<ol>
<li>Wybierz opcję <strong>Krótki wybór</strong> w magazynie Mmobile App (WMA) po rozpoczęciu procesu uruchomienia pracy.</li>
<li>W polu <strong>Ilość pobrana z krótkiego odbioru</strong> wpisz wartość <strong>0</strong> (zero).</li>
<li>W polu <strong>przyczyna</strong> wybierz opcję <strong>krótkie pobieranie z automatyczną zmianą alokacji</strong>.</li>
</ol>
</td>
<td>Krótkie — pobranie obejmujące automatyczne ponowne przydzielanie nie jest obsługiwane.</td>
<td>Krótkie — pobranie obejmujące automatyczne ponowne przydzielanie nie jest obsługiwane.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Zmiana stanu zapasów

> [!NOTE]
> Tę akcję magazynową można wykonać z wielu punktów wejścia. W przykładzie pokazano, że akcja **Zmień stan zapasów** jest używana na stronie **dostępne zapasy w ramach lokalizacji**.

<table>
<thead>
<tr>
<th>Parametry ustawień klucza</th>
<th>Ilość partii jest dostępna</th>
<th>Najważniejsze kroki użytkownika</th>
<th>Praca magazynu</th>
<th>Rezerwacja-zamówienie sprzedaży partii</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Na karcie <strong>magazyn</strong> w rekordzie <strong>Magazynu</strong> w polu<strong>Usuń rezerwacje</strong> i oznaczenia jest ustawiona wartość <strong>rezerwacje</strong> lub <strong>oznaczenia i rezerwacje</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Wybór konkretnej lokalizacji.</li>
<li>Wybierz wiersz z określonym towarem, lokalizacją i numerem identyfikacyjnym (Jeśli lokalizacja jest kontrolowana numerem identyfikacyjnym).</li>
<li>Wybierz <strong>Zmianę stanu zapasów</strong>.</li>
<li>Pole <strong>Stan zapasów</strong> należy skonfigurować na <strong>blokowanie</strong>.</li>
</ol>
</td>
<td>Zmiany stanu zapasów nie są dozwolone dla ilości, które są zarezerwowane dla pracy.</td>
<td>
<ul>
<li>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</li>
<li>Zostaną utworzone dwie transakcje magazynowe o typie <strong>zmiany stanu zapasów</strong>, reprezentujące zmianę w wymiarze stanu zapasów.</li>
<li>Tworzona jest transakcja magazynowa typu <strong>blokowania zapasów</strong> i <strong>zarezerwowany typ fizycznego</strong> wystawienia w celu reprezentowania rezerwacji zablokowanej ilości.</li>
</ul>
</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Zmiany stanu zapasów nie są dozwolone dla ilości, które są zarezerwowane dla pracy.</td>
<td>
<ul>
<li>Rezerwacja jest usuwana.</li>
<li>Zostaną utworzone dwie transakcje magazynowe o typie <strong>zmiany stanu zapasów</strong>, reprezentujące zmianę w wymiarze stanu zapasów.</li>
<li>Tworzona jest transakcja magazynowa typu <strong>blokowania zapasów</strong> i <strong>zarezerwowany typ fizycznego</strong> wystawienia w celu reprezentowania rezerwacji zablokowanej ilości.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Na karcie magazyn w rekordzie <strong>Magazyn</strong> w polu <strong>Magazyn</strong>, pole <strong>Usuń rezerwacje i oznaczenia</strong> ma wartość <strong>Nie</strong>.</td>
<td>Tak</td>
<td>
<ol>
<li>Wybór konkretnej lokalizacji.</li>
<li>Wybierz wiersz z określonym towarem, lokalizacją i numerem identyfikacyjnym (Jeśli lokalizacja jest kontrolowana numerem identyfikacyjnym).</li>
<li>Wybierz <strong>Zmianę stanu zapasów</strong>.</li>
<li>Pole <strong>Stan zapasów</strong> należy skonfigurować na <strong>blokowanie</strong>.</li>
</ol>
</td>
<td>Zmiany stanu zapasów nie są dozwolone dla ilości, które są zarezerwowane dla pracy.</td>
<td>Ilość jest ponownie rezerwowana dla tej samej partii. System losowo przypisuje adres i numer identyfikacyjny (jeśli lokalizacją jest numer identyfikacyjny), gdzie dostępna jest ilość.</td>
</tr>
<tr>
<td>Nie</td>
<td>Przejdź do poprzedniego wiersza.</td>
<td>Zmiany stanu zapasów nie są dozwolone dla ilości, które są zarezerwowane dla pracy.</td>
<td>Zmiany stanu zapasów są niedozwolone.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Ograniczenia

- Funkcja rezerwacji wymiarów na poziomie magazynu elastycznego nie obsługuje następujących funkcji:

    - Zarządzanie ilością efektywną
    - Ujemne wartości magazynu fizycznego
    - Rezerwacja na zamówioną dostawę
    - Zamówienia przeniesienia i pobranie surowca

- Reguła konsolidacji kontenerów dla pakowania według jednostki dyrektywy ma pewne ograniczenia. W przypadku rezerwacji zamówionych zaleca się, aby nie stosować szablonów konstruowania kontenerów, w których jest włączone pole **pakowania według jednostek dyrektywy**. W bieżącym projekcie dyrektywy lokalizacji nie są używane podczas tworzenia pracy magazynowej. Dlatego tylko najniższa jednostka w grupie sekwencji jednostek (jednostka magazynowa) jest stosowana w trakcie kroku konteneryzacji.
