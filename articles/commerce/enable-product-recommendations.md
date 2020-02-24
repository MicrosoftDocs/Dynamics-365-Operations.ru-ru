---
title: Включить рекомендации по продуктам
description: В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024964"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="311b2-103">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="311b2-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="311b2-104">В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="311b2-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="311b2-105">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="311b2-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="311b2-106">Предварительная проверка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="311b2-106">Recommendations pre-check</span></span>

<span data-ttu-id="311b2-107">Перед включением обратите внимание, что рекомендации продуктов поддерживаются только для клиентов Commerce, перенесших свои хранилища с помощью Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="311b2-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="311b2-108">Инструкции по включению ADLS см. в разделе [Включение ADLS в среде Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="311b2-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="311b2-109">Кроме того, убедитесь, что измерения RetailSale включены.</span><span class="sxs-lookup"><span data-stu-id="311b2-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="311b2-110">Для получения дополнительных сведений об этом процессе настройки перейдите [сюда.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="311b2-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="311b2-111">Включение рекомендаций</span><span class="sxs-lookup"><span data-stu-id="311b2-111">Turn on recommendations</span></span>

<span data-ttu-id="311b2-112">Чтобы включить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="311b2-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="311b2-113">Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="311b2-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="311b2-114">В списке общих параметров выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="311b2-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="311b2-115">Для параметра **Включить рекомендации** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="311b2-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![включить рекомендации по продуктам](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="311b2-117">Эта процедура запускает процесс создания списков рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="311b2-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="311b2-118">До того, как списки будут доступны для просмотра на POS-терминале или в Dynamics 365 Commerce, может потребоваться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="311b2-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="311b2-119">Настройка параметров списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="311b2-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="311b2-120">По умолчанию список рекомендаций продуктов на основе AI-ML предоставляет предлагаемые значения.</span><span class="sxs-lookup"><span data-stu-id="311b2-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="311b2-121">Предлагаемые по умолчанию значения можно изменить в соответствии с потоком бизнеса.</span><span class="sxs-lookup"><span data-stu-id="311b2-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="311b2-122">Дополнительные сведения об изменении параметров по умолчанию см. в разделе [Управление результатами рекомендаций продуктов на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="311b2-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="311b2-123">Отображение рекомендаций на POS-устройствах</span><span class="sxs-lookup"><span data-stu-id="311b2-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="311b2-124">После включения рекомендаций в операционных отделах организации Commerce необходимо добавить панель рекомендаций на экран управления POS через инструмент макета.</span><span class="sxs-lookup"><span data-stu-id="311b2-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="311b2-125">Для получения сведений об этом процессе см. [Добавление элемента управления рекомендациями на экране проводки на устройствах POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="311b2-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="311b2-126">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="311b2-126">Enable personalized recommendations</span></span>

<span data-ttu-id="311b2-127">Дополнительные сведения о получении персонализированных рекомендаций см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="311b2-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="311b2-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="311b2-128">Additional resources</span></span>

[<span data-ttu-id="311b2-129">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="311b2-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="311b2-130">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="311b2-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="311b2-131">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="311b2-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="311b2-132">Добавление панели рекомендаций к POS-устройствам</span><span class="sxs-lookup"><span data-stu-id="311b2-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="311b2-133">Обзор модуля семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="311b2-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="311b2-134">Включение ADLS в среде Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="311b2-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

