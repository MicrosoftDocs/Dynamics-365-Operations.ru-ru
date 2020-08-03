---
title: Что нового и что изменилось в Dynamics 365 Human Resources (25 февраля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e5bc232bef257e757086d37d56b0f68b80114749
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555083"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="7f7ee-103">Что нового и что изменилось в Dynamics 365 Human Resources (25 февраля 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

<span data-ttu-id="7f7ee-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7f7ee-105">Изменения применяются для номера сборки 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="7f7ee-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="7f7ee-107">Включение навигации по управлению обращениями и объекта платформы управления данными (DMF) (414754)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="7f7ee-108">Эта предварительная версия функции обеспечивает дополнительную навигацию к вариантам управления обращениями.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="7f7ee-109">Эту предварительную версию функции можно включить в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="7f7ee-110">Эти пункты меню отображаются в рабочей области **Соответствие** Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7f7ee-111">Благодаря этому изменению Human Resources может получить доступ к:</span><span class="sxs-lookup"><span data-stu-id="7f7ee-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="7f7ee-112">Все обращения</span><span class="sxs-lookup"><span data-stu-id="7f7ee-112">All cases</span></span>
- <span data-ttu-id="7f7ee-113">Мои обращения</span><span class="sxs-lookup"><span data-stu-id="7f7ee-113">My cases</span></span>
- <span data-ttu-id="7f7ee-114">Мои открытые обращения</span><span class="sxs-lookup"><span data-stu-id="7f7ee-114">My open cases</span></span>
- <span data-ttu-id="7f7ee-115">Мои просроченные обращения</span><span class="sxs-lookup"><span data-stu-id="7f7ee-115">My overdue cases</span></span>
- <span data-ttu-id="7f7ee-116">Обращения, назначенные мне через рабочий процесс</span><span class="sxs-lookup"><span data-stu-id="7f7ee-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="7f7ee-117">Вместе с этими новыми представлениями обращений также доступен объект DMF **Сведения об обращении**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="7f7ee-118">Включение определений отношений в глобальном адресной книге (414762)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="7f7ee-119">Отношения теперь включены в глобальной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="7f7ee-120">До выпуска этой недели информационное поле **Отношения** отображало все определяемые системой отношения.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="7f7ee-121">Теперь можно определить эти отношения на странице глобальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="7f7ee-122">Должность может быть удалена при наличии активных записей компенсаций для данной должности (414568)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="7f7ee-123">При этом изменении появляется предупреждение при попытке удалить должность, когда работник имеет активную запись компенсации для этой должности.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="7f7ee-124">Когда это происходит, необходимо обновить запись о фиксированной компенсации для сотрудника перед удалением должности.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="7f7ee-125">Рабочий процесс проверки производительности иногда добавляет утверждения от лиц, не являющихся частью процесса (414171)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="7f7ee-126">Это изменение устраняет проблему, в которой в обзор производительности добавляются дополнительные участники утверждения.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="7f7ee-127">Назначение должности сотрудника не создается в Common Data Service при выборе в диалоговом окне нового работника (413479)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-127">Worker position assignment not created in Common Data Service when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="7f7ee-128">Это изменение исправляет проблему при найме нового сотрудника и назначении нового сотрудника на должность через диалоговое окно **Новый сотрудник**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="7f7ee-129">Теперь назначение должности отражается в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-129">Now the position assignment is reflected in Common Data Service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="7f7ee-130">Скоро</span><span class="sxs-lookup"><span data-stu-id="7f7ee-130">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="7f7ee-131">Обновленное решение Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7f7ee-131">Updated Common Data Service solution</span></span>

<span data-ttu-id="7f7ee-132">Новое решение Common Data Service будет доступно в ближайшее время со следующими изменениями:</span><span class="sxs-lookup"><span data-stu-id="7f7ee-132">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="7f7ee-133">Описание</span><span class="sxs-lookup"><span data-stu-id="7f7ee-133">Description</span></span> | <span data-ttu-id="7f7ee-134">Изменение</span><span class="sxs-lookup"><span data-stu-id="7f7ee-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="7f7ee-135">Изменение объекта **Работа/должность**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="7f7ee-136">Добавлено **Регион компенсации**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-136">**Compensation region** added</span></span></br><span data-ttu-id="7f7ee-137">Добавлено **Финансовые аналитики**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="7f7ee-138">Изменения объекта **Работник**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-138">**Worker** entity changes</span></span> | <span data-ttu-id="7f7ee-139">Добавлено **Последовательность имени**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-139">**Name sequence** added</span></span></br><span data-ttu-id="7f7ee-140">Добавлено **Работа из дома**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-140">**Works from home** added</span></span></br><span data-ttu-id="7f7ee-141">Добавлено **Язык**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-141">**Language** added</span></span></br><span data-ttu-id="7f7ee-142">Добавлено **Дата начала стажа**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-142">**Seniority date** added</span></span></br><span data-ttu-id="7f7ee-143">Добавлено **Дата юбилея**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-143">**Anniversary date** added</span></span></br><span data-ttu-id="7f7ee-144">Добавлено **Дата первоначального приема на работу**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-144">**Original hire date** added</span></span> |
| <span data-ttu-id="7f7ee-145">Изменения объекта **Занятость**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-145">**Employment** entity changes</span></span> | <span data-ttu-id="7f7ee-146">Добавлено **Финансовые аналитики**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-146">**Financial dimensions** added</span></span></br><span data-ttu-id="7f7ee-147">Добавлено **Причина увольнения**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-147">**Termination reason** added</span></span></br><span data-ttu-id="7f7ee-148">**Дата увольнения** переименовано на **Дата передачи**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="7f7ee-149">Добавлено **Дата испытательного срока**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-149">**Probation date** added</span></span> |
| <span data-ttu-id="7f7ee-150">Изменения объекта **Адрес работника**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-150">**Worker address** entity changes</span></span> | <span data-ttu-id="7f7ee-151">Добавлен **Адрес улицы**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-151">**Street address** added</span></span></br><span data-ttu-id="7f7ee-152">**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания</span><span class="sxs-lookup"><span data-stu-id="7f7ee-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="7f7ee-153">Новые объекты настройки переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="7f7ee-153">New variable compensation setup entities</span></span> | <span data-ttu-id="7f7ee-154">**Тип плана переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="7f7ee-155">**План переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-155">**Compensation variable plan**</span></span></br><span data-ttu-id="7f7ee-156">**Положения о передаче прав на льготы**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-156">**Vesting rules**</span></span></br><span data-ttu-id="7f7ee-157">**Уровень плана переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="7f7ee-158">Новый объект **Занятость по календарю работников**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="7f7ee-159">Добавлено **Объект рабочего календаря**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="7f7ee-160">Новый объект **Сведения о позиции зарплаты**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="7f7ee-161">Добавлено **Сведения о позиции зарплаты**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="7f7ee-162">Новый объект **Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-162">New **Title** entity</span></span> | <span data-ttu-id="7f7ee-163">Добавлено **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-163">**Title** added.</span></span> <span data-ttu-id="7f7ee-164">Новый объект **Заголовок** будет включен в процесс синхронизации между Управление персоналом и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-164">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="7f7ee-165">Она не должна быть изначально указана в объектах **Позиция** или **Должность**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="7f7ee-166">В течение следующих нескольких недель эти изменения объекта будут доступны во всех средах.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="7f7ee-167">Чтобы вручную установить последнюю версию решения Common Data Service для модуля Human Resources:</span><span class="sxs-lookup"><span data-stu-id="7f7ee-167">To manually install the latest Common Data Service solution for Human Resources:</span></span>

1.  <span data-ttu-id="7f7ee-168">Перейдите к [Центру администрирования Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7f7ee-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="7f7ee-169">Выберите **Среды**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="7f7ee-170">Найдите среду, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="7f7ee-171">Это должно соответствовать значению **Имя среды** в разделе **Сведения Common Data Service** в форме **Сведения** в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="7f7ee-172">Выберите среду, чтобы просмотреть сведения о среде.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="7f7ee-173">В верхней части на панели действий выберите **Управление решениями**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="7f7ee-174">Откроется новое окно браузера; перейдите в **центр администрирования Dynamics 365** в контексте вашей среды.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="7f7ee-175">В списке **Решение** выберите **Привязка Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="7f7ee-176">Выберите **Обновить** для применения последнего решения.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7f7ee-177">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="7f7ee-177">In preview</span></span>

<span data-ttu-id="7f7ee-178">Следующие функции предварительного просмотра станут доступны 3 февраля 2020 г.:</span><span class="sxs-lookup"><span data-stu-id="7f7ee-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="7f7ee-179">**Предварительные функции отпуска и отсутствия** — Дополнительные сведения см. в [Предварительные функции отпуска и отсутствия](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="7f7ee-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="7f7ee-180">**Функция предварительного просмотра управления льготами** — дополнительные сведения, включая известные проблемы, см. в разделе [Обзор управления преимуществами](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7f7ee-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7f7ee-181">См. также</span><span class="sxs-lookup"><span data-stu-id="7f7ee-181">See also</span></span>

[<span data-ttu-id="7f7ee-182">Что нового и что изменилось в Human Resources</span><span class="sxs-lookup"><span data-stu-id="7f7ee-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7f7ee-183">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="7f7ee-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7f7ee-184">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="7f7ee-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7f7ee-185">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="7f7ee-185">Manage features</span></span>](hr-admin-manage-features.md)