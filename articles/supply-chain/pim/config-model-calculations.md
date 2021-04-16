---
title: Расчету модели конфигурации продукта
description: В этом разделе описывается, как создать расчеты для атрибутов в модели конфигурации продукта
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829626"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="7eaa2-103">Расчету модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="7eaa2-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7eaa2-104">В этом разделе описывается, как создать расчеты для атрибутов в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7eaa2-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="7eaa2-105">Prerequisites</span></span>

<span data-ttu-id="7eaa2-106">Расчеты используются в модели конфигурации продукта для расчета значения конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="7eaa2-107">Прежде чем можно будет начать настройку расчетов, должна существовать связанная модель конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="7eaa2-108">Обзор процесса настройки для моделей конфигурации и соответствующих задач см. в разделе [Настройка модели конфигурации продукта](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="7eaa2-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="7eaa2-109">Создание расчета</span><span class="sxs-lookup"><span data-stu-id="7eaa2-109">Create a calculation</span></span>

<span data-ttu-id="7eaa2-110">Расчет состоит из выражения и целевого атрибута.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="7eaa2-111">Дополнительные сведения см. в разделе [Вопросы и ответы по расчетам для моделей конфигурации продуктов](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="7eaa2-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="7eaa2-112">Чтобы создать расчет для существующей модели продукта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="7eaa2-113">Перейдите в раздел **Управление сведениями о продукте \> Общее \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="7eaa2-114">Откройте модель конфигурации продукта, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="7eaa2-115">На экспресс-вкладке **Расчеты** выберите **Добавить**, чтобы добавить расчет, затем установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="7eaa2-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="7eaa2-116">**Имя** — введите имя для расчета.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="7eaa2-117">**Описание** — введите описание расчета.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="7eaa2-118">**Целевой атрибут** — выберите атрибут, для которого выполняется расчет.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="7eaa2-119">Выберите **Изменить выражение**.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="7eaa2-120">В диалоговом окне **Введите расчет** добавьте в выражение необходимые атрибуты, операторы и значения.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="7eaa2-121">Дополнительные сведения о том, как работать с этими элементами, см. в разделе [Ограничения выражений и ограничения таблиц в моделях конфигурации продукта](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="7eaa2-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="7eaa2-122">Когда выражение будет готово, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="7eaa2-123">Пример расчета</span><span class="sxs-lookup"><span data-stu-id="7eaa2-123">Calculation examples</span></span>

<span data-ttu-id="7eaa2-124">В этом разделе представлено несколько примеров, демонстрирующих работу расчетов.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="7eaa2-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7eaa2-125">Example 1</span></span>

<span data-ttu-id="7eaa2-126">Целевой атрибут является логическим, и при расчете используется следующее условное выражение:</span><span class="sxs-lookup"><span data-stu-id="7eaa2-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="7eaa2-127">Это выражение возвращает целевому атрибуту значение *True*, если значение `decimalAttribute2` больше или равно `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="7eaa2-128">В противном случае он возвращает значение *False*.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="7eaa2-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7eaa2-129">Example 2</span></span>

<span data-ttu-id="7eaa2-130">В этом примере текстовый атрибут `textFixedList` используется в качестве целевого атрибута.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="7eaa2-131">Этот атрибут содержит следующий фиксированный список.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="7eaa2-132">значение</span><span class="sxs-lookup"><span data-stu-id="7eaa2-132">Value</span></span> | <span data-ttu-id="7eaa2-133">Значение решателя</span><span class="sxs-lookup"><span data-stu-id="7eaa2-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="7eaa2-134">A</span><span class="sxs-lookup"><span data-stu-id="7eaa2-134">A</span></span> | <span data-ttu-id="7eaa2-135">1a</span><span class="sxs-lookup"><span data-stu-id="7eaa2-135">1a</span></span> |
| <span data-ttu-id="7eaa2-136">млрд</span><span class="sxs-lookup"><span data-stu-id="7eaa2-136">B</span></span> | <span data-ttu-id="7eaa2-137">2b</span><span class="sxs-lookup"><span data-stu-id="7eaa2-137">2b</span></span> |
| <span data-ttu-id="7eaa2-138">C</span><span class="sxs-lookup"><span data-stu-id="7eaa2-138">C</span></span> | <span data-ttu-id="7eaa2-139">2c</span><span class="sxs-lookup"><span data-stu-id="7eaa2-139">2c</span></span> |

<span data-ttu-id="7eaa2-140">На следующем снимке экрана показано, как могут отображаться в вашей системе параметры для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="7eaa2-141">![Настройки типов атрибутов для примера 2](media/model-calculations-example2.png "Настройки типов атрибутов для примера 2")</span><span class="sxs-lookup"><span data-stu-id="7eaa2-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="7eaa2-142">Этот атрибут используется в следующем условном операторе:</span><span class="sxs-lookup"><span data-stu-id="7eaa2-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="7eaa2-143">Если `integerAttribute` меньше 150, эта инструкция возвращает текстовое значение первой записи в фиксированном списке, *A*. В противном случае возвращается текстовое значение третьей записи в фиксированном списке, *C*.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="7eaa2-144">Фиксированный список эквивалентен перечислению (enum) с нуля, и доступ к его значениям осуществляется с помощью соответствующего целого значения.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="7eaa2-145">Таким образом, первое значение фиксированного списка (*A*) сопоставлено значению *0*, второе значение (*B*) сопоставлено *1*, а третье значение (*C*) сопоставлено *2*.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="7eaa2-146">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7eaa2-146">Example 3</span></span>

<span data-ttu-id="7eaa2-147">В этом примере используется целевой атрибут `textFixedList` из предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="7eaa2-148">Он также использует другой текстовый атрибут, `textAttribute`, который содержит следующий фиксированный список.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="7eaa2-149">значение</span><span class="sxs-lookup"><span data-stu-id="7eaa2-149">Value</span></span> | <span data-ttu-id="7eaa2-150">Значение решателя</span><span class="sxs-lookup"><span data-stu-id="7eaa2-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="7eaa2-151">AA</span><span class="sxs-lookup"><span data-stu-id="7eaa2-151">AA</span></span> | <span data-ttu-id="7eaa2-152">1aa</span><span class="sxs-lookup"><span data-stu-id="7eaa2-152">1aa</span></span> |
| <span data-ttu-id="7eaa2-153">BB</span><span class="sxs-lookup"><span data-stu-id="7eaa2-153">BB</span></span> | <span data-ttu-id="7eaa2-154">2bb</span><span class="sxs-lookup"><span data-stu-id="7eaa2-154">2bb</span></span> |

<span data-ttu-id="7eaa2-155">На следующем снимке экрана показано, как могут отображаться в вашей системе параметры для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="7eaa2-156">![Настройки типов атрибутов для примера 3](media/model-calculations-example3.png "Настройки типов атрибутов для примера 3")</span><span class="sxs-lookup"><span data-stu-id="7eaa2-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="7eaa2-157">Значение для атрибута `textFixedList` вычисляется с помощью следующего условного оператора:</span><span class="sxs-lookup"><span data-stu-id="7eaa2-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="7eaa2-158">Если значение `textAttribute` имеет значение решателя, которое равно *1aa*, это выражение возвращает текстовое значение первой записи в фиксированном списке `textFixedList`, *A*. В противном случае возвращается текстовое значение третьей записи в фиксированном списке `textFixedList`, *C*.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="7eaa2-159">Условный оператор должен использовать значение решателя атрибута.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="7eaa2-160">В расчетах могут использоваться только атрибуты текста фиксированного списка.</span><span class="sxs-lookup"><span data-stu-id="7eaa2-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="7eaa2-161">См. также</span><span class="sxs-lookup"><span data-stu-id="7eaa2-161">See also</span></span>

- [<span data-ttu-id="7eaa2-162">Часто задаваемые вопросы по расчетам моделей конфигураций продуктов</span><span class="sxs-lookup"><span data-stu-id="7eaa2-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="7eaa2-163">Добавление ограничения выражения к модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="7eaa2-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="7eaa2-164">Обзор моделей конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="7eaa2-164">Product configuration models overview</span></span>](product-configuration-models.md)
