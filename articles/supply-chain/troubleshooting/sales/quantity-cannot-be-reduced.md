---
title: Невозможно уменьшить количество, когда заказ на продажу отменен
description: Невозможно уменьшить количество, когда заказ на продажу отменен.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230844"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="da7d4-103">Невозможно уменьшить количество, когда заказ на продажу отменен</span><span class="sxs-lookup"><span data-stu-id="da7d4-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="da7d4-104">Код ошибки: SYS138831</span><span class="sxs-lookup"><span data-stu-id="da7d4-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="da7d4-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="da7d4-105">Symptoms</span></span>

<span data-ttu-id="da7d4-106">Система отобразит следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="da7d4-106">The system shows the following error message:</span></span>

> <span data-ttu-id="da7d4-107">Количество не может быть уменьшено.</span><span class="sxs-lookup"><span data-stu-id="da7d4-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="da7d4-108">Количество складских проводок в заказе слишком мало, так как на него ссылаются заказ на выпуск или производственный заказ или оно помечено для других проводок.</span><span class="sxs-lookup"><span data-stu-id="da7d4-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="da7d4-109">Причина</span><span class="sxs-lookup"><span data-stu-id="da7d4-109">Cause</span></span>

<span data-ttu-id="da7d4-110">Если работа связана с заказом на продажу, невозможно отменить заказ на продажу до отмены и сторнирования работы.</span><span class="sxs-lookup"><span data-stu-id="da7d4-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="da7d4-111">Это требование применимо даже в том случае, если работа, связанная с заказом на продажу, закрыта.</span><span class="sxs-lookup"><span data-stu-id="da7d4-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="da7d4-112">Решение</span><span class="sxs-lookup"><span data-stu-id="da7d4-112">Resolution</span></span>

<span data-ttu-id="da7d4-113">Для решения проблемы необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="da7d4-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="da7d4-114">Отмените открытую работу.</span><span class="sxs-lookup"><span data-stu-id="da7d4-114">Cancel open work.</span></span>
1. <span data-ttu-id="da7d4-115">Удалите загрузку.</span><span class="sxs-lookup"><span data-stu-id="da7d4-115">Delete the load.</span></span>
1. <span data-ttu-id="da7d4-116">Уменьшите скомплектованное количество.</span><span class="sxs-lookup"><span data-stu-id="da7d4-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="da7d4-117">Отмена открытой работы</span><span class="sxs-lookup"><span data-stu-id="da7d4-117">Cancel open work</span></span>

<span data-ttu-id="da7d4-118">Чтобы отменить открытую работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da7d4-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="da7d4-119">Перейдите **Управление складом \> Периодические задачи \> Очистка \> Отмена работы**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="da7d4-120">В поле **Код работы** укажите код работы, которую необходимо отменить и у которой в настоящее время есть значение **Статус работы** как *Открыто*, *Выполняется*, *Отменено*, *Объединено* или *Закрыто*.</span><span class="sxs-lookup"><span data-stu-id="da7d4-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="da7d4-121">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-121">Select **OK**.</span></span>
1. <span data-ttu-id="da7d4-122">Выберите **Да** для подтверждения того, что вы хотите отменить работу.</span><span class="sxs-lookup"><span data-stu-id="da7d4-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="da7d4-123">Удаление загрузки</span><span class="sxs-lookup"><span data-stu-id="da7d4-123">Delete the load</span></span>

<span data-ttu-id="da7d4-124">Чтобы удалить загрузку, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="da7d4-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="da7d4-125">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="da7d4-126">Откройте соответствующий заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="da7d4-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="da7d4-127">На экспресс-вкладке **Строки заказа на продажу** выберите **Склад \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="da7d4-128">На странице **Работа** в области действий на вкладке **Работа** в группе **Работа** выберите **Отменить работу**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="da7d4-129">Убедитесь, что в поле **Статус работы** указано значение *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="da7d4-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="da7d4-130">Закройте страницу **Работа**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="da7d4-131">На странице сведений о заказе на продажу на экспресс-вкладке **Строки заказа на продажу** выберите **Склад \> Сведения о загрузке**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="da7d4-132">В области действий выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="da7d4-133">Выберите **Да** для подтверждения того, что вы хотите удалить загрузку.</span><span class="sxs-lookup"><span data-stu-id="da7d4-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="da7d4-134">Закройте страницу **Загрузка**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="da7d4-135">Уменьшение скомплектованного количества</span><span class="sxs-lookup"><span data-stu-id="da7d4-135">Reduce the picked quantity</span></span>

<span data-ttu-id="da7d4-136">После отмены всей работы выполните следующие шаги, чтобы уменьшить скомплектованное количество.</span><span class="sxs-lookup"><span data-stu-id="da7d4-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="da7d4-137">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="da7d4-138">Откройте соответствующий заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="da7d4-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="da7d4-139">На экспресс-вкладке **Строки заказа на продажу** выберите **Обновить строку \> Комплектация** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="da7d4-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="da7d4-140">На странице **Комплектация** в разделе **Проводки** выберите строку, в которой в поле **Статус выпуска** указано значение *Скомплектовано*.</span><span class="sxs-lookup"><span data-stu-id="da7d4-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="da7d4-141">В разделе **Проводки** выберите **Добавить строку комплектации** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="da7d4-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="da7d4-142">В разделе **Строки проводок** выберите **Подтвердить комплектацию всего** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="da7d4-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="da7d4-143">Закройте страницу **Комплектация**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="da7d4-144">На странице сведений заказ на продажу на панели действий на вкладке **Заказ на продажу** в группе **Ведение** выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="da7d4-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="da7d4-145">Выберите **Да** для подтверждения того, что вы хотите отменить заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="da7d4-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
