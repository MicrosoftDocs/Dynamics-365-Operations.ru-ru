---
title: Включение ADLS в среде Dynamics 365 Commerce
description: В этой теме объясняется, как включить и проверить Azure Data Lake Storage (ADLS) для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025275"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="1e244-103">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1e244-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e244-104">В этой теме объясняется, как включить и проверить Azure Data Lake Storage (ADLS) для среды Dynamics 365 Commerce, что является необходимым условием для включения рекомендаций по продукту.</span><span class="sxs-lookup"><span data-stu-id="1e244-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="1e244-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="1e244-105">Overview</span></span>

<span data-ttu-id="1e244-106">В решении Dynamics 365 Commerce все сведения о продуктах и проводках отслеживаются в хранилище объектов среды.</span><span class="sxs-lookup"><span data-stu-id="1e244-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="1e244-107">Чтобы сделать эти данные доступными другим службам Dynamics 365, таким как анализ данных, бизнес-аналитика и персонализированные рекомендации, необходимо подключить среду к принадлежащему заказчику решению Azure Data Lake Storage Gen 2 (ADLS).</span><span class="sxs-lookup"><span data-stu-id="1e244-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="1e244-108">После настройки ADLS в среде все необходимые данные будут зеркально отражены из хранилища объектов, а также защищены и будут управляться клиентом.</span><span class="sxs-lookup"><span data-stu-id="1e244-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="1e244-109">Если в среде также включены рекомендации по продукту или персонализированные рекомендации, то в стеке рекомендаций по продукту будет предоставлен доступ к выделенной папке в ADLS, чтобы извлечь данные клиента и вычислить рекомендации на их основе.</span><span class="sxs-lookup"><span data-stu-id="1e244-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e244-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="1e244-110">Prerequisites</span></span>

<span data-ttu-id="1e244-111">У клиентов должны быть настроены ADLS в подписке Azure, которая им принадлежит.</span><span class="sxs-lookup"><span data-stu-id="1e244-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="1e244-112">Этот раздел не охватывает покупку подписки Azure или настройки учетной записи хранения с ADLS.</span><span class="sxs-lookup"><span data-stu-id="1e244-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="1e244-113">Дополнительные сведения о ADLS см. в разделе [Официальная документация по ADLS](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="1e244-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="1e244-114">Шаги конфигурации</span><span class="sxs-lookup"><span data-stu-id="1e244-114">Configuration steps</span></span>

<span data-ttu-id="1e244-115">В этом разделе описываются этапы настройки, необходимые для включения ADLS в среде.</span><span class="sxs-lookup"><span data-stu-id="1e244-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="1e244-116">Включение ADLS в среде</span><span class="sxs-lookup"><span data-stu-id="1e244-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="1e244-117">Выполните вход на портал операционных отделов организации для среды.</span><span class="sxs-lookup"><span data-stu-id="1e244-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="1e244-118">Выполните поиск **Системные параметры** и перейдите на вкладку **Подключения данных**.</span><span class="sxs-lookup"><span data-stu-id="1e244-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="1e244-119">Установите для **Разрешить интеграцию с Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1e244-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="1e244-120">Установите для **Постепенное обновление Data Lake** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1e244-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="1e244-121">Затем введите следующие необходимые сведения:</span><span class="sxs-lookup"><span data-stu-id="1e244-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="1e244-122">**Код приложения** // **Секретный ключ приложения** // **DNS-имя** — требуется для подключения к KeyVault, где хранится секретный ключ ADLS.</span><span class="sxs-lookup"><span data-stu-id="1e244-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="1e244-123">**Имя секрета** — имя секрета, хранящееся в KeyVault и используемое для аутентификации в ADLS.</span><span class="sxs-lookup"><span data-stu-id="1e244-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="1e244-124">Сохраните изменения в левом верхнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="1e244-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="1e244-125">На следующем рисунке показан пример конфигурации ADLS.</span><span class="sxs-lookup"><span data-stu-id="1e244-125">The following image shows an example ADLS configuration.</span></span>

![Пример конфигурации ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="1e244-127">Проверка подключения ADLS</span><span class="sxs-lookup"><span data-stu-id="1e244-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="1e244-128">Проверьте подключение к KeyVault с помощью ссылки **Проверка Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="1e244-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="1e244-129">Проверьте подключение к ADLS с помощью ссылки **Проверка хранилища Azure**.</span><span class="sxs-lookup"><span data-stu-id="1e244-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="1e244-130">Если проверка завершилась неудачно, проверьте правильность всех добавленных данных KeyVault, а затем повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="1e244-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="1e244-131">После успешного выполнения проверки подключения необходимо включить автоматическое обновление для хранилища объектов.</span><span class="sxs-lookup"><span data-stu-id="1e244-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="1e244-132">Чтобы включить автоматическое обновление хранилища объектов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e244-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="1e244-133">Найдите **Хранилище объектов**.</span><span class="sxs-lookup"><span data-stu-id="1e244-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="1e244-134">В списке слева перейдите к записи **RetailSales** и выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1e244-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="1e244-135">Убедитесь, что для **Автоматическое обновление включено** выбрано значение **Да**, выберите **Обновить**, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e244-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="1e244-136">На следующем рисунке показан пример хранилища объектов с включенным автоматическим обновлением.</span><span class="sxs-lookup"><span data-stu-id="1e244-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Пример хранилища объектов с включенным автоматическим обновлением](./media/exampleADLSConfig2.png)

<span data-ttu-id="1e244-138">Теперь ADLS настроено для среды.</span><span class="sxs-lookup"><span data-stu-id="1e244-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="1e244-139">Если это еще не было выполнено, выполните шаги, необходимые для [включения рекомендаций по продукту и персонализации](enable-product-recommendations.md) для среды.</span><span class="sxs-lookup"><span data-stu-id="1e244-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e244-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e244-140">Additional resources</span></span>

[<span data-ttu-id="1e244-141">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="1e244-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1e244-142">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="1e244-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1e244-143">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="1e244-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="1e244-144">Добавление элемента управления рекомендациями на экране проводки на устройствах POS</span><span class="sxs-lookup"><span data-stu-id="1e244-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


