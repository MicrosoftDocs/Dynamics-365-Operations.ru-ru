---
title: Настройка пути с несколькими отрезками
description: В этой теме описывается, как настроить пути с несколькими отрезками для модуля "Стоимость на складе".
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 88e1d94f7c3a9b624447c5fc000afc3faab395f1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500438"
---
# <a name="multi-leg-journey-setup"></a><span data-ttu-id="acd1a-103">Настройка пути с несколькими отрезками</span><span class="sxs-lookup"><span data-stu-id="acd1a-103">Multi-leg journey setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="acd1a-104">В этой теме описывается, как настроить пути с несколькими отрезками для модуля **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="acd1a-104">This topic describes how to set up multi-leg journeys for the **Landed cost** module.</span></span>

## <a name="legs"></a><span data-ttu-id="acd1a-105">Участки пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-105">Legs</span></span>

<span data-ttu-id="acd1a-106">Отрезки используются для идентификации отдельных частей пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-106">Legs are used to identify separate parts of a journey.</span></span> <span data-ttu-id="acd1a-107">Каждый отрезок создается путем выбора портов отгрузки "из" и "в" и метода транспортировки, используемого для этого отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-107">Each leg is built by selecting the "to" and "from" shipping ports, and the transportation method that is used for that leg.</span></span> <span data-ttu-id="acd1a-108">Время упреждения может быть связано с каждым отрезком.</span><span class="sxs-lookup"><span data-stu-id="acd1a-108">Lead times can be associated with each leg.</span></span> <span data-ttu-id="acd1a-109">Время упреждения может помочь отслеживать отгрузку и может также использоваться для расчета ожидаемой даты поставки товаров в рейсе.</span><span class="sxs-lookup"><span data-stu-id="acd1a-109">Lead times can help track a shipment and can also be used to calculate the estimated delivery date of the goods on a voyage.</span></span> <span data-ttu-id="acd1a-110">Кроме того, когда отрезок пути завершен, статус рейса, контейнера отгрузки и связанных строк заказа на покупку можно обновить с помощью настройки управления отслеживанием.</span><span class="sxs-lookup"><span data-stu-id="acd1a-110">Additionally, when a leg of a journey is completed, the status of the voyage, shipping container, and associated purchase order lines can be updated through the tracking control setup.</span></span> <span data-ttu-id="acd1a-111">Отрезки могут использоваться одним шаблоном пути или могут быть повторно использованы в нескольких шаблонах пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-111">Legs can be used by a single journey template, or they can be reused by multiple journey templates.</span></span> <span data-ttu-id="acd1a-112">Загрузка контейнера, таможенные процедуры и местная транспортировка обычно настраиваются как отрезки, и для них используется не конкретный порт отгрузки.</span><span class="sxs-lookup"><span data-stu-id="acd1a-112">Container loading, customs, and local transport are generally set up as legs, and a non-specific shipping port is used for them.</span></span>

