--- 
title: "Определение канала центра обработки вызовов и атрибутов этого канала"
description: "Эта процедура содержит указания по созданию нового канала розничной торговли и определению атрибутов канала."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1418f04d8fb4d05756ac7a5f4b92a1950037be1d
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="a9842-103">Определение канала центра обработки вызовов и атрибутов этого канала</span><span class="sxs-lookup"><span data-stu-id="a9842-103">Define call center channel and channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a9842-104">Эта процедура содержит указания по созданию нового канала розничной торговли и определению атрибутов канала.</span><span class="sxs-lookup"><span data-stu-id="a9842-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="a9842-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="a9842-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="a9842-106">Эта процедура предназначена для роли "ИТ розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="a9842-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="a9842-107">Создание нового магазина</span><span class="sxs-lookup"><span data-stu-id="a9842-107">Create new store</span></span>
1. <span data-ttu-id="a9842-108">Пойдите к Все рабочие области > Развертывание канала.</span><span class="sxs-lookup"><span data-stu-id="a9842-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="a9842-109">Щелкните "Новый канал".</span><span class="sxs-lookup"><span data-stu-id="a9842-109">Click New channel.</span></span>
3. <span data-ttu-id="a9842-110">Щелкните "Магазин".</span><span class="sxs-lookup"><span data-stu-id="a9842-110">Click Store.</span></span>
4. <span data-ttu-id="a9842-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9842-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a9842-112">В поле "Номер магазина" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9842-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="a9842-113">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a9842-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a9842-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a9842-116">В поле "Часовой пояс магазина" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="a9842-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="a9842-117">В поле "Профиль канала" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a9842-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a9842-119">В поле "Язык" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a9842-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a9842-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a9842-122">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="a9842-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="a9842-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="a9842-125">В поле "Адресная книга клиентов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a9842-126">Выберите адресную книгу, используемую для связывания клиентов с этим магазином.</span><span class="sxs-lookup"><span data-stu-id="a9842-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="a9842-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="a9842-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="a9842-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="a9842-129">Click Select.</span></span>
22. <span data-ttu-id="a9842-130">В поле "Адресная книга сотрудников" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a9842-131">Выберите адресную книгу, используемую для связывания кассиров с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="a9842-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="a9842-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="a9842-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="a9842-134">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="a9842-134">Click Select.</span></span>
26. <span data-ttu-id="a9842-135">В поле "Клиент по умолчанию" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="a9842-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="a9842-137">Разверните или сверните раздел "Макет экрана".</span><span class="sxs-lookup"><span data-stu-id="a9842-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="a9842-138">В поле "Код макета экрана" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a9842-139">Выберите макета экрана POS по умолчанию для этого магазина.</span><span class="sxs-lookup"><span data-stu-id="a9842-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="a9842-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="a9842-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="a9842-142">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="a9842-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="a9842-143">Щелкните "Атрибуты канала".</span><span class="sxs-lookup"><span data-stu-id="a9842-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="a9842-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a9842-144">Click New.</span></span>
35. <span data-ttu-id="a9842-145">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="a9842-146">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="a9842-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="a9842-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a9842-148">Click Save.</span></span>
39. <span data-ttu-id="a9842-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9842-149">Close the page.</span></span>
40. <span data-ttu-id="a9842-150">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="a9842-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="a9842-151">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="a9842-151">Click Payment methods.</span></span>
42. <span data-ttu-id="a9842-152">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a9842-152">Click New.</span></span>
43. <span data-ttu-id="a9842-153">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="a9842-154">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="a9842-155">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="a9842-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="a9842-156">В поле "Номер счета" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="a9842-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="a9842-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a9842-157">Click Save.</span></span>
48. <span data-ttu-id="a9842-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9842-158">Close the page.</span></span>
49. <span data-ttu-id="a9842-159">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="a9842-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="a9842-160">Щелкните "Декларирование наличности".</span><span class="sxs-lookup"><span data-stu-id="a9842-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="a9842-161">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a9842-161">Click New.</span></span>
52. <span data-ttu-id="a9842-162">В поле "Сумма в валюте проводки" введите число.</span><span class="sxs-lookup"><span data-stu-id="a9842-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="a9842-163">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="a9842-164">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="a9842-165">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="a9842-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a9842-166">Click Save.</span></span>
57. <span data-ttu-id="a9842-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9842-167">Close the page.</span></span>
58. <span data-ttu-id="a9842-168">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="a9842-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="a9842-169">Щелкните "Назначение групп указателей магазинов".</span><span class="sxs-lookup"><span data-stu-id="a9842-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="a9842-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a9842-170">Click New.</span></span>
61. <span data-ttu-id="a9842-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a9842-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="a9842-172">В поле "Группа указателей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a9842-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="a9842-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a9842-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="a9842-174">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a9842-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="a9842-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a9842-175">Click Save.</span></span>
66. <span data-ttu-id="a9842-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a9842-176">Close the page.</span></span>


