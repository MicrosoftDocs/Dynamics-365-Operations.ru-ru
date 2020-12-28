---
title: Расчет предложений по количеству канбанов
description: Эта процедура заключается в оптимизации размера и количества канбанов для конкретного правила канбана путем использования расчета количества канбанов.
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa6a01d8f918c45aaa454e5234f80c312d7a5061
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435767"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="a39e4-103">Расчет предложений по количеству канбанов</span><span class="sxs-lookup"><span data-stu-id="a39e4-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a39e4-104">Эта процедура заключается в оптимизации размера и количества канбанов для конкретного правила канбана путем использования расчета количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="a39e4-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a39e4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a39e4-106">Эта процедура предназначена для менеджера потока создания ценности.</span><span class="sxs-lookup"><span data-stu-id="a39e4-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="a39e4-107">Предварительным условием является выполнение процедуры "Добавление политики расчета количества канбанов к правилу канбана".</span><span class="sxs-lookup"><span data-stu-id="a39e4-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="a39e4-108">Создание расчета количества канбанов</span><span class="sxs-lookup"><span data-stu-id="a39e4-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="a39e4-109">Перейдите в раздел "Управление производством" > "Периодические задачи" > "Расчет количества канбанов" > "Рассчитать количество канбанов".</span><span class="sxs-lookup"><span data-stu-id="a39e4-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="a39e4-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a39e4-110">Click New.</span></span>
3. <span data-ttu-id="a39e4-111">В поле "Имя" введите "Speaker2016".</span><span class="sxs-lookup"><span data-stu-id="a39e4-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="a39e4-112">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a39e4-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a39e4-113">Выберите политику, созданную в процедуре "Добавление политики расчета количества канбанов к правилу канбана".</span><span class="sxs-lookup"><span data-stu-id="a39e4-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="a39e4-114">Например, Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="a39e4-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="a39e4-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a39e4-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a39e4-116">В поле "Правило активно на дату" установите дату и время равными "17.12.2012T08:00:00"</span><span class="sxs-lookup"><span data-stu-id="a39e4-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="a39e4-117">На основе этой даты определяется, какие фиксированные правила канбана включены в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="a39e4-118">В поле "Дата начала выполненного периода спроса" установите дату и время равными "17.11.2012T09:00:00"</span><span class="sxs-lookup"><span data-stu-id="a39e4-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="a39e4-119">Дата, начиная с которой проводки по прошлому спросу будут включены в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="a39e4-120">В поле "Дата окончания выполненного периода спроса" установите дату и время равными "17.12.2012T07:59:59"</span><span class="sxs-lookup"><span data-stu-id="a39e4-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="a39e4-121">Дата, по которую проводки по прошлому спросу будут включены в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="a39e4-122">В поле "Дата начала периода спроса" установите дату и время равными "17.12.2012T08:00:00"</span><span class="sxs-lookup"><span data-stu-id="a39e4-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="a39e4-123">Дата, начиная с которой проводки по текущему спросу будут включены в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="a39e4-124">В поле "Дата окончания периода спроса" установите дату и время равными "16.01.2013T07:59:59"</span><span class="sxs-lookup"><span data-stu-id="a39e4-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="a39e4-125">Дата, по которую проводки по текущему спросу будут включены в расчет количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="a39e4-126">Формирование предложения по количеству канбанов</span><span class="sxs-lookup"><span data-stu-id="a39e4-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="a39e4-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a39e4-127">Click Save.</span></span>
2. <span data-ttu-id="a39e4-128">Щелкните "Сформировать".</span><span class="sxs-lookup"><span data-stu-id="a39e4-128">Click Generate.</span></span>
    * <span data-ttu-id="a39e4-129">В результате этого будет создана строка предложения по количеству канбанов для правила канбана 000020.</span><span class="sxs-lookup"><span data-stu-id="a39e4-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="a39e4-130">Запуск расчета количества канбанов</span><span class="sxs-lookup"><span data-stu-id="a39e4-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="a39e4-131">Щелкните "Рассчитать".</span><span class="sxs-lookup"><span data-stu-id="a39e4-131">Click Calculate.</span></span>
    * <span data-ttu-id="a39e4-132">В результате будет рассчитано предложение по количеству канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="a39e4-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a39e4-133">Click OK.</span></span>