<span data-ttu-id="acd1a-113">Для работы с отрезками перейдите **Стоимость на складе \> Настройка пути с несколькими отрезками \> Отрезки**.</span><span class="sxs-lookup"><span data-stu-id="acd1a-113">To work with legs, go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="acd1a-114">Там можно просматривать, открывать, создавать и удалять записи для отрезков.</span><span class="sxs-lookup"><span data-stu-id="acd1a-114">There, you can view, open, create, and delete records for legs.</span></span> <span data-ttu-id="acd1a-115">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="acd1a-115">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="acd1a-116">Поле</span><span class="sxs-lookup"><span data-stu-id="acd1a-116">Field</span></span> | <span data-ttu-id="acd1a-117">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-117">Description</span></span> |
|---|---|
| <span data-ttu-id="acd1a-118">Участок пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-118">Leg</span></span> | <span data-ttu-id="acd1a-119">Введите уникальное идентификационное имя/номер для отрезка пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-119">Enter a unique identification name/number for the journey leg.</span></span> |
| <span data-ttu-id="acd1a-120">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-120">Description</span></span> | <span data-ttu-id="acd1a-121">Введите описание отрезка журнала.</span><span class="sxs-lookup"><span data-stu-id="acd1a-121">Enter a description of the journey leg.</span></span> <span data-ttu-id="acd1a-122">Обычно это описание определяет порты "в" и "из" или этап пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-122">Typically, this description identifies the "to" and "from" ports, or the step of the journey.</span></span> |
| <span data-ttu-id="acd1a-123">Порт отправления</span><span class="sxs-lookup"><span data-stu-id="acd1a-123">From port</span></span> | <span data-ttu-id="acd1a-124">Введите место происхождения товаров в отрезке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-124">Enter the point of origin of the goods on the leg.</span></span> |
| <span data-ttu-id="acd1a-125">Порт назначения</span><span class="sxs-lookup"><span data-stu-id="acd1a-125">To port</span></span> | <span data-ttu-id="acd1a-126">Введите место назначения товаров в отрезке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-126">Enter the point of destination of the goods on the leg.</span></span> |
| <span data-ttu-id="acd1a-127">Способ доставки</span><span class="sxs-lookup"><span data-stu-id="acd1a-127">Delivery method</span></span> | <span data-ttu-id="acd1a-128">Введите способ транспортировки для отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-128">Enter the method of transport for the leg.</span></span> |

## <a name="journey-templates"></a><span data-ttu-id="acd1a-129">Шаблоны пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-129">Journey templates</span></span>

<span data-ttu-id="acd1a-130">Шаблон пути определяет путь с несколькими отрезками между двумя портами, в которые перемещаются товары во время рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-130">A journey template defines the multi-leg journey between two ports that goods travel during a voyage.</span></span> <span data-ttu-id="acd1a-131">Отрезки пути комбинируются для определения количества времени, которое потребуется для перемещения товаров от места происхождения поставщика до конечного склада назначения.</span><span class="sxs-lookup"><span data-stu-id="acd1a-131">The legs of the journey are combined to identify the amount of time that will be required for goods to travel from the vendor's point of origin to the final warehouse destination.</span></span> <span data-ttu-id="acd1a-132">Когда отрезки вносятся в шаблон пути в конкретном заказе, время упреждения будет определять дату каждого отрезка и статус рейса, контейнера и строк покупки для рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-132">When the legs are put on the journey template in a specific order, the lead times will identify the date of each leg and status of the voyage, container, and purchase lines for the voyage.</span></span> <span data-ttu-id="acd1a-133">[Центр управления отслеживания](delivery-information-setup.md) используется для настройки времени упреждения, связанного с каждым отрезком, из которых состоит шаблон пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-133">You use the [Tracking control center](delivery-information-setup.md) to set up the lead times that are associated with each leg that makes up the journey template.</span></span> <span data-ttu-id="acd1a-134">Шаблон пути также используется при настройке автоматических затрат рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-134">The journey template is also used when the automatic costs of a voyage are set up.</span></span> <span data-ttu-id="acd1a-135">Когда определяется путь, затраты, связанные с транспортировкой товаров, могут быть определены на странице автоматических затрат.</span><span class="sxs-lookup"><span data-stu-id="acd1a-135">When a journey is defined, the cost that is associated with the transport of the goods can be defined on the auto costs page.</span></span>

<span data-ttu-id="acd1a-136">Для работы с шаблонами пути перейдите **Стоимость на складе \> Настройка пути с несколькими отрезками \> Шаблоны пути**.</span><span class="sxs-lookup"><span data-stu-id="acd1a-136">To work with journey templates, go to **Landed cost \> Multi-leg journey setup \> Journey templates**.</span></span> <span data-ttu-id="acd1a-137">Там можно просматривать, открывать, создавать и удалять шаблоны пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-137">There, you can view, open, create, and delete journey templates.</span></span>

<span data-ttu-id="acd1a-138">Для каждого шаблона пути установите следующие поля в заголовке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-138">For each journey template, set the following fields on the header.</span></span>

