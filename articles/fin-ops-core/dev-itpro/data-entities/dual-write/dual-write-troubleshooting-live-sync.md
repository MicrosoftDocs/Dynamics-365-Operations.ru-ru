---
title: Устранение проблем с синхронизацией в режиме реального времени
description: В этом разделе содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 69667f8b64c048f5957168d1af21a6c858bc0bad
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782587"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Устранение проблем с синхронизацией в режиме реального времени

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Microsoft Dataverse. А именно, в нем содержатся сведения об устранении неполадок при синхронизации в режиме реального времени.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Azure Active Directory (Azure AD). В каждом разделе объясняется, требуются ли конкретные роль или учетные данные.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>При создании строки в синхронизации в режиме реального времени отображается сообщение об ошибке

При создании строки в приложении Finance and Operations может появиться следующее сообщение об ошибке:

*\[{\\"ошибка\\":{\\"код\\":\\"0x80072560\\",\\"сообщение\\":\\"Пользователь не является членом организации.\\"}}\], Удаленный сервер вернул ошибку: (403) Запрещено."}}".*

Чтобы устранить проблему, выполните шаги, указанные в разделе [Системные требования и предварительные условия](requirements-and-prerequisites.md). Для выполнения этих шагов пользователи с двойной записью, созданные в Dataverse, должен иметь роль администратора системы. Группа-владелец по умолчанию должна также иметь роль администратора системы.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>При попытке сохранить данные таблицы в синхронизации в режиме реального времени будет выведено сообщение об ошибке

**Роль, требуемая для исправления ошибки:** системный администратор

При попытке сохранить данные таблицы в приложении Finance and Operations может появиться следующее сообщение об ошибке:

*Не удается сохранить изменения в базе данных. Единица работы не может зафиксировать проводку. Невозможно записать данные в единицы измерения объекта. Операции записи в UnitOfMeasureEntity заканчиваются сбоем с сообщением об ошибке "Не удается синхронизировать с единицами измерения объекта".*

Чтобы устранить проблему, необходимо убедиться, что необходимые ссылочные данные существуют как в приложении Finance and Operations ,так и в Dataverse. Например, если запись клиента принадлежит определенной группе клиентов, убедитесь, что эта запись группы клиентов существует в Dataverse.

Если данные существуют в обоих местах, и вы убедились, что проблема не связана с данными, выполните следующие действия.

1. Откройте объект **DualWriteProjectConfigurationEntity** с помощью надстройки Excel. Чтобы использовать надстройку, включите режим конструктора в надстройке Finance and Operations Excel и добавьте **DualWriteProjectConfigurationEntity** на лист. Дополнительные сведения см. в разделе [Просмотр и обновление данных сущностей с помощью Excel](../../office-integration/use-excel-add-in.md).
2. Выбор и удаление записей, имеющих проблемы в сопоставлении и проекте с двойной записью. Имеется две записи для каждого сопоставления с двойной записью.
3. Опубликуйте изменения, используя надстройку Excel. Этот шаг важен, поскольку он удаляет записи из объекта и соответствующих таблиц.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Обработка ошибок привилегии чтения или записи при создании данных в приложении Finance and Operations

При создании данных в приложении Finance and Operations может появиться сообщение об ошибке "Ошибочный запрос".

![Пример сообщения об ошибке "Ошибочный запрос".](media/error_record_id_source.png)

Чтобы решить эту проблему, необходимо включить отсутствующую привилегию, назначив правильную роль безопасности для рабочей группы сопоставленного подразделения Dynamics 365 Sales или Dynamics 365 Customer Service.

1. В приложении Finance and Operations найдите подразделение, сопоставленное в наборе подключений интеграции данных.

    ![Сопоставление организации.](media/mapped_business_unit.png)

2. Выполните вход в среду в приложении для взаимодействия с клиентами, перейдите к пункту **Параметры \> Безопасность** и найдите рабочую группу сопоставленного подразделения.

    ![Рабочая группа сопоставленного подразделения.](media/setting_security_page.png)

3. Откройте страницу рабочей группы для редактирования, а затем выберите **Управление ролями**.

    ![Кнопка "Управление ролями".](media/manage_team_roles.png)

4. В диалоговом окне **Управление ролями рабочей группы** назначьте роль с правами доступа на чтение/доступ для соответствующих таблиц, а затем нажмите кнопку **ОК**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Устранение проблем синхронизации в среде с недавно измененной средой Dataverse

**Роль, требуемая для исправления ошибки:** системный администратор

