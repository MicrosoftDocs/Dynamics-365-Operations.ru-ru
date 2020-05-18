---
title: Создание workflow-процесса запросов на отпуск
description: Создание workflow-процесса запросов отпуска и отсутствия для постоянного управления запросами отпуска в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353696"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="16a36-103">Создание workflow-процесса запросов на отпуск</span><span class="sxs-lookup"><span data-stu-id="16a36-103">Create a leave request workflow</span></span>

<span data-ttu-id="16a36-104">Workflow-процесс можно создать в Dynamics 365 Human Resources для постоянного управления запросами отпуска и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="16a36-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="16a36-105">Workflow-процесс **Отпуск и отсутствие** позволяет:</span><span class="sxs-lookup"><span data-stu-id="16a36-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="16a36-106">Определение задач</span><span class="sxs-lookup"><span data-stu-id="16a36-106">Define tasks</span></span>
- <span data-ttu-id="16a36-107">Определите, кто должен выполнять задачи</span><span class="sxs-lookup"><span data-stu-id="16a36-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="16a36-108">Укажите, кто может утверждать или отклонять запросы</span><span class="sxs-lookup"><span data-stu-id="16a36-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="16a36-109">Создание workflow-процесса запросов отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="16a36-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="16a36-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="16a36-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="16a36-111">В **Настройка** выберите **Workflow-процессы управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="16a36-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="16a36-112">Выберите **Создать**, а затем выберите **Запрос отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="16a36-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="16a36-113">Когда появляется окно сообщения **Открыть этот файл?**, выберите **Открыть** и войдите в систему с учетными данными компании.</span><span class="sxs-lookup"><span data-stu-id="16a36-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="16a36-114">С помощью редактора workflow-процессов создайте workflow-процесс для своих запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="16a36-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="16a36-115">Дополнительные сведения о работе с workflow-процессами см. в разделе [Обзор создания workflow-процессов](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="16a36-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="16a36-116">Элементы данных workflow-процесса запросов отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="16a36-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="16a36-117">Следующие элементы данных можно использовать для создания условного или автоматического утверждения в workflow-процессах для запросов отпусков и отсутствия:</span><span class="sxs-lookup"><span data-stu-id="16a36-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="16a36-118">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="16a36-118">**Comment**</span></span>
- <span data-ttu-id="16a36-119">**Организация**</span><span class="sxs-lookup"><span data-stu-id="16a36-119">**Company**</span></span>
- <span data-ttu-id="16a36-120">**Создан**</span><span class="sxs-lookup"><span data-stu-id="16a36-120">**Created by**</span></span>
- <span data-ttu-id="16a36-121">**Дата и время создания**</span><span class="sxs-lookup"><span data-stu-id="16a36-121">**Created date and time**</span></span>
- <span data-ttu-id="16a36-122">**Конечная дата**</span><span class="sxs-lookup"><span data-stu-id="16a36-122">**End date**</span></span>
- <span data-ttu-id="16a36-123">**Тип отпуска**</span><span class="sxs-lookup"><span data-stu-id="16a36-123">**Leave type**</span></span>
- <span data-ttu-id="16a36-124">**Кто изменил**</span><span class="sxs-lookup"><span data-stu-id="16a36-124">**Modified by**</span></span>
- <span data-ttu-id="16a36-125">**Дата и время изменения**</span><span class="sxs-lookup"><span data-stu-id="16a36-125">**Modified date and time**</span></span>
- <span data-ttu-id="16a36-126">**Код основания**</span><span class="sxs-lookup"><span data-stu-id="16a36-126">**Reason code**</span></span>
- <span data-ttu-id="16a36-127">**Код запроса**</span><span class="sxs-lookup"><span data-stu-id="16a36-127">**Request ID**</span></span>
- <span data-ttu-id="16a36-128">**Начальная дата**</span><span class="sxs-lookup"><span data-stu-id="16a36-128">**Start date**</span></span>
- <span data-ttu-id="16a36-129">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="16a36-129">**Status**</span></span> 
- <span data-ttu-id="16a36-130">**Дата отправки**</span><span class="sxs-lookup"><span data-stu-id="16a36-130">**Submission date**</span></span>
- <span data-ttu-id="16a36-131">**Кем отправлено:**</span><span class="sxs-lookup"><span data-stu-id="16a36-131">**Submitted by**</span></span>
- <span data-ttu-id="16a36-132">**Отправлено отделом по управлению персоналом**</span><span class="sxs-lookup"><span data-stu-id="16a36-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="16a36-133">**Отправлено менеджером**</span><span class="sxs-lookup"><span data-stu-id="16a36-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="16a36-134">**Отправлено от имени**</span><span class="sxs-lookup"><span data-stu-id="16a36-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="16a36-135">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="16a36-135">**Worker**</span></span>
- <span data-ttu-id="16a36-136">**Тип работника**</span><span class="sxs-lookup"><span data-stu-id="16a36-136">**Worker type**</span></span>

<span data-ttu-id="16a36-137">В этих примерах показано, как можно создать различные типы условий workflow-процесса, используя эти элементы данных:</span><span class="sxs-lookup"><span data-stu-id="16a36-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="16a36-138">**Код основания** используется в условном выражении для направления запросов на отпуск по болезни с кодом основания **Хирургическая операций** для утверждения отделом управления персоналом, в то время как все остальные коды основания перенаправляются менеджеру.</span><span class="sxs-lookup"><span data-stu-id="16a36-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="16a36-139">Дополнительные сведения об условных выражениях см в разделе [Настройка условных решений в workflow-процессе](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="16a36-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="16a36-140">Используйте **Отправлено отделом по управлению персоналом** и **Отправлено менеджером** в автоматическом действии для автоматического утверждения запросов на отпуск, которые эти роли отправляют от имени сотрудников.</span><span class="sxs-lookup"><span data-stu-id="16a36-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="16a36-141">Дополнительные сведения об автоматических действиях см. в разделе [Настройка процессов утверждения в workflow-процессе](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="16a36-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="16a36-142">**Тип отпуска** используется в условных выражениях или автоматических действиях для управления перенаправление запросов с определенными типами отпусков.</span><span class="sxs-lookup"><span data-stu-id="16a36-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="16a36-143">См. также</span><span class="sxs-lookup"><span data-stu-id="16a36-143">See also</span></span>

- [<span data-ttu-id="16a36-144">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="16a36-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
