---
title: Создание номенклатуры номера продукта для заранее определенных вариантов продукта
description: В этом теме показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257431"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="584ba-103">Создание номенклатуры номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="584ba-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="584ba-104">В этом теме показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="584ba-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="584ba-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="584ba-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="584ba-106">Новая номенклатура номера продукта назначается группе аналитик продукта "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="584ba-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="584ba-107">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="584ba-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="584ba-108">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="584ba-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="584ba-109">Выберите **Определение модели вариантов продукта**.</span><span class="sxs-lookup"><span data-stu-id="584ba-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="584ba-110">Выберите **Номенклатура продуктов**.</span><span class="sxs-lookup"><span data-stu-id="584ba-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="584ba-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="584ba-111">Select **New**.</span></span>
4. <span data-ttu-id="584ba-112">В поле **Имя** введите имя номенклатуры, которое помогает идентифицировать целевую группу аналитик продукта, например `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="584ba-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="584ba-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="584ba-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="584ba-114">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="584ba-114">Select **Add**.</span></span>
7. <span data-ttu-id="584ba-115">Выберите **Номер шаблона продукта**.</span><span class="sxs-lookup"><span data-stu-id="584ba-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="584ba-116">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="584ba-116">Select **Add**.</span></span>
9. <span data-ttu-id="584ba-117">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="584ba-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="584ba-118">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="584ba-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="584ba-119">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="584ba-119">Select **Add**.</span></span>
12. <span data-ttu-id="584ba-120">Выберите **Цвет**.</span><span class="sxs-lookup"><span data-stu-id="584ba-120">Select **Color**.</span></span>
13. <span data-ttu-id="584ba-121">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="584ba-121">Select **Add**.</span></span>
14. <span data-ttu-id="584ba-122">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="584ba-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="584ba-123">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="584ba-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="584ba-124">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="584ba-124">Select **Add**.</span></span>
17. <span data-ttu-id="584ba-125">Выберите **Размер**.</span><span class="sxs-lookup"><span data-stu-id="584ba-125">Select **Size**.</span></span>
18. <span data-ttu-id="584ba-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="584ba-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="584ba-127">Назначение номенклатуры шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="584ba-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="584ba-128">Выберите **Группы аналитик продукта**.</span><span class="sxs-lookup"><span data-stu-id="584ba-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="584ba-129">Выберите группу **Аналитика продукта SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="584ba-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="584ba-130">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="584ba-130">Select **Edit**.</span></span>
4. <span data-ttu-id="584ba-131">Выберите **Да** в поле **Использовать номенклатуру**.</span><span class="sxs-lookup"><span data-stu-id="584ba-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="584ba-132">В поле **Номенклатура номеров вариантов продуктов** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="584ba-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="584ba-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="584ba-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]