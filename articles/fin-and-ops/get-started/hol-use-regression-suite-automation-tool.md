---
title: Учебник по использованию средства Regression Suite Automation Tool
description: В этом разделе показано, как использовать средство Regression Suite Automation Tool (RSAT). В нем описываются различные функции и приводятся примеры использования расширенного сценария.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 8f3cd6a27ba0e09e48c0562aff46791228bb46b5
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703860"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="b70c5-104">Учебник по использованию средства Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="b70c5-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b70c5-105">Загрузите и сохраните эту страницу в формате PDF с помощью средств веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="b70c5-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="b70c5-106">В этом учебнике представлено несколько дополнительных функций средства Regression Suite Automation Tool (RSAT), включается демонстрационное назначение, а также описываются стратегия и ключевые моменты обучения.</span><span class="sxs-lookup"><span data-stu-id="b70c5-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="b70c5-107">Функции RSAT/регистратора задач</span><span class="sxs-lookup"><span data-stu-id="b70c5-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="b70c5-108">Проверка значения поля</span><span class="sxs-lookup"><span data-stu-id="b70c5-108">Validate a field value</span></span>

<span data-ttu-id="b70c5-109">Дополнительные сведения об этой функции см. в разделе [Создание новой записи задачи с функцией проверки](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="b70c5-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="b70c5-110">Сохраненная переменная</span><span class="sxs-lookup"><span data-stu-id="b70c5-110">Saved variable</span></span>

<span data-ttu-id="b70c5-111">Дополнительные сведения об этой функции см. в разделе [Изменение существующей записи задачи для создания сохраненной переменной](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="b70c5-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="b70c5-112">Производный тестовый случай</span><span class="sxs-lookup"><span data-stu-id="b70c5-112">Derived test case</span></span>

1. <span data-ttu-id="b70c5-113">Откройте средство Regression Suite Automation Tool (RSAT) и выберите оба тестовых случая, созданных в разделе [Настройка и установка средства Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b70c5-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="b70c5-114">Выберите **Создать \> Создать производный тестовый случай**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-114">Select **New \> Create derived test case**.</span></span>

    ![Команда создания производного тестового случая в меню создания](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="b70c5-116">Появится сообщение о том, что для каждого выбранного тестового случая в текущем наборе тестов будет создан производный тестовый случай, и что каждый производный тестовый случай будет иметь собственную копию файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="b70c5-117">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b70c5-118">При выполнении производного тестового случая он использует запись задачи своего родительского тестового случая и собственную копию файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="b70c5-119">Таким образом можно выполнить один и тот же тест с другими параметрами без необходимости поддержки более одной записи задачи.</span><span class="sxs-lookup"><span data-stu-id="b70c5-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="b70c5-120">Производный тестовый случай не обязательно должен входить в тот же набор тестов, что и его родительский тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="b70c5-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Окно сообщения](./media/use_rsa_tool_02.png)

    <span data-ttu-id="b70c5-122">Создаются два дополнительных производных тестовых случая, и для них установлен флажок **Производный?**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Созданные производные тестовые случаи](./media/use_rsa_tool_03.png)

    <span data-ttu-id="b70c5-124">Производный тестовый случай создается автоматически в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b70c5-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="b70c5-125">Он является дочерним элементом тестового случая **Создание нового продукта** и помечается с помощью специального ключевого слова: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="b70c5-126">Эти тестовые случаи также автоматически добавляются в план испытаний в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b70c5-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Ключевое слово RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="b70c5-128">Если по какой-либо причине производные тестовые случаи, которые были созданы, не находятся в нужном порядке, перейдите в Azure DevOps и измените порядок тестовых случаев в наборе тестов, чтобы RSAT мог выполнять их в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="b70c5-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="b70c5-129">Выберите производные тестовые случаи, затем выберите **Правка**, чтобы открыть соответствующие файлы параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="b70c5-130">Отредактируйте файлы параметров Excel так же, как и в случае редактирования родительских файлов.</span><span class="sxs-lookup"><span data-stu-id="b70c5-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="b70c5-131">Иными словами, убедитесь, что код продукта настроен таким образом, чтобы он был создан автоматически.</span><span class="sxs-lookup"><span data-stu-id="b70c5-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="b70c5-132">Кроме того, убедитесь, что сохраненная переменная скопирована в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="b70c5-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="b70c5-133">На вкладке **Общие** в обоих файлах параметров Excel обновите значение поля **Компания** на **USSI**, чтобы производные тестовые случаи запускались для другого юридического лица, отличного от родительского тестового случая.</span><span class="sxs-lookup"><span data-stu-id="b70c5-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="b70c5-134">Для выполнения тестовых случаев для конкретного пользователя (или роли, связанной с конкретным пользователем) можно обновить значение в поле **Тестовый пользователь**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="b70c5-135">Выберите **Выполнить**и убедитесь, что продукт создан как в юридическом лице USMF, так и в юридическом лице USSI.</span><span class="sxs-lookup"><span data-stu-id="b70c5-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="b70c5-136">Проверка уведомлений</span><span class="sxs-lookup"><span data-stu-id="b70c5-136">Validate notifications</span></span>

<span data-ttu-id="b70c5-137">Эта функция может использоваться для проверки, произошло ли действие.</span><span class="sxs-lookup"><span data-stu-id="b70c5-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="b70c5-138">Например, когда производственный заказ создается, оценивается, а затем запускается, отображается сообщение Microsoft Dynamics 365 for Finance and Operations "Производство — начало", уведомляющее о запуске производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="b70c5-138">For example, when a production order is created, estimated, and then started, Microsoft Dynamics 365 for Finance and Operations shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Уведомление "Производство — начало"](./media/use_rsa_tool_05.png)

<span data-ttu-id="b70c5-140">Вы можете проверить это сообщение через RSAT, вводя текст сообщения на вкладке **MessageValidation** файла параметров Excel для соответствующей записи.</span><span class="sxs-lookup"><span data-stu-id="b70c5-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Вкладка проверки сообщения](./media/use_rsa_tool_06.png)

<span data-ttu-id="b70c5-142">После запуска тестового случая сообщение в файле параметров Excel сравнивается с сообщением, отображаемым в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b70c5-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown in Finance and Operations.</span></span> <span data-ttu-id="b70c5-143">Если сообщения не совпадают, тестовый случай будет неудачным.</span><span class="sxs-lookup"><span data-stu-id="b70c5-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="b70c5-144">На вкладке **MessageValidation** в файле параметров Excel можно ввести более одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b70c5-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="b70c5-145">Сообщения также могут быть сообщениями об ошибках или предупреждениями, а не информационными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b70c5-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="b70c5-146">Проверка значений с помощью операторов</span><span class="sxs-lookup"><span data-stu-id="b70c5-146">Validate values by using operators</span></span>

<span data-ttu-id="b70c5-147">В предыдущих версиях RSAT можно было проверять значения только в том случае, если значение элемента управления равно ожидаемому значению.</span><span class="sxs-lookup"><span data-stu-id="b70c5-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="b70c5-148">Новая функция позволяет проверять, что переменная не равна, меньше или больше, чем заданное значение.</span><span class="sxs-lookup"><span data-stu-id="b70c5-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="b70c5-149">Для использования этой функции откройте файл **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение в следующем элементе с **false** на **true**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="b70c5-150">В файле параметров Excel появится новое поле **Оператор**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b70c5-151">Если использовалась старая версия RSAT, необходимо создать новые файлы параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Поле оператора](./media/use_rsa_tool_07.png)

<span data-ttu-id="b70c5-153">В следующем примере показано, как можно использовать эту функцию для проверки того, что запасы в наличии больше 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="b70c5-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="b70c5-154">В демонстрационных данных компании **USMF** создайте запись задачи, которая имеет следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="b70c5-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="b70c5-155">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="b70c5-156">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b70c5-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b70c5-157">Например, отфильтруйте по значению **1000** поле **Номер номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="b70c5-158">Выберите **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="b70c5-159">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="b70c5-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b70c5-160">Например, отфильтруйте поле **Сайт** по значению **1**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="b70c5-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b70c5-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="b70c5-162">Убедитесь, что значение поля **Доступное общее количество** равно **411,0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="b70c5-163">Сохраните запись задачи в библиотеке BMP в службах LCS и синхронизируйте ее с Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b70c5-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="b70c5-164">Добавьте тестовый случай в план испытаний и загрузите тестовый случай в RSAT.</span><span class="sxs-lookup"><span data-stu-id="b70c5-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="b70c5-165">Откройте файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-165">Open the Excel parameter file.</span></span> <span data-ttu-id="b70c5-166">На вкладке **InventOnhandItem** будет показан раздел **Проверить InventOnhandItem**, содержащий поле **Оператор**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Поле оператора](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="b70c5-168">Чтобы убедиться, что запасы в наличии всегда будут больше 0, измените значение в поле **Значение** с **411** на **0** и значение поля **Оператор** со знака равенства (**=**) на знак больше (**\>**).</span><span class="sxs-lookup"><span data-stu-id="b70c5-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Изменены значения полей "Значение" и "Оператор"](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="b70c5-170">Сохраните и закройте файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="b70c5-171">Выберите **Отправить**, чтобы сохранить изменения, внесенные в файл параметров Excel, в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b70c5-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="b70c5-172">Теперь если в поле **Доступное общее количество** для указанной номенклатуры в складских запасах значение больше 0 (нуля), тест проходит успешно, независимо от фактического значения запасов в наличии.</span><span class="sxs-lookup"><span data-stu-id="b70c5-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="b70c5-173">Журналы генератора</span><span class="sxs-lookup"><span data-stu-id="b70c5-173">Generator logs</span></span>

<span data-ttu-id="b70c5-174">Эта функция создает папку, содержащую журналы тестовых случаев, которые были запущены.</span><span class="sxs-lookup"><span data-stu-id="b70c5-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="b70c5-175">Для использования этой функции откройте файл **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение в следующем элементе с **false** на **true**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="b70c5-176">После запуска тестовых случаев можно найти файлы журнала в папке **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Папка GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="b70c5-178">Если перед изменением значения в файле. config были существующие тестовые случаи, журналы для этих тестовых случаев не создаются до тех пор, пока не будут созданы новые файлы выполнения тестов.</span><span class="sxs-lookup"><span data-stu-id="b70c5-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Команда создания только файлов выполнения тестов в меню создания](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="b70c5-180">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="b70c5-180">Snapshot</span></span>

<span data-ttu-id="b70c5-181">Эта функция делает снимки экрана шагов, которые были выполнены во время записи задачи.</span><span class="sxs-lookup"><span data-stu-id="b70c5-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="b70c5-182">Для использования этой функции откройте файл **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** в папке установки RSAT (например, **C:\\Program Files (x86)\\Regression Suite Automation Tool**) и измените значение следующего элемента с **false** на **true**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="b70c5-183">В папке **C:\\Users\\\<Имя_пользователя\>\\AppData\\Roaming\\regressionTool\\playback** для каждого выполняемого тестового случая создается отдельная папка.</span><span class="sxs-lookup"><span data-stu-id="b70c5-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Папка моментальных снимков для тестового случая](./media/use_rsa_tool_12.png)

<span data-ttu-id="b70c5-185">В каждой из этих папок можно найти снимки шагов, которые были выполнены во время выполнения тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="b70c5-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Файлы моментальных снимков](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="b70c5-187">Назначение</span><span class="sxs-lookup"><span data-stu-id="b70c5-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="b70c5-188">Сценарий</span><span class="sxs-lookup"><span data-stu-id="b70c5-188">Scenario</span></span>

1. <span data-ttu-id="b70c5-189">Конструктор продуктов создает новый выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="b70c5-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="b70c5-190">Менеджер производства запускает производственный заказ, чтобы восстановить уровень запасов в две единицы.</span><span class="sxs-lookup"><span data-stu-id="b70c5-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="b70c5-191">Производство начинается и завершает производственный заказ, и проверяет, что количество в наличии равно двум единицам.</span><span class="sxs-lookup"><span data-stu-id="b70c5-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="b70c5-192">Группа продавцов получает заказ на четыре единицы нового продукта.</span><span class="sxs-lookup"><span data-stu-id="b70c5-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="b70c5-193">Поэтому группа продаж обновляет чистые потребности с помощью динамического плана.</span><span class="sxs-lookup"><span data-stu-id="b70c5-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="b70c5-194">Поскольку дополнительные мощности отсутствуют, для политики заказа по умолчанию устанавливается значение "купить вместо создания".</span><span class="sxs-lookup"><span data-stu-id="b70c5-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="b70c5-195">Поэтому создается спланированный заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="b70c5-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="b70c5-196">Покупатель добавляет поставщика, подтверждает запланированный заказ на покупку, затем утверждает заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="b70c5-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="b70c5-197">Когда купленные товары поступают в магазин, оператор магазина выполняет поиск товаров соответствующих заказов на покупку и получает товары.</span><span class="sxs-lookup"><span data-stu-id="b70c5-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="b70c5-198">Так как заказ готов, товары могут комплектоваться и упаковываться по заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="b70c5-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="b70c5-199">Финансовый отдел выполняет разноску накладной по покупке и накладной по продаже.</span><span class="sxs-lookup"><span data-stu-id="b70c5-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="b70c5-200">На следующем рисунке показана последовательность операций для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="b70c5-200">The following illustration shows the flow for this scenario.</span></span>

![Последовательность операций для демонстрационного сценария](./media/use_rsa_tool_14.png)

<span data-ttu-id="b70c5-202">На следующем рисунке показаны бизнес-процессы для этого сценария в RSAT.</span><span class="sxs-lookup"><span data-stu-id="b70c5-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Бизнес-процессы для демонстрационного сценария](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="b70c5-204">Стратегия — ключевое обучение</span><span class="sxs-lookup"><span data-stu-id="b70c5-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="b70c5-205">Данные</span><span class="sxs-lookup"><span data-stu-id="b70c5-205">Data</span></span>

- <span data-ttu-id="b70c5-206">Убедитесь в том, что имеются репрезентативные объемы данных (копия производственных/золотых данных конфигурации и перенесенные данные).</span><span class="sxs-lookup"><span data-stu-id="b70c5-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="b70c5-207">При создании новых данных с помощью регистратора задач создайте имена тестов, которые не будут конфликтовать с существующими именами (например, используйте префикс, такой как **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="b70c5-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="b70c5-208">Для повторного выполнения тестов в средах без уровней 1 используйте функцию восстановление на момент времени Azure.</span><span class="sxs-lookup"><span data-stu-id="b70c5-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="b70c5-209">Хотя можно использовать функции Excel **RANDOM** и **NOW** для создания уникальной комбинации, усилия весьма высоки.</span><span class="sxs-lookup"><span data-stu-id="b70c5-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="b70c5-210">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="b70c5-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="b70c5-211">Регистратор задач</span><span class="sxs-lookup"><span data-stu-id="b70c5-211">Task recorder</span></span>

- <span data-ttu-id="b70c5-212">Прежде чем начать запись, определите сценарии.</span><span class="sxs-lookup"><span data-stu-id="b70c5-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="b70c5-213">Хорошо управляемый проект имеет предопределенные сценарии тестирования.</span><span class="sxs-lookup"><span data-stu-id="b70c5-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="b70c5-214">Чтобы создать тестовый случай, необходимо оценить, насколько предсказуемым являются результаты этих сценариев тестирования.</span><span class="sxs-lookup"><span data-stu-id="b70c5-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="b70c5-215">Разделите записи, если они выполняются другими ролями, или если имеется время ожидания или внешнее событие до следующего шага.</span><span class="sxs-lookup"><span data-stu-id="b70c5-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="b70c5-216">Не следует выбирать значения в списках.</span><span class="sxs-lookup"><span data-stu-id="b70c5-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="b70c5-217">Вместо этого используйте текстовые форматы, такие как **FIFO**, **AudioRM** и **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="b70c5-218">При выборе в списке записывается позиция значения в списке, а не само значение.</span><span class="sxs-lookup"><span data-stu-id="b70c5-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="b70c5-219">Если в этот список добавлены элементы, положение значения может измениться</span><span class="sxs-lookup"><span data-stu-id="b70c5-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="b70c5-220">Поэтому запись будет использовать другой параметр, и остальная часть сценария может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="b70c5-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="b70c5-221">Подумайте о поведении нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="b70c5-221">Think about multi-user behavior.</span></span> <span data-ttu-id="b70c5-222">Например, не следует предполагать, что вновь созданный заказ на продажу всегда будет выбран автоматически.</span><span class="sxs-lookup"><span data-stu-id="b70c5-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="b70c5-223">Вместо этого для поиска правильного заказа обязательно следует использовать фильтр.</span><span class="sxs-lookup"><span data-stu-id="b70c5-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="b70c5-224">Используйте функцию копирования в регистраторе задач для сохранения имени вновь созданного продукта, чтобы его можно было использовать в связанных тестовых случаях.</span><span class="sxs-lookup"><span data-stu-id="b70c5-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="b70c5-225">Используйте функцию проверки в регистраторе задач для установки контрольных точек, которые проверяют правильность выполнения шагов.</span><span class="sxs-lookup"><span data-stu-id="b70c5-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="b70c5-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="b70c5-226">RSAT</span></span>

- <span data-ttu-id="b70c5-227">Чтобы выполнить тест в другой компании, можно изменить эту компанию на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b70c5-228">Убедитесь, что параметры и данные доступны в новой выбранной компании.</span><span class="sxs-lookup"><span data-stu-id="b70c5-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="b70c5-229">Тестового пользователя можно изменить на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b70c5-230">Укажите код электронной почты пользователя, который будет выполнять тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="b70c5-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="b70c5-231">Таким образом, тестовый случай может быть выполнен с помощью разрешений безопасности указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b70c5-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="b70c5-232">Чтобы подождать, пока начнется тест, можно определить паузу на вкладке **Общие** файла параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="b70c5-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b70c5-233">Эта пауза может использоваться в пакетном задании (например, если рабочий процесс должен выполняться до того, как будет выполнен следующий шаг).</span><span class="sxs-lookup"><span data-stu-id="b70c5-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="b70c5-234">Дополнительные сценарии</span><span class="sxs-lookup"><span data-stu-id="b70c5-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="b70c5-235">Командная строка</span><span class="sxs-lookup"><span data-stu-id="b70c5-235">Command line</span></span>

<span data-ttu-id="b70c5-236">RSAT можно вызывать из окна **Командная строка**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="b70c5-237">Убедитесь, что для переменной среды **TestRoot** установлен путь установки RSAT.</span><span class="sxs-lookup"><span data-stu-id="b70c5-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="b70c5-238">(В Microsoft Windows откройте **Панель управления**, выберите пункт **Система и безопасность \> Система \> Дополнительные параметры системы**, затем выберите **Переменные среды**.)</span><span class="sxs-lookup"><span data-stu-id="b70c5-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="b70c5-239">Откройте окно **Командная строка** от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="b70c5-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="b70c5-240">Запустите средство из каталога установки.</span><span class="sxs-lookup"><span data-stu-id="b70c5-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="b70c5-241">Выведите список всех команд.</span><span class="sxs-lookup"><span data-stu-id="b70c5-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="b70c5-242">Примеры Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b70c5-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="b70c5-243">Выполнение тестового случая в цикле</span><span class="sxs-lookup"><span data-stu-id="b70c5-243">Run a test case in a loop</span></span>

<span data-ttu-id="b70c5-244">Имеется тестовый сценарий, создающий нового клиента.</span><span class="sxs-lookup"><span data-stu-id="b70c5-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="b70c5-245">С помощью сценариев этот тестовый случай можно выполнить в цикле путем случайного выбора следующих данных перед выполнением каждой итерации:</span><span class="sxs-lookup"><span data-stu-id="b70c5-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="b70c5-246">Код клиента</span><span class="sxs-lookup"><span data-stu-id="b70c5-246">Customer ID</span></span>
- <span data-ttu-id="b70c5-247">Наименование Клиента</span><span class="sxs-lookup"><span data-stu-id="b70c5-247">Customer name</span></span>
- <span data-ttu-id="b70c5-248">Адрес клиента</span><span class="sxs-lookup"><span data-stu-id="b70c5-248">Customer address</span></span>

<span data-ttu-id="b70c5-249">Код клиента будет иметь формат *ATCUS\<номер\>*, где \<номер\> представляет собой значение в диапазоне от **000000001** до **999999999**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="b70c5-250">В следующем примере для определения первого используемого номера используется один параметр, **start**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="b70c5-251">Второй параметр **nr** служит для определения числа клиентов, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="b70c5-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="b70c5-252">Для каждой итерации параметры в файле параметров Excel изменяются с помощью функции UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="b70c5-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="b70c5-253">После этого командная строка RSAT вызывается в функции RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="b70c5-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="b70c5-254">Откройте интегрированную среду сценариев Microsoft Windows PowerShell (ISE) в режиме администратора и вставьте следующий код в окно с именем **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="b70c5-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="b70c5-255">Выполнение сценария, который зависит от данных в Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b70c5-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="b70c5-256">В следующем примере для поиска статуса заказа на покупку используется вызов по протоколу OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b70c5-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="b70c5-257">Если статус не равен **выставлена накладная**, можно, например, вызвать тестовый случай RSAT, который разносит накладную.</span><span class="sxs-lookup"><span data-stu-id="b70c5-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
