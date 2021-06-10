---
title: Настройка навыков
description: Можно отслеживать навыки работника в Dynamics 365 Human Resources. Также можно указывать навыки, необходимые для определенной должности.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076567"
---
# <a name="configure-skills"></a><span data-ttu-id="2ff27-104">Настройка навыков</span><span class="sxs-lookup"><span data-stu-id="2ff27-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2ff27-105">Можно отслеживать навыки работника в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2ff27-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2ff27-106">Также можно указывать навыки, необходимые для определенной должности.</span><span class="sxs-lookup"><span data-stu-id="2ff27-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="2ff27-107">Примеры навыков, которые можно отслеживать:</span><span class="sxs-lookup"><span data-stu-id="2ff27-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="2ff27-108">Способность контролировать - Умение контролировать работу других.</span><span class="sxs-lookup"><span data-stu-id="2ff27-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="2ff27-109">Лидерство -Умение возглавить сотрудников и деловые домены.</span><span class="sxs-lookup"><span data-stu-id="2ff27-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="2ff27-110">Планирование — умение предвидеть, формулировать визуальные утверждения и принимать решения на их основании.</span><span class="sxs-lookup"><span data-stu-id="2ff27-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="2ff27-111">HTML — Возможность создавать код HTML.</span><span class="sxs-lookup"><span data-stu-id="2ff27-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="2ff27-112">Если типы навыков и модели рейтинга еще не настроены, перед созданием навыков необходимо добавить некоторые.</span><span class="sxs-lookup"><span data-stu-id="2ff27-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="2ff27-113">Следующие сотрудники могут ввести навыки для сотрудника:</span><span class="sxs-lookup"><span data-stu-id="2ff27-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="2ff27-114">Работники могут вводить навыки для себя в системе самообслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="2ff27-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="2ff27-115">Эти навыки требуют утверждения руководителем.</span><span class="sxs-lookup"><span data-stu-id="2ff27-115">These skills require manager approval.</span></span>
- <span data-ttu-id="2ff27-116">Менеджеры могут вводить навыки для своих работников.</span><span class="sxs-lookup"><span data-stu-id="2ff27-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="2ff27-117">Можно создать рабочий процесс, который автоматически утверждает эти навыки.</span><span class="sxs-lookup"><span data-stu-id="2ff27-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="2ff27-118">Создание типа навыков</span><span class="sxs-lookup"><span data-stu-id="2ff27-118">Create a skill type</span></span>

<span data-ttu-id="2ff27-119">Типы навыков представляют собой категории, под которые попадают индивидуальные навыки, например, администрирование или продажи.</span><span class="sxs-lookup"><span data-stu-id="2ff27-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="2ff27-120">В рабочей области **Развитие сотрудников** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="2ff27-121">В области **Настройка компетенции** выберите **Типы навыков**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="2ff27-122">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-122">Select **New**.</span></span>

4. <span data-ttu-id="2ff27-123">Заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2ff27-123">Complete the following fields:</span></span>

   - <span data-ttu-id="2ff27-124">**Тип навыка**: введите название для типа навыка.</span><span class="sxs-lookup"><span data-stu-id="2ff27-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="2ff27-125">**Описание**: введите описание для типа навыков.</span><span class="sxs-lookup"><span data-stu-id="2ff27-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="2ff27-126">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="2ff27-127">Создание модели рейтинга</span><span class="sxs-lookup"><span data-stu-id="2ff27-127">Create a rating model</span></span>

<span data-ttu-id="2ff27-128">Модели рейтинга помогают оценить фактического уровня навыков лица, уровень, для которого они должны работать для достижения, или уровень навыка, необходимого для должности.</span><span class="sxs-lookup"><span data-stu-id="2ff27-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="2ff27-129">Каждому уровню в модели рейтинга назначается коэффициент.</span><span class="sxs-lookup"><span data-stu-id="2ff27-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="2ff27-130">В рабочей области **Развитие сотрудников** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="2ff27-131">В области **Настройка компетенции** выберите **Модели рейтинга**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="2ff27-132">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-132">Select **New**.</span></span>

4. <span data-ttu-id="2ff27-133">Заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2ff27-133">Complete the following fields:</span></span>

   - <span data-ttu-id="2ff27-134">**Рейтинг**: введите имя модели рейтинга, например **Навыки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="2ff27-135">**Описание**: введите описание для модели рейтинга, например **Рейтинги навыков**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="2ff27-136">В разделе **Уровни** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="2ff27-137">Для каждого уровня, который требуется добавить, заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2ff27-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="2ff27-138">**Уровень**: введите имя для уровня.</span><span class="sxs-lookup"><span data-stu-id="2ff27-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="2ff27-139">**Описание**: введите описание для уровня.</span><span class="sxs-lookup"><span data-stu-id="2ff27-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="2ff27-140">**Коэффициент**: введите коэффициент, равный 0–9.</span><span class="sxs-lookup"><span data-stu-id="2ff27-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="2ff27-141">Коэффициенты помогают нормировать оценки навыков, использующих разные модели рейтингов.</span><span class="sxs-lookup"><span data-stu-id="2ff27-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="2ff27-142">Каждый уровень должен иметь уникальный коэффициент.</span><span class="sxs-lookup"><span data-stu-id="2ff27-142">Each level must have a unique factor.</span></span> <span data-ttu-id="2ff27-143">Уровни с более высокими значениями коэффициента имеют больший вес в модели рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2ff27-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="2ff27-144">Продолжайте добавлять уровни по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="2ff27-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="2ff27-145">Вы можете ввести до 10 уровней для каждой модели рейтингов.</span><span class="sxs-lookup"><span data-stu-id="2ff27-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="2ff27-146">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="2ff27-147">Создание навыка</span><span class="sxs-lookup"><span data-stu-id="2ff27-147">Create a skill</span></span>

<span data-ttu-id="2ff27-148">Перед назначением навыка или созданием поиска сопоставления навыков или профиля навыков, необходимо ввести информацию о навыках на странице **Навыки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="2ff27-149">Для каждого навыка можно выбрать тип навыков и модель рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2ff27-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="2ff27-150">В рабочей области **Развитие сотрудников** выберите **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="2ff27-151">В области **Настройка компетенции** выберите **Навыки**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="2ff27-152">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-152">Select **New**.</span></span>

4. <span data-ttu-id="2ff27-153">Заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2ff27-153">Complete the following fields:</span></span>

   - <span data-ttu-id="2ff27-154">**Навык**: введите название для навыка.</span><span class="sxs-lookup"><span data-stu-id="2ff27-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="2ff27-155">**Описание**: введите описание для навыка.</span><span class="sxs-lookup"><span data-stu-id="2ff27-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="2ff27-156">**Рейтинг**: введите модель рейтинга, которую хотите использовать для этого навыка.</span><span class="sxs-lookup"><span data-stu-id="2ff27-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="2ff27-157">**Тип навыка**: выберите из списка типов навыков.</span><span class="sxs-lookup"><span data-stu-id="2ff27-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="2ff27-158">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2ff27-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ff27-159">См. также</span><span class="sxs-lookup"><span data-stu-id="2ff27-159">See also</span></span>

[<span data-ttu-id="2ff27-160">Ввод навыков</span><span class="sxs-lookup"><span data-stu-id="2ff27-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="2ff27-161">Сопоставление навыков</span><span class="sxs-lookup"><span data-stu-id="2ff27-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]