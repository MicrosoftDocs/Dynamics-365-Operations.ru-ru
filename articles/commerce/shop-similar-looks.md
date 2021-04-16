---
title: Включение рекомендаций "покупать похожие образы"
description: В этом разделе описывается, как включить рекомендации по продуктам «покупать похожие образы» в Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 06b5721c423330b8840bb546bdb144c3189c25bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795389"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="cc399-103">Включение рекомендаций «Выбрать похожие по виду»</span><span class="sxs-lookup"><span data-stu-id="cc399-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc399-104">В этом разделе описывается, как включить рекомендации по продуктам «покупать похожие образы» в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc399-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cc399-105">Функция рекомендаций "покупать похожие образы" в Dynamics 365 Commerce использует возможности искусственного интеллекта и машинного обучения (ИИ-ML) для предоставления пользователям рекомендаций по визуально похожим продуктам для клиентов.</span><span class="sxs-lookup"><span data-stu-id="cc399-105">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="cc399-106">Благодаря созданию рекомендаций "покупать похожие образы" для всех каналов розничной Commerce предприятия розничной торговли могут повысить уровень удовлетворенности клиентов, помогая клиентам легко находить то, что им нужно.</span><span class="sxs-lookup"><span data-stu-id="cc399-106">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="cc399-107">Функция рекомендаций "покупать похожие образы" использует изображения продукта с вариантами начального продукта, чтобы найти и рекомендовать визуально схожие продукты в каталоге продуктов предприятия розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="cc399-107">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="cc399-108">Рекомендации "покупать похожие образы" доступны как в POS-приложениях, так и в электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="cc399-108">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="cc399-109">Пример сценариев</span><span class="sxs-lookup"><span data-stu-id="cc399-109">Example scenarios</span></span>

- <span data-ttu-id="cc399-110">Клиент смотрит на черный полосатый свитер и получает рекомендацию на аналогичный свитер красного цвета.</span><span class="sxs-lookup"><span data-stu-id="cc399-110">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="cc399-111">Клиент выбирает рекомендуемый продукт вместо первоначально просмотренного, после чего получает рекомендации для подобных продуктов красного цвета.</span><span class="sxs-lookup"><span data-stu-id="cc399-111">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="cc399-112">Клиент использует рекомендации "покупать похожие образы", чтобы обнаружить подходящие серьги для кольца, которое он хочет купить.</span><span class="sxs-lookup"><span data-stu-id="cc399-112">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="cc399-113">Включение рекомендаций "покупать похожие образы" в модуле Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="cc399-113">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="cc399-114">Рекомендации продуктов поддерживаются только для пользователей Commerce, перенесших свои хранилища в Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="cc399-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cc399-115">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="cc399-115">Prerequisites</span></span>

