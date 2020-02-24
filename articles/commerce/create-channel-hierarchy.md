---
title: Создание навигационной иерархии канала
description: В этом разделе описывается, как создать навигационную иерархию канала в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002044"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="f3c18-103">Создание навигационной иерархии канала</span><span class="sxs-lookup"><span data-stu-id="f3c18-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f3c18-104">В этом разделе описывается, как создать навигационную иерархию канала в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3c18-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f3c18-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f3c18-105">Overview</span></span>

<span data-ttu-id="f3c18-106">Навигационная иерархия канала используется для объединения продуктов в категории, чтобы продукты могли просматриваться в Интернете или в POS.</span><span class="sxs-lookup"><span data-stu-id="f3c18-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="f3c18-107">Создание навигационной иерархии канала</span><span class="sxs-lookup"><span data-stu-id="f3c18-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="f3c18-108">Чтобы создать навигационную иерархию канала торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3c18-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f3c18-109">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Навигационные категории каналов**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="f3c18-110">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f3c18-111">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="f3c18-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f3c18-112">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="f3c18-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f3c18-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-113">Select **Create**.</span></span>
1. <span data-ttu-id="f3c18-114">На панели операций выберите **Новый узел категории** для создания корневого узла.</span><span class="sxs-lookup"><span data-stu-id="f3c18-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="f3c18-115">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="f3c18-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f3c18-116">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="f3c18-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f3c18-117">В поле **Понятное имя** введите понятное имя.</span><span class="sxs-lookup"><span data-stu-id="f3c18-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="f3c18-118">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f3c18-119">На следующем рисунке показан пример корневого узла.</span><span class="sxs-lookup"><span data-stu-id="f3c18-119">The following image shows a example root node.</span></span>

![Пример корневого узла](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="f3c18-121">Создание узлов навигационных категорий</span><span class="sxs-lookup"><span data-stu-id="f3c18-121">Create navigation category nodes</span></span>

<span data-ttu-id="f3c18-122">Чтобы создать дополнительные узлы навигационных категорий для представления категорий продуктов в канале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3c18-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="f3c18-123">В области переходов выберите родительский узел, к которому требуется добавить категорию.</span><span class="sxs-lookup"><span data-stu-id="f3c18-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="f3c18-124">На панели операций выберите **Новый узел категории**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="f3c18-125">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="f3c18-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f3c18-126">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="f3c18-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f3c18-127">В поле **Понятное имя** введите понятное имя.</span><span class="sxs-lookup"><span data-stu-id="f3c18-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="f3c18-128">В поле **Порядок отображения** введите порядок отображения (необязательно).</span><span class="sxs-lookup"><span data-stu-id="f3c18-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="f3c18-129">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f3c18-130">На следующем рисунке показан пример готовой навигационной иерархии канала.</span><span class="sxs-lookup"><span data-stu-id="f3c18-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Пример иерархии каналов](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="f3c18-132">Добавление продуктов в узлы категории</span><span class="sxs-lookup"><span data-stu-id="f3c18-132">Add products to category nodes</span></span>

<span data-ttu-id="f3c18-133">Чтобы добавить продукты в узлы категорий, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3c18-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="f3c18-134">Выберите узел категории.</span><span class="sxs-lookup"><span data-stu-id="f3c18-134">Select a category node.</span></span>
1. <span data-ttu-id="f3c18-135">В **Продукты** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="f3c18-136">Найдите новые продукты, которые требуется добавить с использованием номера продукта или наименования продукта, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="f3c18-137">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f3c18-138">Добавление продуктов в узел внутри навигационной иерархии каналов недостаточно для того, чтобы продукты отображались в выбранном канале, продукты также должны быть включены в ассортимент продукта.</span><span class="sxs-lookup"><span data-stu-id="f3c18-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="f3c18-139">На следующем рисунке показан пример узла с добавленными продуктами.</span><span class="sxs-lookup"><span data-stu-id="f3c18-139">The following image shows an example node with products added.</span></span>

![Продукты, добавленные в узел категории](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="f3c18-141">Добавление групп атрибутов продуктов в узлы категорий</span><span class="sxs-lookup"><span data-stu-id="f3c18-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="f3c18-142">Группы атрибутов должны быть созданы до того, как их можно будет добавить в узел внутри навигационной иерархии канала.</span><span class="sxs-lookup"><span data-stu-id="f3c18-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="f3c18-143">Чтобы добавить продукт группы атрибутов в узел категории, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3c18-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="f3c18-144">Выберите узел категории.</span><span class="sxs-lookup"><span data-stu-id="f3c18-144">Select a category node.</span></span>
1. <span data-ttu-id="f3c18-145">В разделе **Группа атрибутов продукта** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="f3c18-146">Найдите группы атрибутов, которые требуется добавить, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="f3c18-147">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f3c18-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f3c18-148">На следующем рисунке показан пример узла с добавленными группами атрибутов продуктов.</span><span class="sxs-lookup"><span data-stu-id="f3c18-148">The following image shows a sample node with product attribute groups added.</span></span>

![Группы атрибутов продукта в узле](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="f3c18-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3c18-150">Additional resources</span></span>

[<span data-ttu-id="f3c18-151">Настройка ассортиментов</span><span class="sxs-lookup"><span data-stu-id="f3c18-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="f3c18-152">Управление атрибутами и группами атрибутов</span><span class="sxs-lookup"><span data-stu-id="f3c18-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)
