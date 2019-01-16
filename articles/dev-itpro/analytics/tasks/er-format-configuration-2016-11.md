--- 
title: "Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать конфигурацию формата для электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: ru-ru
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="5e6c9-103">Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="5e6c9-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e6c9-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="5e6c9-105">Эта конфигурация формата будет определять формат электронных документов, используемых для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="5e6c9-106">В этом примере вам предстоит создать конфигурацию формата для компании-образца Litware, Inc. Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Сопоставление модели с выбранными источникам данных".</span><span class="sxs-lookup"><span data-stu-id="5e6c9-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5e6c9-107">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="5e6c9-107">Create a new format configuration</span></span>
1. <span data-ttu-id="5e6c9-108">Перейдите в раздел **Управление организацией > Рабочие области > Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="5e6c9-109">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="5e6c9-110">В дереве выберите **Платежи (упрощенная модель)**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="5e6c9-111">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="5e6c9-112">Если пункт **Создать конфигурацию** отсутствует, необходимо включить режим конструктора на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="5e6c9-113">В поле **Создать** введите **Формат, основанный на модели данных PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="5e6c9-114">В поле **Имя** введите **BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="5e6c9-115">В поле **Описание** введите **Формат платежа поставщикам BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="5e6c9-116">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5e6c9-117">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5e6c9-118">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="5e6c9-119">Можно определить конкретный формат электронного документа.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="5e6c9-120">Оставьте это поле пустым, если вы хотите выбирать формат во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="5e6c9-121">В поле **Определение модели данных** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="5e6c9-122">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-122">Click **Create configuration**.</span></span> <span data-ttu-id="5e6c9-123">Новая конфигурация создана.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-123">A new configuration has been created.</span></span> <span data-ttu-id="5e6c9-124">Черновую версию можно использовать для хранения разрабатываемого формата для управления электронными документами.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="5e6c9-125">Если пункт **Создать конфигурацию** отсутствует, необходимо включить режим конструктора на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="5e6c9-126">Разработка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="5e6c9-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="5e6c9-127">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-127">Click **Designer**.</span></span>
2. <span data-ttu-id="5e6c9-128">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5e6c9-129">В дереве выберите **Общее\Файл**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="5e6c9-130">В поле **Имя** введите **XML**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="5e6c9-131">В поле **Кодировка** введите **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="5e6c9-132">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-132">Click **OK**.</span></span>
7. <span data-ttu-id="5e6c9-133">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-133">Click **Add**.</span></span>
8. <span data-ttu-id="5e6c9-134">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="5e6c9-135">В поле **Имя** введите **Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="5e6c9-136">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-136">Click **OK**.</span></span>
11. <span data-ttu-id="5e6c9-137">В дереве выберите **Xml\Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="5e6c9-138">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="5e6c9-139">В поле **Имя** введите **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="5e6c9-140">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-140">Click **OK**.</span></span>
15. <span data-ttu-id="5e6c9-141">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="5e6c9-142">В поле "Имя" введите **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="5e6c9-143">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-143">Click **OK**.</span></span>
18. <span data-ttu-id="5e6c9-144">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="5e6c9-145">В поле **Имя** введите **Платежи**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="5e6c9-146">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-146">Click **OK**.</span></span>
21. <span data-ttu-id="5e6c9-147">В дереве выберите **Xml\Сообщение\Платежи**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="5e6c9-148">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="5e6c9-149">В поле **Имя** введите **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="5e6c9-150">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-150">Click **OK**.</span></span>
25. <span data-ttu-id="5e6c9-151">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="5e6c9-152">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-152">Click **Add**.</span></span>
27. <span data-ttu-id="5e6c9-153">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="5e6c9-154">В поле "Имя" введите **Код**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="5e6c9-155">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-155">Click **OK**.</span></span>
30. <span data-ttu-id="5e6c9-156">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-156">Click **Add**.</span></span>
31. <span data-ttu-id="5e6c9-157">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="5e6c9-158">В поле "Имя" введите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="5e6c9-159">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-159">Click **OK**.</span></span>
34. <span data-ttu-id="5e6c9-160">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="5e6c9-161">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="5e6c9-162">В поле "Имя" введите **Имя**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="5e6c9-163">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-163">Click **OK**.</span></span>
38. <span data-ttu-id="5e6c9-164">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="5e6c9-165">В поле **Имя** введите **Банк**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="5e6c9-166">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-166">Click **OK**.</span></span>
41. <span data-ttu-id="5e6c9-167">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="5e6c9-168">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="5e6c9-169">В поле **Имя** введите **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="5e6c9-170">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-170">Click **OK**.</span></span>
45. <span data-ttu-id="5e6c9-171">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="5e6c9-172">В поле **Имя** введите **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="5e6c9-173">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-173">Click **OK**.</span></span>
48. <span data-ttu-id="5e6c9-174">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="5e6c9-175">Щелкните **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-175">Click **Copy**.</span></span>
50. <span data-ttu-id="5e6c9-176">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="5e6c9-177">Щелкните **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-177">Click **Paste**.</span></span>
52. <span data-ttu-id="5e6c9-178">В поле **Имя** введите **Плательщик**,</span><span class="sxs-lookup"><span data-stu-id="5e6c9-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="5e6c9-179">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="5e6c9-180">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="5e6c9-181">В поле **Имя** введите **Валюта**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="5e6c9-182">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-182">Click **OK**.</span></span>
57. <span data-ttu-id="5e6c9-183">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="5e6c9-184">В поле **Имя** введите **Описание**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="5e6c9-185">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-185">Click **OK**.</span></span>
60. <span data-ttu-id="5e6c9-186">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="5e6c9-187">В поле "Имя" введите **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="5e6c9-188">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-188">Click **OK**.</span></span>
63. <span data-ttu-id="5e6c9-189">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="5e6c9-190">В поле "Имя" введите **Сумма**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="5e6c9-191">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="5e6c9-192">Подготовка компонентов формата для сопоставления с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="5e6c9-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="5e6c9-193">В дереве выберите **Xml\Сообщение\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="5e6c9-194">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="5e6c9-195">В дереве выберите **Текст\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="5e6c9-196">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="5e6c9-197">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-197">Click **OK**.</span></span>
6. <span data-ttu-id="5e6c9-198">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="5e6c9-199">Нажмите кнопку **Добавить DateTime**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="5e6c9-200">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="5e6c9-201">В поле **Тип DateTime** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="5e6c9-202">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-202">Click **OK**.</span></span>
11. <span data-ttu-id="5e6c9-203">В дереве выберите **Xml\Сообщение\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="5e6c9-204">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="5e6c9-205">В дереве выберите **Текст\строка**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="5e6c9-206">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-206">Click **OK**.</span></span>
15. <span data-ttu-id="5e6c9-207">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="5e6c9-208">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-208">Click **Add String**.</span></span>
17. <span data-ttu-id="5e6c9-209">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-209">Click **OK**.</span></span>
18. <span data-ttu-id="5e6c9-210">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="5e6c9-211">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-211">Click **Add String**.</span></span>
20. <span data-ttu-id="5e6c9-212">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-212">Click **OK**.</span></span>
21. <span data-ttu-id="5e6c9-213">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="5e6c9-214">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-214">Click **Add String**.</span></span>
23. <span data-ttu-id="5e6c9-215">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-215">Click **OK**.</span></span>
24. <span data-ttu-id="5e6c9-216">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="5e6c9-217">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-217">Click **Add String**.</span></span>
26. <span data-ttu-id="5e6c9-218">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-218">Click **OK**.</span></span>
27. <span data-ttu-id="5e6c9-219">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="5e6c9-220">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-220">Click **Add String**.</span></span>
29. <span data-ttu-id="5e6c9-221">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-221">Click **OK**.</span></span>
30. <span data-ttu-id="5e6c9-222">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="5e6c9-223">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-223">Click **Add String**.</span></span>
32. <span data-ttu-id="5e6c9-224">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-224">Click **OK**.</span></span>
33. <span data-ttu-id="5e6c9-225">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Валюта**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="5e6c9-226">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-226">Click **Add String**.</span></span>
35. <span data-ttu-id="5e6c9-227">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-227">Click **OK**.</span></span>
36. <span data-ttu-id="5e6c9-228">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Описание**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="5e6c9-229">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-229">Click **Add String**.</span></span>
38. <span data-ttu-id="5e6c9-230">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-230">Click **OK**.</span></span>
39. <span data-ttu-id="5e6c9-231">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Сумма**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="5e6c9-232">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-232">Click **Add String**.</span></span>
41. <span data-ttu-id="5e6c9-233">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-233">Click **OK**.</span></span>
42. <span data-ttu-id="5e6c9-234">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-234">Click **Save**.</span></span>
43. <span data-ttu-id="5e6c9-235">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5e6c9-235">Close the page.</span></span>


