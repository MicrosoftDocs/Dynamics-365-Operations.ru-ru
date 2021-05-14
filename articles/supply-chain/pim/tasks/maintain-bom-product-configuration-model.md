---
title: Ведение спецификации для модели конфигурации продукта
description: Выполнение этой процедуры требует существующей модели конфигурации продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921325"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="56454-103">Ведение спецификации для модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="56454-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56454-104">Выполнение этой процедуры требует существующей модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="56454-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="56454-105">Модель динамика класса Hi-End в демонстрационной компании USMF используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="56454-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="56454-106">Добавление строки спецификации</span><span class="sxs-lookup"><span data-stu-id="56454-106">Add a BOM line</span></span>

1. <span data-ttu-id="56454-107">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="56454-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="56454-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="56454-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56454-109">Выберите динамик класса Hi--End для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="56454-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="56454-110">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="56454-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="56454-111">Разверните раздел **Строки спецификации**.</span><span class="sxs-lookup"><span data-stu-id="56454-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="56454-112">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="56454-112">Select **Add**.</span></span>
1. <span data-ttu-id="56454-113">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="56454-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="56454-114">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="56454-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="56454-115">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="56454-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="56454-116">Добавление сведений о строке спецификации</span><span class="sxs-lookup"><span data-stu-id="56454-116">Add BOM line details</span></span>

1. <span data-ttu-id="56454-117">Выберите **Сведения о строке спецификации**.</span><span class="sxs-lookup"><span data-stu-id="56454-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="56454-118">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="56454-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="56454-119">Например, можно выбрать номенклатуру M0055.</span><span class="sxs-lookup"><span data-stu-id="56454-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="56454-120">Для каждого свойства строки спецификации можно выбрать, имеет ли оно фиксированное значение или сопоставляется с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="56454-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="56454-121">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="56454-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="56454-122">Выберите значение *Да* в поле **Расчет**.</span><span class="sxs-lookup"><span data-stu-id="56454-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="56454-123">Настройка свойства **Расчет** как *Да* гарантирует, что строка спецификации включается в расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="56454-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="56454-124">Выберите вкладку **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="56454-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="56454-125">Установите флажок **Задать**.</span><span class="sxs-lookup"><span data-stu-id="56454-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="56454-126">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="56454-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="56454-127">Поле количества определяет количество номенклатуры, которое будет включено в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="56454-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="56454-128">Это могло быть очевидным кандидатом для сопоставления атрибута.</span><span class="sxs-lookup"><span data-stu-id="56454-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="56454-129">Выберите вкладку **Аналитика**.</span><span class="sxs-lookup"><span data-stu-id="56454-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="56454-130">Проверьте наличие активных аналитик продукта, и поэтому необходимо назначить значение или атрибут.</span><span class="sxs-lookup"><span data-stu-id="56454-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="56454-131">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="56454-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]