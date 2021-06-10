---
title: Создание закрытого вопроса
description: Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0316661d8be04cc5912e88bc50b3a1c7a73bbcb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056692"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="78c26-103">Создание закрытого вопроса</span><span class="sxs-lookup"><span data-stu-id="78c26-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="78c26-104">Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.</span><span class="sxs-lookup"><span data-stu-id="78c26-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="78c26-105">Сначала необходимо создать группу ответов с ответами, а затем создать вопрос, в котором будет использоваться группа ответов.</span><span class="sxs-lookup"><span data-stu-id="78c26-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="78c26-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="78c26-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="78c26-107">Создание группы ответов</span><span class="sxs-lookup"><span data-stu-id="78c26-107">Create an answer group</span></span>
1. <span data-ttu-id="78c26-108">Перейдите в раздел "Анкета" > "Дизайн" > "Группы ответов".</span><span class="sxs-lookup"><span data-stu-id="78c26-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="78c26-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78c26-109">Click New.</span></span>
3. <span data-ttu-id="78c26-110">В поле "Группа ответов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="78c26-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="78c26-112">С помощью функциональности "Случайный выбор" можно размещать ответы в новом случайном порядке всякий раз, когда группа ответов используется для вопроса.</span><span class="sxs-lookup"><span data-stu-id="78c26-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="78c26-113">Щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="78c26-113">Click Answer.</span></span>
6. <span data-ttu-id="78c26-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78c26-114">Click New.</span></span>
    * <span data-ttu-id="78c26-115">Порядковый номер определяет порядок, в котором отображаются ответы, кроме случаев, когда для группы ответов выбран параметр "Случайный выбор".</span><span class="sxs-lookup"><span data-stu-id="78c26-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="78c26-116">Ответам могут быть присвоены баллы для использования при оценке анкеты.</span><span class="sxs-lookup"><span data-stu-id="78c26-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="78c26-117">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="78c26-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="78c26-118">Правильный ответ можно пометить, чтобы указать, что выбранный ответ является правильным.</span><span class="sxs-lookup"><span data-stu-id="78c26-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="78c26-119">Это можно использовать для оценки анкеты.</span><span class="sxs-lookup"><span data-stu-id="78c26-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="78c26-120">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="78c26-121">Продолжайте создавать варианты для выбора ответа для группы ответов.</span><span class="sxs-lookup"><span data-stu-id="78c26-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="78c26-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78c26-122">Click New.</span></span>
10. <span data-ttu-id="78c26-123">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="78c26-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="78c26-124">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="78c26-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="78c26-125">Click New.</span></span>
13. <span data-ttu-id="78c26-126">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="78c26-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="78c26-127">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="78c26-128">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="78c26-128">Click New.</span></span>
16. <span data-ttu-id="78c26-129">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="78c26-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="78c26-130">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="78c26-131">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="78c26-131">Click New.</span></span>
19. <span data-ttu-id="78c26-132">В поле "Баллы" введите число.</span><span class="sxs-lookup"><span data-stu-id="78c26-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="78c26-133">В поле "Ответ" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="78c26-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="78c26-134">Close the page.</span></span>
22. <span data-ttu-id="78c26-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="78c26-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="78c26-136">Создание вопроса</span><span class="sxs-lookup"><span data-stu-id="78c26-136">Create the question</span></span>
1. <span data-ttu-id="78c26-137">Перейдите в раздел "Анкета" > "Дизайн" > "Вопросы".</span><span class="sxs-lookup"><span data-stu-id="78c26-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="78c26-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="78c26-138">Click New.</span></span>
3. <span data-ttu-id="78c26-139">С помощью поля "Тип" связанные вопросы можно сгруппировать вместе.</span><span class="sxs-lookup"><span data-stu-id="78c26-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="78c26-140">Для закрытых вопросов можно использовать типы ввода "Флажок", "Переключатель" или "Поле со списком".</span><span class="sxs-lookup"><span data-stu-id="78c26-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="78c26-141">В поле "Тип ввода" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="78c26-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="78c26-142">В поле "Группа ответов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="78c26-143">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="78c26-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]