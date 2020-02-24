---
title: Настройка оценок и отзывов
description: В этом разделе описывается, как настроить сайт электронной коммерции, чтобы показать оценки и обзоры клиентов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002205"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="dfdd7-103">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="dfdd7-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dfdd7-104">В этом разделе описывается, как настроить сайт электронной коммерции, чтобы показать оценки и обзоры клиентов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dfdd7-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="dfdd7-105">Overview</span></span>

<span data-ttu-id="dfdd7-106">Оценки и обзоры на веб-сайтах электронной коммерции помогают пользователям изучить продукты перед принятием решения о покупке, показывая им, что другие клиенты думают об этих продуктах.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="dfdd7-107">Для веб-сайтов электронной коммерции оценки и обзоры также являются механизмом сбора отзывов клиентов о продуктах.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="dfdd7-108">Оценки отображаются на страницах списка продуктов, страницах списка категорий, страницах результатов поиска и других страницах сайта.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="dfdd7-109">Гистограммы оценок и обзоры продуктов показаны на страницах сведений о продукте (PDP).</span><span class="sxs-lookup"><span data-stu-id="dfdd7-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="dfdd7-110">Кнопка **Написать обзор** позволяет пользователям отправлять оценки и обзоры продукта.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="dfdd7-111">Модули оценок и отзывов на страницах PDP</span><span class="sxs-lookup"><span data-stu-id="dfdd7-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="dfdd7-112">Три модуля отображают сводку оценок и обзоров на страницах PDP:</span><span class="sxs-lookup"><span data-stu-id="dfdd7-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="dfdd7-113">Модуль создания отзыва</span><span class="sxs-lookup"><span data-stu-id="dfdd7-113">Write review module</span></span>
- <span data-ttu-id="dfdd7-114">Модуль списка отзывов о продуктах</span><span class="sxs-lookup"><span data-stu-id="dfdd7-114">Product reviews list module</span></span>
- <span data-ttu-id="dfdd7-115">Модуль гистограммы оценок</span><span class="sxs-lookup"><span data-stu-id="dfdd7-115">Ratings histogram module</span></span>
 
