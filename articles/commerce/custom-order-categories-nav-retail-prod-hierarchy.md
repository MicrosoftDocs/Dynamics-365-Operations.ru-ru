---
title: Изменение порядка сортировки для сбытовых объектов
description: В этом разделе объясняются понятия, связанные с управлением порядком отображения различных сбытовых объектов в Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799477"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="17d18-103">Изменение порядка сортировки для сбытовых объектов</span><span class="sxs-lookup"><span data-stu-id="17d18-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="17d18-104">Предприятия розничной торговли считают обнаружение продукта основным средством для взаимодействия с клиентами по всем каналам.</span><span class="sxs-lookup"><span data-stu-id="17d18-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="17d18-105">Различные функциональные возможности позволяют пользователям легко обнаруживать продукты.</span><span class="sxs-lookup"><span data-stu-id="17d18-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="17d18-106">Например, они могут просматривать категории, искать и фильтровать.</span><span class="sxs-lookup"><span data-stu-id="17d18-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="17d18-107">В этом разделе объясняются понятия, связанные с управлением порядком отображения различных сбытовых объектов.</span><span class="sxs-lookup"><span data-stu-id="17d18-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="17d18-108">Здесь также объясняется порядок изменения порядка сортировки.</span><span class="sxs-lookup"><span data-stu-id="17d18-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="17d18-109">Обзор</span><span class="sxs-lookup"><span data-stu-id="17d18-109">Overview</span></span>

<span data-ttu-id="17d18-110">Улучшена поддержка сортировки различных сбытовых объектов.</span><span class="sxs-lookup"><span data-stu-id="17d18-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="17d18-111">Эта поддержка теперь лучше связана с существующими клиентскими сценариями, которым ранее требовали расширений от партнеров по реализации.</span><span class="sxs-lookup"><span data-stu-id="17d18-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="17d18-112">В версиях Retail до версии 10.0.5 порядок сортировки категорий в иерархии переходов был алфавитным.</span><span class="sxs-lookup"><span data-stu-id="17d18-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="17d18-113">Новая функция настраиваемого порядка сортировки позволяет менеджерам по продажам настраивать порядок сортировки для различных сбытовых объектов среди всех клиентов конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="17d18-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="17d18-114">Эти клиенты включают штаб-квартиры (HQ) и центры обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="17d18-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="17d18-115">Настройка порядка отображения категорий в иерархии продукции</span><span class="sxs-lookup"><span data-stu-id="17d18-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="17d18-116">Перед выполнением этой процедуры демонстрационные данные должны быть установлены в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="17d18-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="17d18-117">Перейдите в раздел **Retail и Commerce \> Продукты и категории \> Иерархия продукта Commerce**.</span><span class="sxs-lookup"><span data-stu-id="17d18-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="17d18-118">Щелкните **Изменить иерархию категорий**.</span><span class="sxs-lookup"><span data-stu-id="17d18-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="17d18-119">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="17d18-119">Click **Edit**.</span></span>
4. <span data-ttu-id="17d18-120">В дереве разверните **ВСЕ \> Экстремальные виды спорта**.</span><span class="sxs-lookup"><span data-stu-id="17d18-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="17d18-121">В дереве разверните **ВСЕ \> Командные виды спорта**.</span><span class="sxs-lookup"><span data-stu-id="17d18-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="17d18-122">В поле **Порядок отображения** введите число.</span><span class="sxs-lookup"><span data-stu-id="17d18-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="17d18-123">(Число может быть отрицательным.)</span><span class="sxs-lookup"><span data-stu-id="17d18-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="17d18-124">Повторите шаги с 4 по 6 для любых дополнительных категорий, порядок которых нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="17d18-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="17d18-125">Порядок отображения для иерархии навигации канала будет отражен в головном офисе для иерархии продукции Commerce и выпущенных продуктов по категориям.</span><span class="sxs-lookup"><span data-stu-id="17d18-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Пользовательская сортировка иерархии продуктов с отрицательными значениями](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Выпущенные продукты по категориям с настраиваемой сортировкой на основе иерархии продукции](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="17d18-128">Настройка порядка отображения категорий в иерархии навигации по каналам</span><span class="sxs-lookup"><span data-stu-id="17d18-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="17d18-129">Перед выполнением этой процедуры демонстрационные данные должны быть установлены в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="17d18-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="17d18-130">Выберите **Retail и Commerce \> Продукты и категории \> Навигационные категории каналов**.</span><span class="sxs-lookup"><span data-stu-id="17d18-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="17d18-131">В списке выберите **Навигации по модным продуктам**.</span><span class="sxs-lookup"><span data-stu-id="17d18-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="17d18-132">Щелкните **Изменить иерархию категорий**.</span><span class="sxs-lookup"><span data-stu-id="17d18-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="17d18-133">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="17d18-133">Click **Edit**.</span></span>
5. <span data-ttu-id="17d18-134">В дереве выберите **Мода \> Женская одежда \> Женская обувь**.</span><span class="sxs-lookup"><span data-stu-id="17d18-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="17d18-135">В поле **Порядок отображения** введите число.</span><span class="sxs-lookup"><span data-stu-id="17d18-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="17d18-136">В дереве выберите **Мода \> Женская одежда \> Кофты**.</span><span class="sxs-lookup"><span data-stu-id="17d18-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="17d18-137">Аналогично, можно определить порядок сортировки подкатегорий.</span><span class="sxs-lookup"><span data-stu-id="17d18-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="17d18-138">В дереве выберите **Мода \> Мужская одежда \> Повседневные рубашки**.</span><span class="sxs-lookup"><span data-stu-id="17d18-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="17d18-139">В поле **Порядок отображения** введите число.</span><span class="sxs-lookup"><span data-stu-id="17d18-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="17d18-140">В дереве выберите **Мода \> Мужская одежда \> Пальто и куртки**.</span><span class="sxs-lookup"><span data-stu-id="17d18-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="17d18-141">В поле **Порядок отображения** введите число.</span><span class="sxs-lookup"><span data-stu-id="17d18-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="17d18-142">Повторите для любых дополнительных категорий, порядок которых нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="17d18-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="17d18-143">Порядок отображения для иерархии навигации канала отражается в главном офисе, каталоге и каналах торговли.</span><span class="sxs-lookup"><span data-stu-id="17d18-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Навигационная иерархия канала с настраиваемой сортировкой](./media/ChannelNavCustomSorted.png)

![Пользовательская сортировка иерархии навигации по каталогу, основанная на иерархии навигации канала](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS-терминал с настраиваемой сортировкой категорий](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="17d18-147">По умолчанию функция настраиваемого порядка сортировки отключена.</span><span class="sxs-lookup"><span data-stu-id="17d18-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="17d18-148">Чтобы узнать, как включить эту функцию и другие функции, см. раздел [Управление функциями](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="17d18-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]