| <span data-ttu-id="acd1a-139">Поле</span><span class="sxs-lookup"><span data-stu-id="acd1a-139">Field</span></span> | <span data-ttu-id="acd1a-140">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-140">Description</span></span> |
|---|---|
| <span data-ttu-id="acd1a-141">Шаблон пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-141">Journey template</span></span> | <span data-ttu-id="acd1a-142">Введите уникальное идентификационное имя/номер для шаблона пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-142">Enter a unique identification name/number for the journey template.</span></span> <span data-ttu-id="acd1a-143">Шаблон пути обычно описывает место происхождения и место назначения для пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-143">The journey template typically describes the point of origin and point of destination for the journey.</span></span> |
| <span data-ttu-id="acd1a-144">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-144">Description</span></span> | <span data-ttu-id="acd1a-145">Введите описание шаблона пути.</span><span class="sxs-lookup"><span data-stu-id="acd1a-145">Enter a description of the journey template.</span></span> <span data-ttu-id="acd1a-146">Описание обычно указывает на порты "в" и "из" и тип перемещения.</span><span class="sxs-lookup"><span data-stu-id="acd1a-146">The description typically indicates the "to" and "from" ports, and the type of travel.</span></span> |

<span data-ttu-id="acd1a-147">В разделе **Строки** добавьте строку для каждого отрезка пути и разместите строки в порядке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-147">In the **Lines** section, add a line for each leg of the journey, and put the lines in order.</span></span> <span data-ttu-id="acd1a-148">Для изменения порядка строк можно использовать стрелки **вверх** и **вниз** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="acd1a-148">Use the **Up** and **Down** arrows on the toolbar to change the order of the lines.</span></span> <span data-ttu-id="acd1a-149">В следующей таблице описываются поля, которые доступны для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="acd1a-149">The following table describes the fields that are available for each line.</span></span>

| <span data-ttu-id="acd1a-150">Поле</span><span class="sxs-lookup"><span data-stu-id="acd1a-150">Field</span></span> | <span data-ttu-id="acd1a-151">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-151">Description</span></span> |
|---|---|
| <span data-ttu-id="acd1a-152">Участок пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-152">Leg</span></span> | <span data-ttu-id="acd1a-153">Выберите отрезок для добавления в путь.</span><span class="sxs-lookup"><span data-stu-id="acd1a-153">Select a leg to add to the journey.</span></span> |
| <span data-ttu-id="acd1a-154">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-154">Description</span></span> | <span data-ttu-id="acd1a-155">Описание отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-155">The description of the leg.</span></span> |
| <span data-ttu-id="acd1a-156">Порт отправления</span><span class="sxs-lookup"><span data-stu-id="acd1a-156">From port</span></span> | <span data-ttu-id="acd1a-157">Порт, который является местом происхождения товаров в отрезке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-157">The port that is the point of origin of the goods on the leg.</span></span> <span data-ttu-id="acd1a-158">Этот порт является портом "в", используемым для определения автоматических затрат для рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-158">This port is the "to" port that is used to determine the auto costs for a voyage.</span></span> |
| <span data-ttu-id="acd1a-159">Порт назначения</span><span class="sxs-lookup"><span data-stu-id="acd1a-159">To port</span></span> | <span data-ttu-id="acd1a-160">Окончательный порт назначения товаров в отрезке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-160">The final destination port of the goods on the leg.</span></span> |
| <span data-ttu-id="acd1a-161">Способ поставки</span><span class="sxs-lookup"><span data-stu-id="acd1a-161">Mode of delivery</span></span> | <span data-ttu-id="acd1a-162">Способ доставки, используемый для отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-162">The mode of delivery that is used for the leg.</span></span> |
| <span data-ttu-id="acd1a-163">Порт отправления пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-163">Journey from port</span></span> | <span data-ttu-id="acd1a-164">Если порт, указанный для отрезка, используется для определения автоматических затрат, установите этот флажок, чтобы указать, что он является портом, из которого начинается путь.</span><span class="sxs-lookup"><span data-stu-id="acd1a-164">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey from" port.</span></span> <span data-ttu-id="acd1a-165">Этот порт будет отображаться в заголовке рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-165">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="acd1a-166">Порт назначения пути</span><span class="sxs-lookup"><span data-stu-id="acd1a-166">Journey to port</span></span> | <span data-ttu-id="acd1a-167">Если порт, указанный для отрезка, используется для определения автоматических затрат, установите этот флажок, чтобы указать, что он является портом, в котором заканчивается путь.</span><span class="sxs-lookup"><span data-stu-id="acd1a-167">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey to" port.</span></span> <span data-ttu-id="acd1a-168">Этот порт будет отображаться в заголовке рейса.</span><span class="sxs-lookup"><span data-stu-id="acd1a-168">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="acd1a-169">Компания по отгрузке</span><span class="sxs-lookup"><span data-stu-id="acd1a-169">Shipping company</span></span> | <span data-ttu-id="acd1a-170">Выберите транспортную компанию, которая используется для этого отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-170">Select the shipping company that is used for the leg.</span></span> |

