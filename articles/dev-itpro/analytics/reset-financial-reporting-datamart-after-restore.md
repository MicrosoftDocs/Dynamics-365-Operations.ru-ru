---
title: "Сброс киоска данных финансовой отчетности"
description: "В этом разделе описывается сброс киоска данных финансовой отчетности."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: ru-ru
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Сброс киоска данных финансовой отчетности

[!include[banner](../includes/banner.md)]

В этом разделе объясняется, как сбросить киоск данных финансовой отчетности для следующих версий:

- Microsoft Dynamics 365 for Finance and Operations Financial reporting, выпуск 7.2.6.0 и новее
- Microsoft Dynamics 365 for Finance and Operations Financial reporting, выпуск 7.0.10000.4 и новее
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (локальная версия)

Чтобы получить Finance and Operations Financial reporting выпуска 7.2.6.0 можно загрузить KB 4052514 по адресу <https://support.microsoft.com/en-us/help/4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Сброс киоска данных финансовой отчетности для Finance and Operations Financial reporting выпуска 7.2.6.0 и новее

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Сброс киоска данных финансовой отчетности из конструктора отчетов

> [!NOTE]
> Шаги в этом процессе поддерживаются для Finance and Operations Financial reporting выпуска 7.2.6.0 и новее. В случае более раннего выпуска обратитесь за помощью в службу поддержки.

В определенных случаях может возникнуть необходимость сбросить киоск данных для финансовой отчетности. Можно выполнить эту задачу в клиенте конструктора отчетов. Ниже приводятся некоторые сценарии, в которых может потребоваться сброс киоск данных:

- База данных Finance and Operations была восстановлена, но база данных киоска данных не была восстановлена.
- Вы видите неверные данные за период.
- Службы поддержки дала инструкции сбросить киоск данных в процессе устранения неполадок.

Сброс киоска данных должен выполняться только в течение времени, когда нагрузка на базу данных низкая. Финансовая отчетность будут недоступна в процессе сброса.

#### <a name="reset-the-data-mart"></a>Сброс киоска данных

Чтобы сбросить киоск данных, в конструкторе отчетов в меню **Сервис** выберите пункт **Сброс киоска данных**. Диалоговое окно, которое появляется, состоит из двух разделов: **Статистика** и **Сброс**.

