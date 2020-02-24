---
title: Копирование экземпляра
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010288"
---
# <a name="copy-an-instance"></a><span data-ttu-id="2db9b-102">Копирование экземпляра</span><span class="sxs-lookup"><span data-stu-id="2db9b-102">Copy an instance</span></span>

<span data-ttu-id="2db9b-103">Можно использовать Microsoft Dynamics Lifecycle Services (LCS) для копирования базы данных Microsoft Dynamics 365 Human Resources в среду в песочнице.</span><span class="sxs-lookup"><span data-stu-id="2db9b-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="2db9b-104">При наличии другой среды-песочницы можно также скопировать базу данных из этой среды в целевую среду-песочницу.</span><span class="sxs-lookup"><span data-stu-id="2db9b-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="2db9b-105">Чтобы скопировать экземпляр, необходимо обеспечить следующее:</span><span class="sxs-lookup"><span data-stu-id="2db9b-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="2db9b-106">Экземпляр Human Resources, который требуется перезаписывать, должен быть средой песочницы.</span><span class="sxs-lookup"><span data-stu-id="2db9b-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="2db9b-107">Среды, которых копируются, должны быть в одном регионе.</span><span class="sxs-lookup"><span data-stu-id="2db9b-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="2db9b-108">Нельзя копировать по регионам.</span><span class="sxs-lookup"><span data-stu-id="2db9b-108">You can't copy across regions.</span></span>

