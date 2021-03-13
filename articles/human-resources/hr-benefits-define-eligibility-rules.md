---
title: Определение правил и политик проверки прав на льготы
description: Эта статья показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113969"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="9875e-103">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="9875e-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="9875e-104">Эта тема показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.</span><span class="sxs-lookup"><span data-stu-id="9875e-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="9875e-105">Создание типа правил политики приемлемости льготы</span><span class="sxs-lookup"><span data-stu-id="9875e-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="9875e-106">Перейдите в раздел **Управление персоналом > Льготы > Приемлемость > Типы правил политики права на льготу**.</span><span class="sxs-lookup"><span data-stu-id="9875e-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="9875e-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9875e-107">Select **New**.</span></span>
3. <span data-ttu-id="9875e-108">В поле **Имя правила** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9875e-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="9875e-109">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9875e-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="9875e-110">В поле **Имя запроса** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="9875e-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9875e-111">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9875e-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="9875e-112">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9875e-112">Select **Save**.</span></span>
8. <span data-ttu-id="9875e-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9875e-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="9875e-114">Политика права на льготу</span><span class="sxs-lookup"><span data-stu-id="9875e-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="9875e-115">Перейдите в раздел **Управление персоналом > Льготы > Приемлемость > Политики приемлемости льготы**.</span><span class="sxs-lookup"><span data-stu-id="9875e-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="9875e-116">Выберите существующую политику права на льготу.</span><span class="sxs-lookup"><span data-stu-id="9875e-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="9875e-117">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9875e-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="9875e-118">Переключите развертывание разделов **Организации политики**.</span><span class="sxs-lookup"><span data-stu-id="9875e-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="9875e-119">Можно добавить или удалить организации, которые требуется включить в политику.</span><span class="sxs-lookup"><span data-stu-id="9875e-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="9875e-120">Разверните или сверните раздел **Правила политики**.</span><span class="sxs-lookup"><span data-stu-id="9875e-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="9875e-121">Найдите в списке ранее созданное правило политики.</span><span class="sxs-lookup"><span data-stu-id="9875e-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="9875e-122">Выберите **Создать правило политики**.</span><span class="sxs-lookup"><span data-stu-id="9875e-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="9875e-123">В поле **Действует с** введите дату, когда политика должна вступить в силу.</span><span class="sxs-lookup"><span data-stu-id="9875e-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="9875e-124">Задание даты вступления в силу и даты окончания позволяет вносить в правила политики изменения, которые должны вступить в силу в будущем, чтобы не возвращаться к политике перед моментом вступления их в силу.</span><span class="sxs-lookup"><span data-stu-id="9875e-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="9875e-125">При необходимости добавьте предложение в поле **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="9875e-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="9875e-126">Например, если требуется, чтобы правило применялось только к менеджерам по продажам, можно создать предложение с условием "Где", например: "Где описание должности равно Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="9875e-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="9875e-127">В одно правило можно добавить несколько операторов "Где".</span><span class="sxs-lookup"><span data-stu-id="9875e-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="9875e-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9875e-128">Select **OK**.</span></span>
11. <span data-ttu-id="9875e-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9875e-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="9875e-130">Назначение правила льготе</span><span class="sxs-lookup"><span data-stu-id="9875e-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="9875e-131">Перейдите в раздел **Управление персоналом > Льготы > Льготы**.</span><span class="sxs-lookup"><span data-stu-id="9875e-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="9875e-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9875e-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9875e-133">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9875e-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="9875e-134">Разверните или сверните раздел **Правила приемлемости**.</span><span class="sxs-lookup"><span data-stu-id="9875e-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="9875e-135">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="9875e-135">Select **Edit**.</span></span>
6. <span data-ttu-id="9875e-136">В поле **Приемлемость** выберите правило.</span><span class="sxs-lookup"><span data-stu-id="9875e-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="9875e-137">В поле **Тип правила** выберите ранее созданное правило.</span><span class="sxs-lookup"><span data-stu-id="9875e-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="9875e-138">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9875e-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="9875e-139">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9875e-139">Select **Save**.</span></span>
11. <span data-ttu-id="9875e-140">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="9875e-140">Close the form.</span></span>

