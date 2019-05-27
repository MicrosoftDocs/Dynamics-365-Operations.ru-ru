---
title: Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544779"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="63119-103">Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="63119-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63119-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="63119-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="63119-105">Эта конфигурация формата будет определять формат электронных документов, используемых для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="63119-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="63119-106">В этом примере вам предстоит создать конфигурацию формата для компании-образца Litware, Inc. Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Сопоставление модели с выбранными источникам данных".</span><span class="sxs-lookup"><span data-stu-id="63119-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="63119-107">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="63119-107">Create a new format configuration</span></span>
1. <span data-ttu-id="63119-108">Перейдите в раздел **Управление организацией > Рабочие области > Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="63119-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="63119-109">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="63119-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="63119-110">В дереве выберите **Платежи (упрощенная модель)**.</span><span class="sxs-lookup"><span data-stu-id="63119-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="63119-111">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63119-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="63119-112">Если пункт **Создать конфигурацию** отсутствует, необходимо включить режим конструктора на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="63119-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="63119-113">В поле **Создать** введите **Формат, основанный на модели данных PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="63119-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="63119-114">В поле **Имя** введите **BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="63119-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="63119-115">В поле **Описание** введите **Формат платежа поставщикам BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="63119-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="63119-116">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="63119-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="63119-117">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="63119-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="63119-118">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="63119-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="63119-119">Можно определить конкретный формат электронного документа.</span><span class="sxs-lookup"><span data-stu-id="63119-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="63119-120">Оставьте это поле пустым, если вы хотите выбирать формат во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="63119-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="63119-121">В поле **Определение модели данных** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="63119-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="63119-122">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="63119-122">Click **Create configuration**.</span></span> <span data-ttu-id="63119-123">Новая конфигурация создана.</span><span class="sxs-lookup"><span data-stu-id="63119-123">A new configuration has been created.</span></span> <span data-ttu-id="63119-124">Черновую версию можно использовать для хранения разрабатываемого формата для управления электронными документами.</span><span class="sxs-lookup"><span data-stu-id="63119-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="63119-125">Разработка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="63119-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="63119-126">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="63119-126">Click **Designer**.</span></span>
2. <span data-ttu-id="63119-127">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63119-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="63119-128">В дереве выберите **Общее\Файл**.</span><span class="sxs-lookup"><span data-stu-id="63119-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="63119-129">В поле **Имя** введите **XML**.</span><span class="sxs-lookup"><span data-stu-id="63119-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="63119-130">В поле **Кодировка** введите **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="63119-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="63119-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-131">Click **OK**.</span></span>
7. <span data-ttu-id="63119-132">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63119-132">Click **Add**.</span></span>
8. <span data-ttu-id="63119-133">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="63119-134">В поле **Имя** введите **Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="63119-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="63119-135">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-135">Click **OK**.</span></span>
11. <span data-ttu-id="63119-136">В дереве выберите **Xml\Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="63119-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="63119-137">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="63119-138">В поле **Имя** введите **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="63119-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="63119-139">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-139">Click **OK**.</span></span>
15. <span data-ttu-id="63119-140">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="63119-141">В поле "Имя" введите **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="63119-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="63119-142">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-142">Click **OK**.</span></span>
18. <span data-ttu-id="63119-143">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="63119-144">В поле **Имя** введите **Платежи**.</span><span class="sxs-lookup"><span data-stu-id="63119-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="63119-145">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-145">Click **OK**.</span></span>
21. <span data-ttu-id="63119-146">В дереве выберите **Xml\Сообщение\Платежи**.</span><span class="sxs-lookup"><span data-stu-id="63119-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="63119-147">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="63119-148">В поле **Имя** введите **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="63119-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="63119-149">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-149">Click **OK**.</span></span>
25. <span data-ttu-id="63119-150">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="63119-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="63119-151">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63119-151">Click **Add**.</span></span>
27. <span data-ttu-id="63119-152">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="63119-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="63119-153">В поле "Имя" введите **Код**.</span><span class="sxs-lookup"><span data-stu-id="63119-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="63119-154">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-154">Click **OK**.</span></span>
30. <span data-ttu-id="63119-155">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="63119-155">Click **Add**.</span></span>
31. <span data-ttu-id="63119-156">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="63119-157">В поле "Имя" введите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="63119-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="63119-158">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-158">Click **OK**.</span></span>
34. <span data-ttu-id="63119-159">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="63119-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="63119-160">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="63119-161">В поле "Имя" введите **Имя**.</span><span class="sxs-lookup"><span data-stu-id="63119-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="63119-162">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-162">Click **OK**.</span></span>
38. <span data-ttu-id="63119-163">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="63119-164">В поле **Имя** введите **Банк**.</span><span class="sxs-lookup"><span data-stu-id="63119-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="63119-165">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-165">Click **OK**.</span></span>
41. <span data-ttu-id="63119-166">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк**.</span><span class="sxs-lookup"><span data-stu-id="63119-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="63119-167">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="63119-168">В поле **Имя** введите **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="63119-169">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-169">Click **OK**.</span></span>
45. <span data-ttu-id="63119-170">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="63119-171">В поле **Имя** введите **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="63119-172">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-172">Click **OK**.</span></span>
48. <span data-ttu-id="63119-173">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="63119-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="63119-174">Щелкните **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="63119-174">Click **Copy**.</span></span>
50. <span data-ttu-id="63119-175">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="63119-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="63119-176">Щелкните **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="63119-176">Click **Paste**.</span></span>
52. <span data-ttu-id="63119-177">В поле **Имя** введите **Плательщик**,</span><span class="sxs-lookup"><span data-stu-id="63119-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="63119-178">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="63119-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="63119-179">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="63119-180">В поле **Имя** введите **Валюта**.</span><span class="sxs-lookup"><span data-stu-id="63119-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="63119-181">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-181">Click **OK**.</span></span>
57. <span data-ttu-id="63119-182">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="63119-183">В поле **Имя** введите **Описание**.</span><span class="sxs-lookup"><span data-stu-id="63119-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="63119-184">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-184">Click **OK**.</span></span>
60. <span data-ttu-id="63119-185">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="63119-186">В поле "Имя" введите **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="63119-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="63119-187">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-187">Click **OK**.</span></span>
63. <span data-ttu-id="63119-188">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="63119-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="63119-189">В поле "Имя" введите **Сумма**.</span><span class="sxs-lookup"><span data-stu-id="63119-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="63119-190">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="63119-191">Подготовка компонентов формата для сопоставления с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="63119-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="63119-192">В дереве выберите **Xml\Сообщение\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="63119-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="63119-193">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63119-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="63119-194">В дереве выберите **Текст\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="63119-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="63119-195">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="63119-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="63119-196">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-196">Click **OK**.</span></span>
6. <span data-ttu-id="63119-197">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="63119-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="63119-198">Нажмите кнопку **Добавить DateTime**.</span><span class="sxs-lookup"><span data-stu-id="63119-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="63119-199">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="63119-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="63119-200">В поле **Тип DateTime** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="63119-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="63119-201">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-201">Click **OK**.</span></span>
11. <span data-ttu-id="63119-202">В дереве выберите **Xml\Сообщение\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="63119-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="63119-203">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="63119-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="63119-204">В дереве выберите **Текст\строка**.</span><span class="sxs-lookup"><span data-stu-id="63119-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="63119-205">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-205">Click **OK**.</span></span>
15. <span data-ttu-id="63119-206">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="63119-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="63119-207">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-207">Click **Add String**.</span></span>
17. <span data-ttu-id="63119-208">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-208">Click **OK**.</span></span>
18. <span data-ttu-id="63119-209">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="63119-210">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-210">Click **Add String**.</span></span>
20. <span data-ttu-id="63119-211">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-211">Click **OK**.</span></span>
21. <span data-ttu-id="63119-212">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="63119-213">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-213">Click **Add String**.</span></span>
23. <span data-ttu-id="63119-214">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-214">Click **OK**.</span></span>
24. <span data-ttu-id="63119-215">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="63119-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="63119-216">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-216">Click **Add String**.</span></span>
26. <span data-ttu-id="63119-217">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-217">Click **OK**.</span></span>
27. <span data-ttu-id="63119-218">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="63119-219">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-219">Click **Add String**.</span></span>
29. <span data-ttu-id="63119-220">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-220">Click **OK**.</span></span>
30. <span data-ttu-id="63119-221">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="63119-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="63119-222">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-222">Click **Add String**.</span></span>
32. <span data-ttu-id="63119-223">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-223">Click **OK**.</span></span>
33. <span data-ttu-id="63119-224">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Валюта**.</span><span class="sxs-lookup"><span data-stu-id="63119-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="63119-225">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-225">Click **Add String**.</span></span>
35. <span data-ttu-id="63119-226">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-226">Click **OK**.</span></span>
36. <span data-ttu-id="63119-227">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Описание**.</span><span class="sxs-lookup"><span data-stu-id="63119-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="63119-228">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-228">Click **Add String**.</span></span>
38. <span data-ttu-id="63119-229">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-229">Click **OK**.</span></span>
39. <span data-ttu-id="63119-230">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Сумма**.</span><span class="sxs-lookup"><span data-stu-id="63119-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="63119-231">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="63119-231">Click **Add String**.</span></span>
41. <span data-ttu-id="63119-232">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="63119-232">Click **OK**.</span></span>
42. <span data-ttu-id="63119-233">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="63119-233">Click **Save**.</span></span>
43. <span data-ttu-id="63119-234">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="63119-234">Close the page.</span></span>

