---
title: Настройка оценок и отзывов
description: В этом разделе описывается, как настроить сайт электронной коммерции, чтобы показать оценки и обзоры клиентов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fcdf571378c25d71b3ef4f3baad062a25390417
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993558"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="7eb27-103">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="7eb27-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7eb27-104">В этом разделе описывается, как настроить сайт электронной коммерции, чтобы показать оценки и обзоры клиентов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb27-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7eb27-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="7eb27-105">Overview</span></span>

<span data-ttu-id="7eb27-106">Оценки и обзоры на веб-сайтах электронной коммерции помогают пользователям изучить продукты перед принятием решения о покупке, показывая им, что другие клиенты думают об этих продуктах.</span><span class="sxs-lookup"><span data-stu-id="7eb27-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="7eb27-107">Для веб-сайтов электронной коммерции оценки и обзоры также являются механизмом сбора отзывов клиентов о продуктах.</span><span class="sxs-lookup"><span data-stu-id="7eb27-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="7eb27-108">Настройка сайта для отображения оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="7eb27-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="7eb27-109">Значения конфигурации для оценок и отзывов, например идентификатор клиента, длина текста отзыва и длина заголовка отзыва, настраиваются на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="7eb27-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="7eb27-110">Чтобы настроить сайт для отображения оценок и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7eb27-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="7eb27-111">Перейти к **Домашняя страница \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="7eb27-112">Выберите имя сайта.</span><span class="sxs-lookup"><span data-stu-id="7eb27-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="7eb27-113">Перейдите к **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="7eb27-114">В поле **Максимальная длина текста отзыва** введите максимальное число знаков, которое может иметь текст отзыва (например, **1000**).</span><span class="sxs-lookup"><span data-stu-id="7eb27-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="7eb27-115">В поле **Максимальная длина заголовка отзыва** введите максимальное число знаков, которое может иметь заголовок отзыва (например, **55**).</span><span class="sxs-lookup"><span data-stu-id="7eb27-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="7eb27-116">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="7eb27-117">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb27-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Настройка сайта для отображения оценок и отзывов](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="7eb27-119">Связывание рейтинга продукта с разделом отзывов на странице PDP</span><span class="sxs-lookup"><span data-stu-id="7eb27-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="7eb27-120">Оценка продукта отображается под названием продукта в верхней части страницы PDP.</span><span class="sxs-lookup"><span data-stu-id="7eb27-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="7eb27-121">Рейтинг продукта можно настроить таким образом, чтобы он был связан с разделом **Отзывы** той же страницы PDP.</span><span class="sxs-lookup"><span data-stu-id="7eb27-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="7eb27-122">Чтобы связать оценку продукта с разделом **Отзывы** страницы PDP, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7eb27-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="7eb27-123">Откройте шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="7eb27-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="7eb27-124">Перейти к пункту **Настройки модуля-контейнера поля покупки**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="7eb27-125">В разделе **Поле покупки** выберите **Оценки продуктов**, затем установите флажок **Связать щелчок с полным модулем отзывов**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="7eb27-126">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb27-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Связывание рейтинга продукта с разделом отзывов на странице PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="7eb27-128">Настройка ссылки на страницу конфиденциальности и политики</span><span class="sxs-lookup"><span data-stu-id="7eb27-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="7eb27-129">Чтобы настроить ссылку на страницу конфиденциальности и политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7eb27-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="7eb27-130">Перейти к **Домашняя страница \> Сайты**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="7eb27-131">Выберите имя сайта.</span><span class="sxs-lookup"><span data-stu-id="7eb27-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="7eb27-132">Перейдите к **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="7eb27-133">На вкладке **Маршруты** в области **Конфиденциальность и политика RNR** выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="7eb27-134">Если ссылка уже введена и ее необходимо заменить, выберите ссылку.</span><span class="sxs-lookup"><span data-stu-id="7eb27-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="7eb27-135">В диалоговом окне **Добавление ссылки** выберите ссылку на страницу конфиденциальности и политики, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="7eb27-136">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="7eb27-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="7eb27-137">На следующем рисунке показано, как выглядит эта конфигурация в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb27-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Настройка ссылки на страницу конфиденциальности и политики](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="7eb27-139">Настройка модулей оценок и отзывов на страницах сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="7eb27-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="7eb27-140">Для получения дополнительных сведений о настройке модулей оценок и отзывов на страницах сведений о продукте см . в разделе [Модули оценок и отзывов](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="7eb27-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7eb27-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7eb27-141">Additional resources</span></span>

[<span data-ttu-id="7eb27-142">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="7eb27-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="7eb27-143">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="7eb27-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="7eb27-144">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="7eb27-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="7eb27-145">Настройка модулей оценок и отзывов на страницах сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="7eb27-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="7eb27-146">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="7eb27-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
