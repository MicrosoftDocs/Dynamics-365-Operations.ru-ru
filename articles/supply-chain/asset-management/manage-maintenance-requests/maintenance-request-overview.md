---
title: Запросы на обслуживание
description: В этом разделе содержится обзор управления запросами на обслуживание в «Управлении активами»
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019637"
---
# <a name="maintenance-requests"></a><span data-ttu-id="074ba-103">Запросы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="074ba-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="074ba-104">Запросы на обслуживание — это заметки или декларации, которые создаются для уведомления менеджера или планировщика о том, что активу может потребоваться обслуживание или ремонт, но без создания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="074ba-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="074ba-105">Если содержимое запроса на обслуживание считается действительным, на основе запроса на обслуживание может быть создан заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="074ba-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="074ba-106">Запросы на обслуживание могут быть созданы для любого актива в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="074ba-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="074ba-107">Различные типы запросов на обслуживание могут быть созданы, в зависимости от того, как ваша компания использует запросы на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="074ba-108">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="074ba-108">Here are some examples:</span></span>

- <span data-ttu-id="074ba-109">Запросы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="074ba-109">Maintenance requests</span></span>
- <span data-ttu-id="074ba-110">Основание</span><span class="sxs-lookup"><span data-stu-id="074ba-110">Notes</span></span>
- <span data-ttu-id="074ba-111">Корректировки или расширения</span><span class="sxs-lookup"><span data-stu-id="074ba-111">Corrections or enhancements</span></span>
- <span data-ttu-id="074ba-112">Инвестиции</span><span class="sxs-lookup"><span data-stu-id="074ba-112">Investments</span></span>
- <span data-ttu-id="074ba-113">Ремонт в хранилище (этот тип используется при получении активов из другого местоположения, чтобы вы могли выполнять работы по обслуживанию или ремонту, а затем вернуть актив после завершения задания).</span><span class="sxs-lookup"><span data-stu-id="074ba-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="074ba-114">Просмотр запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="074ba-114">View maintenance requests</span></span>

<span data-ttu-id="074ba-115">Для просмотра запросов на обслуживание выберите **Управление активами** \> **Общее** \> **Запросы на обслуживание** \> **Все запросы на обслуживание**, **Активные запросы на обслуживание**, или **Мои запросы на обслуживание функционального местоположения**.</span><span class="sxs-lookup"><span data-stu-id="074ba-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="074ba-116">На каждой странице списка отображается часть информации, связанной с запросом на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Просмотр запросов на обслуживание](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="074ba-118">Используйте страницу списка **Мои запросы на обслуживание функционального местоположения**, чтобы просмотреть список запросов на обслуживание, которые содержат либо функциональные местоположения, с которыми вы связаны как работник, либо активы, установленные в функциональных местоположениях, с которыми вы связаны как работник.</span><span class="sxs-lookup"><span data-stu-id="074ba-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="074ba-119">(Для получения информации о том, как настроить функциональные местоположения для специалистов по обслуживанию, см. раздел [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="074ba-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="074ba-120">Хотя информация о счете клиента доступна в «Управлении сервисным обслуживанием активов» (внешнее обслуживание), она недоступна в «Управлении активами» (внутреннее обслуживание).</span><span class="sxs-lookup"><span data-stu-id="074ba-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="074ba-121">Чтобы открыть представление сведений о записи, на странице списка **Все запросы на обслуживание** в представлении сетки выберите ссылку в столбце **Запрос на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="074ba-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Просмотр сведений запроса на обслуживание](media/02-manage-maintenance-requests.png)

<span data-ttu-id="074ba-123">Кнопки на панели операций организованы на вкладках.</span><span class="sxs-lookup"><span data-stu-id="074ba-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="074ba-124">В следующей таблице кратко описаны кнопки, связанные с «Управлением активами».</span><span class="sxs-lookup"><span data-stu-id="074ba-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="074ba-125">Название кнопки</span><span class="sxs-lookup"><span data-stu-id="074ba-125">Button name</span></span>                      | <span data-ttu-id="074ba-126">Описание</span><span class="sxs-lookup"><span data-stu-id="074ba-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="074ba-127">Редактировать</span><span class="sxs-lookup"><span data-stu-id="074ba-127">Edit</span></span>                             | <span data-ttu-id="074ba-128">Изменение выбранного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-129">Сoздать</span><span class="sxs-lookup"><span data-stu-id="074ba-129">New</span></span>                              | <span data-ttu-id="074ba-130">Создание нового запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="074ba-131">Стереть</span><span class="sxs-lookup"><span data-stu-id="074ba-131">Delete</span></span>                           | <span data-ttu-id="074ba-132">Удалить выбранный запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-133">Пул заказов на работу</span><span class="sxs-lookup"><span data-stu-id="074ba-133">Work order pool</span></span>                  | <span data-ttu-id="074ba-134">Подключите выбранный запрос на обслуживание к пулу заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="074ba-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="074ba-135">Заказ на работу</span><span class="sxs-lookup"><span data-stu-id="074ba-135">Work order</span></span>                       | <span data-ttu-id="074ba-136">Создайте заказ на работ на основе выбранного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-137">Ошибка актива</span><span class="sxs-lookup"><span data-stu-id="074ba-137">Asset fault</span></span>                      | <span data-ttu-id="074ba-138">Нажмите **Ошибки актива**, где можно создать регистрацию ошибки в выбранном запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-139">Заказы на работу</span><span class="sxs-lookup"><span data-stu-id="074ba-139">Work orders</span></span>                      | <span data-ttu-id="074ba-140">Отображайте список всех заказов на работу, подключенных к выбранному запросу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-141">Обновление состояния запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="074ba-141">Update maintenance request state</span></span> | <span data-ttu-id="074ba-142">Обновление состояния запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="074ba-143">Журнал состояния жизненного цикла</span><span class="sxs-lookup"><span data-stu-id="074ba-143">Lifecycle state log</span></span>              | <span data-ttu-id="074ba-144">Просмотр журнала, отображающего состояния жизненного цикла выбранного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-145">Сведения о запросах на обслуживание</span><span class="sxs-lookup"><span data-stu-id="074ba-145">Maintenance request details</span></span>      | <span data-ttu-id="074ba-146">Печать отчета, в котором отображаются сведения выбранного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-147">Отправить кредитный актив</span><span class="sxs-lookup"><span data-stu-id="074ba-147">Send loan asset</span></span>                  | <span data-ttu-id="074ba-148">Выберите кредитный актив, который должен быть временной заменой актива, выбранного в выбранном запросе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="074ba-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="074ba-149">Возврат кредитного актива</span><span class="sxs-lookup"><span data-stu-id="074ba-149">Return loan asset</span></span>                | <span data-ttu-id="074ba-150">Регистрация кредитных активов как возвращенных.</span><span class="sxs-lookup"><span data-stu-id="074ba-150">Register the loan asset as returned.</span></span> |

