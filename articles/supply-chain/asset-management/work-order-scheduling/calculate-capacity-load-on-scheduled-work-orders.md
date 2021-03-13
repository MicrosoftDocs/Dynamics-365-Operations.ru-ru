---
title: Расчет максимальной мощности по запланированным заказам на работу
description: В этой теме объясняется, как рассчитать максимальную мощность по запланированным заказам на работу в модуле "Управление активами".
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7b7e4a20ed56b1eac29d16d527693d6e455cdc37
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021662"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="be66d-103">Расчет максимальной мощности по запланированным заказам на работу</span><span class="sxs-lookup"><span data-stu-id="be66d-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="be66d-104">Можно рассчитать максимальную мощность по запланированным заказам на работу, чтобы получить обзор рабочей нагрузки на ресурсы за указанный период.</span><span class="sxs-lookup"><span data-stu-id="be66d-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="be66d-105">Расчеты могут выполняться для следующих ресурсов: специалисты по обслуживанию, группы работников, инструменты и активы.</span><span class="sxs-lookup"><span data-stu-id="be66d-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="be66d-106">Щелкните **Управление активами** > **Запросы** > **График** > **Максимальная мощность**.</span><span class="sxs-lookup"><span data-stu-id="be66d-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="be66d-107">В диалоговом окне **Расчет максимальной мощности** > поле **Показать** выберите тип загрузки, который требуется рассчитать: **Мощность**, **Зарезервирован** или **Остаток**.</span><span class="sxs-lookup"><span data-stu-id="be66d-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="be66d-108">Если не требуется показывать результаты, содержащие нули, выберите **Да** для переключателя **Исключать нули**.</span><span class="sxs-lookup"><span data-stu-id="be66d-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="be66d-109">Выберите типы ресурсов, для которых требуется рассчитать максимальную мощность, выбрав значение **Да** для соответствующих переключателях: **Работник**, **Группа специалистов по обслуживанию**, **Инструмент** и **Актив**.</span><span class="sxs-lookup"><span data-stu-id="be66d-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="be66d-110">В поле **Начальная дата** выберите дату начала для расчета.</span><span class="sxs-lookup"><span data-stu-id="be66d-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="be66d-111">В поле **Тип интервала** выберите интервал для расчета: **День**, **Неделя**, **Месяц** или **Квартал**.</span><span class="sxs-lookup"><span data-stu-id="be66d-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="be66d-112">В поле **Частота периода** введите число интервалов, которые требуется рассчитать.</span><span class="sxs-lookup"><span data-stu-id="be66d-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="be66d-113">Например, если в качестве типа интервала выбран **День**, а в этом поле введено число "5", то будет выполнен расчет для пяти дней с даты начала.</span><span class="sxs-lookup"><span data-stu-id="be66d-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="be66d-114">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="be66d-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="be66d-115">На следующем рисунке показан результат вычисления, охватывающий три недели для типа загрузки **Зарезервирован**.</span><span class="sxs-lookup"><span data-stu-id="be66d-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Рисунок 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="be66d-117">При выборе типов загрузки **Мощность** или **Остаток** для расчета этот же результат будет отображаться, если для ресурсов в выбранном периоде не было выполнено резервирование.</span><span class="sxs-lookup"><span data-stu-id="be66d-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="be66d-118">Дополнительные сведения о том, как рассчитать максимальной мощности по строкам графика обслуживания и незапланированным заказам на работу см. в разделе [Расчет максимальной мощности](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="be66d-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

