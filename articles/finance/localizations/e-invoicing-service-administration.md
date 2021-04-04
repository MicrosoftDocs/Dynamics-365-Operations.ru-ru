---
title: Компоненты администрирования надстройки электронного выставления счетов
description: В этой теме приводятся сведения о компонентах, которые относятся к администрированию надстройки электронного выставления накладных.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592582"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="e8a9a-103">Компоненты администрирования надстройки электронного выставления счетов</span><span class="sxs-lookup"><span data-stu-id="e8a9a-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e8a9a-104">В этой теме приводятся сведения о компонентах, которые относятся к администрированию надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="e8a9a-105">Здесь также приводятся сведения о настройке службы надстройки электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="e8a9a-106">Azure</span><span class="sxs-lookup"><span data-stu-id="e8a9a-106">Azure</span></span>

<span data-ttu-id="e8a9a-107">Используйте Microsoft Azure для создания секретов для хранилища ключей и учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="e8a9a-108">Затем используйте эти секреты в конфигурации надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="e8a9a-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e8a9a-109">Lifecycle Services</span></span>

<span data-ttu-id="e8a9a-110">Используйте Microsoft Dynamics Lifecycle Services (LCS), чтобы включить надстройку для микрослужб вашего проекта развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="e8a9a-111">При установке надстройки "микрослужба" в LCS требуется как минимум виртуальная машина уровня 2.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="e8a9a-112">Дополнительные сведения о планирования среды см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e8a9a-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="e8a9a-113">Службы Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="e8a9a-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="e8a9a-114">Dynamics 365 Regulatory Configuration Services (RCS) — это интерфейс, который используется для настройки надстройки электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="e8a9a-115">Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и размещаются в RCS.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="e8a9a-116">Когда ресурсы готовы, они публикуются в службе надстройки электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="e8a9a-117">Для регистрации в RCS см [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="e8a9a-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="e8a9a-118">Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="e8a9a-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="e8a9a-119">Интеграция с надстройкой "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="e8a9a-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="e8a9a-120">Прежде чем можно будет использовать RCS для настройки электронных накладных, необходимо настроить RCS для обеспечения связи с надстройкой электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="e8a9a-121">Эту настройку можно выполнить на вкладке **Надстройка электронного выставления накладных** на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e8a9a-122">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="e8a9a-122">Service endpoint</span></span>

<span data-ttu-id="e8a9a-123">Надстройка электронных накладных доступна в нескольких географических регионах центра обработки данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="e8a9a-124">В приведенной ниже таблице содержится список доступности по регионам.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="e8a9a-125">География центров обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="e8a9a-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="e8a9a-126">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="e8a9a-126">East US</span></span>                    |
| <span data-ttu-id="e8a9a-127">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="e8a9a-127">West US</span></span>                    |
| <span data-ttu-id="e8a9a-128">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="e8a9a-128">North EU</span></span>                   |
| <span data-ttu-id="e8a9a-129">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="e8a9a-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="e8a9a-130">Среды службы</span><span class="sxs-lookup"><span data-stu-id="e8a9a-130">Service environments</span></span>

<span data-ttu-id="e8a9a-131">Среды службы — это логические разделы, создаваемые для поддержки выполнения функций электронного выставления накладных в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="e8a9a-132">Секреты безопасности и цифровые сертификаты, а также руководство (т. е., разрешения доступа) должны быть настроены на уровне среды службы.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="e8a9a-133">Клиенты могут создавать столько сред служб, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="e8a9a-134">Все среды службы, которые создает клиент, независимы друг от друга.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="e8a9a-135">Среды службы должны создаваться и поддерживаться в RCS.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="e8a9a-136">Когда среды службы готовы, они должны быть опубликованы в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="e8a9a-137">Состояние среды службы</span><span class="sxs-lookup"><span data-stu-id="e8a9a-137">Service environment status</span></span>

<span data-ttu-id="e8a9a-138">Управление средами служб осуществляется через их состояние.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-138">Service environments can be managed through status.</span></span> <span data-ttu-id="e8a9a-139">Возможны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="e8a9a-139">The possible options are:</span></span>

- <span data-ttu-id="e8a9a-140">**Не опубликовано** — среда создана, но еще не была опубликована.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="e8a9a-141">**Опубликовано** — среда была опубликована в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="e8a9a-142">**Изменено** — атрибуты опубликованной среды были изменены, но изменения еще не были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="e8a9a-143">Секреты клиентов</span><span class="sxs-lookup"><span data-stu-id="e8a9a-143">Customer secrets</span></span>

