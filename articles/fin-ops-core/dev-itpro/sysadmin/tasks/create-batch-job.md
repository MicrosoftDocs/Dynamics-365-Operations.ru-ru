---
title: Создание пакетного задания
description: Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.
author: maertenm
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f498014555e0beccbc8965dd43e5162944867978
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745869"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="5b97b-103">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="5b97b-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b97b-104">Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.</span><span class="sxs-lookup"><span data-stu-id="5b97b-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="5b97b-105">Пакетные задания выполняются с использованием параметров доступа пользователя, создавшего задание.</span><span class="sxs-lookup"><span data-stu-id="5b97b-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="5b97b-106">Следующая процедура используется для создания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="5b97b-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="5b97b-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5b97b-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="5b97b-108">Создание пакетного задания</span><span class="sxs-lookup"><span data-stu-id="5b97b-108">Create the batch job</span></span>
1. <span data-ttu-id="5b97b-109">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="5b97b-110">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-110">Click **New**.</span></span>
3. <span data-ttu-id="5b97b-111">В поле **Описание задания** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5b97b-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="5b97b-112">В поле **Запланированные дата/время начала** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="5b97b-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="5b97b-113">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="5b97b-114">Создание повторения</span><span class="sxs-lookup"><span data-stu-id="5b97b-114">Create a recurrence</span></span>
1. <span data-ttu-id="5b97b-115">В области действий щелкните **Пакетное задание**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="5b97b-116">Щелкните **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-116">Click **Recurrence**.</span></span> <span data-ttu-id="5b97b-117">Эти параметры используются для ввода диапазона и схемы повторения.</span><span class="sxs-lookup"><span data-stu-id="5b97b-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="5b97b-118">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="5b97b-119">Добавление оповещений</span><span class="sxs-lookup"><span data-stu-id="5b97b-119">Add alerts</span></span>
1. <span data-ttu-id="5b97b-120">В области действий щелкните **Пакетное задание**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="5b97b-121">Щелкните **Оповещения**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-121">Click **Alerts**.</span></span> <span data-ttu-id="5b97b-122">Укажите, требуется ли отправлять оповещения по завершении пакетного задания, в случае ошибки или отмены.</span><span class="sxs-lookup"><span data-stu-id="5b97b-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="5b97b-123">Затем укажите, требуется ли отображать оповещения в виде всплывающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="5b97b-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="5b97b-124">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="5b97b-125">Настройка статуса пакетного задания</span><span class="sxs-lookup"><span data-stu-id="5b97b-125">Adjust batch job status</span></span>
1. <span data-ttu-id="5b97b-126">Перейдите в раздел **Администрирование системы > Запросы > Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="5b97b-127">Выберите соответствующее пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="5b97b-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="5b97b-128">В области действий щелкните **Пакетное задание > Функции > Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="5b97b-129">Выберите соответствующий статус.</span><span class="sxs-lookup"><span data-stu-id="5b97b-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="5b97b-130">**Отложено**: задавайте пакетное задание как **отложено**, чтобы оно откладывалось планировщиком пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="5b97b-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="5b97b-131">Эквивалентно *остановке*.</span><span class="sxs-lookup"><span data-stu-id="5b97b-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="5b97b-132">**Ожидание**: установите пакетное задание как **ожидание**, чтобы оно ожидало обработки планировщиком пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="5b97b-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="5b97b-133">Эквивалентно *запуску*.</span><span class="sxs-lookup"><span data-stu-id="5b97b-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="5b97b-134">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b97b-134">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]