3. <span data-ttu-id="a39e4-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a39e4-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a39e4-135">Обратите внимание, что предлагаемое количество канбанов равно 2.</span><span class="sxs-lookup"><span data-stu-id="a39e4-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="a39e4-136">Изменение количества продукта и повторный расчет</span><span class="sxs-lookup"><span data-stu-id="a39e4-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="a39e4-137">Установите количество продукта равным 5.</span><span class="sxs-lookup"><span data-stu-id="a39e4-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="a39e4-138">Щелкните "Рассчитать".</span><span class="sxs-lookup"><span data-stu-id="a39e4-138">Click Calculate.</span></span>
3. <span data-ttu-id="a39e4-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a39e4-139">Click OK.</span></span>
    * <span data-ttu-id="a39e4-140">Обратите внимание, что при количестве канбанов, равном 5, предложение меняется на количество канбанов, равное 4.</span><span class="sxs-lookup"><span data-stu-id="a39e4-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="a39e4-141">Это связано с тем, что при более низком количестве продукта нам требуется больше канбанов для удовлетворения спроса.</span><span class="sxs-lookup"><span data-stu-id="a39e4-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="a39e4-142">Обновление правила канбана</span><span class="sxs-lookup"><span data-stu-id="a39e4-142">Update kanban rule</span></span>
1. <span data-ttu-id="a39e4-143">В поле "Дата начала действия правила" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="a39e4-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="a39e4-144">Установите значение в поле "Правило активно на дату" равным какой-либо дате в будущем.</span><span class="sxs-lookup"><span data-stu-id="a39e4-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="a39e4-145">Например, сегодня + один год.</span><span class="sxs-lookup"><span data-stu-id="a39e4-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="a39e4-146">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="a39e4-146">Click Update.</span></span>
3. <span data-ttu-id="a39e4-147">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a39e4-147">Click OK.</span></span>
4. <span data-ttu-id="a39e4-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a39e4-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="a39e4-149">Проверка изменения в правиле канбана</span><span class="sxs-lookup"><span data-stu-id="a39e4-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="a39e4-150">Перейдите в раздел "Управление сведениями о продуктах" > "Бережливое производство" > "Правила канбана".</span><span class="sxs-lookup"><span data-stu-id="a39e4-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="a39e4-151">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a39e4-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a39e4-152">Выберите правило канбана, созданное в предыдущей подзадаче.</span><span class="sxs-lookup"><span data-stu-id="a39e4-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="a39e4-153">Это должно быть первое правило канбана в списке, отсортированном по номеру.</span><span class="sxs-lookup"><span data-stu-id="a39e4-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="a39e4-154">Переключите развертывание раздела "Подробности".</span><span class="sxs-lookup"><span data-stu-id="a39e4-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="a39e4-155">Обратите внимание на дату вступления в силу, которое означает, что правило не активируется до этой даты.</span><span class="sxs-lookup"><span data-stu-id="a39e4-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="a39e4-156">Переключите развертывание раздела "Количества".</span><span class="sxs-lookup"><span data-stu-id="a39e4-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="a39e4-157">Обратите внимание, что это количество по умолчанию, которое вы ввели при расчете количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="a39e4-158">Заметьте, что это фиксированное число канбанов, равное 4, из расчета количества канбанов.</span><span class="sxs-lookup"><span data-stu-id="a39e4-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="a39e4-159">Перейдите на вкладку ListPanel.</span><span class="sxs-lookup"><span data-stu-id="a39e4-159">Click the ListPanel tab.</span></span>

