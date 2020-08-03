---
title: Обзор управления льготами
description: Обзор функции управления льготами в Dynamics 365 Human Resources. Предложите своим сотрудникам расширенные возможности с помощью простого в использовании интерактивного опыта.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1043fb18c33e5ec0cde13008b168fd317c7c7be6
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599388"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="9afb3-104">Обзор управления льготами</span><span class="sxs-lookup"><span data-stu-id="9afb3-104">Benefits management overview</span></span>

<span data-ttu-id="9afb3-105">Чтобы остаться конкурентоспособными, вам необходимо предоставить широкий набор преимуществ для привлечения и сохранения лучших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="9afb3-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="9afb3-106">В дополнение к стандартным преимуществам, таким как покрытие медицинских услуг и услуг стоматологии, может возникнуть необходимость предоставить расширенные услуги, такие как помощь в адаптации, программы отдыха и надбавки за одежду.</span><span class="sxs-lookup"><span data-stu-id="9afb3-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="9afb3-107">Управление льготами в Microsoft Dynamics 365 Human Resources предоставляет гибкое решение, поддерживающее разнообразные возможности использования льгот.</span><span class="sxs-lookup"><span data-stu-id="9afb3-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="9afb3-108">Human Resources также содержит простое в использовании взаимодействие сотрудников, демонстрирующее ваши предложения.</span><span class="sxs-lookup"><span data-stu-id="9afb3-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="9afb3-109">Планы расширенных льгот позволяют создавать и управлять уникальными планами льгот и поддерживают сложные таблицы нормативов льгот и вложенные уровни.</span><span class="sxs-lookup"><span data-stu-id="9afb3-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="9afb3-110">Можно легко создавать программы льгот, наборы и правила автоматической регистрации для более простого понимания сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="9afb3-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="9afb3-111">Программы для кредитования по гибкому графику позволяют выполнить оценку в поддержку выхода на пенсию и других жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="9afb3-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="9afb3-112">Расширенные правила допустимости позволяют сделать доступными только те из них, на которые имеют право сотрудники.</span><span class="sxs-lookup"><span data-stu-id="9afb3-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="9afb3-113">Возможность регистрации льгот в Интернете обеспечивает удобное для сотрудников использование.</span><span class="sxs-lookup"><span data-stu-id="9afb3-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="9afb3-114">Квалифицированная обработка событий жизненного цикла поддерживает будущие события жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="9afb3-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="9afb3-115">Если вы хотите получить доступ к демонстрационным данным, вам потребуется повторно развернуть среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="9afb3-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="9afb3-116">Известные проблемы управления льготами</span><span class="sxs-lookup"><span data-stu-id="9afb3-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="9afb3-117">Программы Flex Credit</span><span class="sxs-lookup"><span data-stu-id="9afb3-117">Flex credit programs</span></span>

<span data-ttu-id="9afb3-118">Общая сумма кредита, определенная для гибкой кредитной программы, не отображается в форме **Планы льгот работников**.</span><span class="sxs-lookup"><span data-stu-id="9afb3-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="9afb3-119">Кроме того, если для гибкой кредитной программы задано пропорциональное правило **Нет**, при выборе и подтверждении планов будет выводится сообщение об ошибке в форме **План льгот работника**.</span><span class="sxs-lookup"><span data-stu-id="9afb3-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="9afb3-120">Включение управления льготами</span><span class="sxs-lookup"><span data-stu-id="9afb3-120">Enable Benefits management</span></span>

<span data-ttu-id="9afb3-121">В этой статье описывается, как включить функции в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9afb3-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="9afb3-122">Она также сообщает, какие существующие функции в Human Resources заменяются или отключаются после включения управления льготами.</span><span class="sxs-lookup"><span data-stu-id="9afb3-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9afb3-123">После включения управления льготами в **Производственной** среде его нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="9afb3-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="9afb3-124">Рекомендуется включить и проверить управление льготами в среде **Песочница** перед ее включением в **Производственной** среде.</span><span class="sxs-lookup"><span data-stu-id="9afb3-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="9afb3-125">Существуют значительные различия между устаревшими функциональными возможностями льгот и новой функциональностью управления льготами, которые требуют дополнительной настройки и должны быть протестированы перед тем, как они будут помещены в производство.</span><span class="sxs-lookup"><span data-stu-id="9afb3-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="9afb3-126">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="9afb3-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="9afb3-127">Настройка сведений о сотрудниках</span><span class="sxs-lookup"><span data-stu-id="9afb3-127">Configure employee information</span></span>

