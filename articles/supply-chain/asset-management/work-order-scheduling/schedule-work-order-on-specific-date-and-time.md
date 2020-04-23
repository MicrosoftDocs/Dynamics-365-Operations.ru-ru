---
title: Планирование заказа на работу для конкретной даты и времени
description: В этой теме объясняется, как запланировать заказ на работу на конкретные дату и время в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215271"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="33c13-103">Планирование заказа на работу для конкретной даты и времени</span><span class="sxs-lookup"><span data-stu-id="33c13-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="33c13-104">Если заказ на работу необходимо запланировать на определенные дату *и* время, можно переопределить стандартный процесс планирования в модуле "Управление активами" и создать конкретное расписание для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="33c13-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="33c13-105">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="33c13-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="33c13-106">В списке заказов на работу щелкните код заказа на работу в столбце **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="33c13-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="33c13-107">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="33c13-107">Click **Edit**.</span></span>

4. <span data-ttu-id="33c13-108">На экспресс-вкладке **Заголовок заказа на работу** вставьте значения дат и времени в поля **Ожидаемое начало** и **Ожидаемое завершение**.</span><span class="sxs-lookup"><span data-stu-id="33c13-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Рисунок 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="33c13-110">На вкладке **Общие** щелкните **Запланировать**, чтобы использовать стандартный процесс планирования, или щелкните **Подготовить к отправке**, если требуется назначить заказ на работу конкретному работнику.</span><span class="sxs-lookup"><span data-stu-id="33c13-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="33c13-111">Чтобы переопределить любые существующие резервирования мощности, чтобы заказ на работу был запланирован в ожидаемый период, сделайте выбор, как показано на рисунке ниже, в диалоговом окне **Планирование заказа на работу** > раздел **Ограничение по мощности**.</span><span class="sxs-lookup"><span data-stu-id="33c13-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="33c13-112">Это означает, что процесс планирования будет игнорировать существующие резервирования мощности, поскольку заказ на работу должен начаться в ожидаемое время начала.</span><span class="sxs-lookup"><span data-stu-id="33c13-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Рисунок 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="33c13-114">Щелкните **ОК**, чтобы начать планирование.</span><span class="sxs-lookup"><span data-stu-id="33c13-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="33c13-115">Если в процессе планирования возникнут двойные резервирования, на экран будет выведено сообщение, и можно откорректировать соответствующие заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="33c13-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="33c13-116">Чтобы запланировать специалиста по обслуживанию для заказа на работу, этот специалист по обслуживанию должен быть доступен в ожидаемые дату и время начала работы.</span><span class="sxs-lookup"><span data-stu-id="33c13-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="33c13-117">Доступность работника настраивается в [календаре работника](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="33c13-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

