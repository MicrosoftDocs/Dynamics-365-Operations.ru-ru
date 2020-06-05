---
title: Управление единицей измерения
description: В этой процедуре показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc02c73ae36975fa4872d638fe53cbf0379d15d
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383673"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="9f10f-103">Управление единицей измерения</span><span class="sxs-lookup"><span data-stu-id="9f10f-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f10f-104">В этой процедуре показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="9f10f-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="9f10f-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="9f10f-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="9f10f-106">Перейдите в раздел **Область перехода > Модули > Управление сведениями о продукте > Обслуживание выпущенного продукта**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="9f10f-107">Щелкните **Единицы измерения**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="9f10f-108">Создание единицы измерения</span><span class="sxs-lookup"><span data-stu-id="9f10f-108">Create a unit of measure</span></span>
1. <span data-ttu-id="9f10f-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-109">Click **New**.</span></span>
2. <span data-ttu-id="9f10f-110">В поле **Единица измерения** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="9f10f-111">Введите код или символ, который будет использоваться при ссылке на единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="9f10f-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="9f10f-112">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="9f10f-113">Введите описательное имя для единицы измерения на системном языке.</span><span class="sxs-lookup"><span data-stu-id="9f10f-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="9f10f-114">В поле **Класс единиц измерения** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="9f10f-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="9f10f-115">Класс единиц измерения определяет, к какому логическому группированию (такому как площадь, масса или количество) принадлежит единица измерения.</span><span class="sxs-lookup"><span data-stu-id="9f10f-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="9f10f-116">В поле **Десятичная точность** введите число.</span><span class="sxs-lookup"><span data-stu-id="9f10f-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="9f10f-117">Укажите количество символов после запятой, до которого должна округляться пересчитанная единица измерения при выполнении вычислений для этой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="9f10f-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="9f10f-118">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="9f10f-119">Определение переводов для единицы измерения</span><span class="sxs-lookup"><span data-stu-id="9f10f-119">Define unit translations</span></span>
1. <span data-ttu-id="9f10f-120">На **Панели операций** щелкните **Тексты к единицам измерения**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="9f10f-121">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-121">Click **New**.</span></span> <span data-ttu-id="9f10f-122">Используйте текст к единице измерения для создания перевода кода или символа, представляющего единицу измерения, для использования во внешних документах на языках клиентов или поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9f10f-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="9f10f-123">В поле **Язык** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="9f10f-124">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="9f10f-125">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-125">Click **Save**.</span></span>
6. <span data-ttu-id="9f10f-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f10f-126">Close the page.</span></span>
7. <span data-ttu-id="9f10f-127">На **Панели операций** щелкните **Описания пересчитанных единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="9f10f-128">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-128">Click **New**.</span></span> <span data-ttu-id="9f10f-129">Определите описания единицы измерения для конкретных языков.</span><span class="sxs-lookup"><span data-stu-id="9f10f-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="9f10f-130">В поле **Язык** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="9f10f-131">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="9f10f-132">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-132">Click **Save**.</span></span>
12. <span data-ttu-id="9f10f-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f10f-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="9f10f-134">Определение правил пересчета единицы измерения</span><span class="sxs-lookup"><span data-stu-id="9f10f-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="9f10f-135">На **Панели операций** щелкните **Пересчеты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="9f10f-136">Определите правила для пересчета единицы измерения в другие единицы измерения (и из них) в выбранном классе единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="9f10f-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="9f10f-137">Щелкните **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="9f10f-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="9f10f-138">В поле **Коэффициент** введите число.</span><span class="sxs-lookup"><span data-stu-id="9f10f-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="9f10f-139">Коэффициент пересчета между единицей измерения "Из" и единицей измерения "В".</span><span class="sxs-lookup"><span data-stu-id="9f10f-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="9f10f-140">Например, коэффициент пересчета из сантиметров в метры равен 100, потому что в одном метре 100 сантиметров.</span><span class="sxs-lookup"><span data-stu-id="9f10f-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="9f10f-141">В поле **В ед. изм.** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="9f10f-142">В поле **Округление** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="9f10f-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="9f10f-143">Определите, как должно округляться пересчитанное значение.</span><span class="sxs-lookup"><span data-stu-id="9f10f-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="9f10f-144">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f10f-144">Click **OK**.</span></span>
7. <span data-ttu-id="9f10f-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f10f-145">Close the page.</span></span>

