---
title: Включите персонализированные рекомендации по продуктам
description: В этом разделе описывается, как сделать персонализированные рекомендации о продуктах доступными в Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bdb56a1f45cdea1832bd269502e534efdb207b03
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127913"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="839af-103">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="839af-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="839af-104">В этом разделе описывается, как сделать персонализированные рекомендации о продуктах доступными в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="839af-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="839af-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="839af-105">Overview</span></span>

<span data-ttu-id="839af-106">В Dynamics 365 Commerce розничные продавцы могут сделать доступными персонализированные рекомендации по продуктам (также называемые персонализацией).</span><span class="sxs-lookup"><span data-stu-id="839af-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="839af-107">Таким образом, персонализированные рекомендации могут быть включены в интернет-магазине и в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="839af-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="839af-108">Когда функция персонализации включена, система может связать сведения о покупке пользователя и сведения о продукте, чтобы создать индивидуальные рекомендаций по продуктам.</span><span class="sxs-lookup"><span data-stu-id="839af-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="839af-109">Предварительные условия для персонализации</span><span class="sxs-lookup"><span data-stu-id="839af-109">Personalization prerequisites</span></span>

<span data-ttu-id="839af-110">Перед тем как предоставить пользователям доступ к персонализированным рекомендациям по продуктам, обратите внимание, что рекомендации по продукту поддерживаются только для тех пользователей Commerce, которые выполнили миграцию своего магазина в Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="839af-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="839af-111">Прежде чем клиенты смогут получить персонализированные рекомендации по продуктам, розничные продавцы должны [включить рекомендации по продуктам](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="839af-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="839af-112">При включении рекомендаций по продукту можно также включить персонализацию.</span><span class="sxs-lookup"><span data-stu-id="839af-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="839af-113">Однако если персонализация отключена, другие типы рекомендаций по продукту не отключаются.</span><span class="sxs-lookup"><span data-stu-id="839af-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="839af-114">Дополнительные сведения о рекомендациях продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="839af-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="839af-115">Включение персонализации</span><span class="sxs-lookup"><span data-stu-id="839af-115">Turn on personalization</span></span>

