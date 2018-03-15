---
title: "Ограничения выражений и ограничения таблиц в моделях конфигурации продукта"
description: "В этом разделе описывается использование ограничений выражений и ограничений таблиц. Ограничения управляют значениями атрибутов, которые можно выбирать при настройке продуктов для заказа на продажу, предложения по продажам, заказа на покупку или производственного заказа. Можно использовать ограничения выражений или ограничения таблиц в зависимости того, как вы предпочитаете формировать ограничения."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3206e53c4f2659c6d9b9be64b01ac28cdd17bc88
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="a6714-105">Ограничения выражений и ограничения таблиц в моделях конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="a6714-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a6714-106">В этом разделе описывается использование ограничений выражений и ограничений таблиц.</span><span class="sxs-lookup"><span data-stu-id="a6714-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="a6714-107">Ограничения управляют значениями атрибутов, которые можно выбирать при настройке продуктов для заказа на продажу, предложения по продажам, заказа на покупку или производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="a6714-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="a6714-108">Можно использовать ограничения выражений или ограничения таблиц в зависимости того, как вы предпочитаете формировать ограничения.</span><span class="sxs-lookup"><span data-stu-id="a6714-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="a6714-109">Ограничения используются для управления значениями атрибутов, которые можно выбирать при настройке продуктов для заказа на продажу, предложения по продажам, заказа на покупку или производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="a6714-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="a6714-110">Можно использовать ограничения выражений или ограничения таблиц в зависимости того, как вы предпочитаете формировать ограничения.</span><span class="sxs-lookup"><span data-stu-id="a6714-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="a6714-111">Что такое ограничения выражений?</span><span class="sxs-lookup"><span data-stu-id="a6714-111">What are expression constraints?</span></span>
<span data-ttu-id="a6714-112">Ограничения выражения описываются выражением, которое использует арифметические и логические операторы и функции.</span><span class="sxs-lookup"><span data-stu-id="a6714-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="a6714-113">Ограничение выражения пишется для определенного компонента в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="a6714-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="a6714-114">Его нельзя использовать повторно или совместно с другим компонентом.</span><span class="sxs-lookup"><span data-stu-id="a6714-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="a6714-115">Однако ограничения выражения для компонента могут ссылаться на атрибуты субкомпонентов компонента.</span><span class="sxs-lookup"><span data-stu-id="a6714-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="a6714-116">Что такое ограничения таблиц?</span><span class="sxs-lookup"><span data-stu-id="a6714-116">What are table constraints?</span></span>
<span data-ttu-id="a6714-117">Ограничения таблиц содержат сочетания допустимых значений атрибутов при настройке продукта.</span><span class="sxs-lookup"><span data-stu-id="a6714-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="a6714-118">Определения ограничений таблиц можно использовать универсальным образом.</span><span class="sxs-lookup"><span data-stu-id="a6714-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="a6714-119">При создании ограничения таблицы для компонента в модели конфигурации продукта выбирается определение ограничения таблицы.</span><span class="sxs-lookup"><span data-stu-id="a6714-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="a6714-120">Чтобы создать допустимые комбинации, можно добавить атрибуты конкретных типов к компонентам.</span><span class="sxs-lookup"><span data-stu-id="a6714-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="a6714-121">Каждый тип атрибута имеет определенное значение.</span><span class="sxs-lookup"><span data-stu-id="a6714-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="a6714-122">Пример ограничения таблицы</span><span class="sxs-lookup"><span data-stu-id="a6714-122">Example of a table constraint</span></span>

