---
title: Включение рекомендаций "купить похожие по описанию"
description: В этом разделе описывается, как включить рекомендации по продуктам "купить похожие по описанию" в Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098646"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="a7300-103">Включение рекомендаций "купить похожие по описанию"</span><span class="sxs-lookup"><span data-stu-id="a7300-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7300-104">В этом разделе описывается, как включить рекомендации по продуктам "купить похожие по описанию" в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7300-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a7300-105">Функция рекомендаций "купить похожие по описанию" в Dynamics 365 Commerce использует возможности искусственного интеллекта и машинного обучения (ИИ-ML) для предоставления пользователям рекомендаций по продуктам, описания которых похожи на то, что ищет клиент.</span><span class="sxs-lookup"><span data-stu-id="a7300-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="a7300-106">Благодаря созданию рекомендаций "купить похожие по описанию" для всех каналов розничной Commerce предприятия розничной торговли могут помочь клиентам легко находить то, что им нужно.</span><span class="sxs-lookup"><span data-stu-id="a7300-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="a7300-107">Функция рекомендаций "купить похожие по описанию" использует название и описание начальных продуктов, чтобы найти и рекомендовать схожие продукты в каталоге продуктов предприятия розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="a7300-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="a7300-108">Рекомендации "купить похожие по описанию" доступны как в POS-приложениях, так и в электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="a7300-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="a7300-109">Пример сценариев</span><span class="sxs-lookup"><span data-stu-id="a7300-109">Example scenarios</span></span>

<span data-ttu-id="a7300-110">В следующих примерах сценариев показаны типы рекомендаций, которые может предоставить функция "купить похожие по описанию":</span><span class="sxs-lookup"><span data-stu-id="a7300-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="a7300-111">Клиент просматривает пару очков в роговой оправе в стиле ретро и получает набор рекомендаций для других очков, имеющих подобный дизайн, в контексте отрасли розничного продавца.</span><span class="sxs-lookup"><span data-stu-id="a7300-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="a7300-112">Клиент использует рекомендации "купить похожие по описанию" для обнаружения разновидностей кофе, аналогичных разновидностям, которые ранее были приобретены у продавца.</span><span class="sxs-lookup"><span data-stu-id="a7300-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="a7300-113">Настройка рекомендаций "купить похожие по описанию"</span><span class="sxs-lookup"><span data-stu-id="a7300-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="a7300-114">Рекомендации продуктов поддерживаются только для пользователей Commerce, перенесших свои хранилища в Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="a7300-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a7300-115">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a7300-115">Prerequisites</span></span>

<span data-ttu-id="a7300-116">Перед тем как можно будет отобразить рекомендации "купить похожие по описанию" для клиентов, необходимо выполнить следующие необходимые условия:</span><span class="sxs-lookup"><span data-stu-id="a7300-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="a7300-117">[Включение рекомендаций по продукту](enable-product-recommendations.md) в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="a7300-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="a7300-118">Убедитесь, что сервер мультимедиа поддерживает вызовы HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a7300-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="a7300-119">Включение функции рекомендаций "купить похожие по описанию"</span><span class="sxs-lookup"><span data-stu-id="a7300-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="a7300-120">Чтобы включить функцию рекомендаций "купить похожие по описанию" в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7300-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a7300-121">В рабочей области **Управление функциями** в списке доступных функций найдите и выберите **Купить похожие по описанию**.</span><span class="sxs-lookup"><span data-stu-id="a7300-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="a7300-122">В правой области выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="a7300-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="a7300-123">Когда функция включена, система начинает создавать списки рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="a7300-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="a7300-124">Чтобы эти списки стали доступны и видны и Интернете и POS-терминалах, может потребоваться до одного дня.</span><span class="sxs-lookup"><span data-stu-id="a7300-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="a7300-125">Если выключить эту функцию, это не повлияет на другие типы рекомендаций по продуктам.</span><span class="sxs-lookup"><span data-stu-id="a7300-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="a7300-126">Дополнительные сведения о рекомендациях продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a7300-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="a7300-127">Добавление кнопки "купить похожие по описанию" на страницы сведений о продуктах</span><span class="sxs-lookup"><span data-stu-id="a7300-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="a7300-128">После включения функции рекомендаций "купить похожие по описанию" в Commerce headquarters вы можете добавить кнопку **купить похожие по описанию** в поле покупки на любой странице сведений о продукте (PDP).</span><span class="sxs-lookup"><span data-stu-id="a7300-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="a7300-129">Клиент, который выбрал эту кнопку, переводится на специальную страницу **Купить похожие по описанию**, которая показывает визуально похожие продукты.</span><span class="sxs-lookup"><span data-stu-id="a7300-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="a7300-130">Клиент затем может использовать селекторы для дальнейшей фильтрации продуктов.</span><span class="sxs-lookup"><span data-stu-id="a7300-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="a7300-131">Чтобы добавить кнопку **Купить похожие по описанию** к страницам сведений о продукте с помощью конфигуратора сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7300-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a7300-132">Откройте существующую страницу построителя сайтов, которая содержит модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="a7300-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="a7300-133">В области переходов слева выберите модуль поля покупки.</span><span class="sxs-lookup"><span data-stu-id="a7300-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="a7300-134">В правой области перехода установите флажок **Включить ссылку "купить похожие по описанию"**.</span><span class="sxs-lookup"><span data-stu-id="a7300-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="a7300-135">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a7300-135">Select **Save**.</span></span>
1. <span data-ttu-id="a7300-136">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="a7300-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="a7300-137">После публикации страницы сведения о продукте включают кнопку **Купить похожие по описанию**.</span><span class="sxs-lookup"><span data-stu-id="a7300-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="a7300-138">На следующем рисунке показан флажок **Включить ссылку "Купить похожие по описанию"** и кнопка **Купить похожие по описанию** на примере страницы PDP в конструкторе сайтов.</span><span class="sxs-lookup"><span data-stu-id="a7300-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Флажок "Включить ссылку покупки похожих по описанию" и кнопка "Купить похожие по описанию" на странице PDP в конструкторе сайтов](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="a7300-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7300-140">Additional resources</span></span>

[<span data-ttu-id="a7300-141">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="a7300-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a7300-142">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a7300-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a7300-143">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="a7300-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a7300-144">Включение рекомендаций «Выбрать похожие по виду»</span><span class="sxs-lookup"><span data-stu-id="a7300-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a7300-145">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="a7300-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a7300-146">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="a7300-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a7300-147">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="a7300-147">Product recommendations FAQ</span></span>](faq-recommendations.md)
