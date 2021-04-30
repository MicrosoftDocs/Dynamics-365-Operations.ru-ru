---
title: Учебник Regression Suite Automation Tool
description: В этом разделе показано, как использовать средство Regression Suite Automation Tool (RSAT). В нем описываются различные функции и приводятся примеры использования расширенного сценария.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a194e14c76827650e6752f331081ebe0c2130a13
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866164"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="b9bc6-104">Учебник Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="b9bc6-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b9bc6-105">Загрузите и сохраните эту страницу в формате PDF с помощью средств веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="b9bc6-106">В этом учебнике представлено несколько дополнительных функций средства Regression Suite Automation Tool (RSAT), включается демонстрационное назначение, а также описываются стратегия и ключевые моменты обучения.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="b9bc6-107">Важные функции RSAT и регистратора задач</span><span class="sxs-lookup"><span data-stu-id="b9bc6-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="b9bc6-108">Проверка значения поля</span><span class="sxs-lookup"><span data-stu-id="b9bc6-108">Validate a field value</span></span>

<span data-ttu-id="b9bc6-109">RSAT позволяет включить в тестовый случай шаги проверки для проверки ожидаемых значений.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="b9bc6-110">Сведения об этой функции см. в статье [Проверка ожидаемых значений](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="b9bc6-111">В следующем примере показано, как можно использовать эту функцию для проверки того, что запасы в наличии больше 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="b9bc6-112">В демонстрационных данных компании **USMF** создайте запись задачи, которая имеет следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="b9bc6-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="b9bc6-113">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="b9bc6-114">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b9bc6-115">Например, отфильтруйте по значению **1000** поле **Номер номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="b9bc6-116">Выберите **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="b9bc6-117">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b9bc6-118">Например, отфильтруйте поле **Сайт** по значению **1**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="b9bc6-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="b9bc6-120">Убедитесь, что значение поля **Доступное общее количество** равно **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="b9bc6-121">Сохраните запись задачи как **запись разработчика** и вложите ее в тестовый случай в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="b9bc6-122">Добавьте тестовый случай в план испытаний и загрузите тестовый случай в RSAT.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="b9bc6-123">Откройте файл параметров Excel и перейдите на вкладку **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="b9bc6-124">Чтобы обеспечить, что запасы в наличии всегда будут больше **0**, перейдите на шаг **Проверить общее доступное количество** и измените значение с **411** на **0**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="b9bc6-125">Измените значение поля **Оператор** со знака равенства (**=**) на знак "больше" (**\>**).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="b9bc6-126">Сохраните и закройте файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="b9bc6-127">Выберите **Отправить**, чтобы сохранить изменения, внесенные в файл параметров Excel, в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="b9bc6-128">Теперь если в поле **Доступное общее количество** для указанной номенклатуры в складских запасах значение больше 0 (нуля), тест проходит успешно, независимо от фактического значения запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="b9bc6-129">Сохраненные переменные и цепочки тестовых случаев</span><span class="sxs-lookup"><span data-stu-id="b9bc6-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="b9bc6-130">Одной из важнейших функций RSAT является связывание тестовых случаев, то есть, возможность тестов передавать переменные в другие тесты.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="b9bc6-131">Дополнительные сведения см. в статье [Копирование переменных в цепочку тестовых случаев](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="b9bc6-132">Производный тестовый случай</span><span class="sxs-lookup"><span data-stu-id="b9bc6-132">Derived test case</span></span>

<span data-ttu-id="b9bc6-133">RSAT позволяет использовать одну запись задач с несколькими тестовыми случаями, что позволяет выполнять задачу с различными конфигурациями данных.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="b9bc6-134">Дополнительные сведения см. в статье [Производные тестовые случаи](rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="b9bc6-135">Проверка уведомлений и сообщений</span><span class="sxs-lookup"><span data-stu-id="b9bc6-135">Validate notifications and messages</span></span>

<span data-ttu-id="b9bc6-136">Эта функция может использоваться для проверки, произошло ли действие.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="b9bc6-137">Например, когда производственный заказ создается, оценивается, а затем запускается, в приложении отображается сообщение "Производство — начало", уведомляющее о запуске производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Уведомление "Производство — начало"](./media/use_rsa_tool_05.png)

<span data-ttu-id="b9bc6-139">Вы можете проверить это сообщение через RSAT, вводя текст сообщения на вкладке **MessageValidation** файла параметров Excel для соответствующей записи.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Вкладка проверки сообщения](./media/use_rsa_tool_06.png)

