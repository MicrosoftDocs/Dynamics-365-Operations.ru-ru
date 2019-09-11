---
title: Простой из-за обслуживания
description: В этом разделе описывается простой из-за обслуживания в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918252"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="b8b8b-103">Простой из-за обслуживания</span><span class="sxs-lookup"><span data-stu-id="b8b8b-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b8b8b-104">Можно создавать регистрации времени простоя из-за обслуживания для актива, выбранного в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="b8b8b-105">Это полезно, если необходимо зарегистрировать время простоя из-за обслуживания на одном или нескольких станках в области производства.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="b8b8b-106">Сначала вы создаете коды причин простоя из-за обслуживания, которые вы хотите использовать, например, поломка и плановая остановка.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="b8b8b-107">Это выполняется в разделе **Коды причин простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="b8b8b-108">Далее можно создать регистрации простоя из-за обслуживания в разделе **Простой из-за обслуживания** и добавить соответствующие коды причин.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="b8b8b-109">Создание кодов причин простоя из-за обслуживания</span><span class="sxs-lookup"><span data-stu-id="b8b8b-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="b8b8b-110">Щелкните **Управление активами** > **Настройка** > **Заказы на работу** > **Коды причин простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="b8b8b-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-111">Click **New**.</span></span>

3. <span data-ttu-id="b8b8b-112">Вставьте код в поле **Код причины простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="b8b8b-113">Вставьте имя для кода причины в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="b8b8b-114">Установите флажок **Включить в КПЭ**, если необходимо включить код причины в расчеты ключевого показателя эффективности актива.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="b8b8b-115">Обычно плановые остановки производства не должны включаться в расчеты ключевых показателей эффективности, поскольку они не влияют на ожидаемую производительность.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="b8b8b-116">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-116">Click **Save**.</span></span>

![Рисунок 1](media/15-work-orders.png)


<span data-ttu-id="b8b8b-118">После создания кодов причин простоя из-за обслуживания, которые вы хотите использовать, можно создать регистрации простоя из-за обслуживании для заказов на работу и активов.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="b8b8b-119">Создание регистраций простоя из-за обслуживания</span><span class="sxs-lookup"><span data-stu-id="b8b8b-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="b8b8b-120">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b8b8b-121">Выберите заказ на работу и щелкните **Простой из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="b8b8b-122">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-122">Click **New**.</span></span>

4. <span data-ttu-id="b8b8b-123">Вставьте интервал дат и времени для регистрации простоя из-за обслуживания в полях **От** и **До**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="b8b8b-124">При выходе из поля **До** длительность в часах автоматически вставляется в поле **Продолжительность**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="b8b8b-125">Выберите код причины в поле **Код причины простоя из-за обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="b8b8b-126">Повторите шаги 3–6, если требуется добавить дополнительные регистрации.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="b8b8b-127">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-127">Click **Save**.</span></span>


![Рисунок 2](media/16-work-orders.png)


<span data-ttu-id="b8b8b-129">Календарь, используемый для расчета регистрации простоя из-за обслуживания, зависит от выбора в настройке активов и параметрах.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="b8b8b-130">Если ресурс выбран для актива в **Все активы** > экспресс-вкладка **Основное средство** > поле **Ресурс**, используется календарь, настроенный для связанной группы ресурсов, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Рисунок 3](media/17-work-orders.png)


<span data-ttu-id="b8b8b-132">Если никакой ресурс не выбран для актива, используется стандартный календарь, выбранный в разделе **Параметры управления активами**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Рисунок 4](media/18-work-orders.png)


<span data-ttu-id="b8b8b-134">Щелкните **Управление активами предприятия** > **Запросы** > **Простой из-за обслуживания**, чтобы просмотреть обзор всех регистраций простоя из-за обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="b8b8b-135">Все календари, используемые в модуле **Управление активами**, настраиваются в разделе **Администрирование организации** > **Настройка** > **Календари** > **Календари**.</span><span class="sxs-lookup"><span data-stu-id="b8b8b-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

