---
title: Устранение неполадок заказов на продажу
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с заказами на продажу.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974793"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="6c09e-103">Устранение неполадок заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="6c09e-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="6c09e-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="6c09e-105">При изменении местоположения в заголовке заказа на продажу налоговая информация не обновляется.</span><span class="sxs-lookup"><span data-stu-id="6c09e-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6c09e-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-106">Issue description</span></span>

<span data-ttu-id="6c09e-107">Если сайт, склад или адрес доставки изменяется в заголовке заказа на продажу или на уровне строки, налоговая информация не обновляется автоматически для строк.</span><span class="sxs-lookup"><span data-stu-id="6c09e-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6c09e-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-108">Issue resolution</span></span>

<span data-ttu-id="6c09e-109">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="6c09e-109">This behavior is by design.</span></span> <span data-ttu-id="6c09e-110">Проблема возникает потому, что адрес доставки, сайт и склад не изменяются автоматически на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="6c09e-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="6c09e-111">Их необходимо обновить вручную.</span><span class="sxs-lookup"><span data-stu-id="6c09e-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="6c09e-112">Если для одного периода или перекрывающихся периодов имеется два коммерческих соглашения, всегда выбирается одна и та же строка соглашения.</span><span class="sxs-lookup"><span data-stu-id="6c09e-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6c09e-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-113">Issue description</span></span>

<span data-ttu-id="6c09e-114">Если для одного и того же периода или перекрывающихся периодов определены два коммерческих соглашения, то при создании строк заказа на продажу, содержащих эти номенклатуры, всегда выбирается одно и то же коммерческое соглашение.</span><span class="sxs-lookup"><span data-stu-id="6c09e-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6c09e-115">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-115">Issue resolution</span></span>

<span data-ttu-id="6c09e-116">Если для определенной даты имеется более одного коммерческого соглашения, всегда выбирается коммерческое соглашение с наименьшей ценой.</span><span class="sxs-lookup"><span data-stu-id="6c09e-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="6c09e-117">Для получения дополнительных сведений загрузите следующий технический документ: [Коммерческие соглашения в Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="6c09e-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="6c09e-118">Можно ли связать заказ на покупку с заказом на продажу для удовлетворения спроса?</span><span class="sxs-lookup"><span data-stu-id="6c09e-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="6c09e-119">Можно создать заказ на покупку из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="6c09e-120">Дополнительные сведения см. в разделе [Создание заказа на покупку из заказа на продажу](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="6c09e-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="6c09e-121">Невозможно отменить или удалить заказ на возврат или заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="6c09e-122">Можно отменить только заказы на продажу и заказы на возврат, которые находятся в состоянии *Создано*.</span><span class="sxs-lookup"><span data-stu-id="6c09e-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="6c09e-123">Дополнительные сведения см. в разделе [Отмена заказов на возврат](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="6c09e-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="6c09e-124">При попытке отменить заказ на продажу я получаю ошибку "Не удается удалить резервирования в связи с наличием зависимой от них работы".</span><span class="sxs-lookup"><span data-stu-id="6c09e-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="6c09e-125">Код ошибки: WAX4661</span><span class="sxs-lookup"><span data-stu-id="6c09e-125">Error code: WAX4661</span></span>

<span data-ttu-id="6c09e-126">Если работа связана с заказом на продажу, невозможно отменить заказ на продажу до отмены и сторнирования работы.</span><span class="sxs-lookup"><span data-stu-id="6c09e-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="6c09e-127">Это требование применимо даже в том случае, если работа, связанная с заказом на продажу, закрыта.</span><span class="sxs-lookup"><span data-stu-id="6c09e-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="6c09e-128">Чтобы устранить эту проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6c09e-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="6c09e-129">Отмените работу и поместите запасы обратно в нужное место.</span><span class="sxs-lookup"><span data-stu-id="6c09e-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="6c09e-130">Перейдите к соответствующей нагрузке заказа на продажу и выберите **Уменьшить скомплектованное количество** в строке загрузки или **Сторнировать работу** в области действий.</span><span class="sxs-lookup"><span data-stu-id="6c09e-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="6c09e-131">Работа теперь имеет статус *Отменено*, и новая работа по перемещению запасов автоматически создается и обрабатывается для помещения запасов обратно в местоположение, которое было определено во время сторнирования.</span><span class="sxs-lookup"><span data-stu-id="6c09e-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="6c09e-132">Удалите загрузку.</span><span class="sxs-lookup"><span data-stu-id="6c09e-132">Delete the load.</span></span> <span data-ttu-id="6c09e-133">Отгрузка также удаляется.</span><span class="sxs-lookup"><span data-stu-id="6c09e-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="6c09e-134">Теперь вы сможете перейти к заказу на продажу и отменить его.</span><span class="sxs-lookup"><span data-stu-id="6c09e-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="6c09e-135">Невозможно отменить внутрихолдинговый заказ на покупку, связанный с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6c09e-136">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-136">Issue description</span></span>

