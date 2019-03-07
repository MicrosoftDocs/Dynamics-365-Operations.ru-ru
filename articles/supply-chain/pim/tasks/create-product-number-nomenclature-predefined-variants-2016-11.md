---
title: Создание номенклатуры номера продукта для заранее определенных вариантов продукта
description: На этом руководстве показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "364887"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="e5889-103">Создание номенклатуры номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="e5889-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5889-104">На этом руководстве показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="e5889-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="e5889-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e5889-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e5889-106">Новая номенклатура номера продукта назначается группе аналитик продукта "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="e5889-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="e5889-107">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="e5889-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="e5889-108">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="e5889-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="e5889-109">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="e5889-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e5889-110">Щелкните "Номенклатура продуктов".</span><span class="sxs-lookup"><span data-stu-id="e5889-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="e5889-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e5889-111">Click New.</span></span>
4. <span data-ttu-id="e5889-112">В поле "Имя" введите имя номенклатуры, которое помогает идентифицировать целевую группу аналитик продукта, например ColorSize.</span><span class="sxs-lookup"><span data-stu-id="e5889-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="e5889-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e5889-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e5889-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5889-114">Click Add.</span></span>
7. <span data-ttu-id="e5889-115">Щелкните "Номер шаблона продукта".</span><span class="sxs-lookup"><span data-stu-id="e5889-115">Click Product master number.</span></span>
8. <span data-ttu-id="e5889-116">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5889-116">Click Add.</span></span>
9. <span data-ttu-id="e5889-117">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="e5889-117">Click Text constant.</span></span>
10. <span data-ttu-id="e5889-118">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e5889-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="e5889-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5889-119">Click Add.</span></span>
12. <span data-ttu-id="e5889-120">Щелкните "Цвет".</span><span class="sxs-lookup"><span data-stu-id="e5889-120">Click Color.</span></span>
13. <span data-ttu-id="e5889-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5889-121">Click Add.</span></span>
14. <span data-ttu-id="e5889-122">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="e5889-122">Click Text constant.</span></span>
15. <span data-ttu-id="e5889-123">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e5889-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="e5889-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e5889-124">Click Add.</span></span>
17. <span data-ttu-id="e5889-125">Щелкните "Размер".</span><span class="sxs-lookup"><span data-stu-id="e5889-125">Click Size.</span></span>
18. <span data-ttu-id="e5889-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5889-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="e5889-127">Назначение номенклатуры шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="e5889-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="e5889-128">Щелкните "Группы аналитик продукта".</span><span class="sxs-lookup"><span data-stu-id="e5889-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="e5889-129">Выберите группу аналитик продукта SizeCol.</span><span class="sxs-lookup"><span data-stu-id="e5889-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="e5889-130">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="e5889-130">Click Edit.</span></span>
4. <span data-ttu-id="e5889-131">Выберите "Да" в поле "Использовать номенклатуру".</span><span class="sxs-lookup"><span data-stu-id="e5889-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="e5889-132">В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e5889-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="e5889-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e5889-133">Close the page.</span></span>

