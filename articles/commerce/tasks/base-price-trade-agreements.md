---
title: Базовая цена и коммерческие соглашения
description: Эта процедура содержит инструкции по созданию коммерческих предложений по ценам продажи для конкретных каналов.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022db9365f25c1d3e387870dd9d173077d864b3d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141530"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="a4e51-103">Базовая цена и коммерческие соглашения</span><span class="sxs-lookup"><span data-stu-id="a4e51-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4e51-104">Эта процедура содержит инструкции по созданию коммерческих предложений по ценам продажи для конкретных каналов.</span><span class="sxs-lookup"><span data-stu-id="a4e51-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="a4e51-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="a4e51-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="a4e51-106">В **области переходов** выберите **Модули > Retail и Commerce > Управление ценообразованием и скидками > Группы цен > Все группы цен**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="a4e51-107">Ценовые группы определяют, каким образом коммерческие соглашения назначаются конкретным каналам.</span><span class="sxs-lookup"><span data-stu-id="a4e51-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="a4e51-108">Использование ценовых групп для назначения коммерческих соглашений каналам делает возможным ценообразование на уровне каналов.</span><span class="sxs-lookup"><span data-stu-id="a4e51-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="a4e51-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-109">Click **New**.</span></span>
3. <span data-ttu-id="a4e51-110">В поле **Группы цен** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a4e51-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="a4e51-111">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a4e51-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a4e51-112">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-112">Click **Save**.</span></span>
6. <span data-ttu-id="a4e51-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4e51-113">Close the page.</span></span>
7. <span data-ttu-id="a4e51-114">В области **Область переходов** выберите **Модули > Retail и Commerce > Каналы > Магазины > Все магазины**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="a4e51-115">В списке выберите "Нью-Йорк".</span><span class="sxs-lookup"><span data-stu-id="a4e51-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="a4e51-116">В области действий щелкните **Магазин**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="a4e51-117">Щелкните **Группы цен**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="a4e51-118">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-118">Click **New**.</span></span>
12. <span data-ttu-id="a4e51-119">В поле **Группы цен** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a4e51-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a4e51-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a4e51-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a4e51-121">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-121">Click **Save**.</span></span>
15. <span data-ttu-id="a4e51-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4e51-122">Close the page.</span></span>
16. <span data-ttu-id="a4e51-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4e51-123">Close the page.</span></span>
17. <span data-ttu-id="a4e51-124">В **области переходов** выберите **Модули > Retail и Commerce > Продукты и категории > Выпущенные продукты по категориям**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="a4e51-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a4e51-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="a4e51-126">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-126">Click **Edit**.</span></span>
20. <span data-ttu-id="a4e51-127">Разверните экспресс-вкладку **Продажа**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="a4e51-128">В поле **Цена** введите число.</span><span class="sxs-lookup"><span data-stu-id="a4e51-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="a4e51-129">Эта цена используется, если не найдены подходящие коммерческие соглашения.</span><span class="sxs-lookup"><span data-stu-id="a4e51-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="a4e51-130">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-130">Click **Save**.</span></span>
23. <span data-ttu-id="a4e51-131">В области **Панель операций** щелкните **Продажа**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="a4e51-132">Щелкните **Создать коммерческие соглашения**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="a4e51-133">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-133">Click **New**.</span></span>
26. <span data-ttu-id="a4e51-134">В поле **Имя** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a4e51-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="a4e51-135">В списке выберите **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="a4e51-136">В демонстрационных данных имя журнала **Commerce** по умолчанию имеет связь **Цена (продажи)**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="a4e51-137">Это означает, что все новые созданные строки по умолчанию будут иметь цены продажи из коммерческих соглашений.</span><span class="sxs-lookup"><span data-stu-id="a4e51-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="a4e51-138">В **Панели операций** щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="a4e51-139">В поле **Код счета** выберите "Группа".</span><span class="sxs-lookup"><span data-stu-id="a4e51-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="a4e51-140">В поле **Выбор счета** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a4e51-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="a4e51-141">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a4e51-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="a4e51-142">Это завершить связь от канала к ценовой группе и коммерческому соглашению.</span><span class="sxs-lookup"><span data-stu-id="a4e51-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="a4e51-143">В поле **Связь номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a4e51-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="a4e51-144">В поле **Сумма в валюте** введите число.</span><span class="sxs-lookup"><span data-stu-id="a4e51-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="a4e51-145">На экспресс-вкладке **Сведения** установите или снимите флажок **Найти следующий**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="a4e51-146">Если поле **Найти далее** имеет значение "Да" модуль ценообразования продолжает поиск применимых коммерческих соглашений с более низкой ценой продажи.</span><span class="sxs-lookup"><span data-stu-id="a4e51-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="a4e51-147">Когда поле **Найти далее** имеет значение "Нет", модуль ценообразования прекращает поиск и использует коммерческое соглашение.</span><span class="sxs-lookup"><span data-stu-id="a4e51-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="a4e51-148">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-148">Click **Post**.</span></span>
36. <span data-ttu-id="a4e51-149">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-149">Click **OK**.</span></span>
37. <span data-ttu-id="a4e51-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4e51-150">Close the page.</span></span>
38. <span data-ttu-id="a4e51-151">В области **Панель операций** щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="a4e51-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="a4e51-152">Щелкните **Цена продажи**.</span><span class="sxs-lookup"><span data-stu-id="a4e51-152">Click **Sales price**.</span></span>

