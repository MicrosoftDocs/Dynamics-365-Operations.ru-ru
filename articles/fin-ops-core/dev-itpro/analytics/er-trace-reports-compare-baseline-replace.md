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
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181343"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="49602-103">Усовершенствования в трассировке результатов созданных отчетов электронной отчетности и сравнения их с базовыми значениями</span><span class="sxs-lookup"><span data-stu-id="49602-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="49602-104">В этой теме описывается первый набор усовершенствований, которые были сделаны в компоненте базовых образцов платформы электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="49602-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="49602-105">Эти усовершенствования доступны в Microsoft Dynamics 365 for Finance and Operations версии 10.0.3 (июнь 2019) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="49602-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="49602-106">Автоматизация настройки базовых правил</span><span class="sxs-lookup"><span data-stu-id="49602-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="49602-107">В теме [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md) объясняется, как настроить платформу ER для сбора сведений о выполнении формата ER и оценки результатов этих выполнений.</span><span class="sxs-lookup"><span data-stu-id="49602-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="49602-108">В примере в этом разделе показаны шаги, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="49602-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="49602-109">Вот некоторые из шагов:</span><span class="sxs-lookup"><span data-stu-id="49602-109">Here are some of the steps:</span></span>

- <span data-ttu-id="49602-110">Выполните формат ER для создания исходящего файла и сохраните его локально.</span><span class="sxs-lookup"><span data-stu-id="49602-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="49602-111">Добавьте локальный файла в качестве вложения базового образца, который был добавлен для формата ER.</span><span class="sxs-lookup"><span data-stu-id="49602-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="49602-112">Настройте базовое правило для добавленного базового образца.</span><span class="sxs-lookup"><span data-stu-id="49602-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="49602-113">Эта конфигурация включает в себя следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="49602-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="49602-114">Укажите элемент формата ER, который используется для создания исходящего файла.</span><span class="sxs-lookup"><span data-stu-id="49602-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="49602-115">Выберите вложение, ссылающееся на созданный исходный файл.</span><span class="sxs-lookup"><span data-stu-id="49602-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="49602-116">Эти шаги должны выполняться вручную, даже если новые возможности ER обеспечивают их автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="49602-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="49602-117">Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.</span><span class="sxs-lookup"><span data-stu-id="49602-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="49602-118">Пример. Автоматизация настройки базовых правил</span><span class="sxs-lookup"><span data-stu-id="49602-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="49602-119">Чтобы выполнить шаги данного примера, необходимо сначала выполнить шаги в примере из раздела [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md) вплоть до раздела "Добавление нового базового шаблона для разработанного формата ER".</span><span class="sxs-lookup"><span data-stu-id="49602-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="49602-120">Обзор добавленного базового образца</span><span class="sxs-lookup"><span data-stu-id="49602-120">Review added baseline</span></span>

