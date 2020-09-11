---
title: Копирование экземпляра
description: Можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Human Resources в среду в песочнице.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b52b696d323df6bafead2418ae322d1a9cdf64a
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706236"
---
# <a name="copy-an-instance"></a><span data-ttu-id="a026e-103">Копирование экземпляра</span><span class="sxs-lookup"><span data-stu-id="a026e-103">Copy an instance</span></span>

<span data-ttu-id="a026e-104">Можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Human Resources в среду в песочнице.</span><span class="sxs-lookup"><span data-stu-id="a026e-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="a026e-105">При наличии другой среды-песочницы можно также скопировать базу данных из этой среды в целевую среду-песочницу.</span><span class="sxs-lookup"><span data-stu-id="a026e-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="a026e-106">Чтобы скопировать экземпляр, необходимо помнить о следующих советах:</span><span class="sxs-lookup"><span data-stu-id="a026e-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="a026e-107">Экземпляр Human Resources, который требуется перезаписывать, должен быть средой песочницы.</span><span class="sxs-lookup"><span data-stu-id="a026e-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="a026e-108">Среды, из которых выполняется копирование, должны быть в одном регионе.</span><span class="sxs-lookup"><span data-stu-id="a026e-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="a026e-109">Нельзя копировать по регионам.</span><span class="sxs-lookup"><span data-stu-id="a026e-109">You can't copy across regions.</span></span>

