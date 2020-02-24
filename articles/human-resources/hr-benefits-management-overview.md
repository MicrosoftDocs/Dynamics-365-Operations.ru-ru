---
title: Обзор управления льготами
description: Обзор предварительной функции управления льготами в Dynamics 365 Human Resources. Предложите своим сотрудникам расширенные возможности с помощью простого в использовании интерактивного опыта.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029471"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="91b73-104">Обзор управления льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="91b73-105">Чтобы остаться конкурентоспособными, вам необходимо предоставить широкий набор преимуществ для привлечения и сохранения лучших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="91b73-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="91b73-106">В дополнение к стандартным преимуществам, таким как покрытие медицинских услуг и услуг стоматологии, может возникнуть необходимость предоставить расширенные услуги, такие как помощь в адаптации, программы отдыха и надбавки за одежду.</span><span class="sxs-lookup"><span data-stu-id="91b73-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="91b73-107">Предварительная функция управления льготами в Microsoft Dynamics 365 Human Resources предоставляет гибкое решение, поддерживающее разнообразные возможности использования льгот.</span><span class="sxs-lookup"><span data-stu-id="91b73-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="91b73-108">Human Resources также содержит простое в использовании взаимодействие сотрудников, демонстрирующее ваши предложения.</span><span class="sxs-lookup"><span data-stu-id="91b73-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="91b73-109">Планы расширенных льгот позволяют создавать и управлять уникальными планами льгот и поддерживают сложные таблицы нормативов льгот и вложенные уровни.</span><span class="sxs-lookup"><span data-stu-id="91b73-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="91b73-110">Можно легко создавать программы льгот, наборы и правила автоматической регистрации для более простого понимания сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="91b73-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="91b73-111">Программы для кредитования по гибкому графику позволяют выполнить оценку в поддержку выхода на пенсию и других жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="91b73-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="91b73-112">Расширенные правила допустимости позволяют сделать доступными только те из них, на которые имеют право сотрудники.</span><span class="sxs-lookup"><span data-stu-id="91b73-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="91b73-113">Возможность регистрации льгот в Интернете обеспечивает удобное для сотрудников использование.</span><span class="sxs-lookup"><span data-stu-id="91b73-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="91b73-114">Квалифицированная система обработки жизненных событий интегрирована с самообслуживанием сотрудников, а также поддерживает будущие жизненные события.</span><span class="sxs-lookup"><span data-stu-id="91b73-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="91b73-115">Если вы хотите получить доступ к демонстрационным данным, вам потребуется повторно развернуть среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="91b73-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="91b73-116">Можно предоставить прямую обратную связь или сообщать об ошибках: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="91b73-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="91b73-117">Известные проблемы управления льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="91b73-118">Обработка допустимости</span><span class="sxs-lookup"><span data-stu-id="91b73-118">Eligibility processing</span></span>

<span data-ttu-id="91b73-119">При выполнении проверки допустимости льгот, использующих сумму покрытия 1-5X зарплаты, % от зарплаты и фиксированной суммы, дата **Сведения о льготе** должна быть установлена на **Дата начала сотрудника** в **журнале занятости**.</span><span class="sxs-lookup"><span data-stu-id="91b73-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="91b73-120">Кроме того, необходимо включить **Отработанные часы**, **Частота платежей** и **Сумму зарплаты годовых льгот**.</span><span class="sxs-lookup"><span data-stu-id="91b73-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="91b73-121">Если работник имеет фиксированную компенсацию, введите **Отработанные часы** и **Частота платежей**.</span><span class="sxs-lookup"><span data-stu-id="91b73-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="91b73-122">Будет рассчитываться сумма годовой заработной платы.</span><span class="sxs-lookup"><span data-stu-id="91b73-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="91b73-123">Если сотруднику начисляется заработная плата, **Отработанные часы** вводить не нужно.</span><span class="sxs-lookup"><span data-stu-id="91b73-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="91b73-124">При создании новых работников рекомендуется сначала ввести фиксированную компенсацию.</span><span class="sxs-lookup"><span data-stu-id="91b73-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="91b73-125">Чтобы обновить запись сведений о льготе: перейдите **Работник > Журнал работника> Сведения о занятости**.</span><span class="sxs-lookup"><span data-stu-id="91b73-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="91b73-126">Скорректируйте дату на дату начала работника.</span><span class="sxs-lookup"><span data-stu-id="91b73-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="91b73-127">Самообслуживание сотрудника</span><span class="sxs-lookup"><span data-stu-id="91b73-127">Employee self-service</span></span>

