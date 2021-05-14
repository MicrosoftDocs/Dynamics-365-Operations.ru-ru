---
title: Карантинные заказы
description: В этом разделе описывается, как использовать карантинные заказы для блокировки запасов.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956190"
---
# <a name="quarantine-orders"></a><span data-ttu-id="4aa1f-103">Карантинные заказы</span><span class="sxs-lookup"><span data-stu-id="4aa1f-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa1f-104">В этом разделе описывается, как использовать карантинные заказы для блокировки запасов.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="4aa1f-105">Карантинные заказы позволяют блокировать запасы.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="4aa1f-106">Например, требуется установить карантин для номенклатуры по причинам контроля качества.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="4aa1f-107">Запасы, которые помещены в карантин, переносятся на карантинный склад.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="4aa1f-108">При использовании расширенных процессов управления складом (в модуле управления складом) обработка карантинных заказов используется только для возвращенных заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="4aa1f-109">Помещение номенклатур в наличии в карантин</span><span class="sxs-lookup"><span data-stu-id="4aa1f-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="4aa1f-110">При установлении карантина для номенклатур можно создавать карантинные заказы вручную или настроить систему на их автоматическое создание в ходе обработки входящего потока.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="4aa1f-111">Чтобы настроить систему на автоматическое создание карантинных заказов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="4aa1f-112">Перейдите в раздел **Управление запасами \> Настройка \> Запасы \> Группы номенклатурных моделей**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="4aa1f-113">Выберите подходящую группу моделей в панели списка или создайте новую группу моделей.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="4aa1f-114">На экспресс-вкладке **Политики запасов** установите флажок **Управление карантином**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="4aa1f-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-115">Close the page.</span></span>
1. <span data-ttu-id="4aa1f-116">Также необходимо указать карантинный склад по умолчанию в поле **Карантинный склад** для складов приемки.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="4aa1f-117">Когда номенклатура, зарегистрированная как полученная на складе, принадлежит к группе моделей, в которой установлен флажок **Управление карантином**, система создает для нее карантинный заказ.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="4aa1f-118">Карантинный заказ указывает сотрудникам переместить номенклатуру на карантинный склад.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="4aa1f-119">При создании карантинных заказов вручную на странице **Карантинные заказы** не требуется, чтобы данная номенклатура была настроена для управления карантином в соответствующей группе модели номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="4aa1f-120">Для этого процесса необходимо указать запасы в наличии, которые должны быть помещены в карантин, и карантинный склад, который должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="4aa1f-121">Можно использовать статусы карантинного заказа, чтобы помочь запланировать процесс.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="4aa1f-122">Статусы карантинных заказов</span><span class="sxs-lookup"><span data-stu-id="4aa1f-122">Quarantine order statuses</span></span>

<span data-ttu-id="4aa1f-123">Карантинные заказы могут иметь следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="4aa1f-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="4aa1f-124">Создан</span><span class="sxs-lookup"><span data-stu-id="4aa1f-124">Created</span></span>
- <span data-ttu-id="4aa1f-125">Начато</span><span class="sxs-lookup"><span data-stu-id="4aa1f-125">Started</span></span>
- <span data-ttu-id="4aa1f-126">Принято</span><span class="sxs-lookup"><span data-stu-id="4aa1f-126">Reported as finished</span></span>
- <span data-ttu-id="4aa1f-127">Завершено</span><span class="sxs-lookup"><span data-stu-id="4aa1f-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="4aa1f-128">Создан</span><span class="sxs-lookup"><span data-stu-id="4aa1f-128">Created</span></span>

<span data-ttu-id="4aa1f-129">Если карантинный заказ создан вручную, но номенклатура еще не помещена на карантинный склад, карантинный заказ имеет статус **Создано**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="4aa1f-130">При этом формируются две складские проводки.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="4aa1f-131">Одна проводка — это проводка расхода, которая может иметь статус **Заказано**, **Физ. зарезервировано** или **Скомплектовано**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="4aa1f-132">Вторая провода — это проводка прихода, которая может иметь статус **Заказано** или **Зарегистрировано** на карантинном складе.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="4aa1f-133">Резервировать, комплектовать и регистрировать обновления в запасах можно с помощью обычных процессов.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="4aa1f-134">Начато</span><span class="sxs-lookup"><span data-stu-id="4aa1f-134">Started</span></span>

<span data-ttu-id="4aa1f-135">Когда карантинный заказ имеет статус **Начато**, запасы перемещаются с обычного склада на карантинный склад, и формируется две проводки по запасам.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="4aa1f-136">Одна из них имеет статус **Отпущено**, а другая — статус **Получено**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="4aa1f-137">В это же время создаются две складские проводки для обработки переноса возврата.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="4aa1f-138">Эти проводки не датируются.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-138">These transactions aren't dated.</span></span> <span data-ttu-id="4aa1f-139">Одна из них имеет статус **Физ. зарезервировано**, а другая — статус **Заказано**.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="4aa1f-140">Принято</span><span class="sxs-lookup"><span data-stu-id="4aa1f-140">Reported as finished</span></span>

<span data-ttu-id="4aa1f-141">Для приемки начатого карантинного заказа откройте заказ и выберите **Приемка** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="4aa1f-142">Номенклатура больше не является карантинной, но она еще не переведена на обычный склад.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="4aa1f-143">Перемещение обратно на обычный склад может обрабатываться через журнал "Прибытие номенклатуры", который можно инициализировать в ходе процесса приемки.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="4aa1f-144">Завершено</span><span class="sxs-lookup"><span data-stu-id="4aa1f-144">Ended</span></span>

<span data-ttu-id="4aa1f-145">Когда карантинный заказ заканчивается, номенклатура перемещается с карантинного склада назад на обычный.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="4aa1f-146">Для статуса проводки номенклатуры на карантинном складе устанавливается значение *Продано*, а на обычном складе — значение *Куплено*.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="4aa1f-147">Отправка карантинного заказа в отходы</span><span class="sxs-lookup"><span data-stu-id="4aa1f-147">Quarantine order scrap</span></span>

<span data-ttu-id="4aa1f-148">В рамках обработки карантинного заказа запасы можно отправлять в отходы.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="4aa1f-149">При обработке отхода для запасов устанавливается статус *Продано* посредством проводки расхода из карантинного склада.</span><span class="sxs-lookup"><span data-stu-id="4aa1f-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4aa1f-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4aa1f-150">Additional resources</span></span>

- [<span data-ttu-id="4aa1f-151">Блокировка запасов</span><span class="sxs-lookup"><span data-stu-id="4aa1f-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
