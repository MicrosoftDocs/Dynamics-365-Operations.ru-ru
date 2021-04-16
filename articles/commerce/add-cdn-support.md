---
title: Добавление поддержки сети доставки контента (CDN)
description: В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a56f675b1fb43160625101a067c74e9fcf4f714a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797847"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="1a1ee-103">Добавление поддержки сети доставки содержимого (CDN)</span><span class="sxs-lookup"><span data-stu-id="1a1ee-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a1ee-104">В этом разделе описывается, как добавить сеть доставки содержимого (CDN) в среду Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="1a1ee-105">При настройке среды электронной коммерции в Dynamics 365 Commerce можно настроить ее для работы со службой CDN.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="1a1ee-106">Пользовательский домен может быть включен во время процесса подготовки к работе для среды электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="1a1ee-107">Вместо этого можно использовать запрос на обслуживание, чтобы настроить его после завершения процесса подготовки.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="1a1ee-108">Процесс подготовки для среды электронной коммерции создает имя узла, связанное с данной средой.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="1a1ee-109">Имя этого узла имеет следующий формат, где \<*e-commerce-tenant-name*\> — это имя среды:</span><span class="sxs-lookup"><span data-stu-id="1a1ee-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="1a1ee-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="1a1ee-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="1a1ee-111">Имя узла или конечная точка, создаваемая в ходе процесса подготовки, поддерживает сертификат SSL только для \*commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="1a1ee-112">Оно не поддерживает SSL для пользовательских доменов.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="1a1ee-113">Поэтому необходимо завершить протокол SSL для пользовательских доменов в вашей сети CDN и передать трафик из CDN в имя хоста или конечную точку, созданную Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="1a1ee-114">Кроме того, *статические элементы* (файлы JavaScript или каскадных таблиц стилей \[CSS\]) из Commerce обслуживаются из конечной точки, созданной Commerce (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="1a1ee-115">Статические структуры могут кэшироваться только в том случае, если имя узла или конечной точки, которую создает Commerce, помещается позади сети CDN.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="1a1ee-116">Настроить SSL</span><span class="sxs-lookup"><span data-stu-id="1a1ee-116">Set up SSL</span></span>

<span data-ttu-id="1a1ee-117">После подготовки вашей среды Commerce с предоставленным пользовательским доменом или после предоставления пользовательского домена для среды с помощью запроса на обслуживание необходимо связаться с группой адаптации Commerce, чтобы спланировать изменения DNS.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="1a1ee-118">Как уже упоминалось, созданное имя узла или конечная точка поддерживает сертификат SSL только для \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="1a1ee-119">Оно не поддерживает SSL для пользовательских доменов.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="1a1ee-120">Службы CDN</span><span class="sxs-lookup"><span data-stu-id="1a1ee-120">CDN services</span></span>

<span data-ttu-id="1a1ee-121">Со средой Commerce можно использовать любую службу CDN.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="1a1ee-122">Вот два примера:</span><span class="sxs-lookup"><span data-stu-id="1a1ee-122">Here are two examples:</span></span>

- <span data-ttu-id="1a1ee-123">**Microsoft Azure Front Door Service** — решение Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="1a1ee-124">Дополнительные сведения о службе Azure Front Door Service см. в [документации по Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="1a1ee-125">**Ускоритель динамических сайтов Akamai** — для получения дополнительных сведений см. раздел [Ускоритель динамических сайтов](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="1a1ee-126">Настройка CDN</span><span class="sxs-lookup"><span data-stu-id="1a1ee-126">CDN setup</span></span>

<span data-ttu-id="1a1ee-127">Процесс установки CDN состоит из следующих основных шагов:</span><span class="sxs-lookup"><span data-stu-id="1a1ee-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="1a1ee-128">Добавьте узел переднего плана.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-128">Add a front-end host.</span></span>
1. <span data-ttu-id="1a1ee-129">Настройте серверный пул.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="1a1ee-130">Настройка правил для маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="1a1ee-131">Добавление узла переднего плана</span><span class="sxs-lookup"><span data-stu-id="1a1ee-131">Add a front-end host</span></span>

<span data-ttu-id="1a1ee-132">Можно использовать любую службу CDN, но для примера в этом разделе используется служба Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="1a1ee-133">Сведения о настройке службы Azure Front Door Service см. в разделе [Краткое руководство: Создание службы Front Door для глобального веб-приложения с высокой доступностью](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="1a1ee-134">Настройка серверного пула в службе Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="1a1ee-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="1a1ee-135">Чтобы настроить серверный пул в службе Azure Front Door Service, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="1a1ee-136">Добавьте **&lt;имя-клиента-электронной-коммерции&gt;.commerce.dynamics.com** в серверный пул в качестве настраиваемого узла, который имеет серверный заголовок узла, который совпадает с **&lt;имя-клиента-электронной-коммерции&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="1a1ee-137">В разделе **Балансировка нагрузки** оставьте значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="1a1ee-138">Отключите проверки работоспособности для серверного пула.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="1a1ee-139">На следующем рисунке показано диалоговое окно **Добавление серверного пула** в службе Azure Front Door Service с введенным серверным именем узла.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Диалоговое окно добавления серверного пула](./media/CDN_BackendPool.png)

<span data-ttu-id="1a1ee-141">На следующем рисунке показано диалоговое окно **Добавление серверного пула** в службе Azure Front Door Service со значениями балансировки нагрузки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Диалоговое окно добавления серверного пула (продолжение)](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="1a1ee-143">Убедитесь, что отключены **Зонды работоспособности** при настройке вашей собственной службы Azure Front Door Service для Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="1a1ee-144">Настройка правил в службе Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="1a1ee-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="1a1ee-145">Чтобы настроить правило маршрутизации в службе Azure Front Door Service, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="1a1ee-146">Добавьте правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-146">Add a routing rule.</span></span>
1. <span data-ttu-id="1a1ee-147">В поле **Имя** введите **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="1a1ee-148">В поле **Принятый протокол** выберите **HTTP и HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="1a1ee-149">В поле **Интерфейсные узлы** введите **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="1a1ee-150">В области **Шаблоны для сопоставления** в верхнем поле введите **/\***.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="1a1ee-151">В разделе **Сведения о маршруте** установите параметр **Тип маршрута** в значение **Прямой**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="1a1ee-152">В поле **Серверный пул** выберите **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="1a1ee-153">В группе полей **Протокол переадресации** выберите параметр **Сопоставить запрос**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="1a1ee-154">Установите для параметра **Перезапись URL** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="1a1ee-155">Установите для параметра **Кэширование** значение **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="1a1ee-156">Если используемый домен уже активен и используется, создайте запрос в службу поддержки на плитке **Поддержка** в [Lifecycle Services Microsoft Dynamics](https://lcs.dynamics.com/), чтобы получить помощь для последующих шагов.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="1a1ee-157">Дополнительные сведения см. в разделе [Получение поддержки для приложений Finance and Operations или Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="1a1ee-158">Если домен является новым и не существовал раньше как активный домен, можно добавить личный домен в конфигурацию Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="1a1ee-159">Это позволяет веб-трафику направляться на ваш сайт через экземпляр Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="1a1ee-160">Чтобы добавить пользовательский домен (например, `www.fabrikam.com`), необходимо настроить каноническое имя (CNAME) для домена.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="1a1ee-161">На следующем рисунке показано диалоговое окно **Конфигурация CNAME** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно конфигурации CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="1a1ee-163">Можно использовать службу Azure Front Door Service для управления сертификатом, или можно использовать собственный сертификат для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="1a1ee-164">На следующем рисунке показано диалоговое окно **HTTPS для личного домена** в службе Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Диалоговое окно "HTTPS для личного домена"](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="1a1ee-166">Подробные инструкции по добавлению личного домена в Azure Front Door см. в разделе [Добавление личного домена в Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="1a1ee-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="1a1ee-167">Сеть CDN теперь должна быть правильно настроена, чтобы ее можно было использовать с вашим сайтом Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a1ee-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a1ee-168">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a1ee-168">Additional resources</span></span>

[<span data-ttu-id="1a1ee-169">Параметры реализации сети доставки содержимого</span><span class="sxs-lookup"><span data-stu-id="1a1ee-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
