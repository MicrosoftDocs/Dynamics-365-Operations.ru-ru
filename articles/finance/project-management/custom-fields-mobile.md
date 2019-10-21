---
title: Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet на iOS и Android
description: В этом разделе приводятся общие шаблоны для использования расширений для реализации настраиваемых полей.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175007"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet на iOS и Android

[!include [banner](../includes/banner.md)]

В этом разделе приводятся общие шаблоны для использования расширений для реализации настраиваемых полей. Рассматриваются следующие темы:

- Различные типы данных, поддерживаемые платформой настраиваемых полей
- Порядок отображения доступных только для чтения или редактируемых полей в записях табеля учета рабочего времени, а также сохранения предоставленных пользователем значений обратно в базу данных
- Порядок отображения полей только для чтения в заголовке табеля учета рабочего времени
- Порядок интеграции другой пользовательской бизнес-логики для ввода значений по умолчанию в поля и выполнения дополнительной проверки

## <a name="audience"></a>Аудитория

Этот раздел предназначен для разработчиков, которые интегрируют свои настраиваемые поля в мобильное приложение Microsoft Dynamics 365 Project Timesheet, доступное для Apple iOS и Google Android. Предполагается, что читатели знакомы с разработкой на языке X++ и функциональностью табеля учета рабочего времени проекта.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Контракт данных — класс TSTimesheetCustomField X++

Класс **TSTimesheetCustomField** — это класс контракта данных X++, который представляет информацию о настраиваемом поле для функциональности табеля учета рабочего времени. Списки объектов настраиваемых полей передаются как в контракте данных TSTimesheetDetails, так и в контракте данных TSTimesheetEntry для отображения пользовательских полей в мобильном приложении.

- **TSTimesheetDetails** — контракт заголовка табеля учета рабочего времени.
- **TSTimesheetEntry** — контракт проводки табеля учета рабочего времени. Группы этих объектов с одинаковыми данными проекта и значением **timesheetLineRecId** составляют строку.

### <a name="fieldbasetype-types"></a>fieldBaseType (Типы)

Свойство **FieldBaseType** объекта **TsTimesheetCustom** определяет тип поля, которое отображается в приложении. Поддерживаются следующие типы значений **Types**.

| Значение типов | Вид              | Основание |
|-------------|-------------------|-------|
| 0           | String (и Enum) | Поле отображается как текстовое поле. |
| 1           | Целочисленный           | Значение отображается как число без десятичных знаков. |
| 2           | Действующий              | Значение отображается как число, имеющее десятичные знаки.<p>Чтобы показать реальное значение как валюту в приложении, используйте свойство **fieldExtenededType**. Для задания числа отображаемых десятичных знаков можно использовать свойство **numberOfDecimals**.</p> |
| 3           | Дата              | Форматы дат определяются параметром пользователя **Формат даты, времени и чисел**, указанным в параметрах **Настройки языка и страны/региона** в разделе **Параметры пользователя**. |
| 4           | Логический           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Если свойство **stringOptions** не предусмотрено у объекта **TSTimesheetCustomField**, пользователю предоставляется текстовое поле свободного формата.

    Свойство **stringLength** может использоваться для установки максимальной длины строки, которую пользователи могут вводить.