<span data-ttu-id="839af-116">Чтобы включить персонализацию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="839af-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="839af-117">Выберите **Retail и Commerce \> Рекомендации продуктов \> Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="839af-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="839af-118">В списке общих параметров Retail выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="839af-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="839af-119">Для параметра **Включить персонализацию** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="839af-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Включение персонализации](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="839af-121">При включении персонализации запускается процесс создания персонализированных списков рекомендаций по продуктам.</span><span class="sxs-lookup"><span data-stu-id="839af-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="839af-122">Доступность и отображение этих список в интернете-магазине и POS-терминале может занять до одного дня.</span><span class="sxs-lookup"><span data-stu-id="839af-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="839af-123">Персонализированные списки</span><span class="sxs-lookup"><span data-stu-id="839af-123">Personalized lists</span></span>

<span data-ttu-id="839af-124">В дополнение к персонализации существующих списков, созданных машиной, служба рекомендаций позволяет осуществлять персонализацию поиска продуктов как в интернет-магазине, так и в POS.</span><span class="sxs-lookup"><span data-stu-id="839af-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="839af-125">После включения персонализации в розничных магазинах могут отображаться персонализированные списки "Для вас" в интернет-магазине или "Рекомендуется для клиентов" в POS-терминалах.</span><span class="sxs-lookup"><span data-stu-id="839af-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="839af-126">Кроме того, розничные магазины могут персонализацию для существующих списков рекомендаций по продуктам и обеспечивать отказ от персонализации для прошедших аутентификацию пользователей согласно Общему регламенту по защите данных (GDPR).</span><span class="sxs-lookup"><span data-stu-id="839af-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="839af-127">Если персонализация отключена, вы также отключите эти функции.</span><span class="sxs-lookup"><span data-stu-id="839af-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="839af-128">Списки "Для вас" в интернет-магазине</span><span class="sxs-lookup"><span data-stu-id="839af-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="839af-129">Список "Для вас" представляет собой список машинного обучения с ИИ (AI-ML), который показывает пользователю, прошедшему аутентификацию, персонализированный список предлагаемых продуктов.</span><span class="sxs-lookup"><span data-stu-id="839af-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="839af-130">Этот список основан на многоканальной истории покупок пользователя.</span><span class="sxs-lookup"><span data-stu-id="839af-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="839af-131">Персонализированные рекомендации обновляются динамически по мере того, как пользователь делает больше покупок.</span><span class="sxs-lookup"><span data-stu-id="839af-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="839af-132">Этот тип списка также поддерживает фильтрацию категорий, так что розничные продавцы могут отображать самое популярное на основе навигационных иерархий.</span><span class="sxs-lookup"><span data-stu-id="839af-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="839af-133">Прежде чем список "Для вас" может появиться на любой странице электронной коммерции, должны быть выполнены следующие требования для пользователя:</span><span class="sxs-lookup"><span data-stu-id="839af-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="839af-134">Пользователи должны войти в систему.</span><span class="sxs-lookup"><span data-stu-id="839af-134">Users must be signed in.</span></span> <span data-ttu-id="839af-135">Анонимные пользователи не увидят персонализированных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="839af-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="839af-136">У пользователей должна быть хотя бы одна покупка для своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="839af-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="839af-137">Пользователи должны согласиться на получение персонализированных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="839af-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="839af-138">На следующем рисунке показан пример списка "Для вас" на странице интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="839af-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Список "Для вас" в интернет-магазине](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="839af-140">Списки "Рекомендовано для клиентов" на POS-терминале</span><span class="sxs-lookup"><span data-stu-id="839af-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="839af-141">Для улучшения отношений с клиентами розничные продавцы могут персонализировать существующие страницы сведений о клиентах путем добавления контекстуального списка "Рекомендовано для клиентов".</span><span class="sxs-lookup"><span data-stu-id="839af-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="839af-142">На следующем рисунке показан пример списка "Рекомендовано для клиентов" на странице POS-терминала.</span><span class="sxs-lookup"><span data-stu-id="839af-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Список "Рекомендовано для клиентов" на POS-терминале](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="839af-144">Применение персонализации к существующим спискам рекомендаций</span><span class="sxs-lookup"><span data-stu-id="839af-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="839af-145">Розничные магазины могут применять персонализацию к существующим спискам рекомендаций, таким как "Новые", "Популярные", "Лидеры продаж", "Людям также нравится" и "Часто покупают вместе".</span><span class="sxs-lookup"><span data-stu-id="839af-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="839af-146">Когда персонализация применяется к существующим спискам, номенклатуры, ранее купленные пользователем, удаляются из этих списков.</span><span class="sxs-lookup"><span data-stu-id="839af-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="839af-147">Для анонимных пользователей и пользователей, которые отказались от персонализированных рекомендаций, отображаются версии существующих списков по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="839af-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="839af-148">Таким образом, компаниям розничной торговли не придется вручную управлять отдельными страницами.</span><span class="sxs-lookup"><span data-stu-id="839af-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="839af-149">Например, вошедший в систему пользователь уже приобрел черные часы и коричневые рабочие ботинки, которые появляется в списке "Популярно — по умолчанию" на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="839af-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="839af-150">Таким образом, вместо этих продуктов пользователь увидит новые продукты, как показано в списке "Популярное — персонализировано".</span><span class="sxs-lookup"><span data-stu-id="839af-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Применение персонализации](./media/applypersonalization.png)

<span data-ttu-id="839af-152">Чтобы применить персонализацию к существующему списку рекомендаций в построителе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="839af-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="839af-153">Откройте существующую страницу построителя сайтов, которая содержит модуль коллекции продуктов.</span><span class="sxs-lookup"><span data-stu-id="839af-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="839af-154">В области переходов слева выберите модуль коллекции продуктов.</span><span class="sxs-lookup"><span data-stu-id="839af-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="839af-155">В области переходов под **Продукты**, выберите список.</span><span class="sxs-lookup"><span data-stu-id="839af-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="839af-156">В диалоговом окне **Выбор конфигурации списка продуктов** в **Тип** выберите тип списка.</span><span class="sxs-lookup"><span data-stu-id="839af-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="839af-157">Установите флажок **Применить персонализацию** и затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="839af-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Применение персонализации для списка популярного](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="839af-159">Сохраните страницу, завершите ее редактирование и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="839af-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="839af-160">После публикации страницы вошедшие в систему пользователи увидят персонализированные списки популярного.</span><span class="sxs-lookup"><span data-stu-id="839af-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="839af-161">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="839af-161">Additional resources</span></span>

[<span data-ttu-id="839af-162">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="839af-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="839af-163">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="839af-163">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="839af-164">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="839af-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="839af-165">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="839af-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="839af-166">Добавление списков рекомендаций на сайт электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="839af-166">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="839af-167">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="839af-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="839af-168">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="839af-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="839af-169">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="839af-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="839af-170">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="839af-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="839af-171">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="839af-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="839af-172">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="839af-172">Product recommendations FAQ</span></span>](faq-recommendations.md)
