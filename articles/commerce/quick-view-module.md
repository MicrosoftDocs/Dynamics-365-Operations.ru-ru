---
title: Модуль быстрого просмотра
description: В этом разделе описываются модули быстрого просмотра, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097060"
---
# <a name="quick-view-module"></a><span data-ttu-id="074cd-103">Модуль быстрого просмотра</span><span class="sxs-lookup"><span data-stu-id="074cd-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="074cd-104">В этом разделе описываются модули быстрого просмотра, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="074cd-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="074cd-105">Модуль быстрого просмотра позволяет пользователям быстро просматривать сведения о продукте при просмотре продуктов на странице списка и добавлять один или несколько продуктов в корзину со страницы списка без перехода на страницу сведений о продукте (PDP).</span><span class="sxs-lookup"><span data-stu-id="074cd-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="074cd-106">В модуле быстрого просмотра содержится обзор сведений о продукте, которые требуются пользователям для принятия решения "добавить в корзину".</span><span class="sxs-lookup"><span data-stu-id="074cd-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="074cd-107">Он также предоставляет ссылку на страницу PDP, чтобы пользователи могли просмотреть дополнительные сведения о продукте и параметры покупки.</span><span class="sxs-lookup"><span data-stu-id="074cd-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="074cd-108">Модуль быстрого просмотра поддерживается модулями [коллекции продуктов](product-collection-module-overview.md) и [результатов поиска](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="074cd-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="074cd-109">Модуль быстрого просмотра доступен в выпуске Commerce версии 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="074cd-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="074cd-110">На следующем рисунке показан пример модуля быстрого просмотра на странице списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="074cd-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Пример модуля быстрого просмотра на странице списка продуктов](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="074cd-112">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="074cd-112">Module properties</span></span>

<span data-ttu-id="074cd-113">Модуль быстрого просмотра поддерживает те же функции, что и модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="074cd-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="074cd-114">Таким образом, свойства модуля быстрого просмотра похожи на свойства модуля поля покупки.</span><span class="sxs-lookup"><span data-stu-id="074cd-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="074cd-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="074cd-115">Property</span></span> | <span data-ttu-id="074cd-116">Значения</span><span class="sxs-lookup"><span data-stu-id="074cd-116">Values</span></span> | <span data-ttu-id="074cd-117">описание</span><span class="sxs-lookup"><span data-stu-id="074cd-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="074cd-118">Тег заголовка</span><span class="sxs-lookup"><span data-stu-id="074cd-118">Heading tag</span></span> | <span data-ttu-id="074cd-119">**H1**, **H2**, **H3**, **H4**, **H5** или **H6**</span><span class="sxs-lookup"><span data-stu-id="074cd-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="074cd-120">Это свойство определяет тег заголовка для названия продукта.</span><span class="sxs-lookup"><span data-stu-id="074cd-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="074cd-121">Если модуль быстрого просмотра находится вверху страницы, это свойство должно иметь значение **H1** для соответствия стандартам специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="074cd-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="074cd-122">Разрешить произвольную цену</span><span class="sxs-lookup"><span data-stu-id="074cd-122">Allow custom price</span></span> | <span data-ttu-id="074cd-123">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="074cd-123">**True** or **False**</span></span> | <span data-ttu-id="074cd-124">Если это свойство имеет значение **True**, пользователь может ввести пользовательскую цену.</span><span class="sxs-lookup"><span data-stu-id="074cd-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="074cd-125">Минимальная цена</span><span class="sxs-lookup"><span data-stu-id="074cd-125">Minimum price</span></span> | <span data-ttu-id="074cd-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="074cd-126">Integer</span></span> | <span data-ttu-id="074cd-127">Это свойство применимо только в том случае, если свойство **Разрешить нестандартную цену** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="074cd-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="074cd-128">Оно определяет минимальную цену, которую пользователь может ввести (например, 1 доллар США).</span><span class="sxs-lookup"><span data-stu-id="074cd-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="074cd-129">Максимальная цена</span><span class="sxs-lookup"><span data-stu-id="074cd-129">Maximum price</span></span> | <span data-ttu-id="074cd-130">Целое число</span><span class="sxs-lookup"><span data-stu-id="074cd-130">Integer</span></span> | <span data-ttu-id="074cd-131">Это свойство применимо только в том случае, если свойство **Разрешить нестандартную цену** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="074cd-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="074cd-132">Оно определяет максимальную цену, которую пользователь может ввести (например, 1 000 долларов США).</span><span class="sxs-lookup"><span data-stu-id="074cd-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="074cd-133">Параметры конструктора сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="074cd-133">Commerce site builder settings</span></span>

<span data-ttu-id="074cd-134">Подобно модулю поля покупки, модуль быстрого просмотра учитывает настройки **Параметры сайта \> Расширения \> Добавить продукт в корзину**.</span><span class="sxs-lookup"><span data-stu-id="074cd-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="074cd-135">Однако параметр **Перейти к странице корзины** игнорируется, поскольку он не согласуется с целью модуля быстрого просмотра, который должен позволять пользователям просматривать несколько продуктов на странице списка и добавлять их в корзину без ухода со страницы списка.</span><span class="sxs-lookup"><span data-stu-id="074cd-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="074cd-136">Добавление модуля быстрого просмотра на страницу коллекции продуктов</span><span class="sxs-lookup"><span data-stu-id="074cd-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="074cd-137">Модуль быстрого просмотра может быть добавлен в модули коллекции продуктов и результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="074cd-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="074cd-138">Чтобы добавить модуль быстрого просмотра в модуль коллекции продуктов в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="074cd-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="074cd-139">Перейдите в раздел **Страницы**, затем выберите главную страницу сайта Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="074cd-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="074cd-140">Перейдите к любому модулю **Коллекция продуктов** на главной странице, выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="074cd-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="074cd-141">В диалоговом окне **Добавить модуль** выберите модуль **Быстрый просмотр**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="074cd-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="074cd-142">В области свойств модуля **Быстрый просмотр** выберите **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="074cd-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="074cd-143">В диалоговом окне **Заголовок** задайте в поле **Уровень заголовка** значение **H2**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="074cd-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="074cd-144">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="074cd-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="074cd-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="074cd-145">Additional resources</span></span>

[<span data-ttu-id="074cd-146">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="074cd-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="074cd-147">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="074cd-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="074cd-148">Модуль семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="074cd-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="074cd-149">Модуль результатов поиска</span><span class="sxs-lookup"><span data-stu-id="074cd-149">Search results module</span></span>](search-result-module.md)
