---
title: Использование журнала резервного запаса для обновления минимального покрытия
description: В этой процедуре показано, как рассчитать предложения минимального покрытия на основе статистических проводок, а затем обновить покрытие номенклатуры с учетом предложений.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252806"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="98826-103">Использование журнала резервного запаса для обновления минимального покрытия</span><span class="sxs-lookup"><span data-stu-id="98826-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98826-104">В этой процедуре показано, как рассчитать предложения минимального покрытия на основе статистических проводок, а затем обновить покрытие номенклатуры с учетом предложений.</span><span class="sxs-lookup"><span data-stu-id="98826-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="98826-105">Она выполняется с использованием журнала резервного запаса.</span><span class="sxs-lookup"><span data-stu-id="98826-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="98826-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="98826-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="98826-107">Эта задача назначена для планировщика производства для поддержки минимального покрытия.</span><span class="sxs-lookup"><span data-stu-id="98826-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="98826-108">Создание нового имени журнала резервного запаса</span><span class="sxs-lookup"><span data-stu-id="98826-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="98826-109">В **области переходов** выберите **Сводное планирование > Настройка > Имена журналов резервного запаса**.</span><span class="sxs-lookup"><span data-stu-id="98826-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="98826-110">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98826-110">Click **New**.</span></span>
3. <span data-ttu-id="98826-111">В поле **Имя** введите "Материал".</span><span class="sxs-lookup"><span data-stu-id="98826-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="98826-112">В поле **Описание** введите "Материал".</span><span class="sxs-lookup"><span data-stu-id="98826-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="98826-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98826-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="98826-114">Создание журнала резервного запаса</span><span class="sxs-lookup"><span data-stu-id="98826-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="98826-115">В **области переходов** выберите **Сводное планирование > Сводное планирование > Выполнить > Расчет резервного запаса**.</span><span class="sxs-lookup"><span data-stu-id="98826-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="98826-116">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98826-116">Click **New**.</span></span>
3. <span data-ttu-id="98826-117">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="98826-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="98826-118">Выберите наименование созданного журнала резервного запаса, например "Материал".</span><span class="sxs-lookup"><span data-stu-id="98826-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="98826-119">Щелкните **Создать строки**.</span><span class="sxs-lookup"><span data-stu-id="98826-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="98826-120">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="98826-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="98826-121">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="98826-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="98826-122">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="98826-122">Click **OK**.</span></span> <span data-ttu-id="98826-123">В результате будут созданы строки для аналитик, которые имеют проводки по запасам.</span><span class="sxs-lookup"><span data-stu-id="98826-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="98826-124">Подсчет предложений</span><span class="sxs-lookup"><span data-stu-id="98826-124">Calculate proposal</span></span>
1. <span data-ttu-id="98826-125">Щелкните **Подсчет предложений**.</span><span class="sxs-lookup"><span data-stu-id="98826-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="98826-126">Выберите параметр **Использовать средний расход за время упреждения**.</span><span class="sxs-lookup"><span data-stu-id="98826-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="98826-127">Задайте для параметра **Множитель** значение "10".</span><span class="sxs-lookup"><span data-stu-id="98826-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="98826-128">Коэффициент умножения используется для корректировки предложения.</span><span class="sxs-lookup"><span data-stu-id="98826-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="98826-129">Поскольку демонстрационные данные имеют только несколько проводок, потребуется задать коэффициент для получения реалистического предложения.</span><span class="sxs-lookup"><span data-stu-id="98826-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="98826-130">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="98826-130">Click **OK**.</span></span> <span data-ttu-id="98826-131">Прокрутите вниз, чтобы найти M0002 и M0003.</span><span class="sxs-lookup"><span data-stu-id="98826-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="98826-132">Просмотрите столбец **Рассчитанное минимальное количество**.</span><span class="sxs-lookup"><span data-stu-id="98826-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="98826-133">Обновление минимального количества</span><span class="sxs-lookup"><span data-stu-id="98826-133">Update minimum quantity</span></span>
1. <span data-ttu-id="98826-134">В поле **Новое минимальное количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="98826-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="98826-135">Обновите новое минимальное количество для соответствия значению в поле "Рассчитанное минимальное количество".</span><span class="sxs-lookup"><span data-stu-id="98826-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="98826-136">Если значение "Рассчитанное минимальное количество" равно нулю, можно ввести требуемое будущее значение.</span><span class="sxs-lookup"><span data-stu-id="98826-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="98826-137">Например, можно ввести рассчитанное минимальное количество в это поле для M0002 со складом 12.</span><span class="sxs-lookup"><span data-stu-id="98826-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="98826-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="98826-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="98826-139">Например, можно выбрать M0002 со складом 12.</span><span class="sxs-lookup"><span data-stu-id="98826-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="98826-140">В поле **Новое минимальное количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="98826-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="98826-141">Обновите новое минимальное количество для соответствия значению в поле "Рассчитанное минимальное количество".</span><span class="sxs-lookup"><span data-stu-id="98826-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="98826-142">Если значение "Рассчитанное минимальное количество" равно нулю, можно ввести требуемое будущее значение.</span><span class="sxs-lookup"><span data-stu-id="98826-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="98826-143">Разноска нового минимального количества и проверка результата</span><span class="sxs-lookup"><span data-stu-id="98826-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="98826-144">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="98826-144">Click **Post**.</span></span>
2. <span data-ttu-id="98826-145">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="98826-145">Click **OK**.</span></span>
3. <span data-ttu-id="98826-146">Щелкните для перехода по ссылке в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="98826-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="98826-147">Щелкните для перехода по ссылке в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="98826-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="98826-148">В области **Панель операций** щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="98826-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="98826-149">Щелкните **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="98826-149">Click **Item coverage**.</span></span> <span data-ttu-id="98826-150">Обратите внимание, что **Минимальное количество** было обновлено для отображения нового минимального количества из журнала резервного запаса.</span><span class="sxs-lookup"><span data-stu-id="98826-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]