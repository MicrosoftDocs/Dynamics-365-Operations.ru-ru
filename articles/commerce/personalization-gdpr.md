---
title: Отказ от персонализированных рекомендаций
description: В этой теме объясняется, как предоставить клиентам возможность отказаться от получения персонализированных рекомендаций в Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
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
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025276"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="fc780-103">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="fc780-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc780-104">В этой теме объясняется, как предоставить клиентам возможность отказаться от получения персонализированных рекомендаций в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fc780-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc780-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="fc780-105">Overview</span></span>

<span data-ttu-id="fc780-106">Во время создания учетной записи новые клиенты автоматически настраиваются для получения персонализированных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="fc780-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="fc780-107">Однако предоставляет Dynamics 365 Commerce различные способы, позволяющие пользователям отказаться от получения этих рекомендаций и ограничить обработку личных данных.</span><span class="sxs-lookup"><span data-stu-id="fc780-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="fc780-108">Прошедшие аутентификацию пользователи, которые отказываются от получения персонализированных рекомендаций, сразу перестанут видеть персонализированные списки.</span><span class="sxs-lookup"><span data-stu-id="fc780-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="fc780-109">Кроме того, все личные данные, собранные для персонализации, будут удалены из персонализированных моделей рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="fc780-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="fc780-110">Дополнительные сведения о персонализированных рекомендациях по продуктам см. в разделе [Включение персонализированных рекомендаций](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fc780-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="fc780-111">Способы реализации функции отказа на стороне розничных продавцов</span><span class="sxs-lookup"><span data-stu-id="fc780-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="fc780-112">У розничных продавцов есть три способа реализации функции отказа.</span><span class="sxs-lookup"><span data-stu-id="fc780-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="fc780-113">Отказ от имени пользователей</span><span class="sxs-lookup"><span data-stu-id="fc780-113">Opting out on behalf of users</span></span>

<span data-ttu-id="fc780-114">В управлении учетными записями в бэк-офисе Commerce можно отказаться от имени пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc780-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="fc780-115">На домашней странице бэк-офиса найдите **всех клиентов**.</span><span class="sxs-lookup"><span data-stu-id="fc780-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="fc780-116">Выполните поиск и выберите клиента, а затем выберите экспресс-вкладку **Розничная торговля**.</span><span class="sxs-lookup"><span data-stu-id="fc780-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Экспресс-вкладка "Розничная торговля"](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="fc780-118">В области **Безопасность** задайте для параметра **Отключить персонализацию** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="fc780-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Параметры конфиденциальности](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="fc780-120">Выберите **Сохранить** и закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fc780-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="fc780-121">Функция отказа на основе модуля</span><span class="sxs-lookup"><span data-stu-id="fc780-121">Module-based opt-out experience</span></span>

<span data-ttu-id="fc780-122">Розничные продавцы могут разрешить прошедшим аутентификацию пользователям отказаться от персонализированных рекомендаций самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="fc780-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="fc780-123">Чтобы обеспечить такой отказ, добавьте на страницы профиля учетной записи клиента модуль отказа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc780-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="fc780-124">Настраиваемые расширения</span><span class="sxs-lookup"><span data-stu-id="fc780-124">Custom extensions</span></span>

<span data-ttu-id="fc780-125">Розничные магазины могут создавать свои собственные расширения для управления отказами пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc780-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="fc780-126">Дополнительные сведения см. в разделе [API вызова Retail Server](e-commerce-extensibility/call-retail-server-apis.md) и [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc780-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="fc780-127">Получение цифровой копии данных персонализированных рекомендаций от имени аутентифицированного пользователя</span><span class="sxs-lookup"><span data-stu-id="fc780-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="fc780-128">Клиентам может потребоваться получение цифровой копии своих личных данных, а также просмотр экспортированного представления результатов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="fc780-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="fc780-129">Если клиент запрашивает эту информацию, продавец должен создать настраиваемое расширение, которое будет вызывать API Retail Server и запрашивать полные результаты из списка **Для вас** на основе кода клиента.</span><span class="sxs-lookup"><span data-stu-id="fc780-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="fc780-130">Затем результаты можно экспортировать в формат значений с разделителями-запятыми (CSV) и отправить клиенту.</span><span class="sxs-lookup"><span data-stu-id="fc780-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="fc780-131">Следующий пример показывает, как продавец может выполнить эту задачу.</span><span class="sxs-lookup"><span data-stu-id="fc780-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="fc780-132">Розничный продавец создает пользовательское расширение для получения данных персональных рекомендаций от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc780-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="fc780-133">Сведения о том, как создавать модули, клонировать существующие модули, вызывать API Retail Server и вызывать действия с данными, см. в разделе [Расширяемость канала продаж через Интернет](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc780-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="fc780-134">Настраиваемое расширение выполняет вызов действия основных данных **get-recommendations** и передает в него требуемые сведения на основе требований списка.</span><span class="sxs-lookup"><span data-stu-id="fc780-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="fc780-135">В случае списка **Для вас** расширение должно передать правильное имя списка и код клиента в действие данных.</span><span class="sxs-lookup"><span data-stu-id="fc780-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="fc780-136">Одним из способов создания пользовательского расширения является клонирование существующего модуля коллекции продуктов, используемого для возврата результатов рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="fc780-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="fc780-137">При клонировании существующего модуля розничный продавец может изменить существующий код и добавить новую кнопку, которая экспортирует результаты рекомендаций в файл CSV.</span><span class="sxs-lookup"><span data-stu-id="fc780-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="fc780-138">Дополнительные сведения см. в разделе [Клонирование модуля начального набора](e-commerce-extensibility/clone-starter-module.md) и [Модули семейства продуктов](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc780-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="fc780-139">Полный обзор библиотеки Retail Server API см. в разделе [API клиентов и покупателей розничных серверов](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="fc780-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="fc780-140">После создания пользовательского расширения продавец может экспортировать файл CSV со всеми результатами рекомендаций на основе уникального кода клиента, прошедшего аутентификацию пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc780-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="fc780-141">Розничный продавец может поделиться экспортированным CSV-файлом, содержащим персонализированный список рекомендуемых продуктов, с прошедшим аутентификацию пользователем.</span><span class="sxs-lookup"><span data-stu-id="fc780-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc780-142">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fc780-142">Additional resources</span></span>

[<span data-ttu-id="fc780-143">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="fc780-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fc780-144">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="fc780-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fc780-145">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="fc780-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fc780-146">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="fc780-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="fc780-147">Добавление панели рекомендаций к POS-устройствам</span><span class="sxs-lookup"><span data-stu-id="fc780-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fc780-148">Обзор модуля семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="fc780-148">Product collection module overview</span></span>](product-collection-module-overview.md)
