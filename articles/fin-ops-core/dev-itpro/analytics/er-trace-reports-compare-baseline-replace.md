---
title: Усовершенствования в трассировке результатов созданных отчетов электронной отчетности и сравнения их с базовыми значениями
description: В этом разделе содержатся сведения об улучшении функции базовых образцов ER в Microsoft Dynamics 365 for Finance and Operations версии 10.0.3 (июнь 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 45c0e3b569ca733ae3b70187633d2e84db5ecd87
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771174"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="406d6-103">Усовершенствования в трассировке результатов созданных отчетов электронной отчетности и сравнения их с базовыми значениями</span><span class="sxs-lookup"><span data-stu-id="406d6-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="406d6-104">В этой теме описывается первый набор усовершенствований, которые были сделаны в компоненте базовых образцов платформы электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="406d6-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="406d6-105">Эти усовершенствования доступны в Microsoft Dynamics 365 for Finance and Operations версии 10.0.3 (июнь 2019) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="406d6-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="406d6-106">Автоматизация настройки базовых правил</span><span class="sxs-lookup"><span data-stu-id="406d6-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="406d6-107">В теме [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md) объясняется, как настроить платформу ER для сбора сведений о выполнении формата ER и оценки результатов этих выполнений.</span><span class="sxs-lookup"><span data-stu-id="406d6-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="406d6-108">В примере в этом разделе показаны шаги, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="406d6-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="406d6-109">Вот некоторые из шагов:</span><span class="sxs-lookup"><span data-stu-id="406d6-109">Here are some of the steps:</span></span>

- <span data-ttu-id="406d6-110">Выполните формат ER для создания исходящего файла и сохраните его локально.</span><span class="sxs-lookup"><span data-stu-id="406d6-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="406d6-111">Добавьте локальный файла в качестве вложения базового образца, который был добавлен для формата ER.</span><span class="sxs-lookup"><span data-stu-id="406d6-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="406d6-112">Настройте базовое правило для добавленного базового образца.</span><span class="sxs-lookup"><span data-stu-id="406d6-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="406d6-113">Эта конфигурация включает в себя следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="406d6-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="406d6-114">Укажите элемент формата ER, который используется для создания исходящего файла.</span><span class="sxs-lookup"><span data-stu-id="406d6-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="406d6-115">Выберите вложение, ссылающееся на созданный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="406d6-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="406d6-116">Эти шаги должны выполняться вручную, даже если новые возможности ER обеспечивают их автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="406d6-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="406d6-117">Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.</span><span class="sxs-lookup"><span data-stu-id="406d6-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="406d6-118">Пример. Автоматизация настройки базовых правил</span><span class="sxs-lookup"><span data-stu-id="406d6-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="406d6-119">Чтобы выполнить шаги данного примера, необходимо сначала выполнить шаги в примере из раздела [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md) вплоть до раздела "Добавление нового базового шаблона для разработанного формата ER".</span><span class="sxs-lookup"><span data-stu-id="406d6-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="406d6-120">Обзор добавленного базового образца</span><span class="sxs-lookup"><span data-stu-id="406d6-120">Review added baseline</span></span>

1. <span data-ttu-id="406d6-121">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-122">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="406d6-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="406d6-123">Кнопка **Базовые** в области действий доступна только в том случае, когда параметр пользователя ER **Запустить в режиме отладки** включен для текущей компании.</span><span class="sxs-lookup"><span data-stu-id="406d6-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="406d6-124">Базовый образец добавлен для выбранного формата **Формат для изучения базовых образцов ER**, но базовые правила еще не были добавлены для этого базового образца.</span><span class="sxs-lookup"><span data-stu-id="406d6-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="406d6-125">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline2.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="406d6-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="406d6-126">Создание нового базового правила</span><span class="sxs-lookup"><span data-stu-id="406d6-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="406d6-127">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-128">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="406d6-129">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="406d6-130">На экспресс-вкладке **Версии** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="406d6-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="406d6-131">В поле **Введите ИД** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="406d6-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="406d6-132">Задайте для параметра **Создать базовые файлы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="406d6-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="406d6-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="406d6-133">Select **OK**.</span></span>
8. <span data-ttu-id="406d6-134">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="406d6-134">Select **Baselines**.</span></span>

    <span data-ttu-id="406d6-135">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="406d6-135">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="406d6-136">Созданный исходящий файл автоматически прикрепляется к базовому образцу выполненного формата ER.</span><span class="sxs-lookup"><span data-stu-id="406d6-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="406d6-137">Базовое правило автоматически добавлено к этому базовому образцу, и также содержит ссылку на вложенный файл.</span><span class="sxs-lookup"><span data-stu-id="406d6-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="406d6-138">В поле **Имя** введите **Базовый 1**.</span><span class="sxs-lookup"><span data-stu-id="406d6-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="406d6-139">В поле **Маска имени файла** введите **.xml**.</span><span class="sxs-lookup"><span data-stu-id="406d6-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="406d6-140">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="406d6-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="406d6-141">Выполнение формата</span><span class="sxs-lookup"><span data-stu-id="406d6-141">Run the format</span></span>

<span data-ttu-id="406d6-142">Теперь все готово к выполнению оставшихся шагов в примере в теме [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md), начиная с раздела "Выполнение спроектированного формата ER и просмотр журнала, чтобы проанализировать результаты".</span><span class="sxs-lookup"><span data-stu-id="406d6-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="406d6-143">При удалении автоматически добавленного базового правила на экспресс-вкладке **Базовые** вложение, на которое задана ссылка, не удаляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="406d6-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="406d6-144">Настройка базового образца таким образом, чтобы он игнорировал постоянно изменяющиеся части выходных данных ER</span><span class="sxs-lookup"><span data-stu-id="406d6-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="406d6-145">Если формат ER был создан для того, чтобы содержать сведения, которые изменяются при выполнении формата, необходимо, чтобы формат использовал функцию базовых образцов ER для сравнения созданных результатов с базовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="406d6-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="406d6-146">Например, информация может быть датой и временем обработки или уникальным идентификатором созданного документа в различных форматах (глобальный уникальный идентификатор \[GUID\] и т. д.).</span><span class="sxs-lookup"><span data-stu-id="406d6-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="406d6-147">Новые возможности ER позволяют настроить базовое правило таким образом, чтобы оно игнорировало изменяемые элементы формата ER, когда формат выполняется с целью сравнения значений базового образца с результатами выполнения формата.</span><span class="sxs-lookup"><span data-stu-id="406d6-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="406d6-148">Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.</span><span class="sxs-lookup"><span data-stu-id="406d6-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="406d6-149">Пример. Настройка базового образца таким образом, чтобы он игнорировал постоянно изменяющиеся части выходных данных ER</span><span class="sxs-lookup"><span data-stu-id="406d6-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="406d6-150">Чтобы выполнить шаги данного примера, необходимо сначала выполнить шаги в примере из темы [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="406d6-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="406d6-151">Изменение настроенного формата ER</span><span class="sxs-lookup"><span data-stu-id="406d6-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="406d6-152">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-153">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="406d6-154">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="406d6-155">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="406d6-155">Select **Designer**.</span></span>
5. <span data-ttu-id="406d6-156">В дереве выберите **Вывод\\Документ**.</span><span class="sxs-lookup"><span data-stu-id="406d6-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="406d6-157">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="406d6-157">Select **Add**.</span></span>
7. <span data-ttu-id="406d6-158">В раскрывающемся диалоговом окне в дереве выберите **XML\\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="406d6-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="406d6-159">В поле **Имя** введите **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="406d6-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="406d6-160">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="406d6-160">Select **OK**.</span></span>
10. <span data-ttu-id="406d6-161">На вкладке **Сопоставление** в дереве выберите **Вывод\\Документ\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="406d6-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="406d6-162">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="406d6-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="406d6-163">В поле **Формула** введите следующее выражение: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="406d6-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="406d6-164">Выберите **Сохранить**, затем выберите **Тест**.</span><span class="sxs-lookup"><span data-stu-id="406d6-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="406d6-165">Снова выберите **Тест** для повторного испытания настроенного выражения.</span><span class="sxs-lookup"><span data-stu-id="406d6-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="406d6-166">![Страница конструктора формул](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Снимок экрана страницы конструктора формул")</span><span class="sxs-lookup"><span data-stu-id="406d6-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="406d6-167">На вкладке **Результаты проверки** отображается, что настраиваемое выражение возвращает другое значение даты и времени при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="406d6-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="406d6-168">Закройте страницу **Конструктор формул**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="406d6-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="406d6-169">![Страница конструктора форматов](media/GER-BaselineSample-FormatMappingDesign2.PNG "Снимок экрана страницы конструктора формата")</span><span class="sxs-lookup"><span data-stu-id="406d6-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="406d6-170">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="406d6-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="406d6-171">Удаление существующего базового правила</span><span class="sxs-lookup"><span data-stu-id="406d6-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="406d6-172">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-173">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="406d6-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="406d6-174">В списке базовых образов выберите базовый образец, настроенный для формата **Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="406d6-175">На экспресс-вкладке **Базовые** выберите **Удалить** для удаления ранее настроенного базового правила.</span><span class="sxs-lookup"><span data-stu-id="406d6-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="406d6-176">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline3.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="406d6-176">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="406d6-177">Определение замен для привязок разработанного формата ER</span><span class="sxs-lookup"><span data-stu-id="406d6-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="406d6-178">На странице **Конфигурации** на экспресс-вкладке **Замены** выберите **Выбрать компоненты**.</span><span class="sxs-lookup"><span data-stu-id="406d6-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="406d6-179">В дереве компонентов формата разверните пункт **Вывод**, разверните **Вывод\\Документ**, затем установите флажок для **Вывод\\Документ\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="406d6-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="406d6-180">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="406d6-180">Select **OK**.</span></span>

<span data-ttu-id="406d6-181">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline4.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="406d6-181">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="406d6-182">Выбранный компонент формата ER был добавлен в список компонентов на экспресс-вкладке **Замены**.</span><span class="sxs-lookup"><span data-stu-id="406d6-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="406d6-183">Когда базовый формат ER запускается в режиме отладки, привязка формата для каждого компонента будет заменена привязкой, отображаемой в столбце **Привязка**.</span><span class="sxs-lookup"><span data-stu-id="406d6-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="406d6-184">Чтобы изменить привязку по умолчанию для компонента, указанного на экспресс-вкладке **Замены**, выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="406d6-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="406d6-185">Создание нового базового правила</span><span class="sxs-lookup"><span data-stu-id="406d6-185">Make a new baseline rule</span></span>

<span data-ttu-id="406d6-186">Выполните действия, указанные в разделе "Пример. Автоматизация настройки базовых правил" данной темы.</span><span class="sxs-lookup"><span data-stu-id="406d6-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="406d6-187">Уведомление предупреждает, что исходящий файл был создан с использованием базовых настроек, и что произошла принудительная замена привязок формата.</span><span class="sxs-lookup"><span data-stu-id="406d6-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="406d6-188">![Уведомление на странице конфигураций](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Снимок экрана уведомления на странице "Конфигурации"")</span><span class="sxs-lookup"><span data-stu-id="406d6-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="406d6-189">Подавление предупреждений о замене привязок формата</span><span class="sxs-lookup"><span data-stu-id="406d6-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="406d6-190">Задав определенные параметры ER, можно подавлять оповещения, предупреждающие о замене привязок формата.</span><span class="sxs-lookup"><span data-stu-id="406d6-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="406d6-191">Это подавление может быть полезным, если привязки формата заменены в автоматическом режиме с помощью средства Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="406d6-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="406d6-192">В этом случае предупреждение может считаться сбоем выполняемого тестового случая.</span><span class="sxs-lookup"><span data-stu-id="406d6-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="406d6-193">На странице **Конфигурации** в области действий на вкладке **Конфигурации** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="406d6-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="406d6-194">Установите для параметра **Подавление базовых предупреждений** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="406d6-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="406d6-195">Просмотр сформированного базового файла</span><span class="sxs-lookup"><span data-stu-id="406d6-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="406d6-196">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-197">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="406d6-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="406d6-198">Выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="406d6-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="406d6-199">Созданный файл содержит текст даты и времени обработки (**"#"**) из привязки, которая была настроена в добавленном базовом правиле, а не из привязки формата.</span><span class="sxs-lookup"><span data-stu-id="406d6-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="406d6-200">Закройте страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="406d6-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="406d6-201">Выполнение спроектированного формата ER и просмотр журнала, чтобы проанализировать результаты</span><span class="sxs-lookup"><span data-stu-id="406d6-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="406d6-202">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="406d6-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="406d6-203">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="406d6-204">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="406d6-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="406d6-205">На экспресс-вкладке **Версии** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="406d6-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="406d6-206">В поле **Введите ИД** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="406d6-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="406d6-207">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="406d6-207">Select **OK**.</span></span>
7. <span data-ttu-id="406d6-208">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Журналы отладки конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="406d6-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="406d6-209">Журнал выполнения содержит сведения о результатах сравнения созданного файла с настроенным базовым образцом.</span><span class="sxs-lookup"><span data-stu-id="406d6-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="406d6-210">Журнал указывает, что созданный файл и базовый образец равны, даже если выполняемый формат содержит привязку для ввода постоянно изменяющегося значения даты и времени в исходящем файле.</span><span class="sxs-lookup"><span data-stu-id="406d6-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="406d6-211">Хотя исходящий файл был создан с помощью базовых настроек, которые принудительно заменяют привязки формата, вы не получаете никаких предупреждений о замене.</span><span class="sxs-lookup"><span data-stu-id="406d6-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="406d6-212">Обмен базовыми параметрами между средами</span><span class="sxs-lookup"><span data-stu-id="406d6-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="406d6-213">Экспорт настроек базовых образцов</span><span class="sxs-lookup"><span data-stu-id="406d6-213">Export baseline settings</span></span>

<span data-ttu-id="406d6-214">Новые возможности ER позволяют экспортировать базовые настройки для выбранного формата ER из текущей среды и сохранять их в виде файлов XML.</span><span class="sxs-lookup"><span data-stu-id="406d6-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="406d6-215">Чтобы экспортировать базовые настройки, на странице **Базовые образцы формата электронной отчетности** выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="406d6-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="406d6-216">Импорт базовых параметров</span><span class="sxs-lookup"><span data-stu-id="406d6-216">Import baseline settings</span></span>

<span data-ttu-id="406d6-217">Экспортированные базовые настройки можно импортировать в другую среду.</span><span class="sxs-lookup"><span data-stu-id="406d6-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="406d6-218">Среду сначала следует импортировать как формат ER.</span><span class="sxs-lookup"><span data-stu-id="406d6-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="406d6-219">Затем можно импортировать базовые параметры.</span><span class="sxs-lookup"><span data-stu-id="406d6-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="406d6-220">Чтобы импортировать базовые параметры из локального XML-файла, на странице **Базовые образцы формата электронной отчетности** выберите **Импорт**, затем выберите **Обзор**, чтобы выбрать файл XML.</span><span class="sxs-lookup"><span data-stu-id="406d6-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="406d6-221">![Диалоговое окно импорт базовых параметров](media/GER-BaselineSample-ImportBaseline1.PNG "Снимок экрана диалогового окна импорта базовых параметров")</span><span class="sxs-lookup"><span data-stu-id="406d6-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="406d6-222">Чтобы импортировать базовые параметры из файла XML, хранящегося на сервере Microsoft SharePoint Server, на основе текущих параметров управления документами и выбранного типа документов на странице **Базовые образцы формата электронной отчетности** выберите **Импорт из источника**.</span><span class="sxs-lookup"><span data-stu-id="406d6-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="406d6-223">Затем выберите тип документа и XML-файл.</span><span class="sxs-lookup"><span data-stu-id="406d6-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="406d6-224">Необходимый для доступа к папке SharePoint тип документа должен быть настроен заранее.</span><span class="sxs-lookup"><span data-stu-id="406d6-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="406d6-225">![Диалоговое окно импорта из источника](media/GER-BaselineSample-ImportBaseline2.PNG "Снимок экрана диалогового окна импорта из источника")</span><span class="sxs-lookup"><span data-stu-id="406d6-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="406d6-226">Можно использовать регистратор задач для записи шагов для выбора требуемого типа документа и имени файла в диалоговом окне **Импорт из источника**.</span><span class="sxs-lookup"><span data-stu-id="406d6-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="406d6-227">Таким образом, можно сохранить необходимые базовые параметры на сервере SharePoint Server, а затем автоматически импортировать их путем воспроизведения записи задач при выполнении автоматических тестов с помощью средства Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="406d6-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="406d6-228">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="406d6-228">Additional resources</span></span>

- [<span data-ttu-id="406d6-229">Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями</span><span class="sxs-lookup"><span data-stu-id="406d6-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="406d6-230">Ресурсы регистратора задач</span><span class="sxs-lookup"><span data-stu-id="406d6-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)
