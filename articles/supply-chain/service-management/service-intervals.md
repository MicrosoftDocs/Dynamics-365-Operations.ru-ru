---
title: Диапазоны сервисного обслуживания
description: Интервал обслуживания определяет частоту, с которой строки заказа на обслуживание создаются для строк соглашения на обслуживание при автоматическом создании заказов на обслуживание.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216283"
---
# <a name="service-intervals"></a><span data-ttu-id="8ef33-103">Диапазоны сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="8ef33-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ef33-104">Диапазон соглашения на обслуживание определяет частоту, с которой строки заказа на обслуживание создаются для строк соглашения на обслуживание при автоматическом создании заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="8ef33-105">При автоматическом создании заказов на обслуживание, строки заказа на обслуживание создаются в соответствии с диапазоном, указанной для строки соглашения на обслуживание с начальной даты строки соглашения.</span><span class="sxs-lookup"><span data-stu-id="8ef33-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="8ef33-106">Если поле **Интервал** строки соглашения на обслуживание пусто на странице **Соглашения на обслуживание**, строка является одноразовым событием и не используется для повторного создания заказов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="8ef33-107">пример</span><span class="sxs-lookup"><span data-stu-id="8ef33-107">Example</span></span>

<span data-ttu-id="8ef33-108">Пример показывает, как интервал сервисного обслуживания повлияет на строки заказа и строки соглашения на обслуживание в заказе на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="8ef33-109">Создание соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="8ef33-109">Create a service agreement</span></span>

<span data-ttu-id="8ef33-110">Сначала требуется создать соглашение на обслуживание и установить для параметра **Объединение заказов на сервисное обслуживание** значение **По соглашению о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="8ef33-111">Щелкните **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="8ef33-112">На **Панель операций**, на вкладке **Соглашение о сервисном обслуживании** в группе **Создать**, щелкните **Соглашение о сервисном обслуживании**, чтобы создать новое соглашение на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="8ef33-113">Введите описание, выберите проект в поле **Код проекта**, и введите дату в поле **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="8ef33-114">В поле **Объединение заказов на сервисное обслуживание** выберите **По соглашению о сервисном обслуживании**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="8ef33-115">Было создано следующее соглашение на обслуживание:</span><span class="sxs-lookup"><span data-stu-id="8ef33-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="8ef33-116">Project</span><span class="sxs-lookup"><span data-stu-id="8ef33-116">Project</span></span>      | <span data-ttu-id="8ef33-117">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="8ef33-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef33-118">Ваш проект</span><span class="sxs-lookup"><span data-stu-id="8ef33-118">Your project</span></span> | <span data-ttu-id="8ef33-119">Дата, определенной для проекта.</span><span class="sxs-lookup"><span data-stu-id="8ef33-119">The date you specified for the project.</span></span> <span data-ttu-id="8ef33-120">В этом примере текущая дата.</span><span class="sxs-lookup"><span data-stu-id="8ef33-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="8ef33-121">Создание строки соглашения на обслуживание</span><span class="sxs-lookup"><span data-stu-id="8ef33-121">Create a service agreement line</span></span>

<span data-ttu-id="8ef33-122">Затем создается строка соглашения на обслуживание, которая имеет тип проводки **Час**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="8ef33-123">Чтобы выполнить эту часть примера, можно создать 10-дневный интервал сервисного обслуживания на странице **Диапазоны сервисного обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="8ef33-124">Выберите только что созданное соглашение на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="8ef33-125">На экспресс-вкладке **Строки**, нажмите кнопку **Добавить**, чтобы создать новую строку в нижней части страницы **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="8ef33-126">В поле **Тип проводки** выберите **Час**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="8ef33-127">В поле **Работник** выберите работника, который осуществляет обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="8ef33-128">В поле **Диапазон сервисного обслуживания** выберите диапазон в 10 дней.</span><span class="sxs-lookup"><span data-stu-id="8ef33-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="8ef33-129">Была создана строка соглашения на обслуживание со следующей информацией:</span><span class="sxs-lookup"><span data-stu-id="8ef33-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="8ef33-130">Тип проводки</span><span class="sxs-lookup"><span data-stu-id="8ef33-130">Transaction type</span></span> | <span data-ttu-id="8ef33-131">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="8ef33-131">Start date</span></span>                               | <span data-ttu-id="8ef33-132">Диапазон сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="8ef33-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="8ef33-133">Часы</span><span class="sxs-lookup"><span data-stu-id="8ef33-133">Hour</span></span>             | <span data-ttu-id="8ef33-134">Текущая дата.</span><span class="sxs-lookup"><span data-stu-id="8ef33-134">The current date.</span></span>                        | <span data-ttu-id="8ef33-135">Каждые 10 дней</span><span class="sxs-lookup"><span data-stu-id="8ef33-135">Every 10 days</span></span>    |
| <span data-ttu-id="8ef33-136">Рабочий</span><span class="sxs-lookup"><span data-stu-id="8ef33-136">Worker</span></span>           | <span data-ttu-id="8ef33-137">Работник, который будет выполнять обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="8ef33-138">Нет окна времени, указанного для строки.</span><span class="sxs-lookup"><span data-stu-id="8ef33-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="8ef33-139">Создание планируемые заказов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="8ef33-139">Create planned service orders</span></span>

<span data-ttu-id="8ef33-140">Теперь можно создать планируемые заказы на обслуживание и строки заказа для наступающего месяца.</span><span class="sxs-lookup"><span data-stu-id="8ef33-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="8ef33-141">На странице **Соглашения на обслуживание** в области **Панель операций** на вкладе **Доставлять** щелкните **Планируемые заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="8ef33-142">На странице **Создать заказы на сервисное обслуживание** введите текущую дату в поле **Дата начала** и дату, отстоящую на один месяц. от текущей даты в поле **Дата окончания**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="8ef33-143">Установите ползунок **Час** в положение **Да**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="8ef33-144">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-144">Click **OK**.</span></span>

<span data-ttu-id="8ef33-145">Поскольку отсутствует группировка в заказе на обслуживание (определяется параметром **По соглашению о сервисном обслуживании** в поле **Объединение заказов на сервисное обслуживание**), на каждый заказ на обслуживание создается одна строка заказа на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="8ef33-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="8ef33-146">Созданные заказы на обслуживание</span><span class="sxs-lookup"><span data-stu-id="8ef33-146">Service orders created</span></span>

<span data-ttu-id="8ef33-147">Три строки заказа на обслуживание созданных в интервале времени, определенном в диалоговом окне **Создать заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="8ef33-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="8ef33-148">Можно просмотреть строки заказа на странице **Соглашения на обслуживание** (**Панель операций** \> вкладке **Доставлять** \> кнопке **Показать**).</span><span class="sxs-lookup"><span data-stu-id="8ef33-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ef33-149">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="8ef33-149">Related topics</span></span>

[<span data-ttu-id="8ef33-150">Настройка интервалов обслуживания</span><span class="sxs-lookup"><span data-stu-id="8ef33-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

