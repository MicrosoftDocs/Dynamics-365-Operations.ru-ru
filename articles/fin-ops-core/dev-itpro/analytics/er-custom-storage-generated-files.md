---
title: Определение расположений пользовательского хранилища для создаваемых документов
description: В этом разделе объясняется, как расширить список местоположения хранения для документов, которые формируются форматами электронной отчетности (ER).
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 337e760f28161721d886c7bbec09b5ff8dbfad45
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594917"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Определение расположений пользовательского хранилища для создаваемых документов

[!include[banner](../includes/banner.md)]

Интерфейс прикладного программирования (API) платформы электронной отчетности (ER) позволяет расширять список местоположения хранения для документов, формируемых форматами ER. В этой теме объясняется, как добавить пользовательское место хранения для созданных документов путем делегирования задачи создания мест назначения электронной отчетности в фабрику мест назначения по умолчанию и последующей реализации пользовательского класса, имеющего свою собственную логику места назначения.

## <a name="prerequisites"></a>Необходимые условия

Разверните топологию, которая поддерживает непрерывную сборку. Дополнительные сведения см. в разделе [Развертывание топологий, которые поддерживают непрерывное построение и автоматизацию тестирования](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Необходим доступ к этой топологии для одной из следующих ролей:

- Разработчик электронной отчетности
- Консультант по функциональным возможностям электронной отчетности
- Системный администратор

Кроме того, необходим доступ к среде разработки для этой топологии.

Все задачи в этой теме могут быть выполнены в компании **USMF**.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Импорт формата электронной отчетности для движения основных средств

Чтобы создать документы, для которых планируется добавить пользовательское место хранения, [импортируйте](er-download-configurations-global-repo.md) конфигурацию формата электронной отчетности **Движение основных средств** в текущую топологию.

![Страница репозитория конфигурации.](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Выполнение отчета о движении основных средств

1. Перейдите в раздел **Основные средства** \> **Запросы и отчеты** \> **Отчеты о проводках** \> **Движение основных средств**.
2. В поле **Дата начала** введите **01.01.2017** (1 января 2017).
3. В поле **Дата окончания** введите **31.01.2017** (31 января 2017).
4. В поле **Валюта** выберите **Валюта учета**.
5. В поле **Сопоставление формата** выберите **Движение основных средств**.
6. Нажмите **ОК**.

![Диалоговое окно времени выполнения для отчета о движении основных средств.](./media/er-custom-storage-generated-files-runtime-dialog.png)

В Microsoft Excel просмотрите исходящий документ, который создан и доступен для загрузки. Такое поведение является [поведением по умолчанию](electronic-reporting-destinations.md#default-behavior) для формата электронной отчетности, для которого не настроены [места назначения](electronic-reporting-destinations.md), и который выполняется в интерактивном режиме.

## <a name="review-the-source-code"></a>Проверка исходного кода

Просмотрите код метода `generateReportByGER()` класса `AssetRollForwardService`. Обратите внимание, что метод `Run()` используется для вызова платформы электронной отчетности и создания отчета **Движение основных средств**.

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

## <a name="modify-the-source-code"></a>Изменение исходного кода

1. В вашем проекте Visual Studio добавьте новый класс (`AssetRollForwardDestination` в данном примере) и напишите код для реализации вашего настраиваемого места назначения для создаваемых отчетов **Движение основных средств**.

    - Метод `new()` предназначен для того, чтобы получить исходный объект места назначения электронной отчетности и управляемый логикой приложения параметр, определяющий пользовательское местоположение, в котором должны сохраняться сформированные отчеты. В этом примере пользовательское местоположение представляет собой имя папки локальной файловой системы сервера, на котором запущена служба Application Object Server (AOS).
    - Метод `saveFile()` предназначен для сохранения созданного документа в папке локальной файловой системы сервера, на котором запущена служба AOS.

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

2. В вашем проекте Visual Studio добавьте новый класс (`AssetRollForwardDestinationFactory` в данном примере) и создайте код для настройки пользовательской фабрики назначения, которая делегирует создание места назначения конечной фабрике, используемой по умолчанию, а также для создания оболочки файла назначения с собственным местом назначения.

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

3. Измените существующий класс `AssetRollForwardService` и напишите код для настройки пользовательской фабрики назначения для средства выполнения отчетов. Обратите внимание, что при создании пользовательской фабрики назначения параметр, управляемый приложением, который определяет целевую папку, передается. Таким образом, эта целевая папка используется для хранения созданных файлов.

    > [!NOTE] 
    > Убедитесь, что указанная папка (**c:\\0** в данном примере) присутствует в локальной файловой системе сервера, на котором запущена служба AOS. В противном случае во время выполнения будет создано исключение [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception).

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

4. Заново выполните сборку проекта

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Повторное выполнение отчета о движении основных средств

1. Перейдите в раздел **Основные средства** \> **Запросы и отчеты** \> **Отчеты о проводках** \> **Движение основных средств**.
2. В поле **Дата начала** введите значение **01.01.2017**.
3. В поле **Дата окончания** введите значение **31.01.2017**.
4. В поле **Валюта** выберите **Валюта учета**.
5. В поле **Сопоставление формата** выберите **Движение основных средств**.
6. Нажмите **ОК**.
7. Выполните поиск в локальной папке **C:\\0**, чтобы найти созданный файл.

> [!NOTE]
> Так как объект `originDestination` не используется в объекте `AssetRollForwardDestination` в этом примере, конфигурации для [мест назначения](electronic-reporting-destinations.md) в формате электронной отчетности не будут учитываться во время выполнения.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Места назначения электронной отчетности (ER)](electronic-reporting-destinations.md)
- [Домашняя страница расширяемости](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]