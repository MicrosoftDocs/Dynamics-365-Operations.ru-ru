---
title: Настройка параметров управления льготами
description: Настройка параметров управления льготами в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 07/16/2020
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
ms.openlocfilehash: cb9dd6eb8ef840dab54eabab8526200a3a8e21f0
ms.sourcegitcommit: e100c1c7c8dcdacf066defc206dd2f44b8ce6100
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "4057036"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="ba313-103">Настройка параметров управления льготами</span><span class="sxs-lookup"><span data-stu-id="ba313-103">Set Benefits management parameters</span></span>

<span data-ttu-id="ba313-104">Прежде чем можно будет настроить планы отпусков в Microsoft Dynamics 365 Human Resources, необходимо настроить параметры управления льготами.</span><span class="sxs-lookup"><span data-stu-id="ba313-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="ba313-105">Эти параметры определяют значения по умолчанию, коды причин и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="ba313-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="ba313-106">Настройка общих параметров</span><span class="sxs-lookup"><span data-stu-id="ba313-106">Configure general parameters</span></span>

1. <span data-ttu-id="ba313-107">В рабочей области **Управление льготами** в **Настройка** выберите **Общие параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ba313-107">In the **Benefits management** workspace, under **Setup** , select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="ba313-108">На вкладке **Общие** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="ba313-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ba313-109">Поле</span><span class="sxs-lookup"><span data-stu-id="ba313-109">Field</span></span> | <span data-ttu-id="ba313-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba313-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ba313-111">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="ba313-111">**Country/region**</span></span> | <span data-ttu-id="ba313-112">Поле **Страна/регион** определяет порядок отображения почтовых индексов/регионов.</span><span class="sxs-lookup"><span data-stu-id="ba313-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="ba313-113">Выбранная страна/регион отображается сначала в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="ba313-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="ba313-114">**Код основания регистрации**</span><span class="sxs-lookup"><span data-stu-id="ba313-114">**Enrollment reason code**</span></span> | <span data-ttu-id="ba313-115">Выберите код причины по умолчанию для использования при создании планов сотрудников во время обработки открытой регистрации.</span><span class="sxs-lookup"><span data-stu-id="ba313-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="ba313-116">**Код основания отмены**</span><span class="sxs-lookup"><span data-stu-id="ba313-116">**Cancellation reason code**</span></span> | <span data-ttu-id="ba313-117">Код причины, который будет использоваться при отмене плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ba313-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="ba313-118">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ba313-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ba313-119">При необходимости пользователи могут изменить **Код причины отмены**.</span><span class="sxs-lookup"><span data-stu-id="ba313-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="ba313-120">**Повторное открытие кода основания**</span><span class="sxs-lookup"><span data-stu-id="ba313-120">**Reopen reason code**</span></span> | <span data-ttu-id="ba313-121">Код причины, который будет использоваться при повторном открытии плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ba313-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="ba313-122">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ba313-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ba313-123">При необходимости пользователи могут изменить **Код причины повторного открытия**.</span><span class="sxs-lookup"><span data-stu-id="ba313-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="ba313-124">**Код основания жизненного события**</span><span class="sxs-lookup"><span data-stu-id="ba313-124">**Life event reason code**</span></span> | <span data-ttu-id="ba313-125">Код причины, используемый при происхождении жизненного события.</span><span class="sxs-lookup"><span data-stu-id="ba313-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="ba313-126">**Код основания изменения ставки**</span><span class="sxs-lookup"><span data-stu-id="ba313-126">**Rate change reason code**</span></span> | <span data-ttu-id="ba313-127">Код причины для использования при отмене и повторном открытии плана льгот сотрудника в процессе обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="ba313-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="ba313-128">Он указывает, какие записи были изменены процессом обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="ba313-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="ba313-129">**Годовая зарплата для льгот**</span><span class="sxs-lookup"><span data-stu-id="ba313-129">**Benefits annual salary**</span></span> | <span data-ttu-id="ba313-130">Позволяет настроить сумму **Годовая зарплата льгот** для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ba313-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="ba313-131">Модуль Human Resources использует сумму **Годовая зарплата льгот** при определении сумм покрытия вместо годовой суммы по фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="ba313-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="ba313-132">**Новые подходящие работники**</span><span class="sxs-lookup"><span data-stu-id="ba313-132">**New hire eligible**</span></span> | <span data-ttu-id="ba313-133">Указывает, является ли новый наем допустимым.</span><span class="sxs-lookup"><span data-stu-id="ba313-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="ba313-134">**Период регистрации нового набора сотрудников**</span><span class="sxs-lookup"><span data-stu-id="ba313-134">**New hire enrollment period**</span></span> | <span data-ttu-id="ba313-135">Период времени, в течение которого разрешается новая регистрация для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="ba313-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="ba313-136">**Примечание**. Этот параметр переопределяет любой новый период регистрации найма, установленный для правила допустимости плана.</span><span class="sxs-lookup"><span data-stu-id="ba313-136">**Note** : This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="ba313-137">**Частота платежей по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="ba313-137">**Default pay frequency**</span></span> | <span data-ttu-id="ba313-138">Частота платежей по умолчанию, используемая при добавлении новых работников.</span><span class="sxs-lookup"><span data-stu-id="ba313-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="ba313-139">**Включены жизненные события**</span><span class="sxs-lookup"><span data-stu-id="ba313-139">**Life events enabled**</span></span> | <span data-ttu-id="ba313-140">Включает жизненные события.</span><span class="sxs-lookup"><span data-stu-id="ba313-140">Enables life events.</span></span> |
   | <span data-ttu-id="ba313-141">**Скрыть старые формы льгот**</span><span class="sxs-lookup"><span data-stu-id="ba313-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="ba313-142">Позволяет скрыть устаревшие формы льготы.</span><span class="sxs-lookup"><span data-stu-id="ba313-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="ba313-143">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ba313-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="ba313-144">Настройка параметров дистанционного обслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="ba313-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="ba313-145">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ba313-145">In the **Benefits management** workspace, under **Setup** , select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="ba313-146">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="ba313-146">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ba313-147">Поле</span><span class="sxs-lookup"><span data-stu-id="ba313-147">Field</span></span> | <span data-ttu-id="ba313-148">описание</span><span class="sxs-lookup"><span data-stu-id="ba313-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ba313-149">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="ba313-149">**Benefit verification**</span></span> | <span data-ttu-id="ba313-150">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="ba313-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="ba313-151">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="ba313-151">**Auto select designees**</span></span> | <span data-ttu-id="ba313-152">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="ba313-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="ba313-153">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ba313-153">Select **Save**.</span></span>
