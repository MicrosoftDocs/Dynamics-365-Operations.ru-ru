---
title: Параметры реализации сети доставки содержимого
description: В этом разделе рассматриваются разнообразные параметры реализации сети доставки содержимого (CDN), которые могут использоваться в средах Microsoft Dynamics 365 Commerce. К этим параметрам относятся собственные, предоставляемые Commerce экземпляры Azure Front Door и принадлежащие клиенту экземпляры Azure Front Door.
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582811"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="259b2-104">Параметры реализации сети доставки содержимого</span><span class="sxs-lookup"><span data-stu-id="259b2-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="259b2-105">В этом разделе рассматриваются разнообразные параметры реализации сети доставки содержимого (CDN), которые могут использоваться в средах Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="259b2-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="259b2-106">К этим параметрам относятся собственные, предоставляемые Commerce экземпляры Azure Front Door и принадлежащие клиенту экземпляры Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="259b2-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="259b2-107">У клиентов Commerce есть несколько вариантов, когда они рассматривают, какая служба CDN должна использоваться в их среде Commerce.</span><span class="sxs-lookup"><span data-stu-id="259b2-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="259b2-108">В Commerce используется базовая поддержка Azure Front Door, которая охватывает базовые требования к размещению и личному домену.</span><span class="sxs-lookup"><span data-stu-id="259b2-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="259b2-109">Для компаний, которым требуется больший контроль и более конкретные возможности безопасности, такие как брандмауэр веб-приложения (WAF), наилучшим вариантом может быть использование либо принадлежащего клиенту экземпляра Azure Front Door, либо внешней службы CDN.</span><span class="sxs-lookup"><span data-stu-id="259b2-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="259b2-110">В средах Commerce могут использоваться следующие три варианта реализации CDN:</span><span class="sxs-lookup"><span data-stu-id="259b2-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="259b2-111">Экземпляр Azure Front Door, предоставленный Commerce</span><span class="sxs-lookup"><span data-stu-id="259b2-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="259b2-112">Принадлежащий клиенту экземпляр Azure Front Door (для расширенного контроля и дополнительных функций безопасности)</span><span class="sxs-lookup"><span data-stu-id="259b2-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="259b2-113">Внешняя служба CDN</span><span class="sxs-lookup"><span data-stu-id="259b2-113">An external CDN service</span></span>

