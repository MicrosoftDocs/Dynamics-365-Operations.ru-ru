---
title: Определение и управление программой льгот
description: Человеческие ресурсы обеспечивают комплект инструментов, которые можно использовать для того, чтобы настроить и поддержать льготы, вычеты, и планы компенсации работников, которые организация предлагает или обрабатывает для своих работников. Эта статья обеспечивает информацию, как настроить преимущества и управлять ими.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c31564fdc40cb0cba82b9ab8fbfdfee7adf4f4ee
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053017"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="1e4ff-104">Определение программ льгот и управление ими</span><span class="sxs-lookup"><span data-stu-id="1e4ff-104">Define and manage a benefits program</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1e4ff-105">Human Resources обеспечивает комплект инструментов, которые можно использовать для того, чтобы настроить и поддержать льготы, вычеты, и планы компенсации работников, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-105">Human Resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="1e4ff-106">Эта статья обеспечивает информацию, как настроить преимущества и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="1e4ff-107">Настройка льгот</span><span class="sxs-lookup"><span data-stu-id="1e4ff-107">Benefit setup</span></span>

<span data-ttu-id="1e4ff-108">Прежде чем работников можно зарегистрировать в льготах, вы должны создать элементы каждой льготы.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="1e4ff-109">Эти элементы совмещают сходные планы льгот и определяют параметры по умолчанию, такие как ставки вычетов и детали учета.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="1e4ff-110">Многие из этих установок можно отрегулировать, когда работники позже регистрируются на льготы.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="1e4ff-111">Для каждого плана льгот организация может предложить несколько вариантов регистрации, или работник может отказаться от участия в плане.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="1e4ff-112">[![Поток операций льгот](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="1e4ff-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="1e4ff-113">Элементы льготы</span><span class="sxs-lookup"><span data-stu-id="1e4ff-113">Benefit elements</span></span>

<span data-ttu-id="1e4ff-114">Прежде чем вы начинаете создавать льготы и регистрировать работников в них, вы должны определить элементы, которые составляют льготу: тип, план и варианты.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="1e4ff-115">**Тип** — коллекция планов для конкретной льготы, например медицинской или парковочной.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="1e4ff-116">**План** — конкретная льгота, на которую заключен контракт с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="1e4ff-117">**Вариант** — уровень покрытия, например "только сотрудник" или "сотрудник и супруг/партнер".</span><span class="sxs-lookup"><span data-stu-id="1e4ff-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="1e4ff-118">Для каждого типа льготы, например окулист или стоматолог, организация может предложить одни или несколько планов своим работникам.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="1e4ff-119">Для каждого плана организация может предложить различные варианты.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="1e4ff-120">Например, работники могут купить дополнительное страховое покрытие жизни в размере одной, двух или трех годовых зарплат.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="1e4ff-121">Каждое сочетание из плана и вариантов становится льготой, на которую работники могут зарегистрироваться.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="1e4ff-122">[![Рис. Льготы](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="1e4ff-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="1e4ff-123">Приемлемость</span><span class="sxs-lookup"><span data-stu-id="1e4ff-123">Eligibility</span></span>
<span data-ttu-id="1e4ff-124">Много факторов определяют приемлемость работника для различных типов льгот, которые работодатель предлагает.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="1e4ff-125">Когда вы создаете льготу в Dynamics 365 Human Resources, вы можете установить тип приемлемости, которая применяется к этой льготе.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="1e4ff-126">Вы можете сделать льготу доступной всем работникам.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="1e4ff-127">Например, некоторые компании предлагают парковочные пропуска всем работникам как дополнительную льготу.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="1e4ff-128">Когда вы создаете эту льготу, вы устанавливаете приемлемость как **Имеют право все работники**.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="1e4ff-129">Для других льгот, например удержание части зарплаты и налоговые сборы, приемлемость не применяется.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="1e4ff-130">Когда вы создаете эти типы льгот, вы ставите приемлемость как **Обход процесса допустимости**.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="1e4ff-131">Наконец, приемлемость льгот может быть основана на правилах.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="1e4ff-132">Например, компания предлагает два типа страхования жизни работникам.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="1e4ff-133">Руководители могут пользоваться одним планом страхования жизни, тогда как все другие работники на полном рабочем дне могут пользоваться другим планом страхования жизни.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="1e4ff-134">В Human Resources вы можете создать правило приемлемости льготы, чтобы найти всех руководителей, и другое правило для того, чтобы найти всех других работников на полном рабочем дне, и после этого применить эти правила к соответствующей льготе.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="1e4ff-135">Регистрация</span><span class="sxs-lookup"><span data-stu-id="1e4ff-135">Enrollment</span></span>
<span data-ttu-id="1e4ff-136">После того как вы создавали льготы, которые ваша организация предлагает, и определили приемлемость, вы можете зачислить ваших работников на льготы.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="1e4ff-137">Вы можете зачислить одного работника на льготы, или вы можете зачислить много работников на одну или больше льгот за один процесс.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="1e4ff-138">Иногда, организация прекращает предлагать некоторые преимущества.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="1e4ff-139">В этом случае вы должны обновить льготу и работников, которые зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="1e4ff-140">Массовое истечение срока действия льгот позволяет одновременно изменить дату истечения срока как льготы, так и регистраций работников на эту льготу.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="1e4ff-141">Можно также выбрать несколько сотрудников, включенных в льготу, и изменить дату окончания их покрытия.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="1e4ff-142">Подобным образом, массовое продление льготы позволяет вам продлить дату истечения срока как льготы, так и регистрации работника на эту льготу, если вы решаете предложить льготу дольше, чем вы первоначально запланировали.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]