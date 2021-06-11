---
title: Ввод навыков
description: Работники и менеджеры могут вводить навыки в Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076612"
---
# <a name="enter-skills"></a><span data-ttu-id="b02c5-103">Ввод навыков</span><span class="sxs-lookup"><span data-stu-id="b02c5-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b02c5-104">Можно ввести целевые навыки или фактические навыки для сотрудников, кандидатов и контактных лиц в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b02c5-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b02c5-105">Целевые навык — навык, который лицо хочет получить.</span><span class="sxs-lookup"><span data-stu-id="b02c5-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b02c5-106">Фактический навык — навык, которым лицо обладает.</span><span class="sxs-lookup"><span data-stu-id="b02c5-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="b02c5-107">Создание рабочего процесса для автоматического утверждения навыков</span><span class="sxs-lookup"><span data-stu-id="b02c5-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="b02c5-108">Чтобы ввести навыки без необходимости утверждения, необходимо создать рабочий процесс для автоматического утверждения навыков.</span><span class="sxs-lookup"><span data-stu-id="b02c5-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="b02c5-109">Навыки, введенные сотрудниками, всегда требуют утверждения руководителем.</span><span class="sxs-lookup"><span data-stu-id="b02c5-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="b02c5-110">Этот рабочий процесс только автоматически утверждает навыки, введенные менеджерами от имени своих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b02c5-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="b02c5-111">В рабочей области **Управление персоналом** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b02c5-112">В **Настройка** выберите **Рабочие процессы управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="b02c5-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-113">Select **New**.</span></span>

4. <span data-ttu-id="b02c5-114">В области **Создать рабочий процесс** выберите **Навыки работников**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="b02c5-115">[![Выберите рабочий процесс навыков работника](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="b02c5-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="b02c5-116">В диалоговом окне **Открыть этот файл?** выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="b02c5-117">По запросу введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="b02c5-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="b02c5-118">В редакторе рабочих процессов выберите элемент рабочего процесса **Утверждение навыков** и перетащите его на холст.</span><span class="sxs-lookup"><span data-stu-id="b02c5-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="b02c5-119">[![Выберите элемент рабочего процесса утверждения навыков](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="b02c5-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="b02c5-120">Свяжите элемент **Начало** с элементом **Утверждение навыков 1**, затем свяжите элемент **Утвержденные навыков 1** с элементом **Конец**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="b02c5-121">Возможно, потребуется прокрутить список, чтобы увидеть элемент **Конец**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="b02c5-122">Его можно перетащить ближе к другим элементам.</span><span class="sxs-lookup"><span data-stu-id="b02c5-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="b02c5-123">[![Подключение элементов рабочего процесса](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="b02c5-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="b02c5-124">Дважды щелкните элемент рабочего процесса **Утверждение навыков 1**, затем щелкните правой кнопкой мыши элемент **Шаг 1**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="b02c5-125">Щелкните правой кнопкой мыши элемент **Шаг 1**, затем выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="b02c5-126">В окне **Свойства** выберите **Условие** в левой панели навигации.</span><span class="sxs-lookup"><span data-stu-id="b02c5-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="b02c5-127">Выберите **Выполнять этот шаг только при соблюдении следующего условия**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="b02c5-128">Выберите **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-128">Select **Add condition**.</span></span> <span data-ttu-id="b02c5-129">После **Где** выберите **Навыки самообслуживания сотрудников**, затем выберите **Навыки самообслуживания сотрудников. Лицо**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="b02c5-130">После **является** выберите **поле**, а затем выберите **Отношение пользователя к сотруднику.Лицо**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="b02c5-131">[![Укажите условие](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="b02c5-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="b02c5-132">Выберите **Назначение** на левой панели навигации.</span><span class="sxs-lookup"><span data-stu-id="b02c5-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="b02c5-133">На вкладке **Тип назначения** выберите **Иерархия**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="b02c5-134">На вкладке **Выбор иерархии** в поле **Тип иерархии:** выберите **Управленческая иерархия**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="b02c5-135">[![Укажите управленческую иерархию](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="b02c5-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="b02c5-136">Выберите **Закрыть**, выберите **Рабочий процесс** в модуле навигации холста, затем выберите **Сохранить и закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="b02c5-137">Дополнительные сведения о создании рабочих процессов см. в разделе [Обзор системы рабочих процессов](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b02c5-137">For more information about creating workflows, see [Workflow system overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="b02c5-138">Ввод навыков для сотрудника</span><span class="sxs-lookup"><span data-stu-id="b02c5-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="b02c5-139">Выберите работника.</span><span class="sxs-lookup"><span data-stu-id="b02c5-139">Select a worker.</span></span>

2. <span data-ttu-id="b02c5-140">На панели операций на странице **Работник** выберите **Лицо**, а затем выберите **Навыки**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="b02c5-141">На странице **Навыки** заполните следующие поля для каждого навыка:</span><span class="sxs-lookup"><span data-stu-id="b02c5-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="b02c5-142">**Навык**: выберите навык.</span><span class="sxs-lookup"><span data-stu-id="b02c5-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="b02c5-143">**Тип уровня**: выберите **Фактический** для навыка, который сотрудник уже имеет, или выберите **Цель** для навыка, к которому данный сотрудник стремится.</span><span class="sxs-lookup"><span data-stu-id="b02c5-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="b02c5-144">**Уровень**: выберите уровень навыка работника.</span><span class="sxs-lookup"><span data-stu-id="b02c5-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="b02c5-145">**Дата уровня**: выберите дату в инструменте календаря.</span><span class="sxs-lookup"><span data-stu-id="b02c5-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="b02c5-146">**Экзаменатор**: если необходимо, выберите экзаменатора из списка.</span><span class="sxs-lookup"><span data-stu-id="b02c5-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="b02c5-147">Можно отфильтровать поиск.</span><span class="sxs-lookup"><span data-stu-id="b02c5-147">You can filter your search.</span></span>
   - <span data-ttu-id="b02c5-148">**Опыт работы**: введите опыт работы в годах.</span><span class="sxs-lookup"><span data-stu-id="b02c5-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="b02c5-149">**Проверено**: если навык проверен, установите флажок.</span><span class="sxs-lookup"><span data-stu-id="b02c5-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="b02c5-150">**Кем проверено**: введите имя проверяющего.</span><span class="sxs-lookup"><span data-stu-id="b02c5-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="b02c5-151">По завершении ввода навыков выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b02c5-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b02c5-152">См. также</span><span class="sxs-lookup"><span data-stu-id="b02c5-152">See also</span></span>

[<span data-ttu-id="b02c5-153">Настройка навыков</span><span class="sxs-lookup"><span data-stu-id="b02c5-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="b02c5-154">Сопоставление навыков</span><span class="sxs-lookup"><span data-stu-id="b02c5-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]