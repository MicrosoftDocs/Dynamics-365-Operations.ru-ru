---
title: Создать новый проект
description: В этой теме содержится информация о том, как создать новый проект.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760643"
---
# <a name="create-a-new-project"></a><span data-ttu-id="43a20-103">Создать новый проект</span><span class="sxs-lookup"><span data-stu-id="43a20-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43a20-104">Выполните следующие действия, чтобы создать новый проект.</span><span class="sxs-lookup"><span data-stu-id="43a20-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="43a20-105">На странице **Управление проектами** выберите **Создать проект** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43a20-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="43a20-106">**Тип проекта:** Время и расходы</span><span class="sxs-lookup"><span data-stu-id="43a20-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="43a20-107">**Имя проекта:** Этап 2 обновления XYZ</span><span class="sxs-lookup"><span data-stu-id="43a20-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="43a20-108">**Группа проекта:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="43a20-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="43a20-109">**Код контракта по проекту:** 00000002</span><span class="sxs-lookup"><span data-stu-id="43a20-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="43a20-110">Выберите **Создать проект**.</span><span class="sxs-lookup"><span data-stu-id="43a20-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="43a20-111">Назначение ресурса проекту</span><span class="sxs-lookup"><span data-stu-id="43a20-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="43a20-112">На странице **Работники** в списке **Работники** выберите запись для работника, для которого вы ранее настраивали компетенции, и откройте эту запись работника.</span><span class="sxs-lookup"><span data-stu-id="43a20-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="43a20-113">В области действий на вкладке **Проект** в группе **Настройка** выберите **Назначение проектов**.</span><span class="sxs-lookup"><span data-stu-id="43a20-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="43a20-114">На странице **Назначения проектов проверок ресурсов** на вкладке **Проекты** в поле **Добавить проект к выбранным проектам** выполните фильтрацию по проекту **Этап 2 обновления XYZ**.</span><span class="sxs-lookup"><span data-stu-id="43a20-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="43a20-115">В области **Остальные проекты** области выберите проект, а затем нажмите кнопку со стрелкой, чтобы добавить его в область **Выбранные проекты**.</span><span class="sxs-lookup"><span data-stu-id="43a20-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="43a20-116">Если нужно, можно также назначить категории для ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a20-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="43a20-117">Тип категории — либо **Затраты**, либо **Выручка**.</span><span class="sxs-lookup"><span data-stu-id="43a20-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="43a20-118">Тип категории определяется вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="43a20-118">The category type is determined by your organization.</span></span> <span data-ttu-id="43a20-119">Если ресурсу не назначены категории, Finance производит поиск категории по умолчанию в стоимости часа для затрат и выручки.</span><span class="sxs-lookup"><span data-stu-id="43a20-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="43a20-120">Настройка ресурс проекта и характеристик роли</span><span class="sxs-lookup"><span data-stu-id="43a20-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="43a20-121">Менеджер проекта может использовать функцию выделения ресурсов проекта для создания ролей, необходимых для проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="43a20-122">Роли можно использовать, если во время резервирования ресурсов подтвержденные ресурсы все еще неизвестны.</span><span class="sxs-lookup"><span data-stu-id="43a20-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="43a20-123">Роли можно использовать для временного резервирования в качестве планируемых ресурсов, чтобы можно было продолжить работу над этапами планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="43a20-124">[![Пример роли](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="43a20-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="43a20-125">**Сценарий:** Contoso нанята для выполнения проекта типа "Время и расходы", у которого имеется утвержденный устав проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="43a20-126">Младший менеджер проекта все еще определяет объем работ по проекту.</span><span class="sxs-lookup"><span data-stu-id="43a20-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="43a20-127">Менеджер по ресурсам в данный момент определяет конкретные ресурсы, которые будут зарезервированы для работы на новый проект.</span><span class="sxs-lookup"><span data-stu-id="43a20-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="43a20-128">Из-за критической важности проекта одна из ролей, которую затребовал спонсор проекта, — это старший менеджер проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="43a20-129">Менеджер по ресурсам должен получить новый ресурс и определить роль в системе на тот случай, если младшему менеджеру проекта потребуются сведения о ресурсе при планировании проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="43a20-130">Следующие шаги показывают, как менеджер ресурсов может настроить роль "Старший менеджер проекта" и связать с ней характеристики ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a20-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="43a20-131">Позднее эту роль можно использовать для поиска доступных ресурсов, которые соответствуют обязательным компетенциям ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a20-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="43a20-132">На странице **Настройка ролей** выберите **Создать** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43a20-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="43a20-133">**Код роли:** Старший менеджер проекта</span><span class="sxs-lookup"><span data-stu-id="43a20-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="43a20-134">**Описание:** Старший менеджер проекта</span><span class="sxs-lookup"><span data-stu-id="43a20-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="43a20-135">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="43a20-135">Select **Create**.</span></span>
3. <span data-ttu-id="43a20-136">Выберите роль **Старший менеджер проекта**, а затем выберите **Настроить характеристики**.</span><span class="sxs-lookup"><span data-stu-id="43a20-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="43a20-137">В поле **Тип характеристик** выберите **Навык**.</span><span class="sxs-lookup"><span data-stu-id="43a20-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="43a20-138">В поле **Доступные характеристики** введите навык, который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="43a20-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="43a20-139">В поле **Тип характеристики** выберите **Сертификат**.</span><span class="sxs-lookup"><span data-stu-id="43a20-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="43a20-140">В поле **Доступные характеристики** введите тип сертификата, который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="43a20-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="43a20-141">Назначение ресурса проекта проекту</span><span class="sxs-lookup"><span data-stu-id="43a20-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="43a20-142">На странице **Все проекты** выберите проект **Этап 2 обновления XYZ**.</span><span class="sxs-lookup"><span data-stu-id="43a20-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="43a20-143">На вкладке **Проектная группа и планирование** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="43a20-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="43a20-144">В поле **Роль** выберите **Член группы**.</span><span class="sxs-lookup"><span data-stu-id="43a20-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="43a20-145">Выберите **Зарезервировать из календаря**.</span><span class="sxs-lookup"><span data-stu-id="43a20-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="43a20-146">На странице **Доступность ресурсов** выберите **Просмотр параметров**.</span><span class="sxs-lookup"><span data-stu-id="43a20-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="43a20-147">На странице **Настройка параметров представления** введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43a20-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="43a20-148">**Формат представления диапазона дат:** День</span><span class="sxs-lookup"><span data-stu-id="43a20-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="43a20-149">**Отобразить описания доступности:** Да</span><span class="sxs-lookup"><span data-stu-id="43a20-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="43a20-150">**Показать остаток мощности:** Да</span><span class="sxs-lookup"><span data-stu-id="43a20-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="43a20-151">В списке ресурсов выберите ресурс.</span><span class="sxs-lookup"><span data-stu-id="43a20-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="43a20-152">Выберите **Окончательное резервирование** и **Полная мощность**.</span><span class="sxs-lookup"><span data-stu-id="43a20-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="43a20-153">Назначение ресурса роли по умолчанию</span><span class="sxs-lookup"><span data-stu-id="43a20-153">Assign a resource to a default role</span></span>

