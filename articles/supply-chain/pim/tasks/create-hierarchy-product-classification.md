---
title: Создание иерархии классификации продуктов
description: В этой процедуре показано, как создать новую иерархию категорий и назначить тип иерархии "товарный код".
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ac87356f46edc118a592acd393823603815917a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150128"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="4ca13-103">Создание иерархии классификации продуктов</span><span class="sxs-lookup"><span data-stu-id="4ca13-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ca13-104">В этой процедуре показано, как создать новую иерархию категорий и назначить тип иерархии "товарный код".</span><span class="sxs-lookup"><span data-stu-id="4ca13-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="4ca13-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="4ca13-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4ca13-106">Эта процедура предназначена для менеджера категорий.</span><span class="sxs-lookup"><span data-stu-id="4ca13-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="4ca13-107">Создание новой иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="4ca13-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="4ca13-108">Выберите **Область переходов > Модули > Управление сведениями о продукте > Настройка > Категории и атрибуты > Иерархии категорий**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="4ca13-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-109">Click **New**.</span></span>
3. <span data-ttu-id="4ca13-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="4ca13-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4ca13-112">Щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="4ca13-113">Построение иерархии</span><span class="sxs-lookup"><span data-stu-id="4ca13-113">Build the hierarchy</span></span>
1. <span data-ttu-id="4ca13-114">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="4ca13-114">Click **New** category node.</span></span>
2. <span data-ttu-id="4ca13-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="4ca13-116">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="4ca13-117">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="4ca13-118">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="4ca13-118">Click **New** category node.</span></span>
6. <span data-ttu-id="4ca13-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="4ca13-120">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="4ca13-121">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="4ca13-122">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="4ca13-122">Click **New** category node.</span></span>
10. <span data-ttu-id="4ca13-123">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="4ca13-124">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="4ca13-125">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="4ca13-126">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="4ca13-126">Click **New** category node.</span></span>
14. <span data-ttu-id="4ca13-127">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="4ca13-128">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="4ca13-129">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="4ca13-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="4ca13-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4ca13-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="4ca13-131">Классификация иерархии</span><span class="sxs-lookup"><span data-stu-id="4ca13-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="4ca13-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4ca13-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="4ca13-133">В области **Панель операций** щелкните **Иерархия категорий**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="4ca13-134">Щелкните **Связать тип иерархии**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="4ca13-135">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-135">Click **New**.</span></span>
5. <span data-ttu-id="4ca13-136">В поле **Тип иерархии категорий** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="4ca13-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="4ca13-137">Выберите **Тип иерархии категорий "Товарный код" для классификации продуктов**.</span><span class="sxs-lookup"><span data-stu-id="4ca13-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="4ca13-138">В поле **Иерархия категорий** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="4ca13-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4ca13-139">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="4ca13-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4ca13-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4ca13-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4ca13-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4ca13-141">Close the page.</span></span>

