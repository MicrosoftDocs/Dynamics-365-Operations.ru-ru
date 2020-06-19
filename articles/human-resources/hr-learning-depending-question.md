---
title: Создание вопроса, зависящего от ответа на предыдущий вопрос
description: Зависимые вопросы позволяют указать, какой следующий вопрос будет предложен респонденту, в зависимости от ответа на предыдущий вопрос.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4295b49336ec7ac3cff4deba675bc63511be48de
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429551"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="ef94c-103">Создание вопроса, зависящего от ответа на предыдущий вопрос</span><span class="sxs-lookup"><span data-stu-id="ef94c-103">Make a question dependent on the answer of the previous question</span></span>



<span data-ttu-id="ef94c-104">Зависимые вопросы позволяют указать, какой следующий вопрос будет предложен респонденту, в зависимости от ответа на предыдущий вопрос.</span><span class="sxs-lookup"><span data-stu-id="ef94c-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="ef94c-105">Например, если вы спросили "Вы любите кофе или чай", логичный следующий вопрос можно определить в зависимости от того, кофе или чай респондент выбрал в качестве своего ответа.</span><span class="sxs-lookup"><span data-stu-id="ef94c-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="ef94c-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ef94c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="ef94c-107">Поиск существующей анкеты</span><span class="sxs-lookup"><span data-stu-id="ef94c-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="ef94c-108">Перейдите в раздел "Анкета" > "Дизайн" > "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="ef94c-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="ef94c-109">Выберите в списке анкету WorkFH.</span><span class="sxs-lookup"><span data-stu-id="ef94c-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="ef94c-110">Добавление всех вопросов и подвопросов в анкету</span><span class="sxs-lookup"><span data-stu-id="ef94c-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="ef94c-111">Щелкните "Вопросы".</span><span class="sxs-lookup"><span data-stu-id="ef94c-111">Click Questions.</span></span>
2. <span data-ttu-id="ef94c-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ef94c-112">Click New.</span></span>
3. <span data-ttu-id="ef94c-113">В поле "Вопрос" выберите вопрос номер 00016.</span><span class="sxs-lookup"><span data-stu-id="ef94c-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="ef94c-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ef94c-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ef94c-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ef94c-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ef94c-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ef94c-116">Click Save.</span></span>
7. <span data-ttu-id="ef94c-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ef94c-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="ef94c-118">Установка параметра "Последовательность анкеты" в значение "Зависимый" и создание зависимости между вопросом и соответствующим предыдущим вопросом</span><span class="sxs-lookup"><span data-stu-id="ef94c-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="ef94c-119">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="ef94c-119">Click Edit.</span></span>
2. <span data-ttu-id="ef94c-120">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="ef94c-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="ef94c-121">В поле "Порядок вопросов" выберите "Зависимый".</span><span class="sxs-lookup"><span data-stu-id="ef94c-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="ef94c-122">Щелкните "Зависимый запрос".</span><span class="sxs-lookup"><span data-stu-id="ef94c-122">Click Conditional question.</span></span>
5. <span data-ttu-id="ef94c-123">В дереве выберите "Вопросы\Поясните, почему вы дали такой ответ на предыдущий вопрос?".</span><span class="sxs-lookup"><span data-stu-id="ef94c-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="ef94c-124">В поле "Ведущий вопрос" выберите вопрос 00009.</span><span class="sxs-lookup"><span data-stu-id="ef94c-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="ef94c-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ef94c-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ef94c-126">В поле "Ответ" введите порядковый идентификатор ответа того варианта ответа, от которого должен зависеть вопрос.</span><span class="sxs-lookup"><span data-stu-id="ef94c-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="ef94c-127">Например, для первого варианта ответа введите 1.</span><span class="sxs-lookup"><span data-stu-id="ef94c-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="ef94c-128">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="ef94c-128">Click Save.</span></span>
10. <span data-ttu-id="ef94c-129">В дереве выберите "Вопросы\Я получаю достойную оплату за свою работу".</span><span class="sxs-lookup"><span data-stu-id="ef94c-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="ef94c-130">Обратите внимание, что дерево вопроса обновилось, чтобы отразить зависимость.</span><span class="sxs-lookup"><span data-stu-id="ef94c-130">Note that the question tree updated to show the dependency.</span></span>  

