---
title: Модули оценок и отзывов
description: В этом разделе рассматриваются модули оценок и отзывов, используемые на страницах сведений о продукте в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: a243399536fec3f5361104289c38e550bf8b1144
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193290"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="058cc-103">Модули оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="058cc-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="058cc-104">В этом разделе рассматриваются модули оценок и отзывов, используемые на страницах сведений о продукте (PDP) в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="058cc-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="058cc-105">Оценки и отзывы на веб-сайтах электронной коммерции помогают пользователям изучить продукты перед принятием решения о покупке, а также являются механизмом сбора отзывов клиентов о продуктах.</span><span class="sxs-lookup"><span data-stu-id="058cc-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="058cc-106">Оценки отображаются на страницах списка продуктов, страницах списка категорий, страницах результатов поиска и других страницах сайта.</span><span class="sxs-lookup"><span data-stu-id="058cc-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="058cc-107">Гистограммы оценок и обзоры продуктов показаны на страницах PDP.</span><span class="sxs-lookup"><span data-stu-id="058cc-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="058cc-108">Кнопка **Написать обзор** позволяет пользователям отправлять оценки и обзоры продукта.</span><span class="sxs-lookup"><span data-stu-id="058cc-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="058cc-109">Управление этими функциями PDP осуществляется с помощью модулей оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="058cc-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="058cc-110">Модули оценок и отзывов на страницах PDP</span><span class="sxs-lookup"><span data-stu-id="058cc-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="058cc-111">Три модуля отображают сводку оценок и обзоров на страницах PDP:</span><span class="sxs-lookup"><span data-stu-id="058cc-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="058cc-112">Модуль создания отзыва</span><span class="sxs-lookup"><span data-stu-id="058cc-112">Write review module</span></span>
- <span data-ttu-id="058cc-113">Модуль списка отзывов о продуктах</span><span class="sxs-lookup"><span data-stu-id="058cc-113">Product reviews list module</span></span>
- <span data-ttu-id="058cc-114">Модуль гистограммы оценок</span><span class="sxs-lookup"><span data-stu-id="058cc-114">Ratings histogram module</span></span>
 
<span data-ttu-id="058cc-115">На следующем рисунке показано, как выглядят модули оценки и отзывов на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="058cc-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Модули оценок и отзывов на странице PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="058cc-117">Сведения о том, как оптимизировать шаблоны и макеты PDP, чтобы иметь возможность совместного использования конфигураций для модулей оценок и отзывов на нескольких страницах PDP на сайте электронной коммерции, см. в разделе [Обзор шаблонов и макетов](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="058cc-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="058cc-118">На следующем рисунке показано, как диалоговое окно **Добавить модуль** представляет модули оценок и отзывов в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="058cc-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="058cc-119">![Диалоговое окно добавления модуля](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="058cc-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="058cc-120">Модуль создания отзыва</span><span class="sxs-lookup"><span data-stu-id="058cc-120">Write review module</span></span>

<span data-ttu-id="058cc-121">Модуль создания отзыва включает кнопку **Написать отзыв**, позволяющую пользователям войти в систему, назначать рейтинг и написать отзыв о продукте.</span><span class="sxs-lookup"><span data-stu-id="058cc-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="058cc-122">Этот модуль также позволяет пользователям редактировать рейтинг или отзыв, которые они отправили ранее.</span><span class="sxs-lookup"><span data-stu-id="058cc-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="058cc-123">Этот модуль обычно располагается над модулями гистограммы оценок и списка отзывов о продукте на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="058cc-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="058cc-124">На следующем рисунке показано диалоговое окно **Написать отзыв**, которое появляется, когда клиент выбирает **Написать отзыв**.</span><span class="sxs-lookup"><span data-stu-id="058cc-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="058cc-125">Клиент может использовать это диалоговое окно для отправки рейтинга и отзыва.</span><span class="sxs-lookup"><span data-stu-id="058cc-125">The customer can use this dialog box to submit a rating and a review.</span></span>

