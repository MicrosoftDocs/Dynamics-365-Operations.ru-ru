---
title: Инженерные атрибуты и поиск инженерных атрибутов
description: В этой теме объясняется, как можно использовать инженерные атрибуты для указания всех нестандартных характеристик, чтобы гарантировать, что все данные шаблонов продуктов могут быть зарегистрированы в системе. В нем также объясняется, как можно использовать поиск инженерных атрибутов для быстрого поиска продуктов на основе их зарегистрированных характеристик.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 32cd2c6d0915df1e48973a22a7d391eb8d62a072
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963696"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a><span data-ttu-id="0976f-104">Инженерные атрибуты и поиск инженерных атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-104">Engineering attributes and engineering attribute search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0976f-105">Чтобы гарантировать, что все данные шаблонов продуктов могут быть зарегистрированы в системе, необходимо использовать инженерные атрибуты для указания всех нестандартных характеристик.</span><span class="sxs-lookup"><span data-stu-id="0976f-105">To ensure that all product master data can be registered in the system, you should use engineering attributes to specify all non-standard characteristics.</span></span> <span data-ttu-id="0976f-106">Затем вы можете использовать поиск инженерных атрибутов для быстрого поиска продуктов на основе их зарегистрированных характеристик.</span><span class="sxs-lookup"><span data-stu-id="0976f-106">You can then use engineering attribute search to easily find products, based on those registered characteristics.</span></span>

## <a name="engineering-attributes"></a><span data-ttu-id="0976f-107">Атрибуты разработки</span><span class="sxs-lookup"><span data-stu-id="0976f-107">Engineering attributes</span></span>

<span data-ttu-id="0976f-108">Обычно у инженерных продуктов много характеристик и свойств, которые необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="0976f-108">Typically, engineering products have many characteristics and properties that you must capture.</span></span> <span data-ttu-id="0976f-109">Хотя некоторые свойства можно зарегистрировать с помощью стандартных полей продукта, в случае необходимости можно также создать новые инженерные свойства.</span><span class="sxs-lookup"><span data-stu-id="0976f-109">Although you can register some of the properties by using the standard product fields, you can also create new engineering properties as required.</span></span> <span data-ttu-id="0976f-110">Можно определить собственные *инженерные атрибуты* и сделать их частью определения продукта.</span><span class="sxs-lookup"><span data-stu-id="0976f-110">You can define your own *engineering attributes* and make them part of the product definition.</span></span>

### <a name="create-engineering-attributes-and-attribute-types"></a><span data-ttu-id="0976f-111">Создание технологических атрибутов и типов атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-111">Create engineering attributes and attribute types</span></span>

<span data-ttu-id="0976f-112">Каждый инженерный атрибут должен принадлежать к *типу атрибута*.</span><span class="sxs-lookup"><span data-stu-id="0976f-112">Each engineering attribute must belong to an *attribute type*.</span></span> <span data-ttu-id="0976f-113">Это требование обусловлено тем, что каждый технологический атрибут должен иметь *тип данных*, определяющий типы значений, которые он может содержать.</span><span class="sxs-lookup"><span data-stu-id="0976f-113">This requirement exists because each engineering attribute must have a *data type* that defines the types of values that it can hold.</span></span> <span data-ttu-id="0976f-114">Тип инженерных атрибутов может быть стандартным типом (например, произвольным текстом, целым числом или десятичным числом) или настраиваемым типом (например, текстом, имеющим конкретный набор значений для выбора).</span><span class="sxs-lookup"><span data-stu-id="0976f-114">An engineering attribute type can be a standard type (such as free text, integer, or decimal) or a custom type (such as text that has a specific set of values to select from).</span></span> <span data-ttu-id="0976f-115">Каждый тип атрибута можно повторно использовать с любым количеством инженерных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0976f-115">You can reuse each attribute type with any number of engineering attributes.</span></span>

#### <a name="set-up-engineering-attribute-types"></a><span data-ttu-id="0976f-116">Настройка типов инженерных атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-116">Set up engineering attribute types</span></span>

<span data-ttu-id="0976f-117">Чтобы просмотреть, создать или изменить тип инженерного атрибута, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0976f-117">To view, create, or edit an engineering attribute type, follow these steps.</span></span>