## <a name="activities"></a><span data-ttu-id="acd1a-171">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="acd1a-171">Activities</span></span>

<span data-ttu-id="acd1a-172">Настройки на странице **Мероприятия** определяют типы мероприятий, которые могут выполняться в порту назначения отрезка.</span><span class="sxs-lookup"><span data-stu-id="acd1a-172">The settings on the **Activities** page establish the types of activities that can occur at the destination port of a leg.</span></span> <span data-ttu-id="acd1a-173">Пользователи, работающие на странице **Все контейнеры отгрузки**, могут выбирать среди этих значений при оценке длительности каждого мероприятия и регистрации фактической длительности для сравнения.</span><span class="sxs-lookup"><span data-stu-id="acd1a-173">Users who work on the **All shipping containers** page can select among these values when they estimate the duration of each activity and record the actual duration for comparison purposes.</span></span>

<span data-ttu-id="acd1a-174">Для настройки мероприятий перейдите **Стоимость на складе \> Настройка путей с несколькими отрезками \> Мероприятия**.</span><span class="sxs-lookup"><span data-stu-id="acd1a-174">To set up your activities, go to **Landed cost \> Multi-leg journeys setup \> Activities**.</span></span> <span data-ttu-id="acd1a-175">Здесь можно использовать кнопки на панели операций для добавления, удаления и редактирования мероприятий.</span><span class="sxs-lookup"><span data-stu-id="acd1a-175">There, you can add, remove, and edit activities by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="acd1a-176">В следующей таблице описываются поля, которые доступны для каждого мероприятия в сетке.</span><span class="sxs-lookup"><span data-stu-id="acd1a-176">The following table describes the fields that are available for each activity in the grid.</span></span>

| <span data-ttu-id="acd1a-177">Поле</span><span class="sxs-lookup"><span data-stu-id="acd1a-177">Field</span></span> | <span data-ttu-id="acd1a-178">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-178">Description</span></span> |
|---|---|
| <span data-ttu-id="acd1a-179">Деятельность</span><span class="sxs-lookup"><span data-stu-id="acd1a-179">Activity</span></span> | <span data-ttu-id="acd1a-180">Имя мероприятия.</span><span class="sxs-lookup"><span data-stu-id="acd1a-180">The name of the activity.</span></span> |
| <span data-ttu-id="acd1a-181">описание</span><span class="sxs-lookup"><span data-stu-id="acd1a-181">Description</span></span> | <span data-ttu-id="acd1a-182">Описание мероприятия.</span><span class="sxs-lookup"><span data-stu-id="acd1a-182">A description of the activity.</span></span> |
| <span data-ttu-id="acd1a-183">Компания по отгрузке</span><span class="sxs-lookup"><span data-stu-id="acd1a-183">Shipping company</span></span> | <span data-ttu-id="acd1a-184">Счет поставщика транспортной компании, связанный с мероприятием.</span><span class="sxs-lookup"><span data-stu-id="acd1a-184">The vendor account of the shipping company that is associated with the activity.</span></span> |