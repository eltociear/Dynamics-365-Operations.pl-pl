---
title: Magazyn kopii zapasowej szablonów ER
description: W tym temacie objaśniono sposób korzystania z magazynu kopii zapasowej modułu raportowanie elektroniczne (ER) w celu odzyskania szablonów.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 932ba44b4223bf9c9d93ffb19e17f6e57bb303b5
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553098"
---
# <a name="backup-storage-of-er-templates"></a><span data-ttu-id="5f54b-103">Magazyn kopii zapasowej szablonów ER</span><span class="sxs-lookup"><span data-stu-id="5f54b-103">Backup storage of ER templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f54b-104">Użytkownicy biznesowi używają [modułu Raportowanie elektroniczne (ER)](general-electronic-reporting.md), który umożliwia użytkownikom biznesowym konfigurowanie formatów dokumentów wychodzących zgodnie z wymogami prawnymi obowiązującymi w różnych krajach i regionach.</span><span class="sxs-lookup"><span data-stu-id="5f54b-104">The [Electronic reporting (ER) framework](general-electronic-reporting.md) lets business users configure formats for outbound documents according to the legal requirements of various countries and regions.</span></span> <span data-ttu-id="5f54b-105">W skonfigurowanych formatach ER można używać wstępnie zdefiniowanych szablonów do generowania dokumentów wychodzących w różnych formatach, takich jak Microsoft Excel skoroszyty, Microsoft Word dokumenty i dokumenty PDF.</span><span class="sxs-lookup"><span data-stu-id="5f54b-105">Configured ER formats can use predefined templates to generate outbound documents in various formats, such as Microsoft Excel workbooks, Microsoft Word documents, or PDF documents.</span></span> <span data-ttu-id="5f54b-106">W szablonach są wypełnione dane, których wymaga skonfigurowany przepływ danych dla generowanych dokumentów.</span><span class="sxs-lookup"><span data-stu-id="5f54b-106">The templates are filled with data that the configured dataflow for generated documents requires.</span></span>

<span data-ttu-id="5f54b-107">Każdy skonfigurowany format może zostać opublikowany jako część rozwiązania ER.</span><span class="sxs-lookup"><span data-stu-id="5f54b-107">Each configured format can be published as part of an ER solution.</span></span> <span data-ttu-id="5f54b-108">Każde rozwiązanie ER można wyeksportować z jednego wystąpienia Finance and Operations i importować do innego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5f54b-108">Each ER solution can be exported from one instance of Finance and Operations and imported into another instance.</span></span>

<span data-ttu-id="5f54b-109">Struktura ER używa [Struktury zarządzania dokumentami](../../fin-ops/organization-administration/configure-document-management.md) w celu zachowania wymaganych szablonów bieżącego wystąpienia Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f54b-109">The ER framework uses the [Document management framework](../../fin-ops/organization-administration/configure-document-management.md) to keep the required templates for the current Finance and Operations instance.</span></span> <span data-ttu-id="5f54b-110">W zależności od ustawień struktury ER, można wybrać folder Microsoft Azure Magazyn obiektów BLOB lub folder Microsoft SharePoint jako fizyczną lokalizację magazynu podstawowego dla szablonów.</span><span class="sxs-lookup"><span data-stu-id="5f54b-110">Depending on the settings of the ER framework, Microsoft Azure Blob storage or a Microsoft SharePoint folder can be selected as the physical primary storage location for templates.</span></span> <span data-ttu-id="5f54b-111">(Aby uzyskać więcej informacji, należy zapoznać się ztematem [Konfigurowanie struktury ER](electronic-reporting-er-configure-parameters.md).) Tabela DocuValue zawiera pojedynczy rekord dla każdego szablonu.</span><span class="sxs-lookup"><span data-stu-id="5f54b-111">(For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).) The DocuValue table holds an individual record for each template.</span></span> <span data-ttu-id="5f54b-112">W każdym rekordzie pole **Informacje dotyczące dostępu** zawiera ścieżkę pliku szablonu, który znajduje się w skonfigurowanej lokalizacji magazynu.</span><span class="sxs-lookup"><span data-stu-id="5f54b-112">In each record, the **AccessInformation** field stores the path of a template file that is located in the configured storage location.</span></span>

