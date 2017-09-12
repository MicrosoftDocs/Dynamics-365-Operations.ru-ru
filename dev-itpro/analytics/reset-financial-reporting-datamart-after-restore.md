---
title: "Сброс киоска данных финансовой отчетности после восстановления базы данных"
description: "В этом разделе описывается, как сбросить киоск данных финансовой отчетности после восстановления базы данных Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: ru-ru
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="75991-103">Сброс киоска данных финансовой отчетности после восстановления базы данных</span><span class="sxs-lookup"><span data-stu-id="75991-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="75991-104">В этом разделе описывается, как сбросить киоск данных финансовой отчетности после восстановления базы данных Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75991-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="75991-105">Если вам когда-либо придется восстанавливать свою базу данных Finance and Operations из резервной копии или копировать базу данных из другой среды, необходимо выполнить действия, описанные в этой теме, чтобы гарантировать использование киоском данных финансовой отчетности восстановленной базы данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75991-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="75991-106">Шаги в этом процессе поддерживаются для Dynamics 365 for Operations выпуска за май 2016 г. (сборка приложения 7.0.1265.23014 и сборка финансовой отчетности 7.0.10000.4) и более новых версий.</span><span class="sxs-lookup"><span data-stu-id="75991-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="75991-107">Если у вас более ранняя версия Finance and Operations, обратитесь к специалисту службы поддержки за помощью.</span><span class="sxs-lookup"><span data-stu-id="75991-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="75991-108">Экспорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="75991-108">Export report definitions</span></span>
<span data-ttu-id="75991-109">Сначала экспортируйте макеты отчетов, расположенные в конструкторе отчетов, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="75991-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="75991-110">В конструкторе отчетов откройте **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="75991-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="75991-111">Выберите группу строительных блоков, которую требуется экспортировать, и нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="75991-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="75991-112">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="75991-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="75991-113">Выберите определения отчета для экспорта:</span><span class="sxs-lookup"><span data-stu-id="75991-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="75991-114">Для того, чтобы экспортировать все ваши определения отчета и связанные строительные блоки, щелкните **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="75991-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="75991-115">Чтобы экспортировать определенные отчеты, строки, столбцы, деревья или наборы аналитик, щелкните соответствующую вкладку и выберите элементы для экспорта.</span><span class="sxs-lookup"><span data-stu-id="75991-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="75991-116">Нажмите и удерживайте нажатой клавишу CTRL, чтобы выбрать многочисленные элементы на вкладке.</span><span class="sxs-lookup"><span data-stu-id="75991-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="75991-117">Когда вы выбираете отчеты для экспорта, выбираются связанные строки, столбцы, деревья, и наборы аналитик.</span><span class="sxs-lookup"><span data-stu-id="75991-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="75991-118">Щелкните **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="75991-118">Click **Export**.</span></span>
5.  <span data-ttu-id="75991-119">Введите имя файла и выберите безопасное место, где требуется сохранить экспортированные определения отчетов.</span><span class="sxs-lookup"><span data-stu-id="75991-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="75991-120">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="75991-120">Click **Save**.</span></span>

