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
ms.openlocfilehash: 3a15d1f4ecbf85e22bfadc1dd680d24bc56d807f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007549"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="51925-103">Создание номенклатуры номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="51925-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51925-104">В этом теме показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="51925-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="51925-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="51925-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="51925-106">Новая номенклатура номера продукта назначается группе аналитик продукта "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="51925-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="51925-107">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="51925-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="51925-108">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="51925-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="51925-109">Выберите **Определение модели вариантов продукта**.</span><span class="sxs-lookup"><span data-stu-id="51925-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="51925-110">Выберите **Номенклатура продуктов**.</span><span class="sxs-lookup"><span data-stu-id="51925-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="51925-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="51925-111">Select **New**.</span></span>
4. <span data-ttu-id="51925-112">В поле **Имя** введите имя номенклатуры, которое помогает идентифицировать целевую группу аналитик продукта, например `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="51925-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="51925-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51925-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="51925-114">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="51925-114">Select **Add**.</span></span>
7. <span data-ttu-id="51925-115">Выберите **Номер шаблона продукта**.</span><span class="sxs-lookup"><span data-stu-id="51925-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="51925-116">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="51925-116">Select **Add**.</span></span>
9. <span data-ttu-id="51925-117">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="51925-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="51925-118">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51925-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="51925-119">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="51925-119">Select **Add**.</span></span>
12. <span data-ttu-id="51925-120">Выберите **Цвет**.</span><span class="sxs-lookup"><span data-stu-id="51925-120">Select **Color**.</span></span>
13. <span data-ttu-id="51925-121">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="51925-121">Select **Add**.</span></span>
14. <span data-ttu-id="51925-122">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="51925-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="51925-123">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="51925-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="51925-124">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="51925-124">Select **Add**.</span></span>
17. <span data-ttu-id="51925-125">Выберите **Размер**.</span><span class="sxs-lookup"><span data-stu-id="51925-125">Select **Size**.</span></span>
18. <span data-ttu-id="51925-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="51925-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="51925-127">Назначение номенклатуры шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="51925-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="51925-128">Выберите **Группы аналитик продукта**.</span><span class="sxs-lookup"><span data-stu-id="51925-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="51925-129">Выберите группу **Аналитика продукта SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="51925-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="51925-130">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="51925-130">Select **Edit**.</span></span>
4. <span data-ttu-id="51925-131">Выберите **Да** в поле **Использовать номенклатуру**.</span><span class="sxs-lookup"><span data-stu-id="51925-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="51925-132">В поле **Номенклатура номеров вариантов продуктов** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="51925-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="51925-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="51925-133">Close the page.</span></span>

