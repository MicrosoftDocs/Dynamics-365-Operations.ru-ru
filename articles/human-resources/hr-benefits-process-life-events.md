---
title: Обработка жизненных событий
description: Во время жизненного цикла сотрудников в Microsoft Dynamics 365 Human Resources каждый сотрудник может столкнуться с различными изменениями жизненных событий.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cfb0fc54e3904655cea0c795a46c540bd2a529a2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466262"
---
# <a name="process-life-events"></a><span data-ttu-id="4d60c-103">Обработка жизненных событий</span><span class="sxs-lookup"><span data-stu-id="4d60c-103">Process life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d60c-104">Во время жизненного цикла сотрудников в Microsoft Dynamics 365 Human Resources каждый сотрудник может столкнуться с различными изменениями жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="4d60c-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="4d60c-105">Например, свадьба, изменение трудоустройства или изменение иждивенца/бенефициара.</span><span class="sxs-lookup"><span data-stu-id="4d60c-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="4d60c-106">Для использования жизненных событий необходимо включить жизненные события в форме параметров льгот, настроить типы жизненных событий, а также настроить параметры жизненных событий для типов планов.</span><span class="sxs-lookup"><span data-stu-id="4d60c-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="4d60c-107">Прежде чем обрабатывать жизненные события, необходимо запустить открытую регистрацию как минимум один раз во время найма на работу.</span><span class="sxs-lookup"><span data-stu-id="4d60c-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="4d60c-108">В США открытая регистрация обычно выполняется раз в год.</span><span class="sxs-lookup"><span data-stu-id="4d60c-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="4d60c-109">За пределами США открытая регистрация может выполняться во время найма.</span><span class="sxs-lookup"><span data-stu-id="4d60c-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="4d60c-110">Работнику не нужно выбирать план льгот для обработки жизненных событий, но они должны быть включены в открытую обработку регистрации.</span><span class="sxs-lookup"><span data-stu-id="4d60c-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="4d60c-111">При наличии работников с жизненными событиями, которые выполняются на будущую дату, используйте обработку жизненных событий.</span><span class="sxs-lookup"><span data-stu-id="4d60c-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="4d60c-112">Это событие будет обрабатывать все необработанные жизненные события, которые не были обработаны (такие как будущие жизненные события или добавленные жизненные события, которые не относятся к сотрудникам, например новая льгота).</span><span class="sxs-lookup"><span data-stu-id="4d60c-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="4d60c-113">Жизненные события реального времени являются скрытыми.</span><span class="sxs-lookup"><span data-stu-id="4d60c-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="4d60c-114">Например, если сегодня 1 февраля, а 14 февраля для работника Joe Smith планируется изменить юридические лица, то при выполнении обработки жизненного события на 15 февраля система обрабатывает все события до 15 февраля.</span><span class="sxs-lookup"><span data-stu-id="4d60c-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="4d60c-115">В рабочей области **Управление льготами** в **Обработка** выберите **Обработка жизненных событий**.</span><span class="sxs-lookup"><span data-stu-id="4d60c-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="4d60c-116">В диалоговом окне **Выполнение процесса жизненного события** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="4d60c-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="4d60c-117">Поле</span><span class="sxs-lookup"><span data-stu-id="4d60c-117">Field</span></span> | <span data-ttu-id="4d60c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4d60c-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d60c-119">**Период регистрации**</span><span class="sxs-lookup"><span data-stu-id="4d60c-119">**Enrollment period**</span></span> | <span data-ttu-id="4d60c-120">Период регистрации, для которого необходимо обработать жизненные события.</span><span class="sxs-lookup"><span data-stu-id="4d60c-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="4d60c-121">**Информация о компании**</span><span class="sxs-lookup"><span data-stu-id="4d60c-121">**Legal entity**</span></span> | <span data-ttu-id="4d60c-122">Юридическое лицо, для которого необходимо обработать жизненные события.</span><span class="sxs-lookup"><span data-stu-id="4d60c-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="4d60c-123">**Дата жизненного события**</span><span class="sxs-lookup"><span data-stu-id="4d60c-123">**Life event date**</span></span> | <span data-ttu-id="4d60c-124">Система обрабатывает все события в течение периода регистрации, которые выполняются до этой даты.</span><span class="sxs-lookup"><span data-stu-id="4d60c-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="4d60c-125">**Рабочий**</span><span class="sxs-lookup"><span data-stu-id="4d60c-125">**Worker**</span></span> | <span data-ttu-id="4d60c-126">Работник, для которого необходимо обработать жизненные события.</span><span class="sxs-lookup"><span data-stu-id="4d60c-126">The worker to process life events for.</span></span> <span data-ttu-id="4d60c-127">Если оставить это поле пустым, жизненные события будут обработаны для всех работников.</span><span class="sxs-lookup"><span data-stu-id="4d60c-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="4d60c-128">Если необходимо выполнить процесс в фоновом режиме, выберите **Выполнить в фоновом режиме** и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4d60c-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="4d60c-129">Введите сведения для процесса.</span><span class="sxs-lookup"><span data-stu-id="4d60c-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="4d60c-130">Чтобы настроить повторяющееся задание, выберите **Повторение**, введите сведения о повторении, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d60c-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="4d60c-131">Чтобы настроить оповещение о заданиях, выберите **Оповещения**, выберите получаемые оповещения и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d60c-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="4d60c-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d60c-132">Select **OK**.</span></span> <span data-ttu-id="4d60c-133">Процесс будет выполнен с заданными вами параметрами.</span><span class="sxs-lookup"><span data-stu-id="4d60c-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="4d60c-134">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d60c-134">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]