<span data-ttu-id="91b73-128">Сумма сотрудника не рассчитывается при обновлении суммы покрытия для страхования жизни.</span><span class="sxs-lookup"><span data-stu-id="91b73-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="91b73-129">Например, когда сотруднику предлагается план страхования жизни, они могут выбрать 50 000 долл. США в покрытии при стоимости 0,36 долл. США на 1000 долл. США покрытия.</span><span class="sxs-lookup"><span data-stu-id="91b73-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="91b73-130">Когда сотрудник обновляет сумму покрытия, связанные затраты сотрудника остаются в нулевом виде.</span><span class="sxs-lookup"><span data-stu-id="91b73-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="91b73-131">Если план льготы разрешает только один выбор этого типа плана, пользователь получит сообщение об ошибке, если попытается отказаться от плана после выбора плана.</span><span class="sxs-lookup"><span data-stu-id="91b73-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="91b73-132">Например, пользователь выбирает медицинский план и помещает его в корзину.</span><span class="sxs-lookup"><span data-stu-id="91b73-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="91b73-133">После этого пользователь выбирает **Отказ** для другого медицинского плана.</span><span class="sxs-lookup"><span data-stu-id="91b73-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="91b73-134">При этом пользователь получит сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="91b73-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="91b73-135">Включение управления льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-135">Enable Benefits management</span></span>

<span data-ttu-id="91b73-136">Управление льготами является предварительной функцией и доступно только в средах **песочницы**.</span><span class="sxs-lookup"><span data-stu-id="91b73-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="91b73-137">В этих статьях описывается, как включить предварительный просмотр функций в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91b73-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="91b73-138">Они также сообщают, какие существующие функции в Human Resources заменяются или отключаются после включения управления льготами.</span><span class="sxs-lookup"><span data-stu-id="91b73-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="91b73-139">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="91b73-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="91b73-140">Предварительная версия функции: управление льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="91b73-141">Настройка управления льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-141">Configure Benefits management</span></span>

<span data-ttu-id="91b73-142">Прежде чем можно будет создавать планы льгот для сотрудников, необходимо настроить параметры для планов.</span><span class="sxs-lookup"><span data-stu-id="91b73-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="91b73-143">Настройка параметров управления льготами</span><span class="sxs-lookup"><span data-stu-id="91b73-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="91b73-144">Настройка правил и параметров приемлемости</span><span class="sxs-lookup"><span data-stu-id="91b73-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="91b73-145">Настройка параметров приемлемости личных контактов</span><span class="sxs-lookup"><span data-stu-id="91b73-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="91b73-146">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="91b73-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="91b73-147">Настройка периодичности платежей</span><span class="sxs-lookup"><span data-stu-id="91b73-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="91b73-148">Настройка типов событий жизненного цикла</span><span class="sxs-lookup"><span data-stu-id="91b73-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="91b73-149">Создание типов планов</span><span class="sxs-lookup"><span data-stu-id="91b73-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="91b73-150">Настройка кодов причин</span><span class="sxs-lookup"><span data-stu-id="91b73-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="91b73-151">Настройка кодов уровней</span><span class="sxs-lookup"><span data-stu-id="91b73-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="91b73-152">Настройка ставок</span><span class="sxs-lookup"><span data-stu-id="91b73-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="91b73-153">Настройка вычетов</span><span class="sxs-lookup"><span data-stu-id="91b73-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="91b73-154">Настройка дней ожидания</span><span class="sxs-lookup"><span data-stu-id="91b73-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="91b73-155">Настройка периодов ожидания</span><span class="sxs-lookup"><span data-stu-id="91b73-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="91b73-156">Настройка правил округления</span><span class="sxs-lookup"><span data-stu-id="91b73-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="91b73-157">Создание категорий занятости</span><span class="sxs-lookup"><span data-stu-id="91b73-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="91b73-158">Настройка типов занятости</span><span class="sxs-lookup"><span data-stu-id="91b73-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="91b73-159">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="91b73-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="91b73-160">Создание планов льгот</span><span class="sxs-lookup"><span data-stu-id="91b73-160">Create benefit plans</span></span>

<span data-ttu-id="91b73-161">В этих статьях показано, как создавать планы льгот, в том числе комплекты и программы по гибкой кредитной линии.</span><span class="sxs-lookup"><span data-stu-id="91b73-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="91b73-162">Настройка планов льгот</span><span class="sxs-lookup"><span data-stu-id="91b73-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="91b73-163">Создание планов льгот работников</span><span class="sxs-lookup"><span data-stu-id="91b73-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="91b73-164">Настройка гибких программ кредитования</span><span class="sxs-lookup"><span data-stu-id="91b73-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="91b73-165">Настройка событий будущего</span><span class="sxs-lookup"><span data-stu-id="91b73-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="91b73-166">Обработка планов льгот</span><span class="sxs-lookup"><span data-stu-id="91b73-166">Process benefit plans</span></span>

<span data-ttu-id="91b73-167">Необходимо обработать некоторые изменения, чтобы сделать их активными.</span><span class="sxs-lookup"><span data-stu-id="91b73-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="91b73-168">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="91b73-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="91b73-169">Обработка событий в жизни</span><span class="sxs-lookup"><span data-stu-id="91b73-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="91b73-170">Обработка изменений в жизни</span><span class="sxs-lookup"><span data-stu-id="91b73-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="91b73-171">Обработка приемлемости событий в жизни</span><span class="sxs-lookup"><span data-stu-id="91b73-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="91b73-172">Обработка изменений ставок</span><span class="sxs-lookup"><span data-stu-id="91b73-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

