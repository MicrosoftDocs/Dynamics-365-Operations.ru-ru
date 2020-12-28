---
title: Определение правил и политик проверки прав на льготы
description: Эта статья показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420234"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="ea27a-103">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="ea27a-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="ea27a-104">Эта статья показывает, как создавать правила и политики проверки прав на льготы, а затем назначать правила льготам.</span><span class="sxs-lookup"><span data-stu-id="ea27a-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="ea27a-105">В качестве компании с демонстрационными данными для создания этой записи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ea27a-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="ea27a-106">Создание типа правил политики приемлемости льготы</span><span class="sxs-lookup"><span data-stu-id="ea27a-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="ea27a-107">Перейдите в раздел "Управление персоналом" > "Льготы" > "Приемлемость" > "Типы правил политики права на льготу".</span><span class="sxs-lookup"><span data-stu-id="ea27a-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="ea27a-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ea27a-108">Click New.</span></span>
3. <span data-ttu-id="ea27a-109">В поле "Правило" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ea27a-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="ea27a-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ea27a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ea27a-111">В поле "Имя запроса" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ea27a-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ea27a-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ea27a-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ea27a-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ea27a-113">Click Save.</span></span>
8. <span data-ttu-id="ea27a-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="ea27a-115">Политика права на льготу</span><span class="sxs-lookup"><span data-stu-id="ea27a-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="ea27a-116">Перейдите в раздел "Управление персоналом" > "Льготы" > "Приемлемость" > "Политики приемлемости льготы".</span><span class="sxs-lookup"><span data-stu-id="ea27a-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="ea27a-117">Выберите существующую политику права на льготу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="ea27a-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ea27a-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ea27a-119">Переключите развертывание разделов организаций политики.</span><span class="sxs-lookup"><span data-stu-id="ea27a-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="ea27a-120">Здесь можно добавить или удалить организации, которые требуется включить в политику.</span><span class="sxs-lookup"><span data-stu-id="ea27a-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="ea27a-121">Разверните или сверните раздел "Правила политики".</span><span class="sxs-lookup"><span data-stu-id="ea27a-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="ea27a-122">Найдите в списке ранее созданное правило политики.</span><span class="sxs-lookup"><span data-stu-id="ea27a-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="ea27a-123">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="ea27a-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="ea27a-124">В поле "Действует с" введите дату, когда политика должна вступить в силу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="ea27a-125">Задание даты вступления в силу и даты окончания позволяет вносить в правила политики изменения, которые должны вступить в силу в будущем, не возвращаясь в политике перед моментом вступления их в силу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="ea27a-126">Например, если требуется, чтобы правило применялось только к менеджерам по продажам, можно создать предложение с условием "Где", например: "Где описание должности равно Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="ea27a-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="ea27a-127">В одном правиле можно объединить несколько операторов "Где" с помощью операторов "И" и "Или".</span><span class="sxs-lookup"><span data-stu-id="ea27a-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="ea27a-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ea27a-128">Click OK.</span></span>
11. <span data-ttu-id="ea27a-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-129">Close the page.</span></span>
12. <span data-ttu-id="ea27a-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ea27a-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="ea27a-131">Назначение правила льготе</span><span class="sxs-lookup"><span data-stu-id="ea27a-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="ea27a-132">Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".</span><span class="sxs-lookup"><span data-stu-id="ea27a-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="ea27a-133">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ea27a-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ea27a-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ea27a-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ea27a-135">Разверните или сверните раздел "Правила приемлемости".</span><span class="sxs-lookup"><span data-stu-id="ea27a-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="ea27a-136">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="ea27a-136">Click Edit.</span></span>
6. <span data-ttu-id="ea27a-137">В поле "Приемлемость" выберите из списка "На основе правила".</span><span class="sxs-lookup"><span data-stu-id="ea27a-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="ea27a-138">В поле "Тип правила" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ea27a-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="ea27a-139">Найдите в списке ранее созданное правило и выберите его.</span><span class="sxs-lookup"><span data-stu-id="ea27a-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="ea27a-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ea27a-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ea27a-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ea27a-141">Click Save.</span></span>
11. <span data-ttu-id="ea27a-142">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="ea27a-142">Close the form.</span></span>

