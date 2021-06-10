---
title: Задание управления льготами и параметров самообслуживания сотрудников для всех компаний
description: Настройте параметры для управления льготами и самообслуживания сотрудников в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d668238378e41287c7a9f845ae3e67078fc7776a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058976"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="e9a4b-103">Задание управления льготами и параметров самообслуживания сотрудников для всех компаний</span><span class="sxs-lookup"><span data-stu-id="e9a4b-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9a4b-104">Прежде чем можно будет настроить планы льгот в Microsoft Dynamics 365 Human Resources, необходимо настроить параметры управления льготами.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="e9a4b-105">Эти параметры определяют значения по умолчанию, коды причин и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="e9a4b-106">Настройка общих параметров</span><span class="sxs-lookup"><span data-stu-id="e9a4b-106">Configure general parameters</span></span>

1. <span data-ttu-id="e9a4b-107">В рабочей области **Управление льготами** в **Настройка** выберите **Общие параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="e9a4b-108">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="e9a4b-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="e9a4b-109">Поле</span><span class="sxs-lookup"><span data-stu-id="e9a4b-109">Field</span></span> | <span data-ttu-id="e9a4b-110">описание</span><span class="sxs-lookup"><span data-stu-id="e9a4b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e9a4b-111">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-111">**Country/region**</span></span> | <span data-ttu-id="e9a4b-112">Поле **Страна/регион** определяет порядок отображения почтовых индексов/регионов.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="e9a4b-113">Выбранная страна/регион отображается сначала в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="e9a4b-114">**Код основания регистрации**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-114">**Enrollment reason code**</span></span> | <span data-ttu-id="e9a4b-115">Выберите код причины по умолчанию для использования при создании планов сотрудников во время обработки открытой регистрации.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="e9a4b-116">**Код основания отмены**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-116">**Cancellation reason code**</span></span> | <span data-ttu-id="e9a4b-117">Код причины, который будет использоваться при отмене плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="e9a4b-118">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="e9a4b-119">При необходимости пользователи могут изменить **Код причины отмены**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="e9a4b-120">**Повторное открытие кода основания**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-120">**Reopen reason code**</span></span> | <span data-ttu-id="e9a4b-121">Код причины, который будет использоваться при повторном открытии плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="e9a4b-122">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="e9a4b-123">При необходимости пользователи могут изменить **Код причины повторного открытия**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="e9a4b-124">**Код основания жизненного события**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-124">**Life event reason code**</span></span> | <span data-ttu-id="e9a4b-125">Код причины, используемый при происхождении жизненного события.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="e9a4b-126">**Код основания изменения ставки**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-126">**Rate change reason code**</span></span> | <span data-ttu-id="e9a4b-127">Код причины для использования при отмене и повторном открытии плана льгот сотрудника в процессе обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="e9a4b-128">Он указывает, какие записи были изменены процессом обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="e9a4b-129">**Годовая зарплата для льгот**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-129">**Benefits annual salary**</span></span> | <span data-ttu-id="e9a4b-130">Позволяет настроить сумму **Годовая зарплата льгот** для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="e9a4b-131">Модуль Human Resources использует сумму **Годовая зарплата льгот** при определении сумм покрытия вместо годовой суммы по фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="e9a4b-132">**Новые подходящие работники**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-132">**New hire eligible**</span></span> | <span data-ttu-id="e9a4b-133">Указывает, является ли новый наем допустимым.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="e9a4b-134">**Период регистрации нового набора сотрудников**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-134">**New hire enrollment period**</span></span> | <span data-ttu-id="e9a4b-135">Период времени, в течение которого разрешается новая регистрация для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="e9a4b-136">**Примечание**. Этот параметр переопределяет любой новый период регистрации найма, установленный для правила допустимости плана.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="e9a4b-137">**Частота платежей по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-137">**Default pay frequency**</span></span> | <span data-ttu-id="e9a4b-138">Частота платежей по умолчанию, используемая при добавлении новых работников.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="e9a4b-139">**Включены жизненные события**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-139">**Life events enabled**</span></span> | <span data-ttu-id="e9a4b-140">Включает жизненные события.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-140">Enables life events.</span></span> |
   | <span data-ttu-id="e9a4b-141">**Скрыть старые формы льгот**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="e9a4b-142">Позволяет скрыть устаревшие формы льготы.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="e9a4b-143">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-143">**Benefit verification**</span></span> | <span data-ttu-id="e9a4b-144">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="e9a4b-145">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-145">**Auto select designees**</span></span> | <span data-ttu-id="e9a4b-146">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="e9a4b-147">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="e9a4b-148">Настройка параметров самообслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="e9a4b-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="e9a4b-149">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="e9a4b-150">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="e9a4b-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="e9a4b-151">Поле</span><span class="sxs-lookup"><span data-stu-id="e9a4b-151">Field</span></span> | <span data-ttu-id="e9a4b-152">описание</span><span class="sxs-lookup"><span data-stu-id="e9a4b-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e9a4b-153">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-153">**Benefit verification**</span></span> | <span data-ttu-id="e9a4b-154">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="e9a4b-155">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="e9a4b-155">**Auto select designees**</span></span> | <span data-ttu-id="e9a4b-156">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="e9a4b-157">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e9a4b-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]