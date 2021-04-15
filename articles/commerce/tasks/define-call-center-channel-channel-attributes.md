---
title: Создание каналов центра обработки вызовов и определение атрибутов каналов
description: Эта процедура содержит указания по созданию нового канала и определению атрибутов канала.
author: mugunthanm
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b053ea3a5792d016cfe4850f07c65de97fbfc9e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802703"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="3e2b9-103">Создание каналов центра обработки вызовов и определение атрибутов каналов</span><span class="sxs-lookup"><span data-stu-id="3e2b9-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e2b9-104">Эта процедура содержит указания по созданию нового канала Commerce и определению атрибутов канала.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="3e2b9-105">В качестве компании с демонстрационными данными для создания этой задачи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="3e2b9-106">Эта процедура предназначена для роли "ИТ Commerce".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="3e2b9-107">Создание нового магазина</span><span class="sxs-lookup"><span data-stu-id="3e2b9-107">Create new store</span></span>
1. <span data-ttu-id="3e2b9-108">Пойдите к Все рабочие области > Развертывание канала.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="3e2b9-109">Щелкните "Новый канал".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-109">Click New channel.</span></span>
3. <span data-ttu-id="3e2b9-110">Щелкните "Магазин".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-110">Click Store.</span></span>
4. <span data-ttu-id="3e2b9-111">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3e2b9-112">В поле "Номер магазина" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="3e2b9-113">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3e2b9-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3e2b9-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3e2b9-116">В поле "Часовой пояс магазина" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="3e2b9-117">В поле "Профиль канала" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3e2b9-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3e2b9-119">В поле "Язык" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="3e2b9-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="3e2b9-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="3e2b9-122">В поле "Налоговая группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="3e2b9-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="3e2b9-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="3e2b9-125">В поле "Адресная книга клиентов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3e2b9-126">Выберите адресную книгу, используемую для связывания клиентов с этим магазином.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="3e2b9-127">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="3e2b9-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="3e2b9-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-129">Click Select.</span></span>
22. <span data-ttu-id="3e2b9-130">В поле "Адресная книга сотрудников" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3e2b9-131">Выберите адресную книгу, используемую для связывания кассиров с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="3e2b9-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="3e2b9-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="3e2b9-134">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-134">Click Select.</span></span>
26. <span data-ttu-id="3e2b9-135">В поле "Клиент по умолчанию" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="3e2b9-136">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="3e2b9-137">Разверните или сверните раздел "Макет экрана".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="3e2b9-138">В поле "Код макета экрана" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3e2b9-139">Выберите макета экрана POS по умолчанию для этого магазина.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="3e2b9-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="3e2b9-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="3e2b9-142">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="3e2b9-143">Щелкните "Атрибуты канала".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="3e2b9-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-144">Click New.</span></span>
35. <span data-ttu-id="3e2b9-145">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="3e2b9-146">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="3e2b9-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="3e2b9-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-148">Click Save.</span></span>
39. <span data-ttu-id="3e2b9-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-149">Close the page.</span></span>
40. <span data-ttu-id="3e2b9-150">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="3e2b9-151">Щелкните "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-151">Click Payment methods.</span></span>
42. <span data-ttu-id="3e2b9-152">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-152">Click New.</span></span>
43. <span data-ttu-id="3e2b9-153">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="3e2b9-154">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="3e2b9-155">Разверните или сверните раздел "Разноска".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="3e2b9-156">В поле "Номер счета" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="3e2b9-157">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-157">Click Save.</span></span>
48. <span data-ttu-id="3e2b9-158">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-158">Close the page.</span></span>
49. <span data-ttu-id="3e2b9-159">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="3e2b9-160">Щелкните "Декларирование наличности".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="3e2b9-161">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-161">Click New.</span></span>
52. <span data-ttu-id="3e2b9-162">В поле "Сумма в валюте проводки" введите число.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="3e2b9-163">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="3e2b9-164">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="3e2b9-165">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="3e2b9-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-166">Click Save.</span></span>
57. <span data-ttu-id="3e2b9-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-167">Close the page.</span></span>
58. <span data-ttu-id="3e2b9-168">В области действий щелкните "Настроить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="3e2b9-169">Щелкните "Назначение групп указателей магазинов".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="3e2b9-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-170">Click New.</span></span>
61. <span data-ttu-id="3e2b9-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="3e2b9-172">В поле "Группа указателей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="3e2b9-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="3e2b9-174">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="3e2b9-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3e2b9-175">Click Save.</span></span>
66. <span data-ttu-id="3e2b9-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3e2b9-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]