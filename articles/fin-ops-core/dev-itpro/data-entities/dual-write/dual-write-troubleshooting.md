---
title: Общие рекомендации по устранению неполадок
description: Эта тема предоставляет общая информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse.
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
ms.openlocfilehash: 6356ec6850667f32f9e9e4133686c40f0b6d76d7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688267"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="a2b5f-103">Общие рекомендации по устранению неполадок</span><span class="sxs-lookup"><span data-stu-id="a2b5f-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="a2b5f-104">Эта тема предоставляет общая информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2b5f-105">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a2b5f-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a2b5f-106">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="a2b5f-107">При попытке установить пакет двойной записи с помощью средства Package Deployer доступные решения не отображаются</span><span class="sxs-lookup"><span data-stu-id="a2b5f-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="a2b5f-108">Некоторые версии средства Package Deployer несовместимы с пакетом решения двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="a2b5f-109">Для успешной установки пакета следует использовать [версию 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) или более позднюю версию средства Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="a2b5f-110">После установки средства Package Deployer установите пакет решения, выполнив следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="a2b5f-111">Скачайте последний файл пакета решения из Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="a2b5f-112">После скачивания ZIP-файла пакета щелкните его правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="a2b5f-113">Установите флажок **Разблокировать**, затем выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="a2b5f-114">Если флажок **Разблокировать** не виден, ZIP-файл уже разблокирован и этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Диалоговое окно свойств](media/unblock_option.png)

2. <span data-ttu-id="a2b5f-116">Извлеките ZIP-файл пакета и скопируйте все файлы в папку **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Содержимое папки Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="a2b5f-118">Вставьте все скопированные файлы в папку **Tools** средства Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="a2b5f-119">Запустите **PackageDeployer.exe**, чтобы выбрать среду Dataverse и установить все решения.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Содержимое папки Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="a2b5f-121">Включение и просмотр журнала трассировки подключаемого модуля в Dataverse для просмотра подробных сведений об ошибке</span><span class="sxs-lookup"><span data-stu-id="a2b5f-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="a2b5f-122">**Роль, необходимая для включения журнала трассировки и просмотра ошибок:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="a2b5f-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="a2b5f-123">Чтобы включить журнал трассировки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="a2b5f-124">Выполните вход в приложение на основе модели в Dynamics 365, откройте страницу **Параметры**, затем в области **Система** выберите **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="a2b5f-125">На странице **Администрирование** выберите **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="a2b5f-126">На вкладке **Настройка** в поле **Трассировка подключаемого модуля и пользовательского действия рабочего процесса** выберите **Все**, чтобы включить журнал трассировки подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="a2b5f-127">Если требуется вести журналы трассировки только при возникновении исключений, вместо этого можно выбрать **Исключение**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="a2b5f-128">Чтобы просмотреть журнал трассировки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="a2b5f-129">Выполните вход в приложение на основе модели в Dynamics 365, откройте страницу **Параметры**, затем в области **Настройка** выберите **Журнал трассировки подключаемого модуля**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="a2b5f-130">Найдите журналы трассировки, для которых в поле **Имя типа** указано значение **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="a2b5f-131">Дважды щелкните элемент, чтобы просмотреть полный журнал, а затем на экспресс-вкладке **Выполнение** просмотрите текст **Блок сообщений**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="a2b5f-132">Включение режима отладки для устранения проблем с синхронизацией приложений Finance and Operations в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="a2b5f-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="a2b5f-133">**Роль, необходимая для просмотра ошибок:** системный администратор Ошибки двойной записи, которые возникают в Dataverse, могут отображаться в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="a2b5f-134">В некоторых случаях полный текст сообщения об ошибке недоступен, поскольку сообщение слишком длинное или содержит личную идентификационную информацию (PII).</span><span class="sxs-lookup"><span data-stu-id="a2b5f-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="a2b5f-135">Подробное протоколирование ошибок можно включить, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="a2b5f-136">Все конфигурации проектов в приложениях Finance and Operations имеют свойство **IsDebugMode** в объекте **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="a2b5f-137">Откройте объект **DualWriteProjectConfiguration** с помощью надстройки Excel.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="a2b5f-138">Простой способ открыть объект — включить режим **Конструктор** в надстройке Excel, затем добавить **DualWriteProjectConfigurationEntity** на лист.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="a2b5f-139">Дополнительные сведения см. в разделе [Открытие данных объекта в Excel и из обновление с помощью надстройки Excel](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="a2b5f-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="a2b5f-140">Установите для свойства **IsDebugMode** значение **Да** для проекта.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="a2b5f-141">Выполните сценарий, создающий ошибки.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="a2b5f-142">Подробные журналы доступны в таблице DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="a2b5f-143">Для просмотра данных в обозревателе таблиц используйте следующий URL-адрес (замените **XXX** требуемыми символами):</span><span class="sxs-lookup"><span data-stu-id="a2b5f-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="a2b5f-144">Проверка ошибок синхронизации на виртуальной машине для приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2b5f-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="a2b5f-145">**Роль, требуемая для просмотра ошибок:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="a2b5f-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="a2b5f-146">Выполните вход в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a2b5f-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="a2b5f-147">Откройте проект LCS, который вы выбрали для выполнения тестирования двойной записи.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="a2b5f-148">Выберите плитку **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="a2b5f-149">Используйте удаленный рабочий стол для входа в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="a2b5f-150">Используйте локальную учетную запись, отображаемую в LCS.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="a2b5f-151">Откройте средство просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-151">Open Event viewer.</span></span>
6. <span data-ttu-id="a2b5f-152">Выберите **Журналы приложений и служб \> Microsoft \> Dynamics \> AX-DualWriteSync \> Операционные**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="a2b5f-153">Просмотрите список недавних ошибок.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="a2b5f-154">Удаление связи и связывание с другой средой Dataverse из приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2b5f-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="a2b5f-155">**Роль, необходимая для отмены связи со средой:** системный администратор для приложения Finance and Operations или Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="a2b5f-156">Выполните вход в приложение Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="a2b5f-157">Выберите **Рабочие области \> Управление данными** и выберите плитку **Двойная запись**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="a2b5f-158">Выберите все запущенные отображения, затем выберите **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="a2b5f-159">Выберите **Удалить связь со средой**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="a2b5f-160">Выберите **Да**, чтобы подтвердить операцию.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="a2b5f-161">Теперь можно связать новую среду.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="a2b5f-162">Не удается просмотреть форму сведений о строке заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="a2b5f-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="a2b5f-163">При создании заказа на продажу в Dynamics 365 Sales при нажатии кнопки **+ Добавить продукты** вы можете быть перенаправлены в форму строки заказа Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="a2b5f-164">Из этой формы невозможно просмотреть форму **Сведения** строки заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="a2b5f-165">Параметр для **Сведений** не отображается в раскрывающемся списке в поле **Создать строку заказа**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="a2b5f-166">Это происходит из-за того, что приложение Project Operations было установлено в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="a2b5f-167">Для повторного включения параметра формы **Сведения** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a2b5f-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="a2b5f-168">Перейдите к объекту **Строка заказа**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="a2b5f-169">Найдите форму **Сведения** в узле форм.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="a2b5f-170">Выберите форму **Сведения** и щелкните **Включить роли безопасности**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="a2b5f-171">Измените параметр безопасности на **Показывать всем**.</span><span class="sxs-lookup"><span data-stu-id="a2b5f-171">Change the security setting to **Display to everyone**.</span></span>
