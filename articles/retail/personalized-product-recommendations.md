---
title: "Персональные рекомендаций по продуктам"
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
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d6706cbb7630aeb230bc9eb1c187397897c9de68
ms.contentlocale: ru-ru
ms.lasthandoff: 01/04/2019

---

# <a name="personalized-product-recommendations"></a><span data-ttu-id="f2b7f-103">Персональные рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="f2b7f-103">Personalized product recommendations</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f2b7f-104">Мы удаляем текущую версию службы рекомендации продуктов, так как мы переработали эту функцию с использованием более эффективного алгоритма и новыми возможностями, предназначенными для розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="f2b7f-105">Подробнее см. в разделе [Удаленные или устаревшие функции](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="f2b7f-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

<span data-ttu-id="f2b7f-106">В Dynamics 365 for Retail рекомендации по продукции могут отображаться на устройстве POS.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="f2b7f-107">Рекомендации представляют собой номенклатуры, в которых ваш клиент может быть заинтересован на основе его истории покупок, номенклатур в списке планируемых покупок и номенклатур, приобретенных другими клиентами в Интернете и в физических магазинах.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="f2b7f-108">Для предприятий розничной торговли с большими каталогами рекомендации помогают клиентам узнать о продуктах.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="f2b7f-109">Демонстрируя продукты, соответствующие интересам и привычкам клиента, рекомендации по продуктам могут помочь предприятиям розничной торговли увеличить продажи и перекрестные продажи, а также повысить удержание клиента.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-109">By showcasing products targeted to a customer's interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="f2b7f-110">В Dynamics 365 for Retail рекомендации по продукции строятся на основе интеллектуальных служб и машинного обучения Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

## <a name="scenarios"></a><span data-ttu-id="f2b7f-111">Сценарии</span><span class="sxs-lookup"><span data-stu-id="f2b7f-111">Scenarios</span></span>

<span data-ttu-id="f2b7f-112">Рекомендации по продукции включены в следующих сценариях POS.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="f2b7f-113">Они доступны в Cloud POS или Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f2b7f-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="f2b7f-114">На странице **Сведения о продукте**:</span><span class="sxs-lookup"><span data-stu-id="f2b7f-114">On the **Product details** page:</span></span>

    - <span data-ttu-id="f2b7f-115">Если сотрудник магазина открывает страницу **Сведения о продукте** при просмотре предыдущих проводок в разных каналах, механизм рекомендаций предлагает дополнительные номенклатуры, которые часто приобретаются вместе.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
    - <span data-ttu-id="f2b7f-116">Если сотрудник магазина добавляет клиента в проводку, а затем открывает странице **Сведения о продукте**, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

    <span data-ttu-id="f2b7f-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="f2b7f-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="f2b7f-118">На странице **Проводка**:</span><span class="sxs-lookup"><span data-stu-id="f2b7f-118">On the **Transaction** page:</span></span>

    - <span data-ttu-id="f2b7f-119">Механизм рекомендаций предлагает номенклатуры на основе всего списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
    - <span data-ttu-id="f2b7f-120">Если сотрудник магазина добавляет клиента в проводку, механизм рекомендаций предоставляет персональные рекомендации с помощью истории проводок клиента и списка номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer's transaction history and the list of items in the basket.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2b7f-121">Для отображения рекомендаций на странице **Проводка** предприятие розничной торговли должно обновить макет экрана в Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="f2b7f-122">Элемент управления **Рекомендации** необходимо перетащить на страницу **Проводка**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span>

    <span data-ttu-id="f2b7f-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="f2b7f-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3. <span data-ttu-id="f2b7f-124">На странице **Сведения о клиенте**:</span><span class="sxs-lookup"><span data-stu-id="f2b7f-124">On the **Customer details** page:</span></span>

    - <span data-ttu-id="f2b7f-125">Механизм рекомендаций предлагает номенклатуры на основе кода пользователя и номенклатур в списке пожеланий клиента.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-125">The recommendation engine suggests items based on the user ID and items in the customer's wish list.</span></span>

    <span data-ttu-id="f2b7f-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="f2b7f-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="f2b7f-127">Настройка Dynamics 365 for Retail для включения рекомендаций POS</span><span class="sxs-lookup"><span data-stu-id="f2b7f-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>

