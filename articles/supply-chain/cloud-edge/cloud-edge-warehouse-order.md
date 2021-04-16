---
title: Заказы склада для облачных и пограничных единиц масштабирования
description: В этой теме приводятся сведения о возможности заказов склада, которые используются как часть рабочей нагрузки единицы масштабирования склада.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836694"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="f41de-103">Заказы склада для облачных и пограничных единиц масштабирования</span><span class="sxs-lookup"><span data-stu-id="f41de-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="f41de-104">Не все бизнес-функции полностью поддерживаются в общедоступной предварительной версии, когда используются рабочие нагрузки единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f41de-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="f41de-105">Если вы используете единицы масштабирования, убедитесь в том, что используются только процессы, которые в этой теме описаны как поддерживаемые явным образом.</span><span class="sxs-lookup"><span data-stu-id="f41de-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="f41de-106">Что такое складские заказы?</span><span class="sxs-lookup"><span data-stu-id="f41de-106">What are warehouse orders?</span></span>

<span data-ttu-id="f41de-107">*Складские заказы* представляют собой тип заказа, который был создан для поддержки развертываний склада на концентраторе и единицах масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f41de-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="f41de-108">Они позволяют получать запасы при запуске складской рабочей нагрузки на единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f41de-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="f41de-109">В настоящее время они используются только с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="f41de-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="f41de-110">Складские заказы используются как часть обработки управления складом, например, когда мобильное приложение управления складом используется для регистрации физических запасов в наличии во время обработки входящего заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="f41de-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="f41de-111">Складские заказы создаются как часть процесса *Выпуск на склад*, доступная для заказов на покупку, в которых указывается склад единицы масштабирования и номенклатуры, для которых разрешено использование процессов управления складом.</span><span class="sxs-lookup"><span data-stu-id="f41de-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f41de-112">Складские заказы доступны только в развертываниях, использующих [рабочие нагрузки управления складом для облачных и граничных единиц масштабирования](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="f41de-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="f41de-113">Создание складского заказа</span><span class="sxs-lookup"><span data-stu-id="f41de-113">Create a warehouse order</span></span>

<span data-ttu-id="f41de-114">Чтобы создать складской заказ, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f41de-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="f41de-115">Выполните вход в экземпляр Microsoft Dynamics 365 Supply Chain Management, который выполняется на концентраторе.</span><span class="sxs-lookup"><span data-stu-id="f41de-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="f41de-116">(Необходимо инициировать процесс *Выпуск на склад*, когда вы выполнили входа на концентраторе.)</span><span class="sxs-lookup"><span data-stu-id="f41de-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="f41de-117">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="f41de-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="f41de-118">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="f41de-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f41de-119">Чтобы просмотреть связанные строки складского заказа, откройте соответствующий заказ на покупку, выберите строку в разделе **Строки заказа на покупку**, затем на панели инструментов выберите **Склад \> Строки складского заказа**.</span><span class="sxs-lookup"><span data-stu-id="f41de-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="f41de-120">Чтобы просмотреть все строки, перейдите в раздел **Управление складом \> Запросы и отчеты \> Строки складского заказа**.</span><span class="sxs-lookup"><span data-stu-id="f41de-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="f41de-121">Можно также запустить процесс *Выпуск на склад* из пакетного задания, перейдя **Управление складом > Выпуск на склад > Автоматический выпуск заказов на покупку**.</span><span class="sxs-lookup"><span data-stu-id="f41de-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="f41de-122">При настройке пакетного задания можно выбрать конкретные строки заказа на покупку на основе запроса.</span><span class="sxs-lookup"><span data-stu-id="f41de-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="f41de-123">Типичным сценарием является настройка повторяющегося пакетного задания, в результате выполнения которого будут выпущены все подтвержденные строки заказа на покупку, ожидаемые для прибытия на следующий день.</span><span class="sxs-lookup"><span data-stu-id="f41de-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="f41de-124">Отмена складского заказа</span><span class="sxs-lookup"><span data-stu-id="f41de-124">Cancel a warehouse order</span></span>

<span data-ttu-id="f41de-125">Как часть процесса *Выпуск на склад*, проводки запасов заказа на покупку связываются со складскими заказами, и их обновление с концентратора блокируется.</span><span class="sxs-lookup"><span data-stu-id="f41de-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="f41de-126">Если вы выпустили на склад по ошибке или если у вас есть другая причина отменить создание строк складского заказа, можно запросить отмену строк складского заказа.</span><span class="sxs-lookup"><span data-stu-id="f41de-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="f41de-127">Чтобы отменить строки складского заказа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f41de-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="f41de-128">Выполните вход в экземпляр Supply Chain Management, который выполняется на концентраторе.</span><span class="sxs-lookup"><span data-stu-id="f41de-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="f41de-129">Перейдите в раздел **Управление складом \> Запросы и отчеты \> Строки складского заказа**.</span><span class="sxs-lookup"><span data-stu-id="f41de-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="f41de-130">Выберите соответствующую строку.</span><span class="sxs-lookup"><span data-stu-id="f41de-130">Select the relevant line.</span></span>
1. <span data-ttu-id="f41de-131">В области действий выберите **Отменить строки складского заказа**.</span><span class="sxs-lookup"><span data-stu-id="f41de-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="f41de-132">Запрос на отмену строк будет отклонен для любых строк, уже ожидающих отмены, или которые активно обрабатываются на складе, рабочая нагрузка которого запущена на единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f41de-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="f41de-133">Мониторинг складского заказа</span><span class="sxs-lookup"><span data-stu-id="f41de-133">Monitor a warehouse order</span></span>

<span data-ttu-id="f41de-134">В представлении **Строки складского заказа** можно отслеживать ход входящих приемок путем просмотра значений в столбце **Количество, которое осталось получить**.</span><span class="sxs-lookup"><span data-stu-id="f41de-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="f41de-135">Для просмотра сведений, связанных с работой, выполненной с использованием мобильного приложения управления складом, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="f41de-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="f41de-136">Перейдите в раздел **Управление складом \> Запросы и отчеты \> Строки складского заказа** и используйте фильтр, чтобы найти строки, которые вы ищете.</span><span class="sxs-lookup"><span data-stu-id="f41de-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="f41de-137">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку** и откройте соответствующий заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="f41de-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="f41de-138">В разделе **Строки заказа на покупку** выберите одну или несколько строк, затем на панели инструментов выберите **Склад \> Записи приемки на склад**.</span><span class="sxs-lookup"><span data-stu-id="f41de-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]