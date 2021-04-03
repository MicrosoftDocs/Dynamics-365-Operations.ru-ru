---
title: Задание управления льготами и параметров самообслуживания сотрудников для всех компаний
description: Настройте параметры для управления льготами и самообслуживания сотрудников в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: 5e241475c9652ab2dafe6886479e9c0a93711aca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466768"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="48437-103">Задание управления льготами и параметров самообслуживания сотрудников для всех компаний</span><span class="sxs-lookup"><span data-stu-id="48437-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48437-104">Прежде чем можно будет настроить планы льгот в Microsoft Dynamics 365 Human Resources, необходимо настроить параметры управления льготами.</span><span class="sxs-lookup"><span data-stu-id="48437-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="48437-105">Эти параметры определяют значения по умолчанию, коды причин и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="48437-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="48437-106">Настройка общих параметров</span><span class="sxs-lookup"><span data-stu-id="48437-106">Configure general parameters</span></span>

1. <span data-ttu-id="48437-107">В рабочей области **Управление льготами** в **Настройка** выберите **Общие параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="48437-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="48437-108">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="48437-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="48437-109">Поле</span><span class="sxs-lookup"><span data-stu-id="48437-109">Field</span></span> | <span data-ttu-id="48437-110">описание</span><span class="sxs-lookup"><span data-stu-id="48437-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="48437-111">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="48437-111">**Country/region**</span></span> | <span data-ttu-id="48437-112">Поле **Страна/регион** определяет порядок отображения почтовых индексов/регионов.</span><span class="sxs-lookup"><span data-stu-id="48437-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="48437-113">Выбранная страна/регион отображается сначала в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="48437-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="48437-114">**Код основания регистрации**</span><span class="sxs-lookup"><span data-stu-id="48437-114">**Enrollment reason code**</span></span> | <span data-ttu-id="48437-115">Выберите код причины по умолчанию для использования при создании планов сотрудников во время обработки открытой регистрации.</span><span class="sxs-lookup"><span data-stu-id="48437-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="48437-116">**Код основания отмены**</span><span class="sxs-lookup"><span data-stu-id="48437-116">**Cancellation reason code**</span></span> | <span data-ttu-id="48437-117">Код причины, который будет использоваться при отмене плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="48437-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="48437-118">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="48437-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="48437-119">При необходимости пользователи могут изменить **Код причины отмены**.</span><span class="sxs-lookup"><span data-stu-id="48437-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="48437-120">**Повторное открытие кода основания**</span><span class="sxs-lookup"><span data-stu-id="48437-120">**Reopen reason code**</span></span> | <span data-ttu-id="48437-121">Код причины, который будет использоваться при повторном открытии плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="48437-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="48437-122">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="48437-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="48437-123">При необходимости пользователи могут изменить **Код причины повторного открытия**.</span><span class="sxs-lookup"><span data-stu-id="48437-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="48437-124">**Код основания жизненного события**</span><span class="sxs-lookup"><span data-stu-id="48437-124">**Life event reason code**</span></span> | <span data-ttu-id="48437-125">Код причины, используемый при происхождении жизненного события.</span><span class="sxs-lookup"><span data-stu-id="48437-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="48437-126">**Код основания изменения ставки**</span><span class="sxs-lookup"><span data-stu-id="48437-126">**Rate change reason code**</span></span> | <span data-ttu-id="48437-127">Код причины для использования при отмене и повторном открытии плана льгот сотрудника в процессе обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="48437-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="48437-128">Он указывает, какие записи были изменены процессом обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="48437-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="48437-129">**Годовая зарплата для льгот**</span><span class="sxs-lookup"><span data-stu-id="48437-129">**Benefits annual salary**</span></span> | <span data-ttu-id="48437-130">Позволяет настроить сумму **Годовая зарплата льгот** для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="48437-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="48437-131">Модуль Human Resources использует сумму **Годовая зарплата льгот** при определении сумм покрытия вместо годовой суммы по фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="48437-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="48437-132">**Новые подходящие работники**</span><span class="sxs-lookup"><span data-stu-id="48437-132">**New hire eligible**</span></span> | <span data-ttu-id="48437-133">Указывает, является ли новый наем допустимым.</span><span class="sxs-lookup"><span data-stu-id="48437-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="48437-134">**Период регистрации нового набора сотрудников**</span><span class="sxs-lookup"><span data-stu-id="48437-134">**New hire enrollment period**</span></span> | <span data-ttu-id="48437-135">Период времени, в течение которого разрешается новая регистрация для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="48437-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="48437-136">**Примечание**. Этот параметр переопределяет любой новый период регистрации найма, установленный для правила допустимости плана.</span><span class="sxs-lookup"><span data-stu-id="48437-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="48437-137">**Частота платежей по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="48437-137">**Default pay frequency**</span></span> | <span data-ttu-id="48437-138">Частота платежей по умолчанию, используемая при добавлении новых работников.</span><span class="sxs-lookup"><span data-stu-id="48437-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="48437-139">**Включены жизненные события**</span><span class="sxs-lookup"><span data-stu-id="48437-139">**Life events enabled**</span></span> | <span data-ttu-id="48437-140">Включает жизненные события.</span><span class="sxs-lookup"><span data-stu-id="48437-140">Enables life events.</span></span> |
   | <span data-ttu-id="48437-141">**Скрыть старые формы льгот**</span><span class="sxs-lookup"><span data-stu-id="48437-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="48437-142">Позволяет скрыть устаревшие формы льготы.</span><span class="sxs-lookup"><span data-stu-id="48437-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="48437-143">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="48437-143">**Benefit verification**</span></span> | <span data-ttu-id="48437-144">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="48437-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="48437-145">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="48437-145">**Auto select designees**</span></span> | <span data-ttu-id="48437-146">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="48437-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="48437-147">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="48437-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="48437-148">Настройка параметров самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="48437-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="48437-149">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="48437-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="48437-150">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="48437-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="48437-151">Поле</span><span class="sxs-lookup"><span data-stu-id="48437-151">Field</span></span> | <span data-ttu-id="48437-152">описание</span><span class="sxs-lookup"><span data-stu-id="48437-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="48437-153">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="48437-153">**Benefit verification**</span></span> | <span data-ttu-id="48437-154">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="48437-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="48437-155">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="48437-155">**Auto select designees**</span></span> | <span data-ttu-id="48437-156">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="48437-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="48437-157">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="48437-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]