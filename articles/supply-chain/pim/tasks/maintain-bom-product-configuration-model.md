---
title: Ведение спецификации для модели конфигурации продукта
description: Выполнение этой процедуры требует существующей модели конфигурации продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12eb2d8fcdae5d60efa19e5443a01ab9bd104267
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258811"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="64952-103">Ведение спецификации для модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="64952-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64952-104">Выполнение этой процедуры требует существующей модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="64952-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="64952-105">Модель динамика класса Hi-End в демонстрационной компании USMF используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="64952-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="64952-106">Добавление строки спецификации</span><span class="sxs-lookup"><span data-stu-id="64952-106">Add a BOM line</span></span>
1. <span data-ttu-id="64952-107">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="64952-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="64952-108">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="64952-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="64952-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="64952-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="64952-110">Выберите динамик класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="64952-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="64952-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="64952-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="64952-112">Развернуть раздел "Строки спецификации".</span><span class="sxs-lookup"><span data-stu-id="64952-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="64952-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="64952-113">Click Add.</span></span>
7. <span data-ttu-id="64952-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64952-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="64952-115">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="64952-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="64952-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="64952-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="64952-117">Добавление сведений о строке спецификации</span><span class="sxs-lookup"><span data-stu-id="64952-117">Add BOM line details</span></span>
1. <span data-ttu-id="64952-118">Щелкните "Сведения о строке спецификации".</span><span class="sxs-lookup"><span data-stu-id="64952-118">Click BOM line details.</span></span>
2. <span data-ttu-id="64952-119">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="64952-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="64952-120">Например, можно выбрать номенклатуру M0055.</span><span class="sxs-lookup"><span data-stu-id="64952-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="64952-121">Для каждого свойства строки спецификации можно выбрать, имеет ли оно фиксированное значение или сопоставляется с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="64952-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="64952-122">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="64952-122">Select the Set check box.</span></span>
4. <span data-ttu-id="64952-123">Выберите значение "Да" в поле "Расчет".</span><span class="sxs-lookup"><span data-stu-id="64952-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="64952-124">Настройка свойства расчета как "Да" гарантирует, что строка спецификации включается в расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="64952-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="64952-125">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="64952-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="64952-126">Установите флажок "Задать".</span><span class="sxs-lookup"><span data-stu-id="64952-126">Select the Set check box.</span></span>
7. <span data-ttu-id="64952-127">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="64952-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="64952-128">Поле количества определяет количество номенклатуры, которое будет включено в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="64952-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="64952-129">Это могло быть очевидным кандидатом для сопоставления атрибута.</span><span class="sxs-lookup"><span data-stu-id="64952-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="64952-130">Щелкните вкладку "Аналитика".</span><span class="sxs-lookup"><span data-stu-id="64952-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="64952-131">Проверьте наличие активных аналитик продукта, и поэтому необходимо назначить значение или атрибут.</span><span class="sxs-lookup"><span data-stu-id="64952-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="64952-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="64952-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]