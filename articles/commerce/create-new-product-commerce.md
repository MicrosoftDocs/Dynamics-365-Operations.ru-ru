---
title: Создание нового продукта в Commerce
description: В этом разделе описывается, как создать продукт в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138569"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="a1d04-103">Создание нового продукта в Commerce</span><span class="sxs-lookup"><span data-stu-id="a1d04-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a1d04-104">В этом разделе описывается, как создать продукт в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1d04-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1d04-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="a1d04-105">Overview</span></span>

<span data-ttu-id="a1d04-106">Продукт определяется главным образом номером, названием и описанием продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="a1d04-107">Однако для описания продукта или услуги также требуются другие данные:</span><span class="sxs-lookup"><span data-stu-id="a1d04-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="a1d04-108">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="a1d04-108">Create a new product</span></span>

1. <span data-ttu-id="a1d04-109">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Продукты по категориям**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="a1d04-110">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a1d04-111">В раскрывающемся списке **Тип продукта** выберите **Номенклатура** или **Услуга**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="a1d04-112">В раскрывающемся списке **Подтип продукта** выберите либо **Продукт** (если у продукта не будет вариантов), либо **Шаблон продукта** (если у продукта будут варианты).</span><span class="sxs-lookup"><span data-stu-id="a1d04-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="a1d04-113">В поле **Номер продукта** введите номер продукта, если он еще не был предварительно заполнен.</span><span class="sxs-lookup"><span data-stu-id="a1d04-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="a1d04-114">В поле **Название продукта** введите название продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="a1d04-115">В поле **Краткое наименование** введите краткое наименование.</span><span class="sxs-lookup"><span data-stu-id="a1d04-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="a1d04-116">В раскрывающемся списке **Категория розничной торговли** выберите соответствующую категорию.</span><span class="sxs-lookup"><span data-stu-id="a1d04-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="a1d04-117">Если продукт является комплектом, выберите **Да** для **Комплект продуктов**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="a1d04-118">Если подтип продукта — шаблон продукта, настройте **Группа аналитики продукта**, чтобы включить поддерживаемые варианты.</span><span class="sxs-lookup"><span data-stu-id="a1d04-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="a1d04-119">Варианты включают **Цвет**, **Размер**, **Стиль** и **Конфигурация**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="a1d04-120">При необходимости, возможно, потребуется создать дополнительные группы аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="a1d04-121">В раскрывающемся списке **Технология конфигурации** выберите соответствующий вариант.</span><span class="sxs-lookup"><span data-stu-id="a1d04-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="a1d04-122">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-122">Select **OK**.</span></span>

<span data-ttu-id="a1d04-123">На следующем рисунке показан пример добавляемого продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-123">The following image shows an example product being added.</span></span>

![Создание продукта](media/create-new-product.png)

<span data-ttu-id="a1d04-125">После добавления продукта для него могут быть заданы дополнительные данные, такие как **Описание продукта**, **Группы вариантов**, **Группы аналитик**, **Атрибуты продуктов** и **Связанные продукты**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="a1d04-126">На следующем рисунке показаны дополнительные сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="a1d04-126">The following image shows a product's additional details.</span></span>

![Сведения о продукте](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="a1d04-128">Создание вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="a1d04-128">Create product variants</span></span>

<span data-ttu-id="a1d04-129">Если подтип продукта — **Шаблон продукта**, необходимо создать конкретные варианты.</span><span class="sxs-lookup"><span data-stu-id="a1d04-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="a1d04-130">Чтобы создать варианты продукта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1d04-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="a1d04-131">В области операций выберите **Варианты продукта**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="a1d04-132">Если в области действий выбраны группы вариантов, выберите \**Предложения вариантов*.</span><span class="sxs-lookup"><span data-stu-id="a1d04-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="a1d04-133">Выберите варианты, которые необходимо поддерживать для продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="a1d04-134">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="a1d04-135">Запустить продукт в производство</span><span class="sxs-lookup"><span data-stu-id="a1d04-135">Release a product</span></span>

<span data-ttu-id="a1d04-136">Чтобы продать продукт, он должен быть сначала запущен в производство юридического лица.</span><span class="sxs-lookup"><span data-stu-id="a1d04-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="a1d04-137">На странице продукта выберите **Запуск продуктов в производство**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-137">From the product page, select **Release products**.</span></span>

    ![Запуск продукта в производство](media/create-new-product-3.png)

1. <span data-ttu-id="a1d04-139">Выберите продукт для запуска в производство, а затем нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-139">Select the product to release, and then select **Next**.</span></span>

    ![Выберите продукт для запуска в производство](media/create-new-product-4.png)

1. <span data-ttu-id="a1d04-141">Выберите набор вариантов продукта для запуска в производство, а затем нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Выберите варианты для запуска в производство](media/create-new-product-5.png)

1. <span data-ttu-id="a1d04-143">Выберите юридическое лицо, а затем нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-143">Select the legal entity, and then select **Next**.</span></span>

    ![Выберите юридическое лицо](media/create-new-product-6.png)

1. <span data-ttu-id="a1d04-145">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-145">Select **Finish**.</span></span>

    ![Завершение запуска продукта в производство](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="a1d04-147">Настройка выпущенных продуктов</span><span class="sxs-lookup"><span data-stu-id="a1d04-147">Configure a released product</span></span>

<span data-ttu-id="a1d04-148">После выпуска продукта он потребует дополнительной настройки, которая включает добавление цены к продукту.</span><span class="sxs-lookup"><span data-stu-id="a1d04-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="a1d04-149">В области переходов выберите **Модули \> Retail и Commerce \> Продукты и категории \> Выпущенные продукты по категориям**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="a1d04-150">Выберите узел категории продуктов для выпущенного продукта, а затем выберите продукт из списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="a1d04-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="a1d04-151">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="a1d04-152">В разделе **Покупка** настройте все необходимые свойства, включая **Единица измерения**, **Цена** и **Количество**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="a1d04-153">В области действий выберите **Проверить**, чтобы убедиться в том, что для отсутствующих полей ошибки не выводятся.</span><span class="sxs-lookup"><span data-stu-id="a1d04-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="a1d04-154">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a1d04-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a1d04-155">На следующем рисунке показан пример конфигурации для выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="a1d04-155">The following image shows an example configuration for a released product.</span></span>

![Настройка выпущенного продукта](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="a1d04-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a1d04-157">Additional resources</span></span>

[<span data-ttu-id="a1d04-158">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="a1d04-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="a1d04-159">Создание группы вариантов</span><span class="sxs-lookup"><span data-stu-id="a1d04-159">Create a variant group</span></span>](create-variant-group.md) 
