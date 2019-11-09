---
title: Ukrywanie metod dostawy bez przewoźnika z poziomu opcji wysyłki w punkcie sprzedaży
description: W tym temacie opisano opcję konfiguracji, która może zapobiegać wyświetlaniu metod dostawy bez przewoźnika podczas tworzenia zamówień wysyłek w aplikacji punktu sprzedaży.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659028"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="3a2c1-103">Ukrywanie metod dostawy bez przewoźnika z poziomu opcji wysyłki w punkcie sprzedaży</span><span class="sxs-lookup"><span data-stu-id="3a2c1-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3a2c1-104">W tym temacie opisano opcję konfiguracji dostępną dla aplikacji punktu sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="3a2c1-105">Ta opcja konfiguracji umożliwia zmianę zachowania wyboru metody dostawy podczas tworzenia zamówień wysyłki w punkcie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="3a2c1-106">Użytkownicy tworzący zamówienia wysyłki klienta w punkcie sprzedaży mogą wybrać metodę dostawy dla wysyłki.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="3a2c1-107">Ta funkcja jest dostępna bez względu na to, czy wysyłane jest całe zamówienie, czy tylko wybrane wiersze.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="3a2c1-108">Domyślnie okno dialogowe, w którym jest wybierana metoda dostawy, zawiera wszystkie prawidłowe metody dostawy dla kombinacji kanału, pozycji i adresu dostawy.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="3a2c1-109">Te metody dostawy są definiowane na stronie **Metody dostawy** w programie Retail Headquarters (**Sprzedaż i marketing \> Ustawienia \> \> Metody dostawy**).</span><span class="sxs-lookup"><span data-stu-id="3a2c1-109">These modes of delivery are defined on the **Modes of delivery** page in Retail Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="3a2c1-110">Metody dostawy bez przewoźnika, takie jak **Wyniesienie** lub **Pobranie**, mogą również pojawiać się w oknie dialogowym jako opcje do wyboru.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="3a2c1-111">Dodaliśmy jednak funkcję umożliwiającą ukrywanie metod dostawy bez przewoźnika w oknie dialogowym.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="3a2c1-112">Aby włączyć tę funkcję, na stronie **Parametry sieci sprzedaży** na karcie **Zamówienia odbiorców** ustaw opcję **Pokazuj tylko opcje metod z przewoźnikiem na potrzeby wysyłania zamówień** na **Tak**.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-112">To turn on this feature, on the **Retail parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="3a2c1-113">Po włączeniu tej funkcji i uruchomieniu odpowiednich zadań dystrybucji w celu zsynchronizowania informacji z bazą danych kanału metody dostawy bez przewoźnika nie będą wyświetlane podczas procesu tworzenia zamówień wysyłki w punkcie sprzedaży.</span><span class="sxs-lookup"><span data-stu-id="3a2c1-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>