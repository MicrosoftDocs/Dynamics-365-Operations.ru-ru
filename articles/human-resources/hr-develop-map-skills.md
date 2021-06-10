---
title: Подбор персонала
description: Можно создать поиск для подбора персонала, чтобы найти квалифицированного сотрудника в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076611"
---
# <a name="map-skills"></a><span data-ttu-id="b78ea-103">Подбор персонала</span><span class="sxs-lookup"><span data-stu-id="b78ea-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b78ea-104">Можно создать поиск для подбора персонала, чтобы найти квалифицированного сотрудника в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b78ea-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b78ea-105">Поиск для подбора персонала возвращает результаты для введенного вами критерия путем поиска следующей информации:</span><span class="sxs-lookup"><span data-stu-id="b78ea-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="b78ea-106">Навыки</span><span class="sxs-lookup"><span data-stu-id="b78ea-106">Skills</span></span>
- <span data-ttu-id="b78ea-107">Образование</span><span class="sxs-lookup"><span data-stu-id="b78ea-107">Education</span></span>
- <span data-ttu-id="b78ea-108">Сертификаты</span><span class="sxs-lookup"><span data-stu-id="b78ea-108">Certificates</span></span>
- <span data-ttu-id="b78ea-109">Позиции</span><span class="sxs-lookup"><span data-stu-id="b78ea-109">Positions</span></span>
- <span data-ttu-id="b78ea-110">Проектный опыт</span><span class="sxs-lookup"><span data-stu-id="b78ea-110">Project experience</span></span>

<span data-ttu-id="b78ea-111">Например, можно найти людей в организации, которые получили свои CPA.</span><span class="sxs-lookup"><span data-stu-id="b78ea-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="b78ea-112">Профили подбора персонала позволяют найти текущих сотрудников или кандидатов с квалификациями, которые прямо соответствуют бизнес-потребностям.</span><span class="sxs-lookup"><span data-stu-id="b78ea-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="b78ea-113">Только сотрудники, кандидаты и контактные лица, которые выбраны для включения в поиск подбора персонала, будут отображаться в списке результатов подбора персонала или включаться в профиль навыков.</span><span class="sxs-lookup"><span data-stu-id="b78ea-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="b78ea-114">Для того, чтобы включить пользователя в поиски по подбору персонала, установите для параметра **Включить в подбор персонала** значение **Да** на следующих страницах:</span><span class="sxs-lookup"><span data-stu-id="b78ea-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="b78ea-115">Рабочий</span><span class="sxs-lookup"><span data-stu-id="b78ea-115">Worker</span></span><br>
> - <span data-ttu-id="b78ea-116">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="b78ea-116">Employee</span></span><br>
> - <span data-ttu-id="b78ea-117">Кандидат</span><span class="sxs-lookup"><span data-stu-id="b78ea-117">Applicant</span></span><br>
> - <span data-ttu-id="b78ea-118">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="b78ea-118">Contacts</span></span><br>

<span data-ttu-id="b78ea-119">Чтобы создать подбор персонала, перейдите на страницу **Развитие сотрудников > Ссылки > Подбор персонала**.</span><span class="sxs-lookup"><span data-stu-id="b78ea-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="b78ea-120">Чтобы создать профиль подбора персонала, перейдите на страницу **Развитие сотрудников > Ссылки > Профили подбора персонала**.</span><span class="sxs-lookup"><span data-stu-id="b78ea-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="b78ea-121">Анализ несоответствия навыков и анализ профилей навыков</span><span class="sxs-lookup"><span data-stu-id="b78ea-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="b78ea-122">Можно создать анализ профиля навыков для просмотра списка компетенций сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b78ea-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="b78ea-123">Можно создать анализ несоответствия навыков для сравнения навыков лица с навыками, которые требуются для задания.</span><span class="sxs-lookup"><span data-stu-id="b78ea-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="b78ea-124">Чтобы создать анализ несоответствия, перейдите на страницу **Развитие сотрудников > Ссылки > Сравнительный анализ квалификационных навыков сотрудника заданию**.</span><span class="sxs-lookup"><span data-stu-id="b78ea-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="b78ea-125">Чтобы создать анализ профиля навыков, перейдите на страницу **Развитие сотрудников > Ссылки > Анализ профиля навыков**.</span><span class="sxs-lookup"><span data-stu-id="b78ea-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b78ea-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b78ea-126">See also</span></span>

[<span data-ttu-id="b78ea-127">Настройка навыков</span><span class="sxs-lookup"><span data-stu-id="b78ea-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="b78ea-128">Ввод навыков</span><span class="sxs-lookup"><span data-stu-id="b78ea-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]