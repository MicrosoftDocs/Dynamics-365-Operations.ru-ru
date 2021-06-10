---
title: Вопросы и ответы по вводу в эксплуатацию
description: В этой теме перечислены часто задаваемые вопросы о том, как ввести в эксплуатацию проект реализации Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 550e094fd34bfbdc66665be2ceed306de722c0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055348"
---
# <a name="go-live-faq"></a><span data-ttu-id="f9b67-103">Вопросы и ответы по вводу в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="f9b67-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f9b67-104">В этой теме перечислены часто задаваемые вопросы о том, как ввести в эксплуатацию проект реализации Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f9b67-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="f9b67-105">Когда можно настроить и запросить производственную среду?</span><span class="sxs-lookup"><span data-stu-id="f9b67-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="f9b67-106">Обычно производственная среда разворачивается после того, как удовлетворяются следующие критерии:</span><span class="sxs-lookup"><span data-stu-id="f9b67-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="f9b67-107">Код всех настроек завершен.</span><span class="sxs-lookup"><span data-stu-id="f9b67-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="f9b67-108">Приемочное тестирование пользователем (UAT) завершено.</span><span class="sxs-lookup"><span data-stu-id="f9b67-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="f9b67-109">Клиент утвердил решение.</span><span class="sxs-lookup"><span data-stu-id="f9b67-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="f9b67-110">Нет блокирующих проблем для ввода в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="f9b67-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="f9b67-111">Если на данном этапе имеются квалифицированные клиенты, группа Microsoft FastTrack будет работать с группой проекта, чтобы выполнить оценку ввода в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="f9b67-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="f9b67-112">Какие необходимые условия для развертывания производственной среды?</span><span class="sxs-lookup"><span data-stu-id="f9b67-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="f9b67-113">Список необходимых требований см. в разделе  [Подготовка к вводу в эксплуатацию](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="f9b67-114">Что такое оценка ввода в эксплуатацию?</span><span class="sxs-lookup"><span data-stu-id="f9b67-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="f9b67-115">Оценка ввода в эксплуатацию является частью  [программы Microsoft FastTrack](/dynamics365/fasttrack/).</span><span class="sxs-lookup"><span data-stu-id="f9b67-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="f9b67-116">Во время этого рассмотрения архитектор решений оценивает, готов ли проект реализации к успешному переключению и вводу в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="f9b67-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="f9b67-117">Эта проверка является обязательной для каждого проекта реализации до того, как вы сможете запросить ввод в эксплуатацию в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="f9b67-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="f9b67-118">Наши среды в песочнице развернуты в центре обработки данных в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="f9b67-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="f9b67-119">Мы хотим, чтобы наши производственные среды были развернуты в центре обработки данных в западной части США.</span><span class="sxs-lookup"><span data-stu-id="f9b67-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="f9b67-120">Можно ли выбрать западную часть США в качестве центра обработки данных в моей производственной конфигурации?</span><span class="sxs-lookup"><span data-stu-id="f9b67-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="f9b67-121">LCS не ограничивает выбор других центров обработки данных при развертывании среды Human Resources, но настоятельно не рекомендуется выбирать другой центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="f9b67-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="f9b67-122">Если требуется, чтобы производственная среда была в центре обработки данных в западной части США, необходимо сначала заново развернуть среды в песочнице в центре обработки данных в западной части США, проверить их и утвердить.</span><span class="sxs-lookup"><span data-stu-id="f9b67-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="f9b67-123">Сведения о выборе правильного центра обработки данных см. в разделе [Требования к сети](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="f9b67-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="f9b67-124">Какой уровень доступа требуется для ресурсов Azure в моих средах Human Resources?</span><span class="sxs-lookup"><span data-stu-id="f9b67-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="f9b67-125">Доступ к средам Human Resources ограничивается.</span><span class="sxs-lookup"><span data-stu-id="f9b67-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="f9b67-126">У вас нет доступа к виртуальной машине (VM) или Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="f9b67-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="f9b67-127">Доступ к базе данных также невозможен через Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="f9b67-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="f9b67-128">Хотя непосредственное обращение к вашим ресурсам Azure или среде Dynamics 365 Human Resources, можно использовать дополнительные функции для доступа к данным:</span><span class="sxs-lookup"><span data-stu-id="f9b67-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="f9b67-129">Можно развернуть базу данных SQL Azure в своем собственном клиенте Azure и использовать функцию "назначить собственную базу данных" (BYOD) для синхронизации данных.</span><span class="sxs-lookup"><span data-stu-id="f9b67-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="f9b67-130">Дополнительные сведения см. в разделе [Использование собственной базы данных (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="f9b67-131">Можно использовать интеграцию Dataverse для синхронизации выбранных сущностей в базе данных Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f9b67-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="f9b67-132">Дополнительные сведения см. в разделе [Таблицы Dataverse](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="f9b67-133">Как часто архивируется моя производственная база данных?</span><span class="sxs-lookup"><span data-stu-id="f9b67-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="f9b67-134">Базы данных защищаются автоматическим созданием резервных копий при следующих частотах:</span><span class="sxs-lookup"><span data-stu-id="f9b67-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="f9b67-135">Тип резервного копирования</span><span class="sxs-lookup"><span data-stu-id="f9b67-135">Type of backup</span></span> | <span data-ttu-id="f9b67-136">Частота</span><span class="sxs-lookup"><span data-stu-id="f9b67-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="f9b67-137">Полная резервная копия баз данных</span><span class="sxs-lookup"><span data-stu-id="f9b67-137">Full database backup</span></span> | <span data-ttu-id="f9b67-138">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="f9b67-138">Weekly</span></span> |
| <span data-ttu-id="f9b67-139">Разностная резервная копия баз данных</span><span class="sxs-lookup"><span data-stu-id="f9b67-139">Differential database backup</span></span> | <span data-ttu-id="f9b67-140">Каждые 12–24 часа</span><span class="sxs-lookup"><span data-stu-id="f9b67-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="f9b67-141">Резервное копирование журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="f9b67-141">Transaction log backup</span></span> | <span data-ttu-id="f9b67-142">Каждые 5–10 минут</span><span class="sxs-lookup"><span data-stu-id="f9b67-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="f9b67-143">Корпорация Майкрософт сохраняет необходимые резервные копии, чтобы иметь возможность восстановления до точки во времени (PITR) в течение последних 14 дней.</span><span class="sxs-lookup"><span data-stu-id="f9b67-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="f9b67-144">Дополнительные сведения см. в разделе  [Подробнее об автоматически создаваемых резервных копиях в базе данных SQL](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="f9b67-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="f9b67-145">Можно ли запросить копию резервной копии производственной базы данных?</span><span class="sxs-lookup"><span data-stu-id="f9b67-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="f9b67-146">№ п/п</span><span class="sxs-lookup"><span data-stu-id="f9b67-146">No.</span></span> <span data-ttu-id="f9b67-147">Однако можно отправить запрос на обслуживание обновления базы данных, чтобы скопировать свою производственную среду в среду "песочницы".</span><span class="sxs-lookup"><span data-stu-id="f9b67-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="f9b67-148">Можно развернуть базу данных SQL Azure в своем собственном клиенте Azure и использовать функцию BYOD для синхронизации данных из производственной среды.</span><span class="sxs-lookup"><span data-stu-id="f9b67-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="f9b67-149">Дополнительные сведения см. в разделе [Использование собственной базы данных (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="f9b67-150">Как переместить среду "песочницы" в производство для ввода в эксплуатацию?</span><span class="sxs-lookup"><span data-stu-id="f9b67-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="f9b67-151">Поскольку функция копирования недоступна для переноса среды из среды песочницы в производственную среду, необходимо использовать пакеты данных для переноса данных в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="f9b67-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="f9b67-152">Рекомендуется поддерживать четкий список сущностей, настроенных в вашей среде песочницы в течение всего проекта.</span><span class="sxs-lookup"><span data-stu-id="f9b67-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="f9b67-153">Затем проверьте процесс переключения и миграцию каких-либо пакетов данных, необходимых для ввода в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="f9b67-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="f9b67-154">Необходимо вручную переместить любые пакеты данных в производственную среду, когда будете готовы к вводу в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="f9b67-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="f9b67-155">Что делать, если производственная среда не работает?</span><span class="sxs-lookup"><span data-stu-id="f9b67-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="f9b67-156">Чтобы сообщить об отключении производственной среды, следуйте процедуре, описанной в разделе  [Отчет об отключении производства](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="f9b67-157">См. также</span><span class="sxs-lookup"><span data-stu-id="f9b67-157">See also</span></span>

 [<span data-ttu-id="f9b67-158">Подготовка к вводу в эксплуатацию</span><span class="sxs-lookup"><span data-stu-id="f9b67-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]