<span data-ttu-id="5f54b-113">Podczas zarządzania wystąpieniami Finance and Operations można zdecydować, czy bieżące wystąpienie ma być migrowane do innej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5f54b-113">When you manage your Finance and Operations instances, you might decide to migrate the current instance to another location.</span></span> <span data-ttu-id="5f54b-114">Na przykład wystąpienie produkcji można migrować do nowego środowiska piaskownicy.</span><span class="sxs-lookup"><span data-stu-id="5f54b-114">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="5f54b-115">Jeśli struktura ER jest skonfigurowana do przechowywania szablonów w magazynie obiektów BLOB, tabela DocuValue w nowym środowisku piaskownicy odwołuje się do wystąpienia magazynu obiektów BLOB w środowisku produkcyjnym.</span><span class="sxs-lookup"><span data-stu-id="5f54b-115">If you configured the ER framework to store templates in Blob storage, the DocuValue table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="5f54b-116">Jednak nie można uzyskać dostępu do tego wystąpienia ze środowiska piaskownicy, ponieważ proces migracji nie obsługuje migracji artefaktów w magazynie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="5f54b-116">However, this instance can't be accessed from the sandbox environment, because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="5f54b-117">Dlatego w przypadku próby uruchomienia formatu ER, który używa szablonu do generowania dokumentów biznesowych, wystąpi wyjątek i użytkownik jest powiadamiany o brakujący szablon.</span><span class="sxs-lookup"><span data-stu-id="5f54b-117">Therefore, if you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="5f54b-118">Użytkownik ma również możliwość użycia narzędzia do oczyszczania w celu usunięcia, a następnie ponownego zaimportowania konfiguracji formatu ER, która zawiera szablon.</span><span class="sxs-lookup"><span data-stu-id="5f54b-118">You're also guided to use the ER cleanup tool to delete and then re-import the ER format configuration that contains the template.</span></span> <span data-ttu-id="5f54b-119">Ponieważ może być kilka konfiguracji formatu ER, ten proces może być czasochłonny.</span><span class="sxs-lookup"><span data-stu-id="5f54b-119">Because you might have several ER format configurations, this process can be time consuming.</span></span>

<span data-ttu-id="5f54b-120">Przechowywanie kopii zapasowych w module szablony ER ułatwia tworzenie szablonów w taki sposób, aby były one zawsze dostępne do generowania dokumentów biznesowych.</span><span class="sxs-lookup"><span data-stu-id="5f54b-120">The Backup storage of ER templates feature can help you make your templates so that they are always available to generate business documents.</span></span>

> [!NOTE]
> <span data-ttu-id="5f54b-121">Tej funkcji można używać tylko wtedy, gdy w magazynie obiektów BLOB wybrano lokalizację magazynu fizycznego dla szablonów ER systemu.</span><span class="sxs-lookup"><span data-stu-id="5f54b-121">This feature can be used only when Blob storage has been selected as the physical storage location for ER templates.</span></span>

<span data-ttu-id="5f54b-122">W przypadku tej funkcji każdy szablon nowej konfiguracji formatu modułu ER w bieżącym środowisku jest automatycznie zapisywany w lokalizacji magazynu kopii zapasowej dla szablonów (tabela bazy danych ERDocuDatabaseStorage) po wystąpieniu następujących zdarzeń:</span><span class="sxs-lookup"><span data-stu-id="5f54b-122">For this feature, every template of a new ER format configuration in the current environment is automatically saved to the backup storage location for templates (the ERDocuDatabaseStorage database table) when the following events occur:</span></span>

- <span data-ttu-id="5f54b-123">Zaimportuje się nową konfigurację formatu ER, która zawiera szablon.</span><span class="sxs-lookup"><span data-stu-id="5f54b-123">You import a new ER format configuration that contains a template.</span></span>
- <span data-ttu-id="5f54b-124">Użytkownik wykona wersję roboczą konfiguracji formatu w formacie ER, która zawiera szablon.</span><span class="sxs-lookup"><span data-stu-id="5f54b-124">You complete the draft version of an ER format configuration that contains a template.</span></span>

<span data-ttu-id="5f54b-125">Kopie zapasowe szablonów są migrowane do nowego wystąpienia Finance and Operations jako część bazy danych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5f54b-125">Backup copies of templates are migrated to a new instance of Finance and Operations as part of the application database.</span></span>

<span data-ttu-id="5f54b-126">Jeśli do generowania dokumentów wychodzących jest wymagany szablon formatu ER, w celu przetwarzania płatności dostawców, takich jak generowanie raportów zawiadomienia o płatności i raporty kontrolne, na przykład nie można odnaleźć wymaganego szablonu w lokalizacji magazynu głównego, należy wykonać następujące czynności: zdarzenia:</span><span class="sxs-lookup"><span data-stu-id="5f54b-126">If a template of an ER format is required for generation of outbound documents, to process vendor payments including generation of payment advice and control reports, for example, but the required template isn't found in the primary storage location, the following events occur:</span></span>