<span data-ttu-id="6c09e-137">При попытке отменить внутрихолдинговый заказ на покупку, связанный с заказом на продажу, может быть выведено следующее сообщение об ошибке: "Количество не может быть сокращено, поскольку это повлечет смену знака остатка".</span><span class="sxs-lookup"><span data-stu-id="6c09e-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6c09e-138">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-138">Issue resolution</span></span>

<span data-ttu-id="6c09e-139">Эта проблема была исправлена в Microsoft Dynamics 365 Supply Chain Management версии 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="6c09e-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="6c09e-140">В этой версии и более поздних версиях теперь можно отменить внутрихолдинговый заказ на покупку, связанный с заказом на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="6c09e-141">Можно ли восстановить удаленный заказ на продажу, по которому выставлена накладная?</span><span class="sxs-lookup"><span data-stu-id="6c09e-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="6c09e-142">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-142">Issue description</span></span>

<span data-ttu-id="6c09e-143">Заказ на продажу, по которому выставлена накладная, был удален по ошибке, и необходимо восстановить его или просмотреть сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="6c09e-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6c09e-144">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="6c09e-144">Issue resolution</span></span>

<span data-ttu-id="6c09e-145">Если для удаленного заказа на продажу уже была выставлена накладная, перейдите к разделу **Счет клиента \> Проводки \> Исходный документ \> Просмотр сведений**.</span><span class="sxs-lookup"><span data-stu-id="6c09e-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="6c09e-146">Найдите накладную, которую вы ищете, и выберите ее для просмотра подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="6c09e-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="6c09e-147">Эти сведения включают ссылку на заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-147">These details include the sales order reference.</span></span> <span data-ttu-id="6c09e-148">Кроме того, с этой страницы должна иметься возможность доступа к сведениям о заказах на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="6c09e-149">Крайний срок заголовка заказа на продажу не найден в информационном объекте SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="6c09e-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="6c09e-150">Поле крайнего срока не существует для сущности *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="6c09e-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="6c09e-151">Мне необходимо удалить потерянные записи заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="6c09e-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="6c09e-152">Чтобы удалить потерянные записи заказов на продажу, запустите периодическое задание *Удаление заказа на продажу*, перейдите к одному из следующих мест:</span><span class="sxs-lookup"><span data-stu-id="6c09e-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="6c09e-153">Продажи и маркетинг \> Периодические задачи \> Очистка \> Удалить заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="6c09e-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="6c09e-154">Розничная торговля и коммерция \> ИТ розничной торговли и коммерции \> Очистка \> Удалить заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="6c09e-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="6c09e-155">Существует ли способ расчета комиссий по накладным, которые уже были разнесены?</span><span class="sxs-lookup"><span data-stu-id="6c09e-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="6c09e-156">Supply Chain Management в настоящее время не поддерживает расчет комиссий для разнесенных накладных.</span><span class="sxs-lookup"><span data-stu-id="6c09e-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="6c09e-157">Номенклатура набора не поддерживается во внутрихолдинговом процессе.</span><span class="sxs-lookup"><span data-stu-id="6c09e-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="6c09e-158">Номенклатура набора недоступна для заказа на покупку, поскольку, если исследовать строки заказа на продажу для номенклатуры набора, вы увидите, что количество равно *0* (нулю) и статус *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="6c09e-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="6c09e-159">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="6c09e-159">This behavior is by design.</span></span> <span data-ttu-id="6c09e-160">Заказ на продажу покупает только компоненты номенклатуры набора.</span><span class="sxs-lookup"><span data-stu-id="6c09e-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="6c09e-161">Он не покупает саму номенклатуру набора.</span><span class="sxs-lookup"><span data-stu-id="6c09e-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="6c09e-162">Если необходимо купить набор, подумайте, следует ли помечать его как номенклатуру набора, так как эта функция разработана для сценариев распознавания выручки.</span><span class="sxs-lookup"><span data-stu-id="6c09e-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="6c09e-163">Дополнительные сведения о номенклатурах наборов см. в разделе [Наборы](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="6c09e-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
