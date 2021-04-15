---
title: Создание иерархии продуктов
description: В этом разделе описывается, как создать иерархию продукта в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8aef33a501f43105730eaa21a9159eb1398a1b36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799573"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="78b3a-103">Создание иерархии продуктов</span><span class="sxs-lookup"><span data-stu-id="78b3a-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="78b3a-104">В этом разделе описывается, как создать иерархию продукта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78b3a-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="78b3a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="78b3a-105">Overview</span></span>

<span data-ttu-id="78b3a-106">Dynamics 365 Commerce поддерживает несколько розничных каналов.</span><span class="sxs-lookup"><span data-stu-id="78b3a-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="78b3a-107">Эти розничные каналы включают в себя интернет-магазины, центры обработки вызовов и розничные магазины (также называются физическими магазинами).</span><span class="sxs-lookup"><span data-stu-id="78b3a-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="78b3a-108">Каждый канал розничного магазина может иметь свои собственные способы оплаты, группы цен, контрольно-кассовые машины POS, счета выручки и расходов и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="78b3a-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="78b3a-109">Необходимо настроить все эти элементы перед тем, как можно создать канал розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="78b3a-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="78b3a-110">Иерархия продукта Commerce используется для определения общей иерархии продуктов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="78b3a-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="78b3a-111">Можно использовать иерархию продукта Commerce для мерчендайзинга, ценообразования и специальных акций, отчетности и планирования ассортимента.</span><span class="sxs-lookup"><span data-stu-id="78b3a-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="78b3a-112">Для каждой организации может быть назначена только одна иерархия продуктов Commerce.</span><span class="sxs-lookup"><span data-stu-id="78b3a-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="78b3a-113">Создание и настройка иерархии продукта</span><span class="sxs-lookup"><span data-stu-id="78b3a-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="78b3a-114">Чтобы создать и настроить иерархию продукта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78b3a-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="78b3a-115">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Иерархия продукта Commerce**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="78b3a-116">Если иерархии еще не существует, в **области действий** выберите **Создать**, чтобы создать корень иерархии.</span><span class="sxs-lookup"><span data-stu-id="78b3a-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="78b3a-117">В разделе **Общие**:</span><span class="sxs-lookup"><span data-stu-id="78b3a-117">Under **General**:</span></span>
    1. <span data-ttu-id="78b3a-118">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="78b3a-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="78b3a-119">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="78b3a-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="78b3a-120">В поле **Понятное имя** введите понятное имя.</span><span class="sxs-lookup"><span data-stu-id="78b3a-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="78b3a-121">Задайте для **Активный** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="78b3a-122">Добавлением узлов иерархии</span><span class="sxs-lookup"><span data-stu-id="78b3a-122">Add hierarchy nodes</span></span>

<span data-ttu-id="78b3a-123">Чтобы добавить узлы иерархии, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="78b3a-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="78b3a-124">На панели операций выберите **Изменить иерархию категорий**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="78b3a-125">Выберите родительский узел, к которому требуется добавить новый узел, а затем выберите **Создать узел категории**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="78b3a-126">В разделе **Общие** введите **Имя**, **Описание**, **Понятное имя** и **Ключевые слова**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="78b3a-127">В разделе **Общие**:</span><span class="sxs-lookup"><span data-stu-id="78b3a-127">Under **General**:</span></span>
    1. <span data-ttu-id="78b3a-128">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="78b3a-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="78b3a-129">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="78b3a-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="78b3a-130">В поле **Понятное имя** введите понятное имя.</span><span class="sxs-lookup"><span data-stu-id="78b3a-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="78b3a-131">В поле **Ключевые слова** введите соответствующие ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="78b3a-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="78b3a-132">В поле **Порядок отображения** введите номер порядка отображения (необязательно).</span><span class="sxs-lookup"><span data-stu-id="78b3a-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="78b3a-133">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="78b3a-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="78b3a-134">Повторите описанные выше шаги, чтобы добавить дополнительные узлы.</span><span class="sxs-lookup"><span data-stu-id="78b3a-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="78b3a-135">На следующем рисунке показано создание нового узла иерархии продукта.</span><span class="sxs-lookup"><span data-stu-id="78b3a-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Создание иерархии продуктов](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="78b3a-137">Другие параметры</span><span class="sxs-lookup"><span data-stu-id="78b3a-137">Other settings</span></span>

<span data-ttu-id="78b3a-138">Группы атрибутов категории также могут быть назначены каждой группе в соответствии с необходимостью.</span><span class="sxs-lookup"><span data-stu-id="78b3a-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="78b3a-139">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="78b3a-139">Additional resources</span></span>

[<span data-ttu-id="78b3a-140">Иерархии Commerce</span><span class="sxs-lookup"><span data-stu-id="78b3a-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="78b3a-141">Управление продуктами и категориями продуктов </span><span class="sxs-lookup"><span data-stu-id="78b3a-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="78b3a-142">Изменение порядка сортировки для объектов мерчандайзинга</span><span class="sxs-lookup"><span data-stu-id="78b3a-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]