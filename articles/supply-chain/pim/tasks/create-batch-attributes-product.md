--- 
title: "Создание атрибутов партии для продукта"
description: "В этой процедуре показано, как создать атрибут партии, назначить диапазоны значений по умолчанию и включить атрибут в группу."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 65153dbcfa69046e4f38eb6ffa013bb6fb87ebd8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="6568a-103">Создание атрибутов партии для продукта</span><span class="sxs-lookup"><span data-stu-id="6568a-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6568a-104">В этой процедуре показано, как создать атрибут партии, назначить диапазоны значений по умолчанию и включить атрибут в группу.</span><span class="sxs-lookup"><span data-stu-id="6568a-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="6568a-105">В качестве компании с демонстрационными данными для создания этой процедуры используется компания USP2.</span><span class="sxs-lookup"><span data-stu-id="6568a-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="6568a-106">Перейдите в раздел "Управление запасами" > "Партия" > "Атрибуты партии".</span><span class="sxs-lookup"><span data-stu-id="6568a-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="6568a-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6568a-107">Click New.</span></span>
3. <span data-ttu-id="6568a-108">В поле "Атрибут" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6568a-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="6568a-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6568a-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6568a-110">В поле "Тип атрибута" выберите "Дробь".</span><span class="sxs-lookup"><span data-stu-id="6568a-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="6568a-111">В этой процедуре используется тип "Дробь" для получения десятичных значений.</span><span class="sxs-lookup"><span data-stu-id="6568a-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="6568a-112">Можно выбрать другие типы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6568a-112">You can select other attribute types.</span></span> <span data-ttu-id="6568a-113">При выборе типа "Перечисление" необходимо ввести значения в список перечисления, прежде чем можно будет ввести значение в поле "Цель".</span><span class="sxs-lookup"><span data-stu-id="6568a-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="6568a-114">В поле "Минимум" введите число.</span><span class="sxs-lookup"><span data-stu-id="6568a-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="6568a-115">В поле "Максимум" введите число.</span><span class="sxs-lookup"><span data-stu-id="6568a-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="6568a-116">В поле "Шаг" введите число.</span><span class="sxs-lookup"><span data-stu-id="6568a-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="6568a-117">В поле "Цель" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6568a-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="6568a-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6568a-118">Click Save.</span></span>
11. <span data-ttu-id="6568a-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6568a-119">Close the page.</span></span>
12. <span data-ttu-id="6568a-120">Перейдите в раздел "Управление запасами" > "Партия" > "Группы атрибутов партии".</span><span class="sxs-lookup"><span data-stu-id="6568a-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="6568a-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6568a-121">Click New.</span></span>
14. <span data-ttu-id="6568a-122">В поле "Группа атрибутов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6568a-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="6568a-123">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6568a-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6568a-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6568a-124">Click Save.</span></span>
17. <span data-ttu-id="6568a-125">Щелкните Сгруппировать атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6568a-125">Click Group attributes.</span></span>
18. <span data-ttu-id="6568a-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6568a-126">Click New.</span></span>
19. <span data-ttu-id="6568a-127">В поле "Атрибут" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6568a-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6568a-128">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6568a-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6568a-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6568a-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6568a-130">Атрибут может входить в любую из групп.</span><span class="sxs-lookup"><span data-stu-id="6568a-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="6568a-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6568a-131">Click Save.</span></span>
23. <span data-ttu-id="6568a-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6568a-132">Close the page.</span></span>


