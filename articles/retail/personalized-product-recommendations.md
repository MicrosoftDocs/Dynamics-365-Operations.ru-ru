---
title: "Обзор персонализированных рекомендаций по продуктам"
description: "В Dynamics 365 for Retail рекомендации по продукции могут отображаться на устройстве POS. Рекомендации представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах. Для предприятий розничной торговли с большими каталогами рекомендации помогают клиентам узнать о продуктах. Демонстрируя продукты, соответствующие интересам и привычкам клиента, рекомендации по продуктам могут помочь предприятиям розничной торговли увеличить продажи и перекрестные продажи, а также повысить удержание клиента. В Dynamics 365 for Retail рекомендации по продукции строятся на основе интеллектуальных служб и машинного обучения Microsoft Azure."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 42ffb375d9786b2ac506d6ef06e9da9ee22652a6
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="299f8-107">Обзор персонализированных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="299f8-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="299f8-108">Эта функция в настоящее время доступна только в топологиях развертывания "песочница" и "рабочая среда" (с высокой доступностью).</span><span class="sxs-lookup"><span data-stu-id="299f8-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="299f8-109">В Dynamics 365 for Retail рекомендации по продукции могут отображаться на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="299f8-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="299f8-110">Рекомендации представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="299f8-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="299f8-111">Для предприятий розничной торговли с большими каталогами рекомендации помогают клиентам узнать о продуктах.</span><span class="sxs-lookup"><span data-stu-id="299f8-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="299f8-112">Демонстрируя продукты, соответствующие интересам и привычкам клиента, рекомендации по продуктам могут помочь предприятиям розничной торговли увеличить продажи и перекрестные продажи, а также повысить удержание клиента.</span><span class="sxs-lookup"><span data-stu-id="299f8-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="299f8-113">В Dynamics 365 for Retail рекомендации по продукции строятся на основе интеллектуальных служб и машинного обучения Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="299f8-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="299f8-114">Сценарии</span><span class="sxs-lookup"><span data-stu-id="299f8-114">Scenarios</span></span>
---------

<span data-ttu-id="299f8-115">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="299f8-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="299f8-116">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="299f8-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="299f8-117">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="299f8-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="299f8-118">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, механизм рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="299f8-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="299f8-119">Если сотрудник магазина добавляет клиента в проводку, а затем открывает странице **Сведения о продукте**, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента.</span><span class="sxs-lookup"><span data-stu-id="299f8-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="299f8-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="299f8-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="299f8-121">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="299f8-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="299f8-122">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="299f8-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="299f8-123">Если сотрудник магазина добавляет клиента в проводку, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента и списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="299f8-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="299f8-124">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="299f8-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="299f8-125">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="299f8-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="299f8-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="299f8-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="299f8-127">На странице **Сведения о клиенте**:</span><span class="sxs-lookup"><span data-stu-id="299f8-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="299f8-128">Механизм рекомендаций предлагает номенклатуры на основе кода пользователя и номенклатур в списке пожеланий клиента.</span><span class="sxs-lookup"><span data-stu-id="299f8-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="299f8-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="299f8-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="299f8-130">Настройка Dynamics 365 for Retail для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="299f8-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="299f8-131">Чтобы настроить рекомендации по продуктам, необходимо сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="299f8-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="299f8-132">Убедитесь, что выбрано правильное **Юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="299f8-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="299f8-133">Перейдите в **Хранилище объектов**, выберите **Розничные продажи** и нажмите кнопку **Обновить**. При этом будут взяты демонстрационные данные (или ваши данные) из вашей операционной базы данных и перемещены в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="299f8-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="299f8-134">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="299f8-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="299f8-135">Перейдите в **Параметры розничной торговли**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="299f8-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="299f8-136">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="299f8-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="299f8-137">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="299f8-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="299f8-138">[]()Как это работает?</span><span class="sxs-lookup"><span data-stu-id="299f8-138">[]()How does it work?</span></span>
<span data-ttu-id="299f8-139">При обновлении объекта **Хранилище объектов** выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="299f8-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="299f8-140">Данные в формате, требуемом службами Cognitive Services, извлекаются из операционной базы данных Dynamics 365 for Retail и отправляются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="299f8-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="299f8-141">Эти данные используются фабрикой данных Azure (ADF) для очистки данных с помощью скриптов Hive в рамках работы ADF.</span><span class="sxs-lookup"><span data-stu-id="299f8-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="299f8-142">Очищенные данные сохраняются в хранилище больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="299f8-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="299f8-143">Данные из хранилища больших двоичных объектов используются API Cognitive Services для обучения модели рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="299f8-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="299f8-144">При включении параметра **Включить рекомендации** и выполнении заданий конфигурации выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="299f8-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="299f8-145">Учетные данные и код модели получаются из API и сохраняются в операционной базе данных Dynamics 365 for Retail, в файле web.config для AOS, а также на сервере розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="299f8-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="299f8-146">Учетные данные и код модели становятся доступными для CRT, чтобы можно было обрабатывать вызовы рекомендаций по продуктам из Cloud POS и MPOS в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="299f8-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="299f8-147">См. также</span><span class="sxs-lookup"><span data-stu-id="299f8-147">See also</span></span>
--------

[<span data-ttu-id="299f8-148">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="299f8-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




