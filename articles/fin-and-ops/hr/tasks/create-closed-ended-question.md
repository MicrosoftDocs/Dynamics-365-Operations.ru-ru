--- 
title: "Создание закрытого вопроса"
description: "Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fdfac92b80774adb8376d5c2e945d063173188c8
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="b766d-103">Создание закрытого вопроса</span><span class="sxs-lookup"><span data-stu-id="b766d-103">Create a closed ended question</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b766d-104">Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.</span><span class="sxs-lookup"><span data-stu-id="b766d-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="b766d-105">Сначала необходимо создать группу ответов с ответами, а затем создать вопрос, в котором будет использоваться группа ответов.</span><span class="sxs-lookup"><span data-stu-id="b766d-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="b766d-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b766d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="b766d-107">Создание группы ответов</span><span class="sxs-lookup"><span data-stu-id="b766d-107">Create an answer group</span></span>
1. <span data-ttu-id="b766d-108">Перейдите в раздел "Анкета" > "Дизайн" > "Группы ответов".</span><span class="sxs-lookup"><span data-stu-id="b766d-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="b766d-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b766d-109">Click New.</span></span>
3. <span data-ttu-id="b766d-110">В поле "Группа ответов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="b766d-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b766d-112">С помощью функциональности "Случайный выбор" можно размещать ответы в новом случайном порядке всякий раз, когда группа ответов используется для вопроса.</span><span class="sxs-lookup"><span data-stu-id="b766d-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="b766d-113">Щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="b766d-113">Click Answer.</span></span>
6. <span data-ttu-id="b766d-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b766d-114">Click New.</span></span>
    * <span data-ttu-id="b766d-115">Порядковый номер определяет порядок, в котором отображаются ответы, кроме случаев, когда для группы ответов выбран параметр "Случайный выбор".</span><span class="sxs-lookup"><span data-stu-id="b766d-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="b766d-116">Ответам могут быть присвоены баллы для использования при оценке анкеты.</span><span class="sxs-lookup"><span data-stu-id="b766d-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="b766d-117">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="b766d-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="b766d-118">Правильный ответ можно пометить, чтобы указать, что выбранный ответ является правильным.</span><span class="sxs-lookup"><span data-stu-id="b766d-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="b766d-119">Это можно использовать для оценки анкеты.</span><span class="sxs-lookup"><span data-stu-id="b766d-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="b766d-120">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="b766d-121">Продолжайте создавать варианты для выбора ответа для группы ответов.</span><span class="sxs-lookup"><span data-stu-id="b766d-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="b766d-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b766d-122">Click New.</span></span>
10. <span data-ttu-id="b766d-123">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="b766d-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="b766d-124">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="b766d-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="b766d-125">Click New.</span></span>
13. <span data-ttu-id="b766d-126">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="b766d-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="b766d-127">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="b766d-128">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="b766d-128">Click New.</span></span>
16. <span data-ttu-id="b766d-129">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="b766d-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="b766d-130">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="b766d-131">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="b766d-131">Click New.</span></span>
19. <span data-ttu-id="b766d-132">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="b766d-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="b766d-133">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="b766d-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b766d-134">Close the page.</span></span>
22. <span data-ttu-id="b766d-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b766d-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="b766d-136">Создание вопроса</span><span class="sxs-lookup"><span data-stu-id="b766d-136">Create the question</span></span>
1. <span data-ttu-id="b766d-137">Перейдите в раздел "Анкета" > "Дизайн" > "Вопросы".</span><span class="sxs-lookup"><span data-stu-id="b766d-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="b766d-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b766d-138">Click New.</span></span>
3. <span data-ttu-id="b766d-139">С помощью поля "Тип" связанные вопросы можно сгруппировать вместе.</span><span class="sxs-lookup"><span data-stu-id="b766d-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="b766d-140">Для закрытых вопросов можно использовать типы ввода "Флажок", "Переключатель" или "Поле со списком".</span><span class="sxs-lookup"><span data-stu-id="b766d-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="b766d-141">В поле "Тип ввода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="b766d-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="b766d-142">В поле "Группа ответов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="b766d-143">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b766d-143">In the Text field, type a value.</span></span>


