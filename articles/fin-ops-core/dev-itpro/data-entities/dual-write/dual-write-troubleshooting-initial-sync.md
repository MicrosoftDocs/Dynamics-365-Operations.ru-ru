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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683576"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="312af-103">Устранение неполадок при начальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="312af-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="312af-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="312af-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="312af-105">А именно, содержатся сведения об устранении неполадок, которые могут возникнуть при начальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="312af-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="312af-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="312af-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="312af-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="312af-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="312af-108">Проверка наличия ошибок исходной синхронизации в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="312af-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="312af-109">После включения шаблонов сопоставления статус сопоставлений должно быть **Выполняется**.</span><span class="sxs-lookup"><span data-stu-id="312af-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="312af-110">Если статус **Не выполняется**, при первоначальной синхронизации произошли ошибки.</span><span class="sxs-lookup"><span data-stu-id="312af-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="312af-111">Для просмотра ошибок выберите вкладку **Сведения о начальной синхронизации** на странице **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="312af-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Ошибка на вкладке сведений о начальной синхронизации](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="312af-113">Выполнение начальной синхронизации невозможно: 400 Неправильный запрос</span><span class="sxs-lookup"><span data-stu-id="312af-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="312af-114">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="312af-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="312af-115">При попытке запуска сопоставления и исходной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="312af-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="312af-116">*(\[Неправильный запрос\], Удаленный сервер вернул ошибку: (400) Неправильный запрос.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="312af-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="312af-117">Ниже приведен пример полного сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="312af-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="312af-118">Если эта ошибка происходит постоянно, и вы не можете выполнить начальную синхронизацию, выполните следующие действия для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="312af-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="312af-119">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="312af-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="312af-120">Откройте консоль управления Microsoft.</span><span class="sxs-lookup"><span data-stu-id="312af-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="312af-121">В области **Службы** убедитесь, что запущена служба структуры импорта и экспорта данных Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="312af-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="312af-122">Перезапустите ее, если она была остановлена, так как она необходима для исходной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="312af-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="312af-123">Ошибка начальной синхронизации: 403 Запрещено</span><span class="sxs-lookup"><span data-stu-id="312af-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="312af-124">Во время начальной синхронизации может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="312af-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="312af-125">*(\[Запрещено\], Удаленный сервер вернул ошибку: (403) Запрещено.), при экспорте AX произошла ошибка*</span><span class="sxs-lookup"><span data-stu-id="312af-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="312af-126">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="312af-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="312af-127">Выполните вход в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="312af-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="312af-128">На странице **Приложения Azure Active Directory** удалите клиент **DtAppID** и добавьте его снова.</span><span class="sxs-lookup"><span data-stu-id="312af-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Клиент DtAppID в списке приложений Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="312af-130">Ошибки ссылки на себя или циклических ссылок во время первоначальной синхронизации</span><span class="sxs-lookup"><span data-stu-id="312af-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="312af-131">Если какое-либо сопоставление имеет ссылки на себя или циклические ссылки, вы можете получить сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="312af-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="312af-132">Ошибки делятся на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="312af-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="312af-133">Ошибки в сопоставлении таблиц "Поставщики V2" с msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="312af-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="312af-134">Ошибки в сопоставлениях таблиц "Клиенты V3" с "Организации"</span><span class="sxs-lookup"><span data-stu-id="312af-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="312af-135">Устранение ошибок в сопоставлении таблиц "Поставщики V2" с msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="312af-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="312af-136">Возможны ошибки первоначальной синхронизации для составления **Поставщики V2** с **msdyn\_vendors**, если у этих таблиц есть существующие строки, где есть значения в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="312af-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="312af-137">Эти ошибки возникают в связи с тем, что **InvoiceVendorAccountNumber** — это поле ссылки на себя, а **PrimaryContactPersonId** — это циклическая ссылка в сопоставлении поставщиков.</span><span class="sxs-lookup"><span data-stu-id="312af-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="312af-138">Полученные сообщения об ошибках будет иметь следующую форму.</span><span class="sxs-lookup"><span data-stu-id="312af-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="312af-139">*Не удалось разрешить GUID для поля: \<field\>. Поиск не найден: \<value\>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="312af-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="312af-140">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="312af-140">Here are some examples:</span></span>

- <span data-ttu-id="312af-141">*Не удалось разрешить GUID для поля: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="312af-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="312af-142">*Не удалось разрешить GUID для поля: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Поиск не найден: V24-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="312af-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="312af-143">Если какие-то строки в сущности поставщика имеют значения в полях **PrimaryContactPersonId** и **InvoiceVendorAccountNumber**, выполните следующие шаги, чтобы завершить начальную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="312af-143">If any rows in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="312af-144">В приложении Finance and Operations удалите поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** из сопоставления, затем сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="312af-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="312af-145">На странице сопоставление двойной записи для **Поставщики V2 (msdyn\_vendors)** на вкладке **Сопоставления таблиц** в левом фильтре выберите **Приложения Finance and Operations.Поставщики V2**.</span><span class="sxs-lookup"><span data-stu-id="312af-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="312af-146">В правом фильтре выберите **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="312af-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="312af-147">Выполните поиск **primarycontactperson**, чтобы найти поле источника **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="312af-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="312af-148">Выберите **Действия**, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="312af-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Удаление поля PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="312af-150">Повторите эти шаги для удаления поля **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="312af-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Удаление поля InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="312af-152">Сохраните изменения в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="312af-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="312af-153">Выключите отслеживание изменений для объекта **Поставщики V2**.</span><span class="sxs-lookup"><span data-stu-id="312af-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="312af-154">В рабочей области **Управление данными** выберите плитку **Таблицы данных**.</span><span class="sxs-lookup"><span data-stu-id="312af-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="312af-155">Выберите объект **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="312af-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="312af-156">На панели операций выберите **Параметры**, затем выберите **Отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="312af-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Выбор параметра отслеживания изменений](media/selfref_options.png)

    4. <span data-ttu-id="312af-158">Выберите **Отключить отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="312af-158">Select **Disable Change Tracking**.</span></span>

        ![Выбор "Отключить отслеживание изменений"](media/selfref_tracking.png)

3. <span data-ttu-id="312af-160">Выполните начальную синхронизацию для сопоставления **Поставщики V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="312af-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="312af-161">Начальная синхронизация должна успешно работать без ошибок.</span><span class="sxs-lookup"><span data-stu-id="312af-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="312af-162">Выполните начальную синхронизацию для составления **Контакты CDS V2 (контакты)**.</span><span class="sxs-lookup"><span data-stu-id="312af-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="312af-163">Необходимо синхронизировать это сопоставление, если следует синхронизировать основное поле контакта в объекте "поставщики", так как начальная синхронизация также должна быть выполнена для строк контактов.</span><span class="sxs-lookup"><span data-stu-id="312af-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="312af-164">Добавьте поля **PrimaryContactPersonId** и **InvoiceVendorAccountNumber** обратно в сопоставление **Поставщики V2 (msdyn\_vendors)**, затем сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="312af-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="312af-165">Выполните начальную синхронизацию еще раз для сопоставления **Поставщики V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="312af-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="312af-166">Так как отслеживание изменений отключено, все строки будут синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="312af-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="312af-167">Снова включите отслеживание изменений для объекта **Поставщики V2**.</span><span class="sxs-lookup"><span data-stu-id="312af-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="312af-168">Устранение ошибок в сопоставлениях таблиц "Клиенты V3" с "Организации"</span><span class="sxs-lookup"><span data-stu-id="312af-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="312af-169">Возможны ошибки первоначальной синхронизации для составления **Клиенты V3** с **Организации**, если у этих таблиц есть существующие строки, где есть значения в полях **ContactPersonID** и **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="312af-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="312af-170">Эти ошибки возникают, так как что **InvoiceAccount** — это поле ссылки на себя, а **ContactPersonID** — это циклическая ссылка в сопоставлении поставщиков.</span><span class="sxs-lookup"><span data-stu-id="312af-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="312af-171">Полученные сообщения об ошибках будет иметь следующую форму.</span><span class="sxs-lookup"><span data-stu-id="312af-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="312af-172">*Не удалось разрешить GUID для поля: \<field\>. Поиск не найден: \<value\>. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="312af-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="312af-173">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="312af-173">Here are some examples:</span></span>

- <span data-ttu-id="312af-174">*Не удалось разрешить GUID для поля: primarycontactid.msdyn\_contactpersonid. Поиск не найден: 000056. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="312af-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="312af-175">*Не удалось разрешить GUID для поля: msdyn\_billingaccount.accountnumber. Поиск не найден: 1206-1. Попробуйте использовать этот URL-адрес для проверки существования ссылочных данных: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="312af-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="312af-176">Если какие-то строки в сущности клиента имеют значения в полях **ContactPersonID** и **InvoiceAccount**, выполните следующие шаги, чтобы завершить начальную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="312af-176">If any rows in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="312af-177">Этот подход можно использовать для всех готовых таблиц, таких как **Организации** и **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="312af-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="312af-178">В приложении Finance and Operations удалите поля **ContactPersonID** и **InvoiceAccount** из сопоставления **Клиенты V3 (организации)**, затем сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="312af-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="312af-179">Перейдите на страницу сопоставление двойной записи для **Клиенты V3 (организации)** и перейдите на вкладку **Сопоставления таблиц**. В левом фильтре выберите приложения **Приложение Finance and Operations.Клиенты V3**.</span><span class="sxs-lookup"><span data-stu-id="312af-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="312af-180">В правом фильтре выберите **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="312af-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="312af-181">Выполните поиск **contactperson**, чтобы найти поле источника **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="312af-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="312af-182">Выберите **Действия**, затем выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="312af-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Удаление поля ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="312af-184">Повторите эти шаги для удаления поля **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="312af-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Удаление поля InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="312af-186">Сохраните изменения в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="312af-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="312af-187">Выключите отслеживание изменений для объекта **Клиенты V3**.</span><span class="sxs-lookup"><span data-stu-id="312af-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="312af-188">В рабочей области **Управление данными** выберите плитку **Таблицы данных**.</span><span class="sxs-lookup"><span data-stu-id="312af-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="312af-189">Выберите объект **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="312af-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="312af-190">На панели операций выберите **Параметры**, затем выберите **Отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="312af-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Выбор параметра отслеживания изменений](media/selfref_options.png)

    4. <span data-ttu-id="312af-192">Выберите **Отключить отслеживание изменений**.</span><span class="sxs-lookup"><span data-stu-id="312af-192">Select **Disable Change Tracking**.</span></span>

        ![Выбор "Отключить отслеживание изменений"](media/selfref_tracking.png)