[![Диалоговое окно сброса киоска данных](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>Попытки интеграции

Сетка **Попытки интеграции** показывает, сколько раз система пыталась интегрировать проводки. Система продолжает попытки интеграции данных в течение некоторого количества дней, если первые несколько попыток были неудачными. Вы будете знать, что необходимо произвести сброс киоска данных, если число попыток равно 8 или более, и если имеется много записей комбинации аналитик или проводок. В этом случае данные не включаются в отчетность.

##### <a name="data-status"></a>Статус данных

Сетка **Статус данных** содержит моментальный снимок проводок, валютных курсов и значений аналитик в киоске данных. Большое количество устаревших записей указывает, что было выполнено множество обновлений записей. Это может привести к замедлению создания отчета.

##### <a name="misaligned-main-account-categories"></a>Несопоставленные категории счетов ГК

При использовании более раннего выпуска, чем Microsoft Dynamics 365 for Finance and Operations Financial reporting выпуска 7.2.1, может потребоваться сбросить киоск данных, если вы переименовали счета и перемещали счета между категориями счетов. Эти действия могут вызвать нарушение согласования категорий счетов ГК. Поле **Несопоставленные категории счетов ГК** показывает, имеется ли такая проблема.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Сброс киоска данных в Finance and Operations Financial reporting выпуска 7.2.6.0

Для сброса киоска данных в Finance and Operations Financial reporting выпуска 7.2.6.0 и ранее в диалоговом окне **Сброс киоска данных** установите флажок **Сброс киоска данных**, затем выберите **OK**. Сброс киоска данных можно выполнять только во время запланированного перерыва.

[![Флажок сброса киоска данных](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Сброс киоска данных и выбор причину в Microsoft Dynamics 365 for Finance and Operations Financial reporting выпуска 7.3.0

Если выясняется, что требуется сброс киоска данных, установите флажок **Сброс киоска данных**, затем выберите причину в поле **Причина**. Имеются следующие варианты:

- **Отсутствующие или неправильные данные** — на основе статистики было определено, что данные могут отсутствовать. Прежде чем продолжить, рекомендуется провести работу со службой поддержки для определения основной причины.
- **Восстановить базу данных** — база данных Finance and Operations была восстановлена, но база данных для киоска данных финансовой отчетности не была восстановлена.
- **Прочее** — сброс киоска данных по другим причинам. Если вы считаете, что имеется проблема, обратитесь в службу поддержки для ее выявления.

> [!NOTE]
> Убедитесь, что интеграция всех существующих задач завершена, прежде чем выполнять эти действия. Состояние интеграции можно посмотреть, выбрав **Сервис** &gt; **Статус интеграции**.

#### <a name="clear-users-and-companies"></a>Очистить пользователей и компании

Установите флажок **Очистить пользователей и компании**, если вы восстановили базу данных, но затем внесли изменения в пользователей или компании. Устанавливать этот флажок требуется редко.

Когда вы будете готовы запустить процесс сброса, выберите **OK**. Будет предложено подтвердить, что вы готовы начать процесс. Обратите внимание, что Financial reporting не будут доступна во время сброса и начальной интеграции данных, которая выполняется впоследствии.

Если требуется просмотреть состояние интеграции, выберите **Сервис** &gt; **Статус интеграции** для просмотра времени выполнения последней интеграции и ее статуса.

[![Просмотр статуса интеграции](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Сброс киоска данных финансовой отчетности для Finance and Operations Financial reporting выпуска 7.0.10000.4 и новее

Если вам когда-либо придется восстанавливать свою базу данных Finance and Operations из резервной копии или копировать базу данных из другой среды, необходимо выполнить действия, описанные в этой разделе, чтобы помочь гарантировать правильное использование киоском данных финансовой отчетности Financial reporting восстановленной базы данных Finance and Operations.

> [!NOTE]
> Шаги в этом процессе поддерживаются для приложения Microsoft Dynamics AX версии 7.0.1 (май 2016) (сборка приложения 7.0.1265.23014 и сборка Financial reporting 7.0.10000.4) и позднее. Если у вас более ранняя версия Finance and Operations, обратитесь в службу поддержки за помощью.

### <a name="export-report-definitions"></a>Экспорт определений отчетов

Во-первых, выполните следующие действия для экспорта моделей отчетов из конструктора отчетов.

1. В конструкторе отчетов выберите **Компания** &gt; **Группы строительных блоков**.
2. Выберите группу строительных блоков, которую требуется экспортировать, затем выберите **Экспорт**.

    > [!NOTE]
    > Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.

3. Выберите определения отчета для экспорта:

    - Чтобы экспортировать все определения отчетов и связанные с ними шаблоны, выберите **Выбрать все**.
    - Чтобы экспортировать определенные отчеты, строки, столбцы, деревья или наборы аналитик, выберите соответствующую вкладку и выберите элементы для экспорта. Нажмите и удерживайте клавишу CTRL, чтобы выбрать несколько элементов на вкладке. При выборе отчетов для экспорта выбираются соответствующие строки, столбцы, структуры и наборы аналитик.

4. Выберите **Экспорт**.
5. Введите имя файла и выберите безопасное место, где требуется сохранить экспортированные определения отчетов.
6. Выберите **Сохранить**.

Можно скопировать или отправить файл в надежное место. Таким образом файл можно импортировать в другую среду позже. Сведения об использовании учетной записи хранилища Microsoft Azure см. в разделе [Перенос данных с помощью служебной программы командной строки AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Корпорация Майкрософт не предоставляет учетную запись хранилища в составе договора на Finance and Operations. Необходимо либо приобрести учетную запись хранилища, либо использовать учетную запись хранилища из отдельной подписки Azure.

> [!WARNING]
> Помните о поведении диска D в виртуальных машинах (VM) Azure. Не хранит постоянно ваши экспортированные группы строительных блоков на диске D. Дополнительные сведения о временных дисках см. в разделе [Понимание временного диска на виртуальных машинах Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Остановка служб

Следующие службы Microsoft Windows будут иметь открытые подключения к базе данных Finance and Operations. Поэтому необходимо использовать удаленный рабочий стол Microsoft, чтобы подключить все компьютеры в среде, и затем остановить эти службы с помощью services.msc.

- Служба веб-публикаций (на всех компьютерах Application Object Servers [AOS])
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)
- Management Reporter 2012 Process Service (только на компьютерах Business intelligence [BI])

### <a name="reset"></a>Сбросить

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Загрузка последней версии пакета MinorVersionDataUpgrade.zip

Загрузите последнюю версию пакета MinorVersionDataUpgrade.zip. Сведения о том, как найти и загрузить правильную версию пакета обновления данных, см. в разделе [Загрузка последнего пакета развертывания обновления данных](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Обновление не является обязательным для загрузки пакета MinorVersionDataUpgrade.zip. Таким образом, нужно просто выполнить действия, описанные в подразделе "Загрузка последнего пакета развертывания обновления данных" этого раздела. Можно пропустить все остальные действия из этого раздела.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Выполнение сценариев для базы данных Finance and Operations

Запустите следующие сценарии для базы данных Finance and Operations (не для базы данных Financial reporting):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Эти сценарии помогает гарантировать правильность пользователей, ролей и параметров изменения отслеживания.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Выполнение команды Windows PowerShell для сброса базы данных

На компьютере с сервером AOS запустите Microsoft Windows PowerShell в качестве администратора и выполните следующие команды, чтобы сбросить интеграцию между Finance and Operations и Financial reporting.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Ниже приводится объяснение параметров в команде **Reset-DatamartIntegration**:

- Допустимые значения для параметра **-Reason**: **SERVICING**, **BADDATA** и **OTHER**.
- Параметр **-ReasonDetail** является произвольным текстом.
- Значения параметров Reason и ReasonDetail записываются в данных телеметрии/мониторинга среды.

> [!NOTE]
> После выполнения команд будет предложено ввести **Y** для подтверждения сброса базы данных.

#### <a name="restart-services"></a>Перезапуск служб

Используйте services.msc, чтобы перезапустить службы, остановленные ранее:

- Служба веб-публикаций (на всех компьютерах AOS)
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (только на компьютерах с AOS, не являющихся частными)
- Management Reporter 2012 Process Service (только на компьютерах BI)

#### <a name="import-report-definitions"></a>Импорт определений отчетов

Импортируйте макеты отчетов из конструктора отчетов, используя файл, созданный во время экспорта.

1. В конструкторе отчетов выберите **Компания** &gt; **Группы строительных блоков**.
2. Выберите группу строительных блоков, которую требуется экспортировать, затем выберите **Экспорт**.

    > [!NOTE]
    > Для Finance and Operations поддерживается только одна группа строительных блоков, **По умолчанию**.

3. Выберите строительный блок **По умолчанию**, затем выберите **Импорт**.
4. Выберите файл, содержащий экспортированные определения отчетов, затем выберите **Открыть**.
5. В диалоговом окне **Импорт** выберите определения отчетов для импорта:

    - Чтобы импортировать все определения отчетов и связанные с ними шаблоны, выберите **Выбрать все**.
    - Чтобы импортировать конкретные отчеты, строки, столбцы, деревья или наборы измерений, выберите отчеты, строки, столбцы, деревья или наборы измерений, которые необходимо импортировать, а затем нажмите кнопку Импорт.

6. Выберите **Импорт**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Сброс киоска данных финансовой отчетности Financial reporting для Finance and Operations (локальная версия)

1. Попросите всех пользователей выйти из конструктора отчетов и области финансовой отчетности в Finance and Operations.
2. Запустите следующий сценарий для базы данных финансовой отчетности (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Выполните усечение или удалите все записи из таблицы FINANCIALREPORTS в базе данных Finance and Operations (AXDB).
4. Выполните усечение или удалите все записи из таблицы FINANCIALREPORTVERSION, если эта таблица имеется в базе данных Finance and Operations. Если таблица не существует в базе данных Finance and Operations, пропустите этот шаг.
5. Запустите сценарий **ResetDatamart.sql** для базы данных финансовой отчетности. Этот сценарий отключает интеграцию киоска данных, удаляет все данные киоска данных, затем снова включает интеграцию киоска данных.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. После сброса можно вручную проверить повторную загрузку данных, выполнив следующий запрос базы данных финансовых отчетов Financial reporting.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Убедитесь, что все строки имеют значение **LastRunTime**, а параметр **StateType** имеет значение **5**. Значение **5** параметра **StateType** означает, что данные были успешно перезагружены. Значение **7** указывает на состояние сбоя. В некоторых случаях карта организационной иерархии имеет это состояние при первом запуске. Тем не менее, это состояние ошибки должно быть автоматически разрешено.

