--- 
title: "Настройка профилей разноски основных средства"
description: "В этом руководстве по задаче показано, как настроить профили разноски основных средств."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="6ec58-103">Настройка профилей разноски основных средства</span><span class="sxs-lookup"><span data-stu-id="6ec58-103">Set up fixed asset posting profiles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ec58-104">В этом руководстве по задаче показано, как настроить профили разноски основных средств.</span><span class="sxs-lookup"><span data-stu-id="6ec58-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="6ec58-105">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="6ec58-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="6ec58-106">Примеры, представленные в руководстве по задаче, предназначены для основного профиля разноски, хотя профили разноски должны отвечать требованиям определенных планов счетов и финансовой отчетности.</span><span class="sxs-lookup"><span data-stu-id="6ec58-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="6ec58-107">Перейдите в раздел "Основные средства" > "Настройка" > "Профили разноски основных средств".</span><span class="sxs-lookup"><span data-stu-id="6ec58-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="6ec58-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6ec58-108">Click New.</span></span>
3. <span data-ttu-id="6ec58-109">В поле "Профиль разноски" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="6ec58-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6ec58-111">Потребуется создать профиль разноски для каждого типа проводки основных средств, который будет использоваться при работе с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="6ec58-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="6ec58-112">В этом руководстве по задаче будет использоваться тип проводки "Приобретение".</span><span class="sxs-lookup"><span data-stu-id="6ec58-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="6ec58-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-113">Click Add.</span></span>
6. <span data-ttu-id="6ec58-114">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="6ec58-115">Поле "Группировки" позволяет определить профиль разноски до значения "Таблица" (один счет настраивается для каждого основного средства) или "Группа" (один счет настраивается для каждой группы основных средств).</span><span class="sxs-lookup"><span data-stu-id="6ec58-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="6ec58-116">В этом руководстве по задаче выбрано значение "Все" для применения ко всем основным средствам с указанной книгой.</span><span class="sxs-lookup"><span data-stu-id="6ec58-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="6ec58-117">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="6ec58-118">Для параметра "Приобретения" можно ввести корр. счет или оставить это поле пустым, чтобы заполнить его для определенной проводки.</span><span class="sxs-lookup"><span data-stu-id="6ec58-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="6ec58-119">В поле "Тип проводки" выберите "Корректировка приобретения".</span><span class="sxs-lookup"><span data-stu-id="6ec58-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="6ec58-120">Для проводок о корректировке приобретения используются те же счета, что и для проводок приобретения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="6ec58-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-121">Click Add.</span></span>
10. <span data-ttu-id="6ec58-122">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="6ec58-123">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="6ec58-124">Для параметра "Корректировки приобретений " можно ввести корр. счет или оставить это поле пустым, чтобы заполнить его для определенной проводки.</span><span class="sxs-lookup"><span data-stu-id="6ec58-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="6ec58-125">В поле "Тип проводки" выберите "Амортизация".</span><span class="sxs-lookup"><span data-stu-id="6ec58-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="6ec58-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-126">Click Add.</span></span>
14. <span data-ttu-id="6ec58-127">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="6ec58-128">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="6ec58-129">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="6ec58-130">В поле "Тип проводки" выберите "Корректировка амортизации".</span><span class="sxs-lookup"><span data-stu-id="6ec58-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="6ec58-131">Для проводок о корректировке амортизации используются те же счета, что и для проводок амортизации.</span><span class="sxs-lookup"><span data-stu-id="6ec58-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="6ec58-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-132">Click Add.</span></span>
19. <span data-ttu-id="6ec58-133">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="6ec58-134">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="6ec58-135">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="6ec58-136">В поле "Тип проводки" выберите "Выбытие (продажа)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="6ec58-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-137">Click Add.</span></span>
24. <span data-ttu-id="6ec58-138">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="6ec58-139">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="6ec58-140">Для параметра "Выбытие" можно ввести корр. счет или оставить это поле пустым, чтобы заполнить его для определенной проводки.</span><span class="sxs-lookup"><span data-stu-id="6ec58-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="6ec58-141">В поле "Тип проводки" выберите "Выбытие (отходы)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="6ec58-142">Для параметров "Выбытие (продажа)" и "Выбытие (отходы)" используются те же счета.</span><span class="sxs-lookup"><span data-stu-id="6ec58-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="6ec58-143">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-143">Click Add.</span></span>
28. <span data-ttu-id="6ec58-144">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="6ec58-145">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="6ec58-146">Для параметра "Выбытие" можно ввести корр. счет или оставить это поле пустым, чтобы заполнить его для определенной проводки.</span><span class="sxs-lookup"><span data-stu-id="6ec58-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="6ec58-147">Разверните раздел "Выбытие".</span><span class="sxs-lookup"><span data-stu-id="6ec58-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="6ec58-148">Необходимо настроить профили разноски выбытия как для продажи, так и для отходов.</span><span class="sxs-lookup"><span data-stu-id="6ec58-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="6ec58-149">Начнем с проводок выбытия (продажа).</span><span class="sxs-lookup"><span data-stu-id="6ec58-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="6ec58-150">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-150">Click Add.</span></span>
32. <span data-ttu-id="6ec58-151">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="6ec58-152">В поле "Сумма к разноске" выберите "Стоимость приобретения".</span><span class="sxs-lookup"><span data-stu-id="6ec58-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="6ec58-153">Стоимость приобретения будет зависеть от значений "Приобретение" и "Корректировка приобретения" для всех лет.</span><span class="sxs-lookup"><span data-stu-id="6ec58-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="6ec58-154">Можно также определить счета для этих типов проводок отдельно.</span><span class="sxs-lookup"><span data-stu-id="6ec58-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="6ec58-155">Можно настроить процесс выбытия для использования разных счетов в зависимости от того, к чему приводит выбытие: выручке или убыткам.</span><span class="sxs-lookup"><span data-stu-id="6ec58-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="6ec58-156">Зададим для параметра "Тип суммы реализации" значение "Все", чтобы использовать одни и те же счета для всех типов выбытия.</span><span class="sxs-lookup"><span data-stu-id="6ec58-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="6ec58-157">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="6ec58-158">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="6ec58-159">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-159">Click Add.</span></span>
37. <span data-ttu-id="6ec58-160">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="6ec58-161">В поле "Сумма к разноске" выберите "Амортизация (за истекшие годы)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="6ec58-162">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="6ec58-163">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="6ec58-164">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-164">Click Add.</span></span>
41. <span data-ttu-id="6ec58-165">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="6ec58-166">В поле "Сумма к разноске" выберите "Амортизация (за этот год)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="6ec58-167">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="6ec58-168">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="6ec58-169">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-169">Click Add.</span></span>
46. <span data-ttu-id="6ec58-170">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="6ec58-171">В поле "Сумма к разноске" выберите "Корректировки амортизации (за истекшие годы)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="6ec58-172">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="6ec58-173">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="6ec58-174">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-174">Click Add.</span></span>
51. <span data-ttu-id="6ec58-175">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="6ec58-176">В поле "Сумма к разноске" выберите "Корректировки амортизации (за этот год)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="6ec58-177">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="6ec58-178">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="6ec58-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-179">Click Add.</span></span>
56. <span data-ttu-id="6ec58-180">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="6ec58-181">В поле "Сумма к разноске" выберите "Остаточная стоимость".</span><span class="sxs-lookup"><span data-stu-id="6ec58-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="6ec58-182">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="6ec58-183">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="6ec58-184">В поле "Продажа или отходы" выберите "Отходы".</span><span class="sxs-lookup"><span data-stu-id="6ec58-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="6ec58-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-185">Click Add.</span></span>
62. <span data-ttu-id="6ec58-186">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="6ec58-187">В поле "Сумма к разноске" выберите "Стоимость приобретения".</span><span class="sxs-lookup"><span data-stu-id="6ec58-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="6ec58-188">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="6ec58-189">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="6ec58-190">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-190">Click Add.</span></span>
67. <span data-ttu-id="6ec58-191">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="6ec58-192">В поле "Сумма к разноске" выберите "Амортизация (за истекшие годы)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="6ec58-193">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="6ec58-194">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="6ec58-195">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-195">Click Add.</span></span>
71. <span data-ttu-id="6ec58-196">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="6ec58-197">В поле "Сумма к разноске" выберите "Амортизация (за этот год)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="6ec58-198">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="6ec58-199">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="6ec58-200">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-200">Click Add.</span></span>
76. <span data-ttu-id="6ec58-201">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="6ec58-202">В поле "Сумма к разноске" выберите "Корректировки амортизации (за истекшие годы)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="6ec58-203">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="6ec58-204">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="6ec58-205">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-205">Click Add.</span></span>
81. <span data-ttu-id="6ec58-206">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="6ec58-207">В поле "Сумма к разноске" выберите "Корректировки амортизации (за этот год)".</span><span class="sxs-lookup"><span data-stu-id="6ec58-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="6ec58-208">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="6ec58-209">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="6ec58-210">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6ec58-210">Click Add.</span></span>
86. <span data-ttu-id="6ec58-211">В поле "Книга" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6ec58-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="6ec58-212">В поле "Сумма к разноске" выберите "Остаточная стоимость".</span><span class="sxs-lookup"><span data-stu-id="6ec58-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="6ec58-213">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="6ec58-214">В поле "Корр.счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6ec58-214">In the Offset account field, specify the desired values.</span></span>


