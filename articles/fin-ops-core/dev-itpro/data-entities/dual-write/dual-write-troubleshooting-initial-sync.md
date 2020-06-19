---
title: Устранение неполадок при начальной синхронизации
description: В этом разделе содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410089"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="d7c3a-103">Устранение неполадок при начальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="d7c3a-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7c3a-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="d7c3a-105">А именно, содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7c3a-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d7c3a-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="d7c3a-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="d7c3a-108">Проверка наличия ошибок исходной синхронизации в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7c3a-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="d7c3a-109">После включения шаблонов сопоставления статус сопоставлений должно быть **Выполняется**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="d7c3a-110">Если статус **Не выполняется**, при первоначальной синхронизации произошли ошибки.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="d7c3a-111">Для просмотра ошибок выберите вкладку **Сведения о начальной синхронизации** на странице **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Вкладка сведений о начальной синхронизации](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="d7c3a-113">Выполнение начальной синхронизации невозможно: 400 Неправильный запрос</span><span class="sxs-lookup"><span data-stu-id="d7c3a-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="d7c3a-114">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="d7c3a-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="d7c3a-115">При попытке запуска сопоставления и исходной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="d7c3a-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="d7c3a-116">*Удаленный сервер вернул ошибку: (400) Неправильный запрос.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="d7c3a-117">Ниже приведен пример полного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="d7c3a-118">Если эта ошибка происходит постоянно, и вы не можете выполнить начальную синхронизацию, выполните следующие действия для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="d7c3a-119">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="d7c3a-120">Откройте консоль управления Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="d7c3a-121">В области **Службы** убедитесь, что запущена служба структуры импорта и экспорта данных Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="d7c3a-122">Перезапустите ее, если она была остановлена, так как она необходима для исходной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="d7c3a-123">Ошибка начальной синхронизации: 403 Запрещено</span><span class="sxs-lookup"><span data-stu-id="d7c3a-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="d7c3a-124">Во время начальной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="d7c3a-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="d7c3a-125">*(\[Запрещено\], Удаленный сервер вернул ошибку: (403) Запрещено.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="d7c3a-126">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="d7c3a-127">Выполните вход в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="d7c3a-128">На странице **Приложения Azure Active Directory** удалите клиент **DtAppID** и добавьте его снова.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Список приложений Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="d7c3a-130">Ошибки ссылки на себя или циклических ссылок во время первоначальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="d7c3a-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="d7c3a-131">Если какое-либо сопоставление имеет ссылки на себя или циклические ссылки, вы можете получить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="d7c3a-132">Ошибки делятся на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="d7c3a-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="d7c3a-133">Сопоставление объекта Vendors V2 для msdyn_vendors"</span><span class="sxs-lookup"><span data-stu-id="d7c3a-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="d7c3a-134">Сопоставление объектов Vendors V3 для "Организации"</span><span class="sxs-lookup"><span data-stu-id="d7c3a-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="d7c3a-135">Устранение ошибки в сопоставлении объектов Vendors V2 для msdyn_vendors"</span><span class="sxs-lookup"><span data-stu-id="d7c3a-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="d7c3a-136">Возможны следующие ошибки первоначальной синхронизации в составлении **Vendors V2** для **msdyn_vendors**, если у этих объектов есть существующие записи со значениями в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="d7c3a-137">Это связано с тем, что **InvoiceVendorAccountNumber** — это полем ссылки на себя, а **PrimaryContactPersonId** — это циклическая ссылка в сопоставлении поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="d7c3a-138">*Не удалось разрешить GUID для поля: <field>. Поиск не найден: <value>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="d7c3a-139">Вот несколько примеров:</span><span class="sxs-lookup"><span data-stu-id="d7c3a-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="d7c3a-140">*Не удалось разрешить GUID для поля: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="d7c3a-141">*Не удалось разрешить GUID для поля: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Поиск не найден: V24-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="d7c3a-142">Если имеются записи со значениями в этих полях объекта поставщика, выполните шаги, указанные в приведенном ниже разделе, чтобы успешно завершить начальную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="d7c3a-143">В приложении Finance and Operations удалите поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** из сопоставления и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="d7c3a-144">Перейдите на страницу сопоставление двойной записи для **Vendors V2 (msdyn_vendors)** и перейдите на вкладку **Сопоставления объектов**. В левом фильтре выберите приложения **Finance and Operations. apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="d7c3a-145">В правом фильтре выберите **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="d7c3a-146">Выполните поиск **primarycontactperson**, чтобы найти поле источника **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="d7c3a-147">Щелкните кнопку **Действия** и выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="d7c3a-149">Повторите для удаления поля **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![ссылка на себя или циклическая ссылка 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="d7c3a-151">Сохраните изменения сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="d7c3a-152">Отключение отслеживания изменений для объекта **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="d7c3a-153">Перейдите **Управление данными \> Объекты данных**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="d7c3a-154">Выберите объект **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="d7c3a-155">Щелкните **Параметры** в строке меню и выберите **Отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 5](media/selfref_options.png)
    
    4. <span data-ttu-id="d7c3a-157">Щелкните **Отключить отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-157">Click **Disable Change Tracking**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 6](media/selfref_tracking.png)

3. <span data-ttu-id="d7c3a-159">Выполните начальную синхронизацию сопоставления **Vendors V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="d7c3a-160">Начальная синхронизация должна успешно работать без ошибок.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="d7c3a-161">Выполните начальную синхронизацию для составления **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="d7c3a-162">Необходимо синхронизировать это сопоставление, если следует синхронизировать основное поле контакта в объекте "поставщики", так как записи контактов также должны быть первоначально синхронизованы.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="d7c3a-163">Добавьте поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** обратно в сопоставление **Vendors V2 (msdyn_vendors)** и сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="d7c3a-164">Снова выполните начальную синхронизацию сопоставления **Vendors V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="d7c3a-165">Все записи будут синхронизированы, так как отслеживание изменений отключено.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="d7c3a-166">Включите отслеживание изменений для объекта **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="d7c3a-167">Устранение ошибки в сопоставлениях объектов Customers V3 для "Организации"</span><span class="sxs-lookup"><span data-stu-id="d7c3a-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="d7c3a-168">Возможны следующие ошибки первоначальной синхронизации в составлении **Customers V3** для **"Организации"**, если у этих объектов есть существующие записи со значениями в полях **ContactPersonID** и **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="d7c3a-169">Это связано с тем, что **InvoiceAccount** — это полем ссылки на себя, а **ContactPersonID** — это циклическая ссылка в сопоставлении поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="d7c3a-170">*Не удалось разрешить GUID для поля: <field>. Поиск не найден: <value>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="d7c3a-171">*Не удалось разрешить GUID для поля: primarycontactid.msdyn_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="d7c3a-172">*Не удалось разрешить GUID для поля: msdyn_billingaccount.accountnumber. Поиск не найден: 1206-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="d7c3a-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="d7c3a-173">Если имеются записи со значениями в этих полях объекта клиента, выполните шаги, указанные в приведенном ниже разделе, чтобы успешно завершить начальную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="d7c3a-174">Этот подход можно использовать для всех готовых элементов, таких как "организации" и "контакты".</span><span class="sxs-lookup"><span data-stu-id="d7c3a-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="d7c3a-175">В приложении Finance and Operations удалите поля **ContactPersonID** и **InvoiceAccount** из сопоставления **Клиенты V3 (Организации)** и сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="d7c3a-176">Перейдите на страницу сопоставление двойной записи для **Клиенты V3 (Организации)** и перейдите на вкладку **Сопоставления объектов**. В левом фильтре выберите приложения **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="d7c3a-177">В правом фильтре выберите **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="d7c3a-178">Выполните поиск **contactperson**, чтобы найти поле источника **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="d7c3a-179">Щелкните кнопку **Действия** и выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="d7c3a-181">Повторите для удаления поля **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![ссылка на себя или циклическая ссылка](media/cust_selfref4.png)
    
    5. <span data-ttu-id="d7c3a-183">Сохраните изменения сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="d7c3a-184">Отключение отслеживания изменений для объекта **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="d7c3a-185">Перейдите **Управление данными \> Объекты данных**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="d7c3a-186">Выберите объект **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="d7c3a-187">Щелкните **Параметры** в строке меню и выберите **Отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 5](media/selfref_options.png)
    
    4. <span data-ttu-id="d7c3a-189">Щелкните **Отключить отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-189">Click **Disable Change Tracking**.</span></span>
    
        ![ссылка на себя или циклическая ссылка 6](media/selfref_tracking.png)

