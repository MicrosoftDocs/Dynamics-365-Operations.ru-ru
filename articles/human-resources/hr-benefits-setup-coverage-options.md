---
title: Создание параметров покрытия
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010280"
---
# <a name="create-coverage-options"></a><span data-ttu-id="264d0-102">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="264d0-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="264d0-103">Параметры покрытия в Microsoft Dynamics 365 Human Resources представляют собой уровни покрытия для выбора участника в плане или программе льгот, например "только сотрудник" только для медицинских планов, или заработная плата 2x плана страхования жизни.</span><span class="sxs-lookup"><span data-stu-id="264d0-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="264d0-104">После определения параметры покрытия льгот повторно используются и можно связать параметр с одним или несколькими планами.</span><span class="sxs-lookup"><span data-stu-id="264d0-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="264d0-105">После определения параметров покрытия приложите параметры покрытия к типу плана льгот.</span><span class="sxs-lookup"><span data-stu-id="264d0-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="264d0-106">Этот тип плана затем связывается с планом льгот или программой.</span><span class="sxs-lookup"><span data-stu-id="264d0-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="264d0-107">Параметры покрытия, связанные с типом плана, будут доступны для всех планов, созданных с этим типом плана.</span><span class="sxs-lookup"><span data-stu-id="264d0-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="264d0-108">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Параметры покрытия**.</span><span class="sxs-lookup"><span data-stu-id="264d0-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="264d0-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="264d0-109">Select **New**.</span></span>

3. <span data-ttu-id="264d0-110">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="264d0-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="264d0-111">Поле</span><span class="sxs-lookup"><span data-stu-id="264d0-111">Field</span></span> | <span data-ttu-id="264d0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="264d0-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="264d0-113">**Параметр покрытия**</span><span class="sxs-lookup"><span data-stu-id="264d0-113">**Coverage option**</span></span> | <span data-ttu-id="264d0-114">Уникальное имя параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="264d0-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="264d0-115">**Description**</span></span> | <span data-ttu-id="264d0-116">Описание параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="264d0-117">**Код покрытия**</span><span class="sxs-lookup"><span data-stu-id="264d0-117">**Coverage code**</span></span> | <span data-ttu-id="264d0-118">Коды покрытия присваивают минимальные и максимальные суммы для каждого допустимого типа лица с покрытием.</span><span class="sxs-lookup"><span data-stu-id="264d0-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="264d0-119">Код покрытия показывает, кто охватывается или сумму покрытия, разрешенную для типа плана.</span><span class="sxs-lookup"><span data-stu-id="264d0-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="264d0-120">Сумму покрытия можно выразить как сумму в валюте или как процент.</span><span class="sxs-lookup"><span data-stu-id="264d0-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="264d0-121">Пример:</span><span class="sxs-lookup"><span data-stu-id="264d0-121">For example:</span></span></br></br><span data-ttu-id="264d0-122">- **Emp+1** — для успешной квалификации, необходимо, чтобы у сотрудника был выбран один иждивенец (если выбрано несколько, квалификация отменяется).</span><span class="sxs-lookup"><span data-stu-id="264d0-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="264d0-123">- **Emp+family**— для успешной квалификации у сотрудника должен быть по крайней мере два выбранных иждивенца.</span><span class="sxs-lookup"><span data-stu-id="264d0-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="264d0-124">**Максимальное число**</span><span class="sxs-lookup"><span data-stu-id="264d0-124">**Maximum number**</span></span> | <span data-ttu-id="264d0-125">Максимальное число иждивенцев.</span><span class="sxs-lookup"><span data-stu-id="264d0-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="264d0-126">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="264d0-126">**Status**</span></span> | <span data-ttu-id="264d0-127">Статус параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-127">The status of the coverage option.</span></span> <span data-ttu-id="264d0-128">Если для статуса параметра покрытия выбрано "неактивный", параметр покрытия не может быть выбран в типах планов.</span><span class="sxs-lookup"><span data-stu-id="264d0-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="264d0-129">**Процент**</span><span class="sxs-lookup"><span data-stu-id="264d0-129">**Percent**</span></span> | <span data-ttu-id="264d0-130">Сумма процента.</span><span class="sxs-lookup"><span data-stu-id="264d0-130">The percent amount.</span></span> <span data-ttu-id="264d0-131">Это поле активно, только если выбрано % x зарплаты в поле "Код покрытия".</span><span class="sxs-lookup"><span data-stu-id="264d0-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="264d0-132">**Делитель**</span><span class="sxs-lookup"><span data-stu-id="264d0-132">**Divisor**</span></span> | <span data-ttu-id="264d0-133">Делитель, используемый в расчете при выборе кода покрытия % x зарплаты.</span><span class="sxs-lookup"><span data-stu-id="264d0-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="264d0-134">**Минимальный процент**</span><span class="sxs-lookup"><span data-stu-id="264d0-134">**Percent minimum**</span></span> | <span data-ttu-id="264d0-135">Минимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="264d0-136">**Максимальный процент**</span><span class="sxs-lookup"><span data-stu-id="264d0-136">**Percent maximum**</span></span> | <span data-ttu-id="264d0-137">Максимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="264d0-138">В **Параметры допустимости личного контакта** приложите соответствующий параметр допустимости личного контакта для каждого параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="264d0-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="264d0-139">В **Дистанционное обслуживание** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="264d0-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="264d0-140">Поле</span><span class="sxs-lookup"><span data-stu-id="264d0-140">Field</span></span> | <span data-ttu-id="264d0-141">Описание</span><span class="sxs-lookup"><span data-stu-id="264d0-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="264d0-142">**Разрешить сумму взноса сотрудника**</span><span class="sxs-lookup"><span data-stu-id="264d0-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="264d0-143">Указывает, разрешено ли сотрудникам изменять сумму вклада в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="264d0-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="264d0-144">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы вклада, которую сотрудник введет в систему дистанционного обслуживания льгот.</span><span class="sxs-lookup"><span data-stu-id="264d0-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="264d0-145">**Разрешить сумму покрытия сотрудника**</span><span class="sxs-lookup"><span data-stu-id="264d0-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="264d0-146">Указывает, разрешено ли сотрудникам изменять сумму покрытия в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="264d0-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="264d0-147">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы покрытия, которую сотрудник введет в систему дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="264d0-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="264d0-148">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="264d0-148">Select **Save**.</span></span> 
