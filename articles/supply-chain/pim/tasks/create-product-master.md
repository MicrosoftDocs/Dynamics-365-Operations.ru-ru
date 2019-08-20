---
title: Создание шаблона продукта
description: Создайте шаблон продукта для предопределенных вариантов.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21cfc2699fdcd6024286ee16bb60c3cd6dda5b67
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844725"
---
# <a name="create-a-product-master"></a><span data-ttu-id="3f423-103">Создание шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="3f423-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f423-104">Создайте шаблон продукта для предопределенных вариантов.</span><span class="sxs-lookup"><span data-stu-id="3f423-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="3f423-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="3f423-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3f423-106">Эта процедура предназначена для конструктора продуктов.</span><span class="sxs-lookup"><span data-stu-id="3f423-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="3f423-107">Создание нового шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="3f423-107">Create a new product master</span></span>
1. <span data-ttu-id="3f423-108">Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="3f423-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="3f423-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3f423-109">Click New.</span></span>
3. <span data-ttu-id="3f423-110">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3f423-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="3f423-111">Номер должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="3f423-111">The number must be unique.</span></span> <span data-ttu-id="3f423-112">Для поля "Номер продукта" можно задать номерную серию.</span><span class="sxs-lookup"><span data-stu-id="3f423-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="3f423-113">В этом случае пользователю необязательно вводить значение.</span><span class="sxs-lookup"><span data-stu-id="3f423-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="3f423-114">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3f423-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="3f423-115">Введите описательное наименование продукта.</span><span class="sxs-lookup"><span data-stu-id="3f423-115">Enter a descriptive product name.</span></span> <span data-ttu-id="3f423-116">По умолчанию это значение совпадает с кратким наименованием, однако пользователь может его изменить.</span><span class="sxs-lookup"><span data-stu-id="3f423-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="3f423-117">В поле "Группа аналитик продуктов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3f423-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3f423-118">Группа аналитик продукта определяет, какую из четырех аналитик продукта можно использовать для создания вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="3f423-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="3f423-119">В этом примере используется группа с цветом и размером.</span><span class="sxs-lookup"><span data-stu-id="3f423-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="3f423-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3f423-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3f423-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3f423-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f423-122">Технология конфигурации по умолчанию — "Предопределенный вариант".</span><span class="sxs-lookup"><span data-stu-id="3f423-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="3f423-123">Она и будет использоваться в этом примере.</span><span class="sxs-lookup"><span data-stu-id="3f423-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="3f423-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3f423-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="3f423-125">Выбор групп аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="3f423-125">Select product dimension groups</span></span>
1. <span data-ttu-id="3f423-126">В поле "Группа цветов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3f423-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3f423-127">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="3f423-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3f423-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3f423-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3f423-129">В поле "Группа размеров" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3f423-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3f423-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3f423-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="3f423-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3f423-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="3f423-132">Добавление групп аналитики</span><span class="sxs-lookup"><span data-stu-id="3f423-132">Add dimension groups</span></span>
1. <span data-ttu-id="3f423-133">В области действий щелкните "Продукт".</span><span class="sxs-lookup"><span data-stu-id="3f423-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="3f423-134">Щелкните "Группы аналитики", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3f423-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="3f423-135">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3f423-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3f423-136">С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов.</span><span class="sxs-lookup"><span data-stu-id="3f423-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="3f423-137">Например, аналитика хранения может включать параметры "Сайт" и "Склад".</span><span class="sxs-lookup"><span data-stu-id="3f423-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="3f423-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3f423-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3f423-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3f423-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3f423-140">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3f423-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3f423-141">Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту.</span><span class="sxs-lookup"><span data-stu-id="3f423-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="3f423-142">Например, номер партии и серийный номер используются для отслеживания складских номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3f423-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="3f423-143">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3f423-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3f423-144">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3f423-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3f423-145">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="3f423-145">Click OK.</span></span>
10. <span data-ttu-id="3f423-146">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3f423-146">Click Save.</span></span>
11. <span data-ttu-id="3f423-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3f423-147">Close the page.</span></span>