3. <span data-ttu-id="d7c3a-191">Выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="d7c3a-192">Начальная синхронизация должна успешно работать без ошибок.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="d7c3a-193">Выполните начальную синхронизацию для составления **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="d7c3a-194">Имеется 2 сопоставления с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="d7c3a-195">Выберите один с описанием **Шаблон двойной записи для синхронизации между FO.CDS Vendor Contacts V2 для CDS.Contacts. Требуется новый пакет \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="d7c3a-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="d7c3a-196">на вкладке **Сведения** сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="d7c3a-197">Добавьте поля **InvoiceAccount** и **ContactPersonId** обратно в сопоставление **Клиенты V3 (Организации)** и сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="d7c3a-198">Теперь оба поля **InvoiceAccount** и **ContactPersonId** снова будут учтены в реальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="d7c3a-199">На следующем шаге выполняется начальная синхронизация этих полей.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="d7c3a-200">Снова выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="d7c3a-201">Поскольку отслеживание изменений отключено, выполнение синхронизации приведет к синхронизации данных для **InvoiceAccount** и **ContactPersonId** из приложения Finance and Operations в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="d7c3a-202">Для синхронизации данных для **InvoiceAccount** и **ContactPersonId** из Common Data Service в Finance and Operations можно использовать проект интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="d7c3a-203">В Power Apps создайте проект интеграции данных между объектами **Sales.Account** и **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="d7c3a-204">Направление данных должно быть из Common Data Service в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="d7c3a-205">Поскольку **InvoiceAccount** является новым атрибутом в двойной записи, можно пропустить начальную синхронизацию для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="d7c3a-206">Дополнительные сведения см. в разделе [Интеграция данных в Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="d7c3a-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="d7c3a-207">На следующем рисунке показан проект, который обновляет **CustomerAccount** и **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![ссылка на себя или циклическая ссылка](media/cust_selfref6.png)

    2. <span data-ttu-id="d7c3a-209">Добавьте критерии компании в фильтр со стороны Common Data Service, так как в приложении Finance and Operations будут обновлены только записи, отвечающие условиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="d7c3a-210">Чтобы добавить фильтр, щелкните значок фильтра.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="d7c3a-211">В диалоговом окне **Изменение запроса** можно добавить запрос фильтра, например **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="d7c3a-212">Если значок фильтра отсутствует, создайте запрос на поддержку, чтобы попросить у группы интеграции данных включить функцию фильтра в вашем клиенте.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="d7c3a-213">Если не ввести запрос фильтра для **_msdyn_company_value**, то все записи будут синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![ссылка на себя или циклическая ссылка](media/cust_selfref7.png)

        <span data-ttu-id="d7c3a-215">Это завершение начальной синхронизации записей.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="d7c3a-216">Включите отслеживание изменений для объекта **Customers V3** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d7c3a-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

