---
title: Расчет максимальной мощности
description: В этом разделе описывается, как рассчитать максимальную мощность в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 82f65293679591f278e0e3b79c112ba36debc3bb
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2019
ms.locfileid: "2277951"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="1c19e-103">Расчет максимальной мощности</span><span class="sxs-lookup"><span data-stu-id="1c19e-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1c19e-104">В управлении активами можно рассчитать максимальную мощность</span><span class="sxs-lookup"><span data-stu-id="1c19e-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="1c19e-105">строки графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="1c19e-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="1c19e-106">заказы на работу, которые еще не были запланированы</span><span class="sxs-lookup"><span data-stu-id="1c19e-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="1c19e-107">запланированные заказы на работу</span><span class="sxs-lookup"><span data-stu-id="1c19e-107">scheduled work orders</span></span>

<span data-ttu-id="1c19e-108">Это полезно, если требуется получить обзор ожидаемой загрузки мощностей за конкретный период.</span><span class="sxs-lookup"><span data-stu-id="1c19e-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="1c19e-109">Расчет максимальной мощности может выполняться по всем активам или по выбранным активам.</span><span class="sxs-lookup"><span data-stu-id="1c19e-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="1c19e-110">Кроме того, можно выполнить расчет для мероприятий по простою из-за обслуживания или для пулов заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="1c19e-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="1c19e-111">Щелкните **Управление активами** > **Запросы** > **Максимальная мощность** или **Управление активами** > **Общее** > **Пулы заказов на работу** > **Все пулы заказов на работу** / **Активные пулы заказов на работу** > выберите пул заказов на работу в списке > кнопка **Максимальная мощность** или **Управление активами** > **Общее** > **Мероприятия по простою из-за обслуживания** > **Все мероприятия по простою из-за обслуживания** / **Активные мероприятия по простою из-за обслуживания** > выберите мероприятие по простою из-за обслуживания в списке > кнопка **Максимальная мощность**.</span><span class="sxs-lookup"><span data-stu-id="1c19e-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="1c19e-112">В диалоговом окне **Рассчитать максимальную мощность** выберите период для расчета в полях **Дата и время начала** и **Дата и время окончания**.</span><span class="sxs-lookup"><span data-stu-id="1c19e-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="1c19e-113">Выберите "Да" на кнопке-переключателе **Включить график обслуживания**, если требуется включить строки графика обслуживания в расчет.</span><span class="sxs-lookup"><span data-stu-id="1c19e-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="1c19e-114">Выберите "Да" на кнопке-переключателе **Включить заказ на работу**, если требуется включить задания заказа на работу в расчет.</span><span class="sxs-lookup"><span data-stu-id="1c19e-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="1c19e-115">Можно использовать поле **Уровень**, чтобы указать, насколько подробным должны быть строки загрузки мощностей относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="1c19e-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="1c19e-116">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки графика обслуживания и заказы на работу для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="1c19e-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="1c19e-117">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки графика обслуживания и все заказы на работу на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="1c19e-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="1c19e-118">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="1c19e-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="1c19e-119">В группах панели операций **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="1c19e-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="1c19e-120">Выбранные кнопки группы панели операций выделяются синим цветом.</span><span class="sxs-lookup"><span data-stu-id="1c19e-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="1c19e-121">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="1c19e-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="1c19e-122">На следующем рисунке показан пример интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1c19e-122">The figure below shows an example of the interface.</span></span>

![Рисунок 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="1c19e-124">Если требуется сосредоточиться только на планировании мощностей по запланированным заказам на работу, см. раздел [Расчет максимальной мощности по запланированным заказам на работу](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1c19e-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

