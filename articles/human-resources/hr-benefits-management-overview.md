---
title: Обзор управления льготами
description: Обзор функции управления льготами в Dynamics 365 Human Resources. Предложите своим сотрудникам расширенные возможности с помощью простого в использовании интерактивного опыта.
author: andreabichsel
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 34b0916e0bf618590bcc56a9a3bc7c61576361cc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805786"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="d3dd7-104">Обзор управления льготами</span><span class="sxs-lookup"><span data-stu-id="d3dd7-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d3dd7-105">Чтобы остаться конкурентоспособными, вам необходимо предоставить широкий набор преимуществ для привлечения и сохранения лучших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="d3dd7-106">В дополнение к стандартным преимуществам, таким как покрытие медицинских услуг и услуг стоматологии, может возникнуть необходимость предоставить расширенные услуги, такие как помощь в адаптации, программы отдыха и надбавки за одежду.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="d3dd7-107">Управление льготами в Microsoft Dynamics 365 Human Resources предоставляет гибкое решение, поддерживающее разнообразные возможности использования льгот.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="d3dd7-108">Human Resources также содержит простое в использовании взаимодействие сотрудников, демонстрирующее ваши предложения.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="d3dd7-109">Планы расширенных льгот позволяют создавать и управлять уникальными планами льгот и поддерживают сложные таблицы нормативов льгот и вложенные уровни.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="d3dd7-110">Можно легко создавать программы льгот, наборы и правила автоматической регистрации для более простого понимания сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="d3dd7-111">Программы для кредитования по гибкому графику позволяют выполнить оценку в поддержку выхода на пенсию и других жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="d3dd7-112">Расширенные правила допустимости позволяют сделать доступными только те из них, на которые имеют право сотрудники.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="d3dd7-113">Возможность регистрации льгот в Интернете обеспечивает удобное для сотрудников использование.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="d3dd7-114">Квалифицированная обработка событий жизненного цикла поддерживает будущие события жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="d3dd7-115">Если вы хотите получить доступ к демонстрационным данным, вам потребуется повторно развернуть среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="d3dd7-116">Включение управления льготами</span><span class="sxs-lookup"><span data-stu-id="d3dd7-116">Enable Benefits management</span></span>

<span data-ttu-id="d3dd7-117">В этой теме описывается, как включить функции в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="d3dd7-118">Она также сообщает, какие существующие функции в Human Resources заменяются или отключаются после включения управления льготами.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3dd7-119">После включения управления льготами в **Производственной** среде его нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="d3dd7-120">Рекомендуется включить и проверить управление льготами в среде **Песочница** перед ее включением в **Производственной** среде.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="d3dd7-121">Существуют значительные различия между устаревшими функциональными возможностями льгот и новой функциональностью управления льготами, которые требуют дополнительной настройки и должны быть протестированы перед тем, как они будут помещены в производство.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="d3dd7-122">Управление функциями</span><span class="sxs-lookup"><span data-stu-id="d3dd7-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="d3dd7-123">Настройка сведений о сотрудниках</span><span class="sxs-lookup"><span data-stu-id="d3dd7-123">Configure employee information</span></span>

<span data-ttu-id="d3dd7-124">Перед регистрацией сотрудников для получения льгот необходимо ввести требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="d3dd7-125">Необходимо зарегистрировать сотрудника в пункте **План фиксированной компенсации** на начальной дате, а также необходимо выбрать значение **Частота оплаты льгот** в пункт **Сведения о занятости** в форме **Работник**.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="d3dd7-126">Если имеется сотрудник, который получает дополнительную компенсацию, такую как комиссионные, можно добавить сумму **Годовая зарплата льгот** из записи сотрудника.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="d3dd7-127">Модуль Human Resources использует сумму **Годовая зарплата льгот** при определении сумм покрытия вместо годовой суммы по фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="d3dd7-128">**Годовая зарплата льгот** должна быть действительна по состоянию на дату начала сотрудника или начало периода льготы, в зависимости от того, что является самым последним.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="d3dd7-129">Если для сотрудника записывается и фиксированная компенсация, и сумма годовой зарплаты льгот, годовая зарплата льгот будет использоваться для определения сумм покрытия.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="d3dd7-130">При создании плана льгот, в котором используются ставки на основе пола или возраста, необходимо ввести дату рождения и пол для сотрудника, чтобы рассчитать стоимость льготы.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="d3dd7-131">Настройка управления льготами</span><span class="sxs-lookup"><span data-stu-id="d3dd7-131">Configure Benefits management</span></span>

