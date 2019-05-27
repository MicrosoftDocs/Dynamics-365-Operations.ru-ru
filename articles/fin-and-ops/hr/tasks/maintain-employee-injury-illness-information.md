---
title: Ведение сведений о травмах и заболеваниях сотрудников
description: Рекомендуется сначала выполнить задание "Настройка травм и заболеваний", поскольку здесь используются некоторые сведения о настройке.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7324a1ce08bfe07a7ef96f4a733ebd44cd392ba6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510413"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="f036f-103">Ведение сведений о травмах и заболеваниях сотрудников</span><span class="sxs-lookup"><span data-stu-id="f036f-103">Maintain employee injury and illness information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f036f-104">Рекомендуется сначала выполнить задание "Настройка травм и заболеваний", поскольку здесь используются некоторые сведения о настройке.</span><span class="sxs-lookup"><span data-stu-id="f036f-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="f036f-105">Эта запись задачи охватывает основные шаги по созданию инцидентов травм или заболеваний.</span><span class="sxs-lookup"><span data-stu-id="f036f-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="f036f-106">Кроме отслеживания сведений о травме или заболевании, отслеживается также статус обращения.</span><span class="sxs-lookup"><span data-stu-id="f036f-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="f036f-107">По умолчанию обращения имеет статус "Открыто".</span><span class="sxs-lookup"><span data-stu-id="f036f-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="f036f-108">Статусами можно управлять из меню "Статус обращения" на панели приложения в верхней части формы.</span><span class="sxs-lookup"><span data-stu-id="f036f-108">The statuses can be managed from the 'Case status' menu item in the application bar at the top of the form.</span></span>

