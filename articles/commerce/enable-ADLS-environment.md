---
title: Включение Azure Data Lake Storage в среде Dynamics 365 Commerce
description: В этой теме объясняется, как включить и проверить Azure Data Lake Storage для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 83b829306c2da2d10924e547fd3cac6ae6781db3
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404194"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="835ce-103">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="835ce-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="835ce-104">В этой теме объясняется, как включить и проверить Azure Data Lake Storage для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.</span><span class="sxs-lookup"><span data-stu-id="835ce-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="835ce-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="835ce-105">Overview</span></span>

<span data-ttu-id="835ce-106">В решении Dynamics 365 Commerce все сведения о продуктах и проводках отслеживаются в хранилище объектов среды.</span><span class="sxs-lookup"><span data-stu-id="835ce-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="835ce-107">Чтобы сделать эти данные доступными другим службам Dynamics 365, таким как анализ данных, бизнес-аналитика и персонализированные рекомендации, необходимо подключить среду к принадлежащему заказчику решению Azure Data Lake Storage Gen 2.</span><span class="sxs-lookup"><span data-stu-id="835ce-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="835ce-108">После настройки Azure Data Lake Storage в среде все необходимые данные будут зеркально отражены из хранилища объектов, а также защищены и будут управляться клиентом.</span><span class="sxs-lookup"><span data-stu-id="835ce-108">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="835ce-109">Если в среде также включены рекомендации по продукту или персонализированные рекомендации, то в стеке рекомендаций по продукту будет предоставлен доступ к выделенной папке в Azure Data Lake Storage, чтобы извлечь данные клиента и вычислить рекомендации на их основе.</span><span class="sxs-lookup"><span data-stu-id="835ce-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="835ce-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="835ce-110">Prerequisites</span></span>

<span data-ttu-id="835ce-111">У клиентов должны быть настроены Azure Data Lake Storage в подписке Azure, которая им принадлежит.</span><span class="sxs-lookup"><span data-stu-id="835ce-111">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="835ce-112">Этот раздел не охватывает покупку подписки Azure или настройки учетной записи хранения с Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="835ce-112">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="835ce-113">Дополнительные сведения о Azure Data Lake Storage см. в разделе [Официальная документация по Azure Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="835ce-113">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="835ce-114">Шаги конфигурации</span><span class="sxs-lookup"><span data-stu-id="835ce-114">Configuration steps</span></span>

<span data-ttu-id="835ce-115">В этом разделе описываются этапы настройки, необходимые для включения Azure Data Lake Storage в среде в соответствии с рекомендациями по продуктам.</span><span class="sxs-lookup"><span data-stu-id="835ce-115">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="835ce-116">Более подробное описание шагов, необходимых для включения Azure Data Lake Storage, см. в разделе [Предоставление хранилища объектов как Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="835ce-116">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="835ce-117">Включение Azure Data Lake Storage в среде</span><span class="sxs-lookup"><span data-stu-id="835ce-117">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="835ce-118">Выполните вход на портал операционных отделов организации для среды.</span><span class="sxs-lookup"><span data-stu-id="835ce-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="835ce-119">Выполните поиск **Системные параметры** и перейдите на вкладку **Подключения данных**.</span><span class="sxs-lookup"><span data-stu-id="835ce-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="835ce-120">Установите для **Разрешить интеграцию с Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="835ce-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="835ce-121">Установите для **Постепенное обновление Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="835ce-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="835ce-122">Затем введите следующие необходимые сведения:</span><span class="sxs-lookup"><span data-stu-id="835ce-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="835ce-123">**Код приложения** // **Секретный ключ приложения** // **DNS-имя** — требуется для подключения к KeyVault, где хранится секретный ключ Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="835ce-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="835ce-124">**Имя секрета — имя секрета**, хранящееся в KeyVault и используемое для аутентификации в Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="835ce-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="835ce-125">Сохраните изменения в левом верхнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="835ce-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="835ce-126">На следующем рисунке показан пример конфигурации Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="835ce-126">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Пример конфигурации Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="835ce-128">Проверка подключения Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="835ce-128">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="835ce-129">Проверьте подключение к KeyVault с помощью ссылки **Проверка Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="835ce-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="835ce-130">Проверьте подключение к Azure Data Lake Storage с помощью ссылки **Проверка хранилища Azure**.</span><span class="sxs-lookup"><span data-stu-id="835ce-130">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="835ce-131">Если проверка завершилась неудачно, проверьте правильность всех добавленных данных KeyVault, а затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="835ce-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="835ce-132">После успешного выполнения проверки подключения необходимо включить автоматическое обновление для хранилища объектов.</span><span class="sxs-lookup"><span data-stu-id="835ce-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="835ce-133">Чтобы включить автоматическое обновление хранилища объектов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="835ce-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="835ce-134">Найдите **Хранилище объектов**.</span><span class="sxs-lookup"><span data-stu-id="835ce-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="835ce-135">В списке слева перейдите к записи **RetailSales** и выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="835ce-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="835ce-136">Убедитесь, что для **Автоматическое обновление включено** выбрано значение **Да**, выберите **Обновить**, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="835ce-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="835ce-137">На следующем рисунке показан пример хранилища объектов с включенным автоматическим обновлением.</span><span class="sxs-lookup"><span data-stu-id="835ce-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Пример хранилища объектов с включенным автоматическим обновлением](./media/exampleADLSConfig2.png)

<span data-ttu-id="835ce-139">Теперь Azure Data Lake Storage настроено для среды.</span><span class="sxs-lookup"><span data-stu-id="835ce-139">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="835ce-140">Если это еще не было выполнено, выполните шаги, необходимые для [включения рекомендаций по продукту и персонализации](enable-product-recommendations.md) для среды.</span><span class="sxs-lookup"><span data-stu-id="835ce-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="835ce-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="835ce-141">Additional resources</span></span>

[<span data-ttu-id="835ce-142">Предоставление хранилища объектов как Data Lake</span><span class="sxs-lookup"><span data-stu-id="835ce-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="835ce-143">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="835ce-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="835ce-144">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="835ce-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="835ce-145">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="835ce-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="835ce-146">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="835ce-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="835ce-147">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="835ce-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="835ce-148">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="835ce-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="835ce-149">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="835ce-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="835ce-150">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="835ce-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="835ce-151">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="835ce-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="835ce-152">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="835ce-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
