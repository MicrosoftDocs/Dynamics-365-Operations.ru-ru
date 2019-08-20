---
title: Создание пакетного задания
description: Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851295"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="4740f-103">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="4740f-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4740f-104">Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.</span><span class="sxs-lookup"><span data-stu-id="4740f-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="4740f-105">Пакетные задания выполняются с использованием параметров доступа пользователя, создавшего задание.</span><span class="sxs-lookup"><span data-stu-id="4740f-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="4740f-106">Следующая процедура используется для создания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="4740f-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="4740f-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="4740f-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="4740f-108">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="4740f-108">Create the batch job</span></span>
1. <span data-ttu-id="4740f-109">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="4740f-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="4740f-110">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4740f-110">Click **New**.</span></span>
3. <span data-ttu-id="4740f-111">В поле **Описание задания** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4740f-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="4740f-112">В поле **Запланированные дата/время начала** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="4740f-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="4740f-113">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="4740f-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="4740f-114">Создание повторения</span><span class="sxs-lookup"><span data-stu-id="4740f-114">Create a recurrence</span></span>
1. <span data-ttu-id="4740f-115">В области действий щелкните **Пакетное задание**.</span><span class="sxs-lookup"><span data-stu-id="4740f-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="4740f-116">Щелкните **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="4740f-116">Click **Recurrence**.</span></span> <span data-ttu-id="4740f-117">Эти параметры используются для ввода диапазона и схемы повторения.</span><span class="sxs-lookup"><span data-stu-id="4740f-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="4740f-118">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4740f-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="4740f-119">Добавление оповещений</span><span class="sxs-lookup"><span data-stu-id="4740f-119">Add alerts</span></span>
1. <span data-ttu-id="4740f-120">В области действий щелкните **Пакетное задание**.</span><span class="sxs-lookup"><span data-stu-id="4740f-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="4740f-121">Щелкните **Оповещения**.</span><span class="sxs-lookup"><span data-stu-id="4740f-121">Click **Alerts**.</span></span> <span data-ttu-id="4740f-122">Укажите, требуется ли отправлять оповещения по завершении пакетного задания, в случае ошибки или отмены.</span><span class="sxs-lookup"><span data-stu-id="4740f-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="4740f-123">Затем укажите, требуется ли отображать оповещения в виде всплывающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="4740f-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="4740f-124">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4740f-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="4740f-125">Настройка статуса пакетного задания</span><span class="sxs-lookup"><span data-stu-id="4740f-125">Adjust batch job status</span></span>
1. <span data-ttu-id="4740f-126">Перейдите в раздел **Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="4740f-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="4740f-127">Выберите соответствующее пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="4740f-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="4740f-128">В области действий щелкните **Пакетное задание > Функции > Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="4740f-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="4740f-129">Выберите соответствующий статус.</span><span class="sxs-lookup"><span data-stu-id="4740f-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="4740f-130">**Отложено**: задавайте пакетное задание как **отложено**, чтобы оно откладывалось планировщиком пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="4740f-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="4740f-131">Эквивалентно *остановке*.</span><span class="sxs-lookup"><span data-stu-id="4740f-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="4740f-132">**Ожидание**: установите пакетное задание как **ожидание**, чтобы оно ожидало обработки планировщиком пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="4740f-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="4740f-133">Эквивалентно *запуску*.</span><span class="sxs-lookup"><span data-stu-id="4740f-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="4740f-134">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4740f-134">Click **OK**.</span></span>
