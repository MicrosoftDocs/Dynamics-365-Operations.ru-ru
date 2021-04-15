---
title: Создание планов льгот работников
description: Можно создать планы льгот работника в Microsoft Dynamics 365 Human Resources, чтобы выбрать планы льгот для сотрудников и подтвердить выбор плана льгот.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: baa131b3bcab73d29c7059f6595f1e8943f8164f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804945"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="26450-103">Создание планов льгот работников</span><span class="sxs-lookup"><span data-stu-id="26450-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="26450-104">Можно создать планы льгот работника в Microsoft Dynamics 365 Human Resources, чтобы выбрать планы льгот для сотрудников и подтвердить выбор плана льгот.</span><span class="sxs-lookup"><span data-stu-id="26450-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="26450-105">Обычно сотрудники самостоятельно выбирают планы льгот, используя дистанционное обслуживание сотрудников, а затем администратор льгот подтверждает выбор.</span><span class="sxs-lookup"><span data-stu-id="26450-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="26450-106">В рабочей области **Управления льготами** в **Планы** выберите **Планы льгот работников**.</span><span class="sxs-lookup"><span data-stu-id="26450-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="26450-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="26450-107">Select **New**.</span></span>

3. <span data-ttu-id="26450-108">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="26450-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="26450-109">Поле</span><span class="sxs-lookup"><span data-stu-id="26450-109">Field</span></span> | <span data-ttu-id="26450-110">Описание</span><span class="sxs-lookup"><span data-stu-id="26450-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="26450-111">Период</span><span class="sxs-lookup"><span data-stu-id="26450-111">Period</span></span> | <span data-ttu-id="26450-112">Указывает период льгот, который будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="26450-113">Например, выберите созданный период, который называется "2015", чтобы подтвердить все льготные варианты регистрации для "2015".</span><span class="sxs-lookup"><span data-stu-id="26450-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="26450-114">Рабочий</span><span class="sxs-lookup"><span data-stu-id="26450-114">Worker</span></span> | <span data-ttu-id="26450-115">Указывает работника, который будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-116">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="26450-116">Legal entity</span></span> | <span data-ttu-id="26450-117">Указывает юридическое лицо, которое будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-118">Параметр покрытия</span><span class="sxs-lookup"><span data-stu-id="26450-118">Coverage option</span></span> | <span data-ttu-id="26450-119">Указывает параметр покрытия, который будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-120">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="26450-120">Default</span></span> | <span data-ttu-id="26450-121">Фильтрует планы льгот в зависимости от того, являются ли они планом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26450-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="26450-122">Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="26450-123">Status</span></span> | <span data-ttu-id="26450-124">Фильтры планов льгот по их статусу.</span><span class="sxs-lookup"><span data-stu-id="26450-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="26450-125">Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-126">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="26450-126">Confirmation</span></span> | <span data-ttu-id="26450-127">Указывает статус подтверждения, который будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-128">Отмена</span><span class="sxs-lookup"><span data-stu-id="26450-128">Cancellation</span></span> | <span data-ttu-id="26450-129">Указывает статус отмены, который будет использоваться для фильтрации планов на вкладке планов. Отфильтруйте планы, чтобы помочь выбрать подмножество всех записей плана, чтобы можно было подтвердить подмножество.</span><span class="sxs-lookup"><span data-stu-id="26450-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="26450-130">Фильтр дат вступления в силу</span><span class="sxs-lookup"><span data-stu-id="26450-130">Effective date filter</span></span> | <span data-ttu-id="26450-131">Фильтрует планы в зависимости от того, просрочены они, активны или будут активными в будущем.</span><span class="sxs-lookup"><span data-stu-id="26450-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="26450-132">Установите флажки, соответствующие планам, которые необходимо увидеть на экспресс-вкладке планов.</span><span class="sxs-lookup"><span data-stu-id="26450-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="26450-133">Планы</span><span class="sxs-lookup"><span data-stu-id="26450-133">Plans</span></span> | <span data-ttu-id="26450-134">Экспресс-вкладка "Планы" содержит планы, отвечающие заданным критериям фильтрации.</span><span class="sxs-lookup"><span data-stu-id="26450-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="26450-135">Соответствующие параметры конфигурации, которые были установлены сотрудниками отдела кадров, и выбранные сотрудниками регистрации, включаются в каждую строку.</span><span class="sxs-lookup"><span data-stu-id="26450-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="26450-136">Поле квалификации указывает, имеется ли конфликт проверки с выбранным планом.</span><span class="sxs-lookup"><span data-stu-id="26450-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="26450-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="26450-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]