1. <span data-ttu-id="0976f-118">Перейдите в раздел **Управление техническими изменениями \> Настройка \> Атрибуты \> Типы атрибутов**.</span><span class="sxs-lookup"><span data-stu-id="0976f-118">Go to **Engineering change management \> Setup \> Attributes \> Attribute types**.</span></span>
1. <span data-ttu-id="0976f-119">Выберите существующий тип атрибута в области списка или выберите **Создать** на панели операций, чтобы создать новый тип атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-119">Select an existing attribute type in the list pane, or select **New** on the Action Pane to create a new attribute type.</span></span>
1. <span data-ttu-id="0976f-120">Задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="0976f-120">Set the following fields:</span></span>

    - <span data-ttu-id="0976f-121">**Имя типа атрибута** — введите название для типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-121">**Attribute type name** – Enter a name for the attribute type.</span></span>
    - <span data-ttu-id="0976f-122">**Тип** — выберите стандартный тип данных (*Валюта*, *Дата и время*, *Десятичное число*, *Целое число*, *Текст*, *Логическое* или *Ссылка*).</span><span class="sxs-lookup"><span data-stu-id="0976f-122">**Type** – Select a standard data type (*Currency*, *DateTime*, *Decimal*, *Integer*, *Text*, *Boolean*, or *Reference*).</span></span>
    - <span data-ttu-id="0976f-123">**Фиксированный список** — этот параметр доступен только в том случае, если для поля **Тип** установлено значение *Текст*.</span><span class="sxs-lookup"><span data-stu-id="0976f-123">**Fixed list** – This option is available only if you set the **Type** field to *Text*.</span></span> <span data-ttu-id="0976f-124">Установите значение *Да*, чтобы определить определенные значения для атрибутов этого типа.</span><span class="sxs-lookup"><span data-stu-id="0976f-124">Set it to *Yes* to define specific values for attributes of this type.</span></span> <span data-ttu-id="0976f-125">В этом случае будет создан раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="0976f-125">In this case, a drop-down list will be created.</span></span> <span data-ttu-id="0976f-126">Для задания значений, доступных для этого типа атрибута, используется экспресс-вкладка **Значение**.</span><span class="sxs-lookup"><span data-stu-id="0976f-126">You use the **Value** FastTab to establish the values that are available for this attribute type.</span></span> <span data-ttu-id="0976f-127">Установите для этого параметра значение *Нет*, чтобы пользователи не могли вводить какие-либо значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-127">Set this option to *No* to allow users to enter any value.</span></span> <span data-ttu-id="0976f-128">В этом случае будет создано поле ввода.</span><span class="sxs-lookup"><span data-stu-id="0976f-128">In this case, an input field will be created.</span></span>
    - <span data-ttu-id="0976f-129">**Диапазон значений** — этот параметр доступен только в том случае, если в поле **Тип** указано *Целое число*, *Десятичное число* или *Валюта*.</span><span class="sxs-lookup"><span data-stu-id="0976f-129">**Value range** – This option is available only if you set the **Type** field to *Integer*, *Decimal*, or *Currency*.</span></span> <span data-ttu-id="0976f-130">Установите значение *Да*, чтобы установить минимальное и максимальное значения, которые будут приниматься для атрибутов этого типа.</span><span class="sxs-lookup"><span data-stu-id="0976f-130">Set it to *Yes* to establish minimum and maximum values that will be accepted for attributes of this type.</span></span> <span data-ttu-id="0976f-131">Для определения минимальных и максимальных значений, а также (для валюты) денежной единицы, которая применяется для введенных вами ограничений, используется экспресс-вкладка **Диапазон**.</span><span class="sxs-lookup"><span data-stu-id="0976f-131">You use the **Range** FastTab to establish the minimum and maximum values, and (for currency) the currency that applies for the limits that you entered.</span></span> <span data-ttu-id="0976f-132">Установите для этого параметра значение *Нет*, чтобы принимать любые значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-132">Set this option to *No* to accept any value.</span></span> 
    - <span data-ttu-id="0976f-133">**Единица измерения** — это поле доступно только в том случае, если в поле **Тип** указано *Целое число* или *Десятичное число*.</span><span class="sxs-lookup"><span data-stu-id="0976f-133">**Unit of measure** – This field is available only if you set the **Type** field to *Integer* or *Decimal*.</span></span> <span data-ttu-id="0976f-134">Выберите единицу измерения, которая применяется для этого типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-134">Select the unit of measure that applies for this attribute type.</span></span> <span data-ttu-id="0976f-135">Если единица измерения не требуется, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0976f-135">If no unit is required, leave this field blank.</span></span>

