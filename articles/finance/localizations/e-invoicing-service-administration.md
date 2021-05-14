---
title: Компоненты администрирования электронного выставления накладных
description: В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963199"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="3e22f-103">Компоненты администрирования электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3e22f-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3e22f-104">В этой теме приводятся сведения о компонентах, которые относятся к администрированию электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="3e22f-105">Здесь также приводятся сведения о настройке службы электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3e22f-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="3e22f-106">Azure</span><span class="sxs-lookup"><span data-stu-id="3e22f-106">Azure</span></span>

<span data-ttu-id="3e22f-107">Используйте Microsoft Azure для создания секретов для хранилища ключей и учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3e22f-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="3e22f-108">Затем используйте эти секреты в конфигурации электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="3e22f-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3e22f-109">Lifecycle Services</span></span>

<span data-ttu-id="3e22f-110">Используйте Microsoft Dynamics Lifecycle Services (LCS), чтобы включить микрослужбы для вашего проекта развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="3e22f-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="3e22f-111">При установке микрослужбы в LCS требуется как минимум виртуальная машина уровня 2.</span><span class="sxs-lookup"><span data-stu-id="3e22f-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="3e22f-112">Дополнительные сведения о планирования среды см. в разделе [Планирование среды](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="3e22f-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="3e22f-113">Службы Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="3e22f-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="3e22f-114">Dynamics 365 Regulatory Configuration Services (RCS) — это интерфейс, который используется для настройки электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3e22f-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="3e22f-115">Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и размещаются в RCS.</span><span class="sxs-lookup"><span data-stu-id="3e22f-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="3e22f-116">Когда ресурсы готовы, они публикуются в службе электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="3e22f-117">Для регистрации в RCS см [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="3e22f-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="3e22f-118">Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="3e22f-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="3e22f-119">Интеграция с электронным выставлением накладных</span><span class="sxs-lookup"><span data-stu-id="3e22f-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="3e22f-120">Прежде чем можно будет использовать RCS для настройки электронных накладных, необходимо настроить RCS для обеспечения связи с электронным выставлением накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="3e22f-121">Эту настройку можно выполнить на вкладке **Электронное выставление накладных** на странице **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="3e22f-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="3e22f-122">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="3e22f-122">Service endpoint</span></span>

<span data-ttu-id="3e22f-123">Электронное выставление накладных доступно в нескольких географических регионах центра обработки данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3e22f-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="3e22f-124">В приведенной ниже таблице содержится список доступности по регионам.</span><span class="sxs-lookup"><span data-stu-id="3e22f-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="3e22f-125">География центров обработки данных Azure</span><span class="sxs-lookup"><span data-stu-id="3e22f-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="3e22f-126">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="3e22f-126">East US</span></span>                    |
| <span data-ttu-id="3e22f-127">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="3e22f-127">West US</span></span>                    |
| <span data-ttu-id="3e22f-128">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="3e22f-128">North EU</span></span>                   |
| <span data-ttu-id="3e22f-129">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="3e22f-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="3e22f-130">Среды службы</span><span class="sxs-lookup"><span data-stu-id="3e22f-130">Service environments</span></span>

<span data-ttu-id="3e22f-131">Среды службы — это логические разделы, создаваемые для поддержки выполнения функций электронного выставления накладных в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="3e22f-132">Секреты безопасности и цифровые сертификаты, а также руководство (т. е., разрешения доступа) должны быть настроены на уровне среды службы.</span><span class="sxs-lookup"><span data-stu-id="3e22f-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="3e22f-133">Клиенты могут создавать столько сред служб, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="3e22f-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="3e22f-134">Все среды службы, которые создает клиент, независимы друг от друга.</span><span class="sxs-lookup"><span data-stu-id="3e22f-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="3e22f-135">Среды службы должны создаваться и поддерживаться в RCS.</span><span class="sxs-lookup"><span data-stu-id="3e22f-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="3e22f-136">Когда среды службы готовы, они должны быть опубликованы в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="3e22f-137">Состояние среды службы</span><span class="sxs-lookup"><span data-stu-id="3e22f-137">Service environment status</span></span>

<span data-ttu-id="3e22f-138">Управление средами служб осуществляется через их состояние.</span><span class="sxs-lookup"><span data-stu-id="3e22f-138">Service environments can be managed through status.</span></span> <span data-ttu-id="3e22f-139">Возможны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="3e22f-139">The possible options are:</span></span>

- <span data-ttu-id="3e22f-140">**Не опубликовано** — среда создана, но еще не была опубликована.</span><span class="sxs-lookup"><span data-stu-id="3e22f-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="3e22f-141">**Опубликовано** — среда была опубликована в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="3e22f-142">**Изменено** — атрибуты опубликованной среды были изменены, но изменения еще не были опубликованы.</span><span class="sxs-lookup"><span data-stu-id="3e22f-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="3e22f-143">Секреты клиентов</span><span class="sxs-lookup"><span data-stu-id="3e22f-143">Customer secrets</span></span>

<span data-ttu-id="3e22f-144">Служба электронного выставления накладных отвечает за хранение всех ваших деловых данных в ресурсах Azure, принадлежащих вашей компании.</span><span class="sxs-lookup"><span data-stu-id="3e22f-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="3e22f-145">Для обеспечения правильной работы службы и того, что все деловые данные, необходимые для модуля электронного выставления накладных и создаваемые ими, были доступны должным образом, необходимо создать два основных ресурса Azure:</span><span class="sxs-lookup"><span data-stu-id="3e22f-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="3e22f-146">Учетная запись хранилища Azure (хранилище BLOB-объектов), в которой будут храниться электронные накладные</span><span class="sxs-lookup"><span data-stu-id="3e22f-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="3e22f-147">Azure Key Vault, в котором будут храниться сертификаты и универсальный код ресурса (URI) учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="3e22f-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="3e22f-148">Учетная запись Key Vault и хранилища клиента должна быть выделена специально для использования с электронным выставлением накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="3e22f-149">Дополнительные сведения см. в разделе [Создание учетной записи хранения Azure и Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="3e22f-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="3e22f-150">Чтобы отслеживать работоспособность Key Vault и получать оповещения, настройте Azure Monitor для Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3e22f-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="3e22f-151">При включении ведения журнала Key Vault можно отслеживать, как осуществляется доступ к вашим основным хранилищам, когда и насколько доступны Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3e22f-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="3e22f-152">Дополнительные сведения см. в разделе [Мониторинг и оповещение для Azure Key Vault](/azure/key-vault/general/alert) и [Порядок включения ведения журнала Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="3e22f-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="3e22f-153">Рекомендуется периодически изменять секреты.</span><span class="sxs-lookup"><span data-stu-id="3e22f-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="3e22f-154">Дополнительные сведения см. в [документации по секретам](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="3e22f-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="3e22f-155">Пользователи</span><span class="sxs-lookup"><span data-stu-id="3e22f-155">Users</span></span>

<span data-ttu-id="3e22f-156">В каждой среде службы должны быть перечислены пользователи, которые могут подключаться из Dynamics 365 Finance и Dynamics 365 Supply Chain Management в электронном выставлении накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="3e22f-157">Публикация</span><span class="sxs-lookup"><span data-stu-id="3e22f-157">Publication</span></span>

<span data-ttu-id="3e22f-158">Среды службы должны быть опубликованы в модуле электронного выставления накладных, прежде чем их можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="3e22f-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="3e22f-159">Только опубликованные среды могут быть доступны в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e22f-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="3e22f-160">Кроме того, среда службы должна быть опубликована, прежде чем все обновления ее атрибутов вступят в силу для службы электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="3e22f-161">Подключенные приложения</span><span class="sxs-lookup"><span data-stu-id="3e22f-161">Connected applications</span></span>

<span data-ttu-id="3e22f-162">Подключенные приложения — это экземпляры Finance и Supply Chain Management, которые могут быть доступны через RCS.</span><span class="sxs-lookup"><span data-stu-id="3e22f-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="3e22f-163">Кроме URL-адреса приложения и его клиента, подключенное приложение содержит учетные данные, позволяющие RCS подключиться к среде.</span><span class="sxs-lookup"><span data-stu-id="3e22f-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="3e22f-164">С помощью подключенных приложений можно настроить часть функции электронного выставления накладных в Finance и Supply Chain Management, чтобы сделать всю работу функции электронного выставления счетов.</span><span class="sxs-lookup"><span data-stu-id="3e22f-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="3e22f-165">Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e22f-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="3e22f-166">Интеграция с электронным выставлением накладных</span><span class="sxs-lookup"><span data-stu-id="3e22f-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="3e22f-167">Прежде чем использовать Finance и Supply Chain Management для выдачи электронных накладных через модуль электронного выставления накладных, необходимо настроить его на разрешение связи со службой.</span><span class="sxs-lookup"><span data-stu-id="3e22f-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="3e22f-168">Функция интеграции электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="3e22f-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="3e22f-169">Чтобы включить связь между Finance и Supply Chain Management и модулем электронного выставления накладных, следует включить функцию **Интеграция электронного выставления накладных** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="3e22f-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="3e22f-170">Конечная точка службы</span><span class="sxs-lookup"><span data-stu-id="3e22f-170">Service endpoint</span></span>

<span data-ttu-id="3e22f-171">Конечная точка службы — это URL-адрес, по которому расположен модуль электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="3e22f-172">Прежде чем можно будет выпускать электронные накладные, необходимо настроить конечную точку службы в Finance и Supply Chain Management, чтобы разрешить связь со службой.</span><span class="sxs-lookup"><span data-stu-id="3e22f-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="3e22f-173">Чтобы настроить конечную точку для службы, перейдите в раздел **Администрирование организации \> Настройка \> Параметр электронных документов** на вкладке **Службы отправки** в поле **URL-адрес электронного выставления накладных**, введите URL-адрес, как описано в таблице, описанной в разделе **Конечная точка службы**.</span><span class="sxs-lookup"><span data-stu-id="3e22f-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="3e22f-174">Среды</span><span class="sxs-lookup"><span data-stu-id="3e22f-174">Environments</span></span>

<span data-ttu-id="3e22f-175">Имя среды, введенное в Finance и Supply Chain Management, относится к имени среды, созданной в RCS и опубликованной в модуле электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="3e22f-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="3e22f-176">Среда должна быть настроена на вкладке **Службы отправки** страницы **Параметры электронных документов**, чтобы каждый запрос на выпуск электронных накладных содержал среду, в которой модуль электронного выставления накладных может определить, какая функция электронного выставления накладных должна обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="3e22f-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e22f-177">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3e22f-177">Additional resources</span></span>

- [<span data-ttu-id="3e22f-178">Настройка электронного выставления накладных в RCS</span><span class="sxs-lookup"><span data-stu-id="3e22f-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="3e22f-179">Выпуск электронных накладных в Finance и Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e22f-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
