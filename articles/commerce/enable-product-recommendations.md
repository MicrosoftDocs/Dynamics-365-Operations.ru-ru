---
title: Включить рекомендации по продуктам
description: В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259802"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="4f1a6-103">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="4f1a6-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f1a6-104">В этой теме объясняется, как создать рекомендации продуктов, которые основаны на искусственном интеллекте и машинном обучении (AI-ML), доступном клиентам Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="4f1a6-105">Дополнительные сведения о списках рекомендаций продуктов см. в разделе [Обзор рекомендаций продуктов](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="4f1a6-106">Предварительная проверка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-106">Recommendations pre-check</span></span>

<span data-ttu-id="4f1a6-107">Перед включением обратите внимание, что рекомендации продуктов поддерживаются только для клиентов Commerce, перенесших свои хранилища с помощью Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="4f1a6-108">Перед включением рекомендаций необходимо включить в бэк-офисе следующие конфигурации:</span><span class="sxs-lookup"><span data-stu-id="4f1a6-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="4f1a6-109">Убедитесь, что ADLS было приобретено и успешно проверено в среде.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="4f1a6-110">Дополнительные сведения см. в разделе [Убедитесь, что ADLS было приобретено и успешно проверено в среде](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="4f1a6-111">Убедитесь, что обновление хранилища объектов было автоматизировано.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="4f1a6-112">Дополнительные сведения см. в разделе [Убедитесь, что обновление хранилища данных было автоматизировано](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="4f1a6-113">Убедитесь, что конфигурация удостоверения Azure AD содержит запись для рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="4f1a6-114">Дополнительные сведения о том, как выполнить это действие, см. ниже.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="4f1a6-115">Кроме того, убедитесь, что измерения RetailSale включены.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="4f1a6-116">Дополнительные сведения об этом процессе настройки см. в разделе [Работа с мерами](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="4f1a6-117">Конфигурация удостоверения Azure AD</span><span class="sxs-lookup"><span data-stu-id="4f1a6-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="4f1a6-118">Этот шаг необходим для всех клиентов, использующих конфигурацию инфраструктуры как услуги (IaaS).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="4f1a6-119">Для клиентов, работающих в структуре Service Fabric (SF), этот шаг должен быть автоматическим, и мы рекомендуем проверить правильность настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="4f1a6-120">Настройка</span><span class="sxs-lookup"><span data-stu-id="4f1a6-120">Setup</span></span>

1. <span data-ttu-id="4f1a6-121">В бэк-офисе найдите страницу **Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="4f1a6-122">Проверьте, существует ли запись для "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="4f1a6-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="4f1a6-123">Если запись не существует, добавьте новую запись со следующей информацией:</span><span class="sxs-lookup"><span data-stu-id="4f1a6-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="4f1a6-124">**Код клиента** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="4f1a6-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="4f1a6-125">**Имя** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="4f1a6-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="4f1a6-126">**Код пользователя** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="4f1a6-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="4f1a6-127">Сохраните изменения и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="4f1a6-128">Включение рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-128">Turn on recommendations</span></span>

<span data-ttu-id="4f1a6-129">Чтобы включить рекомендации продуктов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="4f1a6-130">Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Параметры рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="4f1a6-131">В списке общих параметров выберите **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="4f1a6-132">Для параметра **Включить рекомендации** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Включение рекомендаций](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="4f1a6-134">Эта процедура запускает процесс создания списков рекомендаций продуктов.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="4f1a6-135">До того, как списки можно будет просматривать на POS-терминале или в Dynamics 365 Commerce, может потребоваться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="4f1a6-136">Настройка параметров списка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="4f1a6-137">По умолчанию список рекомендаций продуктов на основе AI-ML предоставляет предлагаемые значения.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="4f1a6-138">Предлагаемые по умолчанию значения можно изменить в соответствии с потоком бизнеса.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="4f1a6-139">Дополнительные сведения об изменении параметров по умолчанию см. в разделе [Управление результатами рекомендаций продуктов на основе AI-ML](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="4f1a6-140">Отображение рекомендаций на POS-устройствах</span><span class="sxs-lookup"><span data-stu-id="4f1a6-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="4f1a6-141">После включения рекомендаций в операционных отделах организации Commerce необходимо добавить панель рекомендаций на экран управления POS через инструмент макета.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="4f1a6-142">Для получения сведений об этом процессе см. [Добавление элемента управления рекомендациями на экране проводки на устройствах POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="4f1a6-143">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-143">Enable personalized recommendations</span></span>

<span data-ttu-id="4f1a6-144">В Dynamics 365 Commerce розничные продавцы могут сделать доступными персонализированные рекомендации по продуктам (также называемые персонализацией).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="4f1a6-145">Таким образом, персонализированные рекомендации могут быть включены в интернет-магазине и в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="4f1a6-146">Когда функция персонализации включена, система может связать сведения о покупке пользователя и сведения о продукте, чтобы создать индивидуальные рекомендаций по продуктам.</span><span class="sxs-lookup"><span data-stu-id="4f1a6-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="4f1a6-147">Дополнительные сведения о персонализированных рекомендациях см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a6-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f1a6-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4f1a6-148">Additional resources</span></span>

[<span data-ttu-id="4f1a6-149">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="4f1a6-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4f1a6-150">Включение ADLS в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4f1a6-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4f1a6-151">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4f1a6-152">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="4f1a6-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4f1a6-153">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="4f1a6-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4f1a6-154">Добавление рекомендаций на экран проводки</span><span class="sxs-lookup"><span data-stu-id="4f1a6-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4f1a6-155">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="4f1a6-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4f1a6-156">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="4f1a6-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4f1a6-157">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="4f1a6-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4f1a6-158">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="4f1a6-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