<span data-ttu-id="a6714-123">Этот пример показывает, как вы можете ограничить конфигурацию динамика определенными видами отделки корпуса и передней панели.</span><span class="sxs-lookup"><span data-stu-id="a6714-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="a6714-124">В первой таблице показаны отделки корпуса и передние решетки, которые обычно доступны для настройки.</span><span class="sxs-lookup"><span data-stu-id="a6714-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="a6714-125">Значения определены для типов атрибутов **Отделка корпуса** и **Передняя решетка**.</span><span class="sxs-lookup"><span data-stu-id="a6714-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="a6714-126">Тип атрибута</span><span class="sxs-lookup"><span data-stu-id="a6714-126">Attribute type</span></span> | <span data-ttu-id="a6714-127">Значения</span><span class="sxs-lookup"><span data-stu-id="a6714-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="a6714-128">Отделка корпуса</span><span class="sxs-lookup"><span data-stu-id="a6714-128">Cabinet finish</span></span> | <span data-ttu-id="a6714-129">Черный, Дуб, Палисандр, Белый</span><span class="sxs-lookup"><span data-stu-id="a6714-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="a6714-130">Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="a6714-130">Front grill</span></span>    | <span data-ttu-id="a6714-131">Черная, Металл, Белая</span><span class="sxs-lookup"><span data-stu-id="a6714-131">Black, Metal, White</span></span>         |

<span data-ttu-id="a6714-132">В следующей таблице показаны сочетания, которые определены ограничением таблицы **Цвет и отделка**.</span><span class="sxs-lookup"><span data-stu-id="a6714-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="a6714-133">Путем использование этого ограничения таблицы вы можете задать конфигурацию динамика с отделкой дубом и черной решеткой, с отделкой палисандром и белой решеткой и так далее.</span><span class="sxs-lookup"><span data-stu-id="a6714-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="a6714-134">Готово</span><span class="sxs-lookup"><span data-stu-id="a6714-134">Finish</span></span>         | <span data-ttu-id="a6714-135">Решетка</span><span class="sxs-lookup"><span data-stu-id="a6714-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="a6714-136">Дуб</span><span class="sxs-lookup"><span data-stu-id="a6714-136">Oak</span></span>            | <span data-ttu-id="a6714-137">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-137">Black</span></span>                       |
| <span data-ttu-id="a6714-138">Палисандр</span><span class="sxs-lookup"><span data-stu-id="a6714-138">Rosewood</span></span>       | <span data-ttu-id="a6714-139">Белый</span><span class="sxs-lookup"><span data-stu-id="a6714-139">White</span></span>                       |
| <span data-ttu-id="a6714-140">Белый</span><span class="sxs-lookup"><span data-stu-id="a6714-140">White</span></span>          | <span data-ttu-id="a6714-141">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-141">Black</span></span>                       |
| <span data-ttu-id="a6714-142">Белый</span><span class="sxs-lookup"><span data-stu-id="a6714-142">White</span></span>          | <span data-ttu-id="a6714-143">Белый</span><span class="sxs-lookup"><span data-stu-id="a6714-143">White</span></span>                       |
| <span data-ttu-id="a6714-144">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-144">Black</span></span>          | <span data-ttu-id="a6714-145">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-145">Black</span></span>                       |
| <span data-ttu-id="a6714-146">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-146">Black</span></span>          | <span data-ttu-id="a6714-147">Металл</span><span class="sxs-lookup"><span data-stu-id="a6714-147">Metal</span></span>                       | 

<span data-ttu-id="a6714-148">Вы можете создавать системные и пользовательские ограничения таблиц.</span><span class="sxs-lookup"><span data-stu-id="a6714-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="a6714-149">Дополнительную информацию см. в разделе [Системные и пользовательские ограничения таблиц](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="a6714-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="a6714-150">Какой синтаксис следует использовать для записи ограничений?</span><span class="sxs-lookup"><span data-stu-id="a6714-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="a6714-151">При написании ограничений используется синтаксис языка OML.</span><span class="sxs-lookup"><span data-stu-id="a6714-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="a6714-152">В системе для разрешения ограничений используется решатель ограничений Microsoft Solver Foundation.</span><span class="sxs-lookup"><span data-stu-id="a6714-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="a6714-153">Как выбрать между ограничениями таблиц и ограничениями выражений?</span><span class="sxs-lookup"><span data-stu-id="a6714-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="a6714-154">Можно использовать как ограничения выражений, так и ограничения таблиц, в зависимости того, как вы предпочитаете формировать ограничения.</span><span class="sxs-lookup"><span data-stu-id="a6714-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="a6714-155">Ограничение таблицы формируется как матрица, тогда как ограничение выражения — как отдельное выражение.</span><span class="sxs-lookup"><span data-stu-id="a6714-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="a6714-156">При настройке продукта используемый тип ограничения не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="a6714-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="a6714-157">Следующий пример демонстрирует отличия этих двух методов.</span><span class="sxs-lookup"><span data-stu-id="a6714-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="a6714-158">Когда вы настраиваете продукт путем использования приведенных ниже установок ограничения, разрешены следующие комбинации:</span><span class="sxs-lookup"><span data-stu-id="a6714-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="a6714-159">Продукт в цвете "Черный", размер 30 или 50</span><span class="sxs-lookup"><span data-stu-id="a6714-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="a6714-160">Продукт в цвете "Красный", размер 20</span><span class="sxs-lookup"><span data-stu-id="a6714-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="a6714-161">Настройка ограничений таблицы</span><span class="sxs-lookup"><span data-stu-id="a6714-161">Table constraint setup</span></span>

