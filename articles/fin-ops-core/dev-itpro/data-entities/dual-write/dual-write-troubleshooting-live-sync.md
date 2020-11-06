---
title: Устранение проблем с синхронизацией в режиме реального времени
description: В этом разделе содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.
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
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997310"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="14e26-103">Устранение проблем с синхронизацией в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="14e26-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="14e26-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e26-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="14e26-105">А именно, в нем содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="14e26-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14e26-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="14e26-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="14e26-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="14e26-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="14e26-108">Синхронизация в режиме реального времени создает ошибку "403 Запрещено" при создании записи в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14e26-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="14e26-109">При создании записи в приложении Finance and Operations может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="14e26-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="14e26-110">*\[{\\"ошибка\\":{\\"код\\":\\"0x80072560\\",\\"сообщение\\":\\"Пользователь не является членом организации.\\"}}\], Удаленный сервер вернул ошибку: (403) Запрещено."}}".*</span><span class="sxs-lookup"><span data-stu-id="14e26-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="14e26-111">Чтобы устранить проблему, выполните шаги, указанные в разделе [Системные требования и предварительные условия](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="14e26-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="14e26-112">Для выполнения этих шагов пользователь с двойной записью, созданный в Common Data Service, должен иметь роль администратора системы.</span><span class="sxs-lookup"><span data-stu-id="14e26-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="14e26-113">Группа-владелец по умолчанию должна также иметь роль администратора системы.</span><span class="sxs-lookup"><span data-stu-id="14e26-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="14e26-114">Синхронизация в режиме реального времени для любого объекта постоянно создает аналогичную ошибку при создании записи в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14e26-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="14e26-115">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="14e26-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="14e26-116">При каждом попытке сохранить данные объекта в приложении Finance and Operations может появиться сообщение об ошибке, подобное следующему:</span><span class="sxs-lookup"><span data-stu-id="14e26-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="14e26-117">*Не удается сохранить изменения в базе данных. Единица работы не может зафиксировать проводку. Невозможно записать данные в единицы измерения объекта. Операции записи в UnitOfMeasureEntity заканчиваются сбоем с сообщением об ошибке "Не удается синхронизировать с единицами измерения объекта".*</span><span class="sxs-lookup"><span data-stu-id="14e26-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="14e26-118">Чтобы устранить проблему, необходимо убедиться, что необходимые ссылочные данные существуют как в приложении Finance and Operations ,так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e26-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="14e26-119">Например, если клиент, указанный в приложении Finance and Operations, принадлежит определенной группе клиентов, убедитесь, что эта группа клиентов существует в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e26-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="14e26-120">Если данные существуют на обеих сторонах, и вы убедились, что проблема не связана с данными, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14e26-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="14e26-121">Остановите связанный объект.</span><span class="sxs-lookup"><span data-stu-id="14e26-121">Stop the related entity.</span></span>
2. <span data-ttu-id="14e26-122">Выполните вход в приложение Finance and Operations и убедитесь, что записи для объекта, в котором возникает ошибка, существуют в таблицах DualWriteProjectConfiguration и DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="14e26-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="14e26-123">Например, вот как выглядит запрос, если происходит сбой объекта **Клиенты**.</span><span class="sxs-lookup"><span data-stu-id="14e26-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="14e26-124">Если имеются записи для объекта, в котором возникает ошибка, даже после остановки сопоставления объектов, удалите записи, относящиеся к объекту, в котором возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="14e26-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="14e26-125">Запишите столбец **projectname** в таблице DualWriteProjectConfiguration и извлеките запись в таблице DualWriteProjectFieldConfiguration, используя это имя проекта, чтобы удалить запись.</span><span class="sxs-lookup"><span data-stu-id="14e26-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="14e26-126">Запустите сопоставление объектов.</span><span class="sxs-lookup"><span data-stu-id="14e26-126">Start the entity mapping.</span></span> <span data-ttu-id="14e26-127">Проверьте, были ли данные синхронизированы без каких-либо проблем.</span><span class="sxs-lookup"><span data-stu-id="14e26-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="14e26-128">Обработка ошибок привилегии чтения или записи при создании данных в приложении Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="14e26-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="14e26-129">При создании данных в приложении Finance and Operations может быть получено сообщение об ошибке "Ошибочный запрос", которая напоминает следующий пример.</span><span class="sxs-lookup"><span data-stu-id="14e26-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Пример сообщения об ошибке "Ошибочный запрос"](media/error_record_id_source.png)

