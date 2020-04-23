---
title: Создание параметров покрытия
description: Параметры покрытия в Microsoft Dynamics 365 Human Resources представляют собой уровни покрытия для выборов участника в плане или программе льгот.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 021fea7604af2fff833ddc6868d55a316ef70aae
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230185"
---
# <a name="create-coverage-options"></a><span data-ttu-id="176c6-103">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="176c6-103">Create coverage options</span></span>

<span data-ttu-id="176c6-104">Параметры покрытия в Microsoft Dynamics 365 Human Resources представляют собой уровни покрытия для выборов участника в плане или программе льгот.</span><span class="sxs-lookup"><span data-stu-id="176c6-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="176c6-105">Например, параметры покрытия могут включать **Только сотрудник** для медицинских планов или **Две заработные платы** для плана страхования жизни.</span><span class="sxs-lookup"><span data-stu-id="176c6-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="176c6-106">После определения можно повторно использовать параметры покрытия для льготы.</span><span class="sxs-lookup"><span data-stu-id="176c6-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="176c6-107">Можно связать параметр с одним или несколькими планами.</span><span class="sxs-lookup"><span data-stu-id="176c6-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="176c6-108">После определения параметров покрытия приложите параметры покрытия к типу плана льгот.</span><span class="sxs-lookup"><span data-stu-id="176c6-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="176c6-109">Этот тип плана затем связывается с планом льгот или программой.</span><span class="sxs-lookup"><span data-stu-id="176c6-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="176c6-110">Параметры покрытия, связанные с типом плана, доступны для всех планов, созданных с этим типом плана.</span><span class="sxs-lookup"><span data-stu-id="176c6-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="176c6-111">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Параметры покрытия**.</span><span class="sxs-lookup"><span data-stu-id="176c6-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="176c6-112">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="176c6-112">Select **New**.</span></span>

3. <span data-ttu-id="176c6-113">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="176c6-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="176c6-114">Поле</span><span class="sxs-lookup"><span data-stu-id="176c6-114">Field</span></span> | <span data-ttu-id="176c6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="176c6-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="176c6-116">**Параметр покрытия**</span><span class="sxs-lookup"><span data-stu-id="176c6-116">**Coverage option**</span></span> | <span data-ttu-id="176c6-117">Уникальное имя параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="176c6-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="176c6-118">**Description**</span></span> | <span data-ttu-id="176c6-119">Описание параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="176c6-120">**Код покрытия**</span><span class="sxs-lookup"><span data-stu-id="176c6-120">**Coverage code**</span></span> | <span data-ttu-id="176c6-121">Коды покрытия присваивают минимальные и максимальные суммы для каждого допустимого типа лица с покрытием.</span><span class="sxs-lookup"><span data-stu-id="176c6-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="176c6-122">Код покрытия показывает, кто охватывается или сумму покрытия, разрешенную для типа плана.</span><span class="sxs-lookup"><span data-stu-id="176c6-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="176c6-123">Сумму покрытия можно выразить как сумму в валюте или как процент.</span><span class="sxs-lookup"><span data-stu-id="176c6-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="176c6-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="176c6-124">For example:</span></span></br></br><span data-ttu-id="176c6-125">- **Emp+1** — для успешной квалификации, необходимо, чтобы у сотрудника был выбран один иждивенец (если выбрано несколько, квалификация отменяется).</span><span class="sxs-lookup"><span data-stu-id="176c6-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="176c6-126">- **Emp+family**— для успешной квалификации у сотрудника должен быть по крайней мере два выбранных иждивенца.</span><span class="sxs-lookup"><span data-stu-id="176c6-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="176c6-127">**Максимальное число**</span><span class="sxs-lookup"><span data-stu-id="176c6-127">**Maximum number**</span></span> | <span data-ttu-id="176c6-128">Максимальное число иждивенцев.</span><span class="sxs-lookup"><span data-stu-id="176c6-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="176c6-129">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="176c6-129">**Status**</span></span> | <span data-ttu-id="176c6-130">Статус параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-130">The status of the coverage option.</span></span> <span data-ttu-id="176c6-131">Если для статуса параметра покрытия выбрано "неактивный", параметр покрытия не может быть выбран в типах планов.</span><span class="sxs-lookup"><span data-stu-id="176c6-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="176c6-132">**Процент**</span><span class="sxs-lookup"><span data-stu-id="176c6-132">**Percent**</span></span> | <span data-ttu-id="176c6-133">Сумма процента.</span><span class="sxs-lookup"><span data-stu-id="176c6-133">The percent amount.</span></span> <span data-ttu-id="176c6-134">Это поле активно, только если выбрано % x зарплаты в поле "Код покрытия".</span><span class="sxs-lookup"><span data-stu-id="176c6-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="176c6-135">**Делитель**</span><span class="sxs-lookup"><span data-stu-id="176c6-135">**Divisor**</span></span> | <span data-ttu-id="176c6-136">Делитель, используемый в расчете при выборе кода покрытия % x зарплаты.</span><span class="sxs-lookup"><span data-stu-id="176c6-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="176c6-137">**Минимальный процент**</span><span class="sxs-lookup"><span data-stu-id="176c6-137">**Percent minimum**</span></span> | <span data-ttu-id="176c6-138">Минимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="176c6-139">**Максимальный процент**</span><span class="sxs-lookup"><span data-stu-id="176c6-139">**Percent maximum**</span></span> | <span data-ttu-id="176c6-140">Максимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="176c6-141">В **Параметры допустимости личного контакта** приложите соответствующий параметр допустимости личного контакта для каждого параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="176c6-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="176c6-142">В **Дистанционное обслуживание** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="176c6-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="176c6-143">Поле</span><span class="sxs-lookup"><span data-stu-id="176c6-143">Field</span></span> | <span data-ttu-id="176c6-144">Описание</span><span class="sxs-lookup"><span data-stu-id="176c6-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="176c6-145">**Разрешить сумму взноса сотрудника**</span><span class="sxs-lookup"><span data-stu-id="176c6-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="176c6-146">Указывает, разрешено ли сотрудникам изменять сумму вклада в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="176c6-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="176c6-147">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы вклада, которую сотрудник введет в систему дистанционного обслуживания льгот.</span><span class="sxs-lookup"><span data-stu-id="176c6-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="176c6-148">**Разрешить сумму покрытия сотрудника**</span><span class="sxs-lookup"><span data-stu-id="176c6-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="176c6-149">Указывает, разрешено ли сотрудникам изменять сумму покрытия в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="176c6-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="176c6-150">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы покрытия, которую сотрудник введет в систему дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="176c6-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="176c6-151">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="176c6-151">Select **Save**.</span></span> 
