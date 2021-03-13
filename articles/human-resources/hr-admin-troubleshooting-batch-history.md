---
title: Оптимизация производительности с помощью задач автоматической очистки
description: В этой статье объясняется, как решать некоторые проблемы с производительностью в Microsoft Dynamics 365 Human Resources, выполнив очистку журнала пакетных заданий.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 97f6e310d3a69c870fe8ef03bd7a10cc7ab652e5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114003"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="e330a-103">Оптимизация производительности с помощью задач автоматической очистки</span><span class="sxs-lookup"><span data-stu-id="e330a-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="e330a-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="e330a-104">**Issue**</span></span>

<span data-ttu-id="e330a-105">Microsoft Dynamics 365 Human Resources может столкнуться с проблемами производительности, если журнал пакетных заданий стал слишком большим.</span><span class="sxs-lookup"><span data-stu-id="e330a-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="e330a-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="e330a-106">**Cause**</span></span>

<span data-ttu-id="e330a-107">Часто выполняемые пакетные задания могут стать причиной неконтролируемого роста журнала пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="e330a-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="e330a-108">Это может привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="e330a-108">This can cause performance issues.</span></span> 

<span data-ttu-id="e330a-109">**Приказ**</span><span class="sxs-lookup"><span data-stu-id="e330a-109">**Resolution**</span></span>

<span data-ttu-id="e330a-110">Запланируйте автоматическую задачу для очистки журнала пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="e330a-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="e330a-111">Рекомендуется настроить задание на выполнение еженедельно, но, в зависимости от среды, может потребоваться выполнить очистку чаще или реже.</span><span class="sxs-lookup"><span data-stu-id="e330a-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="e330a-112">Следующая процедура содержит рекомендуемые параметры, но их можно изменить в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="e330a-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="e330a-113">В модуле Human Resources выберите **Администрирование системы**.</span><span class="sxs-lookup"><span data-stu-id="e330a-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e330a-114">На панели **Поиск** введите **Очистка журнала пакетных заданий**.</span><span class="sxs-lookup"><span data-stu-id="e330a-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Поиск очистки журнала пакетных заданий](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="e330a-116">В поле **Горизонт истории (дни)** введите **30**.</span><span class="sxs-lookup"><span data-stu-id="e330a-116">In **History limit (days)**, enter **30**.</span></span>

   ![Задание горизонта истории в 30 дней](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="e330a-118">Выберите **Выполнять в фоновом режиме**, затем выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="e330a-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Задание повторения](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="e330a-120">В области **Определение повторения** задайте поля **Дата начала** и **Время начала** на нерабочее время или выходные, затем выберите **НЕТ ДАТЫ ОКОНЧАНИЯ**.</span><span class="sxs-lookup"><span data-stu-id="e330a-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Задание даты и времени начала повторения](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="e330a-122">В области **ШАБЛОН ПОВТОРЕНИЯ** выберите **Дни** и задайте для параметра **ПОВТОРИТЬ ПОСЛЕ УКАЗАННОГО ИНТЕРВАЛА** значение **7**.</span><span class="sxs-lookup"><span data-stu-id="e330a-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Задание еженедельного повторения очистки](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="e330a-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e330a-124">Select **OK**.</span></span>

8. <span data-ttu-id="e330a-125">При необходимости измените любые другие параметры в области **Выполнять в фоновом режиме**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e330a-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