При создании данных в приложении Finance and Operations может появиться следующее сообщение об ошибке:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Не удается создать полезную нагрузку для объекта CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Сбой создания полезной нагрузки с ошибкой Недопустимый URI: URI пуст."}\],"isErrorCountUpdated":true}*

Ниже приведено сообщение об ошибке в приложении для взаимодействия с клиентами:

> Возникла непредвиденная ошибка в коде независимого разработчика. (ErrorType = ClientError) Непредвиденное исключение от подключаемого модуля (Выполнить): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: не удалось обработать учетную запись объекта — (Сбой попытки подключения, так как подключенная стороне не предоставляет правильный ответ в течение некоторого периода времени, или сбой установленного подключения из-за отсутствия ответа от узла.

Эта ошибка возникает в том случае, когда среда Dataverse ошибочно сбрасывается при попытке создать данные в приложении Finance and Operations.

> [!IMPORTANT]
> Если среда была повторно связана, необходимо остановить все сопоставления объектов перед выполнением действий по устранению рисков.

Чтобы решить эту проблему, необходимо выполнить шаги как в приложении Dataverse, так и в Finance and Operations.

1. В приложении Finance and Operations выполните следующие действия:

    1. Откройте объект **DualWriteProjectConfigurationEntity** с помощью надстройки Excel. Чтобы использовать надстройку, включите режим конструктора в надстройке Finance and Operations Excel и добавьте **DualWriteProjectConfigurationEntity** на лист. Дополнительные сведения см. в разделе [Просмотр и обновление данных сущностей с помощью Excel](../../office-integration/use-excel-add-in.md).
    2. Выбор и удаление записей, имеющих проблемы в сопоставлении и проекте с двойной записью. Имеется две записи для каждого сопоставления с двойной записью.
    3. Опубликуйте изменения, используя надстройку Excel. Этот шаг важен, поскольку он удаляет записи из объекта и соответствующих таблиц.
    4. Чтобы предотвратить возникновение ошибок при повторной связи между средами Finance and Operations или Dataverse убедитесь, что не осталось конфигураций двойной записи.

2. В Dataverse выполните следующие действия:

    1. Выполните вход в среду Dataverse (например, `https://*****.crm.dynamics.com/`).
    2. Перейдите в **Дополнительные параметры** \> **Расширенный поиск**.
    3. Выбор **Конфигурация среды выполнения двойной записи**.
    4. Выберите столбец для просмотра.
    5. Выберите **Результаты**, чтобы посмотреть конфигурации.
    6. Удалите все экземпляры.

3. В приложении Finance and Operations выполните следующие действия:

    1. Откройте объект **DualWriteProjectConfigurationEntity** с помощью надстройки Excel. Чтобы использовать надстройку, включите режим конструктора в надстройке Finance and Operations Excel и добавьте **DualWriteProjectConfigurationEntity** на лист. Дополнительные сведения см. в разделе [Просмотр и обновление данных сущностей с помощью Excel](../../office-integration/use-excel-add-in.md).
    2. Выбор и удаление записей, имеющих проблемы в сопоставлении и проекте с двойной записью. Имеется две записи для каждого сопоставления с двойной записью.
    3. Опубликуйте изменения, используя надстройку Excel. Этот шаг важен, поскольку он удаляет записи из объекта и соответствующих таблиц.
    4. Чтобы предотвратить возникновение ошибок при повторной связи между средами Finance and Operations или Dataverse убедитесь, что не осталось конфигураций двойной записи.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Ошибка синхронизации в режиме реального времени после полного копирования базы данных

После выполнения полного копирования базы данных из одной системы в другую и последующей попытки выполнения операции с базой данных может появиться следующее сообщение об ошибке:

*Организация SecureConfig (???) не совпадает с реальной организацией CRM (???).*

Сообщение об ошибке выводится из подключаемого модуля среды выполнения двойной записи, чтобы гарантировать, что конфигурация двойной записи, настроенная в одной системе, не может использоваться в другой системе.

Чтобы решить эту проблему, удалите все записи в таблице **msdyn_dualwriteruntimeconfig** после восстановления базы данных. Дополнительные сведения см. в разделе " [Удаление связи и повторная связь сред с двойной записью](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Ошибки синхронизации в режиме реального времени, вызванные неверным синтаксисом фильтра запросов на сопоставлениях двойной памяти

Даже если выражение запроса для фильтра двойной записи является синтаксически правильным, оно может работать некорректно. Выражение фильтра относится к объекту, а не к отдельному источнику данных объекта запроса. Таким образом, созданный запрос SQL не возвращает ожидаемых результатов.

Рассмотрим пример:

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Предполагается, что проекты, в которых нет родительского элемента, не будут отфильтрованы. Однако фильтр не работает, поскольку он преобразуется в запрос, похожий на следующий пример.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Фактический результат заключается в том, чтобы поле `parentProject` было оценено как `null`. Однако, `null` не совпадает с пустой строкой. Вследствие такого несоответствия фильтр запроса не возвращает допустимых результатов.

Чтобы устранить проблему, выполните следующие действия.

1. Добавьте вычисляемый столбец, который может быть добавлен в модель расширения и создается с помощью логики, преобразующей `null` в пустую строку.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Используйте фильтр для нового вычисляемого столбца вместо столбца по умолчанию.

Чтобы оценить фильтр в среде разработки, можно использовать следующий код X++ для проверки результатов. Выполните этот код в качестве автономной программы. Его можно использовать для оценки различных видов фильтров, применимых для объекта, прежде чем использовать эти фильтры для сопоставлений двойной записи. Запрос может быть выполнен в базе данных для оценки расхождений.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Данные из приложений Finance and Operations не синхронизированы с Dataverse

Во время синхронизации в режиме реального времени может возникнуть проблема, при которой синхронизируются только части данных из приложений Finance and Operations Dataverse или данные не синхронизируются.

> [!NOTE]
> Эту проблему необходимо устранить в ходе разработки.

Прежде чем начать устранение проблемы, проверьте следующие необходимые условия:

+ Убедитесь, что пользовательские изменения записаны в отдельной области транзакции.
+ Бизнес-события и платформа двойной записи не обрабатывают операции `doinsert()`, `doUpdate()` и `recordset()` или записи, помеченные как `skipBusinessEvents(true)`. Если код находится в этих функциях, двойная запись не будет запущена.
+ Для сопоставляемого источника данных необходимо зарегистрировать бизнес-события. Некоторые источники данных могут использовать внешнее соединение и могут быть помечены как доступные только для чтения в приложениях Finance and Operations. Эти источники данных не отслеживаются.
+ Изменения будут запускаться только в том случае, если изменения относятся к сопоставленным полям. Несопоставленные модификации полей не активируют двойную запись.
+ Убедитесь, что оценки фильтра обеспечивают допустимый результат.

### <a name="troubleshooting-steps"></a>Действия по устранению неполадок

1. Проверьте сопоставления полей на странице администрирования двойной записи. Если поле не сопоставляется из приложений Finance and Operations в Dataverse, оно не будет отслеживаться. Например, на следующем рисунке поле **Описание** отслеживается с Dataverse, но не из приложений Finance and Operations. Изменения в этом поле внутри приложений Finance and Operations отслеживаться не будут.

    ![Отслеживаемое поле.](media/live-sync-troubleshooting-1.png)

2. Определите, отслеживается ли источник данных в определении бизнес-событий. Например, на следующем рисунке не будут отслеживаться никакие поля из таблицы **DefaultDimensionDAVs** и соответствующих таблиц для изменений. Не отслеживаются источники данных, использующие внешнее соединение и помеченные как доступные только для чтения.

    ![Поле, которое не отслеживается.](media/live-sync-troubleshooting-2.png)

3. Определите, появятся ли сопоставленные поля таблицы в таблице **BUSINESSEVENTSDEFINITION**, как показано на следующем рисунке. Если вы не нашли поле, которое вы ищете в результатах запроса, оно не будет запущено с помощью двойной записи.

    ![Отслеживаемое поле в таблице.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Пример сценария

В приложениях Finance and Operations имеется обновление адреса для записи контакта, но изменение адреса не синхронизировано с Dataverse. Эта сценарий возникает, потому что ни одна запись в таблице **BusinessEventsDefinition** не имеет комбинации затронутой таблицы и объекта. В частности, таблица **LogisticsPostalAddress** не является прямым источником данных для объекта **smmContactpersonCDSV2Entity**. Объект **smmContactpersonCDSV2Entity** имеет **smmContactPersonV2Entity** в качестве источника данных, а **smmContactPersonV2Entity**, в свою очередь, имеет **LogisticsPostalAddressBaseEntity** в качестве источника данных. Таблица **LogisticsPostalAddress** представляет собой источник данных для **LogisticsPostalAddressBaseEntity**.

Подобная ситуация может возникнуть в некоторых нестандартных шаблонах, например в случаях, когда изменяемая в приложениях Finance and Operations таблица не связана с объектом, который ее содержит. Например, данные основного адреса рассчитываются для объекта **smmContactPersonCDSV2Entity**. Платформа двойной записи пытается определить, каким образом изменение соответствующей таблицы сопоставляется обратно объектам. Обычно этот подход является достаточным. Однако в некоторых случаях связь имеет настолько сложную структуру, что вы должны быть конкретны. Необходимо убедиться в том, что **RecID** соответствующей таблицы непосредственно доступен для данной сущности. Затем добавьте статический метод для отслеживания изменений в таблице.

В качестве примера рассмотрим метод **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. **CustCustomerV3entity** и **VendVendorV2Entity** были изменены для обработки этой ситуации.

Чтобы устранить проблему, выполните следующие действия.

1. Добавьте поле **PrimaryPostalAddressRecId** в объект **smmContactPersonV2Entity**. Сделайте его внутренним.

    ![Поле, добавленное в объект "smmContactPersonV2Entity".](media/Troubleshoot_live_sync_issue_1.png)

2. Добавьте то же поле в объект **smmContactPersonCDSV2Entity**.

    ![Поле, добавленное в объект "smmContactPersonCDSV2Entity".](media/Troubleshoot_live_sync_issue_2.png)

3. Добавьте следующий метод в класс **smmContactPersonCDSV2Entity**.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Синхронизируйте базу данных и постройте приложение.
5. Останавливает все сопоставления двойной записи, созданные для объекта **smmContactPersonCDSV2Entity**.
6. Запустите сопоставление. Должна отобразиться новая таблица (**LogisticsPostalAddress** в этом примере), которую вы начали отслеживать, используя столбец **RefTableName** для строки, в которой значение **refentityname** равно **smmContactPersonCDSV2Entity** в таблице **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Ошибка при создании записи, в которой несколько записей отправляются из приложения Finance and Operations в Dataverse в одном пакете

Для любой проводки приложение Finance and Operations создает данные в пакете и отправляет их как пакет в Dataverse. Если две записи создаются как часть одной и той же проводки и ссылаются друг на друга, может быть выведено сообщение об ошибке, напоминающее следующий пример в приложении Finance and Operations:

*Не удалось записать данные в объект aaa_fundingsources. Не удалось выполнить поиск ebecsfs_contracts с значениями {PC00...}. Не удалось выполнить поиск aaa_fundingsources с значениями {PC00...} . Запись в aaa_fundingsources завершилась сбоем с сообщением об ошибке Сообщение исключения: удаленный сервер вернул ошибку: (400) неправильный запрос.*

Чтобы устранить проблему, создайте отношения с объектом в приложении Finance and Operations, чтобы указать, что два объекта связаны друг с другом и что связанные записи обрабатываются в одной и той же проводке.

## <a name="enable-verbose-logging-of-error-messages"></a>Включение подробного протоколирования сообщений об ошибках

В приложении Finance and Operations могут возникнуть ошибки, связанные с данной средой Dataverse. Сообщение об ошибке может не содержать полного текста сообщения или других соответствующих данных. Чтобы получить дополнительные сведения, можно включить подробное протоколирование, установив флаг **IsDebugMode**, который присутствует в объекте **DualWriteProjectConfigurationEntity** во всех конфигурациях проектов в приложениях Finance and Operations.

1. Откройте объект **DualWriteProjectConfigurationEntity** с помощью надстройки Excel. Чтобы использовать надстройку, включите режим конструктора в надстройке Finance and Operations Excel и добавьте **DualWriteProjectConfigurationEntity** на лист. Дополнительные сведения см. в разделе [Просмотр и обновление данных сущностей с помощью Excel](../../office-integration/use-excel-add-in.md).
2. Установите для флага **IsDebugMode** значение **Да** для проекта.
3. Выполните сценарий.
4. Подробные журналы доступны в таблице **DualWriteErrorLog**. Для просмотра данных с помощью обозревателя таблиц используйте следующий URL-адрес: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Чтобы записать дополнительные журналы в режиме отладки, установите обновление в [KB 4595434 (исправьте, чтобы пустые значения распространялись при синхронизации двойной записи в режиме реального времени)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Ошибка при добавлении адреса для клиента или контакта

При попытке добавления адреса для клиента или контакта в приложениях Finance and Operations или Dataverse может появиться следующее сообщение об ошибке:

*Не удалось записать данные в объект msdyn_partypostaladdresses. При записи в DirPartyPostalAddressLocationCDSEntity произошла ошибка запроса сообщения об ошибке с кодом состояния BadRequest и код ошибки CDS: 0x 80040265 ответное сообщение: "Произошла ошибка в подключаемом модуле. Запись, имеющая значений атрибутов "Код местонахождения", уже существует. Ключ кода местонахождения ключа объекта требует, чтобы этот набор атрибутов содержал уникальные значения. Выберите уникальные значения и повторите попытку".*

Чтобы устранить эту проблему, установите версию пакета оркестрации двойной записи (2.2.2.60), чтобы определить ключи в таблице **адрес**, как показано в следующей таблице.

| Свойство | значение |
|---|---|
| Отображаемое имя | **Ключ местонахождения** |
| ФИО | **msdyn_locationkey** |
| Поля | **msdyn_locationid**, **parentid** |
| Состояние | **Активные сотрудники** |
| Системное задание | Пустой |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Ошибка при добавлении клиента в Dataverse

При попытке добавить клиента в Dataverse может появиться следующее сообщение об ошибке:

*"RecordError0":"Ошибка записи для объекта Customers v3 с неизвестным исключением — Запись субъекта для типа субъекта "Организация"} не найдена.*

Когда клиент создается в Dataverse, создается новый номер субъекта. Сообщение об ошибке отображается, если запись клиента вместе с субъектом синхронизирована с приложениями Finance and Operations, но уже существует запись клиента с иным номером субъекта.

Чтобы устранить эту проблему, найдите клиента через поиск по субъекту. Создать новую запись клиента, если запись клиента отсутствует. Если клиент существует, воспользуйтесь существующим субъектом, чтобы создать новую запись клиента.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Ошибка при создании нового клиента, поставщика или контакта в Dataverse

При попытке создания нового клиента, поставщика или контакта в Dataverse может появиться следующее сообщение об ошибке:

*Не удается обновить тип субъекта с "DirOrganization" на "DirPerson", вместо этого будет выполнено удаление существующего субъекта, за которым следует вставка с новым типом.*

В Dataverse таблице **msdyn_party** имеется номерная серия. Когда учетная запись создается в Dataverse, создается новый субъект (например, **Party-001** типа **Организация**). Эти данные отправляются в приложение Finance and Operations. Если среда Dataverse была сброшена или среда Finance and Operations связана с другой средой Dataverse, а затем создается новая запись контакта в Dataverse, создается новое значение субъекта, начинающееся с **Party-001**. Создается запись субъекта **Party-001** типа **Физическое лицо**. Когда эти данные синхронизированы, приложения Finance and Operations отображают предыдущее сообщение об ошибке, поскольку запись субъекта **Party-001** для типа **Организация** уже существует.

Чтобы устранить проблему, измените автоматическую номерную серию для поля **msdyn_partynumber** таблицы **msdyn_party** в Dataverse на другой автоматическую номерную серию.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Проблема с производительностью при сопоставлении клиентов или контактов

Можно повысить производительность синхронизации для клиентов и контактов, настроив метод **getEntityDataSourceToFieldMapping** (в объекте **CustCustomerV3Entity**) и метод **getEntityDataSourceToFieldMapping** (в объекте **smmContactPersonCDSV2Entity**). Эти настройки уменьшают число записей в таблице **BusinessEventsDefinition**. Это сокращение количества записей, в свою очередь, уменьшает количество вызываемых событий.

Метод **getEntityDataSourceToFieldMapping** в объекте **CustCustomerV3Entity** гарантирует, что обновление электронного адреса клиента или почтового адреса инициирует бизнес-события, поэтому обновленные данные будут отправлены в Dataverse. Если не используются все поля и информация не нужна для двойной записи, прокомментируйте соответствующие строки в методе. Каждое отслеживаемое поле и таблица, добавленные в этот метод, добавляют запись в таблицу **BusinessEventsDefinition** для комбинации отслеживаемой таблицы и отслеживаемого объекта.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Аналогичным образом, метод **getEntityDataSourceToFieldMapping** в объекте **smmContactPersonCDSV2Entity** гарантирует, что любое обновление электронного адреса контакта или почтового адреса инициирует бизнес-события, поэтому обновленные данные будут отправлены в Dataverse. В методе можно прокомментировать строки для всех неиспользуемых полей.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

После обновления методов выполните следующие действия.

1. Синхронизируйте базу данных и постройте приложение.
2. Останавливает все сопоставления двойной записи в объектах **smmContactPersonCDSV2Entity** и **CustCustomerV3Entity**.
3. Запустите сопоставления. В объектах **smmContactPersonCDSV2Entity** и **CustCustomerV3Entity**, а также в таблице **BusinessEventsDefinition** можно увидеть меньше записей, и производительность может быть повышена.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
