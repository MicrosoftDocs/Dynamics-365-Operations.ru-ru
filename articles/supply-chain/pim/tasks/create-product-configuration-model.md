--- 
title: "Создание модели конфигурации продукта"
description: "Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 03dae7a1b068b744ff37199c797ee62bb7dd2ae0
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="79017-103">Создание модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="79017-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79017-104">Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты.</span><span class="sxs-lookup"><span data-stu-id="79017-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="79017-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="79017-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="79017-106">Создание модели продукции</span><span class="sxs-lookup"><span data-stu-id="79017-106">Create a product model</span></span>
1. <span data-ttu-id="79017-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="79017-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="79017-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="79017-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="79017-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="79017-109">Click New.</span></span>
4. <span data-ttu-id="79017-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="79017-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="79017-112">В поле "Стратегия решателя" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="79017-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="79017-113">Стратегия поиска решения определяет, как обрабатываются ограничения в модели конфигурации на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="79017-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="79017-114">Этот выбор может повлиять на производительность модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="79017-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="79017-115">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="79017-116">Корневой компонент представляет модель конфигурации продукта, но его также можно использовать в других моделях продуктов.</span><span class="sxs-lookup"><span data-stu-id="79017-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="79017-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="79017-117">Click OK.</span></span>
9. <span data-ttu-id="79017-118">В поле "Повторно использовать конфигурации" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="79017-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="79017-119">Если параметр повторного использования конфигураций установлен как "Да", система выполнит поиск одинаковых конфигураций после каждого сеанса конфигурации и осуществит повторное использование, если найдено точное соответствие.</span><span class="sxs-lookup"><span data-stu-id="79017-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="79017-120">Добавить атрибуты</span><span class="sxs-lookup"><span data-stu-id="79017-120">Add attributes</span></span>
1. <span data-ttu-id="79017-121">Разверните раздел "Атрибуты".</span><span class="sxs-lookup"><span data-stu-id="79017-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="79017-122">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="79017-122">Click Add.</span></span>
3. <span data-ttu-id="79017-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="79017-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="79017-124">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="79017-125">В поле "Решатель" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="79017-126">Имя решателя используется решателем ограничения конфигуратора продукта.</span><span class="sxs-lookup"><span data-stu-id="79017-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="79017-127">Оно не должен содержать пробелы или специальные символы кроме _ (подчеркивания).</span><span class="sxs-lookup"><span data-stu-id="79017-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="79017-128">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="79017-129">Текст описания отображается для пользователя конфигурация и поэтому может служить справкой для выбора правильного значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="79017-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="79017-130">В поле "Тип атрибута" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="79017-131">Тип атрибута определяет, какие значения доступны для атрибута.</span><span class="sxs-lookup"><span data-stu-id="79017-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="79017-132">Установите флажок "Включить в повторное использование".</span><span class="sxs-lookup"><span data-stu-id="79017-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="79017-133">Эта форма доступна только в том случае, когда выбран параметр повторного использования конфигураций.</span><span class="sxs-lookup"><span data-stu-id="79017-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="79017-134">Включение атрибута с помощью флажка повторного использования означает, что этот атрибут будет учитываться, когда система выполняет поиск точного соответствия.</span><span class="sxs-lookup"><span data-stu-id="79017-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="79017-135">Добавление субкомпонентов</span><span class="sxs-lookup"><span data-stu-id="79017-135">Add subcomponents</span></span>
1. <span data-ttu-id="79017-136">Разверните раздел "Субкомпоненты".</span><span class="sxs-lookup"><span data-stu-id="79017-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="79017-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="79017-137">Click Add.</span></span>
3. <span data-ttu-id="79017-138">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="79017-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="79017-139">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="79017-140">В поле "Решатель" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="79017-141">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="79017-142">В поле "Компонент" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="79017-143">Каждый субкомпонент должен ссылаться на определение компонента.</span><span class="sxs-lookup"><span data-stu-id="79017-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="79017-144">Эта структура поддерживает многоразовые компоненты и гарантирует, что после определения компонента его можно использовать во многих моделях продуктов.</span><span class="sxs-lookup"><span data-stu-id="79017-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="79017-145">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="79017-145">Click Save.</span></span>
9. <span data-ttu-id="79017-146">Щелкните "Сведения о строке спецификации".</span><span class="sxs-lookup"><span data-stu-id="79017-146">Click BOM line details.</span></span>
    * <span data-ttu-id="79017-147">Форма сведений строки спецификации позволяет пользователю выбрать нужные свойства для субкомпонента.</span><span class="sxs-lookup"><span data-stu-id="79017-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="79017-148">Каждому свойству можно задать фиксированное значение или сопоставить с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="79017-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="79017-149">Сопоставление с атрибутом приведет к тому, что в свойстве строки спецификации будут разные значения в зависимости от выбора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="79017-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="79017-150">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="79017-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="79017-151">Каждый субкомпонент представляет настраиваемый шаблон продукта с учетом технологии конфигурации на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="79017-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="79017-152">Ссылка дается с помощью кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="79017-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="79017-153">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="79017-153">Select the Set check box.</span></span>
12. <span data-ttu-id="79017-154">Выберите значение "Да" в поле "Расчет".</span><span class="sxs-lookup"><span data-stu-id="79017-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="79017-155">Установка параметра расчета гарантирует, что продукт будет включен при выполнении расчета затрат для продукта.</span><span class="sxs-lookup"><span data-stu-id="79017-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="79017-156">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="79017-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="79017-157">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="79017-157">Select the Set check box.</span></span>
15. <span data-ttu-id="79017-158">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="79017-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="79017-159">Поле количества определяет, сколько этого продукта будет потреблено в настроенном продукте.</span><span class="sxs-lookup"><span data-stu-id="79017-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="79017-160">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="79017-160">Select the Set check box.</span></span>
17. <span data-ttu-id="79017-161">В поле "В серии" введите число.</span><span class="sxs-lookup"><span data-stu-id="79017-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="79017-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="79017-162">Click OK.</span></span>


