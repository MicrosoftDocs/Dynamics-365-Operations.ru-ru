---
title: Добавление рекомендаций по продуктам в POS
description: В этом разделе описывается использование рекомендаций продуктов на POS-терминале.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fabf08e8dde1b9b6d27af3e42d3aaff904b467b0
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454541"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="3dcf2-103">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="3dcf2-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3dcf2-104">По своей сути, рекомендации продуктов представляют собой трансформируемое бизнес-приложение, охватывающее все сферы коммерции для создания богатого, привлекательного и специализированного процесса обнаружения продукции.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="3dcf2-105">Чтобы реализовать эту функцию на POS-терминале, следуйте [указаниям по добавлению рекомендаций в POS-устройства](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="3dcf2-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="3dcf2-106">Дополнительные сведения о функциях рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](../commerce/product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3dcf2-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="3dcf2-107">Сценарии</span><span class="sxs-lookup"><span data-stu-id="3dcf2-107">Scenarios</span></span>

<span data-ttu-id="3dcf2-108">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="3dcf2-109">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="3dcf2-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="3dcf2-110">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="3dcf2-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="3dcf2-111">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, служба рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="3dcf2-112">[![Рекомендации на странице "Сведения о продукте"](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="3dcf2-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="3dcf2-113">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="3dcf2-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="3dcf2-114">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3dcf2-115">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3dcf2-116">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="3dcf2-117">[![Рекомендации на странице "Проводки"](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="3dcf2-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="3dcf2-118">Настройка Commerce для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="3dcf2-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="3dcf2-119">Чтобы настроить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="3dcf2-120">Убедитесь, что ваша служба обновлена до **сборки 10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="3dcf2-121">Следуйте инструкциям по [включению рекомендаций продуктов](../commerce/enable-product-recommendations.md) для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="3dcf2-122">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="3dcf2-123">Перейдите в **Параметры Commerce**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="3dcf2-124">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="3dcf2-125">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="3dcf2-126">Устранение неполадок при наличии уже включенных рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="3dcf2-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="3dcf2-127">Откройте **Параметры Commerce** \> **Списки рекомендаций** \> **Отключить рекомендации по продуктам** и выполните **Задание глобальной конфигурации \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="3dcf2-128">Если вы добавили **Элемент управления рекомендациями** на свой экран проводки с помощью **Конструктора макета экрана**, удалите также этот элемент.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="3dcf2-129">При возникновении дополнительных вопросов ознакомьтесь с разделом [Вопросы и ответы по рекомендациям по продуктам](../commerce/faq-recommendations.md) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="3dcf2-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3dcf2-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3dcf2-130">Additional resources</span></span>

[<span data-ttu-id="3dcf2-131">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="3dcf2-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3dcf2-132">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3dcf2-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3dcf2-133">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="3dcf2-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3dcf2-134">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="3dcf2-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3dcf2-135">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="3dcf2-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3dcf2-136">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="3dcf2-136">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3dcf2-137">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="3dcf2-137">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3dcf2-138">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="3dcf2-138">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3dcf2-139">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="3dcf2-139">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3dcf2-140">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="3dcf2-140">Product recommendations FAQ</span></span>](faq-recommendations.md)