| <span data-ttu-id="a6714-162">Цвет</span><span class="sxs-lookup"><span data-stu-id="a6714-162">Color</span></span> | <span data-ttu-id="a6714-163">Размер</span><span class="sxs-lookup"><span data-stu-id="a6714-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="a6714-164">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-164">Black</span></span> | <span data-ttu-id="a6714-165">30</span><span class="sxs-lookup"><span data-stu-id="a6714-165">30</span></span>   |
| <span data-ttu-id="a6714-166">Черный</span><span class="sxs-lookup"><span data-stu-id="a6714-166">Black</span></span> | <span data-ttu-id="a6714-167">50</span><span class="sxs-lookup"><span data-stu-id="a6714-167">50</span></span>   |
| <span data-ttu-id="a6714-168">Красный</span><span class="sxs-lookup"><span data-stu-id="a6714-168">Red</span></span>   | <span data-ttu-id="a6714-169">20</span><span class="sxs-lookup"><span data-stu-id="a6714-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="a6714-170">Настройка ограничения выражения</span><span class="sxs-lookup"><span data-stu-id="a6714-170">Expression constraint setup</span></span>

<span data-ttu-id="a6714-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="a6714-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="a6714-172">Нужно ли использовать операторы или инфиксную нотацию при написании ограничений выражений?</span><span class="sxs-lookup"><span data-stu-id="a6714-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="a6714-173">Вы можете писать ограничения выражений с помощью доступных префиксных операторов или с использованием инфиксной нотации.</span><span class="sxs-lookup"><span data-stu-id="a6714-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="a6714-174">Для операторов **Min**, **Max** и **Abs** использовать инфиксную нотацию нельзя.</span><span class="sxs-lookup"><span data-stu-id="a6714-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="a6714-175">Эти операторы включены в качестве стандартных операторов в большинство языков программирования.</span><span class="sxs-lookup"><span data-stu-id="a6714-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="a6714-176">Какие операторы и инфиксные нотации можно использовать при написании ограничений выражений?</span><span class="sxs-lookup"><span data-stu-id="a6714-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="a6714-177">В следующей таблице перечислены операторы и инфиксные нотации, которые можно использовать при написании ограничений выражений для компонента модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="a6714-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="a6714-178">В примерах в первой таблице показано, как записать выражение с помощью инфиксной нотации или операторов.</span><span class="sxs-lookup"><span data-stu-id="a6714-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6714-179">Оператор</span><span class="sxs-lookup"><span data-stu-id="a6714-179">Operator</span></span></th>
<th><span data-ttu-id="a6714-180">Описание</span><span class="sxs-lookup"><span data-stu-id="a6714-180">Description</span></span></th>
<th><span data-ttu-id="a6714-181">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6714-181">Syntax</span></span></th>
<th><span data-ttu-id="a6714-182">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6714-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6714-183">Implies</span><span class="sxs-lookup"><span data-stu-id="a6714-183">Implies</span></span></td>
<td><span data-ttu-id="a6714-184">Выражение истинно, если первое условие ложно, второе условие истинно или выполняются оба условия.</span><span class="sxs-lookup"><span data-stu-id="a6714-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="a6714-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="a6714-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-186"><strong>Оператор:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="a6714-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="a6714-187"><strong>Инфиксная нотация:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="a6714-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6714-188">И</span><span class="sxs-lookup"><span data-stu-id="a6714-188">And</span></span></td>
<td><span data-ttu-id="a6714-189">Выражение истинно, только если условия истинны.</span><span class="sxs-lookup"><span data-stu-id="a6714-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="a6714-190">Если число условий равно 0, результатом будет <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="a6714-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="a6714-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-192"><strong>Оператор:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="a6714-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="a6714-193"><strong>Инфиксная нотация:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="a6714-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6714-194">Или</span><span class="sxs-lookup"><span data-stu-id="a6714-194">Or</span></span></td>
<td><span data-ttu-id="a6714-195">Выражение истинно, если любое из условий истинно.</span><span class="sxs-lookup"><span data-stu-id="a6714-195">This is true if any condition is true.</span></span> <span data-ttu-id="a6714-196">Если число условий равно 0, результатом будет <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="a6714-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="a6714-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-198"><strong>Оператор:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="a6714-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="a6714-199"><strong>Инфиксная нотация:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="a6714-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6714-200">Плюс</span><span class="sxs-lookup"><span data-stu-id="a6714-200">Plus</span></span></td>
<td><span data-ttu-id="a6714-201">Выражение суммирует его условия.</span><span class="sxs-lookup"><span data-stu-id="a6714-201">This sums its conditions.</span></span> <span data-ttu-id="a6714-202">Если число условий равно 0, результатом будет <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="a6714-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="a6714-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-204"><strong>Оператор:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="a6714-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="a6714-205"><strong>Инфиксная нотация:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="a6714-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6714-206">Минус</span><span class="sxs-lookup"><span data-stu-id="a6714-206">Minus</span></span></td>
<td><span data-ttu-id="a6714-207">Инвертирует свой аргумент.</span><span class="sxs-lookup"><span data-stu-id="a6714-207">This negates its argument.</span></span> <span data-ttu-id="a6714-208">У этого выражения должно быть ровно одно условие.</span><span class="sxs-lookup"><span data-stu-id="a6714-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="a6714-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="a6714-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-210"><strong>Оператор:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="a6714-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="a6714-211"><strong>Инфиксная нотация:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="a6714-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6714-212">Abs</span><span class="sxs-lookup"><span data-stu-id="a6714-212">Abs</span></span></td>
<td><span data-ttu-id="a6714-213">Выражение получает модуль значения условия.</span><span class="sxs-lookup"><span data-stu-id="a6714-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="a6714-214">У этого выражения должно быть ровно одно условие.</span><span class="sxs-lookup"><span data-stu-id="a6714-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="a6714-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="a6714-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="a6714-216"><strong>Оператор:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="a6714-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6714-217">Время</span><span class="sxs-lookup"><span data-stu-id="a6714-217">Times</span></span></td>
<td><span data-ttu-id="a6714-218">Выражение получает произведение условий.</span><span class="sxs-lookup"><span data-stu-id="a6714-218">This takes the product of its conditions.</span></span> <span data-ttu-id="a6714-219">Если число условий равно 0, результатом будет <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="a6714-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="a6714-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-221"><strong>Оператор:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="a6714-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="a6714-222"><strong>Инфиксная нотация:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="a6714-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6714-223">Степень</span><span class="sxs-lookup"><span data-stu-id="a6714-223">Power</span></span></td>
<td><span data-ttu-id="a6714-224">Выражение возводит аргумент в степень.</span><span class="sxs-lookup"><span data-stu-id="a6714-224">This takes an exponential.</span></span> <span data-ttu-id="a6714-225">Возведение в степень применяется справа налево.</span><span class="sxs-lookup"><span data-stu-id="a6714-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="a6714-226">(То есть, это правоассоциативное выражение.) Поэтому выражение <strong>Power[a, b, c]</strong> эквивалентно <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="a6714-227"><strong>Power</strong> можно использовать только в том случае, если экспонента является положительной константой.</span><span class="sxs-lookup"><span data-stu-id="a6714-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="a6714-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="a6714-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-229"><strong>Оператор:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="a6714-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="a6714-230"><strong>Инфиксная нотация:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="a6714-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6714-231">Макс.</span><span class="sxs-lookup"><span data-stu-id="a6714-231">Max</span></span></td>
<td><span data-ttu-id="a6714-232">Выражение получает наибольшее из условий.</span><span class="sxs-lookup"><span data-stu-id="a6714-232">This produces the largest condition.</span></span> <span data-ttu-id="a6714-233">Если число условий равно 0, результатом будет <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="a6714-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="a6714-234">Max[args]</span></span></td>
<td><span data-ttu-id="a6714-235"><strong>Оператор:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="a6714-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6714-236">Мин.</span><span class="sxs-lookup"><span data-stu-id="a6714-236">Min</span></span></td>
<td><span data-ttu-id="a6714-237">Выражение получает наименьшее из условий.</span><span class="sxs-lookup"><span data-stu-id="a6714-237">This produces the smallest condition.</span></span> <span data-ttu-id="a6714-238">Если число условий равно 0, результатом будет <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6714-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="a6714-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="a6714-239">Min[args]</span></span></td>
<td><span data-ttu-id="a6714-240"><strong>Оператор:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="a6714-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6714-241">Не</span><span class="sxs-lookup"><span data-stu-id="a6714-241">Not</span></span></td>
<td><span data-ttu-id="a6714-242">Выражение получает логическую инверсию условия.</span><span class="sxs-lookup"><span data-stu-id="a6714-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="a6714-243">У этого выражения должно быть ровно одно условие.</span><span class="sxs-lookup"><span data-stu-id="a6714-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="a6714-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="a6714-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="a6714-245"><strong>Оператор:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="a6714-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="a6714-246"><strong>Инфиксная нотация:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="a6714-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a6714-247">Примеры в следующей таблице показывают запись в инфиксной нотации.</span><span class="sxs-lookup"><span data-stu-id="a6714-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="a6714-248">Нотация infix</span><span class="sxs-lookup"><span data-stu-id="a6714-248">Infix notation</span></span>    | <span data-ttu-id="a6714-249">описание</span><span class="sxs-lookup"><span data-stu-id="a6714-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6714-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="a6714-250">x + y + z</span></span>         | <span data-ttu-id="a6714-251">Сложение</span><span class="sxs-lookup"><span data-stu-id="a6714-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="a6714-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="a6714-252">x \* y \* z</span></span>       | <span data-ttu-id="a6714-253">Умножение</span><span class="sxs-lookup"><span data-stu-id="a6714-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="a6714-254">x - y</span><span class="sxs-lookup"><span data-stu-id="a6714-254">x - y</span></span>             | <span data-ttu-id="a6714-255">Двоичное вычитание преобразуется так же, как двоичное сложение с измененным знаком второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="a6714-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="a6714-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="a6714-256">x ^ y ^ z</span></span>         | <span data-ttu-id="a6714-257">Возведение в степень является правоассоциативным выражением</span><span class="sxs-lookup"><span data-stu-id="a6714-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="a6714-258">!x</span><span class="sxs-lookup"><span data-stu-id="a6714-258">!x</span></span>                | <span data-ttu-id="a6714-259">Логическое НЕ</span><span class="sxs-lookup"><span data-stu-id="a6714-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="a6714-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="a6714-260">x -: y</span></span>            | <span data-ttu-id="a6714-261">Логическая импликация</span><span class="sxs-lookup"><span data-stu-id="a6714-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="a6714-262">х</span><span class="sxs-lookup"><span data-stu-id="a6714-262">x</span></span> | <span data-ttu-id="a6714-263">y</span><span class="sxs-lookup"><span data-stu-id="a6714-263">y</span></span> | <span data-ttu-id="a6714-264">z</span><span class="sxs-lookup"><span data-stu-id="a6714-264">z</span></span>         | <span data-ttu-id="a6714-265">Логическое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="a6714-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="a6714-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="a6714-266">x & y & z</span></span>         | <span data-ttu-id="a6714-267">Логическое И</span><span class="sxs-lookup"><span data-stu-id="a6714-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="a6714-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="a6714-268">x == y == z</span></span>       | <span data-ttu-id="a6714-269">Равенство</span><span class="sxs-lookup"><span data-stu-id="a6714-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="a6714-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="a6714-270">x != y != z</span></span>       | <span data-ttu-id="a6714-271">Определенный</span><span class="sxs-lookup"><span data-stu-id="a6714-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="a6714-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="a6714-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="a6714-273">Меньше</span><span class="sxs-lookup"><span data-stu-id="a6714-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="a6714-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="a6714-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="a6714-275">Больше</span><span class="sxs-lookup"><span data-stu-id="a6714-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="a6714-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="a6714-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="a6714-277">Меньше или равен</span><span class="sxs-lookup"><span data-stu-id="a6714-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="a6714-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="a6714-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="a6714-279">Больше или равен</span><span class="sxs-lookup"><span data-stu-id="a6714-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="a6714-280">(x)</span><span class="sxs-lookup"><span data-stu-id="a6714-280">(x)</span></span>               | <span data-ttu-id="a6714-281">Скобки имеют наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="a6714-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="a6714-282">Почему мои ограничения выражений не проходят проверку?</span><span class="sxs-lookup"><span data-stu-id="a6714-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="a6714-283">Нельзя использовать зарезервированные ключевые слова, такие как имена решателя, для атрибутов, компонентов или субкомпонентов в модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="a6714-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="a6714-284">Ниже приведен список зарезервированных ключевых слов, которые нельзя использовать.</span><span class="sxs-lookup"><span data-stu-id="a6714-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="a6714-285">Ceiling</span><span class="sxs-lookup"><span data-stu-id="a6714-285">Ceiling</span></span>
-   <span data-ttu-id="a6714-286">Элемент</span><span class="sxs-lookup"><span data-stu-id="a6714-286">Element</span></span>
-   <span data-ttu-id="a6714-287">Равно</span><span class="sxs-lookup"><span data-stu-id="a6714-287">Equal</span></span>
-   <span data-ttu-id="a6714-288">Этаж</span><span class="sxs-lookup"><span data-stu-id="a6714-288">Floor</span></span>
-   <span data-ttu-id="a6714-289">Если</span><span class="sxs-lookup"><span data-stu-id="a6714-289">If</span></span>
-   <span data-ttu-id="a6714-290">Less</span><span class="sxs-lookup"><span data-stu-id="a6714-290">Less</span></span>
-   <span data-ttu-id="a6714-291">Больше</span><span class="sxs-lookup"><span data-stu-id="a6714-291">Greater</span></span>
-   <span data-ttu-id="a6714-292">Implies</span><span class="sxs-lookup"><span data-stu-id="a6714-292">Implies</span></span>
-   <span data-ttu-id="a6714-293">Журнал</span><span class="sxs-lookup"><span data-stu-id="a6714-293">Log</span></span>
-   <span data-ttu-id="a6714-294">Макс.</span><span class="sxs-lookup"><span data-stu-id="a6714-294">Max</span></span>
-   <span data-ttu-id="a6714-295">Мин.</span><span class="sxs-lookup"><span data-stu-id="a6714-295">Min</span></span>
-   <span data-ttu-id="a6714-296">Минус</span><span class="sxs-lookup"><span data-stu-id="a6714-296">Minus</span></span>
-   <span data-ttu-id="a6714-297">Плюс</span><span class="sxs-lookup"><span data-stu-id="a6714-297">Plus</span></span>
-   <span data-ttu-id="a6714-298">Мощность</span><span class="sxs-lookup"><span data-stu-id="a6714-298">Power</span></span>
-   <span data-ttu-id="a6714-299">Время</span><span class="sxs-lookup"><span data-stu-id="a6714-299">Times</span></span>
-   <span data-ttu-id="a6714-300">Интервал</span><span class="sxs-lookup"><span data-stu-id="a6714-300">Slot</span></span>
-   <span data-ttu-id="a6714-301">Модель</span><span class="sxs-lookup"><span data-stu-id="a6714-301">Model</span></span>
-   <span data-ttu-id="a6714-302">Роль в решениях</span><span class="sxs-lookup"><span data-stu-id="a6714-302">Decision</span></span>
-   <span data-ttu-id="a6714-303">Цель</span><span class="sxs-lookup"><span data-stu-id="a6714-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="a6714-304">См. также</span><span class="sxs-lookup"><span data-stu-id="a6714-304">See also</span></span>
--------

<span data-ttu-id="a6714-305">[Создание ограничения выражения (проводник по задаче)](tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="a6714-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="a6714-306">Добавление расчета к модели конфигурации продукта (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="a6714-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