- <span data-ttu-id="5f54b-127">Jeśli szablon jest dostępny w lokalizacji magazynu kopii zapasowej, zostanie on automatycznie pobrany z lokalizacji magazynu kopii zapasowej, przywrócony do lokalizacji głównego magazynu i użyty w bieżącym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="5f54b-127">If the template is available in the backup storage location, it is automatically taken from the backup storage location, restored to the primary storage location, and used for the current execution.</span></span>
- <span data-ttu-id="5f54b-128">Każdy użytkownik przypisany do roli **dewelopera raportowania elektronicznego** lub **administratora systemu** jest powiadamiany o braku wydawanych szablonów za pośrednictwem centrum akcji.</span><span class="sxs-lookup"><span data-stu-id="5f54b-128">Every user who is assigned to the **Electronic reporting developer** or **System administrator** role is notified about the missing template issue through the Action center.</span></span> <span data-ttu-id="5f54b-129">Wyświetlany komunikat zależy od wartości parametru **automatycznego uruchomienia procedury przywracania uszkodzonych szablonów w partii**:</span><span class="sxs-lookup"><span data-stu-id="5f54b-129">The message that appears depends on the value of the **Automatically run the procedure of restoring the broken templates in batch** parameter:</span></span>

    - <span data-ttu-id="5f54b-130">Jeśli ten parametr jest **wyłączony**, komunikat zaleca uruchomienie procesu wsadowego w celu automatycznego rozwiązania podobnych problemów w odniesieniu do innych szablonów konfiguracji w formacie ER.</span><span class="sxs-lookup"><span data-stu-id="5f54b-130">If this parameter is set to **Off**, the message recommends that you start the batch process to automatically fix similar issues for other ER format configuration templates.</span></span> <span data-ttu-id="5f54b-131">Wiadomość zawiera łącze, które można wykorzystać do uruchomienia procesu wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5f54b-131">The message includes a link that you can use to start the batch process.</span></span>
    - <span data-ttu-id="5f54b-132">Jeśli ten parametr jest skonfigurowany jako **włączony**, komunikat powiadamia, że wykryto błąd brakujących szablonów i że nowy proces przetwarzania wsadowego, **przywrócenie przerwanych szablonów z wewnętrznej kopii zapasowej bazy danych** został automatycznie zaplanowane.</span><span class="sxs-lookup"><span data-stu-id="5f54b-132">If this parameter is set to **On**, the message notifies you that a missing templates issue has been discovered, and that a new batch process, **Restore broken templates from internal database backup**, has been automatically scheduled.</span></span> <span data-ttu-id="5f54b-133">Ten proces wsadowy spowoduje automatyczne rozwiązanie podobnych problemów dla innych szablonów.</span><span class="sxs-lookup"><span data-stu-id="5f54b-133">This batch process will automatically fix similar issues for other templates.</span></span>

<span data-ttu-id="5f54b-134">Aby ustawić parametr **automatycznego uruchomienia procedury przywracania uszkodzonych szablonów w partii**, wykonaj kroki:</span><span class="sxs-lookup"><span data-stu-id="5f54b-134">To set up the he **Automatically run the procedure of restoring the broken templates in batch** parameter, complete the following steps:</span></span>

1. <span data-ttu-id="5f54b-135">W module Finance and Operations przejdź do opcji **Administrowanie organizacją \> Raportowanie elektroniczne \> Strona Konfiguracje**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-135">In Finance and Operations, open the **Organization administration \> Electronic reporting \> Configurations page**.</span></span>
2. <span data-ttu-id="5f54b-136">Na stronie **Konfiguracje** w okienku akcji na karcie **Konfiguracje** w grupie **Ustawienia zaawansowane** wybierz opcję **Parametry użytkownika**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-136">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="5f54b-137">W oknie dialogowym **parametry użytkownika** określ wymaganą wartość parametru **automatycznego uruchamiania procedury przywracania uszkodzonych szablonów w partii**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-137">In the **User parameters** dialog box, set the required value for the **Automatically run the procedure of restoring the broken templates in batch** parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="5f54b-138">Ten parametr jest definiowany jako użytkownik aplikacji i jest rejestrowana właściwa firma.</span><span class="sxs-lookup"><span data-stu-id="5f54b-138">This parameter is defined as application user and logged company specific.</span></span>

![Strona konfiguracji raportowania elektronicznego](./media/GER-BackupTemplates-1.png)

<span data-ttu-id="5f54b-140">Na poniższej ilustracji pokazano przykład komunikatu wyświetlanego po **automatycznym uruchomieniu procedury przywracania uszkodzonych szablonów w parametrze wsadowym** jest ustawiony jako **włączony**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-140">The following illustration shows an example of the message that appears when the **Automatically run the procedure of restoring the broken templates in batch** parameter is set to **On**.</span></span>

![Strona arkusza płatności dostawcy](./media/GER-BackupTemplates-2.png)

<span data-ttu-id="5f54b-142">Na poniższej ilustracji przedstawiono proces wsadowy **Przywracanie zepsutych szablonów z wewnętrznej kopii zapasowej bazy danych** na stronie **zadanie wsadowe**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-142">The following illustration shows the **Restore broken templates from internal database backup** batch process on the **Batch job** page.</span></span>

