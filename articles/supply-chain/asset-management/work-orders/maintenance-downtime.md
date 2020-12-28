---
title: Простой из-за обслуживания для заказов на работу
description: В этой теме описывается, как можно создавать регистрации времени простоя из-за обслуживания для актива, выбранного в заказе на работу.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 263a044a0a378e95ea271ac1c6f468f9e3287f26
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435857"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="94d9e-103">Простой из-за обслуживания для заказов на работу</span><span class="sxs-lookup"><span data-stu-id="94d9e-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="94d9e-104">Можно создавать регистрации времени простоя из-за обслуживания для актива, выбранного в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="94d9e-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="94d9e-105">Эта возможность полезна, если необходимо зарегистрировать время простоя из-за обслуживания на одном или нескольких станках в области производства.</span><span class="sxs-lookup"><span data-stu-id="94d9e-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="94d9e-106">Сначала вы создаете коды причин простоя из-за обслуживания, которые вы хотите использовать, например, **поломка** и **плановая остановка**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="94d9e-107">Этот шаг выполняется на странице **Коды причин простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="94d9e-108">Далее можно создать регистрации простоя из-за обслуживания на странице **Простой из-за обслуживания** и добавить соответствующие коды причин простоя из-за обслуживания.</span><span class="sxs-lookup"><span data-stu-id="94d9e-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="94d9e-109">Создание кодов причин простоя из-за обслуживания</span><span class="sxs-lookup"><span data-stu-id="94d9e-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="94d9e-110">Выберите **Управление активами** > **Настройка** > **Заказы на работу** > **Коды причин простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="94d9e-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-111">Select **New**.</span></span>

3. <span data-ttu-id="94d9e-112">В поле **код причины простоя при обслуживании** введите код причины простоя из-за обслуживания.</span><span class="sxs-lookup"><span data-stu-id="94d9e-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="94d9e-113">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="94d9e-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="94d9e-114">Установите флажок **Включить в КПЭ**, если код причины должен включаться в расчеты ключевых показателей эффективности (КПЭ) для актива.</span><span class="sxs-lookup"><span data-stu-id="94d9e-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="94d9e-115">Обычно плановые остановки производства не должны включаться в расчеты ключевых показателей эффективности, поскольку они не влияют на ожидаемую производительность.</span><span class="sxs-lookup"><span data-stu-id="94d9e-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="94d9e-116">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-116">Select **Save**.</span></span>

<span data-ttu-id="94d9e-117">На рисунке ниже показан пример страницы **Коды причин простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Рисунок 1](media/15-work-orders.png)

<span data-ttu-id="94d9e-119">После создания кодов причин простоя из-за обслуживания, которые вы хотите использовать, можно создать регистрации простоя из-за обслуживании для заказов на работу и активов.</span><span class="sxs-lookup"><span data-stu-id="94d9e-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="94d9e-120">Создание регистраций простоя из-за обслуживания</span><span class="sxs-lookup"><span data-stu-id="94d9e-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="94d9e-121">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="94d9e-122">Выберите заказ на работу, а затем в области действий на вкладке **Заказ на работу** в группе **Актив** выберите **Простой из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="94d9e-123">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-123">Select **New**.</span></span>

4. <span data-ttu-id="94d9e-124">Определите интервал дат и времени для регистрации простоя из-за обслуживания в полях **От** и **До**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="94d9e-125">При выходе из поля **До** длительность в часах автоматически вставляется в поле **Продолжительность**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="94d9e-126">Выберите код причины в поле **Код причины простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="94d9e-127">Повторите шаги 3–5, чтобы добавить другие регистрации.</span><span class="sxs-lookup"><span data-stu-id="94d9e-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="94d9e-128">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-128">Select **Save**.</span></span>

<span data-ttu-id="94d9e-129">Иллюстрация ниже показывает пример регистрации простоя из-за обслуживания.</span><span class="sxs-lookup"><span data-stu-id="94d9e-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Рисунок 2](media/16-work-orders.png)

<span data-ttu-id="94d9e-131">Календарь, используемый для расчета регистрации простоя из-за обслуживания, зависит от выбора в настройке активов и параметрах.</span><span class="sxs-lookup"><span data-stu-id="94d9e-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="94d9e-132">Если ресурс выбран для актива в поле **Ресурс** на экспресс-вкладке **основное средство** страницы **Все активы**, используется календарь, настроенный для связанной группы ресурсов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="94d9e-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Рисунок 3](media/17-work-orders.png)

<span data-ttu-id="94d9e-134">Если никакой ресурс не выбран для актива, используется стандартный календарь, выбранный на странице **Параметры управления активами**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="94d9e-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Рисунок 4](media/18-work-orders.png)

<span data-ttu-id="94d9e-136">Щелкните **Управление активами** > **Запросы** > **Простой из-за обслуживания**, чтобы просмотреть обзор всех регистраций простоя из-за обслуживания.</span><span class="sxs-lookup"><span data-stu-id="94d9e-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="94d9e-137">Все календари, используемые в модуле **Управление активами**, настраиваются в разделе **Администрирование организации** > **Настройка** > **Календари** > **Календари**.</span><span class="sxs-lookup"><span data-stu-id="94d9e-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