<span data-ttu-id="b9bc6-141">После запуска тестового случая сообщение в файле параметров Excel сравнивается с отображаемым сообщением.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="b9bc6-142">Если сообщения не совпадают, тестовый случай будет неудачным.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="b9bc6-143">На вкладке **MessageValidation** в файле параметров Excel можно ввести более одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="b9bc6-144">Сообщения также могут быть сообщениями об ошибках или предупреждениями, а не информационными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="b9bc6-145">Снимок</span><span class="sxs-lookup"><span data-stu-id="b9bc6-145">Snapshot</span></span>

<span data-ttu-id="b9bc6-146">Эта функция делает снимки экрана шагов, которые были выполнены во время записи задачи.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="b9bc6-147">Это полезно для целей аудита или отладки.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="b9bc6-148">Для использования этой функции откройте файл **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение следующего элемента с **false** на **true**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="b9bc6-149">При выполнении тестового случая RSAT создает снимки (изображения) шагов в папке воспроизведения тестовых случаев в рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="b9bc6-150">При использовании старой версии RSAT изображения сохраняются по пути **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, при этом для каждого выполняемого тестового случая создается отдельная папка.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="b9bc6-151">Назначение</span><span class="sxs-lookup"><span data-stu-id="b9bc6-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="b9bc6-152">Сценарий</span><span class="sxs-lookup"><span data-stu-id="b9bc6-152">Scenario</span></span>

1. <span data-ttu-id="b9bc6-153">Конструктор продуктов создает новый выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="b9bc6-154">Менеджер производства запускает производственный заказ, чтобы восстановить уровень запасов в две единицы.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="b9bc6-155">Производство начинается и завершает производственный заказ, и проверяет, что количество в наличии равно двум единицам.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="b9bc6-156">Группа продавцов получает заказ на четыре единицы нового продукта.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="b9bc6-157">Поэтому группа продаж обновляет чистые потребности с помощью динамического плана.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="b9bc6-158">Поскольку дополнительные мощности отсутствуют, для политики заказа по умолчанию устанавливается значение "купить вместо создания".</span><span class="sxs-lookup"><span data-stu-id="b9bc6-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="b9bc6-159">Поэтому создается спланированный заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="b9bc6-160">Покупатель добавляет поставщика, подтверждает запланированный заказ на покупку, затем утверждает заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="b9bc6-161">Когда купленные товары поступают в магазин, оператор магазина выполняет поиск товаров соответствующих заказов на покупку и получает товары.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="b9bc6-162">Так как заказ готов, товары могут комплектоваться и упаковываться по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="b9bc6-163">Финансовый отдел выполняет разноску накладной по покупке и накладной по продаже.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="b9bc6-164">На следующем рисунке показана последовательность операций для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-164">The following illustration shows the flow for this scenario.</span></span>

![Последовательность операций для демонстрационного сценария](./media/use_rsa_tool_14.png)

