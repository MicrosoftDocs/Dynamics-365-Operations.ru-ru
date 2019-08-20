---
title: Настройка управления расходами
description: Эта статья описывает вопросы и решения, которые следует принять во время процесса планирования, прежде чем настраивать Управление расходами в Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf0725a368969e8a2f85f38371d9f18f308246a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840921"
---
# <a name="configure-expense-management"></a><span data-ttu-id="b9b95-103">Настройка управления расходами</span><span class="sxs-lookup"><span data-stu-id="b9b95-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b95-104">Эта тема описывает вопросы и решения, которые следует принять во время процесса планирования, прежде чем настраивать Управление расходами в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b9b95-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b9b95-105">В модуле "Управление расходами" можно хранить информацию о способах оплаты, заявки на командировку, отчеты о расходах, политики и т. д.</span><span class="sxs-lookup"><span data-stu-id="b9b95-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="b9b95-106">Поскольку множество решений, которые вы принимаете при планировании конфигурации для управления расходами, основаны на иерархии и финансовой структуре организации, необходимо ссылаться на документы планирования для этих областей.</span><span class="sxs-lookup"><span data-stu-id="b9b95-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="b9b95-107">Внутрихолдинговые расходы</span><span class="sxs-lookup"><span data-stu-id="b9b95-107">Intercompany expenses</span></span>

<span data-ttu-id="b9b95-108">При включении внутрихолдинговых расходов вы позволяете юридическим лицам и сотрудникам совершать расходы от имени другого юридического лица в вашей организации и получать выплату от того юридического лица, в котором трудоустроен сотрудник.</span><span class="sxs-lookup"><span data-stu-id="b9b95-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="b9b95-109">Например, сотрудник в юридическом лице А выполняет проект для юридического лица Б, и в проекте возникают расходы, связанные с командировкой.</span><span class="sxs-lookup"><span data-stu-id="b9b95-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="b9b95-110">Если включены внутрихолдинговые расходы, сотрудник может подать отчет о расходах, в результате чего расходы будут разнесены в юридическом лице Б, и расходы затем должны будут быть выплачены юридическим лицом А. Если в организации только одно юридическое лицо, включать внутрихолдинговые расходы не требуется.</span><span class="sxs-lookup"><span data-stu-id="b9b95-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="b9b95-111">**Решение.** Хотите включить внутрихолдинговые расходы?</span><span class="sxs-lookup"><span data-stu-id="b9b95-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="b9b95-112">Управление финансами</span><span class="sxs-lookup"><span data-stu-id="b9b95-112">Financial management</span></span>

<span data-ttu-id="b9b95-113">Управление расходами тесно интегрировано с управлением финансами организации.</span><span class="sxs-lookup"><span data-stu-id="b9b95-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="b9b95-114">Большая часть настройки для управления расходами будет основываться на решениях, принятых в отношении финансов организации.</span><span class="sxs-lookup"><span data-stu-id="b9b95-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="b9b95-115">В следующих разделах описываются различные области, для которых требуется планирование и решения, основанные на решениях в отношении финансов организации и рекомендациях руководства.</span><span class="sxs-lookup"><span data-stu-id="b9b95-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="b9b95-116">Суточные</span><span class="sxs-lookup"><span data-stu-id="b9b95-116">Per diems</span></span>