1. <span data-ttu-id="49602-121">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-122">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="49602-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49602-123">Кнопка **Базовые** в области действий доступна только в том случае, когда параметр пользователя ER **Запустить в режиме отладки** включен для текущей компании.</span><span class="sxs-lookup"><span data-stu-id="49602-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="49602-124">Базовый образец добавлен для выбранного формата **Формат для изучения базовых образцов ER**, но базовые правила еще не были добавлены для этого базового образца.</span><span class="sxs-lookup"><span data-stu-id="49602-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="49602-125">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline2.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="49602-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="49602-126">Создание нового базового правила</span><span class="sxs-lookup"><span data-stu-id="49602-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="49602-127">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-128">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="49602-129">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="49602-130">На экспресс-вкладке **Версии** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="49602-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="49602-131">В поле **Введите ИД** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="49602-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="49602-132">Задайте для параметра **Создать базовые файлы** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="49602-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="49602-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49602-133">Select **OK**.</span></span>

    <span data-ttu-id="49602-134">![Диалоговое окно параметров электронной отчетности](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Снимок экрана диалогового окна параметров электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="49602-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="49602-135">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="49602-135">Select **Baselines**.</span></span>

    <span data-ttu-id="49602-136">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="49602-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="49602-137">Созданный исходящий файл автоматически прикрепляется к базовому образцу выполненного формата ER.</span><span class="sxs-lookup"><span data-stu-id="49602-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="49602-138">Базовое правило автоматически добавлено к этому базовому образцу, и также содержит ссылку на вложенный файл.</span><span class="sxs-lookup"><span data-stu-id="49602-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="49602-139">В поле **Имя** введите **Базовый 1**.</span><span class="sxs-lookup"><span data-stu-id="49602-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="49602-140">В поле **Маска имени файла** введите **.xml**.</span><span class="sxs-lookup"><span data-stu-id="49602-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="49602-141">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="49602-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="49602-142">Выполнение формата</span><span class="sxs-lookup"><span data-stu-id="49602-142">Run the format</span></span>

<span data-ttu-id="49602-143">Теперь все готово к выполнению оставшихся шагов в примере в теме [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md), начиная с раздела "Выполнение спроектированного формата ER и просмотр журнала, чтобы проанализировать результаты".</span><span class="sxs-lookup"><span data-stu-id="49602-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="49602-144">При удалении автоматически добавленного базового правила на экспресс-вкладке **Базовые** вложение, на которое задана ссылка, не удаляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="49602-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="49602-145">Настройка базового образца таким образом, чтобы он игнорировал постоянно изменяющиеся части выходных данных ER</span><span class="sxs-lookup"><span data-stu-id="49602-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="49602-146">Если формат ER был создан для того, чтобы содержать сведения, которые изменяются при выполнении формата, необходимо, чтобы формат использовал функцию базовых образцов ER для сравнения созданных результатов с базовыми значениями.</span><span class="sxs-lookup"><span data-stu-id="49602-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="49602-147">Например, информация может быть датой и временем обработки или уникальным идентификатором созданного документа в различных форматах (глобальный уникальный идентификатор \[GUID\] и т. д.).</span><span class="sxs-lookup"><span data-stu-id="49602-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="49602-148">Новые возможности ER позволяют настроить базовое правило таким образом, чтобы оно игнорировало изменяемые элементы формата ER, когда формат выполняется с целью сравнения значений базового образца с результатами выполнения формата.</span><span class="sxs-lookup"><span data-stu-id="49602-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="49602-149">Чтобы получить дополнительные сведения об этой функции, выполните следующий пример.</span><span class="sxs-lookup"><span data-stu-id="49602-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="49602-150">Пример. Настройка базового образца таким образом, чтобы он игнорировал постоянно изменяющиеся части выходных данных ER</span><span class="sxs-lookup"><span data-stu-id="49602-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="49602-151">Чтобы выполнить шаги данного примера, необходимо сначала выполнить шаги в примере из темы [Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="49602-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="49602-152">Изменение настроенного формата ER</span><span class="sxs-lookup"><span data-stu-id="49602-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="49602-153">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-154">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="49602-155">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="49602-156">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="49602-156">Select **Designer**.</span></span>
5. <span data-ttu-id="49602-157">В дереве выберите **Вывод\\Документ**.</span><span class="sxs-lookup"><span data-stu-id="49602-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="49602-158">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="49602-158">Select **Add**.</span></span>
7. <span data-ttu-id="49602-159">В раскрывающемся диалоговом окне в дереве выберите **XML\\Атрибут**.</span><span class="sxs-lookup"><span data-stu-id="49602-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="49602-160">В поле **Имя** введите **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="49602-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="49602-161">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49602-161">Select **OK**.</span></span>
10. <span data-ttu-id="49602-162">На вкладке **Сопоставление** в дереве выберите **Вывод\\Документ\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="49602-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="49602-163">Выберите **Изменить формулу**.</span><span class="sxs-lookup"><span data-stu-id="49602-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="49602-164">В поле **Формула** введите следующее выражение: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="49602-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="49602-165">Выберите **Сохранить**, затем выберите **Тест**.</span><span class="sxs-lookup"><span data-stu-id="49602-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="49602-166">Снова выберите **Тест** для повторного испытания настроенного выражения.</span><span class="sxs-lookup"><span data-stu-id="49602-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="49602-167">![Страница конструктора формул](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Снимок экрана страницы конструктора формул")</span><span class="sxs-lookup"><span data-stu-id="49602-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="49602-168">На вкладке **Результаты проверки** отображается, что настраиваемое выражение возвращает другое значение даты и времени при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="49602-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="49602-169">Закройте страницу **Конструктор формул**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="49602-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="49602-170">![Страница конструктора формата](media/GER-BaselineSample-FormatMappingDesign2.PNG "Снимок экрана страницы конструктора формата")</span><span class="sxs-lookup"><span data-stu-id="49602-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="49602-171">Закройте страницу **Конструктор форматов**.</span><span class="sxs-lookup"><span data-stu-id="49602-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="49602-172">Удаление существующего базового правила</span><span class="sxs-lookup"><span data-stu-id="49602-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="49602-173">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-174">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="49602-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="49602-175">В списке базовых образов выберите базовый образец, настроенный для формата **Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="49602-176">На экспресс-вкладке **Базовые** выберите **Удалить** для удаления ранее настроенного базового правила.</span><span class="sxs-lookup"><span data-stu-id="49602-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="49602-177">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline3.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="49602-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="49602-178">Определение замен для привязок разработанного формата ER</span><span class="sxs-lookup"><span data-stu-id="49602-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="49602-179">На странице **Конфигурации** на экспресс-вкладке **Замены** выберите **Выбрать компоненты**.</span><span class="sxs-lookup"><span data-stu-id="49602-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="49602-180">В дереве компонентов формата разверните пункт **Вывод**, разверните **Вывод\\Документ**, затем установите флажок для **Вывод\\Документ\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="49602-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="49602-181">![Диалоговое окно выбора компонентов](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Снимок экрана диалогового окна выбора компонентов")</span><span class="sxs-lookup"><span data-stu-id="49602-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="49602-182">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49602-182">Select **OK**.</span></span>

