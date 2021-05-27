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
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018320"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="aeb00-103">Обновление модели субъекта и глобальной адресной книги</span><span class="sxs-lookup"><span data-stu-id="aeb00-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="aeb00-104">[Шаблон фабрики данных Azure](https://aka.ms/dual-write-gab-adf) помогает обновлять существующие данные таблиц **Учетная запись**, **Контактное лицо** и **Поставщик** с двойной записью для стороны и модели глобальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="aeb00-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="aeb00-105">Шаблон сопоставляет данные обоих приложений Finance and Operations и приложений взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="aeb00-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="aeb00-106">В конце процесса, поля **Сторона** и **Контактное лицо** для записей **Сторона** будут созданы и связаны с записями **Учетная запись**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="aeb00-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="aeb00-107">Файл CSV (`FONewParty.csv`) создается для создания новых записей **Сторона** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aeb00-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="aeb00-108">В этом разделе представлены инструкции по использованию шаблона Фабрики данных и обновлению данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="aeb00-109">При отсутствии каких-либо настроек можно использовать шаблон как есть.</span><span class="sxs-lookup"><span data-stu-id="aeb00-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="aeb00-110">Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, необходимо изменить шаблон с помощью следующих инструкций.</span><span class="sxs-lookup"><span data-stu-id="aeb00-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="aeb00-111">Шаблон помогает обновить только данные **Сторона**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="aeb00-112">В будущих выпусках будут включены почтовый и электронный адрес.</span><span class="sxs-lookup"><span data-stu-id="aeb00-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aeb00-113">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="aeb00-113">Prerequisites</span></span>

<span data-ttu-id="aeb00-114">Эти необходимые условия необходимы:</span><span class="sxs-lookup"><span data-stu-id="aeb00-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="aeb00-115">Подписка Azure</span><span class="sxs-lookup"><span data-stu-id="aeb00-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="aeb00-116">Доступ к шаблону</span><span class="sxs-lookup"><span data-stu-id="aeb00-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="aeb00-117">Вы являетесь существующим клиентом с двойной записью.</span><span class="sxs-lookup"><span data-stu-id="aeb00-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="aeb00-118">Подготовка к обновлению</span><span class="sxs-lookup"><span data-stu-id="aeb00-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="aeb00-119">**Полностью синхронизировано**: обе среды полностью синхронизированы для **Учетная запись (клиент)**, **Контактное лицо** и **Поставщика**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="aeb00-120">**Ключи интеграции**: таблицы **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик** в приложениях взаимодействия с клиентами используют ключи интеграции, которые поставлялись в комплекте.</span><span class="sxs-lookup"><span data-stu-id="aeb00-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="aeb00-121">При настройке ключей интеграции необходимо настроить шаблон.</span><span class="sxs-lookup"><span data-stu-id="aeb00-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="aeb00-122">**Номер стороны**: все записи **Учетная запись (клиент)**, **Контактное лицо** и **Поставщик**, для которых будет выполнено обновление, имеют номер **Стороны**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="aeb00-123">Записи без номера **стороны** будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="aeb00-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="aeb00-124">Если необходимо обновить эти записи, добавьте к ним номер **Стороны** перед началом процесса обновления.</span><span class="sxs-lookup"><span data-stu-id="aeb00-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="aeb00-125">**Отключение системы**: в ходе процесса обновления вам придется в автономном режиме использовать как среду Finance and Operations, так и среду взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="aeb00-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="aeb00-126">**Моментальный снимок**: создание моментальных снимков Finance and Operations и приложений взаимодействия с клиентами.</span><span class="sxs-lookup"><span data-stu-id="aeb00-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="aeb00-127">При необходимости восстановите предыдущее состояние при помощи моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="aeb00-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="aeb00-128">Развертывание</span><span class="sxs-lookup"><span data-stu-id="aeb00-128">Deployment</span></span>

1. <span data-ttu-id="aeb00-129">Загрузите шаблон из [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="aeb00-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="aeb00-130">Войдите в [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="aeb00-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="aeb00-131">Создайте [группу ресурсов](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="aeb00-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="aeb00-132">Создайте [учетную запись хранения](/azure/storage/common/storage-account-create?tabs=azure-portal) в созданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aeb00-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="aeb00-133">Создайте [фабрика данных](/azure/data-factory/quickstart-create-data-factory-portal) в созданной ранее группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aeb00-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="aeb00-134">Откройте фабрику данных и выберите плитку **Автор и Монитор**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="aeb00-135">На вкладке **Управление** выберите **шаблон ARM**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="aeb00-136">Выберите **Импортировать шаблон ARM**, чтобы импортировать шаблон **Стороны**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="aeb00-137">Импортируйте шаблон в фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-137">Import the template into the data factory.</span></span> <span data-ttu-id="aeb00-138">Введите следующие значения для **сведений о проекте** и **сведения об экземпляре**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="aeb00-139">Поле</span><span class="sxs-lookup"><span data-stu-id="aeb00-139">Field</span></span> | <span data-ttu-id="aeb00-140">значение</span><span class="sxs-lookup"><span data-stu-id="aeb00-140">Value</span></span>
    ---|---
    <span data-ttu-id="aeb00-141">Подписка</span><span class="sxs-lookup"><span data-stu-id="aeb00-141">Subscription</span></span> | <span data-ttu-id="aeb00-142">Подписка Azure</span><span class="sxs-lookup"><span data-stu-id="aeb00-142">Azure subscription</span></span>
    <span data-ttu-id="aeb00-143">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="aeb00-143">Resource group</span></span> | <span data-ttu-id="aeb00-144">Укажите ресурс, под которым создается учетная запись хранения.</span><span class="sxs-lookup"><span data-stu-id="aeb00-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="aeb00-145">Область</span><span class="sxs-lookup"><span data-stu-id="aeb00-145">Region</span></span> | <span data-ttu-id="aeb00-146">Укажите регион.</span><span class="sxs-lookup"><span data-stu-id="aeb00-146">Specify region.</span></span>
    <span data-ttu-id="aeb00-147">Название фабрики</span><span class="sxs-lookup"><span data-stu-id="aeb00-147">Factory Name</span></span> | <span data-ttu-id="aeb00-148">Укажите название фабрики.</span><span class="sxs-lookup"><span data-stu-id="aeb00-148">Specify factory name.</span></span>
    <span data-ttu-id="aeb00-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="aeb00-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="aeb00-150">Указывается ключ приложения.</span><span class="sxs-lookup"><span data-stu-id="aeb00-150">Specify the application's key.</span></span>
    <span data-ttu-id="aeb00-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="aeb00-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="aeb00-152">Строка подключения хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb00-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="aeb00-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="aeb00-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="aeb00-154">Пароль для учетной записи пользователя, указанной в качестве имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="aeb00-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="aeb00-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="aeb00-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="aeb00-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="aeb00-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="aeb00-157">Укажите сведения о клиенте (доменное имя или код клиента), под которым приложение будет расположено.</span><span class="sxs-lookup"><span data-stu-id="aeb00-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="aeb00-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="aeb00-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="aeb00-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="aeb00-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="aeb00-160">Указывается идентификатор клиента приложения.</span><span class="sxs-lookup"><span data-stu-id="aeb00-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="aeb00-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="aeb00-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="aeb00-162">Имя пользователя для подключения к Dynamics.</span><span class="sxs-lookup"><span data-stu-id="aeb00-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="aeb00-163">Дополнительные сведения см. в [Ручное распространение шаблона Resource Manager для каждой среды](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Связанные свойства службы](/azure/data-factory/connector-dynamics-ax#linked-service-properties) и [Копировать данные с помощью Фабрики данных Azure](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="aeb00-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="aeb00-164">После развертывания проверьте наборы данных, поток данных и связанную службу фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Наборы данных, поток данных и связанная служба](media/data-factory-validate.png)

11. <span data-ttu-id="aeb00-166">Перейдите к **Управление**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-166">Navigate to **Manage**.</span></span> <span data-ttu-id="aeb00-167">В **Подключения** выберите **связанная служба**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="aeb00-168">Выберите **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="aeb00-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="aeb00-169">В форме **Изменение связанной службы (Dynamics CRM)** введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aeb00-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="aeb00-170">Поле</span><span class="sxs-lookup"><span data-stu-id="aeb00-170">Field</span></span> | <span data-ttu-id="aeb00-171">значение</span><span class="sxs-lookup"><span data-stu-id="aeb00-171">Value</span></span>
    ---|---
    <span data-ttu-id="aeb00-172">ФИО</span><span class="sxs-lookup"><span data-stu-id="aeb00-172">Name</span></span> | <span data-ttu-id="aeb00-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="aeb00-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="aeb00-174">описание</span><span class="sxs-lookup"><span data-stu-id="aeb00-174">Description</span></span> | <span data-ttu-id="aeb00-175">Связанные службы для подключения к экземпляру CRM для получения данных сущностей</span><span class="sxs-lookup"><span data-stu-id="aeb00-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="aeb00-176">Подключение через среду выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="aeb00-176">Connect via integration runtime</span></span> | <span data-ttu-id="aeb00-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="aeb00-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="aeb00-178">Тип развертывания</span><span class="sxs-lookup"><span data-stu-id="aeb00-178">Deployment type</span></span> | <span data-ttu-id="aeb00-179">Интерактивный режим</span><span class="sxs-lookup"><span data-stu-id="aeb00-179">Online</span></span>
    <span data-ttu-id="aeb00-180">URI службы</span><span class="sxs-lookup"><span data-stu-id="aeb00-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="aeb00-181">Тип проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="aeb00-181">Authentication type</span></span> | <span data-ttu-id="aeb00-182">Office365</span><span class="sxs-lookup"><span data-stu-id="aeb00-182">Office365</span></span>
    <span data-ttu-id="aeb00-183">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="aeb00-183">User name</span></span> |
    <span data-ttu-id="aeb00-184">Пароль или Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="aeb00-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="aeb00-185">Пароль</span><span class="sxs-lookup"><span data-stu-id="aeb00-185">Password</span></span>
    <span data-ttu-id="aeb00-186">Пароль</span><span class="sxs-lookup"><span data-stu-id="aeb00-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="aeb00-187">Выполните шаблон</span><span class="sxs-lookup"><span data-stu-id="aeb00-187">Run the template</span></span>

1. <span data-ttu-id="aeb00-188">Остановите следующую двойную запись **Учетная запись**, **Контактное лицо** и **Поставщик** с помощью приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aeb00-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="aeb00-189">Клиенты V3 (accounts)</span><span class="sxs-lookup"><span data-stu-id="aeb00-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="aeb00-190">Клиенты V3 (контакты)</span><span class="sxs-lookup"><span data-stu-id="aeb00-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="aeb00-191">CDS Контакты V2 (контакты)</span><span class="sxs-lookup"><span data-stu-id="aeb00-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="aeb00-192">CDS Контакты V2 (контакты)</span><span class="sxs-lookup"><span data-stu-id="aeb00-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="aeb00-193">Поставщик V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="aeb00-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="aeb00-194">Убедитесь, что сопоставления удалены из таблицы `msdy_dualwriteruntimeconfig` в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="aeb00-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="aeb00-195">Установка [решений стороны с двойной записью и глобальной адресной книги](https://aka.ms/dual-write-gab) из AppSource.</span><span class="sxs-lookup"><span data-stu-id="aeb00-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="aeb00-196">В приложении Finance and Operations, если следующие таблицы содержат данные, выполните **Начальная синхронизация** для них.</span><span class="sxs-lookup"><span data-stu-id="aeb00-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="aeb00-197">Приветствия</span><span class="sxs-lookup"><span data-stu-id="aeb00-197">Salutations</span></span>
    + <span data-ttu-id="aeb00-198">Типы характеров людей</span><span class="sxs-lookup"><span data-stu-id="aeb00-198">Personal character types</span></span>
    + <span data-ttu-id="aeb00-199">Заключение</span><span class="sxs-lookup"><span data-stu-id="aeb00-199">Complimentary closing</span></span>
    + <span data-ttu-id="aeb00-200">Обращения к контактному лицу</span><span class="sxs-lookup"><span data-stu-id="aeb00-200">Contact person titles</span></span>
    + <span data-ttu-id="aeb00-201">Роли принятия решений</span><span class="sxs-lookup"><span data-stu-id="aeb00-201">Decision making roles</span></span>
    + <span data-ttu-id="aeb00-202">Уровни лояльности</span><span class="sxs-lookup"><span data-stu-id="aeb00-202">Loyalty levels</span></span>

5. <span data-ttu-id="aeb00-203">В приложении взаимодействия с клиентами отключите следующие шаги подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="aeb00-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="aeb00-204">Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-204">Account Update</span></span>
         + <span data-ttu-id="aeb00-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="aeb00-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="aeb00-207">Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-207">Contact Update</span></span>
         + <span data-ttu-id="aeb00-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="aeb00-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="aeb00-210">Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="aeb00-210">msdyn_party Update</span></span>
         + <span data-ttu-id="aeb00-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="aeb00-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="aeb00-212">Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="aeb00-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="aeb00-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="aeb00-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="aeb00-214">В приложении взаимодействия с клиентами отключите следующие workflow-процессы:</span><span class="sxs-lookup"><span data-stu-id="aeb00-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="aeb00-215">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-216">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-217">Создание поставщиков типа "респондент" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="aeb00-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="aeb00-218">Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="aeb00-219">Обновление поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-220">Обновление поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="aeb00-221">Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="aeb00-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="aeb00-222">Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="aeb00-223">В фабрике данных выполните шаблон, выбрав **Активировать сейчас**, как показано на следующем изображении.</span><span class="sxs-lookup"><span data-stu-id="aeb00-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="aeb00-224">Этот процесс может занять несколько часов в зависимости от объема данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Активировать выполнение](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="aeb00-226">Если имеются настройки для **Учетная запись**, **Контактное лицо** и **Поставщик**, необходимо изменить шаблон.</span><span class="sxs-lookup"><span data-stu-id="aeb00-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="aeb00-227">Импортируйте новые записи **Стороны** в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aeb00-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="aeb00-228">Загрузите файл `FONewParty.csv` из хранилища BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb00-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="aeb00-229">Путь `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="aeb00-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="aeb00-230">Преобразуйте файл `FONewParty.csv` в файл Excel и импортируйте файл Excel в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aeb00-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="aeb00-231">Если вам подходит импорт csv, можно напрямую импортировать файл CSV.</span><span class="sxs-lookup"><span data-stu-id="aeb00-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="aeb00-232">Для выполнения импорта может потребоваться несколько часов, в зависимости от объема данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="aeb00-233">Дополнительные сведения см. в разделе [Обзор заданий импорта и экспорта данных](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="aeb00-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Импорт записей стороны Datavers](media/data-factory-import-party.png)

9. <span data-ttu-id="aeb00-235">В приложениях взаимодействия с клиентами включите следующие шаги подключаемого модуля:</span><span class="sxs-lookup"><span data-stu-id="aeb00-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="aeb00-236">Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-236">Account Update</span></span>
         + <span data-ttu-id="aeb00-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="aeb00-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Обновление учетной записи</span><span class="sxs-lookup"><span data-stu-id="aeb00-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="aeb00-239">Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-239">Contact Update</span></span>
         + <span data-ttu-id="aeb00-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="aeb00-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Обновление контактного лица</span><span class="sxs-lookup"><span data-stu-id="aeb00-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="aeb00-242">Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="aeb00-242">msdyn_party Update</span></span>
         + <span data-ttu-id="aeb00-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Обновление msdyn_party</span><span class="sxs-lookup"><span data-stu-id="aeb00-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="aeb00-244">Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="aeb00-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="aeb00-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Обновление msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="aeb00-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="aeb00-246">В приложениях взаимодействия с клиентами активируйте следующие workflow-процессы, если они были деактивированы в предыдущих шагах:</span><span class="sxs-lookup"><span data-stu-id="aeb00-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="aeb00-247">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-248">Создание поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-249">Создание поставщиков типа "респондент" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="aeb00-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="aeb00-250">Создание поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="aeb00-251">Обновление поставщиков в таблице "Организации"</span><span class="sxs-lookup"><span data-stu-id="aeb00-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="aeb00-252">Обновление поставщиков в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="aeb00-253">Обновление поставщиков типа "Физическое лицо" в таблице "Контакты"</span><span class="sxs-lookup"><span data-stu-id="aeb00-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="aeb00-254">Обновление поставщиков типа "Физическое лицо" в таблице "Поставщики"</span><span class="sxs-lookup"><span data-stu-id="aeb00-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="aeb00-255">Выполните сопоставления, связанные с **Стороной**, в соответствии с указаниями в [Сторона и глобальная адресная книга](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="aeb00-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="aeb00-256">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="aeb00-256">Troubleshooting</span></span>

1. <span data-ttu-id="aeb00-257">В случае сбоя процесса перезапустите фабрику данных, начиная с невыполненного действия.</span><span class="sxs-lookup"><span data-stu-id="aeb00-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="aeb00-258">Некоторые файлы создаются фабрикой данных, которую можно использовать для целей проверки данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="aeb00-259">Фабрика данных выполняется на основе файлов CSV, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="aeb00-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="aeb00-260">Если имеется значение поля с запятой, оно может повлиять на результаты.</span><span class="sxs-lookup"><span data-stu-id="aeb00-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="aeb00-261">Необходимо удалить запятые.</span><span class="sxs-lookup"><span data-stu-id="aeb00-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="aeb00-262">Вкладка **Мониторинг** содержит сведения обо всех шагах и обработанных данных.</span><span class="sxs-lookup"><span data-stu-id="aeb00-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="aeb00-263">Выбор конкретного шага для его отладки.</span><span class="sxs-lookup"><span data-stu-id="aeb00-263">Select a specific step to debug it.</span></span>

    ![Вкладка "Мониторинг"](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="aeb00-265">Дополнительные сведения о шаблоне</span><span class="sxs-lookup"><span data-stu-id="aeb00-265">Learn more about the template</span></span>

<span data-ttu-id="aeb00-266">Комментарии для шаблона можно найти в файле [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="aeb00-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>