<span data-ttu-id="d3dd7-132">Прежде чем можно будет создавать планы льгот для сотрудников, необходимо настроить параметры для планов.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="d3dd7-133">Настройка параметров управления льготами</span><span class="sxs-lookup"><span data-stu-id="d3dd7-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="d3dd7-134">Настройка правил и параметров приемлемости</span><span class="sxs-lookup"><span data-stu-id="d3dd7-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="d3dd7-135">Настройка параметров приемлемости личных контактов</span><span class="sxs-lookup"><span data-stu-id="d3dd7-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="d3dd7-136">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="d3dd7-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="d3dd7-137">Настройка периодичности платежей</span><span class="sxs-lookup"><span data-stu-id="d3dd7-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="d3dd7-138">Настройка типов событий жизненного цикла</span><span class="sxs-lookup"><span data-stu-id="d3dd7-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="d3dd7-139">Создание типов планов</span><span class="sxs-lookup"><span data-stu-id="d3dd7-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="d3dd7-140">Настройка кодов причин</span><span class="sxs-lookup"><span data-stu-id="d3dd7-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="d3dd7-141">Настройка кодов уровней</span><span class="sxs-lookup"><span data-stu-id="d3dd7-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="d3dd7-142">Настройка ставок</span><span class="sxs-lookup"><span data-stu-id="d3dd7-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="d3dd7-143">Настройка вычетов</span><span class="sxs-lookup"><span data-stu-id="d3dd7-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="d3dd7-144">Настройка дней ожидания</span><span class="sxs-lookup"><span data-stu-id="d3dd7-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="d3dd7-145">Настройка периодов ожидания</span><span class="sxs-lookup"><span data-stu-id="d3dd7-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="d3dd7-146">Настройка правил округления</span><span class="sxs-lookup"><span data-stu-id="d3dd7-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="d3dd7-147">Создание категорий занятости</span><span class="sxs-lookup"><span data-stu-id="d3dd7-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="d3dd7-148">Настройка типов занятости</span><span class="sxs-lookup"><span data-stu-id="d3dd7-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="d3dd7-149">Настройка самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="d3dd7-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="d3dd7-150">Создание планов льгот</span><span class="sxs-lookup"><span data-stu-id="d3dd7-150">Create benefit plans</span></span>

<span data-ttu-id="d3dd7-151">В этих статьях показано, как создавать планы льгот, в том числе комплекты и программы по гибкой кредитной линии.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="d3dd7-152">Настройка планов льгот</span><span class="sxs-lookup"><span data-stu-id="d3dd7-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="d3dd7-153">Настройка гибких программ кредитования</span><span class="sxs-lookup"><span data-stu-id="d3dd7-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="d3dd7-154">Обработка планов льгот</span><span class="sxs-lookup"><span data-stu-id="d3dd7-154">Process benefit plans</span></span>

<span data-ttu-id="d3dd7-155">Необходимо обработать некоторые изменения, чтобы сделать их активными.</span><span class="sxs-lookup"><span data-stu-id="d3dd7-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="d3dd7-156">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="d3dd7-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="d3dd7-157">Обработка событий в жизни</span><span class="sxs-lookup"><span data-stu-id="d3dd7-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="d3dd7-158">Обработка изменений в жизни</span><span class="sxs-lookup"><span data-stu-id="d3dd7-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="d3dd7-159">Обработка приемлемости событий в жизни</span><span class="sxs-lookup"><span data-stu-id="d3dd7-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="d3dd7-160">Обработка изменений ставок</span><span class="sxs-lookup"><span data-stu-id="d3dd7-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]