---
title: Что нового и что изменилось в Dynamics 365 Human Resources (18 февраля 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60b46f5bd8f5eeae8aedc9bf81f1e7892caa0c93
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555347"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="ae17b-103">Что нового и что изменилось в Dynamics 365 Human Resources (18 февраля 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="ae17b-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="ae17b-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae17b-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ae17b-105">Изменения применяются для номера сборки 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="ae17b-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="ae17b-106">Числа в скобках в некоторых заголовках относятся к номерам LCS для справки.</span><span class="sxs-lookup"><span data-stu-id="ae17b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="ae17b-107">Обновление платформы update 32</span><span class="sxs-lookup"><span data-stu-id="ae17b-107">Platform update 32</span></span> 

<span data-ttu-id="ae17b-108">Доступно обновление платформы 32.</span><span class="sxs-lookup"><span data-stu-id="ae17b-108">Platform update 32 is now available.</span></span> <span data-ttu-id="ae17b-109">Для получения дополнительных сведений см. раздел [Что нового и что изменилось в обновлении платформы 32 для Finance and Operations (февраль 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="ae17b-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="ae17b-110">Значения поиска запоминаются при изменении параметров просмотра в упрощенной форме сотрудника (383833)</span><span class="sxs-lookup"><span data-stu-id="ae17b-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="ae17b-111">Новая форма **Работник** теперь запоминает значения поиска при изменении параметров просмотра и применении изменений.</span><span class="sxs-lookup"><span data-stu-id="ae17b-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="ae17b-112">Сводные плитки управления компенсациями в функции предварительного просмотра перенаправляют в неправильную форму (401861)</span><span class="sxs-lookup"><span data-stu-id="ae17b-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="ae17b-113">Плитки управления фиксированной и переменной компенсацией теперь отображают правильные записи в новой форме **Работник**.</span><span class="sxs-lookup"><span data-stu-id="ae17b-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="ae17b-114">Применяется только к функции предварительного просмотра упрощенной формы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ae17b-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="ae17b-115">Эту функцию предварительного просмотра можно включить в **управлении функциями**.</span><span class="sxs-lookup"><span data-stu-id="ae17b-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="ae17b-116">Дополнительные сведения см. в разделе [Управление функциями](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="ae17b-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="ae17b-117">Пустое поле статуса для некоторых записей запроса отпуска в Common Data Service (414915)</span><span class="sxs-lookup"><span data-stu-id="ae17b-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="ae17b-118">Это изменение исправляет проблему с Common Data Service, когда поле **Статус** в запросе отпуска установлено на **Просмотреть**.</span><span class="sxs-lookup"><span data-stu-id="ae17b-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="ae17b-119">Common Data Service теперь отображает статус.</span><span class="sxs-lookup"><span data-stu-id="ae17b-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="ae17b-120">Анализ несоответствия навыков возможен для назначенного задания (411390)</span><span class="sxs-lookup"><span data-stu-id="ae17b-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="ae17b-121">Теперь можно выполнить анализ несоответствия навыков для любого задания, определенного в Управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="ae17b-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="ae17b-122">Системная валюта не синхронизируется из Common Data Service с Управление персоналом в новых средах (418011)</span><span class="sxs-lookup"><span data-stu-id="ae17b-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="ae17b-123">Системная валюта в Common Data Service теперь может синхронизироваться с Управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="ae17b-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ae17b-124">В режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="ae17b-124">In preview</span></span>

- [<span data-ttu-id="ae17b-125">Предварительные функции отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="ae17b-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="ae17b-126">Предварительная версия управления льготами</span><span class="sxs-lookup"><span data-stu-id="ae17b-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="ae17b-127">Скоро</span><span class="sxs-lookup"><span data-stu-id="ae17b-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="ae17b-128">Обновленное решение Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ae17b-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="ae17b-129">Новое решение Common Data Service будет доступно в ближайшее время со следующими изменениями:</span><span class="sxs-lookup"><span data-stu-id="ae17b-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="ae17b-130">Описание</span><span class="sxs-lookup"><span data-stu-id="ae17b-130">Description</span></span> | <span data-ttu-id="ae17b-131">Изменение</span><span class="sxs-lookup"><span data-stu-id="ae17b-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="ae17b-132">Изменение объекта **Работа/должность**</span><span class="sxs-lookup"><span data-stu-id="ae17b-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="ae17b-133">Добавлено **Регион компенсации**</span><span class="sxs-lookup"><span data-stu-id="ae17b-133">**Compensation region** added</span></span></br><span data-ttu-id="ae17b-134">Добавлено **Финансовые аналитики**</span><span class="sxs-lookup"><span data-stu-id="ae17b-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="ae17b-135">Изменения объекта **Работник**</span><span class="sxs-lookup"><span data-stu-id="ae17b-135">**Worker** entity changes</span></span> | <span data-ttu-id="ae17b-136">Добавлено **Последовательность имени**</span><span class="sxs-lookup"><span data-stu-id="ae17b-136">**Name sequence** added</span></span></br><span data-ttu-id="ae17b-137">Добавлено **Работа из дома**</span><span class="sxs-lookup"><span data-stu-id="ae17b-137">**Works from home** added</span></span></br><span data-ttu-id="ae17b-138">Добавлено **Язык**</span><span class="sxs-lookup"><span data-stu-id="ae17b-138">**Language** added</span></span></br><span data-ttu-id="ae17b-139">Добавлено **Дата начала стажа**</span><span class="sxs-lookup"><span data-stu-id="ae17b-139">**Seniority date** added</span></span></br><span data-ttu-id="ae17b-140">Добавлено **Дата юбилея**</span><span class="sxs-lookup"><span data-stu-id="ae17b-140">**Anniversary date** added</span></span></br><span data-ttu-id="ae17b-141">Добавлено **Дата первоначального приема на работу**</span><span class="sxs-lookup"><span data-stu-id="ae17b-141">**Original hire date** added</span></span> |
| <span data-ttu-id="ae17b-142">Изменения объекта **Занятость**</span><span class="sxs-lookup"><span data-stu-id="ae17b-142">**Employment** entity changes</span></span> | <span data-ttu-id="ae17b-143">Добавлено **Финансовые аналитики**</span><span class="sxs-lookup"><span data-stu-id="ae17b-143">**Financial dimensions** added</span></span></br><span data-ttu-id="ae17b-144">Добавлено **Причина увольнения**</span><span class="sxs-lookup"><span data-stu-id="ae17b-144">**Termination reason** added</span></span></br><span data-ttu-id="ae17b-145">**Дата увольнения** переименовано на **Дата передачи**</span><span class="sxs-lookup"><span data-stu-id="ae17b-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="ae17b-146">Добавлено **Дата испытательного срока**</span><span class="sxs-lookup"><span data-stu-id="ae17b-146">**Probation date** added</span></span> |
| <span data-ttu-id="ae17b-147">Изменения объекта **Адрес работника**</span><span class="sxs-lookup"><span data-stu-id="ae17b-147">**Worker address** entity changes</span></span> | <span data-ttu-id="ae17b-148">Добавлен **Адрес улицы**</span><span class="sxs-lookup"><span data-stu-id="ae17b-148">**Street address** added</span></span></br><span data-ttu-id="ae17b-149">**Строка адреса 1**, **Строка адреса 2** и **Строка адреса 3** отмечены для устаревания</span><span class="sxs-lookup"><span data-stu-id="ae17b-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="ae17b-150">Новые объекты настройки переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="ae17b-150">New variable compensation setup entities</span></span> | <span data-ttu-id="ae17b-151">**Тип плана переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="ae17b-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="ae17b-152">**План переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="ae17b-152">**Compensation variable plan**</span></span></br><span data-ttu-id="ae17b-153">**Положения о передаче прав на льготы**</span><span class="sxs-lookup"><span data-stu-id="ae17b-153">**Vesting rules**</span></span></br><span data-ttu-id="ae17b-154">**Уровень плана переменной компенсации**</span><span class="sxs-lookup"><span data-stu-id="ae17b-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="ae17b-155">Новый объект **Занятость по календарю работников**</span><span class="sxs-lookup"><span data-stu-id="ae17b-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="ae17b-156">Добавлено **Объект рабочего календаря**</span><span class="sxs-lookup"><span data-stu-id="ae17b-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="ae17b-157">Новый объект **Сведения о позиции зарплаты**</span><span class="sxs-lookup"><span data-stu-id="ae17b-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="ae17b-158">Добавлено **Сведения о позиции зарплаты**</span><span class="sxs-lookup"><span data-stu-id="ae17b-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="ae17b-159">Новый объект **Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ae17b-159">New **Title** entity</span></span> | <span data-ttu-id="ae17b-160">Добавлено **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="ae17b-160">**Title** added.</span></span> <span data-ttu-id="ae17b-161">Новый объект **Заголовок** будет включен в процесс синхронизации между Управление персоналом и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ae17b-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="ae17b-162">Она не должна быть изначально указана в объектах **Позиция** или **Должность**.</span><span class="sxs-lookup"><span data-stu-id="ae17b-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae17b-163">См. также</span><span class="sxs-lookup"><span data-stu-id="ae17b-163">See also</span></span>

[<span data-ttu-id="ae17b-164">Что нового и что изменилось в Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="ae17b-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ae17b-165">Обзор выпуска Dynamics 365 Human Resources 2019, волна 2</span><span class="sxs-lookup"><span data-stu-id="ae17b-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ae17b-166">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="ae17b-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ae17b-167">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="ae17b-167">Manage features</span></span>](hr-admin-manage-features.md)