<span data-ttu-id="75991-121">Файл можно скопировать или отправить в безопасное место, что позволяет импортировать его в другую среду в другое время.</span><span class="sxs-lookup"><span data-stu-id="75991-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="75991-122">Сведения об использовании учетной записи хранилища Microsoft Azure можно найти в разделе [Перенос данных с помощью служебной программы командной строки AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="75991-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="75991-123">Корпорация Майкрософт не предоставляет учетную запись хранилища в составе договора на Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75991-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="75991-124">Необходимо либо приобрести учетную запись хранилища, либо использовать учетную запись хранилища из отдельной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="75991-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="75991-125">Помните о поведении диска D в виртуальных машинах Azure.</span><span class="sxs-lookup"><span data-stu-id="75991-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="75991-126">Не следует постоянно хранить на нем свои экспортированные группы строительных блоков.</span><span class="sxs-lookup"><span data-stu-id="75991-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="75991-127">Дополнительные сведения о временных дисках см. в разделе [Понимание временного диска на виртуальных машинах Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="75991-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="75991-128">Остановка служб</span><span class="sxs-lookup"><span data-stu-id="75991-128">Stop services</span></span>
<span data-ttu-id="75991-129">С помощью удаленного рабочего стола подключитесь ко всем компьютерам в среде и остановите следующие службы Windows с помощью services.msc:</span><span class="sxs-lookup"><span data-stu-id="75991-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="75991-130">Служба веб-публикаций (на всех компьютерах AOS)</span><span class="sxs-lookup"><span data-stu-id="75991-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="75991-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="75991-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="75991-132">Management Reporter 2012 Process Service (только на компьютерах BI)</span><span class="sxs-lookup"><span data-stu-id="75991-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="75991-133">Эти службы будут иметь открытые подключения к базе данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75991-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="75991-134">Сбросить</span><span class="sxs-lookup"><span data-stu-id="75991-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="75991-135">Поиск и загрузка последней версии пакета MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="75991-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="75991-136">Найдите последний пакет MinorVersionDataUpgrade.zip с помощью инструкций из раздела [Загрузка последнего готового к развертыванию пакета обновления данных](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="75991-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="75991-137">В этих инструкциях поясняется, как найти и загрузить правильную версию пакета обновления данных.</span><span class="sxs-lookup"><span data-stu-id="75991-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="75991-138">Для загрузки пакета MinorVersionDataUpgrade.zip не требуется обновление.</span><span class="sxs-lookup"><span data-stu-id="75991-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="75991-139">Необходим просто выполнить действия, описанные в разделе "Загрузка последнего готового к развертыванию пакета обновления данных" без выполнения каких-либо других шагов в статье, чтобы получить копию пакета MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="75991-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="75991-140">Выполнение сценариев для базы данных Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75991-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="75991-141">Запустите следующие сценарии для базы данных Finance and Operations (не для базы данных финансовых отчетов).</span><span class="sxs-lookup"><span data-stu-id="75991-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="75991-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="75991-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="75991-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="75991-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="75991-144">Эти сценарии обеспечивают правильность пользователей, ролей и параметров изменения отслеживания.</span><span class="sxs-lookup"><span data-stu-id="75991-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="75991-145">Выполнение команды PowerShell для сброса базы данных</span><span class="sxs-lookup"><span data-stu-id="75991-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="75991-146">Выполните следующую команду, непосредственно на компьютере с сервером AOS, чтобы сбросить интеграцию между Finance and Operations и финансовой отчетностью:</span><span class="sxs-lookup"><span data-stu-id="75991-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="75991-147">Откройте Windows PowerShell от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="75991-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="75991-148">Выполните: F:</span><span class="sxs-lookup"><span data-stu-id="75991-148">Execute: F:</span></span>
3.  <span data-ttu-id="75991-149">Выполните: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="75991-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="75991-150">Выполните: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="75991-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="75991-151">Выполните: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;моя причина для сброса&gt;”</span><span class="sxs-lookup"><span data-stu-id="75991-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="75991-152">Будет предложено ввести «Y» для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="75991-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="75991-153">Объяснение параметров:</span><span class="sxs-lookup"><span data-stu-id="75991-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="75991-154">Допустимые значения для параметра -Reason: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="75991-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="75991-155">Параметр -ReasonDetail является произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="75991-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="75991-156">Значения параметров reason и reasonDetail записываются в данных телеметрии/мониторинга среды.</span><span class="sxs-lookup"><span data-stu-id="75991-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="75991-157">Запуск служб</span><span class="sxs-lookup"><span data-stu-id="75991-157">Start services</span></span>
<span data-ttu-id="75991-158">Используйте services.msc, чтобы перезапустить службы, остановленные ранее:</span><span class="sxs-lookup"><span data-stu-id="75991-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="75991-159">Служба веб-публикаций (на всех компьютерах AOS)</span><span class="sxs-lookup"><span data-stu-id="75991-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="75991-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="75991-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="75991-161">Management Reporter 2012 Process Service (только на компьютерах BI)</span><span class="sxs-lookup"><span data-stu-id="75991-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="75991-162">Импорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="75991-162">Import report definitions</span></span>
<span data-ttu-id="75991-163">Импортируйте макеты отчетов из конструктора отчетов, используя файл, созданный во время экспорта:</span><span class="sxs-lookup"><span data-stu-id="75991-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="75991-164">В конструкторе отчетов откройте **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="75991-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="75991-165">Выберите группу строительных блоков, которую требуется экспортировать, и нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="75991-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="75991-166">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="75991-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="75991-167">Выберите строительный блок **По умолчанию** и нажмите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="75991-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="75991-168">Выберите файл, содержащий экспортированные определения отчетов, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="75991-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="75991-169">В диалоговом окнеИмпорт, выберите определения отчета для того, чтобы импортировать:</span><span class="sxs-lookup"><span data-stu-id="75991-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="75991-170">Чтобы импортировать все определения отчетов и поддерживающие строительные блоки, щелкните **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="75991-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="75991-171">Для того, чтобы импортировать специфические отчеты, строки, столбцы, деревья, или Наборы аналитик, выбирают отчеты, строки, столбцы, деревья, или Наборы аналитик, которые импортировать.</span><span class="sxs-lookup"><span data-stu-id="75991-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="75991-172">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="75991-172">Click **Import**.</span></span>