<span data-ttu-id="43a20-154">Чтобы помочь менеджерам проекта или ресурсов, можно подробнее детализировать ресурсы, которые могут быть зарезервированы для проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="43a20-155">Можно связать роль по умолчанию с существующим ресурсом или вновь приобретенным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="43a20-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="43a20-156">Например когда Даниэль был принят на работу, у него были опыт и навыки для выполнения роли бизнес-аналитика.</span><span class="sxs-lookup"><span data-stu-id="43a20-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="43a20-157">Менеджер ресурсов назначил эту роль в качестве роли Даниэля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43a20-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="43a20-158">Таким образом, менеджер ресурсов добавил Даниэля в пул бизнес-аналитиков, которые доступны для работы над проектами.</span><span class="sxs-lookup"><span data-stu-id="43a20-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="43a20-159">Во время резервирования ресурсов менеджеры проектов могут фильтровать ресурсы ролей, доступных для работы в проектах.</span><span class="sxs-lookup"><span data-stu-id="43a20-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="43a20-160">Они могут использовать эту информацию как один из критериев, когда они выполняют анализ решений с несколькими критериями во время заполнения ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a20-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="43a20-161">Они могут также добавить другие характеристики ресурса в фильтр для поиска ресурсов с конкретными навыками, образованием и опытом для данного проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="43a20-162">**Сценарий:** утвержденный проект начался, и роль старшего менеджера проекта была зарезервирована как планируемый ресурс на стадии планирования проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="43a20-163">Менеджер по ресурсам теперь получил ресурс для заполнения роли старшего менеджера проекта.</span><span class="sxs-lookup"><span data-stu-id="43a20-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="43a20-164">На странице **Список ресурсов** выберите **Даниэль Голдшмидт**.</span><span class="sxs-lookup"><span data-stu-id="43a20-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="43a20-165">На странице **Роль ресурса** выберите **Создать** и введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43a20-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="43a20-166">**Действует:** введите текущую дату.</span><span class="sxs-lookup"><span data-stu-id="43a20-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="43a20-167">**Истечение срока:** введите **Никогда**.</span><span class="sxs-lookup"><span data-stu-id="43a20-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="43a20-168">**Роль:** введите **Старший менеджер проекта**.</span><span class="sxs-lookup"><span data-stu-id="43a20-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="43a20-169">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="43a20-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="43a20-170">На вкладке **Компетенции** добавьте навык **ProjectMgmt** и сертификат **PMP**.</span><span class="sxs-lookup"><span data-stu-id="43a20-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