<span data-ttu-id="b9b95-117">Необходимо определить работника для суточных, предоставляемых организацией.</span><span class="sxs-lookup"><span data-stu-id="b9b95-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="b9b95-118">Поскольку суточные обычно используются для покрытия расходов, таких как питание, проживание и другие случайные расходы, можно создать правила для суточных, предлагаемых организацией.</span><span class="sxs-lookup"><span data-stu-id="b9b95-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="b9b95-119">Нормы суточных могут зависеть от времени года, места командировки или от того и другого.</span><span class="sxs-lookup"><span data-stu-id="b9b95-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b9b95-120">При определении правила суточных можно указать, что процент от нормы суточных будет удерживается, если работник получает дополнительное питание или услуги.</span><span class="sxs-lookup"><span data-stu-id="b9b95-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b9b95-121">Также можно определить уровни норм суточных, чтобы задать минимальное и максимальное число часов, разрешенное нормой суточных для командировки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9b95-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="b9b95-122">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-122">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-123">Правила суточных по умолчанию для первого и последнего дней:</span><span class="sxs-lookup"><span data-stu-id="b9b95-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="b9b95-124">Каково минимальное количество часов, которые сотрудник может потребовать в день и получать суточные?</span><span class="sxs-lookup"><span data-stu-id="b9b95-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="b9b95-125">Уменьшается ли сумма, предлагаемая на питание в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="b9b95-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="b9b95-126">Если да, на какой процент она уменьшается?</span><span class="sxs-lookup"><span data-stu-id="b9b95-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b9b95-127">Уменьшается ли сумма, предлагаемая на гостиницу в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="b9b95-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="b9b95-128">Если да, на какой процент она уменьшается?</span><span class="sxs-lookup"><span data-stu-id="b9b95-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b9b95-129">Уменьшается ли сумма, предлагаемая на другие расходы в первый и последний день?</span><span class="sxs-lookup"><span data-stu-id="b9b95-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="b9b95-130">Если да, на какой процент она уменьшается?</span><span class="sxs-lookup"><span data-stu-id="b9b95-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="b9b95-131">Правила суточных по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="b9b95-131">Default per diem rules:</span></span>

    - <span data-ttu-id="b9b95-132">Уменьшается ли сумма суточных в процентах на каждый прием пищи, если, например, питание предоставляется бесплатно?</span><span class="sxs-lookup"><span data-stu-id="b9b95-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="b9b95-133">Если да, на какой процент уменьшается сумма на каждый прием пищи?</span><span class="sxs-lookup"><span data-stu-id="b9b95-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="b9b95-134">Снижение расходов на питание рассчитывается на день, на поездку или на количество приемов пищи в день?</span><span class="sxs-lookup"><span data-stu-id="b9b95-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="b9b95-135">Суммы суточных будут округляться обычным образом или округляться в большую сторону?</span><span class="sxs-lookup"><span data-stu-id="b9b95-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="b9b95-136">Суточные рассчитываются на 24-часовой период времени или на календарный день?</span><span class="sxs-lookup"><span data-stu-id="b9b95-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="b9b95-137">Правила суточных на основании места командировки:</span><span class="sxs-lookup"><span data-stu-id="b9b95-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="b9b95-138">Меняются ли нормы суточных в зависимости от места командировки?</span><span class="sxs-lookup"><span data-stu-id="b9b95-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="b9b95-139">Какие места командировки сюда входят?</span><span class="sxs-lookup"><span data-stu-id="b9b95-139">What locations are included?</span></span>
    - <span data-ttu-id="b9b95-140">Если нормы суточных меняются в зависимости от места командировки, какой процент предусмотрен на следующие типы расходов для каждого места командировки:</span><span class="sxs-lookup"><span data-stu-id="b9b95-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="b9b95-141">Питание</span><span class="sxs-lookup"><span data-stu-id="b9b95-141">Meals</span></span>
        - <span data-ttu-id="b9b95-142">Отель</span><span class="sxs-lookup"><span data-stu-id="b9b95-142">Hotel</span></span>
        - <span data-ttu-id="b9b95-143">Прочие расходы</span><span class="sxs-lookup"><span data-stu-id="b9b95-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="b9b95-144">Журналы и счета управления расходами</span><span class="sxs-lookup"><span data-stu-id="b9b95-144">Expense management journals and accounts</span></span>

