---
title: "Сброс киоска данных финансовой отчетности после восстановления базы данных"
description: "В этом разделе описывается, как сбросить киоск данных финансовой отчетности после восстановления базы данных Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="cd8b0-103">Сброс киоска данных финансовой отчетности после восстановления базы данных</span><span class="sxs-lookup"><span data-stu-id="cd8b0-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cd8b0-104">В этом разделе описывается, как сбросить киоск данных финансовой отчетности после восстановления базы данных Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="cd8b0-105">Если вам когда-либо придется восстанавливать свою базу данных Finance and Operations из резервной копии или копировать базу данных из другой среды, необходимо выполнить действия, описанные в этой теме, чтобы гарантировать использование киоском данных финансовой отчетности восстановленной базы данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="cd8b0-106">Шаги в этом процессе поддерживаются для Dynamics 365 for Operations выпуска за май 2016 г. (сборка приложения 7.0.1265.23014 и сборка финансовой отчетности 7.0.10000.4) и более новых версий.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="cd8b0-107">Если у вас более ранняя версия Finance and Operations, обратитесь к специалисту службы поддержки за помощью.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="cd8b0-108">Экспорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="cd8b0-108">Export report definitions</span></span>
<span data-ttu-id="cd8b0-109">Сначала экспортируйте макеты отчетов, расположенные в конструкторе отчетов, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="cd8b0-110">В конструкторе отчетов откройте **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="cd8b0-111">Выберите группу строительных блоков, которую требуется экспортировать, и нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="cd8b0-112">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="cd8b0-113">Выберите определения отчета для экспорта:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="cd8b0-114">Для того, чтобы экспортировать все ваши определения отчета и связанные строительные блоки, щелкните **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="cd8b0-115">Чтобы экспортировать определенные отчеты, строки, столбцы, деревья или наборы аналитик, щелкните соответствующую вкладку и выберите элементы для экспорта.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="cd8b0-116">Нажмите и удерживайте клавишу CTRL, чтобы выбрать несколько элементов на вкладке. При выборе отчетов для экспорта выбираются соответствующие строки, столбцы, структуры и наборы аналитик.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="cd8b0-117">Щелкните **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-117">Click **Export**.</span></span>
5.  <span data-ttu-id="cd8b0-118">Введите имя файла и выберите безопасное место, где требуется сохранить экспортированные определения отчетов.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="cd8b0-119">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-119">Click **Save**.</span></span>

