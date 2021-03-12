---
title: Обзор исходящих процессов
description: В этой теме приведен обзор исходящего процесса в модуле "Управление запасами".
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27596bf260c069af4a7457c0eb8d02c45e5202b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000242"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="1f2d2-103">Обзор исходящих процессов</span><span class="sxs-lookup"><span data-stu-id="1f2d2-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f2d2-104">В этой теме приведен обзор исходящего процесса в модуле "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="1f2d2-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="1f2d2-105">Заказы на выпуск</span><span class="sxs-lookup"><span data-stu-id="1f2d2-105">Output orders</span></span>

<span data-ttu-id="1f2d2-106">Заказы на выпуск используются для связывания строк заказа на продажу и строк заказа на перемещение с исходящими процессами комплектации, в которых используются листы комплектации.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="1f2d2-107">При формировании листов комплектации из заказов на продажу или из заказов на перемещение автоматически создаются заказы на выпуск и отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="1f2d2-108">Лист комплектации имеет отношение "один к одному" с отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="1f2d2-109">Из отгрузки можно обработать отгрузку заказа на перемещение или отборочную накладную заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="1f2d2-110">На следующей схеме приведен обзор процесса для исходящих заказов.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="1f2d2-111">[![Обзор процесса исходящих заказов.](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="1f2d2-112">Можно настроить исходящие правила для определения того, каким образом программа должна обрабатывать исходящий процесс.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="1f2d2-113">Эти правила можно использовать для управления процессом отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="1f2d2-114">В частности, правила можно использовать для контроля такого, на какой стадии процесса отгрузка может быть отправлена.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="1f2d2-115">Следующие параметры определяют способ обработки исходящих процессов.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="1f2d2-116">Статус маршрута комплектации для продаж и заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="1f2d2-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="1f2d2-117">Выберите **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**, а затем на вкладке **Обновления** выберите значение в поле **Статус маршрута комплектации**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="1f2d2-118">[![Поле "Статус маршрута комплектации" для заказов на продажу](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="1f2d2-119">Если в поле **Статус маршрута комплектации** установлено значение **Завершено**, процесс комплектации происходит автоматически в рамках процесса формирования листов комплектации.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="1f2d2-120">Если в этом поле установлено значение **Активировано**, строки листа комплектации необходимо обновить вручную.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="1f2d2-121">Эта же настройка применяется к заказам на перемещение.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="1f2d2-122">Выберите **Управление запасами** \> **Настройка** \> **Параметры модуля "Управление запасами и складами"**, а затем на вкладке **Транспортировка** выберите значение в поле **Статус маршрута комплектации**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="1f2d2-123">[![Поле "Статус маршрута комплектации" для заказов на перемещение](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="1f2d2-124">Завершение складских заказов на выпуск</span><span class="sxs-lookup"><span data-stu-id="1f2d2-124">End output inventory orders</span></span>

<span data-ttu-id="1f2d2-125">Выберите **Управление запасами** \> **Настройка** \> **Параметры модуля "Управление запасами и складами"**, а затем на вкладке **Общие** задайте параметр **Завершить складской заказ на выпуск**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="1f2d2-126">[![Параметр "Завершить складской заказ на выпуск"](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="1f2d2-127">Когда работник склада уменьшает количества в листе подбора, соответствующие количества складского заказа будут удалены из отгрузки.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="1f2d2-128">При обновлении листа подбора в некоторый момент времени оставшиеся количества передаются обратно в заказ, если для параметра **Завершить складской заказ на выпуск** установлено значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="1f2d2-129">Если для параметра **Завершить складской заказ на выпуск** задано значение **Нет**, оставшиеся количества остаются в качестве количества открытого заказа на выпуск и должны быть добавлены в новый лист подбора в рамках функции **Открытые заказы на выпуск**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="1f2d2-130">[![Команда "Открытые заказы на выпуск" в меню "Функции"](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="1f2d2-131">[![Меню "Функции" на странице "Открытые заказы на выпуск"](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="1f2d2-132">Уменьшить количество</span><span class="sxs-lookup"><span data-stu-id="1f2d2-132">Reduce quantity</span></span>

<span data-ttu-id="1f2d2-133">Третий параметр, который можно использовать в рамках процесса формирования листов комплектации, — это параметр **Уменьшить количество**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="1f2d2-134">Значение этого параметра используется вместе с параметром **Резервирование**, который запускает процесс резервирования в рамках выпуска на склад.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="1f2d2-135">[![Параметр "Уменьшить количество"](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="1f2d2-136">Пример исходящего процесса для заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="1f2d2-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="1f2d2-137">В данном примере имеется заказ на продажу на две номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="1f2d2-138">Во время формирования листа комплектации вы выбираете параметр **Уменьшить количество**.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="1f2d2-139">Следовательно, вы выпускаете и создаете строки комплектации только для доступных запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="1f2d2-140">О комплектации должно сообщаться посредством процесса регистрации для листов комплектации (**Статус маршрута комплектации** = **Активировано**).</span><span class="sxs-lookup"><span data-stu-id="1f2d2-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="1f2d2-141">Запасы, которые еще не зарезервированы, резервируются во время формирования листа комплектации.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="1f2d2-142">Отсутствующие в наличии запасы могут быть либо удалены из заказа на продажу, либо выпущены на склад для исходящей обработки позднее, когда запасы будут доступны для комплектации.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="1f2d2-143">[![Обновление листа комплектации](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="1f2d2-144">Как только все строки комплектации на странице **Регистрация отгрузочной накладной** будут скомплектованы, связанная с ними отгрузка будет завершена.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="1f2d2-145">После этого на основании скомплектованных запасов можно инициализировать процесс для создания отборочных накладных для заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="1f2d2-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="1f2d2-146">[![Обновление исходящих отгрузок](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="1f2d2-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
