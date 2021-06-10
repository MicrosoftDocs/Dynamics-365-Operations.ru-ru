---
title: Создание workflow-процесса запросов на отпуск
description: Создание workflow-процесса запросов отпуска и отсутствия для постоянного управления запросами отпуска в Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056548"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="f01f4-103">Создание workflow-процесса запросов на отпуск</span><span class="sxs-lookup"><span data-stu-id="f01f4-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f01f4-104">Workflow-процесс можно создать в Dynamics 365 Human Resources для постоянного управления запросами отпуска и отсутствия.</span><span class="sxs-lookup"><span data-stu-id="f01f4-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="f01f4-105">Workflow-процесс **Отпуск и отсутствие** позволяет:</span><span class="sxs-lookup"><span data-stu-id="f01f4-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="f01f4-106">Определение задач</span><span class="sxs-lookup"><span data-stu-id="f01f4-106">Define tasks</span></span>
- <span data-ttu-id="f01f4-107">Определите, кто должен выполнять задачи</span><span class="sxs-lookup"><span data-stu-id="f01f4-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="f01f4-108">Укажите, кто может утверждать или отклонять запросы</span><span class="sxs-lookup"><span data-stu-id="f01f4-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="f01f4-109">Создание workflow-процесса запросов отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="f01f4-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="f01f4-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="f01f4-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f01f4-111">В **Настройка** выберите **Workflow-процессы управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="f01f4-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="f01f4-112">Выберите **Создать**, а затем выберите **Запрос отпуска и отсутствия**.</span><span class="sxs-lookup"><span data-stu-id="f01f4-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="f01f4-113">Когда появляется окно сообщения **Открыть этот файл?**, выберите **Открыть** и войдите в систему с учетными данными компании.</span><span class="sxs-lookup"><span data-stu-id="f01f4-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="f01f4-114">С помощью редактора workflow-процессов создайте workflow-процесс для своих запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="f01f4-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="f01f4-115">Дополнительные сведения о работе с workflow-процессами см. в разделе [Обзор создания workflow-процессов](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="f01f4-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="f01f4-116">Элементы данных workflow-процесса запросов отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="f01f4-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="f01f4-117">Следующие элементы данных можно использовать для создания условного или автоматического утверждения в workflow-процессах для запросов отпусков и отсутствия:</span><span class="sxs-lookup"><span data-stu-id="f01f4-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="f01f4-118">**Сумма, руб.**</span><span class="sxs-lookup"><span data-stu-id="f01f4-118">**Amount**</span></span>
- <span data-ttu-id="f01f4-119">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="f01f4-119">**Comment**</span></span>
- <span data-ttu-id="f01f4-120">**Организация**</span><span class="sxs-lookup"><span data-stu-id="f01f4-120">**Company**</span></span>
- <span data-ttu-id="f01f4-121">**Создан**</span><span class="sxs-lookup"><span data-stu-id="f01f4-121">**Created by**</span></span>
- <span data-ttu-id="f01f4-122">**Дата и время создания**</span><span class="sxs-lookup"><span data-stu-id="f01f4-122">**Created date and time**</span></span>
- <span data-ttu-id="f01f4-123">**Конечная дата**</span><span class="sxs-lookup"><span data-stu-id="f01f4-123">**End date**</span></span>
- <span data-ttu-id="f01f4-124">**Тип отпуска**</span><span class="sxs-lookup"><span data-stu-id="f01f4-124">**Leave type**</span></span>
- <span data-ttu-id="f01f4-125">**Кто изменил**</span><span class="sxs-lookup"><span data-stu-id="f01f4-125">**Modified by**</span></span>
- <span data-ttu-id="f01f4-126">**Дата и время изменения**</span><span class="sxs-lookup"><span data-stu-id="f01f4-126">**Modified date and time**</span></span>
- <span data-ttu-id="f01f4-127">**Код основания**</span><span class="sxs-lookup"><span data-stu-id="f01f4-127">**Reason code**</span></span>
- <span data-ttu-id="f01f4-128">**Код запроса**</span><span class="sxs-lookup"><span data-stu-id="f01f4-128">**Request ID**</span></span>
- <span data-ttu-id="f01f4-129">**Начальная дата**</span><span class="sxs-lookup"><span data-stu-id="f01f4-129">**Start date**</span></span>
- <span data-ttu-id="f01f4-130">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f01f4-130">**Status**</span></span> 
- <span data-ttu-id="f01f4-131">**Дата отправки**</span><span class="sxs-lookup"><span data-stu-id="f01f4-131">**Submission date**</span></span>
- <span data-ttu-id="f01f4-132">**Кем отправлено:**</span><span class="sxs-lookup"><span data-stu-id="f01f4-132">**Submitted by**</span></span>
- <span data-ttu-id="f01f4-133">**Отправлено отделом по управлению персоналом**</span><span class="sxs-lookup"><span data-stu-id="f01f4-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="f01f4-134">**Отправлено менеджером**</span><span class="sxs-lookup"><span data-stu-id="f01f4-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="f01f4-135">**Отправлено от имени**</span><span class="sxs-lookup"><span data-stu-id="f01f4-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="f01f4-136">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="f01f4-136">**Worker**</span></span>
- <span data-ttu-id="f01f4-137">**Тип работника**</span><span class="sxs-lookup"><span data-stu-id="f01f4-137">**Worker type**</span></span>

<span data-ttu-id="f01f4-138">В этих примерах показано, как можно создать различные типы условий workflow-процесса, используя эти элементы данных:</span><span class="sxs-lookup"><span data-stu-id="f01f4-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="f01f4-139">**Код основания** используется в условном выражении для направления запросов на отпуск по болезни с кодом основания **Хирургическая операций** для утверждения отделом управления персоналом, в то время как все остальные коды основания перенаправляются менеджеру.</span><span class="sxs-lookup"><span data-stu-id="f01f4-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="f01f4-140">Дополнительные сведения об условных выражениях см в разделе [Настройка условных решений в workflow-процессе](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f01f4-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span></span> 

- <span data-ttu-id="f01f4-141">Используйте **Отправлено отделом по управлению персоналом** и **Отправлено менеджером** в автоматическом действии для автоматического утверждения запросов на отпуск, которые эти роли отправляют от имени сотрудников.</span><span class="sxs-lookup"><span data-stu-id="f01f4-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="f01f4-142">Дополнительные сведения об автоматических действиях см. в разделе [Настройка процессов утверждения в workflow-процессе](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f01f4-142">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="f01f4-143">**Тип отпуска** используется в условных выражениях или автоматических действиях для управления перенаправление запросов с определенными типами отпусков.</span><span class="sxs-lookup"><span data-stu-id="f01f4-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="f01f4-144">См. также</span><span class="sxs-lookup"><span data-stu-id="f01f4-144">See also</span></span>

- [<span data-ttu-id="f01f4-145">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="f01f4-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]