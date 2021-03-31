---
title: Интеграция Dynamics 365 Supply Chain Management (управление активами) с Dynamics 365 Guides
description: В этой теме объясняется, как интегрировать модуль управления активами в Microsoft Dynamics 365 Supply Chain Management с Dynamics 365 Guides, чтобы пользоваться руководствами в смешанной реальности в повседневных процессах обслуживания.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: e3e9e74397faec12f6eecff1f562fd9d731ac5e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230160"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="7c6a9-103">Интеграция Dynamics 365 Supply Chain Management (управление активами) с Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="7c6a9-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="7c6a9-104">Вы можете интегрировать модуль **Управление активами** в Microsoft Dynamics 365 Supply Chain Management с Dynamics 365 Guides, чтобы пользоваться руководствами в смешанной реальности в повседневных процессах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="7c6a9-105">Если руководство связано с заказом на работу по управлению активами, работник, открывающий контрольный список обслуживания в мобильном приложении Supply Chain Management (Dynamics 365), видит, что доступно руководство.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="7c6a9-106">Работник может также найти и открыть руководство в приложении Dynamics 365 Guides HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7c6a9-107">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="7c6a9-107">Prerequisites</span></span>

<span data-ttu-id="7c6a9-108">Прежде чем прикрепить руководств к рабочим заказам на работу при управлении активами, необходимо выполнить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="7c6a9-109">[Настройте Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) версии 10.0.9 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="7c6a9-110">[Включите двойную запись для приложений Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="7c6a9-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="7c6a9-111">[Включите фокус-тестирование](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) для функции **MRGuidesFeature**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="7c6a9-112">(Для производственных сред необходимо сначала отправить запрос в службу поддержки, чтобы ваш клиент был добавлен в группу фокус-тестирования.)</span><span class="sxs-lookup"><span data-stu-id="7c6a9-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="7c6a9-113">[Включите следующие конфигурационные ключи](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) на странице **Конфигурация лицензии**:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="7c6a9-114">Управление активами \> Смешанная реальность управления активами</span><span class="sxs-lookup"><span data-stu-id="7c6a9-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="7c6a9-115">Смешанная реальность \> Руководство в смешанной реальности</span><span class="sxs-lookup"><span data-stu-id="7c6a9-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="7c6a9-116">[Настройте Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) версии 200.0.0.96 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="7c6a9-117">Используйте Dynamics 365 Guides с управлением активами</span><span class="sxs-lookup"><span data-stu-id="7c6a9-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="7c6a9-118">Чтобы установить связь с руководством, используется строка контрольного списка обслуживания в модуле управления активами.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="7c6a9-119">Связь можно создать с помощью шаблона контрольного списка обслуживания, типа задания обслуживания или заказа на работу, так как все три объекта содержат строки контрольного списка обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="7c6a9-120">Вы можете сэкономить время, используя шаблон, поскольку шаблон можно связать со всеми типами заданий обслуживания, в которых он используется.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="7c6a9-121">Например, руководство, связанное с типом задания обслуживания, автоматически связывается со всеми рабочими заказами, в которых указывается этот тип задания.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="7c6a9-122">С другой стороны, руководство, связанное непосредственно с заказом на работу, существует только для данного заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="7c6a9-123">Связывание руководства с шаблоном контрольного списка обслуживания</span><span class="sxs-lookup"><span data-stu-id="7c6a9-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="7c6a9-124">Чтобы связать руководство с шаблоном контрольного списка обслуживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="7c6a9-125">Создайте руководство с помощью приложений Dynamics 365 Guides для Windows и HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="7c6a9-126">Информацию о том, как создать руководство, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="7c6a9-127">Создание руководства с помощью приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="7c6a9-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="7c6a9-128">Использование приложения HoloLens для размещения голограмм</span><span class="sxs-lookup"><span data-stu-id="7c6a9-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="7c6a9-129">В Supply Chain Management [создайте шаблон контрольного списка обслуживания](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="7c6a9-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="7c6a9-130">Свяжите руководство, созданное в строке контрольного списка обслуживания шаблона:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="7c6a9-131">На экспресс-вкладке **Строки контрольного списка обслуживания** выберите строку, которую необходимо связать с руководством.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="7c6a9-132">На экспресс-вкладке **Связанные руководства** выберите **Добавить руководство**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="7c6a9-133">![Связывание руководства со строкой контрольного списка обслуживания](media/am-guides-integration-add-guide.png "Связывание руководства со строкой контрольного списка обслуживания")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="7c6a9-134">В поле **Имя** выберите руководство, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="7c6a9-135">![Выберите руководство в поле "Имя"](media/am-guides-integration-select-guide.png "Выберите руководство в поле "Имя"")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="7c6a9-136">Связывание шаблона контрольного списка обслуживания с типом задания:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="7c6a9-137">[Создайте тип задания обслуживания](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) или выберите существующий тип.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="7c6a9-138">В области действий выберите **Значения по умолчанию для типа заданий обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="7c6a9-139">![Кнопка "Значения по умолчанию для типа заданий обслуживания"](media/am-guides-integration-job-defaults.png "Кнопка "Значения по умолчанию для типа заданий обслуживания"")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="7c6a9-140">Создайте строку, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="7c6a9-141">![Создайте строку](media/am-guides-integration-add-line.png "Создайте строку")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="7c6a9-142">В области действий выберите **Контрольный список обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="7c6a9-143">![Кнопка "Контрольный список обслуживания"](media/am-guides-integration-maintenance-checklist.png "Кнопка "Контрольный список обслуживания"")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="7c6a9-144">На экспресс-вкладке **Строки контрольного списка обслуживания** добавьте строку, а затем измените значение в поле **Тип** на **Шаблон**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="7c6a9-145">![Изменение значения типа](media/am-guides-integration-checklist-lines.png "Изменение значения типа")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="7c6a9-146">На экспресс-вкладке **Сведения по строке** в поле **Шаблон** выберите шаблон, с которым связано данное руководство, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="7c6a9-147">![Выбор шаблона](media/am-guides-integration-checklist-line-details.png "Выбор шаблона")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="7c6a9-148">[Создайте заказ на работу](work-orders/manually-created-workorders.md#create-work-order), а затем выберите тип задания обслуживания, которое использует шаблон контрольного списка обслуживания, с которым связано руководство.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="7c6a9-149">Руководство будет автоматически связано с этим заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="7c6a9-150">![Выберите тип задания обслуживания](media/am-guides-integration-create-work-order.png "Выберите тип задания обслуживания")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="7c6a9-151">Просмотр руководства, связанного с заказом на работу и работниками:</span><span class="sxs-lookup"><span data-stu-id="7c6a9-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="7c6a9-152">Откройте [мобильную рабочую область управления активами](asset-management-mobile-workspace.md), чтобы увидеть заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="7c6a9-153">[Откройте контрольный список обслуживания](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="7c6a9-154">Выберите строку контрольного списка для просмотра связанного руководства.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="7c6a9-155">![Руководство, связанное со строкой контрольного списка](media/am-guides-integration-show-guide.png "Руководство, связанное со строкой контрольного списка")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="7c6a9-156">Откройте руководство в HoloLens.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="7c6a9-157">![Откройте руководство в HoloLens](media/am-guides-integration-hololens-select.png "Откройте руководство в HoloLens")</span><span class="sxs-lookup"><span data-stu-id="7c6a9-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="7c6a9-158">Можно также связать руководство непосредственно в контрольном списке обслуживания заказа на работу или в типе задания.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c6a9-159">Существует известная проблема, в которой при связывании шаблона контрольного списка обслуживания с типом задания обслуживания по умолчанию руководство, связанное с этим шаблоном, не появляется на экспресс-вкладке **Связанные руководства** на странице **Значения по умолчанию для типа заданий обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="7c6a9-160">Однако руководство появится там после применения этого типа заданий к заказу на работу на Экспресс-вкладке **Связанные руководства**.</span><span class="sxs-lookup"><span data-stu-id="7c6a9-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c6a9-161">См. также</span><span class="sxs-lookup"><span data-stu-id="7c6a9-161">See also</span></span>

- [<span data-ttu-id="7c6a9-162">Обзор двойной записи</span><span class="sxs-lookup"><span data-stu-id="7c6a9-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="7c6a9-163">Обзор управления активами</span><span class="sxs-lookup"><span data-stu-id="7c6a9-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]