![Диалоговое окно создания отзыва](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="058cc-127">В следующей таблице показано свойство модуля создания отзыва, которое необходимо настроить в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="058cc-127">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="058cc-128">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="058cc-128">Property name</span></span> | <span data-ttu-id="058cc-129">Стоимость</span><span class="sxs-lookup"><span data-stu-id="058cc-129">Value</span></span>        | <span data-ttu-id="058cc-130">Описание свойства</span><span class="sxs-lookup"><span data-stu-id="058cc-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="058cc-131">Название</span><span class="sxs-lookup"><span data-stu-id="058cc-131">Name</span></span>          | <span data-ttu-id="058cc-132">Написать отзыв</span><span class="sxs-lookup"><span data-stu-id="058cc-132">Write review</span></span> | <span data-ttu-id="058cc-133">Имя модуля создания отзыва.</span><span class="sxs-lookup"><span data-stu-id="058cc-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="058cc-134">Модуль гистограммы оценок</span><span class="sxs-lookup"><span data-stu-id="058cc-134">Ratings histogram module</span></span>

<span data-ttu-id="058cc-135">В модуле гистограммы оценок отображается гистограмма оценок.</span><span class="sxs-lookup"><span data-stu-id="058cc-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="058cc-136">Этот модуль обычно появляется между модулем создания отзыва и модулем списка отзывов о продукте на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="058cc-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="058cc-137">Модуль гистограммы оценок не требует настройки.</span><span class="sxs-lookup"><span data-stu-id="058cc-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="058cc-138">Необходимо просто добавить модуль в шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="058cc-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="058cc-139">На следующем рисунке показано, как выглядит шаблон PDP в Dynamics 365 Commerce в том случае, когда модули оценок и отзывов настроены для отображения на страницах сведений о продуктах.</span><span class="sxs-lookup"><span data-stu-id="058cc-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="058cc-140">![Шаблон PDP, когда оценки и отзыва настроены для отображения на страницах сведений о продуктах](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="058cc-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="058cc-141">Модуль списка отзывов о продуктах</span><span class="sxs-lookup"><span data-stu-id="058cc-141">Product reviews list module</span></span>

<span data-ttu-id="058cc-142">Модуль списка отзывов о продукте отображает список отзывов о продукте вместе с вариантами сортировки, фильтрации и разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="058cc-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="058cc-143">Этот модуль обычно появляется после модуля гистограммы оценок на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="058cc-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="058cc-144">В следующей таблице показаны свойства модуля списка отзывов о продукте, которое необходимо настроить в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="058cc-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="058cc-145">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="058cc-145">Property name</span></span>              | <span data-ttu-id="058cc-146">Стоимость</span><span class="sxs-lookup"><span data-stu-id="058cc-146">Value</span></span> | <span data-ttu-id="058cc-147">Описание свойства</span><span class="sxs-lookup"><span data-stu-id="058cc-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="058cc-148">Отзывы, отображаемые на каждой странице</span><span class="sxs-lookup"><span data-stu-id="058cc-148">Reviews shown on each page</span></span> | <span data-ttu-id="058cc-149">10</span><span class="sxs-lookup"><span data-stu-id="058cc-149">10</span></span>    | <span data-ttu-id="058cc-150">Количество отзывов, которые должны отображаться одновременно на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="058cc-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="058cc-151">Кнопки **Далее** и **Назад** включены, чтобы пользователи могли перемещаться по страницам отзывов.</span><span class="sxs-lookup"><span data-stu-id="058cc-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="058cc-152">Гистограмма оценок — представление сводки</span><span class="sxs-lookup"><span data-stu-id="058cc-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="058cc-153">Модуль списка отзывов о продукте включает слот, позволяющий добавить модуль гистограммы оценок.</span><span class="sxs-lookup"><span data-stu-id="058cc-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="058cc-154">На следующем рисунке показано, как добавить модуль гистограммы оценок в модуль списка отзывов о продукте в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="058cc-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Добавление модуля гистограммы оценок в модуль списка отзывов о продукте](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="058cc-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="058cc-156">Additional resources</span></span>

[<span data-ttu-id="058cc-157">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="058cc-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="058cc-158">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="058cc-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="058cc-159">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="058cc-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="058cc-160">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="058cc-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="058cc-161">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="058cc-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="058cc-162">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="058cc-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="058cc-163">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="058cc-163">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]