<span data-ttu-id="259b2-114">Все три варианта реализации CDN поставляют только динамическое содержимое HTML из личных доменов.</span><span class="sxs-lookup"><span data-stu-id="259b2-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="259b2-115">Commerce автоматически обрабатывает все сценарии JavaScript, каскадные таблицы стилей (CSS), изображения, видео и другое статическое содержимое в управляемой корпорацией Майкрософт CDN.</span><span class="sxs-lookup"><span data-stu-id="259b2-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="259b2-116">Выбранный параметр определяет доступные возможности, возможности контроля и дополнительные возможности обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="259b2-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="259b2-117">На следующем рисунке показан обзор архитектуры Commerce.</span><span class="sxs-lookup"><span data-stu-id="259b2-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Обзор архитектуры Commerce](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="259b2-119">Дополнительные сведения о настройке экземпляра Azure Front Door для сайта Commerce см. в разделе [Добавление поддержки CDN](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="259b2-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="259b2-120">Используйте экземпляр Azure Front Door, предоставленный Commerce</span><span class="sxs-lookup"><span data-stu-id="259b2-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="259b2-121">В приведенной ниже таблице перечислены достоинства и недостатки использования предоставляемого Commerce экземпляра Azure Front Door для управления конечными точками содержимого.</span><span class="sxs-lookup"><span data-stu-id="259b2-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="259b2-122">Преимущества</span><span class="sxs-lookup"><span data-stu-id="259b2-122">Pros</span></span> | <span data-ttu-id="259b2-123">Недостатки</span><span class="sxs-lookup"><span data-stu-id="259b2-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="259b2-124">Экземпляр включен в стоимость Commerce.</span><span class="sxs-lookup"><span data-stu-id="259b2-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="259b2-125">Так как экземпляр управляется рабочая группа Commerce, необходимо меньше обслуживания, и имеются общие шаги настройки.</span><span class="sxs-lookup"><span data-stu-id="259b2-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="259b2-126">Инфраструктура, размещенная в Azure, является масштабируемой, безопасной и надежной.</span><span class="sxs-lookup"><span data-stu-id="259b2-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="259b2-127">SSL-сертификат требует однократной настройки и автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="259b2-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="259b2-128">Рабочая группа Commerce отслеживает экземпляр на предмет ошибок и аномалий.</span><span class="sxs-lookup"><span data-stu-id="259b2-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="259b2-129">WAF не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="259b2-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="259b2-130">Отсутствуют какие-либо настройки или корректировки параметров.</span><span class="sxs-lookup"><span data-stu-id="259b2-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="259b2-131">Экземпляр зависит от рабочей группы Commerce по обновлению или изменению.</span><span class="sxs-lookup"><span data-stu-id="259b2-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="259b2-132">Для вершинные домены требуется отдельный экземпляр Azure Front Door, и требуется дополнительная работа для интеграции вершинные домены с Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="259b2-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="259b2-133">Заказчику не предоставляется телеметрия об ответах в секунду (RPS) или частоте ошибок.</span><span class="sxs-lookup"><span data-stu-id="259b2-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="259b2-134">На следующем рисунке показана архитектура экземпляра Azure Front Door, предоставляемой Commerce.</span><span class="sxs-lookup"><span data-stu-id="259b2-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Экземпляр Azure Front Door, предоставленный Commerce](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="259b2-136">Использование принадлежащего клиенту экземпляра Azure Front Door</span><span class="sxs-lookup"><span data-stu-id="259b2-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="259b2-137">В приведенной ниже таблице перечислены преимущества и недостатки использования принадлежащего клиенту экземпляра Azure Front Door для управления конечными точками содержимого.</span><span class="sxs-lookup"><span data-stu-id="259b2-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="259b2-138">Преимущества</span><span class="sxs-lookup"><span data-stu-id="259b2-138">Pros</span></span> | <span data-ttu-id="259b2-139">Недостатки</span><span class="sxs-lookup"><span data-stu-id="259b2-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="259b2-140">Настройка безопасна и проста в управлении.</span><span class="sxs-lookup"><span data-stu-id="259b2-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="259b2-141">Инфраструктура, размещенная в Azure, является масштабируемой, безопасной и надежной.</span><span class="sxs-lookup"><span data-stu-id="259b2-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="259b2-142">Данный экземпляр позволяет осуществлять интеграцию с WAF и детальный контроль правил для обеспечения безопасности более высокого уровня, которая специально настраивается для сайта.</span><span class="sxs-lookup"><span data-stu-id="259b2-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="259b2-143">Данный экземпляр обеспечивает более точное управление сертификатами SSL (как клиентские, так и управляемые Azure Front Door) и привязкой доменов.</span><span class="sxs-lookup"><span data-stu-id="259b2-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="259b2-144">Экземпляр предлагает решение вершинных доменов, если оно напрямую связано с Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="259b2-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="259b2-145">Предусмотрены телеметрия и оповещение.</span><span class="sxs-lookup"><span data-stu-id="259b2-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="259b2-146">SSL-сертификат требует однократной настройки и автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="259b2-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="259b2-147">Экземпляр является самоуправляемым.</span><span class="sxs-lookup"><span data-stu-id="259b2-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="259b2-148">Требуется наращивание начальных знаний.</span><span class="sxs-lookup"><span data-stu-id="259b2-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="259b2-149">На следующем рисунке показана инфраструктура Commerce, которая включает в себя принадлежащий клиенту экземпляр Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="259b2-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![Инфраструктура Commerce, которая включает в себя принадлежащий клиенту экземпляр Azure Front Door](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="259b2-151">Использование внешней службы CDN</span><span class="sxs-lookup"><span data-stu-id="259b2-151">Use an external CDN service</span></span>

<span data-ttu-id="259b2-152">В следующей таблице перечислены преимущества и недостатки использования внешней службы CDN для управления конечными точками содержимого.</span><span class="sxs-lookup"><span data-stu-id="259b2-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="259b2-153">Преимущества</span><span class="sxs-lookup"><span data-stu-id="259b2-153">Pros</span></span> | <span data-ttu-id="259b2-154">Недостатки</span><span class="sxs-lookup"><span data-stu-id="259b2-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="259b2-155">Этот параметр полезен, если существующий домен уже размещен во внешней сети CDN.</span><span class="sxs-lookup"><span data-stu-id="259b2-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="259b2-156">CDN конкурентов (например, Akamai) могут иметь больше возможностей WAF.</span><span class="sxs-lookup"><span data-stu-id="259b2-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="259b2-157">Требуется отдельный договор и дополнительная калькуляция.</span><span class="sxs-lookup"><span data-stu-id="259b2-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="259b2-158">Протокол SSL может повлечь дополнительные затраты.</span><span class="sxs-lookup"><span data-stu-id="259b2-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="259b2-159">Поскольку служба отличается от облачной структуры Azure, необходимо управлять дополнительной инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="259b2-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="259b2-160">Служба может потребовать более длительной временной инвестиции в настройку конечной точки и безопасности.</span><span class="sxs-lookup"><span data-stu-id="259b2-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="259b2-161">Служба является самоуправляемым.</span><span class="sxs-lookup"><span data-stu-id="259b2-161">The service is self-managed.</span></span></li><li><span data-ttu-id="259b2-162">Служба с самоконтролем.</span><span class="sxs-lookup"><span data-stu-id="259b2-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="259b2-163">На следующем рисунке показана инфраструктура Commerce, которая включает внешнюю службу CDN.</span><span class="sxs-lookup"><span data-stu-id="259b2-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![Инфраструктура Commerce, которая включает внешнюю службу CDN](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="259b2-165">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="259b2-165">Additional resources</span></span>

[<span data-ttu-id="259b2-166">Добавление поддержки сети доставки содержимого (CDN)</span><span class="sxs-lookup"><span data-stu-id="259b2-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)