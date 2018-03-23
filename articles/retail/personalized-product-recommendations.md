---
title: "Обзор персонализированных рекомендаций по продуктам"
description: "В этом разделе содержатся сведения о рекомендациях по продуктам в Dynamics 365 for Retail, которые могут отображаться на устройстве POS-терминала."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.sourcegitcommit: c5b9ee57b0b855766628caca239059205c103b86
ms.openlocfilehash: 4a0586324dddc10d64ad6760222f2540f31d6bce
ms.contentlocale: ru-ru
ms.lasthandoff: 03/08/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="979cd-103">Обзор персонализированных рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="979cd-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="979cd-104">Мы удаляем текущую версию службы рекомендации продуктов, так как мы переработали эту функцию с использованием более эффективного алгоритма и новыми возможностями, предназначенными для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="979cd-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="979cd-105">Подробнее см. в разделе [Удаленные или устаревшие функции](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="979cd-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> <span data-ttu-id="979cd-106">Перейдите в конец страницы, если вы сталкиваетесь с проблемами, связанными с уже включенными рекомендациями по продуктам для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="979cd-106">Navigate to the bottom of the page if you are facing issues with already-enabled product recommendations for your environment.</span></span> 

<span data-ttu-id="979cd-107">В Dynamics 365 for Retail рекомендации по продукции могут отображаться на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="979cd-107">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="979cd-108">Рекомендации представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="979cd-108">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="979cd-109">Для предприятий розничной торговли с большими каталогами рекомендации помогают клиентам узнать о продуктах.</span><span class="sxs-lookup"><span data-stu-id="979cd-109">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="979cd-110">Демонстрируя продукты, соответствующие интересам и привычкам клиента, рекомендации по продуктам могут помочь предприятиям розничной торговли увеличить продажи и перекрестные продажи, а также повысить удержание клиента.</span><span class="sxs-lookup"><span data-stu-id="979cd-110">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="979cd-111">В Dynamics 365 for Retail рекомендации по продукции строятся на основе интеллектуальных служб и машинного обучения Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="979cd-111">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="979cd-112">Сценарии</span><span class="sxs-lookup"><span data-stu-id="979cd-112">Scenarios</span></span>
---------

<span data-ttu-id="979cd-113">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="979cd-113">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="979cd-114">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="979cd-114">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="979cd-115">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="979cd-115">On the **Product details** page:</span></span>

-   <span data-ttu-id="979cd-116">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, механизм рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="979cd-116">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="979cd-117">Если сотрудник магазина добавляет клиента в проводку, а затем открывает странице **Сведения о продукте**, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента.</span><span class="sxs-lookup"><span data-stu-id="979cd-117">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="979cd-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="979cd-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="979cd-119">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="979cd-119">On the **Transaction** page:</span></span>

-   <span data-ttu-id="979cd-120">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="979cd-120">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="979cd-121">Если сотрудник магазина добавляет клиента в проводку, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента и списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="979cd-121">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="979cd-122">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="979cd-122">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="979cd-123">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="979cd-123">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="979cd-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="979cd-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="979cd-125">На странице **Сведения о клиенте**:</span><span class="sxs-lookup"><span data-stu-id="979cd-125">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="979cd-126">Механизм рекомендаций предлагает номенклатуры на основе кода пользователя и номенклатур в списке пожеланий клиента.</span><span class="sxs-lookup"><span data-stu-id="979cd-126">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="979cd-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="979cd-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="979cd-128">Настройка Dynamics 365 for Retail для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="979cd-128">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="979cd-129">Чтобы настроить рекомендации по продуктам, необходимо сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="979cd-129">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="979cd-130">Убедитесь, что выбрано правильное **Юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="979cd-130">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="979cd-131">Перейдите в **Хранилище объектов**, выберите **Розничные продажи**, затем щелкните **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="979cd-131">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="979cd-132">При этом используются демонстрационные данные (или ваши данные) из операционной базы данных, которые перемещаются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="979cd-132">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="979cd-133">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="979cd-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="979cd-134">Перейдите в **Параметры розничной торговли**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="979cd-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="979cd-135">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="979cd-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="979cd-136">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="979cd-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="979cd-137">[]()Как это работает?</span><span class="sxs-lookup"><span data-stu-id="979cd-137">[]()How does it work?</span></span>
<span data-ttu-id="979cd-138">При обновлении объекта **Хранилище объектов** выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="979cd-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="979cd-139">Данные в формате, требуемом службами Cognitive Services, извлекаются из операционной базы данных Dynamics 365 for Retail и отправляются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="979cd-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="979cd-140">Эти данные используются фабрикой данных Azure (ADF) для очистки данных с помощью скриптов Hive в рамках работы ADF.</span><span class="sxs-lookup"><span data-stu-id="979cd-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="979cd-141">Очищенные данные сохраняются в хранилище больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="979cd-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="979cd-142">Данные из хранилища больших двоичных объектов используются API Cognitive Services для обучения модели рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="979cd-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="979cd-143">При включении параметра **Включить рекомендации** и выполнении заданий конфигурации выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="979cd-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="979cd-144">Учетные данные и код модели получаются из API и сохраняются в операционной базе данных Dynamics 365 for Retail, в файле web.config для AOS, а также на сервере розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="979cd-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="979cd-145">Учетные данные и код модели становятся доступными для CRT, чтобы можно было обрабатывать вызовы рекомендаций по продуктам из Cloud POS и MPOS в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="979cd-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="979cd-146">Устранение неполадок при наличии уже включенных рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="979cd-146">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
>- <span data-ttu-id="979cd-147">Откройте **Параметры Retail** > **Машинное обучение** > **Отключить рекомендации по продуктам** и выполните **Задание глобальной конфигурации [1110]**.</span><span class="sxs-lookup"><span data-stu-id="979cd-147">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="979cd-148">Если не удается найти вкладку **Машинное обучение**, обратитесь в службу поддержки Dynamics.</span><span class="sxs-lookup"><span data-stu-id="979cd-148">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 

>- <span data-ttu-id="979cd-149">Если вы добавили **Элемент управления рекомендациями** на свой экран проводки с помощью **Конструктора макета экрана**, удалите также этот элемент.</span><span class="sxs-lookup"><span data-stu-id="979cd-149">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="see-also"></a><span data-ttu-id="979cd-150">См. также</span><span class="sxs-lookup"><span data-stu-id="979cd-150">See also</span></span>
--------

[<span data-ttu-id="979cd-151">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="979cd-151">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




