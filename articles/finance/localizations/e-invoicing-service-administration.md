---
title: Компоненты администрирования надстройки электронного выставления счетов
description: В этой теме приводятся сведения о компонентах, которые относятся к администрированию надстройки электронного выставления накладных.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104430"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="5b9ab-103">Компоненты администрирования надстройки электронного выставления счетов</span><span class="sxs-lookup"><span data-stu-id="5b9ab-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="5b9ab-104">В этой теме приводятся сведения о компонентах, которые относятся к администрированию надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="5b9ab-105">Здесь также приводятся сведения о настройке службы надстройки электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="5b9ab-106">Azure</span><span class="sxs-lookup"><span data-stu-id="5b9ab-106">Azure</span></span>

<span data-ttu-id="5b9ab-107">Используйте Microsoft Azure для создания секретов для хранилища ключей и учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="5b9ab-108">Затем используйте эти секреты в конфигурации надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="5b9ab-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="5b9ab-109">Lifecycle Services</span></span>

<span data-ttu-id="5b9ab-110">Используйте Microsoft Dynamics Lifecycle Services (LCS), чтобы включить надстройку для микрослужб вашего проекта развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="5b9ab-111">В LCS выберите плитку **Управление предварительными версиями функций**, а затем включите функцию **Служба электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="5b9ab-112">Службы Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="5b9ab-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="5b9ab-113">Dynamics 365 Regulatory Configuration Services (RCS) — это интерфейс, который используется для настройки надстройки электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="5b9ab-114">Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и размещаются в RCS.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="5b9ab-115">Когда ресурсы готовы, они публикуются в службе надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="5b9ab-116">Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="5b9ab-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="5b9ab-117">Интеграция с надстройкой "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="5b9ab-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="5b9ab-118">Прежде чем можно будет использовать RCS для настройки электронных накладных, необходимо настроить RCS для обеспечения связи с надстройкой электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="5b9ab-119">Эту настройку можно выполнить на вкладке **Надстройка электронного выставления накладных** на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="5b9ab-120">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-120">Service endpoint</span></span>

<span data-ttu-id="5b9ab-121">URL-адрес конечной точки надстройки электронного выставления накладных может различаться в зависимости от географического расположения центра обработки данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="5b9ab-122">В приведенной ниже таблице содержится список доступности по регионам:</span><span class="sxs-lookup"><span data-stu-id="5b9ab-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="5b9ab-123">География центров обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="5b9ab-123">Azure datacenter geography</span></span> | <span data-ttu-id="5b9ab-124">URL-адрес конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="5b9ab-125">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="5b9ab-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="5b9ab-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="5b9ab-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="5b9ab-127">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="5b9ab-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="5b9ab-128">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="5b9ab-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="5b9ab-129">ИД приложения</span><span class="sxs-lookup"><span data-stu-id="5b9ab-129">Application ID</span></span>

<span data-ttu-id="5b9ab-130">Код приложения — это код приложения надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="5b9ab-131">В этом случае значение фиксировано: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="5b9ab-132">Код среды LCS</span><span class="sxs-lookup"><span data-stu-id="5b9ab-132">LCS environment ID</span></span>

<span data-ttu-id="5b9ab-133">Код среды LCS является кодом подписки LCS вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="5b9ab-134">Среды службы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-134">Service environments</span></span>

<span data-ttu-id="5b9ab-135">Среды службы — это логические разделы, создаваемые для поддержки выполнения функций электронного выставления накладных в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="5b9ab-136">Секреты безопасности и цифровые сертификаты, а также руководство (т. е., разрешения доступа) должны быть настроены на уровне среды службы.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="5b9ab-137">Клиенты могут создавать столько сред служб, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="5b9ab-138">Все среды службы, которые создает клиент, независимы друг от друга.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="5b9ab-139">Среды службы должны создаваться и поддерживаться в RCS.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="5b9ab-140">Когда среды службы готовы, они должны быть опубликованы в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="5b9ab-141">Состояние среды службы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-141">Service environment status</span></span>

<span data-ttu-id="5b9ab-142">Управление средами служб осуществляется через их состояние.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-142">Service environments can be managed through status.</span></span> <span data-ttu-id="5b9ab-143">Возможны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="5b9ab-143">The possible options are:</span></span>

- <span data-ttu-id="5b9ab-144">**Не опубликовано** — среда создана, но еще не была опубликована.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="5b9ab-145">**Опубликовано** — среда была опубликована в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="5b9ab-146">**Изменено** — атрибуты опубликованной среды были изменены, но изменения еще не были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="5b9ab-147">Секреты клиентов</span><span class="sxs-lookup"><span data-stu-id="5b9ab-147">Customer secrets</span></span>

