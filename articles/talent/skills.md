---
title: "Совмещение навыков рабочей силы с потребностями бизнеса"
description: "Можно отслеживать навыки, которые сотрудники, кандидаты или контактные лица имеют или должны иметь, чтобы эффективно выполнять свои роли. Также можно указывать навыки, необходимые для определенной должности."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3a5b9f98b371dbad9b6b0538e0d9975dc5ed701c
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="36ede-104">Совмещение навыков рабочей силы с потребностями бизнеса</span><span class="sxs-lookup"><span data-stu-id="36ede-104">Align workforce skills with business needs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="36ede-105">Можно отслеживать навыки, которые сотрудники, кандидаты или контактные лица имеют или должны иметь, чтобы эффективно выполнять свои роли.</span><span class="sxs-lookup"><span data-stu-id="36ede-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="36ede-106">Также можно указывать навыки, необходимые для определенной должности.</span><span class="sxs-lookup"><span data-stu-id="36ede-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="36ede-107">Примеры навыков, которые можно отслеживать, включают следующее:</span><span class="sxs-lookup"><span data-stu-id="36ede-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="36ede-108">Способность контролировать - Умение контролировать работу других.</span><span class="sxs-lookup"><span data-stu-id="36ede-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="36ede-109">Лидерство -Умение возглавить сотрудников и деловые домены.</span><span class="sxs-lookup"><span data-stu-id="36ede-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="36ede-110">Планирование - Умение предвидеть, формулировать предположения и принимать решения на их основании.</span><span class="sxs-lookup"><span data-stu-id="36ede-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="36ede-111">HTML — Возможность создавать код HTML.</span><span class="sxs-lookup"><span data-stu-id="36ede-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="36ede-112">Перед назначением навыка к лицу или должности, создание поиска Подбора персонала или созданием профиль навыков, необходимо ввести информацию о навыках на странице **Навыки**.</span><span class="sxs-lookup"><span data-stu-id="36ede-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="36ede-113">Для каждого навыка можно выбрать тип навыков и модель рейтинга.</span><span class="sxs-lookup"><span data-stu-id="36ede-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="36ede-114">Модели рейтинга</span><span class="sxs-lookup"><span data-stu-id="36ede-114">Rating models</span></span>
<span data-ttu-id="36ede-115">Модели рейтинга помогают оценить фактического уровня навыков лица, уровень, для которого они должны работать для достижения, или уровень навыка, который необходим для должности.</span><span class="sxs-lookup"><span data-stu-id="36ede-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="36ede-116">Вы можете ввести до 10 уровней для модели рейтингов.</span><span class="sxs-lookup"><span data-stu-id="36ede-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="36ede-117">Каждому уровню в модели рейтинга назначается коэффициент.</span><span class="sxs-lookup"><span data-stu-id="36ede-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="36ede-118">Значение коэффициента будет использоваться для нормирования оценок навыков, использующих разные модели рейтингов.</span><span class="sxs-lookup"><span data-stu-id="36ede-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="36ede-119">Коэффициент должен быть числом от 0 до 9. Каждому уровню должен соответствовать уникальный коэффициент.</span><span class="sxs-lookup"><span data-stu-id="36ede-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="36ede-120">Уровни с более высокими значениями коэффициента имеют больший вес в модели рейтинга.</span><span class="sxs-lookup"><span data-stu-id="36ede-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="36ede-121">Определите навыки должности</span><span class="sxs-lookup"><span data-stu-id="36ede-121">Specify job skills</span></span>
<span data-ttu-id="36ede-122">При вводе информации о должности можно указать навыки, которые сотрудник должен иметь, чтобы выполнять работу, необходимую для должности.</span><span class="sxs-lookup"><span data-stu-id="36ede-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="36ede-123">Кроме того, можно определить желательный уровень для каждого навыка, а также уровень важности навыка.</span><span class="sxs-lookup"><span data-stu-id="36ede-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="36ede-124">Для различных должностей могут потребоваться разные уровни важности одинаковых навыков.</span><span class="sxs-lookup"><span data-stu-id="36ede-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="36ede-125">Ввод навыков для сотрудников, кандидатов и контактных лиц</span><span class="sxs-lookup"><span data-stu-id="36ede-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="36ede-126">Можно ввести целевые навыки или фактические навыки для сотрудников, кандидатов и контактных лиц.</span><span class="sxs-lookup"><span data-stu-id="36ede-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="36ede-127">Целевые навык — навык, который лицо хочет получить.</span><span class="sxs-lookup"><span data-stu-id="36ede-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="36ede-128">Фактический навык — навык, которым лицо обладает.</span><span class="sxs-lookup"><span data-stu-id="36ede-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="36ede-129">Подбор персонала и профили подбора персонала</span><span class="sxs-lookup"><span data-stu-id="36ede-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="36ede-130">Вы можете создать поиск по подбору персонала, чтобы найти работника, заявителя или контактное лицо, обладающих квалификацией для выполнения задачи определенного типа.</span><span class="sxs-lookup"><span data-stu-id="36ede-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="36ede-131">Поиски по подбору персонала просматривают навыки, образование, сертификаты, выборные должности и опыт участия в проектах и возвращают результаты, которые соответствуют введенным критериям.</span><span class="sxs-lookup"><span data-stu-id="36ede-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="36ede-132">Например, может быть полезно знать, какие работники в вашей организации получили свои CPA.</span><span class="sxs-lookup"><span data-stu-id="36ede-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="36ede-133">Профили подбора персонала позволяют найти текущих сотрудников или кандидатов с квалификациями, которые прямо соответствуют бизнес-потребностям.</span><span class="sxs-lookup"><span data-stu-id="36ede-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="36ede-134">Например, вы можете создать профиль подбора персонала для открытой позиции в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="36ede-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="36ede-135">Путем создания профиля для определенной должности или копирования навыков, образования и сертификатов из этой должности в профиль, вы можете быстро искать работников, заявителей и контактных лиц, которые соответствуют одному или нескольким из критериев, введенных в профиль, а также просматривать список кандидатов, навыки которых наиболее близко соответствуют навыкам, необходимых для должности.</span><span class="sxs-lookup"><span data-stu-id="36ede-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="36ede-136">**Примечание.** Только сотрудники, кандидаты и контактные лица, которые выбраны для включения в поиск подбора персонала, могут отображаться в списке результатов подбора персонала или включаться в профиль навыков.</span><span class="sxs-lookup"><span data-stu-id="36ede-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="36ede-137">Для того, чтобы включить работника, заявителя или контактное лицо в поиски по подбору персонала, установите для параметра **Включить в подбор персонала** значение "Да" на следующих страницах:</span><span class="sxs-lookup"><span data-stu-id="36ede-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="36ede-138">Работник</span><span class="sxs-lookup"><span data-stu-id="36ede-138">Worker</span></span>
> + <span data-ttu-id="36ede-139">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="36ede-139">Employee</span></span>
> + <span data-ttu-id="36ede-140">Кандидат</span><span class="sxs-lookup"><span data-stu-id="36ede-140">Applicant</span></span>
> + <span data-ttu-id="36ede-141">Контакты</span><span class="sxs-lookup"><span data-stu-id="36ede-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="36ede-142">Анализ несоответствия навыков и анализ профилей навыков</span><span class="sxs-lookup"><span data-stu-id="36ede-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="36ede-143">Можно создать анализ профилей навыков для просмотра списка всех навыков работника, кандидата или контактного лица на конкретную дату.</span><span class="sxs-lookup"><span data-stu-id="36ede-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="36ede-144">Можно также создать анализ несоответствия навыков для сравнения навыков лица с навыками, которые требуются для конкретной работы</span><span class="sxs-lookup"><span data-stu-id="36ede-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="36ede-145">См. также</span><span class="sxs-lookup"><span data-stu-id="36ede-145">See also</span></span>
--------

[<span data-ttu-id="36ede-146">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="36ede-146">Human resources</span></span>](index.md)




