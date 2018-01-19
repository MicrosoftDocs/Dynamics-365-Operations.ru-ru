---
title: "Обзор персонализированных рекомендаций по продуктам"
description: "В этом разделе содержатся сведения о рекомендациях по продуктам в Dynamics 365 for Retail, которые могут отображаться на устройстве POS-терминала."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: fde7face188bbfd3bfdf66fbff81969f75704302
ms.contentlocale: ru-ru
ms.lasthandoff: 01/19/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="fbddf-103">Обзор персонализированных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="fbddf-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="fbddf-104">Эта функция в настоящее время доступна только в топологиях развертывания "песочница" и "рабочая среда" (с высокой доступностью).</span><span class="sxs-lookup"><span data-stu-id="fbddf-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="fbddf-105">В Dynamics 365 for Retail рекомендации по продукции могут отображаться на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="fbddf-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="fbddf-106">Рекомендации представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="fbddf-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="fbddf-107">Для предприятий розничной торговли с большими каталогами рекомендации помогают клиентам узнать о продуктах.</span><span class="sxs-lookup"><span data-stu-id="fbddf-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="fbddf-108">Демонстрируя продукты, соответствующие интересам и привычкам клиента, рекомендации по продуктам могут помочь предприятиям розничной торговли увеличить продажи и перекрестные продажи, а также повысить удержание клиента.</span><span class="sxs-lookup"><span data-stu-id="fbddf-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="fbddf-109">В Dynamics 365 for Retail рекомендации по продукции строятся на основе интеллектуальных служб и машинного обучения Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbddf-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="fbddf-110">Сценарии</span><span class="sxs-lookup"><span data-stu-id="fbddf-110">Scenarios</span></span>
---------

<span data-ttu-id="fbddf-111">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="fbddf-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="fbddf-112">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="fbddf-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="fbddf-113">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="fbddf-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="fbddf-114">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, механизм рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="fbddf-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="fbddf-115">Если сотрудник магазина добавляет клиента в проводку, а затем открывает странице **Сведения о продукте**, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента.</span><span class="sxs-lookup"><span data-stu-id="fbddf-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="fbddf-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="fbddf-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="fbddf-117">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="fbddf-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="fbddf-118">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="fbddf-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="fbddf-119">Если сотрудник магазина добавляет клиента в проводку, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента и списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="fbddf-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="fbddf-120">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="fbddf-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="fbddf-121">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="fbddf-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="fbddf-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="fbddf-123">На странице **Сведения о клиенте**:</span><span class="sxs-lookup"><span data-stu-id="fbddf-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="fbddf-124">Механизм рекомендаций предлагает номенклатуры на основе кода пользователя и номенклатур в списке пожеланий клиента.</span><span class="sxs-lookup"><span data-stu-id="fbddf-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="fbddf-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="fbddf-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="fbddf-126">Настройка Dynamics 365 for Retail для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="fbddf-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="fbddf-127">Чтобы настроить рекомендации по продуктам, необходимо сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="fbddf-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="fbddf-128">Убедитесь, что выбрано правильное **Юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="fbddf-129">Перейдите в **Хранилище объектов**, выберите **Розничные продажи**, затем щелкните **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="fbddf-130">При этом используются демонстрационные данные (или ваши данные) из операционной базы данных, которые перемещаются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="fbddf-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="fbddf-131">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="fbddf-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="fbddf-132">Перейдите в **Параметры розничной торговли**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="fbddf-133">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="fbddf-134">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="fbddf-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="fbddf-135">[]()Как это работает?</span><span class="sxs-lookup"><span data-stu-id="fbddf-135">[]()How does it work?</span></span>
<span data-ttu-id="fbddf-136">При обновлении объекта **Хранилище объектов** выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fbddf-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="fbddf-137">Данные в формате, требуемом службами Cognitive Services, извлекаются из операционной базы данных Dynamics 365 for Retail и отправляются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="fbddf-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="fbddf-138">Эти данные используются фабрикой данных Azure (ADF) для очистки данных с помощью скриптов Hive в рамках работы ADF.</span><span class="sxs-lookup"><span data-stu-id="fbddf-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="fbddf-139">Очищенные данные сохраняются в хранилище больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="fbddf-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="fbddf-140">Данные из хранилища больших двоичных объектов используются API Cognitive Services для обучения модели рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="fbddf-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="fbddf-141">При включении параметра **Включить рекомендации** и выполнении заданий конфигурации выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fbddf-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="fbddf-142">Учетные данные и код модели получаются из API и сохраняются в операционной базе данных Dynamics 365 for Retail, в файле web.config для AOS, а также на сервере розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="fbddf-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="fbddf-143">Учетные данные и код модели становятся доступными для CRT, чтобы можно было обрабатывать вызовы рекомендаций по продуктам из Cloud POS и MPOS в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="fbddf-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="fbddf-144">См. также</span><span class="sxs-lookup"><span data-stu-id="fbddf-144">See also</span></span>
--------

[<span data-ttu-id="fbddf-145">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="fbddf-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




