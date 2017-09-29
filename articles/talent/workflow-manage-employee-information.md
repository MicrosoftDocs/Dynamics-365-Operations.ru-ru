---
title: "Использование workflow-процессов для управления сведениями о сотрудниках"
description: "В этом разделе объясняется, как можно использовать возможности этого workflow-процесса для модуля \"Управление персоналом\" для управления сведениями о сотрудниках. Например, можно связать workflow-процесс с должностью и настроить workflow-процесс утверждения, который запускается, когда сотрудник вносит изменение в свою запись."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 2dc4671e0b68dffe30fe73d8c95113481673a27a
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017


---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="7b348-104">Использование workflow-процессов для управления сведениями о сотрудниках</span><span class="sxs-lookup"><span data-stu-id="7b348-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="7b348-105">В этом разделе объясняется, как можно использовать возможности этого workflow-процесса для модуля "Управление персоналом" для управления сведениями о сотрудниках.</span><span class="sxs-lookup"><span data-stu-id="7b348-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="7b348-106">Например, можно связать workflow-процесс с должностью и настроить workflow-процесс утверждения, который запускается, когда сотрудник вносит изменение в свою запись.</span><span class="sxs-lookup"><span data-stu-id="7b348-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="7b348-107">Возможности workflow-процесс для модуля "Управление персоналом" предоставляет множество workflow-процессов для управления мероприятиями управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="7b348-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="7b348-108">Кроме того, доступны многочисленные параметры, чтобы вы могли изменять конкретные workflow-процессы и связывать их с иерархией отчетности.</span><span class="sxs-lookup"><span data-stu-id="7b348-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="7b348-109">Предусмотрены workflow-процессы, помогающие управлять изменениями в нескольких стандартных типах сведений о сотрудниках.</span><span class="sxs-lookup"><span data-stu-id="7b348-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="7b348-110">Можно связать workflow-процесс с должностью.</span><span class="sxs-lookup"><span data-stu-id="7b348-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="7b348-111">Затем, если сотрудники вносят изменения в свои записи сотрудника, запускается workflow-процесс, который требует утверждения перед сохранением новой информации.</span><span class="sxs-lookup"><span data-stu-id="7b348-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="7b348-112">Заранее определены workflow-процессы для следующих типов сведений, чтобы помочь эффективно управлять изменениями и поддерживать точность данных сотрудников:</span><span class="sxs-lookup"><span data-stu-id="7b348-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="7b348-113">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="7b348-113">Identification numbers</span></span>
-   <span data-ttu-id="7b348-114">Курсы</span><span class="sxs-lookup"><span data-stu-id="7b348-114">Courses</span></span>
-   <span data-ttu-id="7b348-115">Образование</span><span class="sxs-lookup"><span data-stu-id="7b348-115">Education</span></span>
-   <span data-ttu-id="7b348-116">Изображение</span><span class="sxs-lookup"><span data-stu-id="7b348-116">Image</span></span>
-   <span data-ttu-id="7b348-117">Одолженные номенклатуры</span><span class="sxs-lookup"><span data-stu-id="7b348-117">Loaned items</span></span>
-   <span data-ttu-id="7b348-118">Опыт работы</span><span class="sxs-lookup"><span data-stu-id="7b348-118">Professional experience</span></span>
-   <span data-ttu-id="7b348-119">Проектный опыт</span><span class="sxs-lookup"><span data-stu-id="7b348-119">Project experience</span></span>
-   <span data-ttu-id="7b348-120">Навыки</span><span class="sxs-lookup"><span data-stu-id="7b348-120">Skills</span></span>
-   <span data-ttu-id="7b348-121">Выборные должности</span><span class="sxs-lookup"><span data-stu-id="7b348-121">Positions of trust</span></span>
-   <span data-ttu-id="7b348-122">Действия по управлению персоналом</span><span class="sxs-lookup"><span data-stu-id="7b348-122">Human resources actions</span></span>
-   <span data-ttu-id="7b348-123">Регистрация на курсах</span><span class="sxs-lookup"><span data-stu-id="7b348-123">Course registration</span></span>

