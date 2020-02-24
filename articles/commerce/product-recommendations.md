---
title: Обзор рекомендаций по продуктам
description: В этом разделе приводятся общие сведения о рекомендациях продуктов. Рекомендации по продуктам позволяют пользователям легко и быстро находить нужные продукты и даже те продукты, которые они изначально не планировали покупать.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024987"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="38b30-104">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="38b30-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38b30-105">Microsoft Dynamics 365 Commerce может использоваться для демонстрации рекомендаций по продуктам на веб-сайте электронной коммерции и на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="38b30-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="38b30-106">Рекомендации продуктов — это номенклатуры, которые могут заинтересовать клиента.</span><span class="sxs-lookup"><span data-stu-id="38b30-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="38b30-107">Рекомендации основаны на тенденциях покупки других клиентов в интернет-магазинах и обычных магазинах.</span><span class="sxs-lookup"><span data-stu-id="38b30-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="38b30-108">Рекомендации по продуктам позволяют пользователям легко и быстро находить нужные им продукты, в то время как они имеют опыт, который хорошо им помогает.</span><span class="sxs-lookup"><span data-stu-id="38b30-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="38b30-109">Перекрестные продажи и дополнительные продажи могут быть даже использованы, чтобы помочь клиентам найти другие продукты, которые они изначально не планировали покупать.</span><span class="sxs-lookup"><span data-stu-id="38b30-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="38b30-110">При использовании рекомендаций для обнаружения продукта они могут создавать дополнительные возможности конверсии, повышать доходы от продаж и даже улучшать степень удовлетворенности и удержания клиентов.</span><span class="sxs-lookup"><span data-stu-id="38b30-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="38b30-111">В Commerce рекомендации по продуктам производятся на основе технологий машинного обучения рекомендациям корпорации Microsoft в больших масштабах.</span><span class="sxs-lookup"><span data-stu-id="38b30-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="38b30-112">Сценарии</span><span class="sxs-lookup"><span data-stu-id="38b30-112">Scenarios</span></span>

<span data-ttu-id="38b30-113">Рекомендации по продукции доступны в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="38b30-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="38b30-114">**На любой странице магазина для обзора или целевой странице электронной коммерции**: если клиенты или продавцы магазина посетят страницу магазина, подсистема рекомендаций может предлагать продукты в списках **Новые**, **Лидеры продаж** и **Популярные**.</span><span class="sxs-lookup"><span data-stu-id="38b30-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="38b30-115">**На странице сведений о продукте**: если клиенты или продавцы магазина посещают страницу **Сведения о продукте**, подсистема рекомендаций предлагает дополнительные номенклатуры, которые также могут быть приобретены с высокой вероятностью.</span><span class="sxs-lookup"><span data-stu-id="38b30-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="38b30-116">Эти номенклатуры отображаются в списке **Людям также нравится**.</span><span class="sxs-lookup"><span data-stu-id="38b30-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="38b30-117">**На странице проводки или на странице оформления заказа:** механизм рекомендаций предлагает номенклатуры, основываясь на полном списке номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="38b30-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="38b30-118">Эти номенклатуры отображаются в списке **Вместе с этими товарами часто покупают**.</span><span class="sxs-lookup"><span data-stu-id="38b30-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="38b30-119">**Персонализированные рекомендации**: продавцы могут предоставлять пользователям, вошедшим в систему, персонализированный список **Для вас**, а также новые функции, которые позволяют персонализировать существующие сценарии со списками на основе этого клиента.</span><span class="sxs-lookup"><span data-stu-id="38b30-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="38b30-120">Дополнительные сведения см. в разделе документации по функции: [Включение персонализированных рекомендаций.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="38b30-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="38b30-121">Служба рекомендаций</span><span class="sxs-lookup"><span data-stu-id="38b30-121">Recommendation service</span></span>

<span data-ttu-id="38b30-122">Рекомендации продуктов используют технологии рекомендаций на основе машинного обучению следующим образом:</span><span class="sxs-lookup"><span data-stu-id="38b30-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="38b30-123">Данные в формате, требуемом службой рекомендаций, извлекаются из операционной базы данных Commerce и отправляются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="38b30-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="38b30-124">Служба рекомендаций использует данные для обучения моделей рекомендаций для списков **Людям также нравятся**, **Часто покупаются вместе**, **Новое**, **Лидеры продаж** и **Популярное**.</span><span class="sxs-lookup"><span data-stu-id="38b30-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38b30-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="38b30-125">Additional resources</span></span>

[<span data-ttu-id="38b30-126">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="38b30-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="38b30-127">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="38b30-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="38b30-128">Обзор модуля семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="38b30-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="38b30-129">Создание списков рекомендаций по продукту</span><span class="sxs-lookup"><span data-stu-id="38b30-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="38b30-130">Управление результатами рекомендаций по продукту на основе AI-ML</span><span class="sxs-lookup"><span data-stu-id="38b30-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="38b30-131">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="38b30-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
