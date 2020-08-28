---
title: Отказ от персонализированных рекомендаций
description: В этой теме объясняется, как предоставить клиентам возможность отказаться от получения персонализированных рекомендаций в Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: a51c8c0e2743b67df9d66a8c45ab7a69597f4002
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664938"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="75d5b-103">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="75d5b-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75d5b-104">В этой теме объясняется, как предоставить клиентам возможность отказаться от получения персонализированных рекомендаций в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75d5b-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="75d5b-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="75d5b-105">Overview</span></span>

<span data-ttu-id="75d5b-106">Во время создания учетной записи новые клиенты автоматически настраиваются для получения персонализированных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="75d5b-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="75d5b-107">Однако предоставляет Dynamics 365 Commerce различные способы, позволяющие пользователям отказаться от получения этих рекомендаций и ограничить обработку личных данных.</span><span class="sxs-lookup"><span data-stu-id="75d5b-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="75d5b-108">Прошедшие аутентификацию пользователи, которые отказываются от получения персонализированных рекомендаций, сразу перестанут видеть персонализированные списки.</span><span class="sxs-lookup"><span data-stu-id="75d5b-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="75d5b-109">Кроме того, все личные данные, собранные для персонализации, будут удалены из персонализированных моделей рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="75d5b-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="75d5b-110">Дополнительные сведения о персонализированных рекомендациях по продуктам см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="75d5b-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="75d5b-111">Способы реализации функции отказа на стороне розничных продавцов</span><span class="sxs-lookup"><span data-stu-id="75d5b-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="75d5b-112">У розничных продавцов есть три способа реализации функции отказа.</span><span class="sxs-lookup"><span data-stu-id="75d5b-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="75d5b-113">Отказ от имени пользователей</span><span class="sxs-lookup"><span data-stu-id="75d5b-113">Opting out on behalf of users</span></span>

<span data-ttu-id="75d5b-114">В управлении учетными записями в бэк-офисе Commerce можно отказаться от имени пользователей.</span><span class="sxs-lookup"><span data-stu-id="75d5b-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="75d5b-115">На домашней странице бэк-офиса найдите **всех клиентов**.</span><span class="sxs-lookup"><span data-stu-id="75d5b-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="75d5b-116">Выполните поиск и выберите клиента, а затем выберите экспресс-вкладку **Розничная торговля**.</span><span class="sxs-lookup"><span data-stu-id="75d5b-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Экспресс-вкладка "Розничная торговля"](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="75d5b-118">В области **Безопасность** задайте для параметра **Отключить персонализацию** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="75d5b-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Параметры конфиденциальности](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="75d5b-120">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="75d5b-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="75d5b-121">Функция отказа на основе модуля</span><span class="sxs-lookup"><span data-stu-id="75d5b-121">Module-based opt-out experience</span></span>

<span data-ttu-id="75d5b-122">Розничные продавцы могут разрешить прошедшим аутентификацию пользователям отказаться от персонализированных рекомендаций самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="75d5b-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="75d5b-123">Чтобы обеспечить такой отказ, добавьте на страницы профиля учетной записи клиента модуль отказа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="75d5b-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="75d5b-124">Настраиваемые расширения</span><span class="sxs-lookup"><span data-stu-id="75d5b-124">Custom extensions</span></span>

<span data-ttu-id="75d5b-125">Розничные магазины могут создавать свои собственные расширения для управления отказами пользователей.</span><span class="sxs-lookup"><span data-stu-id="75d5b-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="75d5b-126">Дополнительные сведения см. в разделе [API вызова Retail Server](e-commerce-extensibility/call-retail-server-apis.md) и [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="75d5b-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="75d5b-127">Получение цифровой копии данных персонализированных рекомендаций от имени аутентифицированного пользователя</span><span class="sxs-lookup"><span data-stu-id="75d5b-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="75d5b-128">Клиентам может потребоваться получение цифровой копии своих личных данных, а также просмотр экспортированного представления результатов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="75d5b-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="75d5b-129">Если клиент запрашивает эту информацию, продавец должен создать настраиваемое расширение, которое будет вызывать API Retail Server и запрашивать полные результаты из списка **Для вас** на основе кода клиента.</span><span class="sxs-lookup"><span data-stu-id="75d5b-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="75d5b-130">Затем результаты можно экспортировать в формат значений с разделителями-запятыми (CSV) и отправить клиенту.</span><span class="sxs-lookup"><span data-stu-id="75d5b-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="75d5b-131">Следующий пример показывает, как продавец может выполнить эту задачу.</span><span class="sxs-lookup"><span data-stu-id="75d5b-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="75d5b-132">Розничный продавец создает пользовательское расширение для получения данных персональных рекомендаций от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="75d5b-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="75d5b-133">Сведения о том, как создавать модули, клонировать существующие модули, вызывать API Retail Server и вызывать действия с данными, см. в разделе [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="75d5b-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="75d5b-134">Настраиваемое расширение выполняет вызов действия основных данных **get-recommendations** и передает в него требуемые сведения на основе требований списка.</span><span class="sxs-lookup"><span data-stu-id="75d5b-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="75d5b-135">В случае списка **Для вас** расширение должно передать правильное имя списка и код клиента в действие данных.</span><span class="sxs-lookup"><span data-stu-id="75d5b-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="75d5b-136">Одним из способов создания пользовательского расширения является клонирование существующего модуля коллекции продуктов, используемого для возврата результатов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="75d5b-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="75d5b-137">При клонировании существующего модуля розничный продавец может изменить существующий код и добавить новую кнопку, которая экспортирует результаты рекомендаций в файл CSV.</span><span class="sxs-lookup"><span data-stu-id="75d5b-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="75d5b-138">Дополнительные сведения см. в разделе [Клонирование модуля начального набора](e-commerce-extensibility/clone-starter-module.md) и [Модули семейства продуктов](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="75d5b-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="75d5b-139">Полный обзор библиотеки Retail Server API см. в разделе [API клиентов и покупателей розничных серверов](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="75d5b-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="75d5b-140">После создания пользовательского расширения продавец может экспортировать файл CSV со всеми результатами рекомендаций на основе уникального кода клиента, прошедшего аутентификацию пользователя.</span><span class="sxs-lookup"><span data-stu-id="75d5b-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="75d5b-141">Розничный продавец может поделиться экспортированным CSV-файлом, содержащим персонализированный список рекомендуемых продуктов, с прошедшим аутентификацию пользователем.</span><span class="sxs-lookup"><span data-stu-id="75d5b-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75d5b-142">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75d5b-142">Additional resources</span></span>

[<span data-ttu-id="75d5b-143">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="75d5b-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="75d5b-144">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="75d5b-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="75d5b-145">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="75d5b-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="75d5b-146">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="75d5b-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="75d5b-147">Включение рекомендаций "покупать похожие образы"</span><span class="sxs-lookup"><span data-stu-id="75d5b-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="75d5b-148">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="75d5b-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="75d5b-149">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="75d5b-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="75d5b-150">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="75d5b-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="75d5b-151">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="75d5b-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="75d5b-152">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="75d5b-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="75d5b-153">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="75d5b-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
