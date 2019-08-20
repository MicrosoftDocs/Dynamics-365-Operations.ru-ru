---
title: Состояния жизненного цикла запросов на обслуживание
description: В этом разделе описывается, как настроить состояния жизненного цикла запроса на обслуживание в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790534"
---
# <a name="maintenance-request-states"></a><span data-ttu-id="e8353-103">Состояния запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="e8353-103">Maintenance request states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e8353-104">Состояния жизненного цикла запроса на обслуживание определяют этапы, через которые может пройти запрос.</span><span class="sxs-lookup"><span data-stu-id="e8353-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="e8353-105">Примеры включают **Созданные**, **Активные** и **Завершенные**.</span><span class="sxs-lookup"><span data-stu-id="e8353-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="e8353-106">При преобразовании запроса на обслуживание в заказ на работу, состояние жизненного цикла запроса на обслуживание должно быть обновлено на **Завершено** или **Закрыто**, чтобы указать, что запрос на обслуживание больше не активен.</span><span class="sxs-lookup"><span data-stu-id="e8353-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="e8353-107">На странице списка **Все запросы на обслуживание** можно просматривать все запросы на обслуживание, независимо от их состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="e8353-108">Настройка состояний жизненного цикла запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="e8353-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="e8353-109">Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="e8353-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="e8353-110">Выберите **Создать** для создания состояния жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e8353-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="e8353-111">В поле **Состояния жизненного цикла** введите идентификатор для состояния жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="e8353-112">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="e8353-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e8353-113">На экспресс-вкладке **Подробно** поле **Модели жизненного цикла** показывает количество моделей жизненного цикла запроса на обслуживание, которые используют это состояние жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="e8353-114">На экспресс-вкладке **Общее** установите параметр **Активный** на **Да**, если запрос на обслуживание должен быть активным, пока он в этом состоянии жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="e8353-115">Установите параметр **Установить фактическое окончание** на **Да**, если фактическая дата и время окончания должны автоматически вводиться в запрос на обслуживание, который находится в этом состоянии жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="e8353-116">Установите параметр **Создание заказа на работу** на **Да**, если заказ на работу может быть создан из запроса на обслуживание, который находится в этом состоянии жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="e8353-117">Установите параметр **Удалить** на **Да**, если запрос на обслуживание может быть удален, пока он находится в этом состоянии жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="e8353-118">На экспресс-вкладке **Обновить** параметры **Входящие** и **Исходящие** в разделе **Активы** актуальны, если вы используете ремонт в хранилище. Установите соответствующий параметр на **Да**, если состояние жизненного цикла активов, выбранных в запросе на обслуживание должно автоматически обновляться до **Входящие** или **Исходящие**, когда состояние жизненного цикла этого запроса на обслуживание устанавливается на **Входящие** или **Исходящие**.</span><span class="sxs-lookup"><span data-stu-id="e8353-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="e8353-119">На следующем рисунке показан пример страницы **Состояния жизненного цикла запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="e8353-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Рисунок 1](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="e8353-121">Состояния жизненного цикла запроса на обслуживание, группы состояния жизненного цикла и типы, связанные с ними, и используемые так же, как состояния жизненного цикла запроса на работу, группы состояния жизненного цикла и типы.</span><span class="sxs-lookup"><span data-stu-id="e8353-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="e8353-122">Настройка моделей жизненного цикла запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="e8353-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="e8353-123">После создания состояний жизненного цикла, необходимых для запросов на обслуживание, они могут быть разделены на группы состояния жизненного цикла или модели жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="e8353-124">Модели жизненного цикла запроса на обслуживание используются для создания потока, который может использоваться для различных типов запросов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e8353-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="e8353-125">Как минимум, должна быть создана одна стандартная модель жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e8353-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="e8353-126">Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Модели жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="e8353-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="e8353-127">Выберите **Создать** для создания модели жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e8353-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="e8353-128">В поле **Модель жизненного цикла** введите идентификатор для модели жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="e8353-129">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="e8353-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e8353-130">На экспресс-вкладке **Подробно** **Состояния жизненного цикла** показывает количество состояний жизненного цикла запроса на обслуживание, которые выбраны в этой модели жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="e8353-131">Поле **Типы запросов на обслуживание** показывает количество типов запросов на обслуживание, которые используют эту модель жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="e8353-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="e8353-132">На экспресс-вкладке **Состояния жизненного цикла** выберите состояния жизненного цикла, которые должны быть включены в модель жизненного цикла:</span><span class="sxs-lookup"><span data-stu-id="e8353-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="e8353-133">Чтобы включить состояние жизненного цикла в модель жизненного цикла, выберите его в разделе **Осталось состояний жизненного цикла**, а затем выберите кнопку со стрелкой вправо ![Стрелка вправо](media/03-setup-for-requests.png), чтобы переместить его в раздел **Выбранные состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="e8353-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e8353-134">Чтобы включить все доступные состояния жизненного цикла в модель жизненного цикла, выберите кнопку **Выбрать все доступные состояния** ![Выбрать все доступные состояния](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="e8353-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="e8353-135">Все состояния жизненного цикла перемещаются в раздел **Выбранные состояния жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="e8353-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e8353-136">Чтобы удалить состояние жизненного цикла из модели жизненного цикла, выберите его в разделе **Выбранные состояния жизненного цикла**, а затем выберите кнопку со стрелкой влево ![Стрелка влево](media/05-setup-for-requests.png), чтобы переместить его в раздел **Осталось состояний жизненного цикла**.</span><span class="sxs-lookup"><span data-stu-id="e8353-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="e8353-137">На экспресс-вкладке **Общее** поля в разделе **Обновить** актуальны, если вы используете ремонт в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e8353-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="e8353-138">В поле **Состояния жизненного цикла для полученного актива** выберите состояние жизненного цикла актива, на которое активы, выбранные по запросу на обслуживание, должны быть автоматически обновлены до момента, когда они будут получены для ремонта в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e8353-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="e8353-139">В поле **Состояния жизненного цикла для доставленного актива** выберите состояние жизненного цикла актива, на которое активы, выбранные по запросу на обслуживание, должны быть автоматически обновлены до момента, когда они будут возвращены после ремонта в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e8353-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="e8353-140">На следующем рисунке показан пример страницы **Модели жизненного цикла запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="e8353-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Рисунок 2](media/06-setup-for-requests.png)
