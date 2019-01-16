---
title: "Определение скидок, специфичных для канала"
description: "Продавцы часто устанавливают различные скидки в различных каналах. В этом разделе рассматриваются понятия, которые необходимо знать для создания скидки для конкретного канала."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: a136e245beaf8dfd8bcf19d49f8a355c8871cde7
ms.contentlocale: ru-ru
ms.lasthandoff: 01/04/2019

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="b4742-104">Определение скидок, специфичных для канала</span><span class="sxs-lookup"><span data-stu-id="b4742-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4742-105">Продавцы часто устанавливают различные скидки в различных каналах.</span><span class="sxs-lookup"><span data-stu-id="b4742-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="b4742-106">В этом разделе рассматриваются понятия, которые необходимо знать для создания скидки для конкретного канала.</span><span class="sxs-lookup"><span data-stu-id="b4742-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="b4742-107">Скидки, специфичные для канала</span><span class="sxs-lookup"><span data-stu-id="b4742-107">Channel-specific discounts</span></span>

<span data-ttu-id="b4742-108">Продавцы часто предлагаю различные скидки в различных каналах.</span><span class="sxs-lookup"><span data-stu-id="b4742-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="b4742-109">Это может быть сделано для того, чтобы учесть конъюнктуру местного рынка, или для борьбы с конкурирующими розничными продавцами.</span><span class="sxs-lookup"><span data-stu-id="b4742-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="b4742-110">В Microsoft Dynamics 365 for Retail используются ценовые группы, чтобы определить специфические для канала скидки.</span><span class="sxs-lookup"><span data-stu-id="b4742-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="b4742-111">Ценовые группы можно назначить одной или нескольким из следующих объектов: каналы, каталоги, назначения и программы лояльности.</span><span class="sxs-lookup"><span data-stu-id="b4742-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="b4742-112">В этой статье обсуждаются каналы, но эти же концепции применимы к скидкам по каталогу, скидкам для назначений и скидкам по программам лояльности.</span><span class="sxs-lookup"><span data-stu-id="b4742-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="b4742-113">Группы цен</span><span class="sxs-lookup"><span data-stu-id="b4742-113">Price groups</span></span>

<span data-ttu-id="b4742-114">[![Группы цен](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="b4742-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="b4742-115">Диаграмма выше иллюстрирует отношение между объектами, которые могут находиться в проводке (канал, каталог, назначение, клиент, карточка лояльности) и различные типы скидок, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="b4742-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="b4742-116">Все проводки происходят в канале, поэтому канал гарантировано присутствует в проводке.</span><span class="sxs-lookup"><span data-stu-id="b4742-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="b4742-117">Остальные объекты необязательные.</span><span class="sxs-lookup"><span data-stu-id="b4742-117">The remaining entities are optional.</span></span> <span data-ttu-id="b4742-118">На каждой из страниц справочника имеется ссылка на странице связанных ценовых групп, где можно просматривать и добавлять ценовые группы по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="b4742-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="b4742-119">Ценовая группа используется для того, чтобы связать четыре различных типов объектов со скидками, корректировками цен и коммерческими соглашениями.</span><span class="sxs-lookup"><span data-stu-id="b4742-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="b4742-120">Мы рекомендуем планировать стратегию того, как вы называете ваши ценовые группы, чтобы систематизировать их.</span><span class="sxs-lookup"><span data-stu-id="b4742-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="b4742-121">Один вариант заключается в использовании буквенного или цифрового префикса или суффикса, чтобы различать разные типы.</span><span class="sxs-lookup"><span data-stu-id="b4742-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="b4742-122">Например, 1-xxxxx для ценовых групп канала и 2-xxxxx для ценовых групп каталога.</span><span class="sxs-lookup"><span data-stu-id="b4742-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="b4742-123">Предусмотрено четыре страницы запросов, которые фокусируются на каждом из розничных объектов, с которыми могут быть связаны скидки.</span><span class="sxs-lookup"><span data-stu-id="b4742-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="b4742-124">**Группы цен канала розничной торговли** — эта страница показывает список каналов и скидок, связанных совместно для каждой ценовой группы.</span><span class="sxs-lookup"><span data-stu-id="b4742-124">**Retail channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b4742-125">**Ценовые группы каталога** — эта страница показывает список каталогов и скидок, связанных совместно для каждой ценовой группы.</span><span class="sxs-lookup"><span data-stu-id="b4742-125">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b4742-126">**Группы цен программ лояльности** — эта страница показывает список программ лояльности и скидок, связанных совместно для каждой ценовой группы.</span><span class="sxs-lookup"><span data-stu-id="b4742-126">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b4742-127">**Ценовые группы назначений** — эта страница показывает список назначений и скидок, связанных совместно для каждой ценовой группы.</span><span class="sxs-lookup"><span data-stu-id="b4742-127">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="b4742-128">Пример настройки скидки для канала</span><span class="sxs-lookup"><span data-stu-id="b4742-128">Example channel discount set up</span></span>

<span data-ttu-id="b4742-129">Следующий пример иллюстрирует задачи, входящие в настройку скидки для канала.</span><span class="sxs-lookup"><span data-stu-id="b4742-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="b4742-130">В этом примере имеется канал с названием **Хьюстоном**, и вы собираетесь создать новую скидку с названием **Снова в школу**.</span><span class="sxs-lookup"><span data-stu-id="b4742-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="b4742-131">Поскольку стратегия ценообразования и скидок включает в себя возможность скидок для канала, при создании канала всегда создается специфическая для канала ценовая группа.</span><span class="sxs-lookup"><span data-stu-id="b4742-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="b4742-132">Вы имеете ценовую группу **Хьюстон-ЦГ**, которая задана каналу **Хьюстон**.</span><span class="sxs-lookup"><span data-stu-id="b4742-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="b4742-133">После создания новой скидки **Снова в школу** требуется нажать **Группы цен** вверху страницы **Скидка**.</span><span class="sxs-lookup"><span data-stu-id="b4742-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="b4742-134">Открывается страница **Ценовые группы скидок**.</span><span class="sxs-lookup"><span data-stu-id="b4742-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="b4742-135">Затем нажмите **Создать** и выберите ценовую группу **Хьюстон-ЦГ**.</span><span class="sxs-lookup"><span data-stu-id="b4742-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="b4742-136">Теперь вы можете включить скидку и передать ее в канал.</span><span class="sxs-lookup"><span data-stu-id="b4742-136">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4742-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4742-137">Additional resources</span></span>

[<span data-ttu-id="b4742-138">Корректировки цены и скидки</span><span class="sxs-lookup"><span data-stu-id="b4742-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)

