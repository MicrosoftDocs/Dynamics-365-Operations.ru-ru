---
title: Регистрация потребления
description: В этом разделе описывается, как регистрировать потребление в управлении активами.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c59664346c07f5e74825de41870f6635ced24ebd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216336"
---
# <a name="register-consumption"></a><span data-ttu-id="a6c5b-103">Регистрация потребления</span><span class="sxs-lookup"><span data-stu-id="a6c5b-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a6c5b-104">После завершения задания по обслуживанию в заказе на работу, следующим шагом является создание регистраций потребления и разноска журналов.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="a6c5b-105">Регистрации можно выполнять для следующих типов потребления: часы, номенклатуры и расходы.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="a6c5b-106">Различные типы потребления регистрируются и разносятся на странице **Журналы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="a6c5b-107">Настройка журнала в модуле **Управление активами** используется для создания и разноски отдельных журналов для часов, номенклатур и расходов в модуле **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="a6c5b-108">В некоторых случаях можно добавить или удалить строки прогноза в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="a6c5b-109">Настройка состояния жизненного цикла заказа на работу, соответствующего типа проекта и правил этапа, связанных с типом проекта, определяет, можно ли добавлять или редактировать строки журнала.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="a6c5b-110">Дополнительные сведения о состояниях жизненного цикла заказов на работу и связанных этапах проекта см. в разделе [Прогнозы, заказы на работу и проекты](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="a6c5b-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="a6c5b-111">Можно настроить автоматическую разноску журналов в состоянии жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="a6c5b-112">Дополнительные сведения см. в разделе [Состояния жизненного цикла заказа на работу](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="a6c5b-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="a6c5b-113">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a6c5b-114">Выберите заказ на работу и щелкните **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="a6c5b-115">Щелкните **Копировать из прогноза** для переноса любых строк прогноза, которые могут быть связаны с этим заказом на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="a6c5b-116">Можно выбрать, какие типы потребления требуется перенести.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="a6c5b-117">При необходимости можно добавить дополнительные строки потребления на соответствующую экспресс-вкладку, щелкнув **Добавить строку** и заполнив данные в строке.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="a6c5b-118">Щелкните **Проверка журналов**, чтобы проверять строки журнала перед разноской.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="a6c5b-119">Щелкните **Разнести журналы**, чтобы разнести строки журнала.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="a6c5b-120">После разноски журналов потребления можно обновить состояние жизненного цикла заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="a6c5b-121">Например, чтобы указать, что заказ на работу завершен, можно изменить статус жизненного цикла на "завершено".</span><span class="sxs-lookup"><span data-stu-id="a6c5b-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="a6c5b-122">В поле **Показать**, расположенном в верхней части страницы **Журналы заказов на работу**, выберите, какие строки журнала требуется просмотреть: **все**, **неразнесенные** или **разнесенные**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="a6c5b-123">Разнесенные журналы помечаются флажком **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="a6c5b-124">Когда строки номенклатуры создаются в журнале заказов на работу, аналитики продуктов и аналитики отслеживания, которые связаны с номенклатурой, автоматически переносятся в строку журнала.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="a6c5b-125">На следующем снимке экрана показан пример регистраций времени и номенклатуры в заказе на работу в пункте **Журналы заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Рисунок 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="a6c5b-127">Разбиение часов по заказам на работу с несколькими заданиями заказа на работу</span><span class="sxs-lookup"><span data-stu-id="a6c5b-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="a6c5b-128">Если заказ на работу содержит несколько заданий заказа на работу, можно регистрировать рабочие часы с помощью функции **Разбиение часов**, что означает, что одну строку регистрации времени можно равномерно распределить по каждому заданию заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="a6c5b-129">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a6c5b-130">Выберите заказ на работу и щелкните **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="a6c5b-131">Выберите строку регистрации времени, которую необходимо разделить, и щелкните **Разделение часов**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="a6c5b-132">В диалоговом окне **Разделение часов по заданиям обслуживания заказов на работу** имя работника, вошедшего в систему, автоматически отображается в поле **Работник**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="a6c5b-133">Если необходимо, можно выбрать другого работника.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="a6c5b-134">Выберите категорию для регистрации часов в поле **Категория**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="a6c5b-135">Введите количество разделяемых рабочих часов в поле **Часы**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Рисунок 2](media/02-consumption.png)

7. <span data-ttu-id="a6c5b-137">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-137">Click **OK**.</span></span>

<span data-ttu-id="a6c5b-138">*Пример:* на следующем снимке экрана показаны строки журнала для заказа на работу, содержащего три задания по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="a6c5b-139">Первая строка, содержащая три рабочих часа, была разделена, и один рабочий час регистрируется для каждого задания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="a6c5b-140">После создания трех строк регистрации времени вы решаете, что нужно делать с исходной строкой регистрации часов (первая строка в примере).</span><span class="sxs-lookup"><span data-stu-id="a6c5b-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="a6c5b-141">Ее можно сохранить как есть или удалить.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-141">You can keep it as is or delete it.</span></span> 

![Рисунок 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="a6c5b-143">Финансовые аналитики в регистрациях потребления</span><span class="sxs-lookup"><span data-stu-id="a6c5b-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="a6c5b-144">При создании регистраций потребления финансовые аналитики, связанные с разными типами регистрации, добавляются к регистрациям в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="a6c5b-145">*Регистрации времени и расходов:* сначала добавляются финансовые аналитики из заголовка журнала, если они есть.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a6c5b-146">Затем добавляются финансовые аналитики из соответствующего проекта заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a6c5b-147">Наконец, будут добавлены финансовые аналитики из ресурса (работника).</span><span class="sxs-lookup"><span data-stu-id="a6c5b-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="a6c5b-148">*Регистрации номенклатуры:* сначала добавляются финансовые аналитики из заголовка журнала, если они есть.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a6c5b-149">Затем добавляются финансовые аналитики из соответствующего проекта заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a6c5b-150">Затем добавляются финансовые аналитики из сайта.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="a6c5b-151">Наконец, будут добавлены финансовые аналитики из номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="a6c5b-152">Для всех трех типов регистрации проверяется комбинация финансовых аналитик, и недопустимые комбинации остаются пустыми.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="a6c5b-153">Это стандартная настройка для других приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6c5b-153">This is standard setup with other Finance and Operations apps.</span></span>