3. <span data-ttu-id="312af-194">Выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**.</span><span class="sxs-lookup"><span data-stu-id="312af-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="312af-195">Начальная синхронизация должна успешно работать без ошибок.</span><span class="sxs-lookup"><span data-stu-id="312af-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="312af-196">Выполните начальную синхронизацию для составления **Контакты CDS V2 (контакты)**.</span><span class="sxs-lookup"><span data-stu-id="312af-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="312af-197">Существуют два сопоставления с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="312af-197">There are two maps that have the same name.</span></span> <span data-ttu-id="312af-198">Обязательно выберите сопоставление со следующим описанием на вкладке **Сведения**: **Шаблон двойной записи для синхронизации между FO.CDS Vendor Contacts V2 для CDS.Contacts. Требуется новый пакет \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="312af-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="312af-199">Добавьте поля **InvoiceAccount** и **ContactPersonId** обратно в сопоставление **Клиенты V3 (Организации)**, затем сохраните сопоставление.</span><span class="sxs-lookup"><span data-stu-id="312af-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="312af-200">Оба поля **InvoiceAccount** и **ContactPersonId** теперь будут снова учитываться в режиме синхронизации в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="312af-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="312af-201">На следующем шаге вы выполните начальную синхронизацию для этих полей.</span><span class="sxs-lookup"><span data-stu-id="312af-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="312af-202">Снова выполните начальную синхронизацию для составления **Клиенты V3 (Организации)**.</span><span class="sxs-lookup"><span data-stu-id="312af-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="312af-203">Поскольку отслеживание изменений отключено, данные для **InvoiceAccount** и **ContactPersonId** будут синхронизированы из приложения Finance and Operations в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="312af-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="312af-204">Для синхронизации данных для **InvoiceAccount** и **ContactPersonId** из Dataverse в приложение Finance and Operations необходимо использовать проект интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="312af-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="312af-205">В Power Apps создайте проект интеграции данных между таблицами **Sales.Account** и **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="312af-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="312af-206">Направление данных должно быть из Dataverse в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="312af-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="312af-207">Поскольку **InvoiceAccount** является новым атрибутом в двойной записи, можно пропустить начальную синхронизацию для него.</span><span class="sxs-lookup"><span data-stu-id="312af-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="312af-208">Дополнительные сведения см. в разделе [Интеграция данных в Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="312af-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="312af-209">На следующей иллюстрации показан проект, который обновляет **CustomerAccount** и **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="312af-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Проект интеграции данных для обновления CustomerAccount и ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="312af-211">Добавьте критерии компании в фильтр со стороны Dataverse, так что в приложении Finance and Operations будут обновляться только строки, отвечающие условиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="312af-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="312af-212">Чтобы добавить фильтр, выберите кнопку фильтра.</span><span class="sxs-lookup"><span data-stu-id="312af-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="312af-213">Затем, в диалоговом окне **Изменение запроса** можно добавить запрос фильтра, например **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="312af-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="312af-214">[ПРИМЕЧАНИЕ] Если кнопка фильтра отсутствует, создайте запрос на поддержку, чтобы попросить у группы интеграции данных включить функцию фильтра в вашем клиенте.</span><span class="sxs-lookup"><span data-stu-id="312af-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="312af-215">Если не ввести запрос фильтра для **\_msdyn\_company\_value**, то все строки будут синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="312af-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Добавление запроса фильтра](media/cust_selfref7.png)

    <span data-ttu-id="312af-217">Исходная синхронизация строк теперь завершена.</span><span class="sxs-lookup"><span data-stu-id="312af-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="312af-218">В приложении Finance and Operations снова включите отслеживание изменений для сущности **Клиенты V3**.</span><span class="sxs-lookup"><span data-stu-id="312af-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
