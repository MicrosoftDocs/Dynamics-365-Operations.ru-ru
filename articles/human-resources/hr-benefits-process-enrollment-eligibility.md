---
title: Обработка приемлемости регистрации
description: В этой статье объясняется, как выполнить процесс допустимости регистрации.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429297"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="bd77e-103">Обработка приемлемости регистрации</span><span class="sxs-lookup"><span data-stu-id="bd77e-103">Process enrollment eligibility</span></span>

<span data-ttu-id="bd77e-104">В этой статье объясняется, как выполнить процесс допустимости регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="bd77e-105">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка допустимости регистрации**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="bd77e-106">В диалоговом окне **Выполнение процесса допустимости регистрации льгот** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="bd77e-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="bd77e-107">Поле</span><span class="sxs-lookup"><span data-stu-id="bd77e-107">Field</span></span> | <span data-ttu-id="bd77e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bd77e-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bd77e-109">**Период регистрации**</span><span class="sxs-lookup"><span data-stu-id="bd77e-109">**Enrollment period**</span></span> | <span data-ttu-id="bd77e-110">Период регистрации, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="bd77e-111">**Информация о компании**</span><span class="sxs-lookup"><span data-stu-id="bd77e-111">**Legal entity**</span></span> | <span data-ttu-id="bd77e-112">Юридическое лицо, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="bd77e-113">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="bd77e-113">**Worker**</span></span> | <span data-ttu-id="bd77e-114">Работник, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="bd77e-115">Если оставить это поле пустым, допустимость регистрации будет обработана для всех работников.</span><span class="sxs-lookup"><span data-stu-id="bd77e-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="bd77e-116">**План льготы**</span><span class="sxs-lookup"><span data-stu-id="bd77e-116">**Benefit plan**</span></span> | <span data-ttu-id="bd77e-117">План льгот, для которого необходимо обработать допустимость регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="bd77e-118">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bd77e-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="bd77e-119">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="bd77e-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="bd77e-120">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="bd77e-121">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="bd77e-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-122">Select **OK**.</span></span> <span data-ttu-id="bd77e-123">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="bd77e-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="bd77e-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="bd77e-125">Просмотр результатов обработки</span><span class="sxs-lookup"><span data-stu-id="bd77e-125">View Process Results</span></span>

<span data-ttu-id="bd77e-126">В этой статье объясняется, как просматривать результаты обработки применимости.</span><span class="sxs-lookup"><span data-stu-id="bd77e-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="bd77e-127">В рабочей области **Управление льготами** в **Обработка** выберите **Результаты обработки**.</span><span class="sxs-lookup"><span data-stu-id="bd77e-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="bd77e-128">В форме **Результаты обработки** указываются следующие поля:</span><span class="sxs-lookup"><span data-stu-id="bd77e-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="bd77e-129">Поле</span><span class="sxs-lookup"><span data-stu-id="bd77e-129">Field</span></span> | <span data-ttu-id="bd77e-130">описание</span><span class="sxs-lookup"><span data-stu-id="bd77e-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bd77e-131">**Идентификатор процесса**</span><span class="sxs-lookup"><span data-stu-id="bd77e-131">**Process ID**</span></span> | <span data-ttu-id="bd77e-132">Уникальный код комбинации работника, юридического лица и выполнения обработки.</span><span class="sxs-lookup"><span data-stu-id="bd77e-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="bd77e-133">**Тип процесса**</span><span class="sxs-lookup"><span data-stu-id="bd77e-133">**Process type**</span></span> | <span data-ttu-id="bd77e-134">Этот определяет выполненный процесс.</span><span class="sxs-lookup"><span data-stu-id="bd77e-134">This identifies the process that was run.</span></span> <span data-ttu-id="bd77e-135">Например: Регистрация.</span><span class="sxs-lookup"><span data-stu-id="bd77e-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="bd77e-136">**Отметка времени**</span><span class="sxs-lookup"><span data-stu-id="bd77e-136">**Time stamp**</span></span> | <span data-ttu-id="bd77e-137">Время, в которое был выполнена обработка применимости.</span><span class="sxs-lookup"><span data-stu-id="bd77e-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="bd77e-138">**Информация о компании**</span><span class="sxs-lookup"><span data-stu-id="bd77e-138">**Legal entity**</span></span> | <span data-ttu-id="bd77e-139">Юридическое лицо, указанное в процессе регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="bd77e-140">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="bd77e-140">**Worker**</span></span> | <span data-ttu-id="bd77e-141">Сотрудник, который был обработан.</span><span class="sxs-lookup"><span data-stu-id="bd77e-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="bd77e-142">\*\*План</span><span class="sxs-lookup"><span data-stu-id="bd77e-142">\*\*Plan</span></span> | <span data-ttu-id="bd77e-143">План льгот, для которого была выполнена попытка регистрации.</span><span class="sxs-lookup"><span data-stu-id="bd77e-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="bd77e-144">**Правило допустимости**</span><span class="sxs-lookup"><span data-stu-id="bd77e-144">**Eligibility rule**</span></span> | <span data-ttu-id="bd77e-145">Обработанное правило применимости.</span><span class="sxs-lookup"><span data-stu-id="bd77e-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="bd77e-146">Если ошибка была обнаружена до начала проверки применимости, это поле останется пустым.</span><span class="sxs-lookup"><span data-stu-id="bd77e-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="bd77e-147">Например, если для сотрудника не была определена компенсация, обработка применимости не будет запущена, и это поле останется пустым.</span><span class="sxs-lookup"><span data-stu-id="bd77e-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="bd77e-148">**Полученный статус**</span><span class="sxs-lookup"><span data-stu-id="bd77e-148">**Result status**</span></span> | <span data-ttu-id="bd77e-149">Это будет "Применимо" или "Неприменимо".</span><span class="sxs-lookup"><span data-stu-id="bd77e-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="bd77e-150">Статус результата будет "Неприменимо", если сотрудник не соответствует критериям правила применимости, если работнику не хватает необходимой информации, например, частоты оплаты или фиксированная компенсация, или если отсутствуют сведения о плане льгот, которые не позволяют регистрировать работников.</span><span class="sxs-lookup"><span data-stu-id="bd77e-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="bd77e-151">**Сообщение результата**</span><span class="sxs-lookup"><span data-stu-id="bd77e-151">**Result message**</span></span> | <span data-ttu-id="bd77e-152">Указывает, почему работник не имеет права на план льгот, или выполнены ли условия правила применимости.</span><span class="sxs-lookup"><span data-stu-id="bd77e-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

