---
title: Определение программ лояльности
description: В этой процедуре показано, как настроить программу лояльности с двумя уровнями лояльности.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f30d4d1b66e5b4b90f7df67d8f76a95a100338
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415282"
---
# <a name="define-loyalty-programs"></a><span data-ttu-id="2a2fc-103">Определение программ лояльности</span><span class="sxs-lookup"><span data-stu-id="2a2fc-103">Define loyalty programs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a2fc-104">В этой процедуре показано, как настроить программу лояльности с двумя уровнями лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="2a2fc-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2a2fc-106">Перейдите в раздел Retail и Commerce > ..</span><span class="sxs-lookup"><span data-stu-id="2a2fc-106">Go to Retail and Commerce > ..</span></span> <span data-ttu-id="2a2fc-107">> "Программы лояльности".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="2a2fc-108">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-108">Click New.</span></span>
3. <span data-ttu-id="2a2fc-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2a2fc-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2a2fc-111">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-111">Click Add line.</span></span>
6. <span data-ttu-id="2a2fc-112">В поле "Уровень" введите число.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="2a2fc-113">В поле "Класс" введите название уровня лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="2a2fc-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2a2fc-115">В поле "Интервал дат" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a2fc-116">Этот интервал дат должен распространяться на будущее.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-116">This date interval should extend into the future.</span></span> <span data-ttu-id="2a2fc-117">Например, если продолжительность интервала дат, выбранного для золотого уровня, составляет один год, то клиент, соответствующий критериям золотого уровня, может получать поощрения, назначенные золотому уровню, в течение одного года.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="2a2fc-118">Если клиент повторно выполняет условия золотого уровня, находясь на этом уровне, дата окончания срока действия статуса уровня продлевается еще на один год, начиная с даты повторного выполнения условий.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="2a2fc-119">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2a2fc-120">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-120">Click Add line.</span></span>
12. <span data-ttu-id="2a2fc-121">В поле "Уровень" введите число.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="2a2fc-122">В поле "Класс" введите название уровня лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="2a2fc-123">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="2a2fc-124">В поле "Интервал дат" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="2a2fc-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2a2fc-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-126">Click Save.</span></span>
18. <span data-ttu-id="2a2fc-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a2fc-128">Правила уровня определяют минимальное количество баллов поощрения, которое необходимо набрать в течение периода времени, чтобы выполнить условия этого уровня.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="2a2fc-129">Переключите развертывание раздела "Правила класса".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="2a2fc-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-130">Click New.</span></span>
    * <span data-ttu-id="2a2fc-131">Для одного уровня может существовать несколько правил.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="2a2fc-132">Например, можно иметь три разных критерия, чтобы заработать уровень; потратить 500 долларов за один месяц, потратить 1000 долларов за один год либо иметь 20 транзакций в одном году.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="2a2fc-133">Для этого потребуется создать три правила уровня.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="2a2fc-134">В поле "Точки вознаграждения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a2fc-135">Это должен быть не погашаемый балл поощрения лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="2a2fc-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="2a2fc-137">В поле "Минимальное число накопленных баллов" введите число.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="2a2fc-138">Для самого низкого уровня, если все клиенты выполняют условия, просто участвуя в программе, введите 0 в этом поле.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="2a2fc-139">В поле "Интервал даты оценки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a2fc-140">Этот интервал дат должен распространяться на прошлое.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-140">This date interval should extend into the past.</span></span> <span data-ttu-id="2a2fc-141">Только баллы, полученные в течение этого интервала дат будут засчитываться для достижения минимального значения накопленных баллов.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="2a2fc-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="2a2fc-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-143">Click Save.</span></span>
27. <span data-ttu-id="2a2fc-144">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="2a2fc-145">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-145">Click New.</span></span>
29. <span data-ttu-id="2a2fc-146">В поле "Точки вознаграждения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="2a2fc-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="2a2fc-148">В поле "Минимальное число накопленных баллов" введите число.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="2a2fc-149">В поле "Интервал даты оценки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a2fc-150">Этот интервал дат должен распространяться на прошлое.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="2a2fc-151">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="2a2fc-152">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-152">Click Save.</span></span>
35. <span data-ttu-id="2a2fc-153">Щелкните "Ценовые группы".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-153">Click Price groups.</span></span>
    * <span data-ttu-id="2a2fc-154">Если вы хотите предоставлять скидки клиентам, участвующим в программах лояльности,</span><span class="sxs-lookup"><span data-stu-id="2a2fc-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="2a2fc-155">вам потребуется назначить одну или несколько групп цен программе лояльности и группы цен скидкам.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="2a2fc-156">Рекомендуется не смешивать группы цен между различными типам объектов со скидкам.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="2a2fc-157">Например, не используйте одну и ту же группу для скидок по программе лояльности и для скидок канала.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="2a2fc-158">В поле "Группа цен" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2a2fc-159">Ссылка "Группа цен" в верхней части страницы относится к программе лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="2a2fc-160">Ссылка "Группа цен" на экспресс-вкладке "Классы программы" относится только к конкретному уровню программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-160">The Price groups link in the Program tiers FastTab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="2a2fc-161">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="2a2fc-162">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-162">Click Save.</span></span>
39. <span data-ttu-id="2a2fc-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2a2fc-163">Close the page.</span></span>
40. <span data-ttu-id="2a2fc-164">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2a2fc-164">Click Save.</span></span>