#### <a name="set-up-engineering-attributes"></a><span data-ttu-id="0976f-136">Настройка инженерных атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-136">Set up engineering attributes</span></span>

<span data-ttu-id="0976f-137">Чтобы просмотреть, создать или изменить инженерный атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0976f-137">To view, create, or edit an engineering attribute, follow these steps.</span></span>

1. <span data-ttu-id="0976f-138">Перейдите в раздел **Управление техническими изменениями \> Настройка \> Атрибуты \> Инженерные атрибуты**.</span><span class="sxs-lookup"><span data-stu-id="0976f-138">Go to **Engineering change management \> Setup \> Attributes \> Engineering attributes**.</span></span>
1. <span data-ttu-id="0976f-139">Выберите существующий атрибут в области списка или выберите **Создать** на панели операций, чтобы создать новый атрибут.</span><span class="sxs-lookup"><span data-stu-id="0976f-139">Select an existing attribute in the list pane, or select **New** on the Action Pane to create a new attribute.</span></span>
1. <span data-ttu-id="0976f-140">Задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="0976f-140">Set the following fields:</span></span>

    - <span data-ttu-id="0976f-141">**Имя** — введите имя для атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-141">**Name** – Enter a name for the attribute.</span></span> <span data-ttu-id="0976f-142">Это имя отображается только на странице **Инженерные атрибуты**.</span><span class="sxs-lookup"><span data-stu-id="0976f-142">This name appears only on the **Engineering attributes** page.</span></span> <span data-ttu-id="0976f-143">В любом другом месте в системе значение поля **Понятное имя** обычно отображается для идентификации атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-143">Everywhere else in the system, the value of the **Friendly name** field is usually shown to identify the attribute.</span></span>
    - <span data-ttu-id="0976f-144">**Тип атрибута** — выберите тип атрибута, который был определен в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="0976f-144">**Attribute type** – Select an attribute type that you defined in the previous section.</span></span>
    - <span data-ttu-id="0976f-145">**Понятное имя** — введите имя, которое будет определять атрибут в системе (за исключением страницы **Инженерные атрибуты**).</span><span class="sxs-lookup"><span data-stu-id="0976f-145">**Friendly name** – Enter a name that will identify the attribute in the system (except on the **Engineering attributes** page).</span></span> 
    - <span data-ttu-id="0976f-146">**Описание** — введите описание атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-146">**Description** – Enter a description of the attribute.</span></span>
    - <span data-ttu-id="0976f-147">**Текст справки** — введите текст справки, который сообщает другим пользователям о том, для чего используется данный атрибут.</span><span class="sxs-lookup"><span data-stu-id="0976f-147">**Help text** – Enter Help text that tells other users what the attribute is for.</span></span>
    - <span data-ttu-id="0976f-148">**Значение по умолчанию** — введите значение по умолчанию для атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-148">**Default value** – Enter a default value for the attribute.</span></span> <span data-ttu-id="0976f-149">Параметры, которые отображаются, зависят от выбранного типа атрибута.</span><span class="sxs-lookup"><span data-stu-id="0976f-149">The options that are presented depend on the attribute type that you selected.</span></span>
    - <span data-ttu-id="0976f-150">**Валюта** — если выбранный тип атрибута является валютой, выберите валюту, которую должен принимать этот атрибут и отображать в ней значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-150">**Currency** – If the attribute type that you selected is a currency, select the currency that the attribute will accept and show values in.</span></span>

