---
title: Настройка параметров управления льготами
description: Настройка параметров управления льготами в Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229771"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="155d1-103">Настройка параметров управления льготами</span><span class="sxs-lookup"><span data-stu-id="155d1-103">Set Benefits management parameters</span></span>

<span data-ttu-id="155d1-104">Прежде чем можно будет настроить планы отпусков в Microsoft Dynamics 365 Human Resources, необходимо настроить параметры управления льготами.</span><span class="sxs-lookup"><span data-stu-id="155d1-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="155d1-105">Эти параметры определяют значения по умолчанию, коды причин и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="155d1-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="155d1-106">Настройка общих параметров</span><span class="sxs-lookup"><span data-stu-id="155d1-106">Configure general parameters</span></span>

1. <span data-ttu-id="155d1-107">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="155d1-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="155d1-108">На вкладке **Общие** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="155d1-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="155d1-109">Поле</span><span class="sxs-lookup"><span data-stu-id="155d1-109">Field</span></span> | <span data-ttu-id="155d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="155d1-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="155d1-111">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="155d1-111">**Country/region**</span></span> | <span data-ttu-id="155d1-112">Поле **Страна/регион** определяет порядок отображения почтовых индексов/регионов.</span><span class="sxs-lookup"><span data-stu-id="155d1-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="155d1-113">Выбранная страна отображается сначала в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="155d1-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="155d1-114">**Код основания регистрации**</span><span class="sxs-lookup"><span data-stu-id="155d1-114">**Enrollment reason code**</span></span> | <span data-ttu-id="155d1-115">Выберите код причины по умолчанию для использования при создании планов сотрудников во время обработки открытой регистрации.</span><span class="sxs-lookup"><span data-stu-id="155d1-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="155d1-116">**Код основания отмены**</span><span class="sxs-lookup"><span data-stu-id="155d1-116">**Cancellation reason code**</span></span> | <span data-ttu-id="155d1-117">Код причины, который будет использоваться при отмене плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="155d1-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="155d1-118">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="155d1-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="155d1-119">При необходимости пользователи могут изменить **Код причины отмены**.</span><span class="sxs-lookup"><span data-stu-id="155d1-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="155d1-120">**Повторное открытие кода основания**</span><span class="sxs-lookup"><span data-stu-id="155d1-120">**Reopen reason code**</span></span> | <span data-ttu-id="155d1-121">Код причины, который будет использоваться при повторном открытии плана льготы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="155d1-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="155d1-122">Во время процесса отмены отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="155d1-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="155d1-123">При необходимости пользователи могут изменить **Код причины повторного открытия**.</span><span class="sxs-lookup"><span data-stu-id="155d1-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="155d1-124">**Код основания жизненного события**</span><span class="sxs-lookup"><span data-stu-id="155d1-124">**Life event reason code**</span></span> | <span data-ttu-id="155d1-125">Код причины, используемый при происхождении жизненного события.</span><span class="sxs-lookup"><span data-stu-id="155d1-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="155d1-126">**Код основания изменения ставки**</span><span class="sxs-lookup"><span data-stu-id="155d1-126">**Rate change reason code**</span></span> | <span data-ttu-id="155d1-127">Код причины для использования при отмене и повторном открытии плана льгот сотрудника в процессе обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="155d1-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="155d1-128">Он указывает, какие записи были изменены процессом обновления изменения ставки.</span><span class="sxs-lookup"><span data-stu-id="155d1-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="155d1-129">**Новые подходящие работники**</span><span class="sxs-lookup"><span data-stu-id="155d1-129">**New hire eligible**</span></span> | <span data-ttu-id="155d1-130">Указывает, является ли новый наем допустимым.</span><span class="sxs-lookup"><span data-stu-id="155d1-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="155d1-131">**Период регистрации нового набора сотрудников**</span><span class="sxs-lookup"><span data-stu-id="155d1-131">**New hire enrollment period**</span></span> | <span data-ttu-id="155d1-132">Период времени, в течение которого разрешается новая регистрация для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="155d1-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="155d1-133">**Примечание**. Этот параметр переопределяет любой новый период регистрации найма, установленный для правила допустимости плана.</span><span class="sxs-lookup"><span data-stu-id="155d1-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="155d1-134">**Включены жизненные события**</span><span class="sxs-lookup"><span data-stu-id="155d1-134">**Life events enabled**</span></span> | <span data-ttu-id="155d1-135">Включает жизненные события.</span><span class="sxs-lookup"><span data-stu-id="155d1-135">Enables life events.</span></span> |
   | <span data-ttu-id="155d1-136">**Скрыть старые формы льгот**</span><span class="sxs-lookup"><span data-stu-id="155d1-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="155d1-137">Позволяет скрыть устаревшие формы льготы.</span><span class="sxs-lookup"><span data-stu-id="155d1-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="155d1-138">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="155d1-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="155d1-139">Настройка параметров дистанционного обслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="155d1-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="155d1-140">В рабочей области **Управление льготами** в разделе **Настройка** выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="155d1-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="155d1-141">На вкладке **Дистанционное обслуживание сотрудников** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="155d1-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="155d1-142">Поле</span><span class="sxs-lookup"><span data-stu-id="155d1-142">Field</span></span> | <span data-ttu-id="155d1-143">Описание</span><span class="sxs-lookup"><span data-stu-id="155d1-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="155d1-144">**Проверка льготы**</span><span class="sxs-lookup"><span data-stu-id="155d1-144">**Benefit verification**</span></span> | <span data-ttu-id="155d1-145">Проверочный текст, который будет использоваться при выписке льгот средствами самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="155d1-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="155d1-146">**Автоматически выбирать кандидатов на получение льготы**</span><span class="sxs-lookup"><span data-stu-id="155d1-146">**Auto select designees**</span></span> | <span data-ttu-id="155d1-147">Указывает, следует ли автоматически выбирать иждивенцев и бенефициаров в соответствии с их допустимостью для параметров плана.</span><span class="sxs-lookup"><span data-stu-id="155d1-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="155d1-148">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="155d1-148">Select **Save**.</span></span>