<span data-ttu-id="7b348-124">При приеме на работу, переводе или увольнении сотрудника workflow-процесс может включать процесс рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="7b348-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="7b348-125">Таким образом можно исправить документ или определить сроки действия как часть workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="7b348-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="7b348-126">По завершении процесса рассмотрения документ или действие завершается, и workflow-процесс переходит на этап окончательного утверждения.</span><span class="sxs-lookup"><span data-stu-id="7b348-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="7b348-127">Связывание workflow-процесса с иерархией должностей</span><span class="sxs-lookup"><span data-stu-id="7b348-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="7b348-128">Workflow-процесс может быть связан с любой иерархии, которую вы настроили.</span><span class="sxs-lookup"><span data-stu-id="7b348-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="7b348-129">Например, если должность связана с иерархией матричной отчетности, можно настроить workflow-процесс, который направляет затраты для определенного проекта на руководителя проекта, а не на сотрудника, связанного с этой должностью.</span><span class="sxs-lookup"><span data-stu-id="7b348-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="7b348-130">Чтобы создать новый workflow-процесс или изменить существующий workflow-процесс, на странице **Workflow-процесс управления персоналом** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7b348-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="7b348-131">Выберите workflow-процесс в списке, чтобы запустить конструктор workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="7b348-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="7b348-132">Конструктор можно использовать для создания нового workflow-процесса или изменения этапов существующего workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="7b348-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="7b348-133">При изменении существующего workflow-процесса изменения сохраняются в виде новой версии.</span><span class="sxs-lookup"><span data-stu-id="7b348-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="7b348-134">Таким образом вы всегда можете вернуться к предыдущей версии, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="7b348-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="7b348-135">Настройка workflow-процесса управления персоналом</span><span class="sxs-lookup"><span data-stu-id="7b348-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="7b348-136">Чтобы настроить базовый workflow-процесс, который запускается, когда сотрудники запрашивают изменение своего личного идентификационного кода, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b348-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="7b348-137">На странице **Workflow-процессы управления персоналом** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7b348-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="7b348-138">В списке доступных workflow-процессов выберите **Идентификационные номера**.</span><span class="sxs-lookup"><span data-stu-id="7b348-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="7b348-139">Щелкните **Выполнить** для запуска конструктора workflow-процессов, затем введите имя пользователя и пароль, когда появится запрос.</span><span class="sxs-lookup"><span data-stu-id="7b348-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="7b348-140">Перетащите элемент **Утвердить идентификационный номер** из списка элементов workflow-процесса на холст конструктора.</span><span class="sxs-lookup"><span data-stu-id="7b348-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="7b348-141">Подключите элемент утверждения к **Начало** и **Конец**.</span><span class="sxs-lookup"><span data-stu-id="7b348-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="7b348-142">Дважды щелкните **Элемент утверждения**, затем щелкните правой кнопкой мыши и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7b348-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="7b348-143">Выполните следующие действия, чтобы добавить инструкции для рабочего элемента:</span><span class="sxs-lookup"><span data-stu-id="7b348-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="7b348-144">Выберите **Назначение**, затем выберите **Иерархия** в типе назначения.</span><span class="sxs-lookup"><span data-stu-id="7b348-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="7b348-145">В пункте **Иерархия** выберите **Настраиваемая иерархия**.</span><span class="sxs-lookup"><span data-stu-id="7b348-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="7b348-146">Добавьте условие остановки и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7b348-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="7b348-147">Выполните любые дополнительные инструкции (никаких дополнительных предупреждений быть не должно).</span><span class="sxs-lookup"><span data-stu-id="7b348-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="7b348-148">Нажмите кнопку **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="7b348-148">Click **Save and close**.</span></span> <span data-ttu-id="7b348-149">Активируйте новый workflow-процесс, когда будет открыто диалоговое окно, и выберите **Сделать активным**.</span><span class="sxs-lookup"><span data-stu-id="7b348-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="7b348-150">Перейдите в раздел **Управление персоналом** &gt; **Должности** &gt; **Типы иерархий должностей**.</span><span class="sxs-lookup"><span data-stu-id="7b348-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="7b348-151">Выберите **Матрица**.</span><span class="sxs-lookup"><span data-stu-id="7b348-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="7b348-152">Добавьте workflow-процесс **Идентификационный код работника** в список.</span><span class="sxs-lookup"><span data-stu-id="7b348-152">Add the **Worker identification number** workflow to the list.</span></span>