<span data-ttu-id="f2b7f-128">Чтобы настроить рекомендации по продуктам, необходимо сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-128">To set up product recommendations, you need to do the following.</span></span>

1. <span data-ttu-id="f2b7f-129">Убедитесь, что выбрано правильное **Юридическое лицо**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2. <span data-ttu-id="f2b7f-130">Перейдите в **Хранилище объектов**, выберите **Розничные продажи**, затем щелкните **Обновить**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="f2b7f-131">При этом используются демонстрационные данные (или ваши данные) из операционной базы данных, которые перемещаются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3. <span data-ttu-id="f2b7f-132">Необязательно: чтобы отобразить рекомендации на экране проводки, перейдите в раздел **Макет экрана**, выберите макет экрана, запустите **Конструктор макета экрана**, а затем перетащите элемент управления **рекомендации** в требуемое место.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="f2b7f-133">Перейдите в **Параметры розничной торговли**, выберите **Машинное обучение**, выберите **Да** в разделе **Включить рекомендации POS**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="f2b7f-134">Чтобы видеть рекомендации на POS-терминале, запустите задание глобальной конфигурации **1110**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="f2b7f-135">Для отражения изменений, внесенных в конструкторе макета экрана POS, запустите задание конфигурации канала **1070**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="f2b7f-136">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="f2b7f-136">How does it work?</span></span>

<span data-ttu-id="f2b7f-137">При обновлении объекта **Хранилище объектов** выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

- <span data-ttu-id="f2b7f-138">Данные в формате, требуемом службами Cognitive Services, извлекаются из операционной базы данных Dynamics 365 for Retail и отправляются в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="f2b7f-139">Эти данные используются фабрикой данных Azure (ADF) для очистки данных с помощью скриптов Hive в рамках работы ADF.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="f2b7f-140">Очищенные данные сохраняются в хранилище больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-140">Cleansed data is stored in blob storage.</span></span>
- <span data-ttu-id="f2b7f-141">Данные из хранилища больших двоичных объектов используются API Cognitive Services для обучения модели рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="f2b7f-142">При включении параметра **Включить рекомендации** и выполнении заданий конфигурации выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

- <span data-ttu-id="f2b7f-143">Учетные данные и код модели получаются из API и сохраняются в операционной базе данных Dynamics 365 for Retail, в файле web.config для AOS, а также на сервере розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
- <span data-ttu-id="f2b7f-144">Учетные данные и код модели становятся доступными для CRT, чтобы можно было обрабатывать вызовы рекомендаций по продуктам из Cloud POS и MPOS в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="f2b7f-145">Устранение неполадок при наличии уже включенных рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="f2b7f-145">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="f2b7f-146">Откройте **Параметры Retail** \> **Машинное обучение** \> **Отключить рекомендации по продуктам** и выполните **Задание глобальной конфигурации \[1110\]**.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-146">Navigate to **Retail Parameters** \> **Machine learning** \> **Disable product recommendations** and run **Global configuration job \[1110\]**.</span></span> <span data-ttu-id="f2b7f-147">Если не удается найти вкладку **Машинное обучение**, обратитесь в службу поддержки Dynamics.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-147">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span>
- <span data-ttu-id="f2b7f-148">Если вы добавили **Элемент управления рекомендациями** на свой экран проводки с помощью **Конструктора макета экрана**, удалите также этот элемент.</span><span class="sxs-lookup"><span data-stu-id="f2b7f-148">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2b7f-149">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2b7f-149">Additional resources</span></span>

[<span data-ttu-id="f2b7f-150">Добавление элемента управления рекомендациями на странице проводки на устройстве POS</span><span class="sxs-lookup"><span data-stu-id="f2b7f-150">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)