<span data-ttu-id="b9b95-145">Для управления расходами требуется использовать несколько журналов и счетов.</span><span class="sxs-lookup"><span data-stu-id="b9b95-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="b9b95-146">Необходимо решить, например,будет ли использоваться один и тот же счет для денежных авансов и спорных вопросов по кредитной карте.</span><span class="sxs-lookup"><span data-stu-id="b9b95-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="b9b95-147">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-147">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-148">В какие журналы ГК разносятся утвержденные отчеты по расходам?</span><span class="sxs-lookup"><span data-stu-id="b9b95-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="b9b95-149">Какой счет используется для денежных авансов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="b9b95-150">Следует ли разносить денежные авансы немедленно?</span><span class="sxs-lookup"><span data-stu-id="b9b95-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="b9b95-151">Способы оплаты</span><span class="sxs-lookup"><span data-stu-id="b9b95-151">Payment methods</span></span>

<span data-ttu-id="b9b95-152">Если разрешить сотрудникам совершать расходы от имени организации, необходимо определить способы оплаты, которые могут использовать сотрудники.</span><span class="sxs-lookup"><span data-stu-id="b9b95-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="b9b95-153">Например, можно разрешить сотрудникам использовать наличные деньги или корпоративную кредитную карту.</span><span class="sxs-lookup"><span data-stu-id="b9b95-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="b9b95-154">Также можно разрешить сотрудникам использовать личные кредитные карты, а затем возместить им расходы.</span><span class="sxs-lookup"><span data-stu-id="b9b95-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="b9b95-155">Вы должны принять следующие решения для каждого разрешенного способа оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9b95-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="b9b95-156">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-156">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-157">Какие способы оплаты разрешаются?</span><span class="sxs-lookup"><span data-stu-id="b9b95-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="b9b95-158">Кто владеет расходами по способу оплаты?</span><span class="sxs-lookup"><span data-stu-id="b9b95-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="b9b95-159">Имеется ли тип корр. счета?</span><span class="sxs-lookup"><span data-stu-id="b9b95-159">Is there an offset account type?</span></span> <span data-ttu-id="b9b95-160">Если есть тип корреспондентского счета, какой это тип?</span><span class="sxs-lookup"><span data-stu-id="b9b95-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="b9b95-161">Имеется ли корр. счет, который является счетом?</span><span class="sxs-lookup"><span data-stu-id="b9b95-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="b9b95-162">Если в качестве способа оплаты используется кредитная карта, должен ли способ оплаты использоваться только с импортированными проводками?</span><span class="sxs-lookup"><span data-stu-id="b9b95-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="b9b95-163">Общие категории и категории расходов</span><span class="sxs-lookup"><span data-stu-id="b9b95-163">Expense categories and shared categories</span></span>

