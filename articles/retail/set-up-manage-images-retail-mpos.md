---
title: "Konfigurowanie obrazów i zarządzanie nimi w module Retail Modern POS"
description: "W tym artykule objaśniono etapy konfigurowania obrazów i zarządzania nimi dla różnych jednostek wyświetlanych w module Retail Modern POS (MPOS)."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3985d731709eff4085927b277996528e4e448ba9
ms.contentlocale: pl-pl
ms.lasthandoff: 06/20/2017

---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Konfigurowanie obrazów i zarządzanie nimi w module Retail Modern POS

[!include[banner](includes/banner.md)]


W tym artykule objaśniono etapy konfigurowania obrazów i zarządzania nimi dla różnych jednostek wyświetlanych w module Retail Modern POS (MPOS).

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Konfigurowanie podstawowego adresu URL obiektu multimedialnego i definiowanie szablonów multimediów w celu konfiguracji formatu adresów URL obrazu
-------------------------------------------------------------------------------------------------

Obrazy wyświetlane w aplikacji Retail Modern POS (MPOS) muszą być obsługiwane zewnętrznie, poza programem Microsoft Dynamics 365 for Retail. Zazwyczaj znajdują się one w systemie zarządzania zawartością, sieci dostarczania zawartości (CDN) lub na serwerze multimediów. Następnie MPOS przechwytuje i wyświetla obrazy dla odpowiednich jednostek, takich jak produkty i katalogi, po przejściu do docelowego adresu URL. Aby pobierać te zewnętrznie obsługiwane obrazy, MPOS wymaga poprawnego formatu adresu URL dla obrazów. Wymagany format adresu URL dla obrazów można skonfigurować przez skonfigurowanie wartości **Podstawowy adres URL obiektu multimedialnego** w profilu kanału i za pomocą funkcji **Definiuj szablon multimediów** dla każdej jednostki. Można także zastąpić standardowy format adresu URL dla podzbioru jednostek za pomocą funkcji **Edytuj w programie Excel**. **Ważna uwaga:** W bieżącej wersji programu Dynamics 365 for Retail nie można już konfigurować formatu adresu URL za pomocą kodu XML atrybutu **obraz** dla aplikacji MPOS w grupie atrybutów **Domyślne** dla jednostek. Jeśli znasz system Microsoft Dynamics AX 2012 R3 i korzystasz obecnie z bieżącej wersji programu Dynamics 365 for Retail, pamiętaj, aby do ustawiania obrazów zawsze korzystać z funkcji **Definiuj szablon multimediów**. Nie używaj i nie zmieniaj atrybutu **obrazu** w **domyślnej** grupie atrybutów dla żadnych jednostek, włącznie z produktami. Zmiany wprowadzone bezpośrednio w **domyślnej** grupie atrybutów dla obrazów nie zostaną odzwierciedlone. Ta opcja będzie wyłączona w kolejnej wersji. W poniższych procedurach obrazy są konfigurowane dla jednostki katalogu jako przykład. Procedury te mogą pomogą zapewnić ustawienie prawidłowej docelowej ścieżki obrazu dla wszystkich obrazów z katalogu używających tej samej ścieżki. Na przykład, jeśli serwer multimediów lub CDN został ustawiony zewnętrznie, a chcesz, aby obrazy były wyświetlane w MPOS dla określonego sklepu, użyj funkcji **Definiuj szablon multimediów** w celu ustawienia ścieżki wyszukiwania i pobierania obrazów przez MPOS. **Uwaga:** w tym przykładzie serwer multimediów został wdrożony na serwerze sieci sprzedaży. Można go jednak umieścić w dowolnej lokalizacji poza programem Dynamics 365 for Retail.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Ustawianie podstawowych adresów URL obiektów multimedialnych dla kanału

