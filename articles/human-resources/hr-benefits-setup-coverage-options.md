---
title: Создание параметров покрытия
description: Параметры покрытия в Microsoft Dynamics 365 Human Resources представляют собой уровни покрытия для выбора участника в плане или программе льгот, например "только сотрудник" только для медицинских планов, или заработная плата 2x плана страхования жизни.
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092714"
---
# <a name="create-coverage-options"></a><span data-ttu-id="f37c9-103">Создание параметров покрытия</span><span class="sxs-lookup"><span data-stu-id="f37c9-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f37c9-104">Параметры покрытия в Microsoft Dynamics 365 Human Resources представляют собой уровни покрытия для выбора участника в плане или программе льгот, например "только сотрудник" только для медицинских планов, или заработная плата 2x плана страхования жизни.</span><span class="sxs-lookup"><span data-stu-id="f37c9-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="f37c9-105">После определения параметры покрытия льгот повторно используются и можно связать параметр с одним или несколькими планами.</span><span class="sxs-lookup"><span data-stu-id="f37c9-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="f37c9-106">После определения параметров покрытия приложите параметры покрытия к типу плана льгот.</span><span class="sxs-lookup"><span data-stu-id="f37c9-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="f37c9-107">Этот тип плана затем связывается с планом льгот или программой.</span><span class="sxs-lookup"><span data-stu-id="f37c9-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="f37c9-108">Параметры покрытия, связанные с типом плана, будут доступны для всех планов, созданных с этим типом плана.</span><span class="sxs-lookup"><span data-stu-id="f37c9-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="f37c9-109">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Параметры покрытия**.</span><span class="sxs-lookup"><span data-stu-id="f37c9-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="f37c9-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f37c9-110">Select **New**.</span></span>

3. <span data-ttu-id="f37c9-111">Укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="f37c9-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f37c9-112">Поле</span><span class="sxs-lookup"><span data-stu-id="f37c9-112">Field</span></span> | <span data-ttu-id="f37c9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f37c9-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f37c9-114">**Параметр покрытия**</span><span class="sxs-lookup"><span data-stu-id="f37c9-114">**Coverage option**</span></span> | <span data-ttu-id="f37c9-115">Уникальное имя параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="f37c9-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f37c9-116">**Description**</span></span> | <span data-ttu-id="f37c9-117">Описание параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="f37c9-118">**Код покрытия**</span><span class="sxs-lookup"><span data-stu-id="f37c9-118">**Coverage code**</span></span> | <span data-ttu-id="f37c9-119">Коды покрытия присваивают минимальные и максимальные суммы для каждого допустимого типа лица с покрытием.</span><span class="sxs-lookup"><span data-stu-id="f37c9-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="f37c9-120">Код покрытия показывает, кто охватывается или сумму покрытия, разрешенную для типа плана.</span><span class="sxs-lookup"><span data-stu-id="f37c9-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="f37c9-121">Сумму покрытия можно выразить как сумму в валюте или как процент.</span><span class="sxs-lookup"><span data-stu-id="f37c9-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="f37c9-122">Пример:</span><span class="sxs-lookup"><span data-stu-id="f37c9-122">For example:</span></span></br></br><span data-ttu-id="f37c9-123">- **Emp+1** — для успешной квалификации, необходимо, чтобы у сотрудника был выбран один иждивенец (если выбрано несколько, квалификация отменяется).</span><span class="sxs-lookup"><span data-stu-id="f37c9-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="f37c9-124">- **Emp+family**— для успешной квалификации у сотрудника должен быть по крайней мере два выбранных иждивенца.</span><span class="sxs-lookup"><span data-stu-id="f37c9-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="f37c9-125">**Максимальное число**</span><span class="sxs-lookup"><span data-stu-id="f37c9-125">**Maximum number**</span></span> | <span data-ttu-id="f37c9-126">Максимальное число иждивенцев.</span><span class="sxs-lookup"><span data-stu-id="f37c9-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="f37c9-127">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f37c9-127">**Status**</span></span> | <span data-ttu-id="f37c9-128">Статус параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-128">The status of the coverage option.</span></span> <span data-ttu-id="f37c9-129">Если для статуса параметра покрытия выбрано "неактивный", параметр покрытия не может быть выбран в типах планов.</span><span class="sxs-lookup"><span data-stu-id="f37c9-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="f37c9-130">**Процент**</span><span class="sxs-lookup"><span data-stu-id="f37c9-130">**Percent**</span></span> | <span data-ttu-id="f37c9-131">Сумма процента.</span><span class="sxs-lookup"><span data-stu-id="f37c9-131">The percent amount.</span></span> <span data-ttu-id="f37c9-132">Это поле активно, только если выбрано % x зарплаты в поле "Код покрытия".</span><span class="sxs-lookup"><span data-stu-id="f37c9-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="f37c9-133">**Делитель**</span><span class="sxs-lookup"><span data-stu-id="f37c9-133">**Divisor**</span></span> | <span data-ttu-id="f37c9-134">Делитель, используемый в расчете при выборе кода покрытия % x зарплаты.</span><span class="sxs-lookup"><span data-stu-id="f37c9-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="f37c9-135">**Минимальный процент**</span><span class="sxs-lookup"><span data-stu-id="f37c9-135">**Percent minimum**</span></span> | <span data-ttu-id="f37c9-136">Минимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="f37c9-137">**Максимальный процент**</span><span class="sxs-lookup"><span data-stu-id="f37c9-137">**Percent maximum**</span></span> | <span data-ttu-id="f37c9-138">Максимальный процент при выборе кода процентного покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="f37c9-139">В **Параметры допустимости личного контакта** приложите соответствующий параметр допустимости личного контакта для каждого параметра покрытия.</span><span class="sxs-lookup"><span data-stu-id="f37c9-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="f37c9-140">В **Дистанционное обслуживание** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="f37c9-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="f37c9-141">Поле</span><span class="sxs-lookup"><span data-stu-id="f37c9-141">Field</span></span> | <span data-ttu-id="f37c9-142">Описание</span><span class="sxs-lookup"><span data-stu-id="f37c9-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f37c9-143">**Разрешить сумму взноса сотрудника**</span><span class="sxs-lookup"><span data-stu-id="f37c9-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="f37c9-144">Указывает, разрешено ли сотрудникам изменять сумму вклада в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="f37c9-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f37c9-145">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы вклада, которую сотрудник введет в систему дистанционного обслуживания льгот.</span><span class="sxs-lookup"><span data-stu-id="f37c9-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="f37c9-146">**Разрешить сумму покрытия сотрудника**</span><span class="sxs-lookup"><span data-stu-id="f37c9-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="f37c9-147">Указывает, разрешено ли сотрудникам изменять сумму покрытия в системе дистанционного обслуживания льгот при выборе льгот.</span><span class="sxs-lookup"><span data-stu-id="f37c9-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f37c9-148">Если установить этот флажок, система вычислит параметры плана льготы на основе суммы покрытия, которую сотрудник введет в систему дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="f37c9-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="f37c9-149">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f37c9-149">Select **Save**.</span></span> 
