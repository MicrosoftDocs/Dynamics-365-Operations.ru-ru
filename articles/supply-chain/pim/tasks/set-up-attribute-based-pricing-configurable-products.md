---
title: Настройка ценообразования на основе атрибутов для настраиваемых продуктов
description: В этой теме показано, как настроить ценообразование на основе атрибутов.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f9a78902ff1a0333c46c8ad9142338678b6e7d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986787"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="1e0c2-103">Настройка ценообразования на основе атрибутов для настраиваемых продуктов</span><span class="sxs-lookup"><span data-stu-id="1e0c2-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e0c2-104">В этой теме показано, как настроить ценообразование на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="1e0c2-105">В качестве предварительного условия необходимо иметь модель конфигурации продукта, которая содержит один или несколько компонентов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="1e0c2-106">В этом примере использует модель динамика класса Hi-End в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="1e0c2-107">Обычно менеджер по продуктам использует эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="1e0c2-108">Создание новой модели цены</span><span class="sxs-lookup"><span data-stu-id="1e0c2-108">Create a new price model</span></span>
1. <span data-ttu-id="1e0c2-109">Выберите **Определение модели вариантов продукта** на домашней странице.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="1e0c2-110">Выберите **Модели конфигурации продукта** в разделе **ссылки**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="1e0c2-111">В списке выберите строку **Динамик верхнего сегмента**, но не выбирайте ссылку для имени.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="1e0c2-112">В области действий выберите **Модель**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="1e0c2-113">Выберите **Модели цены**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-113">Select **Price models**.</span></span>
6. <span data-ttu-id="1e0c2-114">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-114">Select **New**.</span></span>
7. <span data-ttu-id="1e0c2-115">В поле **Название модели цены** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="1e0c2-116">Используйте имя, по которому модель легко идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="1e0c2-117">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="1e0c2-118">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="1e0c2-119">Добавление элементов цены</span><span class="sxs-lookup"><span data-stu-id="1e0c2-119">Add price elements</span></span>
1. <span data-ttu-id="1e0c2-120">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-120">Select **Edit**.</span></span> <span data-ttu-id="1e0c2-121">Каждый из компонентов в модели продута может иметь базовый элемент цены и любое количество правил выражения цены.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="1e0c2-122">Можно также добавить цены в разных валютах.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="1e0c2-123">В поле **Выражение базовой цены** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="1e0c2-124">Например, введите "100".</span><span class="sxs-lookup"><span data-stu-id="1e0c2-124">For example, type 100.</span></span> <span data-ttu-id="1e0c2-125">Выражение базовой цены может быть численным значением или оно может состоять из арифметического расчета, включающего один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="1e0c2-126">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-126">Select **Add**.</span></span>
4. <span data-ttu-id="1e0c2-127">В поле **Имя** введите `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="1e0c2-128">Имя выражения цены помогает понять, что представляет элемент цены.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="1e0c2-129">В этом примере нам создаем элемент цены для варианта "Отделка корпуса динамика из палисандра".</span><span class="sxs-lookup"><span data-stu-id="1e0c2-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="1e0c2-130">Выберите **Изменить условие**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-130">Select **Edit condition**.</span></span> <span data-ttu-id="1e0c2-131">Условие цены помогает гарантировать, что элемент выражения цены включается в цену продажи только в том случае, если имеется определенное сочетание атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="1e0c2-132">В поле **ConstraintBody** введите `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="1e0c2-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-133">Select **OK**.</span></span>
8. <span data-ttu-id="1e0c2-134">В поле **Выражение** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="1e0c2-135">Например, введите `50`.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="1e0c2-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e0c2-136">Close the page.</span></span>

