---
title: "Карантинные заказы"
description: "В этой статье описывается, как карантинные заказы используются для блокировки запасов."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/12/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="37bb3-103">Карантинные заказы</span><span class="sxs-lookup"><span data-stu-id="37bb3-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="37bb3-104">В этой статье описывается, как карантинные заказы используются для блокировки запасов.</span><span class="sxs-lookup"><span data-stu-id="37bb3-104">This article describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="37bb3-105">Карантинные заказы можно использовать, чтобы заблокировать запасы.</span><span class="sxs-lookup"><span data-stu-id="37bb3-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="37bb3-106">Например, требуется установить карантин для номенклатуры по причинам контроля качества.</span><span class="sxs-lookup"><span data-stu-id="37bb3-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="37bb3-107">Запасы, которые помещены в карантин, переносятся на карантинный склад.</span><span class="sxs-lookup"><span data-stu-id="37bb3-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="37bb3-108">**Примечание.** При использовании расширенных процессов управления складом (в модуле управления складом) обработка карантинных заказов используется только для возвращенных заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="37bb3-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-onhand-inventory-items"></a><span data-ttu-id="37bb3-109">Помещение номенклатур в наличии в карантин</span><span class="sxs-lookup"><span data-stu-id="37bb3-109">Quarantine onhand inventory items</span></span>
<span data-ttu-id="37bb3-110">При установлении карантина для номенклатур можно создавать карантинные заказы вручную или настроить систему на их автоматическое создание в ходе обработки входящего потока.</span><span class="sxs-lookup"><span data-stu-id="37bb3-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="37bb3-111">Для автоматического создания карантинных заказов выберите вариант **Управление карантином** на вкладке **Политики запасов** на странице **Группы номенклатурных моделей**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="37bb3-112">Также необходимо указать карантинный склад по умолчанию в поле **Карантинный склад** для складов приемки.</span><span class="sxs-lookup"><span data-stu-id="37bb3-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="37bb3-113">Когда физические запасы в наличии регистрируются в заказе на покупку или производственном заказе, карантинные номенклатуры автоматически перемещаются на карантинный склад в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="37bb3-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="37bb3-114">Это перемещение происходит, потому что статус карантинного заказа изменяется на **Начато**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="37bb3-115">При создании карантинных заказов вручную не требуется, чтобы данная номенклатура была настроена для управления карантином в соответствующей группе модели номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="37bb3-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="37bb3-116">Для этого процесса необходимо указать запасы в наличии, которые должны быть помещены в карантин, и карантинный склад, который должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="37bb3-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="37bb3-117">Можно использовать статусы карантинного заказа, чтобы помочь запланировать процесс.</span><span class="sxs-lookup"><span data-stu-id="37bb3-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="37bb3-118">Статусы карантинных заказов</span><span class="sxs-lookup"><span data-stu-id="37bb3-118">Quarantine order statuses</span></span>
<span data-ttu-id="37bb3-119">Карантинные заказы могут иметь следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="37bb3-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="37bb3-120">Создан</span><span class="sxs-lookup"><span data-stu-id="37bb3-120">Created</span></span>
-   <span data-ttu-id="37bb3-121">Начато</span><span class="sxs-lookup"><span data-stu-id="37bb3-121">Started</span></span>
-   <span data-ttu-id="37bb3-122">Принято</span><span class="sxs-lookup"><span data-stu-id="37bb3-122">Reported as finished</span></span>
-   <span data-ttu-id="37bb3-123">Завершено</span><span class="sxs-lookup"><span data-stu-id="37bb3-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="37bb3-124">Создан</span><span class="sxs-lookup"><span data-stu-id="37bb3-124">Created</span></span>

<span data-ttu-id="37bb3-125">Если карантинный заказ создан вручную, но номенклатура еще не помещена на карантинный склад, карантинный заказ имеет статус **Создано**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="37bb3-126">При этом формируются две складские проводки.</span><span class="sxs-lookup"><span data-stu-id="37bb3-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="37bb3-127">Одна проводка — это проводка расхода, которая может иметь статус **Заказано**, **Физ. зарезервировано** или **Скомплектовано**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="37bb3-128">Вторая провода — это проводка прихода, которая может иметь статус **Заказано** или **Зарегистрировано** на карантинном складе.</span><span class="sxs-lookup"><span data-stu-id="37bb3-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="37bb3-129">Резервировать, комплектовать и регистрировать обновления в запасах можно с помощью обычных процессов.</span><span class="sxs-lookup"><span data-stu-id="37bb3-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="37bb3-130">Начато</span><span class="sxs-lookup"><span data-stu-id="37bb3-130">Started</span></span>

<span data-ttu-id="37bb3-131">Когда карантинный заказ имеет статус **Начато**, запасы перемещаются с обычного склада на карантинный склад, и формируется две проводки по запасам.</span><span class="sxs-lookup"><span data-stu-id="37bb3-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="37bb3-132">Одна из них имеет статус **Отпущено**, а другая — статус **Получено**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="37bb3-133">В это же время создаются две складские проводки для обработки переноса возврата.</span><span class="sxs-lookup"><span data-stu-id="37bb3-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="37bb3-134">Эти проводки не датируются.</span><span class="sxs-lookup"><span data-stu-id="37bb3-134">These transactions aren't dated.</span></span> <span data-ttu-id="37bb3-135">Одна из них имеет статус **Физ. зарезервировано**, а другая — статус **Заказано**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="37bb3-136">Принято</span><span class="sxs-lookup"><span data-stu-id="37bb3-136">Reported as finished</span></span>

<span data-ttu-id="37bb3-137">Перевести карантинный заказ из начатого в готовый можно, щелкнув **Приемка**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="37bb3-138">Номенклатура больше не является карантинной, но она еще не переведена на обычный склад.</span><span class="sxs-lookup"><span data-stu-id="37bb3-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="37bb3-139">Перемещение обратно на обычный склад может обрабатываться через журнал "Прибытие номенклатуры", который можно инициализировать в ходе процесса приемки.</span><span class="sxs-lookup"><span data-stu-id="37bb3-139">The movement back to the regular warehouse can be procesed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="37bb3-140">Завершено</span><span class="sxs-lookup"><span data-stu-id="37bb3-140">Ended</span></span>

<span data-ttu-id="37bb3-141">Когда карантинный заказ заканчивается, номенклатура перемещается с карантинного склада назад на обычный.</span><span class="sxs-lookup"><span data-stu-id="37bb3-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="37bb3-142">Для статуса проводки номенклатуры на карантинном складе устанавливается значение **Продано**, а на обычном складе — значение **Куплено**.</span><span class="sxs-lookup"><span data-stu-id="37bb3-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="37bb3-143">Отправка карантинного заказа в отходы</span><span class="sxs-lookup"><span data-stu-id="37bb3-143">Quarantine order scrap</span></span>
<span data-ttu-id="37bb3-144">В рамках обработки карантинного заказа запасы можно отправлять в отходы.</span><span class="sxs-lookup"><span data-stu-id="37bb3-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="37bb3-145">При обработке отхода для запасов устанавливается статус **Продано** посредством проводки расхода из карантинного склада.</span><span class="sxs-lookup"><span data-stu-id="37bb3-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="37bb3-146">См. также</span><span class="sxs-lookup"><span data-stu-id="37bb3-146">See also</span></span>
--------

[<span data-ttu-id="37bb3-147">Блокировка запасов</span><span class="sxs-lookup"><span data-stu-id="37bb3-147">Inventory blocking</span></span>](inventory-blocking.md)

