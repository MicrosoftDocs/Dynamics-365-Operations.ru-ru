---
title: Регистрация потребления
description: В этом разделе описывается, как регистрировать потребление в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024668"
---
# <a name="register-consumption"></a><span data-ttu-id="f11a7-103">Регистрация потребления</span><span class="sxs-lookup"><span data-stu-id="f11a7-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f11a7-104">После завершения задания по обслуживанию в заказе на работу, следующим шагом является создание регистраций потребления и разноска журналов.</span><span class="sxs-lookup"><span data-stu-id="f11a7-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f11a7-105">Регистрации можно выполнять для следующих типов потребления: часы, номенклатуры и расходы.</span><span class="sxs-lookup"><span data-stu-id="f11a7-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f11a7-106">Различные типы потребления регистрируются и разносятся на странице **Журналы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f11a7-107">Настройка журнала в модуле **Управление активами** используется для создания и разноски отдельных журналов для часов, номенклатур и расходов в модуле **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f11a7-108">Можно добавить или удалить строки прогноза в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f11a7-109">Настройка состояния жизненного цикла заказа на работу, соответствующего типа проекта и правил этапа, связанных с типом проекта, определяет, можно ли добавлять или редактировать строки журнала.</span><span class="sxs-lookup"><span data-stu-id="f11a7-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f11a7-110">Более подробную информацию о состояниях жизненного цикла заказов на работу и соответствующих этапах проекта см. в разделе [Интеграция с управлением и учетом по проектам](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="f11a7-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f11a7-111">Можно настроить автоматическую разноску журналов в состоянии жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f11a7-112">Дополнительные сведения см. в разделе [Состояния жизненного цикла заказа на работу](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="f11a7-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f11a7-113">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f11a7-114">Выберите заказ на работу и щелкните **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f11a7-115">Щелкните **Копировать из прогноза** для переноса любых строк прогноза, которые могут быть связаны с этим заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f11a7-116">Можно выбрать, какие типы потребления требуется перенести.</span><span class="sxs-lookup"><span data-stu-id="f11a7-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f11a7-117">При необходимости можно добавить дополнительные строки потребления на соответствующую экспресс-вкладку, щелкнув **Добавить строку** и заполнив данные в строке.</span><span class="sxs-lookup"><span data-stu-id="f11a7-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f11a7-118">Щелкните **Проверка журналов**, чтобы проверять строки журнала перед разноской.</span><span class="sxs-lookup"><span data-stu-id="f11a7-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f11a7-119">Щелкните **Разнести журналы**, чтобы разнести строки журнала.</span><span class="sxs-lookup"><span data-stu-id="f11a7-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f11a7-120">После разноски журналов потребления можно обновить состояние жизненного цикла заказов на работу, например на "Завершено", чтобы указать, что заказ на работу завершен.</span><span class="sxs-lookup"><span data-stu-id="f11a7-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="f11a7-121">В поле **Показать**, расположенном в верхней части страницы **Журналы заказов на работу**, выберите, какие строки журнала требуется просмотреть: все, неразнесенные или разнесенные.</span><span class="sxs-lookup"><span data-stu-id="f11a7-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="f11a7-122">Разнесенные журналы помечаются флажком **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="f11a7-123">Когда строки номенклатуры создаются в журнале заказов на работу, аналитики продуктов и аналитики отслеживания, которые связаны с номенклатурой, автоматически переносятся в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="f11a7-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f11a7-124">На следующем снимке экрана показан пример регистраций времени и номенклатуры в заказе на работу в пункте **Журналы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Рисунок 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f11a7-126">Разбиение часов по заказам на работу с несколькими заданиями заказа на работу</span><span class="sxs-lookup"><span data-stu-id="f11a7-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f11a7-127">Если заказ на работу содержит несколько заданий заказа на работу, можно регистрировать рабочие часы с помощью функции **Разбиение часов**, что означает, что одну строку регистрации времени можно равномерно распределить по каждому заданию заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f11a7-128">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f11a7-129">Выберите заказ на работу и щелкните **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f11a7-130">Выберите строку регистрации времени, которую необходимо разделить, и щелкните **Разделение часов**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f11a7-131">В диалоговом окне **Разделение часов по заданиям обслуживания заказов на работу** имя работника, вошедшего в систему, автоматически отображается в поле **Работник**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f11a7-132">Если необходимо, можно выбрать другого работника.</span><span class="sxs-lookup"><span data-stu-id="f11a7-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f11a7-133">Выберите категорию для регистрации часов в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f11a7-134">Введите количество разделяемых рабочих часов в поле **Часы**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Рисунок 2](media/02-consumption.png)

7. <span data-ttu-id="f11a7-136">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="f11a7-136">Click **OK**.</span></span>

<span data-ttu-id="f11a7-137">*Пример:* на следующем снимке экрана показаны строки журнала для заказа на работу, содержащего три задания по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f11a7-138">Первая строка, содержащая три рабочих часа, была разделена, и один рабочий час регистрируется для каждого задания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f11a7-139">После создания трех строк регистрации времени вы решаете, что нужно делать с исходной строкой регистрации часов (первая строка в примере).</span><span class="sxs-lookup"><span data-stu-id="f11a7-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f11a7-140">Ее можно сохранить как есть или удалить.</span><span class="sxs-lookup"><span data-stu-id="f11a7-140">You can keep it as is or delete it.</span></span> 

![Рисунок 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f11a7-142">Финансовые аналитики в регистрациях потребления</span><span class="sxs-lookup"><span data-stu-id="f11a7-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f11a7-143">При создании регистраций потребления финансовые аналитики, связанные с разными типами регистрации, добавляются к регистрациям в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="f11a7-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="f11a7-144">*Регистрации времени и расходов:* сначала добавляются финансовые аналитики из заголовка журнала, если они есть.</span><span class="sxs-lookup"><span data-stu-id="f11a7-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f11a7-145">Затем добавляются финансовые аналитики из соответствующего проекта заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f11a7-146">Наконец, будут добавлены финансовые аналитики из ресурса (работника).</span><span class="sxs-lookup"><span data-stu-id="f11a7-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="f11a7-147">*Регистрации номенклатуры:* сначала добавляются финансовые аналитики из заголовка журнала, если они есть.</span><span class="sxs-lookup"><span data-stu-id="f11a7-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f11a7-148">Затем добавляются финансовые аналитики из соответствующего проекта заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="f11a7-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f11a7-149">Затем добавляются финансовые аналитики из сайта.</span><span class="sxs-lookup"><span data-stu-id="f11a7-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f11a7-150">Наконец, будут добавлены финансовые аналитики из номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f11a7-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f11a7-151">Для всех трех типов регистрации проверяется комбинация финансовых аналитик, и недопустимые комбинации остаются пустыми.</span><span class="sxs-lookup"><span data-stu-id="f11a7-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f11a7-152">Это стандартная настройка в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f11a7-152">This is standard setup in Finance and Operations.</span></span>

