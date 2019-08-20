---
title: Ведение спецификации для модели конфигурации продукта
description: Выполнение этой процедуры требует существующей модели конфигурации продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f663c28dfcbf6b365e3e88d3a4f6385ce2fcca9f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844401"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="3c95a-103">Ведение спецификации для модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="3c95a-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c95a-104">Выполнение этой процедуры требует существующей модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="3c95a-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="3c95a-105">Модель динамика класса Hi-End в демонстрационной компании USMF используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="3c95a-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="3c95a-106">Добавление строки спецификации</span><span class="sxs-lookup"><span data-stu-id="3c95a-106">Add a BOM line</span></span>
1. <span data-ttu-id="3c95a-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="3c95a-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3c95a-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="3c95a-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="3c95a-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3c95a-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3c95a-110">Выберите динамик класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="3c95a-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="3c95a-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3c95a-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3c95a-112">Развернуть раздел "Строки спецификации".</span><span class="sxs-lookup"><span data-stu-id="3c95a-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="3c95a-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="3c95a-113">Click Add.</span></span>
7. <span data-ttu-id="3c95a-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3c95a-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="3c95a-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3c95a-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="3c95a-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3c95a-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="3c95a-117">Добавление сведений о строке спецификации</span><span class="sxs-lookup"><span data-stu-id="3c95a-117">Add BOM line details</span></span>
1. <span data-ttu-id="3c95a-118">Щелкните "Сведения о строке спецификации".</span><span class="sxs-lookup"><span data-stu-id="3c95a-118">Click BOM line details.</span></span>
2. <span data-ttu-id="3c95a-119">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3c95a-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="3c95a-120">Например, можно выбрать номенклатуру M0055.</span><span class="sxs-lookup"><span data-stu-id="3c95a-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="3c95a-121">Для каждого свойства строки спецификации можно выбрать, имеет ли оно фиксированное значение или сопоставляется с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="3c95a-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="3c95a-122">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="3c95a-122">Select the Set check box.</span></span>
4. <span data-ttu-id="3c95a-123">Выберите значение "Да" в поле "Расчет".</span><span class="sxs-lookup"><span data-stu-id="3c95a-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="3c95a-124">Настройка свойства расчета как "Да" гарантирует, что строка спецификации включается в расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="3c95a-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="3c95a-125">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="3c95a-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="3c95a-126">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="3c95a-126">Select the Set check box.</span></span>
7. <span data-ttu-id="3c95a-127">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="3c95a-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3c95a-128">Поле количества определяет количество номенклатуры, которое будет включено в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="3c95a-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="3c95a-129">Это могло быть очевидным кандидатом для сопоставления атрибута.</span><span class="sxs-lookup"><span data-stu-id="3c95a-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="3c95a-130">Щелкните вкладку "Аналитика".</span><span class="sxs-lookup"><span data-stu-id="3c95a-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="3c95a-131">Проверьте наличие активных аналитик продукта, и поэтому необходимо назначить значение или атрибут.</span><span class="sxs-lookup"><span data-stu-id="3c95a-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="3c95a-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3c95a-132">Click OK.</span></span>

