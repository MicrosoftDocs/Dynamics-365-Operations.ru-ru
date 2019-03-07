---
title: Настройка кодов методов обработки
description: Эта процедура заключается в настройке кода метода обработки, который можно использовать на мобильном устройстве для процесса получения заказа на возврат.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "324131"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="f0515-103">Настройка кодов методов обработки</span><span class="sxs-lookup"><span data-stu-id="f0515-103">Set up dispositions codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0515-104">Эта процедура заключается в настройке кода метода обработки, который можно использовать на мобильном устройстве для процесса получения заказа на возврат.</span><span class="sxs-lookup"><span data-stu-id="f0515-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="f0515-105">Коды методов обработки — это коллекция правил, которые можно использовать получении номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f0515-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="f0515-106">Например, если пользователь работы использует мобильное устройство для получения поврежденных номенклатур, пользователь должен отсканировать код метода обработки для поврежденных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f0515-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="f0515-107">По отсканированному коду метода обработки можно определить статус складских запасов полученных товаров, шаблон работы и директиву места хранения.</span><span class="sxs-lookup"><span data-stu-id="f0515-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="f0515-108">Для процесса получения заказа на покупку и процесса приемки производственного заказа использование кода метода обработки обязательным не является.</span><span class="sxs-lookup"><span data-stu-id="f0515-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="f0515-109">Для процесса получения возврата заказа на продажу, если номенклатуры зарегистрированы с помощью мобильного устройства, использование кода метода обработки является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f0515-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="f0515-110">Это руководство было создано с использованием демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="f0515-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="f0515-111">Эта процедура предназначена для менеджера склада.</span><span class="sxs-lookup"><span data-stu-id="f0515-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="f0515-112">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Коды метода обработки".</span><span class="sxs-lookup"><span data-stu-id="f0515-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="f0515-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f0515-113">Click New.</span></span>
    * <span data-ttu-id="f0515-114">Создайте новый код метода обработки, который будет использоваться для возвратов от клиентов.</span><span class="sxs-lookup"><span data-stu-id="f0515-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="f0515-115">В поле "Код метода обработки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f0515-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="f0515-116">В поле "Статус запасов" выберите состояние запасов, при котором запасы блокируются.</span><span class="sxs-lookup"><span data-stu-id="f0515-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="f0515-117">При использовании компании USMF выберите "Блокировка".</span><span class="sxs-lookup"><span data-stu-id="f0515-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="f0515-118">К коду метода обработки можно добавить статус запасов, чтобы переопределить статус по умолчанию в строках заказа.</span><span class="sxs-lookup"><span data-stu-id="f0515-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="f0515-119">В поле "Шаблон работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f0515-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="f0515-120">Необязательно: выберите код шаблона работы, связанный с заказом на возврат.</span><span class="sxs-lookup"><span data-stu-id="f0515-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="f0515-121">Если не указывать значение, шаблон работы будет определен автоматически по стандартным правилам, настроенным в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="f0515-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="f0515-122">Выбор шаблона работы ограничивает число процессов, с которыми может использоваться этот код метода обработки.</span><span class="sxs-lookup"><span data-stu-id="f0515-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="f0515-123">Например, если код метода обработки имеет шаблон работы с заказом на выполнение работ типа "заказ на продажу", его нельзя использовать для регистрации номенклатур, возвращаемых клиентами.</span><span class="sxs-lookup"><span data-stu-id="f0515-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="f0515-124">В поле "Вернуть код метода обработки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f0515-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="f0515-125">Код метода обработки возврата определяет, в чем состоит остаток процесса обработки заказа на возврат для зарегистрированных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f0515-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="f0515-126">В этом примере клиент должен получить кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="f0515-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="f0515-127">Необходимо добавить код метода обработки возвратов, содержащий действие "Кредит".</span><span class="sxs-lookup"><span data-stu-id="f0515-127">Add a returns disposition code that contains an action Credit.</span></span>  