1. <span data-ttu-id="f036f-109">Перейдите в раздел "Управление персоналом" > "Работники" > "Травмы и заболевания" > "Случаи травм и заболеваний".</span><span class="sxs-lookup"><span data-stu-id="f036f-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="f036f-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f036f-110">Click New.</span></span>
3. <span data-ttu-id="f036f-111">В поле "Описание обращения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="f036f-112">Пример: травма запястья</span><span class="sxs-lookup"><span data-stu-id="f036f-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="f036f-113">В поле "Работник" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-114">Пример: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="f036f-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="f036f-115">В поле "Дата и время случая" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="f036f-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="f036f-116">Пример: 20.01.2016 10:00</span><span class="sxs-lookup"><span data-stu-id="f036f-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="f036f-117">В поле "Тип травмы или заболевания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-118">Пример: перелом</span><span class="sxs-lookup"><span data-stu-id="f036f-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="f036f-119">В поле "Часть тела" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-120">Пример: запястье</span><span class="sxs-lookup"><span data-stu-id="f036f-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="f036f-121">В поле "Тип исхода" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-122">Пример: терапия</span><span class="sxs-lookup"><span data-stu-id="f036f-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="f036f-123">В поле "Дата и время указаны" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="f036f-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="f036f-124">Указанные дата и время должны быть позднее, чем дата и время инцидента.</span><span class="sxs-lookup"><span data-stu-id="f036f-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="f036f-125">В поле "Лицо, подавшее обращение" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-126">Это может быть сотрудник или другой свидетель инцидента.</span><span class="sxs-lookup"><span data-stu-id="f036f-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="f036f-127">Пример: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="f036f-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="f036f-128">Разверните раздел "Случай".</span><span class="sxs-lookup"><span data-stu-id="f036f-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="f036f-129">В поле "Место, где произошел инцидент" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="f036f-130">Пример: склад</span><span class="sxs-lookup"><span data-stu-id="f036f-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="f036f-131">Выберите значение "Да" в поле "В рабочих помещениях".</span><span class="sxs-lookup"><span data-stu-id="f036f-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="f036f-132">Если инцидент произошел в рабочих помещениях, выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="f036f-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="f036f-133">В поле "Дата и время начала работы" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="f036f-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="f036f-134">Введите дату и время, когда участник инцидента начал работать, до времени инцидента.</span><span class="sxs-lookup"><span data-stu-id="f036f-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="f036f-135">В поле "Задание или задача сотрудника" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="f036f-136">Введите задание или задачу, которую сотрудник выполнял, когда произошел инцидент.</span><span class="sxs-lookup"><span data-stu-id="f036f-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="f036f-137">Пример: погрузка ящиков</span><span class="sxs-lookup"><span data-stu-id="f036f-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="f036f-138">В поле "Причина случая" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="f036f-139">Введите причину инцидента.</span><span class="sxs-lookup"><span data-stu-id="f036f-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="f036f-140">Пример: поскользнулся на влажном полу</span><span class="sxs-lookup"><span data-stu-id="f036f-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="f036f-141">В поле "Уровень серьезности" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="f036f-142">В поле "Предпринимаемое действие" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="f036f-143">Пример: вовремя убирать пролитую жидкость</span><span class="sxs-lookup"><span data-stu-id="f036f-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="f036f-144">В поле "Ожидаемые дни нетрудоспособности" введите число.</span><span class="sxs-lookup"><span data-stu-id="f036f-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="f036f-145">Введите ожидаемое количество дней, в течение которых лицо не сможет работать.</span><span class="sxs-lookup"><span data-stu-id="f036f-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="f036f-146">Как только лицо возвращается к работе, внесите в поле "Дней невыхода на работу" фактическое количество дней, когда сотрудник не работал.</span><span class="sxs-lookup"><span data-stu-id="f036f-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="f036f-147">Разверните раздел "Затраты по травме или заболеванию".</span><span class="sxs-lookup"><span data-stu-id="f036f-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="f036f-148">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f036f-148">Click Add.</span></span>
22. <span data-ttu-id="f036f-149">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="f036f-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="f036f-150">В поле "Тип затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-151">Пример:  "Лечение".    Можно также указать сумму и прикрепить подтверждающую документацию, например счета от врача или врачебную выписку.</span><span class="sxs-lookup"><span data-stu-id="f036f-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="f036f-152">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f036f-152">Click Add.</span></span>
25. <span data-ttu-id="f036f-153">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="f036f-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="f036f-154">В поле "Тип затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-155">Пример: Врач</span><span class="sxs-lookup"><span data-stu-id="f036f-155">Example: Doctor</span></span>  
27. <span data-ttu-id="f036f-156">Разверните раздел "Лечение травм и заболеваний".</span><span class="sxs-lookup"><span data-stu-id="f036f-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="f036f-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="f036f-157">Click Add.</span></span>
29. <span data-ttu-id="f036f-158">В поле "Дата лечения" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="f036f-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="f036f-159">В поле "Тип лечения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="f036f-160">Пример: шина</span><span class="sxs-lookup"><span data-stu-id="f036f-160">Example:  Splint</span></span>  
31. <span data-ttu-id="f036f-161">При необходимости установите для поля "Посещение больницы скорой помощи" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="f036f-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="f036f-162">В поле "Комментарии к лечению" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="f036f-163">Пример: лонгет на 2 недели</span><span class="sxs-lookup"><span data-stu-id="f036f-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="f036f-164">В поле "Имя врача" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="f036f-165">Пример: доктор Иванов</span><span class="sxs-lookup"><span data-stu-id="f036f-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="f036f-166">В поле "Медицинское учреждение и его расположение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="f036f-167">Пример: станция скорой помощи №333</span><span class="sxs-lookup"><span data-stu-id="f036f-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="f036f-168">В поле "Сведения о лечении" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f036f-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="f036f-169">Пример: рентгеновский снимок подтверждает перелом, носить лонгету</span><span class="sxs-lookup"><span data-stu-id="f036f-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="f036f-170">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f036f-170">Click Save.</span></span>
    * <span data-ttu-id="f036f-171">Статус инцидента можно изменить в любое время.</span><span class="sxs-lookup"><span data-stu-id="f036f-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="f036f-172">Установите для инцидента статус "В работе", если выполняется обработка травмы или заболевания.</span><span class="sxs-lookup"><span data-stu-id="f036f-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="f036f-173">После закрытия инцидента можно только добавлять или удалять затраты, лечение или отчеты, связанные с инцидентом.</span><span class="sxs-lookup"><span data-stu-id="f036f-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="f036f-174">Чтобы изменить другую информацию, повторное откройте инцидент.</span><span class="sxs-lookup"><span data-stu-id="f036f-174">To modify other information, reopen the case.</span></span>  

