---
title: Специалисты и группы специалистов по обслуживанию
description: В этом разделе описываются специалисты и группы специалистов по обслуживанию в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783534"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="51f06-103">Специалисты и группы специалистов по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="51f06-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="51f06-104">В этом разделе описываются специалисты и группы специалистов по обслуживанию в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="51f06-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="51f06-105">В «Управлении активами» можно подключить специалистов по обслуживанию к функциональным местоположениям.</span><span class="sxs-lookup"><span data-stu-id="51f06-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="51f06-106">(Для получения дополнительной информации о функциональных местоположениях см. раздел [Создание функциональных местоположений](../functional-locations/create-functional-locations.md).) Эта функциональность может быть полезна, если, например, вы планируете задание обслуживания на машине, расположенной в функциональном местоположении 01, и вы хотите распределить специалистов по обслуживанию из того же местоположения для выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="51f06-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="51f06-107">Можно также создать группы специалистов по обслуживанию и связать с ними специалистов по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="51f06-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="51f06-108">Эта функция полезна при простом планировании заказов на работу, и когда вы хотите запланировать группу специалистов по обслуживанию по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="51f06-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="51f06-109">Вы можете использовать специалистов и группы специалистов по обслуживанию для настройки предпочтительных специалистов по обслуживанию и ответственных специалистов по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="51f06-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="51f06-110">Создание работников</span><span class="sxs-lookup"><span data-stu-id="51f06-110">Create workers</span></span>

1. <span data-ttu-id="51f06-111">Выберите **Управление активами** \> **Настройка** \> **Работники** \> **Работники**.</span><span class="sxs-lookup"><span data-stu-id="51f06-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="51f06-112">Выберите **Создать** чтобы добавить работника в список.</span><span class="sxs-lookup"><span data-stu-id="51f06-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="51f06-113">В поле **Работник** выберите работника.</span><span class="sxs-lookup"><span data-stu-id="51f06-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="51f06-114">Установите параметр **Активный** на **Да**, чтобы спланировать работника по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="51f06-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="51f06-115">На экспресс-вкладке **Общее** поля **Ресурс** и **Описание** автоматически заполняются, если ресурс был выбран для работника.</span><span class="sxs-lookup"><span data-stu-id="51f06-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="51f06-116">Поле **Календарь** также автоматически заполняется при условии, что вы настроили работника в качестве ресурса и распределили календарь этому ресурсу на странице **Ресурсы** (**Администрирование организации** \> **Ресурсы** \> **Ресурсы**).</span><span class="sxs-lookup"><span data-stu-id="51f06-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="51f06-117">На экспресс-вкладке **Группы** выберите **Добавить**, а затем выберите группу специалистов по обслуживанию для работника.</span><span class="sxs-lookup"><span data-stu-id="51f06-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="51f06-118">Работник может связан с несколькими группами.</span><span class="sxs-lookup"><span data-stu-id="51f06-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="51f06-119">В стандартной настройке принадлежность работника к группе вступает в силу с даты добавления группы, и срок ее действия не ограничен.</span><span class="sxs-lookup"><span data-stu-id="51f06-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="51f06-120">Эта дата отображается в поле **Действует с**.</span><span class="sxs-lookup"><span data-stu-id="51f06-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="51f06-121">Чтобы увидеть поле **Действует с**, выберите **Просмотр** \> **Все**.</span><span class="sxs-lookup"><span data-stu-id="51f06-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="51f06-122">Если принадлежность работника к группе должна быть ограничена определенным периодом, используйте поля **Действует с** и **Действует по** для определения периода.</span><span class="sxs-lookup"><span data-stu-id="51f06-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="51f06-123">На экспресс-вкладке **Функциональные местоположения** выберите **Добавить**, а затем выберите функциональное местоположение для специалиста по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="51f06-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="51f06-124">Также укажите, какое местоположение является основным функциональным местоположением для работника.</span><span class="sxs-lookup"><span data-stu-id="51f06-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51f06-125">При добавлении функциональных местоположений работнику все активные активы, связанные с этими функциональными местоположениями, отображаются в различных пунктах меню, таких как **Мои активные активы** и **Мои активные функциональные местоположения**.</span><span class="sxs-lookup"><span data-stu-id="51f06-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="51f06-126">Они также отображаются в поисках активов, которые отображаются при создании нового актива, запроса на обслуживание или заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="51f06-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="51f06-127">Поля на экспресс-вкладке **Подробно** показывают количество групп специалистов по обслуживанию и функциональных местоположений, с которыми связан выбранный специалист по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="51f06-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="51f06-128">Создание групп работника</span><span class="sxs-lookup"><span data-stu-id="51f06-128">Create worker groups</span></span>

1. <span data-ttu-id="51f06-129">Выберите **Управление активами** \> **Настройка** \> **Работники** \> **Группы специалистов по обслуживанию**.</span><span class="sxs-lookup"><span data-stu-id="51f06-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="51f06-130">Выберите **Создать** чтобы добавить группу в список.</span><span class="sxs-lookup"><span data-stu-id="51f06-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="51f06-131">В поле **Группа специалистов по обслуживанию** введите идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="51f06-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="51f06-132">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="51f06-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="51f06-133">На экспресс-вкладке **Работники** выберите **Добавить**, а затем выберите специалиста по обслуживанию для группы специалистов.</span><span class="sxs-lookup"><span data-stu-id="51f06-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="51f06-134">Для получения информации о полях **Действует с** и **Действует по** см. шаг 6 в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="51f06-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="51f06-135">Если группа ресурсов должна быть связана с выбранной группой специалистов по обслуживанию, выберите **Копировать из группы ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="51f06-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="51f06-136">В поле **Группа** выберите группу ресурсов для копирования параметров календаря.</span><span class="sxs-lookup"><span data-stu-id="51f06-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="51f06-137">Затем в поле **Группа специалистов** выберите группу специалистов для копирования параметров календаря группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51f06-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="51f06-138">Этот шаг актуален только в том случае, если вы хотите, чтобы специалисты по обслуживанию использовали календарь, связанный с ресурсом (рабочим центром) во время планирования заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="51f06-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="51f06-139">Поле на экспресс-вкладке **Подробно** показывает количество специалистов по обслуживанию, которые были связаны с выбранной группой специалистов по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="51f06-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>