1.  Otwórz portal Dynamics 365 for Retail HQ.
2.  Kliknij kolejno opcje **Handel detaliczny** &gt; **Ustawienia kanału** &gt; **Profile kanału**. [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  W profilu kanału używanym przez sklep dla MPOS zaktualizuj pole **Podstawowy adres URL obiektu multimedialnego**, wprowadzając podstawowy adres URL serwera multimediów lub CDN. Podstawowy adres URL jest pierwszą częścią adresu URL, który jest współużytkowany przez wszystkie foldery obrazów różnych jednostek.[![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definiowanie szablonu multimediów dla jednostki

1.  Kliknij kolejno opcje **Handel detaliczny** &gt; **Zarządzanie katalogiem** &gt; **Obrazy katalogu**.
2.  Na stronie **obrazów w katalogu** w okienku akcji kliknij **Definiuj szablon multimediów**. W oknie dialogowym **Definiuj szablon multimediów** w polu **Jednostka** **Katalog** powinien być wybrany domyślnie.
3.  Na skróconej karcie **Ścieżka do multimediów** wprowadź pozostałe ścieżki lokalizacji obrazu. Ścieżka do multimediów obsługuje **LanguageID** jako zmienną. Na przykład w przypadku danych demonstracyjnych, można utworzyć folder **katalogów** dla wszystkich obrazów w katalogu znajdujących się pod podstawowym adresem URL obiektów multimedialnych na serwerze multimediów (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Następnie można skonfigurować folder dla każdego języka, na przykład en US lub fr-FR i skopiować odpowiednie obrazy w każdym folderze. Jeśli nie masz różnych obrazów dla różnych języków, możesz pominąć zmienną **LanguageID** ze struktury folderu i przejść bezpośrednio do folderu katalogów zawierającego obrazy katalogu. **Uwaga:** aktualna wersja programu Dynamics 365 for Retail obsługuje token **{LanguageId}** dla jednostek Katalog, Produkt i Kategoria. (Token **{LanguageID}** nie jest obsługiwany dla jednostek Odbiorca i Pracownik, zgodna z istniejącym standardem począwszy systemu Microsoft Dynamics AX 6.x.)
4.  W przypadku obrazów format nazwy pliku jest na stałe zakodowany w nazwie katalogu i nie można go zmienić. W związku z tym należy zmienić nazwy obrazów, tak aby miały nazwy odpowiedniego katalogu, w celu zagwarantowania, że MPOS obsługuje je poprawnie.
5.  W polu **Rozszerzenie pliku** wybierz oczekiwane rozszerzenie nazwy pliku, w zależności od typu obrazów, które masz. Na przykład w przypadku danych demonstracyjnych, obrazy katalogu mają rozszerzenie .jpg. (Pliki obrazów są również zmieniane, tak aby miały nazwy katalogu).
6.  Kliknij przycisk **OK**
7.  Aby sprawdzić, czy szablon multimediów dla obrazów został zapisany poprawnie, na stronie **obrazów katalogu** kliknij ponownie **Definiuj szablon multimediów**. Aby sprawdzić szablon bez zamykania pola dialogowego **Definiuj szablon multimediów**, użyj skróconej karty **Generuj adresy URL obrazów dla programu Excel**. Sprawdź wygląd adresu URL obrazu wygląd i zobacz, czy adres URL jest zgodny ze standardem szablonu. Okno dialogowe **Definiuj szablon multimediów** okno ma teraz niejawnie ustawioną ścieżkę obrazu dla wszystkich obrazów katalogu używających tej wspólnej ścieżki adresu URL. Ta ścieżka URL dotyczy wszystkich obrazów z katalogu, chyba że zostaną zastąpione. Pierwsza część ścieżki obrazu jest pobierana z podstawowego adresu URL obiektu multimedialnego zdefiniowanego w profilu kanału. Pozostała część ścieżki pochodzi ze ścieżki zdefiniowanej w szablonie multimediów. Dwie części są tak łączone, by zawierały pełny adres URL lokalizacji obrazu. Na przykład, katalog w obrębie danych demonstracyjnych nosi nazwę Fabrikam Base Catalog. W związku z tym nazwa obrazu musi mieć postać Fabrikam Base Catalog.jpg (używa nazwy katalogu i rozszerzenia .jpg skonfigurowanych w szablonie). W takim przypadku po połączeniu, adres URL będzie miał postać https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Uruchom zadania synchronizacji, aby przesunąć nowy szablon do bazy danych kanału, tak aby MPOS mógł używać tego szablonu do uzyskania dostępu do obrazów.
9.  Aby zaktualizować szablon multimediów dla obrazów w katalogu po stronie kanału, uruchom zadanie **Catalog Job 1150** z okna **Dane IT sieci sprzedaży** &gt; **Harmonogram dystrybucji**.[![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Wyświetlenie podglądu obrazu na poziomie jednostki
1.  Ze strony jednostki pozycji w HQ można wyświetlić podgląd obrazu, który używa adresu URL obrazu, który został utworzony na podstawie szablonu multimediów. Na przykład przejdź do odpowiedniego katalogu, a następnie w okienku akcji kliknij kolejno opcje **Multimedia** &gt; **Obrazy**. Z listy rozwijanej wybierz różne sklepy, które mogą mieć inne profile kanału.
2.  Aby edytować lub usunąć niejawny szablon multimediów, wróć do pola dialogowego **Definiuj szablon multimediów** na stronie **obrazów w katalogu**.
3.  Można użyć przycisków **Dodaj** i **Usuń**, aby ręcznie zmienić ścieżkę na podstawie niejawnego szablonu, używaną do określonego obrazu. Aby uzyskać więcej informacji zobacz sekcję "Zastępowaniu szablonu multimediów dla pozycji jednostki" w dalszej części tego artykułu.
4.  Po przejrzeniu obrazu i wprowadzeniu zmian uruchom wystąpienie programu MPOS dla odpowiedniego sklepu i zobacz, czy zostaną wyświetlone obrazy z katalogu.[![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Uwaga:** możesz użyć tej samej procedury dla wszystkich pięciu obsługiwanych jednostek: Pracownik, Odbiorca, Katalog, Kategoria i Produkty. „Produkty katalogu” (produkty, które są ustawione na poziomie katalogu) i „Produkty kanału” (produkty, które są ustawione na poziomie kanału) używają szablonu multimediów ustawionego dla jednostki Produkty. W przypadku szablonu multimediów produktów można wybrać liczbę wyświetlanych obrazów dla każdego produktu. Można również ustawić domyślny obraz dla danego produktu. W ten sposób można zapobiec wyświetlaniu pustych obrazów w MPOS i kontrolować, które obrazy będą używane jako domyślne dla produktu. W poniższym przykładzie każdy produkt ma pięć obrazów, a pierwszy obraz jest ustawiony jako domyślny. Produkty z wariantami są traktowane w taki sam sposób jak produkty główne. Nazwa pliku dla pliku obrazu powinna opierać się na numerze produktu. Niektóre znaki są również usuwane, gdy generowana jest nazwa pliku. Dlatego warto sprawdzić nazwę pliku w sekcji **generowanie adresów URL obrazu dla programu Excel**. [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Zadania synchronizacji do wysyłania szablonu multimediów do kanału
Dla wszystkich pięciu obsługiwanych jednostek (pracownika, odbiorcy, katalogu, kategorii i produktów) przy każdej aktualizacji okna dialogowego **Definiuj szablon multimediów** w celu ustawienia obrazu pamiętaj o uruchomieniu zadania Catalog job (1150) z okna **Dane IT sieci sprzedaży** &gt; **Harmonogram dystrybucji**. To zadanie umożliwi zsynchronizowanie zaktualizowanego szablonu multimediów w kanale i używanie go przez MPOS. Uruchom zadanie Catalog job (1150) po dokonaniu dowolnych z następujących zmian:

-   Aby zaktualizować szablon multimediów obrazu z katalogu, przejdź do okna **Obrazy katalogu** &gt; **Definiuj szablon multimediów**.
-   Aby zaktualizować szablon multimediów obrazu pracownika, przejdź do okna **Obrazy pracowników** &gt; **Definiuj szablon multimediów**.
-   Aby zaktualizować szablon multimediów obrazu odbiorcy, przejdź do okna **Obrazy odbiorcy** &gt; **Definiuj szablon multimediów**.
-   Aby zaktualizować szablon multimediów obrazu produktu, przejdź do menu **Obrazy produktu** &gt; **Definiuj szablon multimediów**.
-   Aby zaktualizować szablon multimediów obrazu kategorii, przejdź do okna **Obrazy kategorii** &gt; **Definiuj szablon multimediów**. Należy również opublikować kanał.

## <a name="overwriting-the-media-template-for-entity-items"></a>Zastępowanie szablonu multimediów dla pozycji jednostki
Jak wiesz z poprzedniej sekcji, szablon multimediów dla danej jednostki obsługuje tylko jedna wspólną ścieżkę. Ta ścieżka opiera się na skonfigurowanym podstawowym adresie URL obiektu multimedialnego i określonej ścieżce multimediów. Jednak w wielu przypadkach sprzedawcy chcą używać obrazów pochodzących z różnych źródeł dla podzbioru pozycji w jednostce. Na przykład sklep używa własnego serwera multimediów dla jednego zestawu obrazów z katalogu, ale dla innego zestawu obrazów używa adresów URL z sieci CDN. Aby zastąpić adresy URL obrazu oparte na szablonie multimediów dla obrazów jednostki na poziomie jednostki, można użyć opcji Edytuj w programie Excel i Edycja ręczna na stronie **podglądu**.

### <a name="overwrite-by-using-edit-in-excel"></a>Zastępowanie za pomocą edycji w programie Excel

1.  Kliknij kolejno opcje **Handel detaliczny** &gt; **Zarządzanie katalogiem** &gt; **Obrazy katalogu**.
2.  Na stronie **obrazów w katalogu** 
kliknij **Definiuj szablon multimediów**. W oknie dialogowym **Definiuj szablon multimediów** w polu **Jednostka** powinien być wybrany **Katalog**.
3.  Na skróconej karcie **Ścieżka do multimediów** sprawdź lokalizację obrazu.
4.  Na skróconej karcie **generowanie adresów URL obrazu dla programu Excel** kliknij **Generuj**. **Ważne:** po każdej zmianie szablonu multimediów należy kliknąć opcję **generowania** przed użyciem edycji programu Excel. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Teraz widać podgląd adresów URL obrazów wygenerowanych na podstawie ostatnio zapisanej wersji szablonu multimediów. [![excel2](./media/excel2.png)](./media/excel2.png) **Uwaga:** Adresy URL, które są generowane dla programu Excel, używają ścieżki i konwencji szablonu multimediów, który jest zdefiniowany. Konwencje te obejmują konwencje nazewnictwa plików. Oczekuje się, że masz już zestaw obrazów fizycznych poza programem Dynamics 365 for Retail, a obrazy mogą być pobierane z adresów URL, które pochodzą ze zdefiniowanego wcześniej szablonu multimediów. Możesz zastąpić te adresy URL przy użyciu funkcji edycji programu Excel.
5.  Kliknij **Edytuj w programie Excel**.
6.  Po otworzeniu arkusza programu Microsoft Excel kliknij przycisk **Włącz edytowanie**, gdy zobaczysz monit.
7.  Gdy zostanie wyświetlony monit, kliknij przycisk **Zaufaj temu dodatkowi** w prawym okienku i poczekaj na zakończenie instalacji dodatku. [![Zaufaj temu dodatkowi](./media/excel4.jpg)](./media/excel4.jpg)
8.  Jeśli zostanie wyświetlony monit o logowanie, wprowadź poświadczenia użyte do zarejestrowania się do HQ. [![Monit o zalogowanie się](./media/excel5.png)](./media/excel5.png)
9.  Po zalogowaniu można wyświetlić listę adresów URL obrazu dla poszczególnych pozycji w katalogu.
10. Można edytować, dodawać i usuwać adresy URL obrazu dla różnych pozycji jednostek.
11. Można zastąpić adresy URL obrazów dla wszystkich jednostek poza produktami. Modyfikuj istniejący adres URL obrazu tak, aby używał nowego docelowego adresu URL obrazu, i zaktualizuj nazwę pliku, podając nową nazwę pliku dla pliku obrazu. Nazwa pliku musi być unikatowa w celu zagwarantowania, że rekord jest unikatowy. [![Zastępowanie adresów URL obrazów w programie Excel](./media/excel6.jpg)](./media/excel6.jpg) **Uwaga:** Podczas zastępowania adresów URL obrazów dla jednostek produktów za pomocą funkcji Edytuj w programie Excel lub strony pozycji jednostki aplikacja MPOS zawsze pokazuje wszystkie adresy URL obrazów z szablonu multimediów wraz z zastąpionymi adresami URL obrazów.
12. Po zakończeniu wprowadzania zmian kliknij przycisk **publikowania w programie Excel**, aby utworzyć nowy wpis jawnego skojarzenia.
13. Wróć do HQ i kliknij przycisk **OK**.
14. Uruchom odpowiednie zadania synchronizacji dla jednostki i sprawdź podgląd na stronie jednostki lub w MPOS.

#### <a name="creating-new-records"></a>Tworzenie nowego rekordu

Można tworzyć nowe rekordy w programie Excel. Ale upewnij się, że podajesz poprawne informacje. Na przykład aby utworzyć nowy wpis dla katalogu, upewnij się, czy ID i nazwa katalogu są prawidłowe oraz podaj niepowtarzalną nazwę pliku. Niepowtarzalna nazwa pliku jest bardzo ważna, ponieważ podczas publikowania sprawdzana jest unikatowość rekordów w programie Excel. Najpierw skopiuj szczegóły z katalogu, w którym chcesz utworzyć nowy rekord, a następnie skopiuj rekord. Wystarczy zaktualizować tylko nazwę pliku i URL, bo pozostałe informacje będą takie same. Aby utworzyć nowe rekordy dla pozycji jednostki Produkt, użyj tej samej podstawowej procedury. Z arkusza programu Excel skopiuj istniejący rekord produktu, dla którego chcesz utworzyć nowy rekord, a następnie zastąp URL obrazu i nazwę pliku. Upewnij się, że nazwa pliku jest unikatowa.

#### <a name="deleting-an-existing-record"></a>Usuwanie istniejącego rekordu

Można usunąć tylko zastąpione rekordy URL obrazu. Po usunięciu obrazu i zakończeniu synchronizacji, obraz nie będzie już wyświetlany na stronie **podglądu**, ani w MPOS. Nie można usunąć rekordów adresu URL obrazu, które pochodzą z szablonu multimediów, ponieważ te rekordy zawsze pochodzą z szablonu multimediów.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Zastępowanie na stronie podglądu na poziomie jednostki

Dla wszystkich jednostek za wyjątkiem produktów można zastąpić adres URL obrazu dla danej pozycji jednostki na poziomie pozycji jednostki na stronie **podglądu**. W przypadku produktów możesz użyć strony jednostki „Produkty z katalogu”. W tym przykładzie pokazano, jak zastąpić obraz z katalogu.

1.  Kliknij kolejno opcje **Katalogi** &gt; **Multimedia** &gt; **Obrazy** i wybierz obraz katalogu do zaktualizowania.
2.  Kliknij **Dodaj**, a następnie wprowadź adres URL obrazu, aby zastąpić adres URL szablonu multimediów.
3.  Jeśli chcesz, aby ten obraz był wyświetlany w MPOS dla katalogu, możesz go zapisać jako domyślny.
4.  Kliknij przycisk **OK** Adres URL obrazu jest aktualizowany dla tego obrazu z katalogu i zostanie wyświetlony podgląd. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Możesz także wyświetlić podgląd obrazu dla wszystkich zastąpionych adresów URL obrazu na stronie galerii **obrazów w katalogu**.

**[![preview-4](./media/preview-4.png)](./media/preview-4.png)Uwaga:** Obecnie galeria nie pokazuje podglądów obrazów dla adresów URL obrazów z szablonu multimediów. W przypadku Katalogu, Pracownika, Odbiorcy i Kategorii, jeśli użytkownik jawnie ustala URL na tej stronie, zalecamy wskazanie obrazu domyślnego, ponieważ oprogramowanie klienckie usługi Retail Server pokazuje tylko po jednym obrazie na Katalog, Odbiorcę, Pracownika i Kategorię. Jeśli użytkownik nie określi domyślnego obrazu, system określa domyślny obraz i wysyła go do aparatu wywołaniu usługi Retail Server (MPOS lub handel elektroniczny).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Zastępowanie adresu URL obrazu dla obrazu produktu z katalogu na stronie podglądu.

Aby zastąpić adresy URL obrazu dla obrazów produktu z katalogu, trzeba użyć strony **podglądu**. Nie można tego zrobić przy użyciu funkcji edycji programu Excel.

1.  Aby zastąpić obrazy produktów na poziomie katalogu, wybierz katalog, a następnie wybierz produkt, którego obraz chcesz zastąpić.
2.  Kliknij opcję **Atrybuty**.
3.  Na następnej stronie wybierz **Obraz** i kliknij **Edytuj**. Strona **Podgląd** otworzy się jako przesuwane okno dialogowe.
4.  Kliknij **Dodaj** i zastąp adres URL obrazu przy użyciu nowego adresu URL.
5.  Kliknij przycisk **OK** Teraz widać podgląd nowego obrazu i można go ustawić jako domyślny.

**[![cat3](./media/cat3.png)](./media/cat3.png)Uwaga:** Po skojarzeniu obrazu kategorii należy opublikować kanał i włączyć zadanie kanału w celu zagwarantowania opublikowania zmian w bazie danych kanału.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Konfigurowanie obrazów do wyświetlania w trybie offline w MPOS
MPOS można uruchomić w trybie Online (w przypadku MPOS połączonych z serwerem sieci sprzedaży) lub w trybie Offline (jeśli nie ma serwera sieci sprzedaży lub nie ma połączenia z internetem, a transakcje są przechowywane offline w lokalnej bazie danych). Jeśli MPOS działa w trybie Offline, go nie można pobrać obrazów z zewnętrznego serwera, ponieważ połączenie z serwerem sprzedaży detalicznej zostało zerwane. Ale nadal można skonfigurować obrazy, tak aby były wyświetlane po przejściu MPOS w tryb Offline.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Konfigurowanie obrazów produktów do wyświetlania w trybie offline w MPOS

Obrazy produktu, które muszą być używane w trybie Offline, można skonfigurować poprzez przesłanie odpowiedniego obrazu fizycznego do obrazu podstawowego produktu.

1.  Kliknij kolejno opcje **Zarządzanie informacjami o produktach** &gt; **Produkty** &gt; **Produkty**.
2.  Wybierz produkt, aby ustawić dla niego obraz w trybie offline.
3.  Kliknij **Edytuj**, a następnie kliknij strzałkę w prawym rogu ekranu, aby wyświetlić prawe okienko.
4.  Na skróconej karcie **obraz produktu** kliknij przycisk **Zmień obraz** i prześlij fizyczny obraz, który ma być używany dla wybranego produktu w trybie Offline.
5.  Zapisz i zamknij stronę.
6.  Mimo że MPOS jest w trybie Online, należy uruchomić zadanie katalogu w HQ, aby upewnić się, że dane zostały przesłane co najmniej jeden raz do bazy danych offline.
7.  Umieść MPOS w trybie Offline. Powinien być widoczny obraz przesłany dla określonego produktu w HQ. [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Ustawianie obrazów katalogu, kategorii, pracownika i odbiorcy do wyświetlania w trybie Offline dla MPOS

Obrazy katalogu, pracownika, odbiorcy i kategorii, które muszą być używane w trybie Offline, można ustawić poprzez dodanie do galerii wymaganego łącza docelowego obrazu oraz ustawienie obrazu jako domyślnego dla wybranej jednostki.

1.  Przejdź do katalogu, a następnie w okienku akcji kliknij kolejno opcje **Multimedia** &gt; **Obrazy**.
2.  Postępuj zgodnie z instrukcjami w sekcji „**Zastępowanie na stronie podglądu na poziomie jednostki**”, aby dodać adres URL obrazu zewnętrznego.
3.  Oznacz ten obraz jako domyślny dla katalogu, zaznaczając pole wyboru obok obrazu w siatce.
4.  Uruchom zadanie katalogu. Ten obraz będzie teraz używany jako obraz w trybie Offline dla tego katalogu w MPOS.
5.  Należy wykonać podobną procedurę dla kategorii, pracownika i odbiorcy.

[![offline2](./media/offline2.png)](./media/offline2.png)    



