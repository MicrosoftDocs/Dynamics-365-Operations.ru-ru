---
title: "Пакетный выпуск частично зарезервированных заказов на перемещение"
description: "В этой теме описывается, как настроить и применить пакетный выпуск частично зарезервированных заказов на перемещение на мобильном устройстве."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="b5e03-103">Пакетный выпуск частично зарезервированных заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="b5e03-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b5e03-104">Функциональные возможности для пакетного выпуска частично зарезервированных заказов на перемещение позволяют частично выпускать заказы на перемещение на склад с помощью пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="b5e03-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="b5e03-105">Имея возможность выпустить неполное количество, не нужно ждать, пока на складе будет в наличии все количество заказа, прежде чем выпустить заказ.</span><span class="sxs-lookup"><span data-stu-id="b5e03-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="b5e03-106">Выпуск заказов на склад — это процесс, относящийся к комплексным функциям управления складом.</span><span class="sxs-lookup"><span data-stu-id="b5e03-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="b5e03-107">Этот процесс включает действия, такие как комплектация, упаковка и отгрузка, которые работник склада можно выполнить с помощью мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b5e03-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="b5e03-108">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="b5e03-108">Where it applies</span></span>

<span data-ttu-id="b5e03-109">При использовании этой функциональности заказы на перемещение выпускаются на склад с помощью пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="b5e03-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="b5e03-110">Пользоваться этой функциональностью удобно, если на складе нет достаточного количества запасов, однако вам все равно необходимо переместить номенклатуры с одного склада на другой.</span><span class="sxs-lookup"><span data-stu-id="b5e03-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="b5e03-111">Порядок настройки</span><span class="sxs-lookup"><span data-stu-id="b5e03-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="b5e03-112">Задание критериев выполнения для заквзов на перемещение и заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="b5e03-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="b5e03-113">Прежде чем заказ можно будет частично выпустить на склад в пакете, должны быть выполнены критерии выполнения.</span><span class="sxs-lookup"><span data-stu-id="b5e03-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="b5e03-114">Эти критерии выполнения определяются политикой выполнения.</span><span class="sxs-lookup"><span data-stu-id="b5e03-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="b5e03-115">Политики выполнения для заказов на перемещение и заказов на продажу задаются на уровне компании.</span><span class="sxs-lookup"><span data-stu-id="b5e03-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="b5e03-116">В зависимости от настройки политики выполнения выпуск заказов в пакете будет принят или отклонен.</span><span class="sxs-lookup"><span data-stu-id="b5e03-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="b5e03-117">Заказы затем будут обработаны соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b5e03-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="b5e03-118">Чтобы создать политики выполнения для заказов на перемещение и заказов на продажу, выберите **Управление складом** \> **Настройка** \> **Запуск на склад** \> **Политика выполнения**, а затем создайте политику выполнения, введя имя и описание.</span><span class="sxs-lookup"><span data-stu-id="b5e03-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="b5e03-119">Чтобы указать ставку выполнения, тип значения и сообщение, выводимое при нарушении политики выполнения, выберите **Управление складом** \> **Настройка** \> **Запуск на склад** \> **Политика выполнения**, а затем задайте значения в полях **Ставка выполнения**, **Тип значения** и **Сообщения по нарушениям выполнения**.</span><span class="sxs-lookup"><span data-stu-id="b5e03-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="b5e03-120">Задание политик выполнения для заказов на перемещение и заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="b5e03-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="b5e03-121">Чтобы задать политики выполнения для заказов на перемещение, выберите **Управление запасами** \> **Настройка** \> **Параметры модуля "Управление запасами и складами"** \> **Заказы на перемещение** \> **Управление складом**, а затем выберите политику выполнения заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="b5e03-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="b5e03-122">Чтобы задать политики выполнения для заказов на продажу, выберите **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами** \> **Управление складом**, а затем выберите политику выполнения заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="b5e03-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="b5e03-123">Разрешение выпуска в пакете и задание количества, выпускаемого в пакете</span><span class="sxs-lookup"><span data-stu-id="b5e03-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="b5e03-124">Для выпуска заказов на склад в пакете используется пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="b5e03-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="b5e03-125">Параметры, которые отличают заказы, которые следует выполнять в пакетном задании, задаются в самом пакетном задании.</span><span class="sxs-lookup"><span data-stu-id="b5e03-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="b5e03-126">Параметр **Количество** указывает, какое количество должно выпускаться в пакете — все количество или физически зарезервированное количество.</span><span class="sxs-lookup"><span data-stu-id="b5e03-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="b5e03-127">Параметр **Разрешить выпуск частично выпущенных заказов** определяет, должны ли заказы в пакете приниматься или отклоняться, если они были частично выпущены ранее.</span><span class="sxs-lookup"><span data-stu-id="b5e03-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="b5e03-128">Чтобы задать параметры **Количество** и **Разрешить выпуск частично выпущенных заказов** для заказов на перемещение, выберите **Управление складом** \> **Запуск на склад** \> **Автоматический выпуск заказов на перемещение**.</span><span class="sxs-lookup"><span data-stu-id="b5e03-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="b5e03-129">Чтобы задать параметры **Количество** и **Разрешить выпуск частично выпущенных заказов** для заказов на продажу, выберите **Управление складом** \> **Запуск на склад** \> **Автоматический выпуск заказов на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b5e03-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