<span data-ttu-id="e8a9a-144">Служба надстройки электронного выставления накладных отвечает за хранение всех ваших деловых данных в ресурсах Azure, принадлежащих вашей компании.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="e8a9a-145">Для обеспечения правильной работы службы и того, что все деловые данные, необходимые для дополнения электронных накладных и создаваемые этим дополнением, доступны только для этого дополнения, необходимо создать два основных ресурса Azure:</span><span class="sxs-lookup"><span data-stu-id="e8a9a-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="e8a9a-146">Учетная запись хранилища Azure (хранилище BLOB-объектов), в которой будут храниться электронные накладные</span><span class="sxs-lookup"><span data-stu-id="e8a9a-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="e8a9a-147">Хранилище ключей Azure, в котором будут храниться сертификаты и универсальный код ресурса (URI) учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="e8a9a-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="e8a9a-148">Учетная запись хранилища ключей и хранилища BLOB-объектов клиента должна быть выделена специально для использования с дополнением электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e8a9a-149">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e8a9a-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="e8a9a-150">Пользователи</span><span class="sxs-lookup"><span data-stu-id="e8a9a-150">Users</span></span>

<span data-ttu-id="e8a9a-151">В каждой среде службы должны быть перечислены пользователи, которые могут подключаться из Dynamics 365 Finance и Dynamics 365 Supply Chain Management в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="e8a9a-152">Публикация</span><span class="sxs-lookup"><span data-stu-id="e8a9a-152">Publication</span></span>

<span data-ttu-id="e8a9a-153">Среды службы должны быть опубликованы в надстройке электронного выставления накладных, прежде чем их можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="e8a9a-154">Только опубликованные среды могут быть доступны в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="e8a9a-155">Кроме того, среда службы должна быть опубликована, прежде чем все обновления ее атрибутов вступят в силу для службы электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="e8a9a-156">Подключенные приложения</span><span class="sxs-lookup"><span data-stu-id="e8a9a-156">Connected applications</span></span>

<span data-ttu-id="e8a9a-157">Подключенные приложения — это экземпляры Finance и Supply Chain Management, которые могут быть доступны через RCS.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="e8a9a-158">Кроме URL-адреса приложения и его клиента, подключенное приложение содержит учетные данные, позволяющие RCS подключиться к среде.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="e8a9a-159">С помощью подключенных приложений можно настроить часть функции электронного выставления накладных в Finance и Supply Chain Management, чтобы сделать всю работу функции электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="e8a9a-160">Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8a9a-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="e8a9a-161">Интеграция с надстройкой "Электронное выставление счетов"</span><span class="sxs-lookup"><span data-stu-id="e8a9a-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="e8a9a-162">Прежде чем использовать Finance и Supply Chain Management для выдачи электронных накладных через надстройку электронного выставления накладных, необходимо настроить надстройку на разрешение связи со службой.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="e8a9a-163">Функция интеграции надстройки электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="e8a9a-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="e8a9a-164">Чтобы включить связь между Finance и Supply Chain Management и надстройкой электронного выставления накладных, следует включить функцию **Интеграция надстройки электронного выставления накладных** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e8a9a-165">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="e8a9a-165">Service endpoint</span></span>

<span data-ttu-id="e8a9a-166">Конечная точка службы — это URL-адрес, по которому расположена надстройка электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="e8a9a-167">Прежде чем можно будет выпускать электронные накладные, необходимо настроить конечную точку службы в Finance и Supply Chain Management, чтобы разрешить связь со службой.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="e8a9a-168">Чтобы настроить конечную точку для службы, перейдите в раздел **Администрирование организации \> Настройка \> Параметр электронных документов** на вкладке **Службы отправки** в поле **URL-адрес надстройки электронного выставления накладных**, введите URL-адрес, как описано в таблице, описанной в разделе **Конечная точка службы**.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="e8a9a-169">Среды</span><span class="sxs-lookup"><span data-stu-id="e8a9a-169">Environments</span></span>

<span data-ttu-id="e8a9a-170">Имя среды, введенное в Finance и Supply Chain Management, относится к имени среды, созданной в RCS и опубликованной в надстройке электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e8a9a-171">Среда должна быть настроена на вкладке **Службы отправки** страницы **Параметры электронных документов**, чтобы каждый запрос на выпуск электронных накладных содержал среду, в которой надстройка электронного выставления накладных может определить, какая функция электронного выставления накладных должна обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8a9a-172">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e8a9a-172">Additional resources</span></span>

- [<span data-ttu-id="e8a9a-173">Настройка электронного выставления накладных в RCS</span><span class="sxs-lookup"><span data-stu-id="e8a9a-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="e8a9a-174">Выпуск электронных накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8a9a-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