<span data-ttu-id="b9b95-164">Когда сотрудники создают отчет по расходам, каждый регистрируемый расход необходимо связать с категорией расхода.</span><span class="sxs-lookup"><span data-stu-id="b9b95-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="b9b95-165">Категории расходов наследуются от общих категорий, которые можно использоваться во всех юридических лицах в пределах организации.</span><span class="sxs-lookup"><span data-stu-id="b9b95-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="b9b95-166">Эти категории также можно использовать в модуле "Управление и учет по проектам" в зависимости от того, как определена ваша организация.</span><span class="sxs-lookup"><span data-stu-id="b9b95-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="b9b95-167">На основании определения организации и рекомендаций специалистов по внедрению определите, будут ли категории, используемые в модуле "Управление расходами", использоваться только в этом модуле или будут использоваться одновременно в модулях "Управление и учет по проектам" и "Управление расходами".</span><span class="sxs-lookup"><span data-stu-id="b9b95-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="b9b95-168">Обратите внимание, что эти категории можно совместно использовать в проекте и расходах или в проекте и производстве, но не в расходах и производстве.</span><span class="sxs-lookup"><span data-stu-id="b9b95-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="b9b95-169">Необходимо принять следующие решения для каждой категории расходов.</span><span class="sxs-lookup"><span data-stu-id="b9b95-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="b9b95-170">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-170">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-171">Что такое категория расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-171">What is the expense category?</span></span> <span data-ttu-id="b9b95-172">Примерами являются категории для авиабилетов, гостиниц или пробега автомобиля.</span><span class="sxs-lookup"><span data-stu-id="b9b95-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="b9b95-173">Может ли данная категория расходов также использоваться в модуле "Управление и учет по проектам"?</span><span class="sxs-lookup"><span data-stu-id="b9b95-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="b9b95-174">Что такое тип расхода?</span><span class="sxs-lookup"><span data-stu-id="b9b95-174">What is the expense type?</span></span>
- <span data-ttu-id="b9b95-175">Какой способ оплаты по умолчанию используется для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="b9b95-176">Должны ли расходы в категории расходов быть детализированы?</span><span class="sxs-lookup"><span data-stu-id="b9b95-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="b9b95-177">Какой основной счет по умолчанию используется для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="b9b95-178">Какая налоговая группа номенклатур по умолчанию используется для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="b9b95-179">Разрешены ли дополнительные способы оплаты для категории расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="b9b95-180">Если разрешены дополнительные способы оплаты, какие это способы?</span><span class="sxs-lookup"><span data-stu-id="b9b95-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="b9b95-181">Имеются ли подкатегории в данной категории расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="b9b95-182">Если имеются подкатегории, необходимо также принять следующие решения:</span><span class="sxs-lookup"><span data-stu-id="b9b95-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="b9b95-183">Исключены ли какие-либо подкатегории из возмещения налога?</span><span class="sxs-lookup"><span data-stu-id="b9b95-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="b9b95-184">Какая налоговая группа номенклатур используется для подкатегорий?</span><span class="sxs-lookup"><span data-stu-id="b9b95-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="b9b95-185">Если эта категория расходов также используется в модуле "Управление и учет по проектам", ответьте на оставшиеся вопросы.</span><span class="sxs-lookup"><span data-stu-id="b9b95-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="b9b95-186">В противном случае переходите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="b9b95-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="b9b95-187">Какие счета затрат будут использоваться для следующих расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="b9b95-188">Затраты</span><span class="sxs-lookup"><span data-stu-id="b9b95-188">Cost</span></span>
    - <span data-ttu-id="b9b95-189">Распределение зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9b95-189">Payroll allocation</span></span>
    - <span data-ttu-id="b9b95-190">НЗП - Себестоимость</span><span class="sxs-lookup"><span data-stu-id="b9b95-190">WIP-cost value</span></span>
    - <span data-ttu-id="b9b95-191">Себестоимость — Номенклатура</span><span class="sxs-lookup"><span data-stu-id="b9b95-191">Cost-item</span></span>
    - <span data-ttu-id="b9b95-192">НЗП - Себестоимость - Номенклатура</span><span class="sxs-lookup"><span data-stu-id="b9b95-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="b9b95-193">Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="b9b95-193">Accrued loss</span></span>
    - <span data-ttu-id="b9b95-194">НЗП — Начисленный убыток</span><span class="sxs-lookup"><span data-stu-id="b9b95-194">WIP-accrued loss</span></span>