<span data-ttu-id="cc399-116">Прежде чем предприятия розничной торговли смогут отобразить для клиентов рекомендации "покупать похожие образы", необходимо выполнить два необходимых действия:</span><span class="sxs-lookup"><span data-stu-id="cc399-116">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="cc399-117">[Включение рекомендаций по продукту](enable-product-recommendations.md) в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc399-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="cc399-118">Убедитесь, что сервер мультимедиа поддерживает вызовы HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cc399-118">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="cc399-119">Чтобы модуль рекомендаций был доступен для доступа к изображениям продуктов, предприятиям розничной торговли необходимо создать URL-адреса продуктов.</span><span class="sxs-lookup"><span data-stu-id="cc399-119">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="cc399-120">Чтобы сгенерировать URL-адреса продуктов в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cc399-120">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cc399-121">Перейдите к **Изображения продуктов**.</span><span class="sxs-lookup"><span data-stu-id="cc399-121">Go to **Product images**.</span></span>
1. <span data-ttu-id="cc399-122">В области действий выберите **Определить шаблон СМИ**.</span><span class="sxs-lookup"><span data-stu-id="cc399-122">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="cc399-123">В области свойств **Определить шаблон СМИ** в разделе **URL-адреса СМИ** выберите **создать URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="cc399-123">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc399-124">При включении рекомендаций "покупать похожие образы" начинается процесс создания списков рекомендаций по продуктам.</span><span class="sxs-lookup"><span data-stu-id="cc399-124">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="cc399-125">Доступность и отображение этих список в интернете-магазине и POS-терминалах может занять до одного дня.</span><span class="sxs-lookup"><span data-stu-id="cc399-125">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="cc399-126">Чтобы включить функцию рекомендаций "покупать похожие образы" в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cc399-126">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cc399-127">Перейдите к **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="cc399-127">Go to **Feature management**.</span></span>
1. <span data-ttu-id="cc399-128">В списке доступных функций выполните поиск и выберите вариант **покупать похожие образы**.</span><span class="sxs-lookup"><span data-stu-id="cc399-128">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="cc399-129">В правой области выберите **Включить**, чтобы включить службу.</span><span class="sxs-lookup"><span data-stu-id="cc399-129">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="cc399-130">На следующем рисунке показана функция **покупать похожие образы** на странице **управления функциями** в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="cc399-130">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Функция "покупать похожие образы" на странице управления функциями в Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="cc399-132">После выполнения предыдущих задач POS-приложения автоматически расширяются с помощью контекстной области **покупать похожие продукты**.</span><span class="sxs-lookup"><span data-stu-id="cc399-132">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="cc399-133">Если установить флажок **Показать больше**, пользователи POS-терминала могут быть направлены на специальную страницу "покупать похожие образы", которая может быть отфильтрована в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="cc399-133">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="cc399-134">Если отключить функцию рекомендаций "покупать похожие образы", никакие другие типы рекомендаций не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="cc399-134">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="cc399-135">Дополнительные сведения о рекомендациях продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="cc399-135">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="cc399-136">Добавление кнопки "покупать похожие образы" к страницам со сведениями о продукте с помощью конфигуратора сайта Commerce</span><span class="sxs-lookup"><span data-stu-id="cc399-136">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="cc399-137">После включения функции рекомендаций "покупать похожие образы" в Commerce headquarters в конфигураторе сайта Commerce предприятий розничной торговли могут добавить кнопку **покупать похожие образы** в поле "Покупка" на любой странице сведений о продукте (PDP).</span><span class="sxs-lookup"><span data-stu-id="cc399-137">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="cc399-138">Клиент, который выбрал эту кнопку, переводится на специальную страницу «покупать похожие образы», которая возвращает визуально похожие продукты.</span><span class="sxs-lookup"><span data-stu-id="cc399-138">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="cc399-139">В этом случае клиент может использовать селекторы для дальнейшей фильтрации продуктов.</span><span class="sxs-lookup"><span data-stu-id="cc399-139">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="cc399-140">Чтобы добавить кнопку **покупать похожие образы** к страницам сведений о продукте с помощью конфигуратора сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cc399-140">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cc399-141">Откройте существующую страницу построителя сайтов, которая содержит модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="cc399-141">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="cc399-142">В области переходов слева выберите модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="cc399-142">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="cc399-143">В правой области перехода, установите флажок **Включить ссылку "покупать похожие образы"**.</span><span class="sxs-lookup"><span data-stu-id="cc399-143">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="cc399-144">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="cc399-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="cc399-145">После публикации страницы сведения о продукте включают кнопку **покупать похожие образы**.</span><span class="sxs-lookup"><span data-stu-id="cc399-145">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="cc399-146">На следующем рисунке показан флажок **Включить ссылку "покупать похожие образы"** и кнопка **покупать похожие образы** на примере PDP в конструкторе сайтов.</span><span class="sxs-lookup"><span data-stu-id="cc399-146">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Флажок Включить ссылку "покупать похожие образы" и кнопка "покупать похожие образы" на примере PDP в конструкторе сайтов](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="cc399-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc399-148">Additional resources</span></span>

[<span data-ttu-id="cc399-149">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="cc399-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="cc399-150">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cc399-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="cc399-151">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="cc399-151">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="cc399-152">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="cc399-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="cc399-153">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="cc399-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="cc399-154">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="cc399-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="cc399-155">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="cc399-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="cc399-156">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="cc399-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="cc399-157">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="cc399-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="cc399-158">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="cc399-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
