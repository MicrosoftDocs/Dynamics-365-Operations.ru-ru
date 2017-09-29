--- 
title: "Создание иерархии отчетности организации"
description: "Эта процедура используется для создания иерархии отчетности для организации."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f593c59660abcf5b0d5771ddd9daced6ec5fbfb4
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="4bb9c-103">Создание иерархии отчетности организации</span><span class="sxs-lookup"><span data-stu-id="4bb9c-103">Create an organization report hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bb9c-104">Эта процедура используется для создания иерархии отчетности для организации.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="4bb9c-105">Назначение этой записи — провести вас по иерархии аналитик, чтобы вы могли продолжать до тех пор, пока не будет создана вся структура отчетности организации.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="4bb9c-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="4bb9c-107">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="4bb9c-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-108">Click New.</span></span>
3. <span data-ttu-id="4bb9c-109">В поле HierarchyTypeComboBox выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="4bb9c-110">Выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="4bb9c-111">Тип Иерархия классификации аналитик используется для определения правил и целей отчетности.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="4bb9c-112">Он поддерживает все аналитики, например объекты затрат, элементы затрат и статистические аналитики.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="4bb9c-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-113">Click Create.</span></span>
5. <span data-ttu-id="4bb9c-114">В поле "Имя иерархии аналитик" введите "Организация USP2".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="4bb9c-115">В поле "Аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-116">Выберите "Центры затрат".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="4bb9c-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-117">Click Save.</span></span>
8. <span data-ttu-id="4bb9c-118">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="4bb9c-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-119">Click New.</span></span>
10. <span data-ttu-id="4bb9c-120">В поле "Имя узла" введите "Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="4bb9c-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-121">Click Save.</span></span>
12. <span data-ttu-id="4bb9c-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-122">Click New.</span></span>
13. <span data-ttu-id="4bb9c-123">В поле "Имя узла" введите "Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="4bb9c-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-124">Click Save.</span></span>
15. <span data-ttu-id="4bb9c-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-125">Click New.</span></span>
16. <span data-ttu-id="4bb9c-126">В поле "Имя узла" введите "Восточный регион".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="4bb9c-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-127">Click Save.</span></span>
18. <span data-ttu-id="4bb9c-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-128">Click New.</span></span>
19. <span data-ttu-id="4bb9c-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="4bb9c-130">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-131">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="4bb9c-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-132">Click Save.</span></span>
22. <span data-ttu-id="4bb9c-133">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="4bb9c-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-134">Click New.</span></span>
24. <span data-ttu-id="4bb9c-135">В поле "Имя узла" введите "Западный регион".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="4bb9c-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-136">Click Save.</span></span>
26. <span data-ttu-id="4bb9c-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-137">Click New.</span></span>
27. <span data-ttu-id="4bb9c-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="4bb9c-139">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-140">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="4bb9c-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-141">Click Save.</span></span>
30. <span data-ttu-id="4bb9c-142">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="4bb9c-143">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-143">Click New.</span></span>
32. <span data-ttu-id="4bb9c-144">В поле "Имя узла" введите "Центры затрат финансового директора".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="4bb9c-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-145">Click Save.</span></span>
34. <span data-ttu-id="4bb9c-146">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-146">Click New.</span></span>
35. <span data-ttu-id="4bb9c-147">В поле "Имя узла" введите "Маркетинговая камп.".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="4bb9c-148">В поле "Имя узла" введите "Маркетинговая кампания".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="4bb9c-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-149">Click Save.</span></span>
38. <span data-ttu-id="4bb9c-150">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-150">Click New.</span></span>
39. <span data-ttu-id="4bb9c-151">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="4bb9c-152">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-153">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="4bb9c-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-154">Click Save.</span></span>
42. <span data-ttu-id="4bb9c-155">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-155">In the tree, select 'Oganization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="4bb9c-156">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-156">Click New.</span></span>
44. <span data-ttu-id="4bb9c-157">В поле "Имя узла" введите "Выставки".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="4bb9c-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-158">Click Save.</span></span>
46. <span data-ttu-id="4bb9c-159">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-159">Click New.</span></span>
47. <span data-ttu-id="4bb9c-160">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="4bb9c-161">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-162">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="4bb9c-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-163">Click Save.</span></span>
50. <span data-ttu-id="4bb9c-164">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="4bb9c-165">В поле "Имя узла" введите "Центры затрат директора по ИТ".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="4bb9c-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-166">Click Save.</span></span>
53. <span data-ttu-id="4bb9c-167">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-167">Click New.</span></span>
54. <span data-ttu-id="4bb9c-168">В поле "Имя узла" введите "Центры обработки вызовов".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="4bb9c-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-169">Click Save.</span></span>
56. <span data-ttu-id="4bb9c-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-170">Click New.</span></span>
57. <span data-ttu-id="4bb9c-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="4bb9c-172">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="4bb9c-173">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="4bb9c-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="4bb9c-174">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4bb9c-174">Click Save.</span></span>


