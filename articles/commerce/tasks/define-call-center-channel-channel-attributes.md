---
title: Создание каналов центра обработки вызовов и определение атрибутов каналов
description: Эта процедура содержит указания по созданию нового канала розничной торговли и определению атрибутов канала.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4b6db1bfdaf17cd857a0a08515f1e0413994bd6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023801"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="91361-103">Создание каналов центра обработки вызовов и определение атрибутов каналов</span><span class="sxs-lookup"><span data-stu-id="91361-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="91361-104">Эта процедура содержит указания по созданию нового канала Commerce и определению атрибутов канала.</span><span class="sxs-lookup"><span data-stu-id="91361-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="91361-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="91361-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="91361-106">Эта процедура предназначена для роли "ИТ Commerce".</span><span class="sxs-lookup"><span data-stu-id="91361-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="91361-107">Создание нового магазина</span><span class="sxs-lookup"><span data-stu-id="91361-107">Create new store</span></span>
1. <span data-ttu-id="91361-108">Пойдите к Все рабочие области > Развертывание канала.</span><span class="sxs-lookup"><span data-stu-id="91361-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="91361-109">Щелкните "Новый канал".</span><span class="sxs-lookup"><span data-stu-id="91361-109">Click New channel.</span></span>
3. <span data-ttu-id="91361-110">Щелкните "Магазин".</span><span class="sxs-lookup"><span data-stu-id="91361-110">Click Store.</span></span>
4. <span data-ttu-id="91361-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91361-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="91361-112">В поле "Номер магазина" введите значение.</span><span class="sxs-lookup"><span data-stu-id="91361-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="91361-113">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="91361-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="91361-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="91361-116">В поле "Часовой пояс магазина" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="91361-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="91361-117">В поле "Профиль канала" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="91361-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="91361-119">В поле "Язык" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="91361-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="91361-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="91361-122">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="91361-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="91361-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="91361-125">В поле "Адресная книга клиентов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="91361-126">Выберите адресную книгу, используемую для связывания клиентов с этим магазином.</span><span class="sxs-lookup"><span data-stu-id="91361-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="91361-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="91361-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="91361-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="91361-129">Click Select.</span></span>
22. <span data-ttu-id="91361-130">В поле "Адресная книга сотрудников" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="91361-131">Выберите адресную книгу, используемую для связывания кассиров с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="91361-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="91361-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="91361-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="91361-134">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="91361-134">Click Select.</span></span>
26. <span data-ttu-id="91361-135">В поле "Клиент по умолчанию" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="91361-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="91361-137">Разверните или сверните раздел "Макет экрана".</span><span class="sxs-lookup"><span data-stu-id="91361-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="91361-138">В поле "Код макета экрана" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="91361-139">Выберите макета экрана POS по умолчанию для этого магазина.</span><span class="sxs-lookup"><span data-stu-id="91361-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="91361-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="91361-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="91361-142">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="91361-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="91361-143">Щелкните "Атрибуты канала".</span><span class="sxs-lookup"><span data-stu-id="91361-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="91361-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91361-144">Click New.</span></span>
35. <span data-ttu-id="91361-145">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="91361-146">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="91361-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="91361-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="91361-148">Click Save.</span></span>
39. <span data-ttu-id="91361-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91361-149">Close the page.</span></span>
40. <span data-ttu-id="91361-150">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="91361-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="91361-151">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="91361-151">Click Payment methods.</span></span>
42. <span data-ttu-id="91361-152">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91361-152">Click New.</span></span>
43. <span data-ttu-id="91361-153">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="91361-154">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="91361-155">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="91361-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="91361-156">В поле "Номер счета" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="91361-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="91361-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="91361-157">Click Save.</span></span>
48. <span data-ttu-id="91361-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91361-158">Close the page.</span></span>
49. <span data-ttu-id="91361-159">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="91361-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="91361-160">Щелкните "Декларирование наличности".</span><span class="sxs-lookup"><span data-stu-id="91361-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="91361-161">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91361-161">Click New.</span></span>
52. <span data-ttu-id="91361-162">В поле "Сумма в валюте проводки" введите число.</span><span class="sxs-lookup"><span data-stu-id="91361-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="91361-163">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="91361-164">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="91361-165">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="91361-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="91361-166">Click Save.</span></span>
57. <span data-ttu-id="91361-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91361-167">Close the page.</span></span>
58. <span data-ttu-id="91361-168">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="91361-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="91361-169">Щелкните "Назначение групп указателей магазинов".</span><span class="sxs-lookup"><span data-stu-id="91361-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="91361-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="91361-170">Click New.</span></span>
61. <span data-ttu-id="91361-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="91361-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="91361-172">В поле "Группа указателей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="91361-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="91361-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="91361-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="91361-174">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91361-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="91361-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="91361-175">Click Save.</span></span>
66. <span data-ttu-id="91361-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="91361-176">Close the page.</span></span>

