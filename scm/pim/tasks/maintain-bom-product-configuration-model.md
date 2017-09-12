--- 
title: "Ведение спецификации для модели конфигурации продукта"
description: "Выполнение этой процедуры требует существующей модели конфигурации продукта."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 380e902f9c8266f583e44fa7ea643dc5d5ab52d3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="db190-103">Ведение спецификации для модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="db190-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db190-104">Выполнение этой процедуры требует существующей модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="db190-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="db190-105">Модель динамика класса Hi-End в демонстрационной компании USMF используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="db190-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="db190-106">Добавление строки спецификации</span><span class="sxs-lookup"><span data-stu-id="db190-106">Add a BOM line</span></span>
1. <span data-ttu-id="db190-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="db190-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="db190-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="db190-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="db190-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="db190-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="db190-110">Выберите динамик класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="db190-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="db190-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="db190-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="db190-112">Развернуть раздел "Строки спецификации".</span><span class="sxs-lookup"><span data-stu-id="db190-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="db190-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="db190-113">Click Add.</span></span>
7. <span data-ttu-id="db190-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="db190-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="db190-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="db190-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="db190-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="db190-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="db190-117">Добавление сведений о строке спецификации</span><span class="sxs-lookup"><span data-stu-id="db190-117">Add BOM line details</span></span>
1. <span data-ttu-id="db190-118">Щелкните "Сведения о строке спецификации".</span><span class="sxs-lookup"><span data-stu-id="db190-118">Click BOM line details.</span></span>
2. <span data-ttu-id="db190-119">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="db190-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="db190-120">Например, можно выбрать номенклатуру M0055.</span><span class="sxs-lookup"><span data-stu-id="db190-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="db190-121">Для каждого свойства строки спецификации можно выбрать, имеет ли оно фиксированное значение или сопоставляется с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="db190-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="db190-122">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="db190-122">Select the Set check box.</span></span>
4. <span data-ttu-id="db190-123">Выберите значение "Да" в поле "Расчет".</span><span class="sxs-lookup"><span data-stu-id="db190-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="db190-124">Настройка свойства расчета как "Да" гарантирует, что строка спецификации включается в расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="db190-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="db190-125">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="db190-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="db190-126">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="db190-126">Select the Set check box.</span></span>
7. <span data-ttu-id="db190-127">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="db190-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="db190-128">Поле количества определяет количество номенклатуры, которое будет включено в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="db190-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="db190-129">Это могло быть очевидным кандидатом для сопоставления атрибута.</span><span class="sxs-lookup"><span data-stu-id="db190-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="db190-130">Щелкните вкладку "Аналитика".</span><span class="sxs-lookup"><span data-stu-id="db190-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="db190-131">Проверьте наличие активных аналитик продукта, и поэтому необходимо назначить значение или атрибут.</span><span class="sxs-lookup"><span data-stu-id="db190-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="db190-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="db190-132">Click OK.</span></span>


