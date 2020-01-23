---
title: Создание атрибутов партии для продукта
description: В этой процедуре показано, как создать атрибут партии, назначить диапазоны значений по умолчанию и включить атрибут в группу.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934943"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="004a1-103">Создание атрибутов партии для продукта</span><span class="sxs-lookup"><span data-stu-id="004a1-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="004a1-104">В этой процедуре показано, как создать атрибут партии, назначить диапазоны значений по умолчанию и включить атрибут в группу.</span><span class="sxs-lookup"><span data-stu-id="004a1-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="004a1-105">В качестве компании с демонстрационными данными для создания этой процедуры используется компания USP2.</span><span class="sxs-lookup"><span data-stu-id="004a1-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="004a1-106">Перейдите в раздел "Управление запасами" > "Партия" > "Атрибуты партии".</span><span class="sxs-lookup"><span data-stu-id="004a1-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="004a1-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="004a1-107">Click New.</span></span>
3. <span data-ttu-id="004a1-108">В поле "Атрибут" введите значение.</span><span class="sxs-lookup"><span data-stu-id="004a1-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="004a1-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="004a1-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="004a1-110">В поле "Тип атрибута" выберите "Дробь".</span><span class="sxs-lookup"><span data-stu-id="004a1-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="004a1-111">В этой процедуре используется тип "Дробь" для получения десятичных значений.</span><span class="sxs-lookup"><span data-stu-id="004a1-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="004a1-112">Можно выбрать другие типы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="004a1-112">You can select other attribute types.</span></span> <span data-ttu-id="004a1-113">При выборе типа "Перечисление" необходимо ввести значения в список перечисления, прежде чем можно будет ввести значение в поле "Цель".</span><span class="sxs-lookup"><span data-stu-id="004a1-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="004a1-114">В поле "Минимум" введите число.</span><span class="sxs-lookup"><span data-stu-id="004a1-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="004a1-115">В поле "Максимум" введите число.</span><span class="sxs-lookup"><span data-stu-id="004a1-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="004a1-116">В поле "Шаг" введите число.</span><span class="sxs-lookup"><span data-stu-id="004a1-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="004a1-117">В поле "Цель" введите значение.</span><span class="sxs-lookup"><span data-stu-id="004a1-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="004a1-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="004a1-118">Click Save.</span></span>
11. <span data-ttu-id="004a1-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="004a1-119">Close the page.</span></span>
12. <span data-ttu-id="004a1-120">Перейдите в раздел "Управление запасами" > "Партия" > "Группы атрибутов партии".</span><span class="sxs-lookup"><span data-stu-id="004a1-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="004a1-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="004a1-121">Click New.</span></span>
14. <span data-ttu-id="004a1-122">В поле "Группа атрибутов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="004a1-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="004a1-123">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="004a1-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="004a1-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="004a1-124">Click Save.</span></span>
17. <span data-ttu-id="004a1-125">Щелкните Сгруппировать атрибуты.</span><span class="sxs-lookup"><span data-stu-id="004a1-125">Click Group attributes.</span></span>
18. <span data-ttu-id="004a1-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="004a1-126">Click New.</span></span>
19. <span data-ttu-id="004a1-127">В поле "Атрибут" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="004a1-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="004a1-128">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="004a1-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="004a1-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="004a1-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="004a1-130">Атрибут может входить в любую из групп.</span><span class="sxs-lookup"><span data-stu-id="004a1-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="004a1-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="004a1-131">Click Save.</span></span>
23. <span data-ttu-id="004a1-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="004a1-132">Close the page.</span></span>

