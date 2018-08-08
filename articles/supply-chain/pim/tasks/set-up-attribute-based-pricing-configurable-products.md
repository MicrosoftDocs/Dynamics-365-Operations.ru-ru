--- 
title: "Настройка ценообразования на основе атрибутов для настраиваемых продуктов"
description: "В этой процедуре показано, как настроить ценообразование на основе атрибутов."
author: ShylaThompson
manager: AnnBe
ms.date: 10/12/2016
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
ms.openlocfilehash: f1eaa53a652a59d4d970781f734e1332aa762ca2
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="a7e8f-103">Настройка ценообразования на основе атрибутов для настраиваемых продуктов</span><span class="sxs-lookup"><span data-stu-id="a7e8f-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7e8f-104">В этой процедуре показано, как настроить ценообразование на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="a7e8f-105">В качестве предварительного условия необходимо иметь модель конфигурации продукта, которая содержит один или несколько компонентов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="a7e8f-106">В этом примере использует модель динамика класса Hi-End в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="a7e8f-107">Обычно менеджер по продуктам использует эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="a7e8f-108">Создание новой модели цены</span><span class="sxs-lookup"><span data-stu-id="a7e8f-108">Create a new price model</span></span>
1. <span data-ttu-id="a7e8f-109">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a7e8f-110">Щелкните "Модели конфигурации продукта".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="a7e8f-111">В списке выберите строку динамика верхнего сегмента, но не нажимайте ссылку для имени.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="a7e8f-112">В области действий щелкните "Модель".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="a7e8f-113">Щелкните "Модели цены".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-113">Click Price models.</span></span>
6. <span data-ttu-id="a7e8f-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-114">Click New.</span></span>
7. <span data-ttu-id="a7e8f-115">В поле "Название модели цены" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="a7e8f-116">Используйте имя, по которому модель легко идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="a7e8f-117">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a7e8f-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="a7e8f-119">Добавление элементов цены</span><span class="sxs-lookup"><span data-stu-id="a7e8f-119">Add price elements</span></span>
1. <span data-ttu-id="a7e8f-120">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-120">Click Edit.</span></span>
    * <span data-ttu-id="a7e8f-121">Каждый из компонентов в модели продута может иметь базовый элемент цены и любое количество правил выражения цены.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="a7e8f-122">Можно также добавить цены в разных валютах.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="a7e8f-123">В поле "Выражение базовой цены" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="a7e8f-124">Например, введите "100".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-124">For example, type 100.</span></span>   <span data-ttu-id="a7e8f-125">Выражение базовой цены может быть численным значением или оно может состоять из арифметического расчета, включающего один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="a7e8f-126">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-126">Click Add.</span></span>
4. <span data-ttu-id="a7e8f-127">В поле "Имя" введите "Палисандр".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="a7e8f-128">Имя выражения цены помогает понять, что представляет элемент цены.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="a7e8f-129">В этом примере нам создаем элемент цены для варианта "Отделка корпуса динамика из палисандра".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="a7e8f-130">Щелкните "Изменить условие".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-130">Click Edit condition.</span></span>
    * <span data-ttu-id="a7e8f-131">Условие цены помогает гарантировать, что элемент выражения цены включается в цену продажи только в том случае, если имеется определенное сочетание атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="a7e8f-132">В поле "ConstraintBody" введите "CabinetFinish=="Rosewood"".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="a7e8f-133">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-133">Click OK.</span></span>
8. <span data-ttu-id="a7e8f-134">В поле "Выражение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="a7e8f-135">Например, введите "50".</span><span class="sxs-lookup"><span data-stu-id="a7e8f-135">For example, type 50.</span></span>  
9. <span data-ttu-id="a7e8f-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-136">Close the page.</span></span>
10. <span data-ttu-id="a7e8f-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a7e8f-137">Close the page.</span></span>


