---
title: Workflow-процессы модуля "Закупки и источники"
description: В некоторых организациях требуется, чтобы заявки на покупку и заказы на покупку утверждались пользователем, отличным от сотрудника, который ввел проводку. Чтобы настроить процесс утверждения, можно создать workflow-процесс.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909239"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="5181b-104">Workflow-процессы модуля "Закупки и источники"</span><span class="sxs-lookup"><span data-stu-id="5181b-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5181b-105">В некоторых организациях требуется, чтобы заявки на покупку и заказы на покупку утверждались пользователем, отличным от сотрудника, который ввел проводку.</span><span class="sxs-lookup"><span data-stu-id="5181b-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="5181b-106">Чтобы настроить процесс утверждения, можно создать workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="5181b-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="5181b-107">Бизнес-правило представляет бизнес-процесс.</span><span class="sxs-lookup"><span data-stu-id="5181b-107">A workflow represents a business process.</span></span> <span data-ttu-id="5181b-108">Он определяет путь движения документа по системе и указывает, кто должен выполнить ту или иную задачу или утвердить тот или иной документ.</span><span class="sxs-lookup"><span data-stu-id="5181b-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="5181b-109">Имеется несколько преимуществ использования системы workflow-процессов в организации:</span><span class="sxs-lookup"><span data-stu-id="5181b-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="5181b-110">**Непротиворечивые процессы** — можно определить процесс утверждения для конкретных документов, таких как заявки на покупку и отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="5181b-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="5181b-111">Использование системы workflow-процессов позволяет обеспечить обработку и утверждение документов непротиворечивым и эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="5181b-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="5181b-112">**Видимость процессов** — можно отслеживать статус, историю и метрики производительности конкретного экземпляра workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="5181b-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="5181b-113">Это позволяет определить, должны ли быть внесены изменения в workflow-процесс для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="5181b-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="5181b-114">**Централизованный список работ** — пользователи могут просматривать централизованный список работ для просмотра задач workflow-процесса и утверждений, в которых они участвуют.</span><span class="sxs-lookup"><span data-stu-id="5181b-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="5181b-115">Это доступно на странице "Рабочие элементы".</span><span class="sxs-lookup"><span data-stu-id="5181b-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="5181b-116">Типы бизнес-правил, которые можно создавать</span><span class="sxs-lookup"><span data-stu-id="5181b-116">The types of workflows that you can create</span></span>

<span data-ttu-id="5181b-117">Доступны следующие типы бизнес-правила для Закупок и источников.</span><span class="sxs-lookup"><span data-stu-id="5181b-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="5181b-118">Вид</span><span class="sxs-lookup"><span data-stu-id="5181b-118">Type</span></span> | <span data-ttu-id="5181b-119">Тип, который будет использоваться</span><span class="sxs-lookup"><span data-stu-id="5181b-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="5181b-120">Обзор заявок на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-120">Purchase requisition review</span></span> | <span data-ttu-id="5181b-121">Создание workflow-процессов проверки и утверждения для заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="5181b-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="5181b-122">Рассмотрение строки заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-122">Purchase requisition line review</span></span> | <span data-ttu-id="5181b-123">Создание workflow-процессов проверки и утверждения для строк заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="5181b-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="5181b-124">Workflow-процесс заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-124">Purchase order workflow</span></span> | <span data-ttu-id="5181b-125">Проверка и утверждение бизнес-правил для заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="5181b-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="5181b-126">Workflow-процесс строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-126">Purchase order line workflow</span></span> | <span data-ttu-id="5181b-127">Создание бизнес-правила для проверки и утверждения для строк заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="5181b-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="5181b-128">Workflow-процесс приложения добавления поставщика</span><span class="sxs-lookup"><span data-stu-id="5181b-128">Vendor add application workflow</span></span> | <span data-ttu-id="5181b-129">Создание workflow-процессов проверки и утверждения для добавления новых поставщиков через запросы поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5181b-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="5181b-130">При добавлении нового рабочего процесса можно также увидеть следующие устаревшие рабочие процессы, перечисленные в диалоговом окне **Создание рабочего процесса**.</span><span class="sxs-lookup"><span data-stu-id="5181b-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="5181b-131">Они связаны с функциональностью *подтверждения поступления*, которая была доступна в [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), но которая в данный момент устарела.</span><span class="sxs-lookup"><span data-stu-id="5181b-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="5181b-132">Эти рабочие процессы в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5181b-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="5181b-133">Workflow-процесс уведомления о сроке выполнения поставки</span><span class="sxs-lookup"><span data-stu-id="5181b-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="5181b-134">Workflow-процесс уведомления о полученной накладной</span><span class="sxs-lookup"><span data-stu-id="5181b-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="5181b-135">Не удалось выполнить workflow-процесс уведомления для поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="5181b-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="5181b-136">Workflow-процесс уведомления об отклонении неподтверждённого поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="5181b-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="5181b-137">Создание workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="5181b-137">Creating a workflow</span></span>

