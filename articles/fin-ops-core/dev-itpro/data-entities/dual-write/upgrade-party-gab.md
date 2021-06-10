---
title: Обновление модели субъекта и глобальной адресной книги
description: В этом разделе описывается обновление данных с двойной записью для стороны и модели глобальной адресной книги.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112681"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="816e8-103">Обновление модели субъекта и глобальной адресной книги</span><span class="sxs-lookup"><span data-stu-id="816e8-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="816e8-104">[Шаблон фабрики данных Microsoft Azure](https://aka.ms/dual-write-gab-adf) помогает обновлять существующие данные таблиц **Учетная запись**, **Контактное лицо** и **Поставщик** с двойной записью для стороны и модели глобальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="816e8-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="816e8-105">Шаблон сопоставляет данные обоих приложений Finance and Operations и приложений взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="816e8-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="816e8-106">В конце процесса, поля **Сторона** и **Контактное лицо** для записей **Сторона** будут созданы и связаны с записями **Учетная запись**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="816e8-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="816e8-107">Файл CSV (`FONewParty.csv`) создается для создания новых записей **Сторона** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="816e8-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="816e8-108">В этом разделе представлены инструкции о том, как использовать шаблон фабрики данных и обновлять данные.</span><span class="sxs-lookup"><span data-stu-id="816e8-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="816e8-109">При отсутствии каких-либо настроек можно использовать шаблон как есть.</span><span class="sxs-lookup"><span data-stu-id="816e8-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="816e8-110">Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, необходимо изменить шаблон с помощью следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="816e8-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="816e8-111">Шаблон обновляет только данные **Сторона**.</span><span class="sxs-lookup"><span data-stu-id="816e8-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="816e8-112">В будущих выпусках будут включены почтовый и электронный адрес.</span><span class="sxs-lookup"><span data-stu-id="816e8-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="816e8-113">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="816e8-113">Prerequisites</span></span>

<span data-ttu-id="816e8-114">Для обновления стороны и модели глобальной адресной книги необходимо выполнить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="816e8-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="816e8-115">Подписка Azure</span><span class="sxs-lookup"><span data-stu-id="816e8-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="816e8-116">Доступ к шаблону</span><span class="sxs-lookup"><span data-stu-id="816e8-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="816e8-117">Вы должны быть существующим клиентом с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="816e8-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="816e8-118">Подготовка к обновлению</span><span class="sxs-lookup"><span data-stu-id="816e8-118">Prepare for the upgrade</span></span>
<span data-ttu-id="816e8-119">Для подготовки к обновлению необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="816e8-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="816e8-120">**Полностью синхронизировано**: обе среды полностью синхронизированы для параметров **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик**.</span><span class="sxs-lookup"><span data-stu-id="816e8-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="816e8-121">**Ключи интеграции**: таблицы **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами используют ключи интеграции, которые поставлялись в комплекте.</span><span class="sxs-lookup"><span data-stu-id="816e8-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="816e8-122">При настройке ключей интеграции необходимо настроить шаблон.</span><span class="sxs-lookup"><span data-stu-id="816e8-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="816e8-123">**Номер стороны**: все записи **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик**, для которых будет выполнено обновление, имеют номер **Стороны**.</span><span class="sxs-lookup"><span data-stu-id="816e8-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="816e8-124">Записи без номера **стороны** будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="816e8-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="816e8-125">Если необходимо обновить эти записи, добавьте к ним номер **Стороны** перед началом процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="816e8-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="816e8-126">**Отключение системы**: в ходе процесса обновления вам придется в автономном режиме использовать как среду Finance and Operations, так и среду взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="816e8-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="816e8-127">**Моментальный снимок**: создание моментальных снимков приложений Finance and Operations и приложений взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="816e8-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="816e8-128">При необходимости восстановите предыдущее состояние при помощи моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="816e8-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="816e8-129">Развертывание</span><span class="sxs-lookup"><span data-stu-id="816e8-129">Deployment</span></span>

1. <span data-ttu-id="816e8-130">Загрузите шаблон из [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="816e8-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="816e8-131">Войдите в [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="816e8-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="816e8-132">Создайте [группу ресурсов](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="816e8-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="816e8-133">Создайте [учетную запись хранения](/azure/storage/common/storage-account-create?tabs=azure-portal) в созданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="816e8-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="816e8-134">Создайте [фабрика данных](/azure/data-factory/quickstart-create-data-factory-portal) в созданной ранее группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="816e8-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="816e8-135">Откройте фабрику данных и выберите плитку **Автор и Монитор**.</span><span class="sxs-lookup"><span data-stu-id="816e8-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="816e8-136">На вкладке **Управление** выберите **шаблон ARM**.</span><span class="sxs-lookup"><span data-stu-id="816e8-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="816e8-137">Выберите **Импортировать шаблон ARM**, чтобы импортировать шаблон **Стороны**.</span><span class="sxs-lookup"><span data-stu-id="816e8-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="816e8-138">Импортируйте шаблон в фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-138">Import the template into the data factory.</span></span> <span data-ttu-id="816e8-139">Введите следующие значения для **сведений о проекте** и **сведения об экземпляре**.</span><span class="sxs-lookup"><span data-stu-id="816e8-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="816e8-140">Поле</span><span class="sxs-lookup"><span data-stu-id="816e8-140">Field</span></span> | <span data-ttu-id="816e8-141">значение</span><span class="sxs-lookup"><span data-stu-id="816e8-141">Value</span></span>
    ---|---
    <span data-ttu-id="816e8-142">Подписка</span><span class="sxs-lookup"><span data-stu-id="816e8-142">Subscription</span></span> | <span data-ttu-id="816e8-143">Подписка Azure</span><span class="sxs-lookup"><span data-stu-id="816e8-143">Azure subscription</span></span>
    <span data-ttu-id="816e8-144">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="816e8-144">Resource group</span></span> | <span data-ttu-id="816e8-145">Укажите ресурс, под которым создается учетная запись хранения.</span><span class="sxs-lookup"><span data-stu-id="816e8-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="816e8-146">Область</span><span class="sxs-lookup"><span data-stu-id="816e8-146">Region</span></span> | <span data-ttu-id="816e8-147">Укажите регион.</span><span class="sxs-lookup"><span data-stu-id="816e8-147">Specify region.</span></span>
    <span data-ttu-id="816e8-148">Название фабрики</span><span class="sxs-lookup"><span data-stu-id="816e8-148">Factory Name</span></span> | <span data-ttu-id="816e8-149">Укажите название фабрики.</span><span class="sxs-lookup"><span data-stu-id="816e8-149">Specify factory name.</span></span>
    <span data-ttu-id="816e8-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="816e8-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="816e8-151">Указывается ключ приложения.</span><span class="sxs-lookup"><span data-stu-id="816e8-151">Specify the application's key.</span></span>
    <span data-ttu-id="816e8-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="816e8-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="816e8-153">Строка подключения хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="816e8-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="816e8-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="816e8-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="816e8-155">Пароль для учетной записи пользователя, указанной в качестве имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="816e8-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="816e8-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="816e8-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="816e8-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="816e8-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="816e8-158">Укажите сведения о клиенте (доменное имя или код клиента), под которым приложение будет расположено.</span><span class="sxs-lookup"><span data-stu-id="816e8-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="816e8-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="816e8-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="816e8-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="816e8-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="816e8-161">Указывается идентификатор клиента приложения.</span><span class="sxs-lookup"><span data-stu-id="816e8-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="816e8-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="816e8-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="816e8-163">Имя пользователя для подключения к Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="816e8-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="816e8-164">Дополнительные сведения см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="816e8-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="816e8-165">Ручное распространение шаблона Resource Manager для каждой среды</span><span class="sxs-lookup"><span data-stu-id="816e8-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="816e8-166">Свойства связанной службы</span><span class="sxs-lookup"><span data-stu-id="816e8-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="816e8-167">Копировать данные с помощью Фабрики данных Azure</span><span class="sxs-lookup"><span data-stu-id="816e8-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="816e8-168">После развертывания проверьте наборы данных, поток данных и связанную службу фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Наборы данных, поток данных и связанная служба](media/data-factory-validate.png)

11. <span data-ttu-id="816e8-170">Перейдите к **Управление**.</span><span class="sxs-lookup"><span data-stu-id="816e8-170">Navigate to **Manage**.</span></span> <span data-ttu-id="816e8-171">В **Подключения** выберите **связанная служба**.</span><span class="sxs-lookup"><span data-stu-id="816e8-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="816e8-172">Выберите **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="816e8-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="816e8-173">В форме **Изменение связанной службы (Dynamics CRM)** введите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="816e8-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="816e8-174">Поле</span><span class="sxs-lookup"><span data-stu-id="816e8-174">Field</span></span> | <span data-ttu-id="816e8-175">значение</span><span class="sxs-lookup"><span data-stu-id="816e8-175">Value</span></span>
    ---|---
    <span data-ttu-id="816e8-176">ФИО</span><span class="sxs-lookup"><span data-stu-id="816e8-176">Name</span></span> | <span data-ttu-id="816e8-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="816e8-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="816e8-178">описание</span><span class="sxs-lookup"><span data-stu-id="816e8-178">Description</span></span> | <span data-ttu-id="816e8-179">Связанные службы для подключения к экземпляру CRM для получения данных сущностей</span><span class="sxs-lookup"><span data-stu-id="816e8-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="816e8-180">Подключение через среду выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="816e8-180">Connect via integration runtime</span></span> | <span data-ttu-id="816e8-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="816e8-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="816e8-182">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="816e8-182">Deployment type</span></span> | <span data-ttu-id="816e8-183">Интерактивный режим</span><span class="sxs-lookup"><span data-stu-id="816e8-183">Online</span></span>
    <span data-ttu-id="816e8-184">URI службы</span><span class="sxs-lookup"><span data-stu-id="816e8-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="816e8-185">Тип проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="816e8-185">Authentication type</span></span> | <span data-ttu-id="816e8-186">Office365</span><span class="sxs-lookup"><span data-stu-id="816e8-186">Office365</span></span>
    <span data-ttu-id="816e8-187">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="816e8-187">User name</span></span> |
    <span data-ttu-id="816e8-188">Пароль или Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="816e8-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="816e8-189">Пароль</span><span class="sxs-lookup"><span data-stu-id="816e8-189">Password</span></span>
    <span data-ttu-id="816e8-190">Пароль</span><span class="sxs-lookup"><span data-stu-id="816e8-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="816e8-191">Выполните шаблон</span><span class="sxs-lookup"><span data-stu-id="816e8-191">Run the template</span></span>

1. <span data-ttu-id="816e8-192">Остановите сопоставления двойной записи **Учетная запись**, **Контактное лицо** и **Поставщик** с помощью приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="816e8-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="816e8-193">Клиенты V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="816e8-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="816e8-194">Клиенты V3 (контакты)</span><span class="sxs-lookup"><span data-stu-id="816e8-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="816e8-195">CDS Контакты V2 (контакты)</span><span class="sxs-lookup"><span data-stu-id="816e8-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="816e8-196">CDS Контакты V2 (контакты)</span><span class="sxs-lookup"><span data-stu-id="816e8-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="816e8-197">Поставщик V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="816e8-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="816e8-198">Убедитесь, что сопоставления удалены из таблицы `msdy_dualwriteruntimeconfig` в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="816e8-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="816e8-199">Установка [решений стороны с двойной записью и глобальной адресной книги](https://aka.ms/dual-write-gab) из AppSource.</span><span class="sxs-lookup"><span data-stu-id="816e8-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="816e8-200">В приложении Finance and Operations, если следующие таблицы содержат данные, выполните действие **Начальная синхронизация** для них.</span><span class="sxs-lookup"><span data-stu-id="816e8-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="816e8-201">Приветствия</span><span class="sxs-lookup"><span data-stu-id="816e8-201">Salutations</span></span>
    + <span data-ttu-id="816e8-202">Типы характеров людей</span><span class="sxs-lookup"><span data-stu-id="816e8-202">Personal character types</span></span>
    + <span data-ttu-id="816e8-203">Заключение</span><span class="sxs-lookup"><span data-stu-id="816e8-203">Complimentary closing</span></span>
    + <span data-ttu-id="816e8-204">Обращения к контактному лицу</span><span class="sxs-lookup"><span data-stu-id="816e8-204">Contact person titles</span></span>
    + <span data-ttu-id="816e8-205">Роли принятия решений</span><span class="sxs-lookup"><span data-stu-id="816e8-205">Decision making roles</span></span>
    + <span data-ttu-id="816e8-206">Уровни лояльности</span><span class="sxs-lookup"><span data-stu-id="816e8-206">Loyalty levels</span></span>

5. <span data-ttu-id="816e8-207">В приложении взаимодействия с клиентами отключите следующие шаги подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="816e8-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="816e8-208">Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-208">Account Update</span></span>
         + <span data-ttu-id="816e8-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="816e8-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="816e8-211">Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-211">Contact Update</span></span>
         + <span data-ttu-id="816e8-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="816e8-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="816e8-214">Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="816e8-214">msdyn_party Update</span></span>
         + <span data-ttu-id="816e8-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="816e8-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="816e8-216">Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="816e8-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="816e8-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="816e8-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="816e8-218">В приложении взаимодействия с клиентами отключите следующие workflow-процессы:</span><span class="sxs-lookup"><span data-stu-id="816e8-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="816e8-219">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-220">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-221">Создание поставщиков типа "респондент" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="816e8-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="816e8-222">Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="816e8-223">Обновление поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-224">Обновление поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="816e8-225">Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="816e8-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="816e8-226">Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="816e8-227">В фабрике данных выполните шаблон, выбрав **Активировать сейчас**, как показано на следующем изображении.</span><span class="sxs-lookup"><span data-stu-id="816e8-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="816e8-228">Этот процесс может занять несколько часов в зависимости от объема данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Активировать выполнение](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="816e8-230">Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, требуется изменить шаблон.</span><span class="sxs-lookup"><span data-stu-id="816e8-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="816e8-231">Импортируйте новые записи **Стороны** в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="816e8-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="816e8-232">Загрузите файл `FONewParty.csv` из хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="816e8-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="816e8-233">Путь `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="816e8-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="816e8-234">Преобразуйте файл `FONewParty.csv` в файл Excel и импортируйте файл Excel в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="816e8-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="816e8-235">Если вам подходит импорт csv, можно напрямую импортировать файл CSV.</span><span class="sxs-lookup"><span data-stu-id="816e8-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="816e8-236">Для выполнения импорта может потребоваться несколько часов, в зависимости от объема данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="816e8-237">Дополнительные сведения см. в разделе [Обзор заданий импорта и экспорта данных](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="816e8-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Импорт записей стороны Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="816e8-239">В приложениях взаимодействия с клиентами включите следующие шаги подключаемого модуля:</span><span class="sxs-lookup"><span data-stu-id="816e8-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="816e8-240">Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-240">Account Update</span></span>
         + <span data-ttu-id="816e8-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="816e8-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="816e8-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="816e8-243">Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-243">Contact Update</span></span>
         + <span data-ttu-id="816e8-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="816e8-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="816e8-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="816e8-246">Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="816e8-246">msdyn_party Update</span></span>
         + <span data-ttu-id="816e8-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="816e8-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="816e8-248">Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="816e8-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="816e8-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="816e8-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="816e8-250">В приложениях взаимодействия с клиентами активируйте следующие workflow-процессы, если они были деактивированы в предыдущих шагах:</span><span class="sxs-lookup"><span data-stu-id="816e8-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="816e8-251">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-252">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-253">Создание поставщиков типа "респондент" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="816e8-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="816e8-254">Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="816e8-255">Обновление поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="816e8-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="816e8-256">Обновление поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="816e8-257">Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="816e8-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="816e8-258">Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="816e8-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="816e8-259">Выполните сопоставления, связанные с **Стороной**, в соответствии с указаниями в [Сторона и глобальная адресная книга](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="816e8-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="816e8-260">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="816e8-260">Troubleshooting</span></span>

1. <span data-ttu-id="816e8-261">В случае сбоя процесса перезапустите фабрику данных, начиная с невыполненного действия.</span><span class="sxs-lookup"><span data-stu-id="816e8-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="816e8-262">Некоторые файлы создаются фабрикой данных, которую можно использовать для целей проверки данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="816e8-263">Фабрика данных выполняется на основе файлов CSV, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="816e8-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="816e8-264">Если имеется значение поля с запятой, оно может повлиять на результаты.</span><span class="sxs-lookup"><span data-stu-id="816e8-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="816e8-265">Необходимо удалить запятые.</span><span class="sxs-lookup"><span data-stu-id="816e8-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="816e8-266">Вкладка **Мониторинг** содержит сведения обо всех шагах и обработанных данных.</span><span class="sxs-lookup"><span data-stu-id="816e8-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="816e8-267">Выбор конкретного шага для его отладки.</span><span class="sxs-lookup"><span data-stu-id="816e8-267">Select a specific step to debug it.</span></span>

    ![Вкладка "Мониторинг"](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="816e8-269">Дополнительные сведения о шаблоне</span><span class="sxs-lookup"><span data-stu-id="816e8-269">Learn more about the template</span></span>

<span data-ttu-id="816e8-270">Дополнительные сведения о шаблоне можно найти в [комментариях к файлу сведений для шаблона фабрики данных Azure](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="816e8-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
