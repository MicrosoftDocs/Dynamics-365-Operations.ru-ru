---
title: Создание иерархии отчетности организации
description: Эта процедура используется для создания иерархии отчетности для организации.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5684c710b8e167a4a39f106eb3c0fd77e3011dbd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187851"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="6d1dc-103">Создание иерархии отчетности организации</span><span class="sxs-lookup"><span data-stu-id="6d1dc-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d1dc-104">Эта процедура используется для создания иерархии отчетности для организации.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="6d1dc-105">Назначение этой записи — провести вас по иерархии аналитик, чтобы вы могли продолжать до тех пор, пока не будет создана вся структура отчетности организации.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="6d1dc-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="6d1dc-107">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6d1dc-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-108">Click New.</span></span>
3. <span data-ttu-id="6d1dc-109">В поле HierarchyTypeComboBox выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="6d1dc-110">Выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="6d1dc-111">Тип Иерархия классификации аналитик используется для определения правил и целей отчетности.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="6d1dc-112">Он поддерживает все аналитики, например объекты затрат, элементы затрат и статистические аналитики.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="6d1dc-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-113">Click Create.</span></span>
5. <span data-ttu-id="6d1dc-114">В поле "Имя иерархии аналитик" введите "Организация USP2".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="6d1dc-115">В поле "Аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-116">Выберите "Центры затрат".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="6d1dc-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-117">Click Save.</span></span>
8. <span data-ttu-id="6d1dc-118">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="6d1dc-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-119">Click New.</span></span>
10. <span data-ttu-id="6d1dc-120">В поле "Имя узла" введите "Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="6d1dc-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-121">Click Save.</span></span>
12. <span data-ttu-id="6d1dc-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-122">Click New.</span></span>
13. <span data-ttu-id="6d1dc-123">В поле "Имя узла" введите "Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="6d1dc-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-124">Click Save.</span></span>
15. <span data-ttu-id="6d1dc-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-125">Click New.</span></span>
16. <span data-ttu-id="6d1dc-126">В поле "Имя узла" введите "Восточный регион".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="6d1dc-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-127">Click Save.</span></span>
18. <span data-ttu-id="6d1dc-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-128">Click New.</span></span>
19. <span data-ttu-id="6d1dc-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6d1dc-130">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-131">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="6d1dc-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-132">Click Save.</span></span>
22. <span data-ttu-id="6d1dc-133">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="6d1dc-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-134">Click New.</span></span>
24. <span data-ttu-id="6d1dc-135">В поле "Имя узла" введите "Западный регион".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="6d1dc-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-136">Click Save.</span></span>
26. <span data-ttu-id="6d1dc-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-137">Click New.</span></span>
27. <span data-ttu-id="6d1dc-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="6d1dc-139">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-140">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="6d1dc-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-141">Click Save.</span></span>
30. <span data-ttu-id="6d1dc-142">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="6d1dc-143">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-143">Click New.</span></span>
32. <span data-ttu-id="6d1dc-144">В поле "Имя узла" введите "Центры затрат финансового директора".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="6d1dc-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-145">Click Save.</span></span>
34. <span data-ttu-id="6d1dc-146">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-146">Click New.</span></span>
35. <span data-ttu-id="6d1dc-147">В поле "Имя узла" введите "Маркетинговая камп.".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="6d1dc-148">В поле "Имя узла" введите "Маркетинговая кампания".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="6d1dc-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-149">Click Save.</span></span>
38. <span data-ttu-id="6d1dc-150">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-150">Click New.</span></span>
39. <span data-ttu-id="6d1dc-151">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="6d1dc-152">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-153">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="6d1dc-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-154">Click Save.</span></span>
42. <span data-ttu-id="6d1dc-155">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат финансового директора".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="6d1dc-156">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-156">Click New.</span></span>
44. <span data-ttu-id="6d1dc-157">В поле "Имя узла" введите "Выставки".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="6d1dc-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-158">Click Save.</span></span>
46. <span data-ttu-id="6d1dc-159">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-159">Click New.</span></span>
47. <span data-ttu-id="6d1dc-160">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="6d1dc-161">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-162">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="6d1dc-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-163">Click Save.</span></span>
50. <span data-ttu-id="6d1dc-164">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="6d1dc-165">В поле "Имя узла" введите "Центры затрат директора по ИТ".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="6d1dc-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-166">Click Save.</span></span>
53. <span data-ttu-id="6d1dc-167">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-167">Click New.</span></span>
54. <span data-ttu-id="6d1dc-168">В поле "Имя узла" введите "Центры обработки вызовов".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="6d1dc-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-169">Click Save.</span></span>
56. <span data-ttu-id="6d1dc-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-170">Click New.</span></span>
57. <span data-ttu-id="6d1dc-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="6d1dc-172">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6d1dc-173">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="6d1dc-174">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d1dc-174">Click Save.</span></span>

