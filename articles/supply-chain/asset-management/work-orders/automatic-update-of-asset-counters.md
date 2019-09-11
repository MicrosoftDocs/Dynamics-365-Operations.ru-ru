---
title: Автоматическое обновление счетчиков основных средств
description: В этом разделе описываются автоматическое обновление счетчиков активов в модуле "Управление активами".
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875868"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="70efb-103">Автоматическое обновление счетчиков основных средств</span><span class="sxs-lookup"><span data-stu-id="70efb-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="70efb-104">В предыдущем разделе описана регистрация вручную для счетчиков активов.</span><span class="sxs-lookup"><span data-stu-id="70efb-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="70efb-105">Настройка счетчиков активов описывается в разделе [Счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="70efb-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="70efb-106">Значения счетчика также могут быть автоматически обновлены из регистраций производства на основе часов работы или произведенного количества.</span><span class="sxs-lookup"><span data-stu-id="70efb-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="70efb-107">Это выполняется в разделе **Обновление счетчиков активов**.</span><span class="sxs-lookup"><span data-stu-id="70efb-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="70efb-108">Можно обновить один или несколько активов путем вставки одного параметра, **С даты**.</span><span class="sxs-lookup"><span data-stu-id="70efb-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="70efb-109">Этот параметр определяет начальную дату для регистраций производства (количество часов или произведенное количество), что означает начальную дату, начиная с которой должны быть обновлены значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="70efb-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="70efb-110">Все активы, которые относятся к ресурсу *и* имеют счетчики активов, которые настроены для обновления на основе произведенного количества или часов производства, будут включены в автоматическое обновление, и будут созданы новые значения счетчиков.</span><span class="sxs-lookup"><span data-stu-id="70efb-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="70efb-111">Для счетчиков, основанных на количестве продукции, годное количество, а также зарегистрированное количество брака включаются в подсчет.</span><span class="sxs-lookup"><span data-stu-id="70efb-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="70efb-112">Если единица измерения, используемая для регистрации произведенного количества, отлична от единицы измерения, используемой в счетчике, количество преобразуется в соответствие с единицей измерения счетчика.</span><span class="sxs-lookup"><span data-stu-id="70efb-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="70efb-113">Как упоминалось выше, автоматические счетчики можно обновлять из производственных регистраций.</span><span class="sxs-lookup"><span data-stu-id="70efb-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="70efb-114">Поэтому актив, для которого необходимо автоматически обновлять счетчики, должен иметь отношение к ресурсу (станку).</span><span class="sxs-lookup"><span data-stu-id="70efb-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="70efb-115">Следующие описания предоставляют обзор настройки и обработки производственных заказов ( в модуле **Управление производством**), который используется в качестве основы для автоматического обновления счетчиков в активе в модуле **Управлении активами**.</span><span class="sxs-lookup"><span data-stu-id="70efb-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="70efb-116">Если для ресурса были зарегистрированы произведенные количества или рабочее время, можно обновить соответствующие счетчики активов.</span><span class="sxs-lookup"><span data-stu-id="70efb-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="70efb-117">Щелкните **Управление активами** > **Периодические операции** > **Активы** > **Обновить счетчики активов**.</span><span class="sxs-lookup"><span data-stu-id="70efb-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="70efb-118">В поле **Начальная дата** выберите дату начала автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="70efb-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="70efb-119">Дата в этом поле — это дата "незавершенного производства" из **Маршрутные проводки** (**Управление производством** > **Запросы и отчеты** > **Производство** > **Маршрутные проводки** > поле **Физ. дата**).</span><span class="sxs-lookup"><span data-stu-id="70efb-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="70efb-120">Если требуется выбрать отдельные активы, типы основных средств или ресурсы для автоматического обновления, щелкните **Фильтр** на экспресс-вкладке **Записи для добавления** и выберите требуемые настройки.</span><span class="sxs-lookup"><span data-stu-id="70efb-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="70efb-121">Если требуется, можно настроить автоматическое обновление в виде пакетного задания на экспресс-вкладке **Выполнять в фоновом режиме**.</span><span class="sxs-lookup"><span data-stu-id="70efb-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Рисунок 1](media/12-work-orders.png)

5. <span data-ttu-id="70efb-123">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="70efb-123">Click **OK**.</span></span> <span data-ttu-id="70efb-124">После завершения автоматического обновления счетчика актива можно просмотреть регистрации счетчика, соответствующие активу, разделе **Счетчики актива** (**Управление активами** > **Общее** > **Активы** > **Все активы** > выберите актив > кнопка **Счетчики**).</span><span class="sxs-lookup"><span data-stu-id="70efb-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="70efb-125">В поле **Итоговые значения счетчиков активов** можно получить обзор последней регистрации, выполненной для всех типов счетчиков во всех активах.</span><span class="sxs-lookup"><span data-stu-id="70efb-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="70efb-126">Щелкните **Управление активами** > **Запросы** > **Активы** > **Общее значение по активам**.</span><span class="sxs-lookup"><span data-stu-id="70efb-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="70efb-127">Представление очень похоже на представление **Счетчики активов**, но нельзя добавлять или изменять регистрации в представлении **Общее значение по активам**.</span><span class="sxs-lookup"><span data-stu-id="70efb-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="70efb-128">Оно используется только для обзора.</span><span class="sxs-lookup"><span data-stu-id="70efb-128">It is for overview only.</span></span>

![Рисунок 2](media/13-work-orders.png)


- <span data-ttu-id="70efb-130">Для типов счетчиков, которые автоматически обновляются, все равно можно создать регистрацию значений счетчиков вручную.</span><span class="sxs-lookup"><span data-stu-id="70efb-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="70efb-131">Дополнительные сведения см. в разделе "Обновление счетчиков активов вручную".</span><span class="sxs-lookup"><span data-stu-id="70efb-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="70efb-132">Можно настроить счетчики, имеющие отношение к другому счетчику, что означает, что при обновлении счетчика соответствующие счетчики автоматически обновляются одновременно.</span><span class="sxs-lookup"><span data-stu-id="70efb-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="70efb-133">Сведения о настройке связанных счетчиков см. в разделе [Счетчики](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="70efb-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
