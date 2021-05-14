---
title: Управление единицами измерения
description: В этой теме показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921349"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="98930-103">Управление единицами измерения</span><span class="sxs-lookup"><span data-stu-id="98930-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98930-104">В этой теме показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="98930-105">Откройте страницу единиц измерения</span><span class="sxs-lookup"><span data-stu-id="98930-105">Open the Units page</span></span>

<span data-ttu-id="98930-106">Чтобы создать единицы измерения, доступные в системе, и работать с ними, перейдите в раздел **Администрирование организации \> Настройка \> Единицы измерения \> Единицы измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="98930-107">В остальных разделах этой главы описываются возможные действия на странице **Единицы измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="98930-108">Создание стандартных единиц измерения и преобразования</span><span class="sxs-lookup"><span data-stu-id="98930-108">Create standard units and conversions</span></span>

<span data-ttu-id="98930-109">Если ваша система еще не включала наиболее часто используемые единицы измерения для системы показателей и/или пользовательской системы США (USCS), мастер настройки единиц измерения поможет быстро начать работу с определениями базовых единиц измерения и их преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="98930-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="98930-110">Чтобы завершить работу мастера, выберите **Мастер создания единиц измерения** на панели операций, а затем следуйте инструкциям на экране.</span><span class="sxs-lookup"><span data-stu-id="98930-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="98930-111">Создание или изменение единицы измерения</span><span class="sxs-lookup"><span data-stu-id="98930-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="98930-112">Чтобы создать или изменить единицу измерения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98930-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="98930-113">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="98930-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="98930-114">Чтобы изменить существующую единицу измерения, выберите ее на панели списка.</span><span class="sxs-lookup"><span data-stu-id="98930-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="98930-115">Чтобы создать новую единицу измерения, на панели операций выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98930-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="98930-116">В заголовке записи задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="98930-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="98930-117">**Единица измерения** — введите код или символ, который будет использоваться для ссылки на единицу измерения на системном языке.</span><span class="sxs-lookup"><span data-stu-id="98930-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="98930-118">Этот код обычно является типичным сокращением для единицы измерения, например *ea* для "each" (каждый) или *cm* для сантиметра.</span><span class="sxs-lookup"><span data-stu-id="98930-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="98930-119">**Описание** — введите описательное имя для единицы измерения на системном языке.</span><span class="sxs-lookup"><span data-stu-id="98930-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="98930-120">Обычно это имя является полным именем единицы измерения, например, *Каждый* или *Сантиметр*.</span><span class="sxs-lookup"><span data-stu-id="98930-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="98930-121">На экспресс-вкладке **Общие** настройте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="98930-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="98930-122">**Класс единиц измерения** — выберите свойство, которое измеряет единица измерения (например, длина, площадь, масса или количество).</span><span class="sxs-lookup"><span data-stu-id="98930-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="98930-123">**Система единиц измерения** — выберите систему измерений, к которой принадлежит единица измерения (*Метрические единицы измерения* или *Типичные единицы измерения США*).</span><span class="sxs-lookup"><span data-stu-id="98930-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="98930-124">**Базовая единица измерения** — установите для этого параметра значение *Да*, чтобы использовать текущую единицу измерения в качестве базовой единицы для класса единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="98930-125">В этом случае необходимо указать коэффициент преобразования между базовой единицей измерения и каждой дополнительной единицей измерения в классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="98930-126">Затем система может преобразовать все единицы измерения в этом классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="98930-127">Таким образом, упрощается настройка преобразований.</span><span class="sxs-lookup"><span data-stu-id="98930-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="98930-128">Например, если галлон является базовой единицей для класса единиц измерения *Объем*, необходимо настроить коэффициенты преобразования из кварты в галлон и из пинты в галлон.</span><span class="sxs-lookup"><span data-stu-id="98930-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="98930-129">Затем система может также преобразовать из кварты в пинту.</span><span class="sxs-lookup"><span data-stu-id="98930-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="98930-130">Для одного класса единицы измерения может быть только одна базовая единица измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="98930-131">**Системная единица** — установите для этого параметра значение *Да*, чтобы использовать текущую единицу измерения в качестве предполагаемой единицы всех неуказанных изменений в классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="98930-132">Например, если поле, используемое для ввода количества, не разрешает указание единицы измерения (если пользователь не выбирает единицу измерения), система использует единицу измерения, заданную в качестве системной единицы измерения для класса единиц измерения *Количество*.</span><span class="sxs-lookup"><span data-stu-id="98930-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="98930-133">Для одного класса единицы измерения может быть только одна системная единица измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="98930-134">**Точность в десятичных знаках** — указывается число десятичных разрядов, для которых задаются значения для текущей единицы измерения или до которых округляются при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="98930-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="98930-135">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="98930-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="98930-136">Определение переводов для единицы измерения</span><span class="sxs-lookup"><span data-stu-id="98930-136">Define unit translations</span></span>