- Если свойство **stringOptions** предоставляется в объекте **TSTimesheetCustomField**, эти элементы списка являются единственными значениями, которые пользователи могут выбрать с помощью кнопок параметров (переключателей).

    В этом случае строковое поле может действовать как значение перечисления для целей ввода пользователем. Чтобы сохранить значение в базе данных в качестве перечисления, вручную сопоставьте строковому значению значение перечисления перед сохранением в базе данных, используя цепочку команд (см. раздел "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе, например).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Это свойство можно использовать для форматирования вещественных значений как валюты. Этот подход применяется только в том случае, если параметр **fieldBaseType** имеет значение **Real**.

- **TSCustomFieldExtendedType:None** — форматирование не применяется.
- **TSCustomFieldExtendedType::Currency** — форматирование значения как валюты.

    Когда форматирование валюты активно, поле **stringValue** может использоваться для передачи кода валюты, который должен отображаться в приложении. Значение является значением только для чтения.

    Поле **realValue** содержит сумму денег, которая должна быть сохранена в базе данных.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Это свойство можно использовать, чтобы указать, где в приложении должно отображаться настраиваемое поле.

- **TSCustomFieldSection::Header** — поле появится в разделе **Подробнее** приложения. Эти поля всегда предназначены только для чтения.
- **TSCustomFieldSection::Line** — поле будет отображаться после всех готовых полей строки в записях табеля учета рабочего времени. Эти поля могут быть как редактируемыми, так и только для чтения.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть редактируемым пользователями. Установите для свойства значение **Нет**, чтобы поле было доступно только для чтения.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть обязательным.

### <a name="label-str"></a>label (str)

Это свойство определяет метку, которая отображается рядом с полем в приложении.

### <a name="stringoptions-list-of-strings"></a>stringOptions (список строк)

Это свойство применяется только тогда, когда для параметра **fieldBaseType** задано значение **String**. Если задано значение **stringOptions**, строковые значения, доступные для выбора с помощью кнопок параметров (переключателей), определяются строками в списке. Если строки не указаны, запись свободного текста в поле строки разрешена (пример см. в пункте "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе).

### <a name="stringlength-int"></a>stringLength (int)

Это свойство определяет максимальную длину строкового поля. Оно применяется только тогда, когда для параметра **fieldBaseType** задано значение **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Это свойство определяет число десятичных разрядов, отображаемых в вещественных полях. Оно применяется только тогда, когда для параметра **fieldBaseType** задано значение **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Это свойство управляет порядком отображения настраиваемых полей в приложении, когда указано более одного настраиваемого поля. Поля, имеющие меньшие номера, отображаются первыми.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Для полей типа **Boolean** это свойство передает логическое значение поля между сервером и приложением.

### <a name="guidvalue-guid"></a>guidValue (guid)

Для полей типа **GUID** это свойство передает значение глобально уникального идентификатора (GUID) поля между сервером и приложением.

### <a name="int64value-int64"></a>int64Value (int64)

Для полей типа **Int64** это свойство передает значение Int64 поля между сервером и приложением.

### <a name="intvalue-int"></a>intValue (int)

Для полей типа **Int** это свойство передает целое значение поля между сервером и приложением.

### <a name="realvalue-real"></a>realValue (real)

Для полей типа **Real** это свойство передает вещественное значение поля между сервером и приложением.

### <a name="stringvalue-str"></a>stringValue (str)

Для полей типа **String** это свойство передает строковое значение поля между сервером и приложением. Оно также используется для полей типа **Real**, отформатированных как валюта. Для этих полей свойство используется для передачи кода валюты в приложение.

### <a name="datevalue-date"></a>dateValue (date)

Для полей типа **Date** это свойство передает значение даты поля между сервером и приложением.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Отображение и сохранение настраиваемого поля в разделе записи табеля учета рабочего времени

Далее представлен снимок экрана мобильного приложения для создания записи табеля учета рабочего времени. На нем отображаются готовые поля и настраиваемое поле в разделе "Запись времени", называемое "Тестовая строка" с уже установленным значением перечислимого типа "Второй параметр".

![Настраиваемое поле тестовой строки в приложении](media/timesheet-entry.jpg)



Ниже представлен снимок экрана мобильного приложения, на котором пользователь выбирает один из вариантов перечисления, доступных для настраиваемого поля "Тестовая строка".  Двумя вариантами являются "Первый параметр" и "Второй параметр", которые отображаются в виде переключателей. В данный момент выбран второй вариант.

![Кнопки параметров (переключатели) для настраиваемого поля "Тестовая строка"](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Расширение таблицы TSTimesheetLine таким образом, чтобы она содержала настраиваемое поле

В обычных сценариях существует вероятность того, что данные для настраиваемого поля в разделе записи табеля учета рабочего времени будут сохранены в таблице TSTimesheetLine. Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTrans, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).

Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных. Они могут создаваться динамически в соответствии с логикой X++. Этот подход может быть полезен в сценариях только для чтения (пример динамически создаваемых значений настраиваемого поля см. в разделе "Использование цепочки команд класса TSTimesheetDetails, метод buildCustomFieldListForHeader для заполнения подробных сведений табеля учета рабочего времени").

Далее представлен снимок экрана репозитария прикладных объектов из Visual Studio. Он показывает расширение таблицы TSTimesheetLine с полем TestLineString, добавленным в качестве настраиваемого поля.

![Строка строки](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе записи табеля учета рабочего времени

Этот код управляет параметрами отображения для поля в приложении. Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.

В следующем примере показано строковое поле для записей времени. В этом поле имеются два параметра, **Первый вариант** и **Второй вариант**, которые доступны через кнопки параметров(переключатели). Поле в приложении связано с полем **TestLineString**, которое добавляется в таблицу TSTimesheetLine.

Обратите внимание на использование метода **TSTimesheetCustomField::newFromMetatdata()**, чтобы упростить инициализацию свойств настраиваемого поля: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** и **numberOfDecimals**. При желании эти параметры также можно настроить вручную.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Использование цепочки команд метода buildCustomFieldListForEntry класса TSTimesheetEntry для ввода значений в запись табеля учета рабочего времени

Метод **buildCustomFieldListForEntry** используется для ввода значений в сохраненных строках табеля учета рабочего времени в мобильном приложении. Он принимает в качестве параметра запись TSTimesheetTrans. Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Используйте цепочку команд класса TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных

Чтобы сохранить настраиваемое поле обратно в базу данных в обычном режиме использования, необходимо расширить несколько методов:

- Метод **timesheetLineNeedsUpdating** используется для определения того, была ли запись строки изменена пользователем в приложении и должна ли она быть сохранена в базе данных. Если производительность не критична, этот метод может быть упрощен, чтобы он всегда возвращал значение **true**.
- Методы **populateTimesheetLineFromEntryDuringCreate** и **populateTimesheetLineFromEntryDuringUpdate** могут быть расширены таким образом, чтобы они могли вводить значения в запись базы данных TSTimesheetLine из представленной записи контракта данных TSTimesheetEntry. В приведенном ниже примере обратите внимание на то, как сопоставление между полем базы данных и полем ввода выполняется вручную с помощью кода X++.
- Метод **populateTimesheetWeekFromEntry** также может быть расширен, если настраиваемое поле, сопоставленное с объектом **TSTimesheetEntry**, должно быть записано обратно в таблицу базы данных TSTimesheetLineweek.

> [!NOTE]
> В следующем примере сохраняется значение **firstOption** или **secondOption**, которое пользователь выбирает, в базу данных в качестве необработанного строкового значения. Если поле базы данных является полем типа **Enum**, эти значения можно вручную сопоставить значению перечисления, а затем сохранить в поле перечисления таблицы базы данных.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Отображение настраиваемого поля в разделе заголовка табеля учета рабочего времени

Далее представлен снимок экрана мобильного приложения при просмотре табеля учета рабочего времени пользователем. Кнопка "Дополнительно" была выбрана в верхнем правом углу для отображения параметра "Подробнее".  

![Команда "Подробнее"](media/show-more.png)



Далее представлен снимок экрана мобильного приложения, в котором отображается раздел "Дополнительно" табеля учета рабочего времени. В раздел заголовка табеля учета рабочего времени добавлено настраиваемое поле, называемое "Коэффициент использования этого табеля учета рабочего времени (вычисляемое настраиваемое поле)" Для настраиваемого поля задается значение "0,667", доступное только для чтения.

![Раздел "Дополнительно"](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Расширение таблицы TSTimesheetTable таким образом, чтобы она содержала настраиваемое поле

В обычных сценариях вероятно, что данные для настраиваемого поля в разделе заголовка будут извлекаться из таблицы TSTimesheetHeader. Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTable, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).

Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных. Они могут создаваться динамически в соответствии с логикой X++. В следующем примере показан такой подход.

Поля в разделе заголовка в приложении всегда доступны только для чтения.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе заголовка

Этот код управляет параметрами отображения для поля в приложении. Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.

В следующем примере показано вычисленное значение в разделе заголовка в приложении.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для заполнения сведений табеля учета рабочего времени

Метод **buildCustomFieldListForHeader** используется для ввода сведений заголовка табеля учета рабочего времени в мобильном приложении. Он принимает в качестве параметра запись TSTimesheetTable. Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении. В следующем примере не считываются никакие значения из базы данных. Вместо этого используется логика X++ для создания вычисляемого значения, которое затем отображается в приложении.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Другие возможности настройки/расширяемости

### <a name="adding-additional-validation-for-the-app"></a>Добавление дополнительной проверки для приложения

Существующая логика для функций табеля учета рабочего времени на уровне базы данных будет продолжать работать, как ожидается. Чтобы прервать выполнение операции сохранения или отправки и показать определенное сообщение об ошибке, можно добавить **throw error("сообщение пользователю")** в код, используя цепочку расширения команд. Ниже приведены три примера полезных расширяемых методов:

- Если **validateWrite** в таблице TSTimesheetLine возвращает значение **false** во время операции сохранения для строки табеля учета рабочего времени, в мобильном приложении отображается сообщение об ошибке.
- Если **validateSubmit** в таблице TSTimesheetTable возвращает значение **false** во время операции отправки табеля учета рабочего времени, в приложении, пользователю отображается сообщение об ошибке.
- Логика, которая заполняет поля (например, **Свойство строки**), когда метод **insert** в таблице TSTimesheetLine будет по-прежнему выполняться.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Скрытие и отметка готовых полей как доступных только для чтения через конфигурацию

Из параметров проекта можно сделать так, чтобы готовые поля были доступны только для чтения или были скрыты в мобильном приложении. Задайте параметры в разделе **Мобильные табели учета рабочего времени** на вкладке **Табель учета рабочего времени** на странице **Параметры модуля "Управление и учет по проектам"**.

![Параметры проекта](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Изменение доступных для выбора действий с помощью расширений

Действия, доступные для выбора для проекта, заполняются с помощью методов **getActivitiesForProject()** и **getActivityQuery()** в классе **TsTimesheetProjectService**. Можно использовать цепочку команд для изменения этого поведения в соответствии с бизнес-ситуацией для мероприятий, доступных для выбора для конкретного проекта.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Ввод категории проекта по умолчанию в записи табеля учета рабочего времени

Ввод категории проекта по умолчанию в записи табеля учета рабочего времени происходит на трех уровнях. Можно использовать цепочку команд для расширения поведения на любом из этих уровней или на всех уровнях, чтобы добиться желаемого поведения. Используется следующая иерархия:

1. Приложение пытается поместить категорию по умолчанию из ресурса проекта. Эта категория по умолчанию задается в методах **getCurrentUserResource** и **getDelegatedResourcesForCurrentUser** в классе **TSTimesheetSettingsService**.
2. Если категория по умолчанию не указана на уровне ресурсов проекта, приложение пытается извлечь ее из проектной деятельности. Эта категория по умолчанию задается в методе **getActivitiesForProject** в классе **TSTimesheetProjectService**.
3. Если категория по умолчанию не указана на уровне действий проекта, категория по умолчанию берется из параметров проекта. Эта категория по умолчанию задается в методе **getProjectDetailsbyRule** в классе **TSTimesheetProjectService**.