<span data-ttu-id="5181b-138">Чтобы создать workflow-процесс, перейдите к пункту "Закупки и источники" &gt; "Настройка" &gt; "Workflow-процессы модуля "Закупки и источники" и создайте новый workflow-процесс, выбрав тип создаваемого workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="5181b-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="5181b-139">В холсте workflow-процесса можно перетаскивать элементы workflow-процесса в конструктор и связывать элементы в поток.</span><span class="sxs-lookup"><span data-stu-id="5181b-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="5181b-140">Элементы workflow-процесса должны быть настроены.</span><span class="sxs-lookup"><span data-stu-id="5181b-140">The workflow elements should be configured.</span></span> <span data-ttu-id="5181b-141">Для утверждения и элементов workflow-процесса задачи можно настроить, какой участник должен выполнять действие.</span><span class="sxs-lookup"><span data-stu-id="5181b-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="5181b-142">Типы участников</span><span class="sxs-lookup"><span data-stu-id="5181b-142">Types of participants</span></span>

<span data-ttu-id="5181b-143">Можно назначить шаг утверждения следующим группам участников.</span><span class="sxs-lookup"><span data-stu-id="5181b-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="5181b-144">Группа пользователей</span><span class="sxs-lookup"><span data-stu-id="5181b-144">User group</span></span> | <span data-ttu-id="5181b-145">Описание</span><span class="sxs-lookup"><span data-stu-id="5181b-145">Description</span></span> |
|---|---|
| <span data-ttu-id="5181b-146">Участник</span><span class="sxs-lookup"><span data-stu-id="5181b-146">Participant</span></span> | <span data-ttu-id="5181b-147">Назначение шага утверждения членам группы или роли.</span><span class="sxs-lookup"><span data-stu-id="5181b-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="5181b-148">Иерархия</span><span class="sxs-lookup"><span data-stu-id="5181b-148">Hierarchy</span></span> | <span data-ttu-id="5181b-149">Назначение шага утверждения пользователям в определенной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="5181b-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="5181b-150">Пользователь workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="5181b-150">Workflow user</span></span> | <span data-ttu-id="5181b-151">Назначение шага утверждения пользователям данного workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="5181b-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="5181b-152">Очередь</span><span class="sxs-lookup"><span data-stu-id="5181b-152">Queue</span></span> | <span data-ttu-id="5181b-153">Назначение шага утверждения очереди задач.</span><span class="sxs-lookup"><span data-stu-id="5181b-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="5181b-154">Пользователь</span><span class="sxs-lookup"><span data-stu-id="5181b-154">User</span></span> | <span data-ttu-id="5181b-155">Назначение шага утверждения для конкретных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5181b-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5181b-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5181b-156">Additional resources</span></span>

- [<span data-ttu-id="5181b-157">Определение workflow-процессов бизнес-процессов для заявок на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="5181b-158">Бизнес-правило для заявок на покупку</span><span class="sxs-lookup"><span data-stu-id="5181b-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="5181b-159">Адаптация поставщиков</span><span class="sxs-lookup"><span data-stu-id="5181b-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]