<span data-ttu-id="98930-137">Чтобы определить переводы для идентификатора или символа и описание для единицы измерения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98930-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="98930-138">Создайте или выберите единицу измерения, для которой необходимо создать переводы.</span><span class="sxs-lookup"><span data-stu-id="98930-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="98930-139">В области действий выберите **Тексты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="98930-140">Отображается страница **Тексты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="98930-141">Эта страница используется, чтобы определить переводы для идентификатора или символа выбранной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="98930-142">Эти переводы затем могут быть использованы для внешних документов на языках, отличных от клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="98930-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="98930-143">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98930-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98930-144">В поле **Язык** выберите язык, на который следует перевести идентификатор или символ единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="98930-145">В поле **Текст** введите перевод идентификатора или символа единицы измерения на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="98930-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="98930-146">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="98930-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="98930-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98930-147">Close the page.</span></span>
1. <span data-ttu-id="98930-148">На **Панели операций** выберите **Описания пересчитанных единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="98930-149">Будет открыта страница **Описания переведенных единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="98930-150">Эта страница используется для определения зависящих от языка описаний для выбранной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="98930-151">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98930-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="98930-152">В поле **Язык** выберите язык, на который следует перевести описание единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="98930-153">В поле **Описание** введите перевод описания единицы измерения на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="98930-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="98930-154">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="98930-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="98930-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98930-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="98930-156">Определение правил пересчета единицы измерения</span><span class="sxs-lookup"><span data-stu-id="98930-156">Define unit conversion rules</span></span>

<span data-ttu-id="98930-157">Чтобы определить правила преобразования между единицами измерения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98930-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="98930-158">Создайте или выберите единицу измерения, для которой необходимо задать правила преобразования.</span><span class="sxs-lookup"><span data-stu-id="98930-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="98930-159">В области действий выберите **Пересчет единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="98930-160">Откроется страница **Пересчеты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="98930-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="98930-161">На этой странице определите правила для пересчета выбранной единицы измерения в другие единицы измерения (и из них) в выбранном классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="98930-162">В зависимости от типа пересчета, которое нужно настроить, выберите одну из следующих вкладок:</span><span class="sxs-lookup"><span data-stu-id="98930-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="98930-163">**Стандартные преобразования** — настройка стандартных правил преобразования для всех продуктов.</span><span class="sxs-lookup"><span data-stu-id="98930-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="98930-164">**Преобразования внутри класса** — настройка правил преобразования для конкретного продукта для единиц в одном и том же классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="98930-165">**Преобразования между классами** — настройка правил преобразования для конкретного продукта для единиц в разных классах единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="98930-166">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="98930-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="98930-167">Чтобы создать новый пересчет, на панели инструментов выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="98930-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="98930-168">Чтобы изменить существующее преобразование, выберите преобразование в сетке, а затем нажмите **Правка** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="98930-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="98930-169">В раскрывшемся диалоговом окне задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="98930-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="98930-170">**Продукт** — выберите конкретный продукт, к которому применяется преобразование.</span><span class="sxs-lookup"><span data-stu-id="98930-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="98930-171">Это поле доступно только для преобразования внутри класса и между классами.</span><span class="sxs-lookup"><span data-stu-id="98930-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="98930-172">**Структура формулы** — оставьте в поле значение *Простая*, чтобы задать простое преобразование с одним множителем.</span><span class="sxs-lookup"><span data-stu-id="98930-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="98930-173">Задайте *Расширенная*, чтобы настроить более сложное уравнение.</span><span class="sxs-lookup"><span data-stu-id="98930-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="98930-174">Формат сложных уравнений изменяется в зависимости от класса единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="98930-175">**Из единицы** — в этом поле отображается выбранная единица измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="98930-176">Обычно изменять значение нельзя.</span><span class="sxs-lookup"><span data-stu-id="98930-176">Usually, you should not change the value.</span></span> <span data-ttu-id="98930-177">(Если нужно изменить значение, необходимо открыть страницу **Пересчеты единиц измерения** для выбранной единицы измерения, чтобы просмотреть новое преобразование после его сохранения.)</span><span class="sxs-lookup"><span data-stu-id="98930-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="98930-178">**В единицу** — выберите единицу измерения, в которую которое необходимо выполнить пересчет.</span><span class="sxs-lookup"><span data-stu-id="98930-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="98930-179">**Округление** — выберите способ округления на основе значения **Десятичная точность** выбранной единицы измерения (*До ближайшего*, *Вверх* или *Вниз*).</span><span class="sxs-lookup"><span data-stu-id="98930-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="98930-180">**Формула преобразования** — воспользуйтесь оставшимися полями в верхней части диалогового окна, чтобы указать формулу для преобразования двух единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="98930-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="98930-181">Доступные поля изменяются в зависимости от выбранного класса единиц измерения и структуры формулы.</span><span class="sxs-lookup"><span data-stu-id="98930-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="98930-182">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="98930-182">Select **OK**.</span></span>
1. <span data-ttu-id="98930-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98930-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="98930-184">Можно также настроить пересчет единицы для варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="98930-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="98930-185">Дополнительные сведения см. в разделе [Преобразование единиц измерения для вариантов продукта](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="98930-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