<span data-ttu-id="49602-183">![Страница базовых образцов формата электронной отчетности](media/GER-BaselineSample-AddBaseline4.PNG "Снимок экрана страницы базовых образцов формата электронной отчетности")</span><span class="sxs-lookup"><span data-stu-id="49602-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="49602-184">Выбранный компонент формата ER был добавлен в список компонентов на экспресс-вкладке **Замены**.</span><span class="sxs-lookup"><span data-stu-id="49602-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="49602-185">Когда базовый формат ER запускается в режиме отладки, привязка формата для каждого компонента будет заменена привязкой, отображаемой в столбце **Привязка**.</span><span class="sxs-lookup"><span data-stu-id="49602-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="49602-186">Чтобы изменить привязку по умолчанию для компонента, указанного на экспресс-вкладке **Замены**, выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="49602-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="49602-187">Создание нового базового правила</span><span class="sxs-lookup"><span data-stu-id="49602-187">Make a new baseline rule</span></span>

<span data-ttu-id="49602-188">Выполните действия, указанные в разделе "Пример. Автоматизация настройки базовых правил" данной темы.</span><span class="sxs-lookup"><span data-stu-id="49602-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="49602-189">Уведомление предупреждает, что исходящий файл был создан с использованием базовых настроек, и что произошла принудительная замена привязок формата.</span><span class="sxs-lookup"><span data-stu-id="49602-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="49602-190">![Уведомление на странице "Конфигурации"](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Снимок экрана уведомления на странице \"Конфигурации\"")</span><span class="sxs-lookup"><span data-stu-id="49602-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="49602-191">Подавление предупреждений о замене привязок формата</span><span class="sxs-lookup"><span data-stu-id="49602-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="49602-192">Задав определенные параметры ER, можно подавлять оповещения, предупреждающие о замене привязок формата.</span><span class="sxs-lookup"><span data-stu-id="49602-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="49602-193">Это подавление может быть полезным, если привязки формата заменены в автоматическом режиме с помощью средства Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="49602-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="49602-194">В этом случае предупреждение может считаться сбоем выполняемого тестового случая.</span><span class="sxs-lookup"><span data-stu-id="49602-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="49602-195">На странице **Конфигурации** в области действий на вкладке **Конфигурации** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="49602-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="49602-196">Установите для параметра **Подавление базовых предупреждений** значение **Да**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49602-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="49602-197">![Диалоговое окно параметров пользователя](media/GER-BaselineSample-ERUserParameters1.png "Снимок экрана диалогового окна параметров пользователя")</span><span class="sxs-lookup"><span data-stu-id="49602-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="49602-198">Просмотр сформированного базового файла</span><span class="sxs-lookup"><span data-stu-id="49602-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="49602-199">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-200">Выберите **Базовые**.</span><span class="sxs-lookup"><span data-stu-id="49602-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="49602-201">Выберите **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="49602-201">Select **Attachments**.</span></span>

    <span data-ttu-id="49602-202">![Страница вложений](media/GER-BaselineSample-AttachedBaselineFile.PNG "Снимок экрана страницы вложений")</span><span class="sxs-lookup"><span data-stu-id="49602-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="49602-203">Созданный файл содержит текст даты и времени обработки (**"#"**) из привязки, которая была настроена в добавленном базовом правиле, а не из привязки формата.</span><span class="sxs-lookup"><span data-stu-id="49602-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="49602-204">Закройте страницу **Вложения**.</span><span class="sxs-lookup"><span data-stu-id="49602-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="49602-205">Выполнение спроектированного формата ER и просмотр журнала, чтобы проанализировать результаты</span><span class="sxs-lookup"><span data-stu-id="49602-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="49602-206">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="49602-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="49602-207">В дереве разверните **Модель для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="49602-208">В дереве выберите **Модель для изучения базовых образцов ER\\Формат для изучения базовых образцов ER**.</span><span class="sxs-lookup"><span data-stu-id="49602-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="49602-209">На экспресс-вкладке **Версии** выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="49602-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="49602-210">В поле **Введите ИД** введите **1**.</span><span class="sxs-lookup"><span data-stu-id="49602-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="49602-211">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49602-211">Select **OK**.</span></span>