<span data-ttu-id="cd8b0-120">Файл можно скопировать или отправить в безопасное место, что позволяет импортировать его в другую среду в другое время.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="cd8b0-121">Сведения об использовании учетной записи хранилища Microsoft Azure можно найти в разделе [Перенос данных с помощью служебной программы командной строки AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="cd8b0-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="cd8b0-122">Корпорация Майкрософт не предоставляет учетную запись хранилища в составе договора на Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="cd8b0-123">Необходимо либо приобрести учетную запись хранилища, либо использовать учетную запись хранилища из отдельной подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="cd8b0-124">Помните о поведении диска D в виртуальных машинах Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="cd8b0-125">Не следует постоянно хранить на нем свои экспортированные группы строительных блоков.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="cd8b0-126">Дополнительные сведения о временных дисках см. в разделе [Понимание временного диска на виртуальных машинах Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="cd8b0-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="cd8b0-127">Остановка служб</span><span class="sxs-lookup"><span data-stu-id="cd8b0-127">Stop services</span></span>
<span data-ttu-id="cd8b0-128">С помощью удаленного рабочего стола подключитесь ко всем компьютерам в среде и остановите следующие службы Windows с помощью services.msc:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="cd8b0-129">Служба веб-публикаций (на всех компьютерах AOS)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="cd8b0-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="cd8b0-131">Management Reporter 2012 Process Service (только на компьютерах BI)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="cd8b0-132">Эти службы будут иметь открытые подключения к базе данных Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="cd8b0-133">Сбросить</span><span class="sxs-lookup"><span data-stu-id="cd8b0-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="cd8b0-134">Поиск и загрузка последней версии пакета MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="cd8b0-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="cd8b0-135">Найдите последний пакет MinorVersionDataUpgrade.zip с помощью инструкций из раздела [Загрузка последнего готового к развертыванию пакета обновления данных](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="cd8b0-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="cd8b0-136">В этих инструкциях поясняется, как найти и загрузить правильную версию пакета обновления данных.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="cd8b0-137">Для загрузки пакета MinorVersionDataUpgrade.zip не требуется обновление.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="cd8b0-138">Необходим просто выполнить действия, описанные в разделе "Загрузка последнего готового к развертыванию пакета обновления данных" без выполнения каких-либо других шагов в статье, чтобы получить копию пакета MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="cd8b0-139">Выполнение сценариев для базы данных Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cd8b0-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="cd8b0-140">Запустите следующие сценарии для базы данных Finance and Operations (не для базы данных финансовых отчетов).</span><span class="sxs-lookup"><span data-stu-id="cd8b0-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="cd8b0-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="cd8b0-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="cd8b0-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="cd8b0-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="cd8b0-143">Эти сценарии обеспечивают правильность пользователей, ролей и параметров изменения отслеживания.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="cd8b0-144">Выполнение команды PowerShell для сброса базы данных</span><span class="sxs-lookup"><span data-stu-id="cd8b0-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="cd8b0-145">На компьютере с сервером AOS выполните следующие команды в PowerShell от имени администратора, чтобы сбросить интеграцию между Finance and Operations и финансовой отчетностью:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="cd8b0-146">После выполнения команд вам будет предложено ввести "Y" для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="cd8b0-147">Объяснение параметров:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="cd8b0-148">Допустимые значения для параметра -Reason: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="cd8b0-149">Параметр -ReasonDetail является произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="cd8b0-150">Значения параметров reason и reasonDetail записываются в данных телеметрии/мониторинга среды.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="cd8b0-151">Запуск служб</span><span class="sxs-lookup"><span data-stu-id="cd8b0-151">Start services</span></span>
<span data-ttu-id="cd8b0-152">Используйте services.msc, чтобы перезапустить службы, остановленные ранее:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="cd8b0-153">Служба веб-публикаций (на всех компьютерах AOS)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="cd8b0-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="cd8b0-155">Management Reporter 2012 Process Service (только на компьютерах BI)</span><span class="sxs-lookup"><span data-stu-id="cd8b0-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="cd8b0-156">Импорт определений отчетов</span><span class="sxs-lookup"><span data-stu-id="cd8b0-156">Import report definitions</span></span>
<span data-ttu-id="cd8b0-157">Импортируйте макеты отчетов из конструктора отчетов, используя файл, созданный во время экспорта:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="cd8b0-158">В конструкторе отчетов откройте **Компания** &gt; **Группы строительных блоков**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="cd8b0-159">Выберите группу строительных блоков, которую требуется экспортировать, и нажмите кнопку **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="cd8b0-160">Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="cd8b0-161">Выберите строительный блок **По умолчанию** и нажмите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="cd8b0-162">Выберите файл, содержащий экспортированные определения отчетов, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="cd8b0-163">В диалоговом окнеИмпорт, выберите определения отчета для того, чтобы импортировать:</span><span class="sxs-lookup"><span data-stu-id="cd8b0-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="cd8b0-164">Чтобы импортировать все определения отчетов и поддерживающие строительные блоки, щелкните **Выбрать все**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="cd8b0-165">Для того, чтобы импортировать специфические отчеты, строки, столбцы, деревья, или Наборы аналитик, выбирают отчеты, строки, столбцы, деревья, или Наборы аналитик, которые импортировать.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="cd8b0-166">Нажмите кнопку **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="cd8b0-166">Click **Import**.</span></span>





