---
title: Создание рабочего процесса запросов покупки и продажи отпуска
description: Создание рабочего процесса запросов покупки и продажи отпуска для постоянного управления запросами покупки и продажи отпуска в Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4732b5dafc8074c5c59f10f02bbee7e22f51960a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5116052"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="a362a-103">Создание рабочего процесса запросов покупки и продажи отпуска</span><span class="sxs-lookup"><span data-stu-id="a362a-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="a362a-104">Рабочий процесс можно создать в Dynamics 365 Human Resources для постоянного управления запросами покупки и продажи отпуска.</span><span class="sxs-lookup"><span data-stu-id="a362a-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="a362a-105">Рабочий процесс **Покупка и продажа отпуска** позволяет:</span><span class="sxs-lookup"><span data-stu-id="a362a-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="a362a-106">Определение задач</span><span class="sxs-lookup"><span data-stu-id="a362a-106">Define tasks</span></span>
- <span data-ttu-id="a362a-107">Определите, кто должен выполнять задачи</span><span class="sxs-lookup"><span data-stu-id="a362a-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="a362a-108">Укажите, кто может утверждать или отклонять запросы</span><span class="sxs-lookup"><span data-stu-id="a362a-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="a362a-109">Создание рабочего процесса запросов покупки и продажи отпуска</span><span class="sxs-lookup"><span data-stu-id="a362a-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="a362a-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="a362a-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="a362a-111">В **Настройка** выберите **Workflow-процессы управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="a362a-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="a362a-112">Выберите **Создать**, затем выберите **Запрос покупки и продажи отпуска**.</span><span class="sxs-lookup"><span data-stu-id="a362a-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="a362a-113">Когда появляется окно сообщения **Открыть этот файл?**, выберите **Открыть** и войдите в систему с учетными данными компании.</span><span class="sxs-lookup"><span data-stu-id="a362a-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="a362a-114">С помощью редактора workflow-процессов создайте workflow-процесс для своих запросов на отпуск.</span><span class="sxs-lookup"><span data-stu-id="a362a-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="a362a-115">Дополнительные сведения о работе с workflow-процессами см. в разделе [Обзор создания workflow-процессов](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="a362a-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="a362a-116">Элементы данных workflow-процесса запросов отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="a362a-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="a362a-117">Следующие элементы данных можно использовать для создания условного или автоматического утверждения в рабочих процессах для запросов покупки и продажи отпусков:</span><span class="sxs-lookup"><span data-stu-id="a362a-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="a362a-118">**Сумма, руб.**</span><span class="sxs-lookup"><span data-stu-id="a362a-118">**Amount**</span></span>
- <span data-ttu-id="a362a-119">**Политика покупки и продажи отпусков**</span><span class="sxs-lookup"><span data-stu-id="a362a-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="a362a-120">**Организация**</span><span class="sxs-lookup"><span data-stu-id="a362a-120">**Company**</span></span>
- <span data-ttu-id="a362a-121">**Создан**</span><span class="sxs-lookup"><span data-stu-id="a362a-121">**Created by**</span></span>
- <span data-ttu-id="a362a-122">**Дата и время создания**</span><span class="sxs-lookup"><span data-stu-id="a362a-122">**Created date and time**</span></span>
- <span data-ttu-id="a362a-123">**Конечная дата**</span><span class="sxs-lookup"><span data-stu-id="a362a-123">**End date**</span></span>
- <span data-ttu-id="a362a-124">**Тип отпуска**</span><span class="sxs-lookup"><span data-stu-id="a362a-124">**Leave type**</span></span>
- <span data-ttu-id="a362a-125">**Изменено**</span><span class="sxs-lookup"><span data-stu-id="a362a-125">**Modified by**</span></span>
- <span data-ttu-id="a362a-126">**Дата и время изменения**</span><span class="sxs-lookup"><span data-stu-id="a362a-126">**Modified date and time**</span></span>
- <span data-ttu-id="a362a-127">**Код запроса**</span><span class="sxs-lookup"><span data-stu-id="a362a-127">**Request ID**</span></span>
- <span data-ttu-id="a362a-128">**Начальная дата**</span><span class="sxs-lookup"><span data-stu-id="a362a-128">**Start date**</span></span>
- <span data-ttu-id="a362a-129">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a362a-129">**Status**</span></span> 
- <span data-ttu-id="a362a-130">**Дата отправки**</span><span class="sxs-lookup"><span data-stu-id="a362a-130">**Submission date**</span></span>
- <span data-ttu-id="a362a-131">**Кем отправлено:**</span><span class="sxs-lookup"><span data-stu-id="a362a-131">**Submitted by**</span></span>
- <span data-ttu-id="a362a-132">**Отправлено отделом по управлению персоналом**</span><span class="sxs-lookup"><span data-stu-id="a362a-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="a362a-133">**Отправлено менеджером**</span><span class="sxs-lookup"><span data-stu-id="a362a-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="a362a-134">**Отправлено от имени**</span><span class="sxs-lookup"><span data-stu-id="a362a-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="a362a-135">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="a362a-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="a362a-136">Примеры рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="a362a-136">Workflow examples</span></span>

<span data-ttu-id="a362a-137">В этих примерах показано, как можно создать различные типы условий workflow-процесса, используя эти элементы данных:</span><span class="sxs-lookup"><span data-stu-id="a362a-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="a362a-138">Используйте **Отправлено отделом по управлению персоналом** и **Отправлено менеджером** в автоматическом действии для автоматического утверждения запросов покупки и продажи отпуска, которые эти роли отправляют от имени сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a362a-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="a362a-139">Дополнительные сведения об автоматических действиях см. в разделе [Настройка процессов утверждения в workflow-процессе](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="a362a-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="a362a-140">**Тип отпуска** используется в условных выражениях или автоматических действиях для управления перенаправление запросов с определенными типами отпусков.</span><span class="sxs-lookup"><span data-stu-id="a362a-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="a362a-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a362a-141">See also</span></span>

[<span data-ttu-id="a362a-142">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="a362a-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="a362a-143">Управление политиками покупки и продажи отпусков</span><span class="sxs-lookup"><span data-stu-id="a362a-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

