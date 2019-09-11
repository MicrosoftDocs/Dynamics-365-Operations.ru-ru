---
title: Ручное обновление счетчиков основных средств
description: В этом разделе описываются ручное обновление счетчиков активов в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875863"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="dd1c4-103">Ручное обновление счетчиков основных средств</span><span class="sxs-lookup"><span data-stu-id="dd1c4-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="dd1c4-104">Счетчики используются для создания регистраций в активе, относящихся, например, к количеству часов работы или количеству произведенных товаров.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="dd1c4-105">Если тип счетчика, выбранный для счетчика, настроен на наследование значений счетчиков (**Управление активами** > **Настройка** > **Типы активов** > **Счетчики** > экспресс-вкладка **Общие** > переключатель **Наследовать значения счетчика актива**, для которого задано значение "Да"), то при создании новой строки счетчиков этого типа все дочерние активы, использующие этот же тип счетчика, автоматически обновляются.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="dd1c4-106">В разделе **Все активы** создаются регистрации счетчика времени или количества для актива на основе показаний для актива.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="dd1c4-107">Щелкните **Управление активами** > **Общие** > **Активы** > **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="dd1c4-108">Выберите актив в списке и щелкните **Счетчики**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="dd1c4-109">В форме **Счетчики актива** отображается список всех предыдущих регистраций счетчиков для выбранного актива.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="dd1c4-110">Нажмите кнопку **Создать**, чтобы создать новую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="dd1c4-111">Код актива будет вставлен автоматически.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="dd1c4-112">В поле **Счетчик** выберите соответствующий счетчик.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="dd1c4-113">Доступны только счетчики, соответствующие типу актива, выбранному в активе.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="dd1c4-114">Связанная единица измерения автоматически вставляется в поле **Единица измерения**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="dd1c4-115">Выберите дату и время для регистрации счетчика.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="dd1c4-116">В поле **Значение** вставьте номер с момента последней регистрации счетчика, или в поле **Общее значение** введите общее число счетчика.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="dd1c4-117">При физической установке нового счетчика для актива необходимо зарегистрировать изменение в активе в разделе **Счетчики актива**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="dd1c4-118">Затем необходимо создать две строки регистрации с одинаковыми отметками времени, а в строке относительно нового счетчика установить флажок **Сброс счетчика**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="dd1c4-119">При создании двух строк регистрации первая строка должна быть задана для заменяемого счетчика.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="dd1c4-120">В поле **Итого** общее число счетчиков представляет собой сумму всех итоговых зарегистрированных значений для этого типа счетчика.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="dd1c4-121">Если установлен флажок **Сброс счетчика** для актива с использованием плана обслуживания с типом интервала "Один раз с..." или "После достижения...", счетчик по-прежнему активен в новой строке счетчика, так как создается отдельная строка счетчика, которая начинается с нового счетчика.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Рисунок 1](media/11-work-orders.png)


<span data-ttu-id="dd1c4-123">Если требуется выполнить регистрацию счетчиков на нескольких активах, это можно сделать в разделе **Управление активами** > **Запросы** > **Активы** > **Счетчики активов**.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="dd1c4-124">Можно настроить диапазон, чтобы определить отклонения в ручных регистрациях счетчиков, а также тип сообщения, которое должно отображаться, если регистрации выходят за пределы определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="dd1c4-125">Сведения о настройке счетчиков см. в теме [Счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="dd1c4-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
