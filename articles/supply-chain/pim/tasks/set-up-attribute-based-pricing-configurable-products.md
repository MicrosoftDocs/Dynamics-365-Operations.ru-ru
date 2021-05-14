---
title: Настройка ценообразования на основе атрибутов для настраиваемых продуктов
description: В этой теме показано, как настроить ценообразование на основе атрибутов.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921249"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="b3213-103">Настройка ценообразования на основе атрибутов для настраиваемых продуктов</span><span class="sxs-lookup"><span data-stu-id="b3213-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3213-104">В этой теме показано, как настроить ценообразование на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3213-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="b3213-105">В качестве предварительного условия необходимо иметь модель конфигурации продукта, которая содержит один или несколько компонентов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3213-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="b3213-106">В этом примере использует модель динамика класса Hi-End в демонстрационных данных компании USMF.</span><span class="sxs-lookup"><span data-stu-id="b3213-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="b3213-107">Обычно менеджер по продуктам использует эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="b3213-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="b3213-108">Создание новой модели цены</span><span class="sxs-lookup"><span data-stu-id="b3213-108">Create a new price model</span></span>

1. <span data-ttu-id="b3213-109">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="b3213-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="b3213-110">В списке выберите строку **Динамик верхнего сегмента**, но не выбирайте ссылку для имени.</span><span class="sxs-lookup"><span data-stu-id="b3213-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="b3213-111">В области действий выберите **Модель**.</span><span class="sxs-lookup"><span data-stu-id="b3213-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="b3213-112">Выберите **Модели цены**.</span><span class="sxs-lookup"><span data-stu-id="b3213-112">Select **Price models**.</span></span>
1. <span data-ttu-id="b3213-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b3213-113">Select **New**.</span></span>
1. <span data-ttu-id="b3213-114">В поле **Название модели цены** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3213-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="b3213-115">Используйте имя, по которому модель легко идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="b3213-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="b3213-116">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3213-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="b3213-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b3213-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="b3213-118">Добавление элементов цены</span><span class="sxs-lookup"><span data-stu-id="b3213-118">Add price elements</span></span>

1. <span data-ttu-id="b3213-119">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b3213-119">Select **Edit**.</span></span> <span data-ttu-id="b3213-120">Каждый из компонентов в модели продута может иметь базовый элемент цены и любое количество правил выражения цены.</span><span class="sxs-lookup"><span data-stu-id="b3213-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="b3213-121">Можно также добавить цены в разных валютах.</span><span class="sxs-lookup"><span data-stu-id="b3213-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="b3213-122">В поле **Выражение базовой цены** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3213-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="b3213-123">Например, введите "100".</span><span class="sxs-lookup"><span data-stu-id="b3213-123">For example, type 100.</span></span> <span data-ttu-id="b3213-124">Выражение базовой цены может быть численным значением или оно может состоять из арифметического расчета, включающего один или несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3213-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="b3213-125">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b3213-125">Select **Add**.</span></span>
4. <span data-ttu-id="b3213-126">В поле **Имя** введите `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="b3213-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="b3213-127">Имя выражения цены помогает понять, что представляет элемент цены.</span><span class="sxs-lookup"><span data-stu-id="b3213-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="b3213-128">В этом примере нам создаем элемент цены для варианта "Отделка корпуса динамика из палисандра".</span><span class="sxs-lookup"><span data-stu-id="b3213-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="b3213-129">Выберите **Изменить условие**.</span><span class="sxs-lookup"><span data-stu-id="b3213-129">Select **Edit condition**.</span></span> <span data-ttu-id="b3213-130">Условие цены помогает гарантировать, что элемент выражения цены включается в цену продажи только в том случае, если имеется определенное сочетание атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3213-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="b3213-131">В поле **ConstraintBody** введите `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="b3213-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="b3213-132">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b3213-132">Select **OK**.</span></span>
8. <span data-ttu-id="b3213-133">В поле **Выражение** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b3213-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="b3213-134">Например, введите `50`.</span><span class="sxs-lookup"><span data-stu-id="b3213-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="b3213-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b3213-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]