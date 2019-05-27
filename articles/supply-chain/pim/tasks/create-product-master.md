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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e34f7c630e872468d888938e0f1aa57f3f0d4c4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570014"
---
# <a name="create-a-product-master"></a><span data-ttu-id="30656-103">Создание шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="30656-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30656-104">Создайте шаблон продукта для предопределенных вариантов.</span><span class="sxs-lookup"><span data-stu-id="30656-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="30656-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="30656-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="30656-106">Эта процедура предназначена для конструктора продуктов.</span><span class="sxs-lookup"><span data-stu-id="30656-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="30656-107">Создание нового шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="30656-107">Create a new product master</span></span>
1. <span data-ttu-id="30656-108">Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="30656-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="30656-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30656-109">Click New.</span></span>
3. <span data-ttu-id="30656-110">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="30656-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="30656-111">Номер должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="30656-111">The number must be unique.</span></span> <span data-ttu-id="30656-112">Для поля "Номер продукта" можно задать номерную серию.</span><span class="sxs-lookup"><span data-stu-id="30656-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="30656-113">В этом случае пользователю необязательно вводить значение.</span><span class="sxs-lookup"><span data-stu-id="30656-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="30656-114">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="30656-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="30656-115">Введите описательное наименование продукта.</span><span class="sxs-lookup"><span data-stu-id="30656-115">Enter a descriptive product name.</span></span> <span data-ttu-id="30656-116">По умолчанию это значение совпадает с кратким наименованием, однако пользователь может его изменить.</span><span class="sxs-lookup"><span data-stu-id="30656-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="30656-117">В поле "Группа аналитик продуктов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="30656-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="30656-118">Группа аналитик продукта определяет, какую из четырех аналитик продукта можно использовать для создания вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="30656-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="30656-119">В этом примере используется группа с цветом и размером.</span><span class="sxs-lookup"><span data-stu-id="30656-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="30656-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30656-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="30656-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30656-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="30656-122">Технология конфигурации по умолчанию — "Предопределенный вариант".</span><span class="sxs-lookup"><span data-stu-id="30656-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="30656-123">Она и будет использоваться в этом примере.</span><span class="sxs-lookup"><span data-stu-id="30656-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="30656-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30656-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="30656-125">Выбор групп аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="30656-125">Select product dimension groups</span></span>
1. <span data-ttu-id="30656-126">В поле "Группа цветов" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="30656-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="30656-127">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="30656-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="30656-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30656-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="30656-129">В поле "Группа размеров" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="30656-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="30656-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30656-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="30656-131">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30656-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="30656-132">Добавление групп аналитики</span><span class="sxs-lookup"><span data-stu-id="30656-132">Add dimension groups</span></span>
1. <span data-ttu-id="30656-133">В области действий щелкните "Продукт".</span><span class="sxs-lookup"><span data-stu-id="30656-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="30656-134">Щелкните "Группы аналитики", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30656-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="30656-135">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="30656-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="30656-136">С помощью аналитик хранения можно управлять хранением и извлечением номенклатур из запасов.</span><span class="sxs-lookup"><span data-stu-id="30656-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="30656-137">Например, аналитика хранения может включать параметры "Сайт" и "Склад".</span><span class="sxs-lookup"><span data-stu-id="30656-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="30656-138">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30656-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="30656-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30656-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="30656-140">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="30656-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="30656-141">Группа аналитик отслеживания определяет, какие аналитики отслеживания можно добавить к продукту.</span><span class="sxs-lookup"><span data-stu-id="30656-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="30656-142">Например, номер партии и серийный номер используются для отслеживания складских номенклатур.</span><span class="sxs-lookup"><span data-stu-id="30656-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="30656-143">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30656-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="30656-144">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30656-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="30656-145">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="30656-145">Click OK.</span></span>
10. <span data-ttu-id="30656-146">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="30656-146">Click Save.</span></span>
11. <span data-ttu-id="30656-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="30656-147">Close the page.</span></span>