- <span data-ttu-id="b9b95-195">Какие счета выручки будут использоваться для следующего?</span><span class="sxs-lookup"><span data-stu-id="b9b95-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="b9b95-196">Выручка по выставленным накладным</span><span class="sxs-lookup"><span data-stu-id="b9b95-196">Invoiced revenue</span></span>
    - <span data-ttu-id="b9b95-197">Начисленный доход — сумма реализации</span><span class="sxs-lookup"><span data-stu-id="b9b95-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="b9b95-198">НЗП — Сумма реализации</span><span class="sxs-lookup"><span data-stu-id="b9b95-198">WIP-sales value</span></span>
    - <span data-ttu-id="b9b95-199">Начисленный доход — Производство</span><span class="sxs-lookup"><span data-stu-id="b9b95-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="b9b95-200">НЗП — Производство</span><span class="sxs-lookup"><span data-stu-id="b9b95-200">WIP-production</span></span>
    - <span data-ttu-id="b9b95-201">Начисленный доход — Прибыль</span><span class="sxs-lookup"><span data-stu-id="b9b95-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="b9b95-202">НЗП-— Прибыль</span><span class="sxs-lookup"><span data-stu-id="b9b95-202">WIP-profit</span></span>
    - <span data-ttu-id="b9b95-203">Начисленный доход — Подписка</span><span class="sxs-lookup"><span data-stu-id="b9b95-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="b9b95-204">НЗП — Подписка</span><span class="sxs-lookup"><span data-stu-id="b9b95-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="b9b95-205">Налоги</span><span class="sxs-lookup"><span data-stu-id="b9b95-205">Taxes</span></span>

<span data-ttu-id="b9b95-206">Для связанных с расходами налогов необходимо определить, что включать в отчеты по расходам.</span><span class="sxs-lookup"><span data-stu-id="b9b95-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="b9b95-207">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-207">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-208">Включен ли налог в суммы расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="b9b95-209">Следует ли включить возмещение налога для расходов?</span><span class="sxs-lookup"><span data-stu-id="b9b95-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="b9b95-210">При планировании главной книги, если вы решили применять налоги США и использовать правила налогов, вы не можете включить возмещение налогов по расходам.</span><span class="sxs-lookup"><span data-stu-id="b9b95-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="b9b95-211">(Для применения налогов США и использования правил налогов установите параметр **Применить правила налогообложения** в значение **Да**.)</span><span class="sxs-lookup"><span data-stu-id="b9b95-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="b9b95-212">Политики</span><span class="sxs-lookup"><span data-stu-id="b9b95-212">Policies</span></span>

<span data-ttu-id="b9b95-213">Путем создания политик отчетов по расходам вы можете помочь своей организации экономить время и деньги, когда сотрудники совершают расходы от ее имени.</span><span class="sxs-lookup"><span data-stu-id="b9b95-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="b9b95-214">Политики помогают гарантировать, что сотрудники будут оставаться в рамках бюджета, предоставлять всю необходимую информацию и тратить деньги только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b9b95-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="b9b95-215">Необходимо принять следующие решения для каждой создаваемой политики отчетов по расходам и каждой политики утверждения отчетов по расходам.</span><span class="sxs-lookup"><span data-stu-id="b9b95-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="b9b95-216">**Решения.**</span><span class="sxs-lookup"><span data-stu-id="b9b95-216">**Decisions:**</span></span>

- <span data-ttu-id="b9b95-217">Каково имя политики?</span><span class="sxs-lookup"><span data-stu-id="b9b95-217">What is the name of the policy?</span></span>
- <span data-ttu-id="b9b95-218">Для чего предназначена политика?</span><span class="sxs-lookup"><span data-stu-id="b9b95-218">What is the expense policy for?</span></span>
- <span data-ttu-id="b9b95-219">Если вы ранее решили включить внутрихолдинговые расходы, к каким компаниям в вашей организации будет применяться эта политика?</span><span class="sxs-lookup"><span data-stu-id="b9b95-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="b9b95-220">Когда политика вступает в силу?</span><span class="sxs-lookup"><span data-stu-id="b9b95-220">When does the policy become effective?</span></span>
- <span data-ttu-id="b9b95-221">Когда истекает срок действия политики?</span><span class="sxs-lookup"><span data-stu-id="b9b95-221">When does the policy expire?</span></span>
- <span data-ttu-id="b9b95-222">Что такое правило политики?</span><span class="sxs-lookup"><span data-stu-id="b9b95-222">What is the policy rule?</span></span>
- <span data-ttu-id="b9b95-223">Каков результат правила политики?</span><span class="sxs-lookup"><span data-stu-id="b9b95-223">What is the outcome of the policy rule?</span></span>