<span data-ttu-id="dfdd7-116">На следующем рисунке показано, как выглядят модули оценки и отзывов на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Модули оценок и отзывов на странице PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="dfdd7-118">Сведения о том, как оптимизировать шаблоны и макеты PDP, чтобы иметь возможность совместного использования конфигураций для модулей оценок и отзывов на нескольких страницах PDP на сайте электронной коммерции, см. в разделе [Обзор шаблонов и макетов](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dfdd7-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="dfdd7-119">На следующем рисунке показано, как диалоговое окно **Добавить модуль** представляет модули оценок и отзывов в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Диалоговое окно добавления модуля](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="dfdd7-121">Модуль создания отзыва</span><span class="sxs-lookup"><span data-stu-id="dfdd7-121">Write review module</span></span>

<span data-ttu-id="dfdd7-122">Модуль создания отзыва включает кнопку **Написать отзыв**, позволяющую пользователям войти в систему, назначать рейтинг и написать отзыв о продукте.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="dfdd7-123">Этот модуль также позволяет пользователям редактировать рейтинг или отзыв, которые они отправили ранее.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="dfdd7-124">Этот модуль обычно располагается над модулями гистограммы оценок и списка отзывов о продукте на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="dfdd7-125">На следующем рисунке показано диалоговое окно **Написать отзыв**, которое появляется, когда клиент выбирает **Написать отзыв**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="dfdd7-126">Клиент может использовать это диалоговое окно для отправки рейтинга и отзыва.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Диалоговое окно создания отзыва](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="dfdd7-128">В следующей таблице показано свойство модуля создания отзыва, которое необходимо настроить в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="dfdd7-129">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="dfdd7-129">Property name</span></span> | <span data-ttu-id="dfdd7-130">Стоимость</span><span class="sxs-lookup"><span data-stu-id="dfdd7-130">Value</span></span>        | <span data-ttu-id="dfdd7-131">Описание свойства</span><span class="sxs-lookup"><span data-stu-id="dfdd7-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="dfdd7-132">Название</span><span class="sxs-lookup"><span data-stu-id="dfdd7-132">Name</span></span>          | <span data-ttu-id="dfdd7-133">Написать отзыв</span><span class="sxs-lookup"><span data-stu-id="dfdd7-133">Write review</span></span> | <span data-ttu-id="dfdd7-134">Имя модуля создания отзыва.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="dfdd7-135">Модуль гистограммы оценок</span><span class="sxs-lookup"><span data-stu-id="dfdd7-135">Ratings histogram module</span></span>

<span data-ttu-id="dfdd7-136">В модуле гистограммы оценок отображается гистограмма оценок.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="dfdd7-137">Этот модуль обычно появляется между модулем создания отзыва и модулем списка отзывов о продукте на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="dfdd7-138">Модуль гистограммы оценок не требует настройки.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="dfdd7-139">Необходимо просто добавить модуль в шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="dfdd7-140">На следующем рисунке показано, как выглядит шаблон PDP в Dynamics 365 Commerce в том случае, когда модули оценок и отзывов настроены для отображения на страницах сведений о продуктах.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![Шаблон PDP, когда оценки и отзыва настроены для отображения на страницах сведений о продуктах](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="dfdd7-142">Модуль списка отзывов о продуктах</span><span class="sxs-lookup"><span data-stu-id="dfdd7-142">Product reviews list module</span></span>

<span data-ttu-id="dfdd7-143">Модуль списка отзывов о продукте отображает список отзывов о продукте вместе с вариантами сортировки, фильтрации и разбивки на страницы.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="dfdd7-144">Этот модуль обычно появляется после модуля гистограммы оценок на странице PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="dfdd7-145">В следующей таблице показаны свойства модуля списка отзывов о продукте, которое необходимо настроить в инструменте разработки.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="dfdd7-146">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="dfdd7-146">Property name</span></span>              | <span data-ttu-id="dfdd7-147">Стоимость</span><span class="sxs-lookup"><span data-stu-id="dfdd7-147">Value</span></span> | <span data-ttu-id="dfdd7-148">Описание свойства</span><span class="sxs-lookup"><span data-stu-id="dfdd7-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="dfdd7-149">Отзывы, отображаемые на каждой странице</span><span class="sxs-lookup"><span data-stu-id="dfdd7-149">Reviews shown on each page</span></span> | <span data-ttu-id="dfdd7-150">10</span><span class="sxs-lookup"><span data-stu-id="dfdd7-150">10</span></span>    | <span data-ttu-id="dfdd7-151">Количество отзывов, которые должны отображаться одновременно на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="dfdd7-152">Кнопки **Далее** и **Назад** включены, чтобы пользователи могли перемещаться по страницам отзывов.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="dfdd7-153">Гистограмма оценок — представление сводки</span><span class="sxs-lookup"><span data-stu-id="dfdd7-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="dfdd7-154">Модуль списка отзывов о продукте включает слот, позволяющий добавить модуль гистограммы оценок.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="dfdd7-155">На следующем рисунке показано, как добавить модуль гистограммы оценок в модуль списка отзывов о продукте в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Добавление модуля гистограммы оценок в модуль списка отзывов о продукте](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="dfdd7-157">Настройка сайта для отображения оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="dfdd7-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="dfdd7-158">Значения конфигурации для оценок и отзывов, например идентификатор клиента, длина текста отзыва и длина заголовка отзыва, настраиваются на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="dfdd7-159">Чтобы настроить сайт для отображения оценок и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="dfdd7-160">Перейти к **Домашняя страница \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="dfdd7-161">Выберите имя сайта.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="dfdd7-162">Перейдите к пункту на **Управление сайтом \> Расширяемость**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="dfdd7-163">В поле **Максимальная длина текста отзыва** введите максимальное число знаков, которое может иметь текст отзыва (например, **1000**).</span><span class="sxs-lookup"><span data-stu-id="dfdd7-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="dfdd7-164">В поле **Максимальная длина заголовка отзыва** введите максимальное число знаков, которое может иметь заголовок отзыва (например, **55**).</span><span class="sxs-lookup"><span data-stu-id="dfdd7-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="dfdd7-165">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="dfdd7-166">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Настройка сайта для отображения оценок и отзывов](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="dfdd7-168">Связывание рейтинга продукта с разделом отзывов на странице PDP</span><span class="sxs-lookup"><span data-stu-id="dfdd7-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="dfdd7-169">Оценка продукта отображается под названием продукта в верхней части страницы PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="dfdd7-170">Рейтинг продукта можно настроить таким образом, чтобы он был связан с разделом **Отзывы** той же страницы PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="dfdd7-171">Чтобы связать оценку продукта с разделом **Отзывы** страницы PDP, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="dfdd7-172">Откройте шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="dfdd7-173">Перейти к пункту **Настройки модуля-контейнера поля покупки**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="dfdd7-174">В разделе **Поле покупки** выберите **Оценки продуктов**, затем установите флажок **Связать щелчок с полным модулем отзывов**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="dfdd7-175">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Связывание рейтинга продукта с разделом отзывов на странице PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="dfdd7-177">Настройка ссылки на страницу конфиденциальности и политики</span><span class="sxs-lookup"><span data-stu-id="dfdd7-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="dfdd7-178">Чтобы настроить ссылку на страницу конфиденциальности и политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="dfdd7-179">Перейти к **Домашняя страница \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="dfdd7-180">Выберите имя сайта.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="dfdd7-181">Перейдите к пункту на **Управление сайтом \> Расширяемость**</span><span class="sxs-lookup"><span data-stu-id="dfdd7-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="dfdd7-182">На вкладке **Маршруты** в области **Конфиденциальность и политика RNR** выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="dfdd7-183">Если ссылка уже введена и ее необходимо заменить, выберите ссылку.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="dfdd7-184">В диалоговом окне **Добавление ссылки** выберите ссылку на страницу конфиденциальности и политики, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="dfdd7-185">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="dfdd7-186">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfdd7-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Настройка ссылки на страницу конфиденциальности и политики](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="dfdd7-188">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dfdd7-188">Additional resources</span></span>

[<span data-ttu-id="dfdd7-189">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="dfdd7-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="dfdd7-190">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="dfdd7-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="dfdd7-191">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="dfdd7-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="dfdd7-192">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="dfdd7-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
