---
title: Что нового и что изменилось в Dynamics 365 Talent - Core HR (10 сентября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462391"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="2c2c7-103">Что нового и что изменилось в Dynamics 365 Talent - Core HR (10 сентября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="2c2c7-104">**Сборка 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="2c2c7-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="2c2c7-105">В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="2c2c7-106">Возможность указания конкретного времени суток в запросах на отгулы (на половину дня)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="2c2c7-107">Если модуль "Управление отпусками и отсутствиями" настроен так, что продолжительность отгулов указывается в днях, теперь можно включить возможность указания половины дня.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="2c2c7-108">После этого при отправке запросов на отгулы пользователи могут указать, когда они хотят взять отгул — в первую половину для или во вторую.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="2c2c7-109">По умолчанию эта возможность отключена.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-109">By default, this option is turned off.</span></span> <span data-ttu-id="2c2c7-110">Чтобы сотрудники могли запрашивать отгулы в первой или второй половине дня, необходимо включить эту возможность в области **Отпуска и отсутствия** параметров управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="2c2c7-111">Привилегия безопасности, которая для этого требуется, — "Ведение параметров управления персоналом".</span><span class="sxs-lookup"><span data-stu-id="2c2c7-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="2c2c7-112">Проверка записей отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="2c2c7-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="2c2c7-113">В зависимости от того, как настроены отпуска, сотрудники, пытающиеся отправить запрос на отгул, длительность которого превышает их рабочий день, получают предупредительное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="2c2c7-114">Иными словами, система предупреждает их, когда они пытаются взять отгул продолжительностью больше целого дня на отдельно взятую дату.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="2c2c7-115">Такая проверка всегда включена.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-115">This validation is always turned on.</span></span> <span data-ttu-id="2c2c7-116">Каждый раз, сотрудники превышают заданное пороговое значение, они получают предупреждение при отправке запроса на отгул.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="2c2c7-117">Дополнительные поля для условных операторов в workflow-процессах</span><span class="sxs-lookup"><span data-stu-id="2c2c7-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="2c2c7-118">В условные операторы и заполнители для нескольких workflow-процессов в Core HR были добавлены дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="2c2c7-119">В workflow-процессы компенсации, увольнения и перемещения были добавлены следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2c2c7-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="2c2c7-120">EmploymentType (Тип трудоустройства)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-120">EmploymentType</span></span>
- <span data-ttu-id="2c2c7-121">LegalEntity (Юридическое лицо)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-121">LegalEntity</span></span>
- <span data-ttu-id="2c2c7-122">AdjustedWorkerStartDate (Скорректированная дата приема работника на работу)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="2c2c7-123">EmployerNoticeAmount (Сумма в уведомлении работодателя)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="2c2c7-124">EmployerUnitOfNotice (Подразделение для уведомления работодателя)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="2c2c7-125">TransitionDate (Дата перевода)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-125">TransitionDate</span></span>
- <span data-ttu-id="2c2c7-126">WorkerNoticeAmount (Сумма в уведомлении работника)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="2c2c7-127">WorkerStartDate (Дата приема работника на работу)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-127">WorkerStartDate</span></span>
- <span data-ttu-id="2c2c7-128">WorkerUnitOfNotice (Подразделение для уведомления работника)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="2c2c7-129">ProbationEndDate (Дата окончания испытательного срока)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-129">ProbationEndDate</span></span>
- <span data-ttu-id="2c2c7-130">Position (Занимаемая должность)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-130">Position</span></span>
- <span data-ttu-id="2c2c7-131">Union (Профсоюз)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-131">Union</span></span>
- <span data-ttu-id="2c2c7-132">Подразделение (Department)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-132">Department</span></span>
- <span data-ttu-id="2c2c7-133">PositionType (Тип должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-133">PositionType</span></span>
- <span data-ttu-id="2c2c7-134">CompLocation (Местоположение для компенсации)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-134">CompLocation</span></span>
- <span data-ttu-id="2c2c7-135">Title (Название должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-135">Title</span></span>
- <span data-ttu-id="2c2c7-136">Job (Должность)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-136">Job</span></span>
- <span data-ttu-id="2c2c7-137">JobType (Тип должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-137">JobType</span></span>
- <span data-ttu-id="2c2c7-138">JobFamily (Семейство должностей)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-138">JobFamily</span></span>
- <span data-ttu-id="2c2c7-139">JobFunction (Функциональные обязанности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-139">JobFunction</span></span>

<span data-ttu-id="2c2c7-140">В workflow-процессы должности были добавлены следующие поля:</span><span class="sxs-lookup"><span data-stu-id="2c2c7-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="2c2c7-141">Position (Занимаемая должность)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-141">Position</span></span>
- <span data-ttu-id="2c2c7-142">Union (Профсоюз)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-142">Union</span></span>
- <span data-ttu-id="2c2c7-143">Department (Подразделение)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-143">Department</span></span>
- <span data-ttu-id="2c2c7-144">PositionType (Тип должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-144">PositionType</span></span>
- <span data-ttu-id="2c2c7-145">CompLocation (Местоположение для компенсации)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-145">CompLocation</span></span>
- <span data-ttu-id="2c2c7-146">Title (Название должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-146">Title</span></span>
- <span data-ttu-id="2c2c7-147">Job (Должность)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-147">Job</span></span>
- <span data-ttu-id="2c2c7-148">JobType (Тип должности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-148">JobType</span></span>
- <span data-ttu-id="2c2c7-149">JobFamily (Семейство должностей)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-149">JobFamily</span></span>
- <span data-ttu-id="2c2c7-150">JobFunction (Функциональные обязанности)</span><span class="sxs-lookup"><span data-stu-id="2c2c7-150">JobFunction</span></span>

<span data-ttu-id="2c2c7-151">Поля в условных операторах и заполнителях доступны для всех пользователей, имеющих доступ к настройке упомянутых выше workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="2c2c7-152">Переход из Attract в управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2c2c7-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="2c2c7-153">В управлении персоналом, если модуль Attract не настроен, в разделе **Кандидаты для приема на работу** пользователям предлагается начать работу с Attract, вместо отображения сообщения "Данные для отображения не найдены".</span><span class="sxs-lookup"><span data-stu-id="2c2c7-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="2c2c7-154">Другие изменения</span><span class="sxs-lookup"><span data-stu-id="2c2c7-154">Other changes</span></span>

<span data-ttu-id="2c2c7-155">Этот выпуск содержит несколько дополнительных исправлений ошибок:</span><span class="sxs-lookup"><span data-stu-id="2c2c7-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="2c2c7-156">При найме подрядчика вкладка **Компенсация** не должна быть доступна на странице запроса/действия.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="2c2c7-157">В процессе запроса увольнения нельзя продолжить, пока все обязательные поля не будут содержать данные.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="2c2c7-158">Решены проблемы с порядком сортировки и отображения дат в аналитике управления персоналом.</span><span class="sxs-lookup"><span data-stu-id="2c2c7-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