![Strona zadania wsadowe](./media/GER-BackupTemplates-3.png)

<span data-ttu-id="5f54b-144">Dziennik wykonania zakończonego procesu wsadowego **Przywracanie zepsutych szablonów z wewnętrznej kopii zapasowej bazy danych** zawiera informacje o szablonach przywróconych z lokalizacji magazynu kopii zapasowej w lokalizacji magazynu głównego.</span><span class="sxs-lookup"><span data-stu-id="5f54b-144">The execution log of the completed **Restore broken templates from internal database backup** batch process includes information about the templates that have been restored from the backup storage location to the primary storage location.</span></span>

![Strona historii zadań wsadowych](./media/GER-BackupTemplates-4.png)

<span data-ttu-id="5f54b-146">Domyślnie jest włączany proces automatycznego tworzenia kopii zapasowych szablonów znajdujących się w konfiguracjach formatu ER.</span><span class="sxs-lookup"><span data-stu-id="5f54b-146">By default, the process of automatically creating backup copies of templates that reside in ER format configurations is turned on.</span></span> <span data-ttu-id="5f54b-147">Aby zatrzymać tworzenie kopii zapasowych szablonów, należy skonfigurować opcję **Zatrzymaj tworzenie kopii zapasowych szablonu** na **tak** na karcie **Załączniki** na stronie **Parametry elektronicznego reportowania**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-147">To stop making backup copies of templates, set the **Stop making backup copies of template** option to **Yes** on the **Attachments** tab of the **Electronic reporting parameters** page.</span></span> <span data-ttu-id="5f54b-148">Tę stronę można otworzyć z obszaru roboczego **Raportowanie elektroniczne**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-148">You can open this page from the **Electronic reporting** workspace.</span></span>

<span data-ttu-id="5f54b-149">Jeśli dla opcji **Zatrzymaj tworzenie kopii zapasowych szablonów** ustawiono wartość **tak** i nie chcesz przechowywać kopii zapasowych poprzednio utworzonych szablonów, wybierz opcję **Oczyść magazyn kopii zapasowych** na stronie **Parametry raportowania elektronicznego**.</span><span class="sxs-lookup"><span data-stu-id="5f54b-149">If you set the **Stop making backup copies of templates** option to **Yes** and don't want to keep the backup copies that were previously made of templates, select **Clean up backup storage** on the **Electronic reporting parameters** page.</span></span>

<span data-ttu-id="5f54b-150">Jeśli środowisko zostało uaktualnione do Finance and Operations wersji operacyjnych 10.0.5 (październik 2019), a użytkownik chce przeprowadzić migrację do nowego środowiska zawierającego konfiguracje formatu ER, które można uruchomić, należy wybrać opcję **Wypełnij w magazynie kopii zapasowych** na stronie **Parametry raportowania elektronicznego** przed migracją.</span><span class="sxs-lookup"><span data-stu-id="5f54b-150">If you upgraded your environment to Finance and Operations version 10.0.5 (October 2019) and want to migrate to a new environment that includes ER format configurations that can be run, select **Fill in backup storage** on the **Electronic reporting parameters** page before the migration occurs.</span></span> <span data-ttu-id="5f54b-151">Kliknięcie tego przycisku powoduje uruchomienie procesu tworzenia kopii zapasowych wszystkich dostępnych szablonów, dzięki czemu można je przechowywać w lokalizacji magazynu kopii zapasowych ER dla szablonów.</span><span class="sxs-lookup"><span data-stu-id="5f54b-151">This button starts the process of making backup copies of all available templates, so that they can be stored in the ER backup storage location for templates.</span></span>

![Strona parametrów raportowania elektronicznego](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a><span data-ttu-id="5f54b-153">Obsługiwane wdrożenia</span><span class="sxs-lookup"><span data-stu-id="5f54b-153">Supported deployments</span></span>

<span data-ttu-id="5f54b-154">W module Finance and Operations w wersji 10.0.5 funkcja magazynowania kopii zapasowych szablonów ER jest dostępna tylko w wdrożeniach w chmurze.</span><span class="sxs-lookup"><span data-stu-id="5f54b-154">In Finance and Operations version 10.0.5, the Backup storage of ER templates feature is available only in cloud deployments.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f54b-155">Dodatkowe zasoby</span><span class="sxs-lookup"><span data-stu-id="5f54b-155">Additional resources</span></span>

[<span data-ttu-id="5f54b-156">Omówienie raportowania elektronicznego</span><span class="sxs-lookup"><span data-stu-id="5f54b-156">Electronic reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5f54b-157">Konfigurowanie struktury modułu Raportowanie elektroniczne</span><span class="sxs-lookup"><span data-stu-id="5f54b-157">Configure the Electronic reporting framework</span></span>](electronic-reporting-er-configure-parameters.md)