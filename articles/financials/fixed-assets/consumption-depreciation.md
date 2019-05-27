---
title: Амортизация потребления
description: Эта статья содержит обзор метода амортизации "Потребление".
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f64fee275f63a3e6b31a196df872e41c84dde6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562561"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="6aec3-103">Амортизация потребления</span><span class="sxs-lookup"><span data-stu-id="6aec3-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6aec3-104">Эта статья содержит обзор метода амортизации "Потребление".</span><span class="sxs-lookup"><span data-stu-id="6aec3-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="6aec3-105">При настройке профиля амортизации основных средств и выборе значения **Потребление** в поле **Метод** на странице **Профили амортизации** основные средства назначаются этому профилю амортизации на основе их использования.</span><span class="sxs-lookup"><span data-stu-id="6aec3-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="6aec3-106">Вы не должны настроить проценты и интервалы на странице **Профили амортизации**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="6aec3-107">После создания профиля амортизации, использующего метод "Потребление", этот метод можно настроить различными способами.</span><span class="sxs-lookup"><span data-stu-id="6aec3-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="6aec3-108">Настройка и использование амортизации потребления</span><span class="sxs-lookup"><span data-stu-id="6aec3-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="6aec3-109">На странице **Профили амортизации** создайте профиль амортизации.</span><span class="sxs-lookup"><span data-stu-id="6aec3-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="6aec3-110">Для выполнения расчетов потребления профиль амортизации должен включать код и название, а в поле **Метод** должно быть выбрано значение **Потребление**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="6aec3-111">На странице **Коэффициенты выпуска/пробега** настройте факторы потребления.</span><span class="sxs-lookup"><span data-stu-id="6aec3-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="6aec3-112">Каждый коэффициент потребления должен иметь код и название и коэффициент потребления, который указан как количество или как процент.</span><span class="sxs-lookup"><span data-stu-id="6aec3-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="6aec3-113">На странице **Единицы измерения потребления** настройте единицы измерения потребления.</span><span class="sxs-lookup"><span data-stu-id="6aec3-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="6aec3-114">Каждая единица потребления должна иметь код и название.</span><span class="sxs-lookup"><span data-stu-id="6aec3-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="6aec3-115">Единицы измерения амортизации используются для расчета амортизации по потреблению на странице **Амортизация потребления**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="6aec3-116">Примерами единиц измерения являются кг, км и час.</span><span class="sxs-lookup"><span data-stu-id="6aec3-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="6aec3-117">На странице **Основные фонды** настройте индивидуальные основные фонды.</span><span class="sxs-lookup"><span data-stu-id="6aec3-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="6aec3-118">Для каждого основного средства выберите модели стоимости и журналы амортизации, имеющие методы амортизации.</span><span class="sxs-lookup"><span data-stu-id="6aec3-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="6aec3-119">Необходимо настроить модели стоимости или журналы амортизации для амортизации потребления, если какие-либо основные средства используют профили амортизации на основе метода амортизации "Потребление".</span><span class="sxs-lookup"><span data-stu-id="6aec3-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="6aec3-120">Эта настройка выполняется на вкладке **Амортизация** страницы **Модели стоимости** или на экспресс-вкладке **Общие** страницы **Профиль амортизации**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="6aec3-121">Одну и ту же модель стоимости можно использовать для нескольких основных средств.</span><span class="sxs-lookup"><span data-stu-id="6aec3-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="6aec3-122">Методы амортизации являются частью модели стоимости или журнала амортизации, которые выбираются для каждого основного средства.</span><span class="sxs-lookup"><span data-stu-id="6aec3-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="6aec3-123">Невозможно добавлять или изменять методы непосредственно на странице **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="6aec3-124">Вы можете изменить профили амортизации только на странице **Журналы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="6aec3-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="6aec3-125">На странице **Модели стоимости** или **Журналы амортизации** в группе полей **Амортизация потребления** введите сведения в следующих полях:</span><span class="sxs-lookup"><span data-stu-id="6aec3-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="6aec3-126">Коэффициент выпуска/пробега</span><span class="sxs-lookup"><span data-stu-id="6aec3-126">Consumption factor</span></span>
    -   <span data-ttu-id="6aec3-127">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="6aec3-127">Unit</span></span>
    -   <span data-ttu-id="6aec3-128">Единица измерения амортизации</span><span class="sxs-lookup"><span data-stu-id="6aec3-128">Unit depreciation</span></span>
    -   <span data-ttu-id="6aec3-129">Оценка потребления</span><span class="sxs-lookup"><span data-stu-id="6aec3-129">Estimated consumption</span></span>

    <span data-ttu-id="6aec3-130">В поле **Разнесенное потребление** отображается амортизация потребления в единицах, которые уже были разнесены для комбинации основных средств и модели стоимости или для журнала амортизации.</span><span class="sxs-lookup"><span data-stu-id="6aec3-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="6aec3-131">Значение этого поля нельзя изменить вручную.</span><span class="sxs-lookup"><span data-stu-id="6aec3-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="6aec3-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="6aec3-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="6aec3-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6aec3-133">Example 1</span></span>

<span data-ttu-id="6aec3-134">Следующий коэффициент выпуска/пробега настроен для 31 января:</span><span class="sxs-lookup"><span data-stu-id="6aec3-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="6aec3-135">Количество равно 1 000.</span><span class="sxs-lookup"><span data-stu-id="6aec3-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="6aec3-136">Цена за единицу измерения амортизации, указанная для основных средств, равна 1,5.</span><span class="sxs-lookup"><span data-stu-id="6aec3-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="6aec3-137">Предложение амортизации от 31-го января выглядит следующим образом: Количество × Единица измерения амортизации 1 000× 1,5 = 1 500 Если коэффициент, который определен для основных средств, является процентным коэффициентом, количество, оцененное в поле **Оценка потребления** для модели стоимости основных средств, умножается на процент, который настроен для выбранной даты окончания.</span><span class="sxs-lookup"><span data-stu-id="6aec3-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="6aec3-138">Получающееся количество затем предлагается как количество амортизации за период.</span><span class="sxs-lookup"><span data-stu-id="6aec3-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="6aec3-139">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6aec3-139">Example 2</span></span>

<span data-ttu-id="6aec3-140">Следующий коэффициент для амортизации потребления настроен для 31 января:</span><span class="sxs-lookup"><span data-stu-id="6aec3-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="6aec3-141">Процентное отношение равно составляет 10 процентов.</span><span class="sxs-lookup"><span data-stu-id="6aec3-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="6aec3-142">Цена за единицу измерения амортизации, указанная для основных средств, равна 1,5.</span><span class="sxs-lookup"><span data-stu-id="6aec3-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="6aec3-143">Предполагаемое количество основного средства равно 2 000.</span><span class="sxs-lookup"><span data-stu-id="6aec3-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="6aec3-144">Предложение амортизации на 31-е января выглядит следующим образом: Оцененное количество × Процент × Единица измерения амортизации 2 000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="6aec3-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