- <span data-ttu-id="a026e-110">Вы должны быть администратором в целевой среде, чтобы можно было войти в систему после копирования экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a026e-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="a026e-111">При копировании базы данных Human Resources не копируются элементы (приложения или данные), содержащиеся в среде Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a026e-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="a026e-112">Сведения о способе копирования элементов в среде Power Apps см. в разделе [Копирование среды](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="a026e-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="a026e-113">Среда Power Apps, которую требуется перезаписывать, должна быть средой песочницы.</span><span class="sxs-lookup"><span data-stu-id="a026e-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="a026e-114">Чтобы изменить производственную среду Power Apps на среду песочницы, необходимо быть глобальным администратором клиента.</span><span class="sxs-lookup"><span data-stu-id="a026e-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="a026e-115">Дополнительные сведения об изменении среды Power Apps см. в разделе [Переключение экземпляра](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="a026e-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="a026e-116">Если экземпляр копируется в среду "песочницы" и требуется интегрировать среду "песочницы" с Common Data Service, необходимо повторно применить настраиваемые поля к сущностям Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a026e-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span> <span data-ttu-id="a026e-117">См. раздел [Применение настраиваемых полей к Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="a026e-117">See [Apply custom fields to Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="a026e-118">Результаты копирования базы данных Human Resources</span><span class="sxs-lookup"><span data-stu-id="a026e-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="a026e-119">При копировании базы данных Human Resources происходят следующие события:</span><span class="sxs-lookup"><span data-stu-id="a026e-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="a026e-120">Процесс копирования стирает существующую базу данных в целевой среде.</span><span class="sxs-lookup"><span data-stu-id="a026e-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="a026e-121">После завершения процесса копирования восстановить существующую базу данных невозможно.</span><span class="sxs-lookup"><span data-stu-id="a026e-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="a026e-122">Целевая среда будет недоступна до завершения процесса копирования.</span><span class="sxs-lookup"><span data-stu-id="a026e-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="a026e-123">Документы в хранилище BLOB-объектов Microsoft Azure не копируются из одной среды в другую.</span><span class="sxs-lookup"><span data-stu-id="a026e-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="a026e-124">В результате все документы и шаблоны, которые прикрепляются, не будут скопированы и останутся в исходной среде.</span><span class="sxs-lookup"><span data-stu-id="a026e-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="a026e-125">Все пользователи, кроме администратора и других учетных записей пользователей внутренних служб, будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="a026e-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="a026e-126">Пользователь с правами администратора может удалять или заменять данные до того, как другие пользователи смогут вернуться в систему.</span><span class="sxs-lookup"><span data-stu-id="a026e-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="a026e-127">Пользователь-администратор должен выполнить необходимые изменения конфигурации, такие как повторное подключение конечных точек интеграции к отдельным службам или URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="a026e-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="a026e-128">Копирование базы данных Human Resources</span><span class="sxs-lookup"><span data-stu-id="a026e-128">Copy the Human Resources database</span></span>

<span data-ttu-id="a026e-129">Чтобы выполнить эту задачу, необходимо сначала скопировать экземпляр, а затем войти в центр администрирования Microsoft Power Platform, чтобы скопировать среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a026e-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="a026e-130">При копировании экземпляра база данных удаляется из целевого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a026e-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="a026e-131">Целевой экземпляр недоступен в ходе этого процесса.</span><span class="sxs-lookup"><span data-stu-id="a026e-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="a026e-132">Выполните вход LCS и выберите проект LCS, содержащий экземпляр, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="a026e-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="a026e-133">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a026e-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="a026e-134">Выберите экземпляр для копирования, а затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="a026e-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="a026e-135">В области задач **Копирование экземпляра** выберите экземпляр, который требуется перезаписать, и нажмите кнопку **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="a026e-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="a026e-136">Дождитесь обновления значения поля **Статус копирования** до **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="a026e-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="a026e-137">Выберите экземпляр для перезаписи</span><span class="sxs-lookup"><span data-stu-id="a026e-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="a026e-138">Выберите **Power Platform** и выполните вход в центр администрирования Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="a026e-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="a026e-139">Выберите Power Platform</span><span class="sxs-lookup"><span data-stu-id="a026e-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="a026e-140">Выберите среду Power Apps для копирования, а затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="a026e-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="a026e-141">После завершения процесса копирования выполните вход в целевой экземпляр и включите интеграцию Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a026e-141">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="a026e-142">Для получения дополнительных сведений и инструкций см. раздел [Настройка интеграции Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="a026e-142">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="a026e-143">Элементы данных и статусы</span><span class="sxs-lookup"><span data-stu-id="a026e-143">Data elements and statuses</span></span>

<span data-ttu-id="a026e-144">Следующие элементы данных не копируются при копировании экземпляра Human Resources:</span><span class="sxs-lookup"><span data-stu-id="a026e-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="a026e-145">Адреса электронной почты в таблице **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="a026e-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="a026e-146">Журнал пакетных заданий в **BatchJobHistory**, **BatchHistory** и **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="a026e-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="a026e-147">Пароль SMTP в таблице **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="a026e-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="a026e-148">Сервер ретрансляции SMTP в таблице **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="a026e-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="a026e-149">Параметры управления печатью в таблицах **PrintMgmtSettings** и **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="a026e-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="a026e-150">Записи, специфические для данной среды в таблицах **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** и **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="a026e-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="a026e-151">Вложения документов в таблице DocuValue.</span><span class="sxs-lookup"><span data-stu-id="a026e-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="a026e-152">К этим вложениям относятся все шаблоны Microsoft Office, которые были перезаписаны в исходной среде</span><span class="sxs-lookup"><span data-stu-id="a026e-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="a026e-153">Строка доступа в таблице **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a026e-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="a026e-154">Некоторые из этих элементов не копируются, поскольку они связаны с определенной средой.</span><span class="sxs-lookup"><span data-stu-id="a026e-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="a026e-155">Примерами являются записи **BatchServerConfig** и **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="a026e-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="a026e-156">Другие элементы не копируются из-за объема запросов технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="a026e-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="a026e-157">Пример:</span><span class="sxs-lookup"><span data-stu-id="a026e-157">For example:</span></span>

- <span data-ttu-id="a026e-158">Повторяющиеся сообщения электронной почты могут быть отправлены, поскольку протокол SMTP все еще включен в среде приемочного тестирования пользователем (песочнице).</span><span class="sxs-lookup"><span data-stu-id="a026e-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="a026e-159">Недопустимые сообщения интеграции могут быть отправлены, так как все еще включены пакетные задания.</span><span class="sxs-lookup"><span data-stu-id="a026e-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="a026e-160">Пользователи могут быть включены, прежде чем администраторы смогут выполнять действия по очистке после обновления.</span><span class="sxs-lookup"><span data-stu-id="a026e-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="a026e-161">Также при копировании экземпляра изменяются следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="a026e-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="a026e-162">Все пользователи, кроме администраторов задаются как **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="a026e-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="a026e-163">Все пакетные задания, за исключением некоторых системных заданий, устанавливаются в значение **Удержание**.</span><span class="sxs-lookup"><span data-stu-id="a026e-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="a026e-164">Администратор среды</span><span class="sxs-lookup"><span data-stu-id="a026e-164">Environment admin</span></span>

<span data-ttu-id="a026e-165">Все пользователи в целевой среде песочницы, включая администраторов, заменяются пользователями исходной среды.</span><span class="sxs-lookup"><span data-stu-id="a026e-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="a026e-166">Перед копированием экземпляра убедитесь, что вы являетесь администратором в исходной среде.</span><span class="sxs-lookup"><span data-stu-id="a026e-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="a026e-167">Если это не так, после завершения копирования вы не сможете войти в целевую среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="a026e-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="a026e-168">Все пользователи, не являющиеся администраторами в целевой среде песочницы, отключены для защиты от нежелательного входа в среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="a026e-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="a026e-169">Администраторы могут повторно включить пользователей, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a026e-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-common-data-service"></a><span data-ttu-id="a026e-170">Применение настраиваемых полей к Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a026e-170">Apply custom fields to Common Data Service</span></span>

<span data-ttu-id="a026e-171">Если экземпляр копируется в среду "песочницы" и требуется интегрировать среду "песочницы" с Common Data Service, необходимо повторно применить настраиваемые поля к сущностям Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a026e-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Common Data Service, you must reapply custom fields to Common Data Service entities.</span></span>

<span data-ttu-id="a026e-172">Для каждого настраиваемого поля, доступного для сущностей Common Data Service, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="a026e-172">For each custom field that's exposed on Common Data Service entities, do the following steps:</span></span>

1. <span data-ttu-id="a026e-173">Перейдите в настраиваемое поле и выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a026e-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="a026e-174">Отмените выбор поля **Включено** для каждой сущности cdm_\*, для которой включено настраиваемое поле.</span><span class="sxs-lookup"><span data-stu-id="a026e-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="a026e-175">Выберите **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="a026e-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="a026e-176">Снова выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a026e-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="a026e-177">Выберите поле **Включено** для каждой сущности cdm_\*, для которой включено настраиваемое поле.</span><span class="sxs-lookup"><span data-stu-id="a026e-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="a026e-178">Снова выберите **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="a026e-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="a026e-179">Процесс отмены выбора, применения изменений, повторного выбора и повторного применения изменений приводит к изменению схемы в Common Data Service, чтобы включить в нее настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="a026e-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Common Data Service to include the custom fields.</span></span>

<span data-ttu-id="a026e-180">Дополнительные сведения о настраиваемых полях см. в разделе [Создание настраиваемых полей и работа с ними](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="a026e-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="a026e-181">См. также</span><span class="sxs-lookup"><span data-stu-id="a026e-181">See also</span></span>

[<span data-ttu-id="a026e-182">Обеспечение Human Resources</span><span class="sxs-lookup"><span data-stu-id="a026e-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="a026e-183">Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="a026e-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="a026e-184">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="a026e-184">Update process</span></span>](hr-admin-setup-update-process.md)

