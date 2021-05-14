---
title: Создание модели конфигурации продукта
description: Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921373"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="bc45d-103">Создание модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="bc45d-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc45d-104">Ниже описан порядок создания модели конфигурации продукта и ввода основных сведений, таких как атрибуты и субкомпоненты.</span><span class="sxs-lookup"><span data-stu-id="bc45d-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="bc45d-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bc45d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="bc45d-106">Создание модели продукции</span><span class="sxs-lookup"><span data-stu-id="bc45d-106">Create a product model</span></span>

1. <span data-ttu-id="bc45d-107">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="bc45d-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-108">Select **New**.</span></span>
1. <span data-ttu-id="bc45d-109">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="bc45d-110">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="bc45d-111">В поле **Стратегия поиска решения** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="bc45d-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="bc45d-112">Стратегия поиска решения определяет, как обрабатываются ограничения в модели конфигурации на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="bc45d-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="bc45d-113">Этот выбор может повлиять на производительность модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="bc45d-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="bc45d-114">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="bc45d-115">Корневой компонент представляет модель конфигурации продукта, но его также можно использовать в других моделях продуктов.</span><span class="sxs-lookup"><span data-stu-id="bc45d-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="bc45d-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-116">Select **OK**.</span></span>
1. <span data-ttu-id="bc45d-117">В поле **Повторно использовать конфигурации** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="bc45d-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="bc45d-118">Если параметр повторного использования конфигураций установлен как "Да", система выполнит поиск одинаковых конфигураций после каждого сеанса конфигурации и осуществит повторное использование, если найдено точное соответствие.</span><span class="sxs-lookup"><span data-stu-id="bc45d-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="bc45d-119">Добавить атрибуты</span><span class="sxs-lookup"><span data-stu-id="bc45d-119">Add attributes</span></span>

1. <span data-ttu-id="bc45d-120">Разверните раздел **Атрибуты**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="bc45d-121">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-121">Select **Add**.</span></span>
3. <span data-ttu-id="bc45d-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bc45d-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bc45d-123">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="bc45d-124">В поле **Имя решателя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="bc45d-125">Имя решателя используется решателем ограничения конфигуратора продукта.</span><span class="sxs-lookup"><span data-stu-id="bc45d-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="bc45d-126">Оно не должен содержать пробелы или специальные символы кроме _ (подчеркивания).</span><span class="sxs-lookup"><span data-stu-id="bc45d-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="bc45d-127">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="bc45d-128">Текст описания отображается для пользователя конфигурация и поэтому может служить справкой для выбора правильного значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="bc45d-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="bc45d-129">В поле **Тип атрибута** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc45d-130">Тип атрибута определяет, какие значения доступны для атрибута.</span><span class="sxs-lookup"><span data-stu-id="bc45d-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="bc45d-131">Установите флажок **Включить в повторное использование**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="bc45d-132">Эта форма доступна только в том случае, когда выбран параметр повторного использования конфигураций.</span><span class="sxs-lookup"><span data-stu-id="bc45d-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="bc45d-133">Включение атрибута с помощью флажка повторного использования означает, что этот атрибут будет учитываться, когда система выполняет поиск точного соответствия.</span><span class="sxs-lookup"><span data-stu-id="bc45d-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="bc45d-134">Добавление субкомпонентов</span><span class="sxs-lookup"><span data-stu-id="bc45d-134">Add subcomponents</span></span>

1. <span data-ttu-id="bc45d-135">Разверните раздел **Субкомпоненты**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="bc45d-136">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-136">Select **Add**.</span></span>
3. <span data-ttu-id="bc45d-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bc45d-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bc45d-138">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="bc45d-139">В поле **Имя решателя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="bc45d-140">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="bc45d-141">В поле **Компонент** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc45d-142">Каждый субкомпонент должен ссылаться на определение компонента.</span><span class="sxs-lookup"><span data-stu-id="bc45d-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="bc45d-143">Эта структура поддерживает многоразовые компоненты и гарантирует, что после определения компонента его можно использовать во многих моделях продуктов.</span><span class="sxs-lookup"><span data-stu-id="bc45d-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="bc45d-144">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-144">Select **Save**.</span></span>
9. <span data-ttu-id="bc45d-145">Выберите **Сведения о строке спецификации**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="bc45d-146">Форма сведений строки спецификации позволяет пользователю выбрать нужные свойства для субкомпонента.</span><span class="sxs-lookup"><span data-stu-id="bc45d-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="bc45d-147">Каждому свойству можно задать фиксированное значение или сопоставить с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="bc45d-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="bc45d-148">Сопоставление с атрибутом приведет к тому, что в свойстве строки спецификации будут разные значения в зависимости от выбора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bc45d-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="bc45d-149">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bc45d-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc45d-150">Каждый субкомпонент представляет настраиваемый шаблон продукта с учетом технологии конфигурации на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="bc45d-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="bc45d-151">Ссылка дается с помощью кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="bc45d-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="bc45d-152">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="bc45d-153">Выберите значение **Да** в поле **Расчет**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="bc45d-154">Установка параметра расчета гарантирует, что продукт будет включен при выполнении расчета затрат для продукта.</span><span class="sxs-lookup"><span data-stu-id="bc45d-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="bc45d-155">Выберите вкладку **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="bc45d-156">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="bc45d-157">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="bc45d-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="bc45d-158">Поле количества определяет, сколько этого продукта будет потреблено в настроенном продукте.</span><span class="sxs-lookup"><span data-stu-id="bc45d-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="bc45d-159">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="bc45d-160">В поле **В серии** введите число.</span><span class="sxs-lookup"><span data-stu-id="bc45d-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="bc45d-161">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bc45d-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]