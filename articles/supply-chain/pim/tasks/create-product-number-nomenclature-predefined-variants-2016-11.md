---
title: Создание номенклатуры номера продукта для заранее определенных вариантов продукта
description: В этом теме показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920665"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="e0f6c-103">Создание номенклатуры номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="e0f6c-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0f6c-104">В этом теме показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="e0f6c-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0f6c-106">Новая номенклатура номера продукта назначается группе аналитик продукта "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="e0f6c-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="e0f6c-107">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="e0f6c-108">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="e0f6c-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="e0f6c-109">Перейдите в раздел **Управление сведениями о продукте \> Настройка \> Номенклатура продукта**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="e0f6c-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-110">Select **New**.</span></span>
1. <span data-ttu-id="e0f6c-111">В поле **Имя** введите имя номенклатуры, которое помогает идентифицировать целевую группу аналитик продукта, например `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="e0f6c-112">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="e0f6c-113">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-113">Select **Add**.</span></span>
1. <span data-ttu-id="e0f6c-114">Выберите **Номер шаблона продукта**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="e0f6c-115">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-115">Select **Add**.</span></span>
1. <span data-ttu-id="e0f6c-116">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="e0f6c-117">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="e0f6c-118">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-118">Select **Add**.</span></span>
1. <span data-ttu-id="e0f6c-119">Выберите **Цвет**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-119">Select **Color**.</span></span>
1. <span data-ttu-id="e0f6c-120">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-120">Select **Add**.</span></span>
1. <span data-ttu-id="e0f6c-121">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="e0f6c-122">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="e0f6c-123">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-123">Select **Add**.</span></span>
1. <span data-ttu-id="e0f6c-124">Выберите **Размер**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-124">Select **Size**.</span></span>
1. <span data-ttu-id="e0f6c-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="e0f6c-126">Назначение номенклатуры шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="e0f6c-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="e0f6c-127">Выберите **Группы аналитик продукта**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="e0f6c-128">Выберите группу **Аналитика продукта SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="e0f6c-129">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-129">Select **Edit**.</span></span>
4. <span data-ttu-id="e0f6c-130">Выберите **Да** в поле **Использовать номенклатуру**.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="e0f6c-131">В поле **Номенклатура номеров вариантов продуктов** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="e0f6c-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e0f6c-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]