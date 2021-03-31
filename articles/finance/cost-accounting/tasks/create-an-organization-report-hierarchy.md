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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3db8465c462caffeaf6bd12d17c4b61355ed8eed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208759"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="9dcd2-103">Создание иерархии отчетности организации</span><span class="sxs-lookup"><span data-stu-id="9dcd2-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dcd2-104">Эта процедура используется для создания иерархии отчетности для организации.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="9dcd2-105">Назначение этой записи — провести вас по иерархии аналитик, чтобы вы могли продолжать до тех пор, пока не будет создана вся структура отчетности организации.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="9dcd2-106">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="9dcd2-107">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="9dcd2-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-108">Click New.</span></span>
3. <span data-ttu-id="9dcd2-109">В поле HierarchyTypeComboBox выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="9dcd2-110">Выберите "Иерархия классификации аналитик".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="9dcd2-111">Тип Иерархия классификации аналитик используется для определения правил и целей отчетности.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="9dcd2-112">Он поддерживает все аналитики, например объекты затрат, элементы затрат и статистические аналитики.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="9dcd2-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-113">Click Create.</span></span>
5. <span data-ttu-id="9dcd2-114">В поле "Имя иерархии аналитик" введите "Организация USP2".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="9dcd2-115">В поле "Аналитика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-116">Выберите "Центры затрат".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="9dcd2-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-117">Click Save.</span></span>
8. <span data-ttu-id="9dcd2-118">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="9dcd2-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-119">Click New.</span></span>
10. <span data-ttu-id="9dcd2-120">В поле "Имя узла" введите "Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="9dcd2-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-121">Click Save.</span></span>
12. <span data-ttu-id="9dcd2-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-122">Click New.</span></span>
13. <span data-ttu-id="9dcd2-123">В поле "Имя узла" введите "Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="9dcd2-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-124">Click Save.</span></span>
15. <span data-ttu-id="9dcd2-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-125">Click New.</span></span>
16. <span data-ttu-id="9dcd2-126">В поле "Имя узла" введите "Восточный регион".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="9dcd2-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-127">Click Save.</span></span>
18. <span data-ttu-id="9dcd2-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-128">Click New.</span></span>
19. <span data-ttu-id="9dcd2-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="9dcd2-130">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-131">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="9dcd2-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-132">Click Save.</span></span>
22. <span data-ttu-id="9dcd2-133">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат генерального директора".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="9dcd2-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-134">Click New.</span></span>
24. <span data-ttu-id="9dcd2-135">В поле "Имя узла" введите "Западный регион".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="9dcd2-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-136">Click Save.</span></span>
26. <span data-ttu-id="9dcd2-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-137">Click New.</span></span>
27. <span data-ttu-id="9dcd2-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="9dcd2-139">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-140">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="9dcd2-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-141">Click Save.</span></span>
30. <span data-ttu-id="9dcd2-142">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="9dcd2-143">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-143">Click New.</span></span>
32. <span data-ttu-id="9dcd2-144">В поле "Имя узла" введите "Центры затрат финансового директора".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="9dcd2-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-145">Click Save.</span></span>
34. <span data-ttu-id="9dcd2-146">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-146">Click New.</span></span>
35. <span data-ttu-id="9dcd2-147">В поле "Имя узла" введите "Маркетинговая камп.".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="9dcd2-148">В поле "Имя узла" введите "Маркетинговая кампания".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="9dcd2-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-149">Click Save.</span></span>
38. <span data-ttu-id="9dcd2-150">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-150">Click New.</span></span>
39. <span data-ttu-id="9dcd2-151">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="9dcd2-152">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-153">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="9dcd2-154">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-154">Click Save.</span></span>
42. <span data-ttu-id="9dcd2-155">В дереве выберите "Организация USP2\Генеральный директор\Центры затрат финансового директора".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="9dcd2-156">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-156">Click New.</span></span>
44. <span data-ttu-id="9dcd2-157">В поле "Имя узла" введите "Выставки".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="9dcd2-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-158">Click Save.</span></span>
46. <span data-ttu-id="9dcd2-159">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-159">Click New.</span></span>
47. <span data-ttu-id="9dcd2-160">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="9dcd2-161">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-162">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="9dcd2-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-163">Click Save.</span></span>
50. <span data-ttu-id="9dcd2-164">В дереве выберите "Организация USP2\Генеральный директор".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="9dcd2-165">В поле "Имя узла" введите "Центры затрат директора по ИТ".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="9dcd2-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-166">Click Save.</span></span>
53. <span data-ttu-id="9dcd2-167">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-167">Click New.</span></span>
54. <span data-ttu-id="9dcd2-168">В поле "Имя узла" введите "Центры обработки вызовов".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="9dcd2-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-169">Click Save.</span></span>
56. <span data-ttu-id="9dcd2-170">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-170">Click New.</span></span>
57. <span data-ttu-id="9dcd2-171">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="9dcd2-172">В поле "Из элемента аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9dcd2-173">Выберите элемент аналитики, соответствующий узлу.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="9dcd2-174">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9dcd2-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]