<span data-ttu-id="14e26-131">Чтобы решить эту проблему, необходимо назначить правильную роль безопасности для рабочей группы сопоставленного подразделения Dynamics 365 Sales или Dynamics 365 Customer Service, чтобы включить отсутствующую привилегию.</span><span class="sxs-lookup"><span data-stu-id="14e26-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="14e26-132">В приложении Finance and Operations найдите подразделение, сопоставленное в наборе подключений интеграции данных.</span><span class="sxs-lookup"><span data-stu-id="14e26-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Сопоставление организации](media/mapped_business_unit.png)

2. <span data-ttu-id="14e26-134">Выполните вход в среду приложения на основе модели в Dynamics 365, перейдите к пункту **Параметры \>Безопасность** и найдите рабочую группу сопоставленного подразделения.</span><span class="sxs-lookup"><span data-stu-id="14e26-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![Рабочая группа сопоставленного подразделения](media/setting_security_page.png)

3. <span data-ttu-id="14e26-136">Откройте страницу этой рабочей группы для редактирования, затем выберите **Управление ролями** , чтобы открыть диалоговое окно **Управление ролями группы**.</span><span class="sxs-lookup"><span data-stu-id="14e26-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Кнопка "Управление ролями"](media/manage_team_roles.png)

4. <span data-ttu-id="14e26-138">Назначьте роль с привилегиями на чтение/запись для соответствующих объектов, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="14e26-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="14e26-139">Устранение проблем синхронизации в среде с недавно измененной средой Common Data Service</span><span class="sxs-lookup"><span data-stu-id="14e26-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="14e26-140">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="14e26-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="14e26-141">При создании данных в приложении Finance and Operations может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="14e26-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="14e26-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Не удается создать полезную нагрузку для объекта CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Сбой создания полезной нагрузки с ошибкой Недопустимый URI: URI пуст."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="14e26-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="14e26-143">Вот как выглядит эта ошибка в приложении на основе модели в Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="14e26-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="14e26-144">*Возникла непредвиденная ошибка в коде независимого разработчика. (ErrorType = ClientError) Непредвиденное исключение от подключаемого модуля (Выполнить): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: не удалось обработать учетную запись объекта - (Сбой попытки подключения, так как подключенная стороне не предоставляет правильный ответ в течение некоторого периода времени, или сбой установленного подключения из-за отсутствия ответа от хост-компьютера*</span><span class="sxs-lookup"><span data-stu-id="14e26-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="14e26-145">Эта ошибка возникает в том случае, когда среда Common Data Service ошибочно сбрасывается одновременно с попыткой создать данные в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="14e26-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="14e26-146">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14e26-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="14e26-147">Выполните вход на виртуальную машину Finance and Operations, откройте SQL Server Management Studio (SSMS) и выполните поиск записей в таблице DUALWRITEPROJECTCONFIGURATIONENTITY, где **internalentityname** равно **Customers V3** и **externalentityname** равно **accounts**.</span><span class="sxs-lookup"><span data-stu-id="14e26-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="14e26-148">Вот как выглядит этот запрос.</span><span class="sxs-lookup"><span data-stu-id="14e26-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="14e26-149">Используйте имя проекта из результатов предыдущего запроса, чтобы выполнить следующий запрос.</span><span class="sxs-lookup"><span data-stu-id="14e26-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="14e26-150">Убедитесь, что столбец **externalenvironmentURL** имеет правильный URL-адрес Common Data Service или приложения.</span><span class="sxs-lookup"><span data-stu-id="14e26-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="14e26-151">Удалите все дубликаты записей, которые указывают на неправильный URL-адрес Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14e26-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="14e26-152">Удалите соответствующие записи в таблицах DUALWRITEPROJECTFIELDCONFIGURATION и DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="14e26-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="14e26-153">Остановите сопоставление объектов, а затем перезапустите его</span><span class="sxs-lookup"><span data-stu-id="14e26-153">Stop the entity mapping, and then restart it</span></span>
