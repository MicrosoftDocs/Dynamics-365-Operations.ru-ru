---
title: Оптимизация производительности путем планирования пакетных заданий на нерабочие часы
description: В этой теме объясняется, как решать некоторые проблемы с производительностью в Microsoft Dynamics 365 Human Resources путем планирования пакетных заданий на нерабочие часы.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114032"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="7cda3-103">Оптимизация производительности путем планирования пакетных заданий на нерабочие часы</span><span class="sxs-lookup"><span data-stu-id="7cda3-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="7cda3-104">Расход</span><span class="sxs-lookup"><span data-stu-id="7cda3-104">Issue</span></span>

<span data-ttu-id="7cda3-105">Microsoft Dynamics 365 Human Resources может столкнуться с проблемами производительности, если долгосрочные пакетные задания запускаются в обычное рабочее время.</span><span class="sxs-lookup"><span data-stu-id="7cda3-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="7cda3-106">Приказ</span><span class="sxs-lookup"><span data-stu-id="7cda3-106">Resolution</span></span>

<span data-ttu-id="7cda3-107">Запланируйте следующие пакетные задания на нерабочее время.</span><span class="sxs-lookup"><span data-stu-id="7cda3-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="7cda3-108">Также рекомендуется проверить частоту часто выполняемых пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="7cda3-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="7cda3-109">Если это возможно, уменьшите число повторений пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="7cda3-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="7cda3-110">Во многих случаях достаточно частоты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7cda3-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="7cda3-111">Следующие пакетные задания должны запускаться ночью или в нерабочее время.</span><span class="sxs-lookup"><span data-stu-id="7cda3-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="7cda3-112">Обязательно проверьте часовой пояс для этих повторяющихся пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="7cda3-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="7cda3-113">Некоторые пакетные задания могут использовать стандартное тихоокеанское время (PST).</span><span class="sxs-lookup"><span data-stu-id="7cda3-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="7cda3-114">Пакетное задание</span><span class="sxs-lookup"><span data-stu-id="7cda3-114">Batch job</span></span> | <span data-ttu-id="7cda3-115">Повторение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7cda3-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="7cda3-116">Очистка истории пакетных заданий</span><span class="sxs-lookup"><span data-stu-id="7cda3-116">Batch job history cleanup</span></span> | <span data-ttu-id="7cda3-117">1 раз в месяц</span><span class="sxs-lookup"><span data-stu-id="7cda3-117">1 time per month</span></span> |
| <span data-ttu-id="7cda3-118">Экспорт очистки промежуточных данных</span><span class="sxs-lookup"><span data-stu-id="7cda3-118">Export staging cleanup</span></span> | <span data-ttu-id="7cda3-119">1 раз в день</span><span class="sxs-lookup"><span data-stu-id="7cda3-119">1 time per day</span></span> |
| <span data-ttu-id="7cda3-120">Синхронизация пропущенных запросов интеграции Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7cda3-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="7cda3-121">1 раз в день</span><span class="sxs-lookup"><span data-stu-id="7cda3-121">1 time per day</span></span> |
| <span data-ttu-id="7cda3-122">Системное задание сжатия базы данных, которое должно регулярно запускаться в нерабочие часы</span><span class="sxs-lookup"><span data-stu-id="7cda3-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="7cda3-123">1 раз в день</span><span class="sxs-lookup"><span data-stu-id="7cda3-123">1 time per day</span></span> |
| <span data-ttu-id="7cda3-124">Системное задание перестроения индекса базы данных, которое должно регулярно запускаться в нерабочие часы</span><span class="sxs-lookup"><span data-stu-id="7cda3-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="7cda3-125">1 раз в день</span><span class="sxs-lookup"><span data-stu-id="7cda3-125">1 time per day</span></span> |

1. <span data-ttu-id="7cda3-126">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="7cda3-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7cda3-127">В строке **Поиск** выполните поиск по одному из указанных выше пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="7cda3-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="7cda3-128">Выберите **Выполнять в фоновом режиме**, затем выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="7cda3-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Задание повторения](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="7cda3-130">В области **Определение повторения** задайте значения **Дата начала** и **Время начала**, чтобы они приходились на нерабочее время или выходные.</span><span class="sxs-lookup"><span data-stu-id="7cda3-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="7cda3-131">Выберите **Без даты окончания**.</span><span class="sxs-lookup"><span data-stu-id="7cda3-131">Select **No end date**.</span></span> 

   ![Задание даты и времени начала повторения](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="7cda3-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7cda3-133">Select **OK**.</span></span>

6. <span data-ttu-id="7cda3-134">При необходимости измените любые другие параметры в области **Выполнять в фоновом режиме**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7cda3-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cda3-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7cda3-135">Additional resources</span></span>

[<span data-ttu-id="7cda3-136">Оптимизация производительности с помощью задач автоматической очистки</span><span class="sxs-lookup"><span data-stu-id="7cda3-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