- <span data-ttu-id="2db9b-109">Вы должны быть администратором в целевой среде, чтобы можно было войти в систему после копирования экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2db9b-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="2db9b-110">При копировании базы данных Human Resources не копируются элементы (приложения или данные), содержащиеся в среде Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="2db9b-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="2db9b-111">Сведения о способе копирования элементов в среде PowerApps см. в разделе [Копирование среды](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="2db9b-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="2db9b-112">Среда PowerApps, которую требуется перезаписывать, должна быть средой песочницы.</span><span class="sxs-lookup"><span data-stu-id="2db9b-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="2db9b-113">Чтобы изменить производственную среду PowerApps на среду песочницы, необходимо быть глобальным администратором клиента.</span><span class="sxs-lookup"><span data-stu-id="2db9b-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="2db9b-114">Дополнительные сведения об изменении среды PowerApps см. в разделе [Переключение экземпляра](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="2db9b-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="2db9b-115">Результаты копирования базы данных Human Resources</span><span class="sxs-lookup"><span data-stu-id="2db9b-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="2db9b-116">При копировании базы данных Human Resources происходят следующие события:</span><span class="sxs-lookup"><span data-stu-id="2db9b-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="2db9b-117">Процесс копирования стирает существующую базу данных в целевой среде.</span><span class="sxs-lookup"><span data-stu-id="2db9b-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="2db9b-118">После завершения процесса копирования восстановить существующую базу данных невозможно.</span><span class="sxs-lookup"><span data-stu-id="2db9b-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="2db9b-119">Целевая среда будет недоступна до завершения процесса копирования.</span><span class="sxs-lookup"><span data-stu-id="2db9b-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="2db9b-120">Документы в хранилище BLOB-объектов Microsoft Azure не копируются из одной среды в другую.</span><span class="sxs-lookup"><span data-stu-id="2db9b-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="2db9b-121">Таким образом, все документы и шаблоны, которые прикрепляются, не будут скопированы и останутся в исходной среде.</span><span class="sxs-lookup"><span data-stu-id="2db9b-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="2db9b-122">Все пользователи, кроме администратора и других учетных записей пользователей внутренних служб, будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="2db9b-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="2db9b-123">Таким образом, пользователь с правами администратора может удалять или заменять данные до того, как другие пользователи смогут вернуться в систему.</span><span class="sxs-lookup"><span data-stu-id="2db9b-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="2db9b-124">Пользователь-администратор должен выполнить необходимые изменения конфигурации, такие как повторное подключение конечных точек интеграции к отдельным службам или URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="2db9b-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="2db9b-125">Копирование базы данных Human Resources</span><span class="sxs-lookup"><span data-stu-id="2db9b-125">Copy the Human Resources database</span></span>

<span data-ttu-id="2db9b-126">Чтобы выполнить эту задачу, необходимо сначала скопировать экземпляр, а затем войти в центр администрирования Microsoft Power Platform, чтобы скопировать среду PowerApps.</span><span class="sxs-lookup"><span data-stu-id="2db9b-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="2db9b-127">При копировании экземпляра база данных удаляется из целевого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2db9b-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="2db9b-128">Целевой экземпляр недоступен в ходе этого процесса.</span><span class="sxs-lookup"><span data-stu-id="2db9b-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="2db9b-129">Выполните вход LCS и выберите проект LCS, содержащий экземпляр, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="2db9b-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="2db9b-130">В проекте LCS выберите плитку **Управление приложением Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="2db9b-131">Выберите экземпляр для копирования, а затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="2db9b-132">В области задач **Копирование экземпляра** выберите экземпляр, который требуется перезаписать, и нажмите кнопку **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="2db9b-133">Дождитесь обновления значения поля **Статус копирования** до **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="2db9b-134">Выберите экземпляр для перезаписи</span><span class="sxs-lookup"><span data-stu-id="2db9b-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="2db9b-135">Выберите **Power Platform** и выполните вход в центр администрирования Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="2db9b-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="2db9b-136">Выберите Power Platform</span><span class="sxs-lookup"><span data-stu-id="2db9b-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="2db9b-137">Выберите среду PowerApps для копирования, а затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="2db9b-138">После завершения процесса копирования выполните вход в целевой экземпляр и включите интеграцию Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="2db9b-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="2db9b-139">Для получения дополнительных сведений и инструкций см. раздел [Настройка интеграции Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="2db9b-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="2db9b-140">Элементы данных и статусы</span><span class="sxs-lookup"><span data-stu-id="2db9b-140">Data elements and statuses</span></span>

<span data-ttu-id="2db9b-141">Следующие элементы данных не копируются при копировании экземпляра Human Resources:</span><span class="sxs-lookup"><span data-stu-id="2db9b-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="2db9b-142">Адреса электронной почты в таблице **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="2db9b-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="2db9b-143">Журнал пакетных заданий в **BatchJobHistory**, **BatchHistory** и **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="2db9b-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="2db9b-144">Пароль SMTP в таблице **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="2db9b-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="2db9b-145">Сервер ретрансляции SMTP в таблице **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="2db9b-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="2db9b-146">Параметры управления печатью в таблицах **PrintMgmtSettings** и **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="2db9b-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="2db9b-147">Записи, специфические для данной среды в таблицах **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** и **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="2db9b-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="2db9b-148">Вложения документов в таблице DocuValue.</span><span class="sxs-lookup"><span data-stu-id="2db9b-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="2db9b-149">К этим вложениям относятся все шаблоны Microsoft Office, которые были перезаписаны в исходной среде</span><span class="sxs-lookup"><span data-stu-id="2db9b-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="2db9b-150">Строка доступа в таблице **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="2db9b-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="2db9b-151">Некоторые из этих элементов не копируются, поскольку они связаны с определенной средой.</span><span class="sxs-lookup"><span data-stu-id="2db9b-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="2db9b-152">Примерами являются записи **BatchServerConfig** и **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="2db9b-153">Другие элементы не копируются из-за объема запросов технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="2db9b-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="2db9b-154">Например, повторяющиеся сообщения электронной почты могут быть отправлены, поскольку протокол SMTP все еще включен в среде приемочного тестирования пользователя (песочнице), могут быть отправлены недопустимые сообщения интеграции, так как пакетные задания по-прежнему включены, и пользователи могут быть включены до того, как администраторы смогут выполнить действия по очистке после обновления.</span><span class="sxs-lookup"><span data-stu-id="2db9b-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="2db9b-155">Кроме того, при копировании экземпляра изменяются следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="2db9b-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="2db9b-156">Все пользователи, кроме администраторов задаются как **Отключено**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="2db9b-157">Все пакетные задания, за исключением некоторых системных заданий, устанавливаются в значение **Удержание**.</span><span class="sxs-lookup"><span data-stu-id="2db9b-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="2db9b-158">Администратор среды</span><span class="sxs-lookup"><span data-stu-id="2db9b-158">Environment admin</span></span>

<span data-ttu-id="2db9b-159">Все пользователи в целевой среде песочницы, включая администраторов, заменяются пользователями исходной среды.</span><span class="sxs-lookup"><span data-stu-id="2db9b-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="2db9b-160">Перед копированием экземпляра убедитесь, что вы являетесь администратором в целевой среде.</span><span class="sxs-lookup"><span data-stu-id="2db9b-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="2db9b-161">Если это не так, после завершения копирования вы не сможете войти в целевую среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="2db9b-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="2db9b-162">Все пользователи, не являющиеся администраторами в целевой среде песочницы, отключены для защиты от нежелательного входа в среду песочницы.</span><span class="sxs-lookup"><span data-stu-id="2db9b-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="2db9b-163">Администраторы могут повторно включить пользователей, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="2db9b-163">Administrators can reenable users if needed.</span></span>
