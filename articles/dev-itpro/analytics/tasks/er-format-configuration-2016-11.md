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
ms.sourcegitcommit: 29e19b6d91e5761178627ef2051f3385f5d7cfe5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/08/2019
ms.locfileid: "377557"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="f1f00-103">Электронная отчетность — Создание конфигурации формата (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="f1f00-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1f00-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать конфигурацию формата для электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f1f00-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="f1f00-105">Эта конфигурация формата будет определять формат электронных документов, используемых для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="f1f00-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="f1f00-106">В этом примере вам предстоит создать конфигурацию формата для компании-образца Litware, Inc. Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Сопоставление модели с выбранными источникам данных".</span><span class="sxs-lookup"><span data-stu-id="f1f00-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f1f00-107">Создание новой конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="f1f00-107">Create a new format configuration</span></span>
1. <span data-ttu-id="f1f00-108">Перейдите в раздел **Управление организацией > Рабочие области > Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="f1f00-109">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="f1f00-110">В дереве выберите **Платежи (упрощенная модель)**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="f1f00-111">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f1f00-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="f1f00-112">Если пункт **Создать конфигурацию** отсутствует, необходимо включить режим конструктора на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="f1f00-113">В поле **Создать** введите **Формат, основанный на модели данных PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="f1f00-114">В поле **Имя** введите **BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="f1f00-115">В поле **Описание** введите **Формат платежа поставщикам BACS (Великобритания, вымышленный)**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="f1f00-116">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="f1f00-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="f1f00-117">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f1f00-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="f1f00-118">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="f1f00-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="f1f00-119">Можно определить конкретный формат электронного документа.</span><span class="sxs-lookup"><span data-stu-id="f1f00-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="f1f00-120">Оставьте это поле пустым, если вы хотите выбирать формат во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1f00-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="f1f00-121">В поле **Определение модели данных** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f1f00-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="f1f00-122">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-122">Click **Create configuration**.</span></span> <span data-ttu-id="f1f00-123">Новая конфигурация создана.</span><span class="sxs-lookup"><span data-stu-id="f1f00-123">A new configuration has been created.</span></span> <span data-ttu-id="f1f00-124">Черновую версию можно использовать для хранения разрабатываемого формата для управления электронными документами.</span><span class="sxs-lookup"><span data-stu-id="f1f00-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="f1f00-125">Разработка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="f1f00-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="f1f00-126">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-126">Click **Designer**.</span></span>
2. <span data-ttu-id="f1f00-127">Щелкните **Добавить корень**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f1f00-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="f1f00-128">В дереве выберите **Общее\Файл**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="f1f00-129">В поле **Имя** введите **XML**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="f1f00-130">В поле **Кодировка** введите **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="f1f00-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-131">Click **OK**.</span></span>
7. <span data-ttu-id="f1f00-132">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-132">Click **Add**.</span></span>
8. <span data-ttu-id="f1f00-133">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="f1f00-134">В поле **Имя** введите **Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="f1f00-135">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-135">Click **OK**.</span></span>
11. <span data-ttu-id="f1f00-136">В дереве выберите **Xml\Сообщение**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="f1f00-137">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="f1f00-138">В поле **Имя** введите **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="f1f00-139">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-139">Click **OK**.</span></span>
15. <span data-ttu-id="f1f00-140">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="f1f00-141">В поле "Имя" введите **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="f1f00-142">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-142">Click **OK**.</span></span>
18. <span data-ttu-id="f1f00-143">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="f1f00-144">В поле **Имя** введите **Платежи**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="f1f00-145">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-145">Click **OK**.</span></span>
21. <span data-ttu-id="f1f00-146">В дереве выберите **Xml\Сообщение\Платежи**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="f1f00-147">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="f1f00-148">В поле **Имя** введите **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="f1f00-149">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-149">Click **OK**.</span></span>
25. <span data-ttu-id="f1f00-150">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="f1f00-151">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-151">Click **Add**.</span></span>
27. <span data-ttu-id="f1f00-152">В дереве выберите **XML\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="f1f00-153">В поле "Имя" введите **Код**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="f1f00-154">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-154">Click **OK**.</span></span>
30. <span data-ttu-id="f1f00-155">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-155">Click **Add**.</span></span>
31. <span data-ttu-id="f1f00-156">В дереве выберите **XML\Элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="f1f00-157">В поле "Имя" введите **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="f1f00-158">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-158">Click **OK**.</span></span>
34. <span data-ttu-id="f1f00-159">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="f1f00-160">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="f1f00-161">В поле "Имя" введите **Имя**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="f1f00-162">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-162">Click **OK**.</span></span>
38. <span data-ttu-id="f1f00-163">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="f1f00-164">В поле **Имя** введите **Банк**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="f1f00-165">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-165">Click **OK**.</span></span>
41. <span data-ttu-id="f1f00-166">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="f1f00-167">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="f1f00-168">В поле **Имя** введите **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="f1f00-169">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-169">Click **OK**.</span></span>
45. <span data-ttu-id="f1f00-170">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="f1f00-171">В поле **Имя** введите **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="f1f00-172">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-172">Click **OK**.</span></span>
48. <span data-ttu-id="f1f00-173">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="f1f00-174">Щелкните **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-174">Click **Copy**.</span></span>
50. <span data-ttu-id="f1f00-175">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="f1f00-176">Щелкните **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-176">Click **Paste**.</span></span>
52. <span data-ttu-id="f1f00-177">В поле **Имя** введите **Плательщик**,</span><span class="sxs-lookup"><span data-stu-id="f1f00-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="f1f00-178">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="f1f00-179">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="f1f00-180">В поле **Имя** введите **Валюта**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="f1f00-181">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-181">Click **OK**.</span></span>
57. <span data-ttu-id="f1f00-182">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="f1f00-183">В поле **Имя** введите **Описание**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="f1f00-184">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-184">Click **OK**.</span></span>
60. <span data-ttu-id="f1f00-185">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="f1f00-186">В поле "Имя" введите **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="f1f00-187">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-187">Click **OK**.</span></span>
63. <span data-ttu-id="f1f00-188">Щелкните **Добавить элемент**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="f1f00-189">В поле "Имя" введите **Сумма**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="f1f00-190">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="f1f00-191">Подготовка компонентов формата для сопоставления с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="f1f00-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="f1f00-192">В дереве выберите **Xml\Сообщение\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="f1f00-193">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f1f00-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="f1f00-194">В дереве выберите **Текст\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="f1f00-195">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="f1f00-196">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-196">Click **OK**.</span></span>
6. <span data-ttu-id="f1f00-197">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="f1f00-198">Нажмите кнопку **Добавить DateTime**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="f1f00-199">В поле **Формат** введите **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="f1f00-200">В поле **Тип DateTime** выберите **Дата**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="f1f00-201">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-201">Click **OK**.</span></span>
11. <span data-ttu-id="f1f00-202">В дереве выберите **Xml\Сообщение\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="f1f00-203">Щелкните **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f1f00-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="f1f00-204">В дереве выберите **Текст\строка**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="f1f00-205">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-205">Click **OK**.</span></span>
15. <span data-ttu-id="f1f00-206">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="f1f00-207">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-207">Click **Add String**.</span></span>
17. <span data-ttu-id="f1f00-208">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-208">Click **OK**.</span></span>
18. <span data-ttu-id="f1f00-209">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="f1f00-210">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-210">Click **Add String**.</span></span>
20. <span data-ttu-id="f1f00-211">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-211">Click **OK**.</span></span>
21. <span data-ttu-id="f1f00-212">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="f1f00-213">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-213">Click **Add String**.</span></span>
23. <span data-ttu-id="f1f00-214">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-214">Click **OK**.</span></span>
24. <span data-ttu-id="f1f00-215">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="f1f00-216">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-216">Click **Add String**.</span></span>
26. <span data-ttu-id="f1f00-217">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-217">Click **OK**.</span></span>
27. <span data-ttu-id="f1f00-218">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="f1f00-219">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-219">Click **Add String**.</span></span>
29. <span data-ttu-id="f1f00-220">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-220">Click **OK**.</span></span>
30. <span data-ttu-id="f1f00-221">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="f1f00-222">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-222">Click **Add String**.</span></span>
32. <span data-ttu-id="f1f00-223">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-223">Click **OK**.</span></span>
33. <span data-ttu-id="f1f00-224">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Валюта**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="f1f00-225">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-225">Click **Add String**.</span></span>
35. <span data-ttu-id="f1f00-226">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-226">Click **OK**.</span></span>
36. <span data-ttu-id="f1f00-227">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Описание**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="f1f00-228">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-228">Click **Add String**.</span></span>
38. <span data-ttu-id="f1f00-229">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-229">Click **OK**.</span></span>
39. <span data-ttu-id="f1f00-230">В дереве выберите **Xml\Сообщение\Платежи\Номенклатура\Сумма**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="f1f00-231">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-231">Click **Add String**.</span></span>
41. <span data-ttu-id="f1f00-232">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-232">Click **OK**.</span></span>
42. <span data-ttu-id="f1f00-233">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f1f00-233">Click **Save**.</span></span>
43. <span data-ttu-id="f1f00-234">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f1f00-234">Close the page.</span></span>