1. <span data-ttu-id="0976f-151">Если выбранный тип атрибута является целым или десятичным числом, отображается экспресс-вкладка **Диапазон**.</span><span class="sxs-lookup"><span data-stu-id="0976f-151">If the attribute type that you selected is an integer or a decimal, the **Range** FastTab is shown.</span></span> <span data-ttu-id="0976f-152">На этой экспресс-вкладке настройте следующие поля требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="0976f-152">On this FastTab, set the following fields as required:</span></span>

    - <span data-ttu-id="0976f-153">**Действие по обеспечению допуска** — выберите способ реакции системы, если пользователь вводит значение вне указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="0976f-153">**Tolerance action** – Select how the system should respond if a user enters a value outside the specified range.</span></span> <span data-ttu-id="0976f-154">Если выбрать *Предупреждение*, отображается предупреждение, но пользователь может сохранить значение.</span><span class="sxs-lookup"><span data-stu-id="0976f-154">If you select *Warning*, a warning is shown, but the user can save the value.</span></span> <span data-ttu-id="0976f-155">Если выбрано значение *Не разрешено*, будет выведено предупреждение, и значение невозможно сохранить до тех пор, пока оно не будет исправлено пользователем.</span><span class="sxs-lookup"><span data-stu-id="0976f-155">If you select *Not allowed*, a warning is shown, and the value can't be saved until the user corrects it.</span></span>
    - <span data-ttu-id="0976f-156">**Минимум** — используется для ввода минимального рекомендуемого или приемлемого значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-156">**Minimum** – Enter the minimum recommended or accepted value.</span></span>
    - <span data-ttu-id="0976f-157">**Максимум** — используется для ввода максимального рекомендуемого или приемлемого значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-157">**Maximum** – Enter the maximum recommended or accepted value.</span></span>

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a><span data-ttu-id="0976f-158">Соединение технологических атрибутов с категорией технологических продуктов</span><span class="sxs-lookup"><span data-stu-id="0976f-158">Connect engineering attributes to an engineering product category</span></span>

<span data-ttu-id="0976f-159">Некоторые технологические атрибуты применяются ко всем продуктам, в то время как другие относятся к отдельным продуктам или категориям продуктов.</span><span class="sxs-lookup"><span data-stu-id="0976f-159">Some engineering attributes apply to all products, whereas others are specific to individual products or product categories.</span></span> <span data-ttu-id="0976f-160">Например, электрические атрибуты не требуются для механических продуктов.</span><span class="sxs-lookup"><span data-stu-id="0976f-160">For example, electrical attributes aren't required for mechanical products.</span></span> <span data-ttu-id="0976f-161">Таким образом, можно настроить *категории технологических продуктов*.</span><span class="sxs-lookup"><span data-stu-id="0976f-161">Therefore, you can set up *engineering product categories*.</span></span> <span data-ttu-id="0976f-162">Категория технологических продуктов определяет коллекцию технологических атрибутов, которые должны быть частью определения продуктов, принадлежащих данной категории.</span><span class="sxs-lookup"><span data-stu-id="0976f-162">An engineering product category establishes the collection of engineering attributes that must be part of the definition for products that belong to that category.</span></span> <span data-ttu-id="0976f-163">Можно также указать, какие технологические атрибуты являются обязательными, и имеется ли значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0976f-163">You can also specify which engineering attributes are mandatory and whether there is a default value.</span></span>

