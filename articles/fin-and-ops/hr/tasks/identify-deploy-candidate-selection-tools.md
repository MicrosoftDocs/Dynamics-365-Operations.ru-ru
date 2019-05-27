---
title: Определение и развертывание средств выбора кандидатов
description: Найти соответствующих кандидатов для заполнения вакансий может быть трудно, особенно если для должности требуется уникальный набор навыков.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51200a67a51097c438370866cb9d0ccbebe8392c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507690"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="754ad-103">Определение и развертывание средств выбора кандидатов</span><span class="sxs-lookup"><span data-stu-id="754ad-103">Identify and deploy candidate selection tools</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="754ad-104">Найти соответствующих кандидатов для заполнения вакансий может быть трудно, особенно если для должности требуется уникальный набор навыков.</span><span class="sxs-lookup"><span data-stu-id="754ad-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="754ad-105">Однако кандидаты с необходимыми навыками могут уже работать в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="754ad-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="754ad-106">Вы можете выполнить поиск определенного набора навыков среди существующих сотрудников или новых кандидатов.</span><span class="sxs-lookup"><span data-stu-id="754ad-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="754ad-107">Это позволяет менеджеру по найму быстро найти и просмотреть кандидатов, которые подали заявление на открытую позицию в данный момент или в прошлом, или найти потенциальных кандидатов среди существующих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="754ad-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="754ad-108">Используйте эту запись задачи, чтобы узнать, как функция подбора персонала может помочь найти нужного человека на открытую позицию.</span><span class="sxs-lookup"><span data-stu-id="754ad-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="754ad-109">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="754ad-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="754ad-110">Перейдите в раздел "Управление персоналом" > "Компетенции" > "Анализ навыков" > "Профили подбора персонала".</span><span class="sxs-lookup"><span data-stu-id="754ad-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="754ad-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="754ad-111">Click New.</span></span>
3. <span data-ttu-id="754ad-112">В поле "Подбор персонала" введите имя подбора персонала.</span><span class="sxs-lookup"><span data-stu-id="754ad-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="754ad-113">Пример: "Бухгалтер".</span><span class="sxs-lookup"><span data-stu-id="754ad-113">Example: Accountant.</span></span>
4. <span data-ttu-id="754ad-114">В поле "Описание" введите описание подбора персонала.</span><span class="sxs-lookup"><span data-stu-id="754ad-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="754ad-115">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="754ad-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="754ad-116">Щелкните "Выбор профиля".</span><span class="sxs-lookup"><span data-stu-id="754ad-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="754ad-117">Используйте параметр "Выбор профиля", чтобы получить данные "Сертификат", "Навык" и "Образование" из выбранного раздела "Человек", "Задание" или "Курс" в качестве основы для поиска.</span><span class="sxs-lookup"><span data-stu-id="754ad-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="754ad-118">Затем можно добавить или удалить критерии, указать, являются ли критерии дополнительными, и ранжировать важность критериев.</span><span class="sxs-lookup"><span data-stu-id="754ad-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="754ad-119">Щелкните "Задание".</span><span class="sxs-lookup"><span data-stu-id="754ad-119">Click Job.</span></span>
8. <span data-ttu-id="754ad-120">В поле "Задание" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="754ad-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="754ad-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="754ad-121">Click OK.</span></span>
10. <span data-ttu-id="754ad-122">Разверните экспресс-вкладку "Диапазон" и введите дополнительные сведения, например подразделение.</span><span class="sxs-lookup"><span data-stu-id="754ad-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="754ad-123">Разверните экспресс-вкладку "Сертификаты", чтобы просмотреть или изменить сертификаты.</span><span class="sxs-lookup"><span data-stu-id="754ad-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="754ad-124">Разверните экспресс-вкладку "Навыки", чтобы просмотреть или изменить навыки.</span><span class="sxs-lookup"><span data-stu-id="754ad-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="754ad-125">Разверните экспресс-вкладку "Образование", чтобы просмотреть или изменить критерии образования.</span><span class="sxs-lookup"><span data-stu-id="754ad-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="754ad-126">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="754ad-126">Click Execute.</span></span>
15. <span data-ttu-id="754ad-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="754ad-127">Click OK.</span></span>
16. <span data-ttu-id="754ad-128">Щелкните "Результат".</span><span class="sxs-lookup"><span data-stu-id="754ad-128">Click Result.</span></span>
17. <span data-ttu-id="754ad-129">Щелкните "Результат".</span><span class="sxs-lookup"><span data-stu-id="754ad-129">Click Result.</span></span>
18. <span data-ttu-id="754ad-130">Щелкните Восстановить.</span><span class="sxs-lookup"><span data-stu-id="754ad-130">Click Resume.</span></span>
19. <span data-ttu-id="754ad-131">Щелкните "Сертификаты".</span><span class="sxs-lookup"><span data-stu-id="754ad-131">Click Certificates.</span></span>
    * <span data-ttu-id="754ad-132">Можно выполнить детализацию по каждому лицу и просмотреть более подробные сведения об образовании, навыках, опыте работы и т. д.</span><span class="sxs-lookup"><span data-stu-id="754ad-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="754ad-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="754ad-133">Close the page.</span></span>
21. <span data-ttu-id="754ad-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="754ad-134">Close the page.</span></span>
22. <span data-ttu-id="754ad-135">Выберите результат еще раз.</span><span class="sxs-lookup"><span data-stu-id="754ad-135">Select result again.</span></span>
23. <span data-ttu-id="754ad-136">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="754ad-136">Click Report.</span></span>
    * <span data-ttu-id="754ad-137">Лучшие совпадения будут указаны вверху списка в отчете.</span><span class="sxs-lookup"><span data-stu-id="754ad-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="754ad-138">В списке также указывается элемент несоответствия.</span><span class="sxs-lookup"><span data-stu-id="754ad-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="754ad-139">Это разница между уровнем, указанным при подборе персонала, и уровнем навыка, который назначен лицу.</span><span class="sxs-lookup"><span data-stu-id="754ad-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="754ad-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="754ad-140">Close the page.</span></span>
25. <span data-ttu-id="754ad-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="754ad-141">Click Save.</span></span>

