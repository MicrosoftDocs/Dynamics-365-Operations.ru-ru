---
title: Создание закрытого вопроса
description: Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b08988a3872cec39b7592732d23862e959aae79
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "332273"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="84e46-103">Создание закрытого вопроса</span><span class="sxs-lookup"><span data-stu-id="84e46-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84e46-104">Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.</span><span class="sxs-lookup"><span data-stu-id="84e46-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="84e46-105">Сначала необходимо создать группу ответов с ответами, а затем создать вопрос, в котором будет использоваться группа ответов.</span><span class="sxs-lookup"><span data-stu-id="84e46-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="84e46-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="84e46-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="84e46-107">Создание группы ответов</span><span class="sxs-lookup"><span data-stu-id="84e46-107">Create an answer group</span></span>
1. <span data-ttu-id="84e46-108">Перейдите в раздел "Анкета" > "Дизайн" > "Группы ответов".</span><span class="sxs-lookup"><span data-stu-id="84e46-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="84e46-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84e46-109">Click New.</span></span>
3. <span data-ttu-id="84e46-110">В поле "Группа ответов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="84e46-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="84e46-112">С помощью функциональности "Случайный выбор" можно размещать ответы в новом случайном порядке всякий раз, когда группа ответов используется для вопроса.</span><span class="sxs-lookup"><span data-stu-id="84e46-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="84e46-113">Щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="84e46-113">Click Answer.</span></span>
6. <span data-ttu-id="84e46-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84e46-114">Click New.</span></span>
    * <span data-ttu-id="84e46-115">Порядковый номер определяет порядок, в котором отображаются ответы, кроме случаев, когда для группы ответов выбран параметр "Случайный выбор".</span><span class="sxs-lookup"><span data-stu-id="84e46-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="84e46-116">Ответам могут быть присвоены баллы для использования при оценке анкеты.</span><span class="sxs-lookup"><span data-stu-id="84e46-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="84e46-117">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="84e46-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="84e46-118">Правильный ответ можно пометить, чтобы указать, что выбранный ответ является правильным.</span><span class="sxs-lookup"><span data-stu-id="84e46-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="84e46-119">Это можно использовать для оценки анкеты.</span><span class="sxs-lookup"><span data-stu-id="84e46-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="84e46-120">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="84e46-121">Продолжайте создавать варианты для выбора ответа для группы ответов.</span><span class="sxs-lookup"><span data-stu-id="84e46-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="84e46-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84e46-122">Click New.</span></span>
10. <span data-ttu-id="84e46-123">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="84e46-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="84e46-124">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="84e46-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84e46-125">Click New.</span></span>
13. <span data-ttu-id="84e46-126">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="84e46-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="84e46-127">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="84e46-128">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84e46-128">Click New.</span></span>
16. <span data-ttu-id="84e46-129">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="84e46-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="84e46-130">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="84e46-131">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84e46-131">Click New.</span></span>
19. <span data-ttu-id="84e46-132">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="84e46-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="84e46-133">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="84e46-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e46-134">Close the page.</span></span>
22. <span data-ttu-id="84e46-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e46-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="84e46-136">Создание вопроса</span><span class="sxs-lookup"><span data-stu-id="84e46-136">Create the question</span></span>
1. <span data-ttu-id="84e46-137">Перейдите в раздел "Анкета" > "Дизайн" > "Вопросы".</span><span class="sxs-lookup"><span data-stu-id="84e46-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="84e46-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84e46-138">Click New.</span></span>
3. <span data-ttu-id="84e46-139">С помощью поля "Тип" связанные вопросы можно сгруппировать вместе.</span><span class="sxs-lookup"><span data-stu-id="84e46-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="84e46-140">Для закрытых вопросов можно использовать типы ввода "Флажок", "Переключатель" или "Поле со списком".</span><span class="sxs-lookup"><span data-stu-id="84e46-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="84e46-141">В поле "Тип ввода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="84e46-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="84e46-142">В поле "Группа ответов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="84e46-143">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84e46-143">In the Text field, type a value.</span></span>

