---
title: Отмена задания сводного планирования
description: В этой теме объясняется, как отменить активное задание планирования, в котором используются встроенные функции планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947488"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="a2045-103">Отмена задания сводного планирования</span><span class="sxs-lookup"><span data-stu-id="a2045-103">Cancel a master planning job</span></span>

<span data-ttu-id="a2045-104">В Microsoft Dynamics 365 Supply Chain Management есть несколько вариантов отмены задания сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="a2045-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="a2045-105">Например, можно отменить задание сводного планирования, если оно было запущено по ошибке или работает дольше, чем ожидалось, и вы хотите закончить его.</span><span class="sxs-lookup"><span data-stu-id="a2045-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="a2045-106">Лучший способ отменить задание планирования — это страница **Незавершенные процессы планирования**.</span><span class="sxs-lookup"><span data-stu-id="a2045-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="a2045-107">Альтернативные варианты на страницах **Пакетные задания** и **Расширенные пакетные задания** должны использоваться только в том случае, если отмена задания сводного планирования на странице **Незавершенные процессы планирования** не была завершена в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="a2045-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="a2045-108">Предпочтительный вариант отмены</span><span class="sxs-lookup"><span data-stu-id="a2045-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="a2045-109">Отмена задания сводного планирования на странице **Незавершенные процессы планирования**</span><span class="sxs-lookup"><span data-stu-id="a2045-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="a2045-110">Перейдите в раздел **Сводное планирование > Запросы и отчеты > Сводное планирование > Незавершенные процессы планирования**.</span><span class="sxs-lookup"><span data-stu-id="a2045-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="a2045-111">Выберите строку процесса планирования, который следует отменить.</span><span class="sxs-lookup"><span data-stu-id="a2045-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="a2045-112">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="a2045-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="a2045-113">дополнительные параметры отмены</span><span class="sxs-lookup"><span data-stu-id="a2045-113">Additional cancel options</span></span>
<span data-ttu-id="a2045-114">Они должны использоваться, только если отмена задания сводного планирования на странице **Незавершенные процессы планирования** не завершилась в течение нескольких минут.</span><span class="sxs-lookup"><span data-stu-id="a2045-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="a2045-115">Удаление задания сводного планирования на странице **Пакетных заданий**</span><span class="sxs-lookup"><span data-stu-id="a2045-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="a2045-116">Перейдите в раздел **Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="a2045-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="a2045-117">Выберите строку задания планирования, которое следует удалить.</span><span class="sxs-lookup"><span data-stu-id="a2045-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="a2045-118">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a2045-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="a2045-119">Отмена задачи задания сводного планирования на странице **Расширенные пакетные задания**</span><span class="sxs-lookup"><span data-stu-id="a2045-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="a2045-120">Перейдите в раздел **Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="a2045-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="a2045-121">Если идентификатор задания не отображается в списке, щелкните **Переключить форму в расширенное представление**, в противном случае приступите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="a2045-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="a2045-122">Откройте пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="a2045-122">Open the batch job.</span></span> <span data-ttu-id="a2045-123">Нажмите **Идентификатор задания** для пакетного задания с задачами, которые вы хотите закончить.</span><span class="sxs-lookup"><span data-stu-id="a2045-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="a2045-124">В **Пакетные задания** выберите задачи для завершения.</span><span class="sxs-lookup"><span data-stu-id="a2045-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="a2045-125">На экспресс-вкладке **Пакетные задачи** нажмите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="a2045-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