<span data-ttu-id="9afb3-128">Перед регистрацией сотрудников для получения льгот необходимо ввести требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="9afb3-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="9afb3-129">Необходимо зарегистрировать сотрудника в пункте **План фиксированной компенсации** на начальной дате, а также необходимо выбрать значение **Частота оплаты льгот** в пункт **Сведения о занятости** в форме **Работник**.</span><span class="sxs-lookup"><span data-stu-id="9afb3-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="9afb3-130">Если имеется сотрудник, который получает дополнительную компенсацию, такую как комиссионные, можно добавить сумму **Годовая зарплата льгот** из записи сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9afb3-130">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="9afb3-131">Модуль Human Resources использует сумму **Годовая зарплата льгот** при определении сумм покрытия вместо годовой суммы по фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="9afb3-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="9afb3-132">**Годовая зарплата льгот** должна быть действительна по состоянию на дату начала сотрудника или начало периода льготы, в зависимости от того, что является самым последним.</span><span class="sxs-lookup"><span data-stu-id="9afb3-132">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="9afb3-133">Если для сотрудника записывается и фиксированная компенсация, и сумма годовой зарплаты льгот, годовая зарплата льгот будет использоваться для определения сумм покрытия.</span><span class="sxs-lookup"><span data-stu-id="9afb3-133">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="9afb3-134">При создании плана льгот, в котором используются ставки на основе пола или возраста, необходимо ввести дату рождения и пол для сотрудника, чтобы рассчитать стоимость льготы.</span><span class="sxs-lookup"><span data-stu-id="9afb3-134">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="9afb3-135">Настройка управления льготами</span><span class="sxs-lookup"><span data-stu-id="9afb3-135">Configure Benefits management</span></span>

<span data-ttu-id="9afb3-136">Прежде чем можно будет создавать планы льгот для сотрудников, необходимо настроить параметры для планов.</span><span class="sxs-lookup"><span data-stu-id="9afb3-136">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="9afb3-137">Настройка параметров управления льготами</span><span class="sxs-lookup"><span data-stu-id="9afb3-137">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="9afb3-138">Настройка правил и параметров приемлемости</span><span class="sxs-lookup"><span data-stu-id="9afb3-138">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="9afb3-139">Настройка параметров приемлемости личных контактов</span><span class="sxs-lookup"><span data-stu-id="9afb3-139">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="9afb3-140">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="9afb3-140">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="9afb3-141">Настройка периодичности платежей</span><span class="sxs-lookup"><span data-stu-id="9afb3-141">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="9afb3-142">Настройка типов событий жизненного цикла</span><span class="sxs-lookup"><span data-stu-id="9afb3-142">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="9afb3-143">Создание типов планов</span><span class="sxs-lookup"><span data-stu-id="9afb3-143">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="9afb3-144">Настройка кодов причин</span><span class="sxs-lookup"><span data-stu-id="9afb3-144">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="9afb3-145">Настройка кодов уровней</span><span class="sxs-lookup"><span data-stu-id="9afb3-145">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="9afb3-146">Настройка ставок</span><span class="sxs-lookup"><span data-stu-id="9afb3-146">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="9afb3-147">Настройка вычетов</span><span class="sxs-lookup"><span data-stu-id="9afb3-147">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="9afb3-148">Настройка дней ожидания</span><span class="sxs-lookup"><span data-stu-id="9afb3-148">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="9afb3-149">Настройка периодов ожидания</span><span class="sxs-lookup"><span data-stu-id="9afb3-149">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="9afb3-150">Настройка правил округления</span><span class="sxs-lookup"><span data-stu-id="9afb3-150">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="9afb3-151">Создание категорий занятости</span><span class="sxs-lookup"><span data-stu-id="9afb3-151">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="9afb3-152">Настройка типов занятости</span><span class="sxs-lookup"><span data-stu-id="9afb3-152">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="9afb3-153">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="9afb3-153">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="9afb3-154">Создание планов льгот</span><span class="sxs-lookup"><span data-stu-id="9afb3-154">Create benefit plans</span></span>

<span data-ttu-id="9afb3-155">В этих статьях показано, как создавать планы льгот, в том числе комплекты и программы по гибкой кредитной линии.</span><span class="sxs-lookup"><span data-stu-id="9afb3-155">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="9afb3-156">Настройка планов льгот</span><span class="sxs-lookup"><span data-stu-id="9afb3-156">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="9afb3-157">Настройка гибких программ кредитования</span><span class="sxs-lookup"><span data-stu-id="9afb3-157">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="9afb3-158">Обработка планов льгот</span><span class="sxs-lookup"><span data-stu-id="9afb3-158">Process benefit plans</span></span>

<span data-ttu-id="9afb3-159">Необходимо обработать некоторые изменения, чтобы сделать их активными.</span><span class="sxs-lookup"><span data-stu-id="9afb3-159">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="9afb3-160">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="9afb3-160">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="9afb3-161">Обработка событий в жизни</span><span class="sxs-lookup"><span data-stu-id="9afb3-161">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="9afb3-162">Обработка изменений в жизни</span><span class="sxs-lookup"><span data-stu-id="9afb3-162">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="9afb3-163">Обработка приемлемости событий в жизни</span><span class="sxs-lookup"><span data-stu-id="9afb3-163">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="9afb3-164">Обработка изменений ставок</span><span class="sxs-lookup"><span data-stu-id="9afb3-164">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

