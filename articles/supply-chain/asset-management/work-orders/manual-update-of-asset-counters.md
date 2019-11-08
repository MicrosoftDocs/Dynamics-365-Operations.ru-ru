---
title: Ручное обновление счетчиков основных средств
description: В этом разделе описываются ручное обновление счетчиков активов в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3072ab204b53b16988d2973b28a697041cb84c27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626147"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="c6fae-103">Ручное обновление счетчиков основных средств</span><span class="sxs-lookup"><span data-stu-id="c6fae-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c6fae-104">Счетчики используются для создания регистраций для актива, например регистрации количества часов, в течение которых актив был в эксплуатации, или количества, которое было произведено.</span><span class="sxs-lookup"><span data-stu-id="c6fae-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="c6fae-105">Для типа счетчика, выбранного для счетчика, можно настроить наследование значений счетчиков.</span><span class="sxs-lookup"><span data-stu-id="c6fae-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="c6fae-106">Другими словами, параметр **Наследовать значения счетчика актива** имеет значение **да** на экспресс-вкладке **общие** на странице **счетчики** (**Управление активами** > **Настройка** > **Типы активов** > **Счетчики**).</span><span class="sxs-lookup"><span data-stu-id="c6fae-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="c6fae-107">В этом случае при создании новой строки счетчиков этого типа все дочерние активы, использующие один и тот же тип счетчика, автоматически обновляются.</span><span class="sxs-lookup"><span data-stu-id="c6fae-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="c6fae-108">На странице **Все активы** создаются регистрации счетчика времени или количества для актива на основе показаний для актива.</span><span class="sxs-lookup"><span data-stu-id="c6fae-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="c6fae-109">Выберите **Управление активами** > **Общие** > **Активы** > **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="c6fae-110">Выберите актив, затем в области действий на вкладке **Актив** в группе **Профилактическое** выберите **Счетчики**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="c6fae-111">Страница **Счетчики актива** отображает список всех предыдущих регистраций счетчиков, которые были сделаны для выбранного актива.</span><span class="sxs-lookup"><span data-stu-id="c6fae-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="c6fae-112">Выберите **Создать** для создания регистрации.</span><span class="sxs-lookup"><span data-stu-id="c6fae-112">Select **New** to create a registration.</span></span> <span data-ttu-id="c6fae-113">Код актива автоматически вводится в поле **Актив**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="c6fae-114">В поле **Счетчик** выберите соответствующий счетчик.</span><span class="sxs-lookup"><span data-stu-id="c6fae-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="c6fae-115">Для выбора доступны только счетчики, соответствующие типу актива, выбранному в активе.</span><span class="sxs-lookup"><span data-stu-id="c6fae-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="c6fae-116">Связанная единица измерения автоматически вводится в поле **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="c6fae-117">В поле **зарегистрировано** выберите дату и время для регистрации счетчика.</span><span class="sxs-lookup"><span data-stu-id="c6fae-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="c6fae-118">В поле **значение** введите номер с момента последней регистрации счетчика.</span><span class="sxs-lookup"><span data-stu-id="c6fae-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="c6fae-119">В качестве альтернативы в поле **Общее значение** введите общее число счетчика.</span><span class="sxs-lookup"><span data-stu-id="c6fae-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="c6fae-120">Обратите внимание на следующие аспекты:</span><span class="sxs-lookup"><span data-stu-id="c6fae-120">Note the following points:</span></span>

- <span data-ttu-id="c6fae-121">При физической установке нового счетчика для актива необходимо зарегистрировать изменение в активе на странице **Счетчики актива**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="c6fae-122">Затем необходимо создать две строки регистрации с одинаковыми метками времени.</span><span class="sxs-lookup"><span data-stu-id="c6fae-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="c6fae-123">Первая строка должна относиться к заменяемому счетчику.</span><span class="sxs-lookup"><span data-stu-id="c6fae-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="c6fae-124">В строке, которая относится к новому счетчику, установите флажок **Сброс счетчика**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="c6fae-125">В поле **Итого** общее число счетчиков представляет собой сумму всех итоговых зарегистрированных значений для этого типа счетчика.</span><span class="sxs-lookup"><span data-stu-id="c6fae-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="c6fae-126">Если установлен флажок **Сброс счетчика** для актива с использованием плана обслуживания с типом интервала "Один раз с..." или "После достижения...", счетчик по-прежнему активен в новой строке счетчика, так как создается отдельная строка счетчика, которая начинается с нового счетчика.</span><span class="sxs-lookup"><span data-stu-id="c6fae-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="c6fae-127">На приведенном ниже рисунке показан пример страницы **Счетчики актива**.</span><span class="sxs-lookup"><span data-stu-id="c6fae-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Рисунок 1](media/11-work-orders.png)

<span data-ttu-id="c6fae-129">На странице **Счетчики актива** (**Управление активами** > **Запросы** > **Активы** > **Счетчики актива**), можно выполнять регистрацию счетчика на нескольких активах одновременно, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c6fae-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="c6fae-130">Можно настроить диапазон для определения отклонений в регистрациях счетчиков вручную.</span><span class="sxs-lookup"><span data-stu-id="c6fae-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="c6fae-131">Можно также указать тип сообщения, которое будет отображаться, если регистрации выходят за пределы определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="c6fae-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="c6fae-132">Дополнительные сведения о настройке счетчиков см. в разделе [Счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="c6fae-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

