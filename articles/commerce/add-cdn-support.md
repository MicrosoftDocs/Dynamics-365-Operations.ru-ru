---
title: Добавление поддержки сети доставки контента (CDN)
description: В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945636"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="df6a4-103">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="df6a4-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="df6a4-104">В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df6a4-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="df6a4-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="df6a4-105">Overview</span></span>

<span data-ttu-id="df6a4-106">При настройке среды электронной коммерции в Dynamics 365 Commerce можно настроить ее для работы со службой CDN.</span><span class="sxs-lookup"><span data-stu-id="df6a4-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="df6a4-107">Пользовательский домен может быть включен во время процесса подготовки к работе для среды электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="df6a4-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="df6a4-108">Вместо этого можно использовать запрос на обслуживание, чтобы настроить его после завершения процесса подготовки.</span><span class="sxs-lookup"><span data-stu-id="df6a4-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="df6a4-109">Процесс подготовки для среды электронной коммерции создает имя узла, связанное с данной средой.</span><span class="sxs-lookup"><span data-stu-id="df6a4-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="df6a4-110">Имя этого узла имеет следующий формат, где *e-commerce-tenant-name* — это имя среды:</span><span class="sxs-lookup"><span data-stu-id="df6a4-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="df6a4-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="df6a4-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="df6a4-112">Имя узла или конечная точка, создаваемая в ходе процесса подготовки, поддерживает сертификат SSL только для \*commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="df6a4-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="df6a4-113">Оно не поддерживает SSL для пользовательских доменов.</span><span class="sxs-lookup"><span data-stu-id="df6a4-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="df6a4-114">Поэтому необходимо завершить протокол SSL для пользовательских доменов в вашей сети CDN и передать трафик из CDN в имя хоста или конечную точку, созданную Commerce.</span><span class="sxs-lookup"><span data-stu-id="df6a4-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="df6a4-115">Кроме того, *статические элементы* (файлы JavaScript или каскадных таблиц стилей \[CSS\]) из Commerce обслуживаются из конечной точки, созданной Commerce (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="df6a4-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="df6a4-116">Статические структуры могут кэшироваться только в том случае, если имя узла или конечной точки, которую создает Commerce, помещается позади сети CDN.</span><span class="sxs-lookup"><span data-stu-id="df6a4-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="df6a4-117">Настройка SSL</span><span class="sxs-lookup"><span data-stu-id="df6a4-117">Set up SSL</span></span>

<span data-ttu-id="df6a4-118">Чтобы гарантировать настройку SSL и правильность кэширования статических структур, необходимо настроить CDN так, чтобы он был связан с именем узла, созданным Commerce для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="df6a4-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="df6a4-119">Кроме того, необходимо кэшировать следующий шаблон только для статических структур:</span><span class="sxs-lookup"><span data-stu-id="df6a4-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="df6a4-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="df6a4-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="df6a4-121">После подготовки вашей среды Commerce с предоставленным пользовательским доменом или после предоставления пользовательского домена для среды с помощью запроса на обслуживание направьте пользовательский домен на имя узла или конечную точку, которая была создана в Commerce.</span><span class="sxs-lookup"><span data-stu-id="df6a4-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="df6a4-122">Как уже упоминалось, созданное имя узла или конечная точка поддерживает сертификат SSL только для \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="df6a4-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="df6a4-123">Оно не поддерживает SSL для пользовательских доменов.</span><span class="sxs-lookup"><span data-stu-id="df6a4-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="df6a4-124">Службы CDN</span><span class="sxs-lookup"><span data-stu-id="df6a4-124">CDN services</span></span>

<span data-ttu-id="df6a4-125">Со средой Commerce можно использовать любую службу CDN.</span><span class="sxs-lookup"><span data-stu-id="df6a4-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="df6a4-126">Вот два примера:</span><span class="sxs-lookup"><span data-stu-id="df6a4-126">Here are two examples:</span></span>

- <span data-ttu-id="df6a4-127">**Microsoft Azure Front Door Service** — решение Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="df6a4-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="df6a4-128">Дополнительные сведения о службе Azure Front Door Service см. в [документации по Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="df6a4-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="df6a4-129">**Ускоритель динамических сайтов Akamai** — для получения дополнительных сведений см. раздел [Ускоритель динамических сайтов](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="df6a4-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="df6a4-130">Настройка CDN</span><span class="sxs-lookup"><span data-stu-id="df6a4-130">CDN setup</span></span>

<span data-ttu-id="df6a4-131">Процесс установки CDN состоит из следующих основных шагов:</span><span class="sxs-lookup"><span data-stu-id="df6a4-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="df6a4-132">Добавьте узел переднего плана.</span><span class="sxs-lookup"><span data-stu-id="df6a4-132">Add a front-end host.</span></span>
1. <span data-ttu-id="df6a4-133">Настройте серверный пул.</span><span class="sxs-lookup"><span data-stu-id="df6a4-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="df6a4-134">Настройте правила для маршрутизации и кэширования.</span><span class="sxs-lookup"><span data-stu-id="df6a4-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="df6a4-135">Добавление узла переднего плана</span><span class="sxs-lookup"><span data-stu-id="df6a4-135">Add a front-end host</span></span>

<span data-ttu-id="df6a4-136">Можно использовать любую службу CDN, но для примера в этом разделе используется служба Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="df6a4-137">Сведения о настройке службы Azure Front Door Service см. в разделе [Краткое руководство: Создание службы Front Door для глобального веб-приложения с высокой доступностью](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="df6a4-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="df6a4-138">Настройка серверного пула в службе Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="df6a4-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="df6a4-139">Чтобы настроить серверный пул в службе Azure Front Door Service, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="df6a4-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="df6a4-140">Добавьте **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** в серверный пул в качестве пользовательского узла с пустым заголовком серверного узла.</span><span class="sxs-lookup"><span data-stu-id="df6a4-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="df6a4-141">В области **Зонды работоспособности** в поле **Путь** введите **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="df6a4-142">В поле **Интервалы (с)** введите **255**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="df6a4-143">В разделе **Балансировка нагрузки** оставьте значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df6a4-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="df6a4-144">На следующем рисунке показано диалоговое окно **Добавление серверного пула** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно добавления серверного пула](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="df6a4-146">Настройка правил в службе Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="df6a4-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="df6a4-147">Чтобы настроить правило маршрутизации в службе Azure Front Door Service, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="df6a4-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="df6a4-148">Добавьте правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="df6a4-148">Add a routing rule.</span></span>
1. <span data-ttu-id="df6a4-149">В поле **Имя** введите **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="df6a4-150">В поле **Принятый протокол** выберите **HTTP и HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="df6a4-151">В поле **Интерфейсные узлы** введите **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="df6a4-152">В области **Шаблоны для сопоставления** в верхнем поле введите **/\***.</span><span class="sxs-lookup"><span data-stu-id="df6a4-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="df6a4-153">В разделе **Сведения о маршруте** установите параметр **Тип маршрута** в значение **Прямой**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="df6a4-154">В поле **Серверный пул** выберите **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="df6a4-155">В группе полей **Протокол переадресации** выберите параметр **Сопоставить запрос**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="df6a4-156">Установите для параметра **Перезапись URL** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="df6a4-157">Установите для параметра **Кэширование** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="df6a4-158">Чтобы настроить правило кэширования в службе Azure Front Door Service, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="df6a4-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="df6a4-159">Добавьте правило кэширования.</span><span class="sxs-lookup"><span data-stu-id="df6a4-159">Add a caching rule.</span></span>
1. <span data-ttu-id="df6a4-160">В поле **Имя** введите **статические**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="df6a4-161">В поле **Принятый протокол** выберите **HTTP и HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="df6a4-162">В поле **Интерфейсные узлы** введите **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="df6a4-163">В области **Шаблоны для сопоставления** в верхнем поле введите **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="df6a4-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="df6a4-164">В разделе **Сведения о маршруте** установите параметр **Тип маршрута** в значение **Прямой**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="df6a4-165">В поле **Серверный пул** выберите **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="df6a4-166">В группе полей **Протокол переадресации** выберите параметр **Сопоставить запрос**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="df6a4-167">Установите для параметра **Перезапись URL** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="df6a4-168">Установите для параметра **Кэширование** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="df6a4-169">В поле поведение **Режим кэширования строк запросов** выберите **Кэшировать каждый уникальный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="df6a4-170">В группе полей **Динамическое сжатие** выберите **Включено**.</span><span class="sxs-lookup"><span data-stu-id="df6a4-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="df6a4-171">На следующем рисунке показано диалоговое окно **Добавление правила** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно добавления правила](./media/CDN_CachingRule.png)

<span data-ttu-id="df6a4-173">После развертывания первоначальной конфигурации необходимо добавить пользовательский домен в конфигурацию для службы Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="df6a4-174">Чтобы добавить пользовательский домен (например, `www.fabrikam.com`), необходимо настроить каноническое имя (CNAME) для домена.</span><span class="sxs-lookup"><span data-stu-id="df6a4-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="df6a4-175">На следующем рисунке показано диалоговое окно **Конфигурация CNAME** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно конфигурации CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="df6a4-177">Если домен, который вы будете использовать, уже активен и введен в действие, обратитесь в службу поддержки, чтобы включить этот домен в службе Azure Front Door Service и настроить проверку.</span><span class="sxs-lookup"><span data-stu-id="df6a4-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="df6a4-178">Можно использовать службу Azure Front Door Service для управления сертификатом, или можно использовать собственный сертификат для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="df6a4-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="df6a4-179">На следующем рисунке показано диалоговое окно **HTTPS для личного домена** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="df6a4-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно "HTTPS для личного домена"](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="df6a4-181">Сеть CDN теперь должна быть правильно настроена, чтобы ее можно было использовать с вашим сайтом Commerce.</span><span class="sxs-lookup"><span data-stu-id="df6a4-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df6a4-182">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df6a4-182">Additional resources</span></span>

[<span data-ttu-id="df6a4-183">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="df6a4-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="df6a4-184">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="df6a4-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="df6a4-185">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="df6a4-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="df6a4-186">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="df6a4-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="df6a4-187">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="df6a4-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="df6a4-188">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="df6a4-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="df6a4-189">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="df6a4-189">Enable location-based store detection</span></span>](enable-store-detection.md)
