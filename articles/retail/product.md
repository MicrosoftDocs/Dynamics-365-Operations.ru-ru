---
title: Рекомендации продуктов в POS
description: В этом разделе описывается использование рекомендаций продуктов на POS-терминале.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 98c84e987c40adf136d0240117f7b0f119bf2f59
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811125"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="f8e69-103">Рекомендации продуктов в POS</span><span class="sxs-lookup"><span data-stu-id="f8e69-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8e69-104">По своей сути, рекомендации продуктов представляют собой трансформируемое бизнес-приложение, охватывающее все сферы розничной торговли для создания богатого, привлекательного и специализированного процесса обнаружения продукции.</span><span class="sxs-lookup"><span data-stu-id="f8e69-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="f8e69-105">Чтобы реализовать эту функцию на POS-терминале, следуйте [указаниям по добавлению рекомендаций в POS-устройства](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="f8e69-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="f8e69-106">Дополнительные сведения о функциях рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](../commerce/product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="f8e69-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="f8e69-107">Сценарии</span><span class="sxs-lookup"><span data-stu-id="f8e69-107">Scenarios</span></span>

<span data-ttu-id="f8e69-108">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="f8e69-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="f8e69-109">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f8e69-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="f8e69-110">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="f8e69-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="f8e69-111">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, служба рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="f8e69-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="f8e69-112">[![Рекомендации на странице "Сведения о продукте"](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="f8e69-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="f8e69-113">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="f8e69-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="f8e69-114">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="f8e69-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8e69-115">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f8e69-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="f8e69-116">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="f8e69-117">[![Рекомендации на странице "Проводки"](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="f8e69-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="f8e69-118">Настройка Dynamics 365 Retail для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="f8e69-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="f8e69-119">Чтобы настроить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="f8e69-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="f8e69-120">Убедитесь, что ваша служба обновлена до **сборки 10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="f8e69-121">Следуйте инструкциям по [включению рекомендаций продуктов](../commerce/enable-product-recommendations.md) для вашего бизнеса.</span><span class="sxs-lookup"><span data-stu-id="f8e69-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="f8e69-122">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="f8e69-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="f8e69-123">Перейдите в **Параметры розничной торговли**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="f8e69-124">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="f8e69-125">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="f8e69-126">Устранение неполадок при наличии уже включенных рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="f8e69-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="f8e69-127">Откройте **Параметры Retail** \> **Списки рекомендаций** \> **Отключить рекомендации по продуктам** и выполните **Задание глобальной конфигурации \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="f8e69-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="f8e69-128">Если вы добавили **Элемент управления рекомендациями** на свой экран проводки с помощью **Конструктора макета экрана**, удалите также этот элемент.</span><span class="sxs-lookup"><span data-stu-id="f8e69-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="f8e69-129">При возникновении дополнительных вопросов ознакомьтесь с разделом [Вопросы и ответы по рекомендациям по продуктам](../commerce/faq-recommendations.md) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="f8e69-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8e69-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8e69-130">Additional resources</span></span>

[<span data-ttu-id="f8e69-131">Добавление элемента управления рекомендациями на экране проводки на устройствах POS</span><span class="sxs-lookup"><span data-stu-id="f8e69-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="f8e69-132">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="f8e69-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="f8e69-133">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="f8e69-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
