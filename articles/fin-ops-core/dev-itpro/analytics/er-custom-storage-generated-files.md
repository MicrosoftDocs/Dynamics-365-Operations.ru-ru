---
title: Определение расположений пользовательского хранилища для создаваемых документов
description: В этом разделе объясняется, как расширить список местоположения хранения для документов, которые формируются форматами электронной отчетности (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680766"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="28cfd-103">Определение расположений пользовательского хранилища для создаваемых документов</span><span class="sxs-lookup"><span data-stu-id="28cfd-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="28cfd-104">Интерфейс прикладного программирования (API) платформы электронной отчетности (ER) позволяет расширять список местоположения хранения для документов, формируемых форматами ER.</span><span class="sxs-lookup"><span data-stu-id="28cfd-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="28cfd-105">В этой теме объясняется, как добавить пользовательское место хранения для созданных документов путем делегирования задачи создания мест назначения электронной отчетности в фабрику мест назначения по умолчанию и последующей реализации пользовательского класса, имеющего свою собственную логику места назначения.</span><span class="sxs-lookup"><span data-stu-id="28cfd-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="28cfd-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="28cfd-106">Prerequisites</span></span>

<span data-ttu-id="28cfd-107">Разверните топологию, которая поддерживает непрерывную сборку.</span><span class="sxs-lookup"><span data-stu-id="28cfd-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="28cfd-108">Дополнительные сведения см. в разделе [Развертывание топологий, которые поддерживают непрерывное построение и автоматизацию тестирования](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span><span class="sxs-lookup"><span data-stu-id="28cfd-108">For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="28cfd-109">Необходим доступ к этой топологии для одной из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="28cfd-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="28cfd-110">Разработчик электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="28cfd-110">Electronic reporting developer</span></span>
- <span data-ttu-id="28cfd-111">Консультант по функциональным возможностям электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="28cfd-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="28cfd-112">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="28cfd-112">System administrator</span></span>

<span data-ttu-id="28cfd-113">Кроме того, необходим доступ к среде разработки для этой топологии.</span><span class="sxs-lookup"><span data-stu-id="28cfd-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="28cfd-114">Все задачи в этой теме могут быть выполнены в компании **USMF**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="28cfd-115">Импорт формата электронной отчетности для движения основных средств</span><span class="sxs-lookup"><span data-stu-id="28cfd-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="28cfd-116">Чтобы создать документы, для которых планируется добавить пользовательское место хранения, [импортируйте](er-download-configurations-global-repo.md) конфигурацию формата электронной отчетности **Движение основных средств** в текущую топологию.</span><span class="sxs-lookup"><span data-stu-id="28cfd-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![Страница репозитория конфигурации](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="28cfd-118">Выполнение отчета о движении основных средств</span><span class="sxs-lookup"><span data-stu-id="28cfd-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="28cfd-119">Перейдите в раздел **Основные средства** \> **Запросы и отчеты** \> **Отчеты о проводках** \> **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="28cfd-120">В поле **Дата начала** введите **01.01.2017** (1 января 2017).</span><span class="sxs-lookup"><span data-stu-id="28cfd-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="28cfd-121">В поле **Дата окончания** введите **31.01.2017** (31 января 2017).</span><span class="sxs-lookup"><span data-stu-id="28cfd-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="28cfd-122">В поле **Валюта** выберите **Валюта учета**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="28cfd-123">В поле **Сопоставление формата** выберите **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="28cfd-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-124">Select **OK**.</span></span>

![Диалоговое окно времени выполнения для отчета о движении основных средств](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="28cfd-126">В Microsoft Excel просмотрите исходящий документ, который создан и доступен для загрузки.</span><span class="sxs-lookup"><span data-stu-id="28cfd-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="28cfd-127">Такое поведение является [поведением по умолчанию](electronic-reporting-destinations.md#default-behavior) для формата электронной отчетности, для которого не настроены [места назначения](electronic-reporting-destinations.md), и который выполняется в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="28cfd-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="28cfd-128">Проверка исходного кода</span><span class="sxs-lookup"><span data-stu-id="28cfd-128">Review the source code</span></span>

<span data-ttu-id="28cfd-129">Просмотрите код метода `generateReportByGER()` класса `AssetRollForwardService`.</span><span class="sxs-lookup"><span data-stu-id="28cfd-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="28cfd-130">Обратите внимание, что метод `Run()` используется для вызова платформы электронной отчетности и создания отчета **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="28cfd-131">Изменение исходного кода</span><span class="sxs-lookup"><span data-stu-id="28cfd-131">Modify the source code</span></span>

1. <span data-ttu-id="28cfd-132">В вашем проекте Visual Studio добавьте новый класс (`AssetRollForwardDestination` в данном примере) и напишите код для реализации вашего настраиваемого места назначения для создаваемых отчетов **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="28cfd-133">Метод `new()` предназначен для того, чтобы получить исходный объект места назначения электронной отчетности и управляемый логикой приложения параметр, определяющий пользовательское местоположение, в котором должны сохраняться сформированные отчеты.</span><span class="sxs-lookup"><span data-stu-id="28cfd-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="28cfd-134">В этом примере пользовательское местоположение представляет собой имя папки локальной файловой системы сервера, на котором запущена служба Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="28cfd-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="28cfd-135">Метод `saveFile()` предназначен для сохранения созданного документа в папке локальной файловой системы сервера, на котором запущена служба AOS.</span><span class="sxs-lookup"><span data-stu-id="28cfd-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="28cfd-136">В вашем проекте Visual Studio добавьте новый класс (`AssetRollForwardDestinationFactory` в данном примере) и создайте код для настройки пользовательской фабрики назначения, которая делегирует создание места назначения конечной фабрике, используемой по умолчанию, а также для создания оболочки файла назначения с собственным местом назначения.</span><span class="sxs-lookup"><span data-stu-id="28cfd-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="28cfd-137">Измените существующий класс `AssetRollForwardService` и напишите код для настройки пользовательской фабрики назначения для средства выполнения отчетов.</span><span class="sxs-lookup"><span data-stu-id="28cfd-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="28cfd-138">Обратите внимание, что при создании пользовательской фабрики назначения параметр, управляемый приложением, который определяет целевую папку, передается.</span><span class="sxs-lookup"><span data-stu-id="28cfd-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="28cfd-139">Таким образом, эта целевая папка используется для хранения созданных файлов.</span><span class="sxs-lookup"><span data-stu-id="28cfd-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="28cfd-140">Убедитесь, что указанная папка (**c:\\0** в данном примере) присутствует в локальной файловой системе сервера, на котором запущена служба AOS.</span><span class="sxs-lookup"><span data-stu-id="28cfd-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="28cfd-141">В противном случае во время выполнения будет создано исключение [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="28cfd-141">Otherwise, a [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="28cfd-142">Заново выполните сборку проекта</span><span class="sxs-lookup"><span data-stu-id="28cfd-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="28cfd-143">Повторное выполнение отчета о движении основных средств</span><span class="sxs-lookup"><span data-stu-id="28cfd-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="28cfd-144">Перейдите в раздел **Основные средства** \> **Запросы и отчеты** \> **Отчеты о проводках** \> **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="28cfd-145">В поле **Дата начала** введите значение **01.01.2017**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="28cfd-146">В поле **Дата окончания** введите значение **31.01.2017**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="28cfd-147">В поле **Валюта** выберите **Валюта учета**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="28cfd-148">В поле **Сопоставление формата** выберите **Движение основных средств**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="28cfd-149">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28cfd-149">Select **OK**.</span></span>
7. <span data-ttu-id="28cfd-150">Выполните поиск в локальной папке **C:\\0**, чтобы найти созданный файл.</span><span class="sxs-lookup"><span data-stu-id="28cfd-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="28cfd-151">Так как объект `originDestination` не используется в объекте `AssetRollForwardDestination` в этом примере, конфигурации для [мест назначения](electronic-reporting-destinations.md) в формате электронной отчетности не будут учитываться во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="28cfd-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28cfd-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="28cfd-152">Additional resources</span></span>

- [<span data-ttu-id="28cfd-153">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="28cfd-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="28cfd-154">Домашняя страница расширяемости</span><span class="sxs-lookup"><span data-stu-id="28cfd-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
