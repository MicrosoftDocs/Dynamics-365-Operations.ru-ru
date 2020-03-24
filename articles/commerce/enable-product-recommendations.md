---
title: Включить рекомендации по продуктам
description: В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127890"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="d3636-103">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="d3636-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d3636-104">В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3636-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="d3636-105">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="d3636-106">Предварительная проверка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-106">Recommendations pre-check</span></span>

<span data-ttu-id="d3636-107">Перед включением обратите внимание, что рекомендации продуктов поддерживаются только для клиентов Commerce, перенесших свои хранилища с помощью Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="d3636-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="d3636-108">Инструкции по включению ADLS см. в разделе [Включение ADLS в среде Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="d3636-109">Кроме того, убедитесь, что измерения RetailSale включены.</span><span class="sxs-lookup"><span data-stu-id="d3636-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="d3636-110">Для получения дополнительных сведений об этом процессе настройки перейдите [сюда.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="d3636-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="d3636-111">Включение рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-111">Turn on recommendations</span></span>

<span data-ttu-id="d3636-112">Чтобы включить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="d3636-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="d3636-113">Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="d3636-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="d3636-114">В списке общих параметров выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="d3636-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="d3636-115">Для параметра **Включить рекомендации** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d3636-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![включить рекомендации по продуктам](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="d3636-117">Эта процедура запускает процесс создания списков рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="d3636-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="d3636-118">До того, как списки будут доступны для просмотра на POS-терминале или в Dynamics 365 Commerce, может потребоваться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="d3636-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="d3636-119">Настройка параметров списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="d3636-120">По умолчанию список рекомендаций продуктов на основе AI-ML предоставляет предлагаемые значения.</span><span class="sxs-lookup"><span data-stu-id="d3636-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="d3636-121">Предлагаемые по умолчанию значения можно изменить в соответствии с потоком бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d3636-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="d3636-122">Дополнительные сведения об изменении параметров по умолчанию см. в разделе [Управление результатами рекомендаций продуктов на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="d3636-123">Отображение рекомендаций на POS-устройствах</span><span class="sxs-lookup"><span data-stu-id="d3636-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="d3636-124">После включения рекомендаций в операционных отделах организации Commerce необходимо добавить панель рекомендаций на экран управления POS через инструмент макета.</span><span class="sxs-lookup"><span data-stu-id="d3636-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="d3636-125">Для получения сведений об этом процессе см. [Добавление элемента управления рекомендациями на экране проводки на устройствах POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="d3636-126">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-126">Enable personalized recommendations</span></span>

<span data-ttu-id="d3636-127">Дополнительные сведения о получении персонализированных рекомендаций см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3636-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3636-128">Additional resources</span></span>

[<span data-ttu-id="d3636-129">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="d3636-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d3636-130">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d3636-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d3636-131">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d3636-132">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d3636-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d3636-133">Добавление списков рекомендаций на сайт электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="d3636-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d3636-134">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="d3636-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d3636-135">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="d3636-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d3636-136">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="d3636-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d3636-137">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="d3636-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d3636-138">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="d3636-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d3636-139">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="d3636-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

