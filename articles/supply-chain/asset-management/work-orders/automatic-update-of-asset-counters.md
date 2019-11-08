---
title: Автоматическое обновление счетчиков основных средств
description: В этом разделе описываются автоматическое обновление счетчиков активов в модуле "Управление активами".
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
ms.openlocfilehash: d51b9a7684e460d555632c3896e9dd8a4e10d92c
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626186"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="a85fd-103">Автоматическое обновление счетчиков основных средств</span><span class="sxs-lookup"><span data-stu-id="a85fd-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a85fd-104">Дополнительные сведения о регистрации счетчика активов вручную см. раздел [Обновление счетчиков актива вручную](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="a85fd-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="a85fd-105">Для получения дополнительных сведений о настройке счетчиков активов см. в разделе [счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="a85fd-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="a85fd-106">Значения счетчика также могут быть автоматически обновлены из регистраций производства на основе часов работы или произведенного количества (то есть количество, которое производится).</span><span class="sxs-lookup"><span data-stu-id="a85fd-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="a85fd-107">Это обновление выполняется на странице **обновление счетчиков активов**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="a85fd-108">Можно обновить один или несколько активов путем настройки одного параметра, **Дата начала**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="a85fd-109">Этот параметр определяет начальную дату для производственных регистраций (количество рабочих часов или количеств в производстве).</span><span class="sxs-lookup"><span data-stu-id="a85fd-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="a85fd-110">Иными словами, он указывает дату, начиная с которой должны быть обновлены значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="a85fd-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="a85fd-111">Все активы, которые относятся к ресурсу *и* имеют счетчики активов, которые настроены для обновления на основе производственных часов или произведенного количества, будут включены в автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="a85fd-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="a85fd-112">Будут созданы новые значения счетчиков.</span><span class="sxs-lookup"><span data-stu-id="a85fd-112">New counter values will be created.</span></span>

<span data-ttu-id="a85fd-113">Для счетчиков, которые основаны на производственном количестве, в расчет включается как количество товаров, так и зарегистрированное количество ошибок.</span><span class="sxs-lookup"><span data-stu-id="a85fd-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="a85fd-114">Если единица измерения, используемая для регистрации произведенного количества, отлична от единицы измерения, используемой в счетчике, количество преобразуется в соответствии с единицей измерения счетчика.</span><span class="sxs-lookup"><span data-stu-id="a85fd-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="a85fd-115">Как упоминалось выше, автоматические счетчики можно обновлять из производственных регистраций.</span><span class="sxs-lookup"><span data-stu-id="a85fd-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="a85fd-116">Поэтому актив, для которого необходимо автоматически обновлять счетчики, должен иметь отношение к ресурсу (станку).</span><span class="sxs-lookup"><span data-stu-id="a85fd-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="a85fd-117">Если для ресурса были зарегистрированы произведенные количества или рабочее время, можно обновить соответствующие счетчики активов.</span><span class="sxs-lookup"><span data-stu-id="a85fd-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="a85fd-118">Выберите **Управление активами** > **Периодические операции** > **Активы** > **Обновить счетчики активов**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="a85fd-119">В поле **Начальная дата** выберите дату начала автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="a85fd-119">In the **From date** field, select the start date of the automatic update.</span></span>

>[!NOTE]
><span data-ttu-id="a85fd-120">Дата в этом поле — это дата "незавершенного производства" из **Маршрутные проводки** (**Управление производством** > **Запросы и отчеты** > **Производство** > **Маршрутные проводки** > поле **Физ. дата**).</span><span class="sxs-lookup"><span data-stu-id="a85fd-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="a85fd-121">На экспресс-вкладке **Включаемые записи** можно выбрать отдельные активы, типы активов или ресурсы для автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="a85fd-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="a85fd-122">Выберите **Фильтр** и сделайте соответствующие выборки.</span><span class="sxs-lookup"><span data-stu-id="a85fd-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="a85fd-123">На экспресс-вкладке **Выполнять в фоновом режиме** можно настроить автоматическое обновление в виде пакетного задания, по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a85fd-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

<span data-ttu-id="a85fd-124">На приведенном ниже рисунке показан пример диалогового окна **Обновление счетчиков активов**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

![Рисунок 1](media/12-work-orders.png)

5. <span data-ttu-id="a85fd-126">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-126">Select **OK**.</span></span> 

<span data-ttu-id="a85fd-127">После завершения автоматического обновления счетчика активов можно просмотреть регистрации счетчика, относящиеся к активу на странице **счетчики активов**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="a85fd-128">Выберите **Управление активами** > **Общее** > **Активы** > **Все активы**, выберите актив, затем в области действий на вкладке **Активы** в группе **Профилактическое** выберите **Счетчики**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="a85fd-129">На странице **Общее значение по активам** можно получить обзор последней регистрации, выполненной для всех типов счетчиков во всех активах.</span><span class="sxs-lookup"><span data-stu-id="a85fd-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="a85fd-130">Выберите **Управление активами** > **Запросы** > **Активы** > **Общее значение по активам**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="a85fd-131">Эта страница похожа на страницу **счетчики активов**, но добавлять или изменять регистрации нельзя.</span><span class="sxs-lookup"><span data-stu-id="a85fd-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="a85fd-132">Она используется только для обзора.</span><span class="sxs-lookup"><span data-stu-id="a85fd-132">It's for overview only.</span></span>

<span data-ttu-id="a85fd-133">На приведенном ниже рисунке показан пример страницы **Общее значение по активам**.</span><span class="sxs-lookup"><span data-stu-id="a85fd-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Рисунок 2](media/13-work-orders.png)

<span data-ttu-id="a85fd-135">Обратите внимание на следующие аспекты:</span><span class="sxs-lookup"><span data-stu-id="a85fd-135">Note the following points:</span></span>

- <span data-ttu-id="a85fd-136">Для типов счетчиков, которые автоматически обновляются, все еще можно создать регистрацию значений счетчиков вручную.</span><span class="sxs-lookup"><span data-stu-id="a85fd-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="a85fd-137">Дополнительные сведения см. в разделе [Обновление счетчиков активов вручную](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="a85fd-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="a85fd-138">Можно настроить счетчики, имеющие отношение к другому счетчику.</span><span class="sxs-lookup"><span data-stu-id="a85fd-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="a85fd-139">В этом случае при обновлении счетчика соответствующие счетчики автоматически обновляются в то же время.</span><span class="sxs-lookup"><span data-stu-id="a85fd-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="a85fd-140">Дополнительные сведения о настройке связанных счетчиков см. в разделе [Счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="a85fd-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

