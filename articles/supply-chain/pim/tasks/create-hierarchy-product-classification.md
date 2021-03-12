---
title: Создание иерархии классификации продуктов
description: В этой процедуре показано, как создать новую иерархию категорий и назначить тип иерархии "товарный код".
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74be72ac5787273e13692abdb9db18be4c5ccc08
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966963"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="ddaee-103">Создание иерархии классификации продуктов</span><span class="sxs-lookup"><span data-stu-id="ddaee-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddaee-104">В этой процедуре показано, как создать новую иерархию категорий и назначить тип иерархии "товарный код".</span><span class="sxs-lookup"><span data-stu-id="ddaee-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="ddaee-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ddaee-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ddaee-106">Эта процедура предназначена для менеджера категорий.</span><span class="sxs-lookup"><span data-stu-id="ddaee-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="ddaee-107">Создание новой иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="ddaee-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="ddaee-108">Выберите **Область переходов > Модули > Управление сведениями о продукте > Настройка > Категории и атрибуты > Иерархии категорий**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="ddaee-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-109">Click **New**.</span></span>
3. <span data-ttu-id="ddaee-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="ddaee-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ddaee-112">Щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="ddaee-113">Построение иерархии</span><span class="sxs-lookup"><span data-stu-id="ddaee-113">Build the hierarchy</span></span>
1. <span data-ttu-id="ddaee-114">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="ddaee-114">Click **New** category node.</span></span>
2. <span data-ttu-id="ddaee-115">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="ddaee-116">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="ddaee-117">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="ddaee-118">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="ddaee-118">Click **New** category node.</span></span>
6. <span data-ttu-id="ddaee-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="ddaee-120">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="ddaee-121">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="ddaee-122">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="ddaee-122">Click **New** category node.</span></span>
10. <span data-ttu-id="ddaee-123">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="ddaee-124">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="ddaee-125">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="ddaee-126">Щелкните **Создать** узел категории.</span><span class="sxs-lookup"><span data-stu-id="ddaee-126">Click **New** category node.</span></span>
14. <span data-ttu-id="ddaee-127">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="ddaee-128">В поле **Код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="ddaee-129">В поле **Понятное имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ddaee-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="ddaee-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ddaee-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="ddaee-131">Классификация иерархии</span><span class="sxs-lookup"><span data-stu-id="ddaee-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="ddaee-132">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ddaee-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="ddaee-133">В области **Панель операций** щелкните **Иерархия категорий**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="ddaee-134">Щелкните **Связать тип иерархии**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="ddaee-135">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-135">Click **New**.</span></span>
5. <span data-ttu-id="ddaee-136">В поле **Тип иерархии категорий** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="ddaee-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="ddaee-137">Выберите **Тип иерархии категорий "Товарный код" для классификации продуктов**.</span><span class="sxs-lookup"><span data-stu-id="ddaee-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="ddaee-138">В поле **Иерархия категорий** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ddaee-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ddaee-139">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="ddaee-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ddaee-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ddaee-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ddaee-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ddaee-141">Close the page.</span></span>