<span data-ttu-id="5b9ab-148">Служба надстройки электронного выставления накладных отвечает за хранение всех ваших деловых данных в ресурсах Azure, принадлежащих вашей компании.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="5b9ab-149">Для обеспечения правильной работы службы и того, что все деловые данные, необходимые для дополнения электронных накладных и создаваемые этим дополнением, доступны только для этого дополнения, необходимо создать два основных ресурса Azure:</span><span class="sxs-lookup"><span data-stu-id="5b9ab-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="5b9ab-150">Учетная запись хранилища Azure (хранилище BLOB-объектов), в которой будут храниться электронные накладные</span><span class="sxs-lookup"><span data-stu-id="5b9ab-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="5b9ab-151">Хранилище ключей Azure, в котором будут храниться сертификаты и универсальный код ресурса (URI) учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="5b9ab-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="5b9ab-152">Учетная запись хранилища ключей и хранилища BLOB-объектов клиента должна быть выделена специально для использования с дополнением электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="5b9ab-153">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="5b9ab-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="5b9ab-154">Пользователи</span><span class="sxs-lookup"><span data-stu-id="5b9ab-154">Users</span></span>

<span data-ttu-id="5b9ab-155">В каждой среде службы должны быть перечислены пользователи, которые могут подключаться из Dynamics 365 Finance и Dynamics 365 Supply Chain Management в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="5b9ab-156">Публикация</span><span class="sxs-lookup"><span data-stu-id="5b9ab-156">Publication</span></span>

<span data-ttu-id="5b9ab-157">Среды службы должны быть опубликованы в надстройке электронного выставления накладных, прежде чем их можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="5b9ab-158">Только опубликованные среды могут быть доступны в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="5b9ab-159">Кроме того, среда службы должна быть опубликована, прежде чем все обновления ее атрибутов вступят в силу для службы электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="5b9ab-160">Подключенные приложения</span><span class="sxs-lookup"><span data-stu-id="5b9ab-160">Connected applications</span></span>

<span data-ttu-id="5b9ab-161">Подключенные приложения — это экземпляры Finance и Supply Chain Management, которые могут быть доступны через RCS.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="5b9ab-162">Кроме URL-адреса приложения и его клиента, подключенное приложение содержит учетные данные, позволяющие RCS подключиться к среде.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="5b9ab-163">С помощью подключенных приложений можно настроить часть функции электронного выставления накладных в Finance и Supply Chain Management, чтобы сделать всю работу функции электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="5b9ab-164">Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b9ab-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="5b9ab-165">Интеграция с надстройкой "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="5b9ab-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="5b9ab-166">Прежде чем использовать Finance и Supply Chain Management для выдачи электронных накладных через надстройку электронного выставления накладных, необходимо настроить надстройку на разрешение связи со службой.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="5b9ab-167">Функция интеграции надстройки электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="5b9ab-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="5b9ab-168">Чтобы включить связь между Finance и Supply Chain Management и надстройкой электронного выставления накладных, следует включить функцию **Интеграция надстройки электронного выставления накладных** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="5b9ab-169">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-169">Service endpoint</span></span>

<span data-ttu-id="5b9ab-170">Конечная точка службы — это URL-адрес, по которому расположена надстройка электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="5b9ab-171">Прежде чем можно будет выпускать электронные накладные, необходимо настроить конечную точку службы в Finance и Supply Chain Management, чтобы разрешить связь со службой.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="5b9ab-172">Чтобы настроить конечную точку для службы, перейдите в раздел **Администрирование организации \> Настройка \> Параметр электронных документов** на вкладке **Службы отправки** в поле **URL-адрес надстройки электронного выставления накладных**, введите URL-адрес, как описано в таблице, описанной в разделе **Конечная точка службы**.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="5b9ab-173">Среды</span><span class="sxs-lookup"><span data-stu-id="5b9ab-173">Environments</span></span>

<span data-ttu-id="5b9ab-174">Имя среды, введенное в Finance и Supply Chain Management, относится к имени среды, созданной в RCS и опубликованной в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="5b9ab-175">Среда должна быть настроена на вкладке **Службы отправки** страницы **Параметры электронных документов**, чтобы каждый запрос на выпуск электронных накладных содержал среду, в которой надстройка электронного выставления накладных может определить, какая функция электронного выставления накладных должна обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="5b9ab-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b9ab-176">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b9ab-176">Additional resources</span></span>

- [<span data-ttu-id="5b9ab-177">Настройка электронного выставления накладных в RCS</span><span class="sxs-lookup"><span data-stu-id="5b9ab-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="5b9ab-178">Выпуск электронных накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b9ab-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
