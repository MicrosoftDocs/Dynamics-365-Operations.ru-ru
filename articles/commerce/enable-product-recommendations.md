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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770147"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="52d5d-103">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="52d5d-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="52d5d-104">В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="52d5d-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="52d5d-105">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="52d5d-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="52d5d-106">Предварительная проверка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="52d5d-106">Recommendations pre-check</span></span>
<span data-ttu-id="52d5d-107">Перед включением обратите внимание, что рекомендации продуктов поддерживаются только для клиентов F&O, поддерживающих сборку 10.0.6 и перенесших свои хранилища с помощью BDL.</span><span class="sxs-lookup"><span data-stu-id="52d5d-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="52d5d-108">Кроме того, убедитесь, что измерения RetailSale включены.</span><span class="sxs-lookup"><span data-stu-id="52d5d-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="52d5d-109">Для получения дополнительных сведений об этом процессе настройки перейдите [сюда.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="52d5d-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="52d5d-110">Включение рекомендаций</span><span class="sxs-lookup"><span data-stu-id="52d5d-110">Turn on recommendations</span></span>

<span data-ttu-id="52d5d-111">Чтобы включить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="52d5d-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="52d5d-112">Выберите **Retail** &gt; **Рекомендации продуктов** &gt; **Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="52d5d-113">В списке общих параметров Retail выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="52d5d-114">Для параметра **Включить рекомендации** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="52d5d-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![включить рекомендации по продуктам](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="52d5d-116">Эта процедура запускает процесс создания списков рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="52d5d-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="52d5d-117">До того, как списки будут доступны для просмотра на POS-терминале или в Dynamics 365 for Commerce, может потребоваться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="52d5d-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="52d5d-118">Настройка параметров списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="52d5d-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="52d5d-119">По умолчанию список рекомендаций продуктов на основе AI-ML предоставляет предлагаемые значения.</span><span class="sxs-lookup"><span data-stu-id="52d5d-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="52d5d-120">Предлагаемые по умолчанию значения можно изменить в соответствии с потоком бизнеса.</span><span class="sxs-lookup"><span data-stu-id="52d5d-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="52d5d-121">Дополнительные сведения об изменении параметров по умолчанию см. в разделе [Управление результатами рекомендаций продуктов на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="52d5d-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="52d5d-122">Отображение рекомендаций на POS-устройствах</span><span class="sxs-lookup"><span data-stu-id="52d5d-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="52d5d-123">После включения рекомендаций в серверной части необходимо добавить панель рекомендаций на экран управления POS через инструмент макета.</span><span class="sxs-lookup"><span data-stu-id="52d5d-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="52d5d-124">Для получения сведений об этом процессе настройки перейдите [сюда.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="52d5d-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="52d5d-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="52d5d-125">Additional resources</span></span>

[<span data-ttu-id="52d5d-126">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="52d5d-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="52d5d-127">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="52d5d-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="52d5d-128">Добавление панели рекомендаций к POS-устройствам</span><span class="sxs-lookup"><span data-stu-id="52d5d-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