7. <span data-ttu-id="49602-212">Перейдите в раздел **Администрирование организации** \> **Электронная отчетность** \> **Журналы отладки конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="49602-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="49602-213">Журнал выполнения содержит сведения о результатах сравнения созданного файла с настроенным базовым образцом.</span><span class="sxs-lookup"><span data-stu-id="49602-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="49602-214">Журнал указывает, что созданный файл и базовый образец равны, даже если выполняемый формат содержит привязку для ввода постоянно изменяющегося значения даты и времени в исходящем файле.</span><span class="sxs-lookup"><span data-stu-id="49602-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="49602-215">Хотя исходящий файл был создан с помощью базовых настроек, которые принудительно заменяют привязки формата, вы не получаете никаких предупреждений о замене.</span><span class="sxs-lookup"><span data-stu-id="49602-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="49602-216">Обмен базовыми параметрами между средами</span><span class="sxs-lookup"><span data-stu-id="49602-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="49602-217">Экспорт настроек базовых образцов</span><span class="sxs-lookup"><span data-stu-id="49602-217">Export baseline settings</span></span>

<span data-ttu-id="49602-218">Новые возможности ER позволяют экспортировать базовые настройки для выбранного формата ER из текущей среды и сохранять их в виде файлов XML.</span><span class="sxs-lookup"><span data-stu-id="49602-218">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="49602-219">Чтобы экспортировать базовые настройки, на странице **Базовые образцы формата электронной отчетности** выберите **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="49602-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="49602-220">Импорт базовых параметров</span><span class="sxs-lookup"><span data-stu-id="49602-220">Import baseline settings</span></span>

<span data-ttu-id="49602-221">Экспортированные базовые настройки можно импортировать в другую среду.</span><span class="sxs-lookup"><span data-stu-id="49602-221">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="49602-222">Среду сначала следует импортировать как формат ER.</span><span class="sxs-lookup"><span data-stu-id="49602-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="49602-223">Затем можно импортировать базовые параметры.</span><span class="sxs-lookup"><span data-stu-id="49602-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="49602-224">Чтобы импортировать базовые параметры из локального XML-файла, на странице **Базовые образцы формата электронной отчетности** выберите **Импорт**, затем выберите **Обзор**, чтобы выбрать файл XML.</span><span class="sxs-lookup"><span data-stu-id="49602-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="49602-225">![Диалоговое окно импорт базовых параметров](media/GER-BaselineSample-ImportBaseline1.PNG "Снимок экрана диалогового окна импорта базовых параметров")</span><span class="sxs-lookup"><span data-stu-id="49602-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="49602-226">Чтобы импортировать базовые параметры из файла XML, хранящегося на сервере Microsoft SharePoint Server, на основе текущих параметров управления документами и выбранного типа документов на странице **Базовые образцы формата электронной отчетности** выберите **Импорт из источника**.</span><span class="sxs-lookup"><span data-stu-id="49602-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="49602-227">Затем выберите тип документа и XML-файл.</span><span class="sxs-lookup"><span data-stu-id="49602-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="49602-228">Необходимый для доступа к папке SharePoint тип документа должен быть настроен заранее.</span><span class="sxs-lookup"><span data-stu-id="49602-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="49602-229">![Диалоговое окно импорта из источника](media/GER-BaselineSample-ImportBaseline2.PNG "Снимок экрана диалогового окна импорта из источника")</span><span class="sxs-lookup"><span data-stu-id="49602-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="49602-230">Можно использовать регистратор задач для записи шагов для выбора требуемого типа документа и имени файла в диалоговом окне **Импорт из источника**.</span><span class="sxs-lookup"><span data-stu-id="49602-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="49602-231">Таким образом, можно сохранить необходимые базовые параметры на сервере SharePoint Server, а затем автоматически импортировать их путем воспроизведения записи задач при выполнении автоматических тестов с помощью средства Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="49602-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49602-232">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="49602-232">Additional resources</span></span>

- [<span data-ttu-id="49602-233">Отслеживание результатов из сформированного отчета и их сравнение с базовыми значениями</span><span class="sxs-lookup"><span data-stu-id="49602-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="49602-234">Регистратор задач</span><span class="sxs-lookup"><span data-stu-id="49602-234">Task recorder</span></span>](../user-interface/task-recorder.md)