<span data-ttu-id="b9bc6-166">На следующем рисунке показана иерархия бизнес-процессов для этого сценария в средстве моделирования бизнес-процессов LCS.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Бизнес-процессы для демонстрационного сценария](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="b9bc6-168">Стратегия — ключевое обучение</span><span class="sxs-lookup"><span data-stu-id="b9bc6-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="b9bc6-169">Данные</span><span class="sxs-lookup"><span data-stu-id="b9bc6-169">Data</span></span>

- <span data-ttu-id="b9bc6-170">Убедитесь в том, что имеются репрезентативные объемы данных (копия производственных/золотых данных конфигурации и перенесенные данные).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="b9bc6-171">При создании новых данных с помощью регистратора задач создайте имена тестов, которые не будут конфликтовать с существующими именами (например, используйте префикс, такой как **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="b9bc6-172">Для повторного выполнения тестов в средах без уровней 1 используйте функцию восстановление на момент времени Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="b9bc6-173">Хотя можно использовать функции Excel **RANDOM** и **NOW** для создания уникальной комбинации, усилия весьма высоки.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="b9bc6-174">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="b9bc6-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="b9bc6-175">Регистратор задач</span><span class="sxs-lookup"><span data-stu-id="b9bc6-175">Task recorder</span></span>

- <span data-ttu-id="b9bc6-176">Прежде чем начать запись, определите сценарии.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="b9bc6-177">Хорошо управляемый проект имеет предопределенные сценарии тестирования.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="b9bc6-178">Чтобы создать тестовый случай, необходимо оценить, насколько предсказуемым являются результаты этих сценариев тестирования.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="b9bc6-179">Разделите записи, если они выполняются другими ролями, или если имеется время ожидания или внешнее событие до следующего шага.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="b9bc6-180">Не следует выбирать значения в списках.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="b9bc6-181">Вместо этого используйте текстовые форматы, такие как **FIFO**, **AudioRM** и **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="b9bc6-182">При выборе в списке записывается позиция значения в списке, а не само значение.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="b9bc6-183">Если в этот список добавлены элементы, положение значения может измениться</span><span class="sxs-lookup"><span data-stu-id="b9bc6-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="b9bc6-184">Поэтому запись будет использовать другой параметр, и остальная часть сценария может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="b9bc6-185">Подумайте о поведении нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-185">Think about multi-user behavior.</span></span> <span data-ttu-id="b9bc6-186">Например, не следует предполагать, что вновь созданный заказ на продажу всегда будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="b9bc6-187">Вместо этого для поиска правильного заказа обязательно следует использовать фильтр.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="b9bc6-188">Используйте функцию копирования в регистраторе задач для сохранения имени вновь созданного продукта, чтобы его можно было использовать в связанных тестовых случаях.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="b9bc6-189">Используйте функцию проверки в регистраторе задач для установки контрольных точек, которые проверяют правильность выполнения шагов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="b9bc6-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="b9bc6-190">RSAT</span></span>

- <span data-ttu-id="b9bc6-191">Чтобы выполнить тест в другой компании, можно изменить эту компанию на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b9bc6-192">Убедитесь, что параметры и данные доступны в новой выбранной компании.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="b9bc6-193">Тестового пользователя можно изменить на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b9bc6-194">Укажите код электронной почты пользователя, который будет выполнять тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="b9bc6-195">Таким образом, тестовый случай может быть выполнен с помощью разрешений безопасности указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="b9bc6-196">Чтобы подождать, пока начнется тест, можно определить паузу на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b9bc6-197">Эта пауза может использоваться в пакетном задании (например, если рабочий процесс должен выполняться до того, как будет выполнен следующий шаг).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="b9bc6-198">Дополнительные сценарии</span><span class="sxs-lookup"><span data-stu-id="b9bc6-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="b9bc6-199">CLI</span><span class="sxs-lookup"><span data-stu-id="b9bc6-199">CLI</span></span>

<span data-ttu-id="b9bc6-200">RSAT можно вызывать из окна **Командная строка** или **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="b9bc6-201">Убедитесь, что для переменной среды **TestRoot** установлен путь установки RSAT.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="b9bc6-202">(В Microsoft Windows откройте **Панель управления**, выберите пункт **Система и безопасность \> Система \> Дополнительные параметры системы**, затем выберите **Переменные среды**.)</span><span class="sxs-lookup"><span data-stu-id="b9bc6-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="b9bc6-203">Откройте окно **Командная строка** или **PowerShell** от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="b9bc6-204">Перейдите в каталог установки RSAT.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="b9bc6-205">Выведите список всех команд.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-205">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="b9bc6-206">?</span><span class="sxs-lookup"><span data-stu-id="b9bc6-206">?</span></span>

<span data-ttu-id="b9bc6-207">Отображение справки обо всех доступных командах и их параметрах.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="b9bc6-208">?: Необязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-208">?: Optional parameters</span></span>

<span data-ttu-id="b9bc6-209">`command`: где ``[command]`` — одна из команд, указанных далее.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="b9bc6-210">о программе</span><span class="sxs-lookup"><span data-stu-id="b9bc6-210">about</span></span>

<span data-ttu-id="b9bc6-211">Отображает текущую версию.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="b9bc6-212">cls</span><span class="sxs-lookup"><span data-stu-id="b9bc6-212">cls</span></span>

<span data-ttu-id="b9bc6-213">Очищает экран.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="b9bc6-214">загрузить</span><span class="sxs-lookup"><span data-stu-id="b9bc6-214">download</span></span>

<span data-ttu-id="b9bc6-215">Загружает вложения для указанного тестового случая в выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="b9bc6-216">Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b9bc6-217">Используйте любое значение из первого столбца в качестве параметра **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="b9bc6-218">загрузить: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-218">download: required parameters</span></span>

+ <span data-ttu-id="b9bc6-219">`test_case_id`: представляет идентификатор тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b9bc6-220">`output_dir`: представляет выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b9bc6-221">Каталог должна существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="b9bc6-222">загрузить: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="b9bc6-223">изменить</span><span class="sxs-lookup"><span data-stu-id="b9bc6-223">edit</span></span>

<span data-ttu-id="b9bc6-224">Позволяет открыть файл параметров в программе Excel и изменить его.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="b9bc6-225">изменить: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-225">edit: required parameters</span></span>

+ <span data-ttu-id="b9bc6-226">`excel_file`: должен содержать полный путь к существующему файлу Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="b9bc6-227">изменить: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="b9bc6-228">создать</span><span class="sxs-lookup"><span data-stu-id="b9bc6-228">generate</span></span>

<span data-ttu-id="b9bc6-229">Создает для указанного тестового случая в выходном каталоге параметры выполнения тестов и файлы параметров.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="b9bc6-230">Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b9bc6-231">Используйте любое значение из первого столбца в качестве параметра **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="b9bc6-232">создать: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-232">generate: required parameters</span></span>

+ <span data-ttu-id="b9bc6-233">`test_case_id`: представляет идентификатор тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b9bc6-234">`output_dir`: представляет выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b9bc6-235">Каталог должна существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="b9bc6-236">создать: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="b9bc6-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="b9bc6-237">generatederived</span></span>

<span data-ttu-id="b9bc6-238">Создает новый тестовый случай, производный от предоставленного тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="b9bc6-239">Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b9bc6-240">Используйте любое значение из первого столбца в качестве параметра **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="b9bc6-241">generatederived: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="b9bc6-242">`parent_test_case_id`: представляет идентификатор родительского тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="b9bc6-243">`test_plan_id`: представляет идентификатор плана тестирования.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="b9bc6-244">`test_suite_id`: представляет идентификатор набора тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="b9bc6-245">generatederived: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="b9bc6-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="b9bc6-246">generatetestonly</span></span>

<span data-ttu-id="b9bc6-247">Создает для указанного тестового случая в выходном каталоге только файл параметров.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="b9bc6-248">Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b9bc6-249">Используйте любое значение из первого столбца в качестве параметра **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="b9bc6-250">generatetestonly: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="b9bc6-251">`test_case_id`: представляет идентификатор тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b9bc6-252">`output_dir`: представляет выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b9bc6-253">Каталог должна существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="b9bc6-254">generatetestonly: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="b9bc6-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="b9bc6-255">generatetestsuite</span></span>

<span data-ttu-id="b9bc6-256">Создает все тестовые случаи для указанного набора в выходном каталоге.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="b9bc6-257">Можно использовать команду ``listtestsuitenames`` для извлечения всех доступных наборов тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="b9bc6-258">Используйте любое значение из столбца в качестве параметра **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="b9bc6-259">generatetestsuite: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="b9bc6-260">`test_suite_name`: представляет имя набора тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="b9bc6-261">`output_dir`: представляет выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b9bc6-262">Каталог должна существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="b9bc6-263">generatetestsuite: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="b9bc6-264">справка</span><span class="sxs-lookup"><span data-stu-id="b9bc6-264">help</span></span>

<span data-ttu-id="b9bc6-265">Идентично значению [?](#section)</span><span class="sxs-lookup"><span data-stu-id="b9bc6-265">Identical to the [?](#section)</span></span> <span data-ttu-id="b9bc6-266">команда.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="b9bc6-267">списка</span><span class="sxs-lookup"><span data-stu-id="b9bc6-267">list</span></span>

<span data-ttu-id="b9bc6-268">Список всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="b9bc6-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="b9bc6-269">listtestplans</span></span>

<span data-ttu-id="b9bc6-270">Список всех доступных планов тестирования.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="b9bc6-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="b9bc6-271">listtestsuite</span></span>

<span data-ttu-id="b9bc6-272">Перечисляет тестовые случаи для указанного набора тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="b9bc6-273">Можно использовать команду ``listtestsuitenames`` для извлечения всех доступных наборов тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="b9bc6-274">Используйте любое значение из первого столбца в качестве параметра **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="b9bc6-275">listtestsuite: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="b9bc6-276">`suite_name`: имя нужного набора.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="b9bc6-277">listtestsuite: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="b9bc6-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="b9bc6-278">listtestsuitenames</span></span>

<span data-ttu-id="b9bc6-279">Список всех доступных наборов тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="b9bc6-280">воспроизведение</span><span class="sxs-lookup"><span data-stu-id="b9bc6-280">playback</span></span>

<span data-ttu-id="b9bc6-281">Воспроизводит тестовый случай с помощью файла Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="b9bc6-282">воспроизведение: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-282">playback: required parameters</span></span>

+ <span data-ttu-id="b9bc6-283">`excel_file`: полный путь к файлу Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="b9bc6-284">Файл должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="b9bc6-285">воспроизведение: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="b9bc6-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="b9bc6-286">playbackbyid</span></span>

<span data-ttu-id="b9bc6-287">Воспроизведение нескольких тестовых случаев одновременно.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="b9bc6-288">Можно использовать команду ``list`` для извлечения всех доступных тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b9bc6-289">Используйте любое значение из первого столбца в качестве параметра **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="b9bc6-290">playbackbyid: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="b9bc6-291">`test_case_id1`: идентификатор существующего тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="b9bc6-292">`test_case_id2`: идентификатор существующего тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="b9bc6-293">`test_case_idN`: идентификатор существующего тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="b9bc6-294">playbackbyid: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="b9bc6-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="b9bc6-295">playbackmany</span></span>

<span data-ttu-id="b9bc6-296">Воспроизведение нескольких тестовых случаев одновременно с использованием файлов Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="b9bc6-297">playbackmany: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="b9bc6-298">`excel_file1`: полный путь к файлу Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="b9bc6-299">Файл должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-299">File must exist.</span></span>
+ <span data-ttu-id="b9bc6-300">`excel_file2`: полный путь к файлу Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="b9bc6-301">Файл должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-301">File must exist.</span></span>
+ <span data-ttu-id="b9bc6-302">`excel_fileN`: полный путь к файлу Excel.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="b9bc6-303">Файл должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="b9bc6-304">playbackmany: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="b9bc6-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="b9bc6-305">playbacksuite</span></span>

<span data-ttu-id="b9bc6-306">Воспроизведение всех тестовых случаев из указанного набора тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="b9bc6-307">Можно использовать команду ``listtestsuitenames`` для извлечения всех доступных наборов тестов.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="b9bc6-308">Используйте любое значение из первого столбца в качестве параметра **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="b9bc6-309">playbacksuite: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="b9bc6-310">`suite_name`: имя нужного набора.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="b9bc6-311">playbacksuite: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="b9bc6-312">закрыть</span><span class="sxs-lookup"><span data-stu-id="b9bc6-312">quit</span></span>

<span data-ttu-id="b9bc6-313">Закрывает приложение.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="b9bc6-314">отправить</span><span class="sxs-lookup"><span data-stu-id="b9bc6-314">upload</span></span>

<span data-ttu-id="b9bc6-315">Отправляет все файлы, относящиеся к определенному набору тестов или тестовым случаям.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="b9bc6-316">отправить: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-316">upload: required parameters</span></span>

+ <span data-ttu-id="b9bc6-317">`suite_name`: все файлы, относящиеся к определенному набору тестов, будут отправлены.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="b9bc6-318">`testcase_id`: все файлы, относящиеся к определенному тестовому случаю, будут отправлены.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="b9bc6-319">отправить: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="b9bc6-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="b9bc6-320">uploadrecording</span></span>

<span data-ttu-id="b9bc6-321">Отправляет только файл записи, принадлежащий к определенным тестовым случаям.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="b9bc6-322">uploadrecording: обязательные параметры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="b9bc6-323">`testcase_id`: файл записи, принадлежащий к определенным тестовым случаям, будет отправлен.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="b9bc6-324">uploadrecording: примеры</span><span class="sxs-lookup"><span data-stu-id="b9bc6-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="b9bc6-325">использование</span><span class="sxs-lookup"><span data-stu-id="b9bc6-325">usage</span></span>

<span data-ttu-id="b9bc6-326">Описание двух способов вызова этого приложения: один — с использованием файла параметров по умолчанию, другой — с указанием файла параметров.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="b9bc6-327">Примеры Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9bc6-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="b9bc6-328">Выполнение тестового случая в цикле</span><span class="sxs-lookup"><span data-stu-id="b9bc6-328">Run a test case in a loop</span></span>

<span data-ttu-id="b9bc6-329">Имеется тестовый сценарий, создающий нового клиента.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="b9bc6-330">С помощью сценариев этот тестовый случай можно выполнить в цикле путем случайного выбора следующих данных перед выполнением каждой итерации:</span><span class="sxs-lookup"><span data-stu-id="b9bc6-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="b9bc6-331">Код клиента</span><span class="sxs-lookup"><span data-stu-id="b9bc6-331">Customer ID</span></span>
- <span data-ttu-id="b9bc6-332">Наименование Клиента</span><span class="sxs-lookup"><span data-stu-id="b9bc6-332">Customer name</span></span>
- <span data-ttu-id="b9bc6-333">Адрес клиента</span><span class="sxs-lookup"><span data-stu-id="b9bc6-333">Customer address</span></span>

<span data-ttu-id="b9bc6-334">Код клиента будет иметь формат *ATCUS\<number\>*, где \<number\> представляет собой значение в диапазоне от **000000001** до **999999999**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="b9bc6-335">В следующем примере для определения первого используемого номера используется один параметр, **start**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="b9bc6-336">Второй параметр **nr** служит для определения числа клиентов, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="b9bc6-337">Для каждой итерации параметры в файле параметров Excel изменяются с помощью функции UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="b9bc6-338">После этого командная строка RSAT вызывается в функции RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="b9bc6-339">Откройте интегрированную среду сценариев Microsoft Windows PowerShell (ISE) в режиме администратора и вставьте следующий код в окно с именем **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="b9bc6-340">Выполнение сценария, который зависит от данных в Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b9bc6-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="b9bc6-341">В следующем примере для поиска статуса заказа на покупку используется вызов по протоколу OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b9bc6-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="b9bc6-342">Если статус не равен **выставлена накладная**, можно, например, вызвать тестовый случай RSAT, который разносит накладную.</span><span class="sxs-lookup"><span data-stu-id="b9bc6-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]