<span data-ttu-id="0976f-164">Дополнительные сведения о работе с категориями технологических продуктов, включая сведения о способах подключения атрибутов к категориям, см. в разделе [Инженерные версии и категории технологических продуктов](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="0976f-164">For more information about how to work with engineering product categories, including information about how to connect attributes to categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

### <a name="set-values-for-engineering-attributes"></a><span data-ttu-id="0976f-165">Задание значений для технологических атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-165">Set values for engineering attributes</span></span>

<span data-ttu-id="0976f-166">Инженерные атрибуты, которые связаны с категорией технологических продуктов, представлены при создании нового инженерного продукта, основанного на этой категории.</span><span class="sxs-lookup"><span data-stu-id="0976f-166">The engineering attributes that are connected to an engineering product category are presented when you create a new engineering product that is based on that category.</span></span> <span data-ttu-id="0976f-167">В это время можно задать значения для атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0976f-167">At that time, you can set values for the attributes.</span></span> <span data-ttu-id="0976f-168">Впоследствии эти значения можно изменить на странице **Инженерная версия** или в рамках управления техническими изменениями в заказе на техническое изменение.</span><span class="sxs-lookup"><span data-stu-id="0976f-168">Later, those values can be changed on the **Engineering version** page or as part of engineering change management in an engineering change order.</span></span> <span data-ttu-id="0976f-169">Дополнительные сведения см. в разделе [Управления изменениями для технологических продуктов](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="0976f-169">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>

### <a name="create-an-engineering-product"></a><span data-ttu-id="0976f-170">Создание технического продукта</span><span class="sxs-lookup"><span data-stu-id="0976f-170">Create an engineering product</span></span>

<span data-ttu-id="0976f-171">Чтобы создать инженерный продукт, откройте страницу **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="0976f-171">To create an engineering product, open the **Released products** page.</span></span> <span data-ttu-id="0976f-172">Затем в области действий на вкладке **Продукт** в группе **Создать** выберите **Технический продукт**.</span><span class="sxs-lookup"><span data-stu-id="0976f-172">Then, on the Action Pane, on **Product** tab, in the **New** group, select **Engineering product**.</span></span>

<span data-ttu-id="0976f-173">Необходимо указать инженерную категорию, к которой относится продукт.</span><span class="sxs-lookup"><span data-stu-id="0976f-173">You must specify the engineering category that the product belongs to.</span></span> <span data-ttu-id="0976f-174">В категории будут установлены все значения и характеристики продукта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0976f-174">The category will set all the default values and characteristics for the product.</span></span> <span data-ttu-id="0976f-175">Также будут установлены атрибуты, применимые к продукту.</span><span class="sxs-lookup"><span data-stu-id="0976f-175">It will also set the attributes that are applicable to the product.</span></span> <span data-ttu-id="0976f-176">После того как выбрана категория, для атрибутов будут заданы значения.</span><span class="sxs-lookup"><span data-stu-id="0976f-176">After the category is selected, values will be set for the attributes.</span></span> <span data-ttu-id="0976f-177">Затем эти значения можно изменить.</span><span class="sxs-lookup"><span data-stu-id="0976f-177">You can then modify those values.</span></span>

## <a name="search-for-products-by-using-engineering-attribute-values"></a><span data-ttu-id="0976f-178">Поиск продуктов с использованием значений инженерных атрибутов</span><span class="sxs-lookup"><span data-stu-id="0976f-178">Search for products by using engineering attribute values</span></span>

<span data-ttu-id="0976f-179">Поиск продуктов можно выполнить с помощью поиска инженерных атрибутов, выполнив поиск их значений инженерных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0976f-179">You can use engineering attribute search to find products by searching for their engineering attributes values.</span></span> <span data-ttu-id="0976f-180">Таким образом, на основе их характеристик можно легко найти инженерные продукты.</span><span class="sxs-lookup"><span data-stu-id="0976f-180">Therefore, you can easily find engineering products, based on their characteristics.</span></span> <span data-ttu-id="0976f-181">Можно выполнять поиск в продуктах, относящихся к категории технологических продуктов, или можно выполнять поиск во всех технологических продуктах.</span><span class="sxs-lookup"><span data-stu-id="0976f-181">You can search in the products that belong to an engineering product category, or you can search across all engineering products.</span></span>

<span data-ttu-id="0976f-182">Поиск доступен на страницах шаблонов продуктов и из элементов проводок в системе, например заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="0976f-182">The search is available on product master data pages and from transactional items in the system, such as sales orders.</span></span> <span data-ttu-id="0976f-183">Для транзакционной номенклатуры можно использовать страницу **Поиск инженерных атрибутов**, чтобы выполнить поиск продукта.</span><span class="sxs-lookup"><span data-stu-id="0976f-183">For a transactional item, you can use the **Engineering attribute search** page to search for a product.</span></span> <span data-ttu-id="0976f-184">Затем можно использовать кнопку **Добавить как новую строку**, чтобы добавить продукт в строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="0976f-184">You can then use the **Add as new line** button to add the product to the sales order lines.</span></span> <span data-ttu-id="0976f-185">Продукты в результатах поиска могут быть также добавлены непосредственно в заказ.</span><span class="sxs-lookup"><span data-stu-id="0976f-185">Products in the search results can also be added directly to the order.</span></span>