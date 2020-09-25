---
title: Производительность планирования ресурсов проекта
description: В этой теме содержатся сведения о том, как улучшить производительность планирования ресурсов для большого количества проектов.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760649"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="dafbf-103">Производительность планирования ресурсов проекта</span><span class="sxs-lookup"><span data-stu-id="dafbf-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="dafbf-104">Проблемы с производительностью, связанные с планированием ресурсов, могут возникать, когда число проектов достигает тысяч.</span><span class="sxs-lookup"><span data-stu-id="dafbf-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="dafbf-105">Для повышения производительности планирования ресурсов доступна функция, позволяющая пользователям сократить время, необходимое для запуска формы доступности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dafbf-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="dafbf-106">В частности, это приведет к удалению процесса синхронизации свертки емкости ресурсов и использует таблицу **ResProjectResource** для ускорения поиска ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dafbf-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="dafbf-107">Обратите внимание, что таблица **ResRollup** больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="dafbf-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dafbf-108">Если имеется зависимость от процесса синхронизации по свертке емкости ресурсов или таблицы **ResProjectResource**, не используйте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="dafbf-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="dafbf-109">Включение улучшения производительности планирования ресурсов</span><span class="sxs-lookup"><span data-stu-id="dafbf-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="dafbf-110">Чтобы включить улучшение производительности планирования ресурсов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dafbf-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="dafbf-111">Выберите **Управление функциями** > **Все** и в списке функций найдите функцию **Включение улучшения производительности планирования ресурсов проектов**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="dafbf-112">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="dafbf-113">Если вы не можете найти функцию в списке, выберите **Проверить наличие обновлений**, чтобы обновить список.</span><span class="sxs-lookup"><span data-stu-id="dafbf-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="dafbf-114">Обновите веб-браузер, затем перейдите в раздел **Управление и учет по проектам** > **Периодические задачи** > **Ресурсы проекта** > **Синхронизация мощностей для календарей ресурсов во всех компаниях**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="dafbf-115">Установите для параметра **Удаление существующих записей о мощностях** значение **Да**, чтобы удалить предыдущие данные.</span><span class="sxs-lookup"><span data-stu-id="dafbf-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="dafbf-116">Если требуется генерировать инкрементные данные, установите для него значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="dafbf-117">В поле **Код периода** выберите период, в котором должны быть созданы данные.</span><span class="sxs-lookup"><span data-stu-id="dafbf-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="dafbf-118">При выборе кода периода дату начала и окончания не требуется определять.</span><span class="sxs-lookup"><span data-stu-id="dafbf-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="dafbf-119">Если оставить поле **Код периода** пустым, выберите для создания данных конкретные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="dafbf-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="dafbf-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="dafbf-121">При этом общие данные будут распределены в таблице **ResCalendarCapacity** по всем компаниям в вашей среде, поэтому пакетное задание должно быть выполнено только в одном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="dafbf-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="dafbf-122">Данные в этом пакетном задании необходимы для расчета емкости ресурсов через связанный календарь.</span><span class="sxs-lookup"><span data-stu-id="dafbf-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="dafbf-123">Выберите **Управление и учет по проектам** > **Периодические операции** > **Ресурсы проекта** > **Заполнить ресурсы проекта по всем компаниям**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="dafbf-124">Это сценарий обновления данных для общих данных в таблицах **ResProjectResource**, **ResCalendarDateTimeRange** и **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="dafbf-125">Значения для поля **PSAPRojSchedRole.RootActivity** также обновляются.</span><span class="sxs-lookup"><span data-stu-id="dafbf-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="dafbf-126">Если это не было выполнено, при попытке выполнить операции по планированию ресурсов будет выводиться предупреждение.</span><span class="sxs-lookup"><span data-stu-id="dafbf-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="dafbf-127">Выключение улучшения производительности планирования ресурсов</span><span class="sxs-lookup"><span data-stu-id="dafbf-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="dafbf-128">Выберите **Управление функциями** > **Все** и найдите функцию **Включение улучшения производительности планирования ресурсов проектов**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="dafbf-129">Выберите функцию, затем выберите кнопку **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="dafbf-130">Обновите веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="dafbf-130">Refresh your browser.</span></span>
4. <span data-ttu-id="dafbf-131">Выберите **Управление и учет по проектам** > **Периодические операции** > **Синхронизация мощностей** > **Синхронизация сверток емкости ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="dafbf-132">На странице **Синхронизация свертки емкости** установите для параметра **Удалить существующие записи о емкости** значение **Да**, чтобы удалить предыдущие данные.</span><span class="sxs-lookup"><span data-stu-id="dafbf-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="dafbf-133">Если требуется генерировать инкрементные данные, установите для него значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="dafbf-134">В поле **Код периода** выберите период, в котором должны быть созданы данные.</span><span class="sxs-lookup"><span data-stu-id="dafbf-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="dafbf-135">При выборе кода периода дату начала и окончания не требуется определять.</span><span class="sxs-lookup"><span data-stu-id="dafbf-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="dafbf-136">Если оставить поле **Код периода** пустым, выберите для создания данных конкретные даты начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="dafbf-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="dafbf-137">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="dafbf-138">При этом общие данные будут распределены в таблице **ResRollup** по всем компаниям в вашей среде, поэтому пакетное задание должно быть выполнено только в одном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="dafbf-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="dafbf-139">Это пакетное задание требуется для всех представлений **Доступность ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="dafbf-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="dafbf-140">Если пакетное задание не выполняется, данные **ResRollup** будут создаваться на ходу, что может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="dafbf-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
