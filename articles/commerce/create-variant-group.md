---
title: Создание группы вариантов
description: В этом разделе описывается, как создать группу вариантов размера, стиля или цвета для продукта в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001883"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="22716-103">Создание группы вариантов</span><span class="sxs-lookup"><span data-stu-id="22716-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="22716-104">В этом разделе описывается, как создать группу вариантов размера, стиля или цвета для продукта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22716-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22716-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="22716-105">Overview</span></span>

<span data-ttu-id="22716-106">Dynamics 365 Commerce поддерживает несколько вариантов продуктов.</span><span class="sxs-lookup"><span data-stu-id="22716-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="22716-107">Для различных категорий продуктов лучше всего настроить группы вариантов.</span><span class="sxs-lookup"><span data-stu-id="22716-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="22716-108">Например, группа размера может быть создана для футболок с размерами "самый малый", "малый", "средний", "большой" и "огромный", либо можно создать группу цвета, чтобы включить все доступные цвета продукта.</span><span class="sxs-lookup"><span data-stu-id="22716-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="22716-109">Группы вариантов необходимо добавить перед добавлением продуктов.</span><span class="sxs-lookup"><span data-stu-id="22716-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="22716-110">В этом разделе будет создана и настроена группа размера.</span><span class="sxs-lookup"><span data-stu-id="22716-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="22716-111">Аналогичные процедуры могут использоваться для добавления и настройки групп стилей и групп цветов.</span><span class="sxs-lookup"><span data-stu-id="22716-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="22716-112">Создание группы цвета</span><span class="sxs-lookup"><span data-stu-id="22716-112">Create a size group</span></span>

<span data-ttu-id="22716-113">Чтобы создать группу цвета, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="22716-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="22716-114">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Группы вариантов \> Группы размера**.</span><span class="sxs-lookup"><span data-stu-id="22716-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="22716-115">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="22716-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="22716-116">В поле **Группа размера** введите имя для группы размера.</span><span class="sxs-lookup"><span data-stu-id="22716-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="22716-117">В поле **Описание** введите соответствующее описание.</span><span class="sxs-lookup"><span data-stu-id="22716-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="22716-118">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="22716-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="22716-119">Добавление атрибутов в группу размеров</span><span class="sxs-lookup"><span data-stu-id="22716-119">Add attributes to the size group</span></span>

<span data-ttu-id="22716-120">Чтобы добавить атрибуты в группу размера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="22716-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="22716-121">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Группы вариантов \> Группы размера**</span><span class="sxs-lookup"><span data-stu-id="22716-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="22716-122">В области переходов категорий выберите группу размера.</span><span class="sxs-lookup"><span data-stu-id="22716-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="22716-123">В области **Строки группы размера** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="22716-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="22716-124">В поле **Группа размера** введите строку, представляющую размер (например, "XL").</span><span class="sxs-lookup"><span data-stu-id="22716-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="22716-125">В поле **Имя размера** введите название для размера (например, "огромный").</span><span class="sxs-lookup"><span data-stu-id="22716-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="22716-126">В поле **Вес пополнения** введите число, обозначающее вес пополнения.</span><span class="sxs-lookup"><span data-stu-id="22716-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="22716-127">В поле **Номер в штрих-коде** введите число, представляющее штрих-код.</span><span class="sxs-lookup"><span data-stu-id="22716-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="22716-128">В поле **Порядок отображения** введите номер порядка отображения.</span><span class="sxs-lookup"><span data-stu-id="22716-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="22716-129">По завершении добавления размеров выберите **Сохранить** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="22716-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="22716-130">На следующем рисунке показан пример группы размера для "размеров повседневных футболок".</span><span class="sxs-lookup"><span data-stu-id="22716-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Создание группы цвета](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="22716-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22716-132">Additional resources</span></span>

[<span data-ttu-id="22716-133">Обзор сведений о продуктах</span><span class="sxs-lookup"><span data-stu-id="22716-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="22716-134">Настройка розничных продуктов</span><span class="sxs-lookup"><span data-stu-id="22716-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="22716-135">Аналитики продуктов</span><span class="sxs-lookup"><span data-stu-id="22716-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
