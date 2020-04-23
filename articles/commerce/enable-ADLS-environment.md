---
title: Включение ADLS в среде Dynamics 365 Commerce
description: В этой теме объясняется, как включить и проверить Azure Data Lake Storage (ADLS) для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.
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
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259756"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="d9e8e-103">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d9e8e-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9e8e-104">В этой теме объясняется, как включить и проверить Azure Data Lake Storage (ADLS) для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="d9e8e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d9e8e-105">Overview</span></span>

<span data-ttu-id="d9e8e-106">В решении Dynamics 365 Commerce все сведения о продуктах и проводках отслеживаются в хранилище объектов среды.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="d9e8e-107">Чтобы сделать эти данные доступными другим службам Dynamics 365, таким как анализ данных, бизнес-аналитика и персонализированные рекомендации, необходимо подключить среду к принадлежащему заказчику решению Azure Data Lake Storage Gen 2 (ADLS).</span><span class="sxs-lookup"><span data-stu-id="d9e8e-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="d9e8e-108">После настройки ADLS в среде все необходимые данные будут зеркально отражены из хранилища объектов, а также защищены и будут управляться клиентом.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="d9e8e-109">Если в среде также включены рекомендации по продукту или персонализированные рекомендации, то в стеке рекомендаций по продукту будет предоставлен доступ к выделенной папке в ADLS, чтобы извлечь данные клиента и вычислить рекомендации на их основе.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9e8e-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d9e8e-110">Prerequisites</span></span>

<span data-ttu-id="d9e8e-111">У клиентов должны быть настроены ADLS в подписке Azure, которая им принадлежит.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="d9e8e-112">Этот раздел не охватывает покупку подписки Azure или настройки учетной записи хранения с ADLS.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="d9e8e-113">Дополнительные сведения о ADLS см. в разделе [Официальная документация по ADLS](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="d9e8e-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="d9e8e-114">Шаги конфигурации</span><span class="sxs-lookup"><span data-stu-id="d9e8e-114">Configuration steps</span></span>

<span data-ttu-id="d9e8e-115">В этом разделе описываются этапы настройки, необходимые для включения ADLS в среде в соответствии с рекомендациями по продуктам.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-115">This section covers the configuration steps necessary for enabling ADLS in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="d9e8e-116">Более подробное описание шагов, необходимых для включения ADLS, см. в разделе [Предоставление хранилища объектов как Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="d9e8e-116">For a more in-depth overview of the steps required to enable ADLS, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="d9e8e-117">Включение ADLS в среде</span><span class="sxs-lookup"><span data-stu-id="d9e8e-117">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="d9e8e-118">Выполните вход на портал операционных отделов организации для среды.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="d9e8e-119">Выполните поиск **Системные параметры** и перейдите на вкладку **Подключения данных**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="d9e8e-120">Установите для **Разрешить интеграцию с Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="d9e8e-121">Установите для **Постепенное обновление Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="d9e8e-122">Затем введите следующие необходимые сведения:</span><span class="sxs-lookup"><span data-stu-id="d9e8e-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="d9e8e-123">**Код приложения** // **Секретный ключ приложения** // **DNS-имя** — требуется для подключения к KeyVault, где хранится секретный ключ ADLS.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="d9e8e-124">**Имя секрета** — имя секрета, хранящееся в KeyVault и используемое для аутентификации в ADLS.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="d9e8e-125">Сохраните изменения в левом верхнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="d9e8e-126">На следующем рисунке показан пример конфигурации ADLS.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-126">The following image shows an example ADLS configuration.</span></span>

![Пример конфигурации ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="d9e8e-128">Проверка подключения ADLS</span><span class="sxs-lookup"><span data-stu-id="d9e8e-128">Test the ADLS connection</span></span>

1. <span data-ttu-id="d9e8e-129">Проверьте подключение к KeyVault с помощью ссылки **Проверка Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="d9e8e-130">Проверьте подключение к ADLS с помощью ссылки **Проверка хранилища Azure**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-130">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="d9e8e-131">Если проверка завершилась неудачно, проверьте правильность всех добавленных данных KeyVault, а затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="d9e8e-132">После успешного выполнения проверки подключения необходимо включить автоматическое обновление для хранилища объектов.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="d9e8e-133">Чтобы включить автоматическое обновление хранилища объектов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="d9e8e-134">Найдите **Хранилище объектов**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="d9e8e-135">В списке слева перейдите к записи **RetailSales** и выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="d9e8e-136">Убедитесь, что для **Автоматическое обновление включено** выбрано значение **Да**, выберите **Обновить**, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="d9e8e-137">На следующем рисунке показан пример хранилища объектов с включенным автоматическим обновлением.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Пример хранилища объектов с включенным автоматическим обновлением](./media/exampleADLSConfig2.png)

<span data-ttu-id="d9e8e-139">Теперь ADLS настроено для среды.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-139">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="d9e8e-140">Если это еще не было выполнено, выполните шаги, необходимые для [включения рекомендаций по продукту и персонализации](enable-product-recommendations.md) для среды.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9e8e-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9e8e-141">Additional resources</span></span>

[<span data-ttu-id="d9e8e-142">Предоставление хранилища объектов как Data Lake</span><span class="sxs-lookup"><span data-stu-id="d9e8e-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="d9e8e-143">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="d9e8e-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d9e8e-144">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="d9e8e-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d9e8e-145">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d9e8e-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d9e8e-146">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="d9e8e-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d9e8e-147">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="d9e8e-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d9e8e-148">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="d9e8e-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d9e8e-149">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="d9e8e-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d9e8e-150">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="d9e8e-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d9e8e-151">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="d9e8e-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d9e8e-152">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="d9e8e-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
