---
title: Настройка ресурсов проектов
description: В этой теме приводятся сведения о настройке или запросе ресурсов для проекта.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760648"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="f491e-103">Настройка ресурсов проектов</span><span class="sxs-lookup"><span data-stu-id="f491e-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f491e-104">Необходимо настроить календарь и связать его с сотрудником или работником.</span><span class="sxs-lookup"><span data-stu-id="f491e-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="f491e-105">Календарь используется для планирования проекта и рабочего времени ресурсов, которые зарезервированы для проекта.</span><span class="sxs-lookup"><span data-stu-id="f491e-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="f491e-106">При настройке календаря менеджеры проектов могут выполнять выравнивание ресурсов как часть оптимизации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f491e-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="f491e-107">На основе расписания календаря на ресурсы можно накладывать ограничения.</span><span class="sxs-lookup"><span data-stu-id="f491e-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="f491e-108">Можно настроить календарь на странице **Календари**.</span><span class="sxs-lookup"><span data-stu-id="f491e-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="f491e-109">При настройке работника в качестве ресурса проекта можно выбирать из сотрудников, работающих в компании, для которой выполняется настройка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f491e-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="f491e-110">Также можно выбирать работников из других компаний в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f491e-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="f491e-111">Эти работники называются внутрихолдинговыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="f491e-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="f491e-112">Следующие процедуры показывают, как настроить работника в качестве ресурса проекта в рамках вашей компании, а также как настроить внутрихолдинговый ресурс проекта.</span><span class="sxs-lookup"><span data-stu-id="f491e-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="f491e-113">Настройка работника в качестве ресурса проекта</span><span class="sxs-lookup"><span data-stu-id="f491e-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="f491e-114">На странице **Работники** в списке **Работники** выберите работника, добавленного как ресурс проекта, и откройте запись работника.</span><span class="sxs-lookup"><span data-stu-id="f491e-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="f491e-115">В области действий выберите **Проект** &gt; **Настройка** &gt; **Настройка проекта**.</span><span class="sxs-lookup"><span data-stu-id="f491e-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="f491e-116">Выберите календарь, затем закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f491e-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="f491e-117">Можно также указать проекты по умолчанию для ресурса в качестве типа предварительного назначения.</span><span class="sxs-lookup"><span data-stu-id="f491e-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="f491e-118">Предварительные назначения можно использовать, когда менеджер ресурсов или менеджер проекта заранее знают, над какими проектами будет работать ресурс.</span><span class="sxs-lookup"><span data-stu-id="f491e-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="f491e-119">Предварительные назначения могут также основываться на запросе спонсора проекта или клиента.</span><span class="sxs-lookup"><span data-stu-id="f491e-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="f491e-120">Чтобы задать предварительные назначения для проекта, на странице **Назначение проектов** на вкладке **Проекты** в списке **Остальные проекты** выберите соответствующий проект.</span><span class="sxs-lookup"><span data-stu-id="f491e-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="f491e-121">Настройка внутрихолдингового ресурса</span><span class="sxs-lookup"><span data-stu-id="f491e-121">Set up an intercompany resource</span></span>

<span data-ttu-id="f491e-122">При настройке работника в качестве внутрихолдингового ресурса необходимо выполнить настройку и в компании-арендодателе и в заимствующей компании.</span><span class="sxs-lookup"><span data-stu-id="f491e-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="f491e-123">В компании-арендодателе</span><span class="sxs-lookup"><span data-stu-id="f491e-123">In the lending company</span></span>

1. <span data-ttu-id="f491e-124">В Finance убедитесь, что выбрана компания-арендодатель, затем выполните процедуру, описанную в предыдущем разделе, "Настройка работника в качестве ресурса проекта".</span><span class="sxs-lookup"><span data-stu-id="f491e-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="f491e-125">На странице **Внутрихолдинговый учет** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f491e-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="f491e-126">В поле **Код информации о компании** выберите компанию-арендодателя.</span><span class="sxs-lookup"><span data-stu-id="f491e-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="f491e-127">Требуемым образом заполните оставшиеся поля и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f491e-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="f491e-128">На странице **Трансферная цена** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f491e-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="f491e-129">В поле **Получающая информация о компании** выберите заимствующую компанию.</span><span class="sxs-lookup"><span data-stu-id="f491e-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="f491e-130">Чтобы передать в аренду заимствующей компании только ресурс, созданный в начале этого раздела, в поле **Ресурс** выберите имя ресурса, который вы создали.</span><span class="sxs-lookup"><span data-stu-id="f491e-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="f491e-131">Чтобы все ресурсы в компании-арендодателе были доступны заимствующей компании, оставьте поле **Ресурс** пустым.</span><span class="sxs-lookup"><span data-stu-id="f491e-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="f491e-132">На странице **Параметры модуля "Управление и учет по проектам"** на вкладке **Внутрихолдинговый** выберите в поле **Включить планирование и графики внутрихолдинговых ресурсов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f491e-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="f491e-133">В заимствующей компании</span><span class="sxs-lookup"><span data-stu-id="f491e-133">In the borrowing company</span></span>

- <span data-ttu-id="f491e-134">На странице **Список ресурсов** в фильтре поиска введите имя ресурса, созданного для компании-арендодателя, чтобы убедиться, что это имя включено в список ресурсов для заимствующей компании.</span><span class="sxs-lookup"><span data-stu-id="f491e-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="f491e-135">Запрос ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="f491e-135">Request project resources</span></span>
<span data-ttu-id="f491e-136">Функциональность для планирования ресурсов проекта позволяет менеджерам ресурсов только распределять укомплектованные ресурсы по обязательствам или проектам.</span><span class="sxs-lookup"><span data-stu-id="f491e-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="f491e-137">Чтобы включить эту функциональность, выполните следующие задачи или убедитесь, что они уже выполнены:</span><span class="sxs-lookup"><span data-stu-id="f491e-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="f491e-138">Настройка номерных серий.</span><span class="sxs-lookup"><span data-stu-id="f491e-138">Set up number sequences.</span></span>
- <span data-ttu-id="f491e-139">Настройте workflow-процессы управления и учета по проектам.</span><span class="sxs-lookup"><span data-stu-id="f491e-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="f491e-140">Включение workflow-процессов запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="f491e-140">Enable resource request workflows.</span></span>

<span data-ttu-id="f491e-141">После выполнения предыдущих задач можно выполнить необходимые из следующих задач:</span><span class="sxs-lookup"><span data-stu-id="f491e-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="f491e-142">Создание запроса ресурса из предварительно зарезервированного укомплектованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="f491e-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="f491e-143">Мониторинг запросов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f491e-143">Monitor resource requests.</span></span>
- <span data-ttu-id="f491e-144">Обеспечение запросов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f491e-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="f491e-145">Запрос укомплектованного ресурса из СДР.</span><span class="sxs-lookup"><span data-stu-id="f491e-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="f491e-146">Резервирование ресурсов для проекта без запроса укомплектованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="f491e-146">Book resources to a project without having a request for a staffed resource.</span></span>
