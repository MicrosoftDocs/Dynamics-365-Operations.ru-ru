<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="ru-RU">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet на iOS и Android</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этом разделе приводятся общие шаблоны для использования расширений для реализации настраиваемых полей.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet на iOS и Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">В этом разделе приводятся общие шаблоны для использования расширений для реализации настраиваемых полей.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Рассматриваются следующие темы:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Различные типы данных, поддерживаемые платформой настраиваемых полей</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Порядок отображения доступных только для чтения или редактируемых полей в записях табеля учета рабочего времени, а также сохранения предоставленных пользователем значений обратно в базу данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Порядок отображения полей только для чтения в заголовке табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Порядок интеграции другой пользовательской бизнес-логики для ввода значений по умолчанию в поля и выполнения дополнительной проверки</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Аудитория</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот раздел предназначен для разработчиков, которые интегрируют свои настраиваемые поля в мобильное приложение Microsoft Dynamics 365 Project Timesheet, доступное для Apple iOS и Google Android.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Предполагается, что читатели знакомы с разработкой на языке X++ и функциональностью табеля учета рабочего времени проекта.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Контракт данных — класс TSTimesheetCustomField X++</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Класс <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> — это класс контракта данных X++, который представляет информацию о настраиваемом поле для функциональности табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Списки объектов настраиваемых полей передаются как в контракте данных TSTimesheetDetails, так и в контракте данных TSTimesheetEntry для отображения пользовательских полей в мобильном приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> — контракт заголовка табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> — контракт проводки табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Группы этих объектов с одинаковыми данными проекта и значением <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> составляют строку.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="0" state="translated">fieldBaseType (Типы)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Свойство <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> объекта <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> определяет тип поля, которое отображается в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поддерживаются следующие типы значений <bpt id="p1">**</bpt>Types<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Значение типов</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Вид</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Основание</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">String (и Enum)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поле отображается как текстовое поле.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Целочисленный</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение отображается как число без десятичных знаков.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Действующий</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Значение отображается как число, имеющее десятичные знаки.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Чтобы показать реальное значение как валюту в приложении, используйте свойство <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Для задания числа отображаемых десятичных знаков можно использовать свойство <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Дата</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Форматы дат определяются параметром пользователя <bpt id="p1">**</bpt>Формат даты, времени и чисел<ept id="p1">**</ept>, указанным в параметрах <bpt id="p2">**</bpt>Настройки языка и страны/региона<ept id="p2">**</ept> в разделе <bpt id="p3">**</bpt>Параметры пользователя<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Логический</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="0" state="translated">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если свойство <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> не предусмотрено у объекта <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>, пользователю предоставляется текстовое поле свободного формата.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Свойство <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> может использоваться для установки максимальной длины строки, которую пользователи могут вводить.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если свойство <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> предоставляется в объекте <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>, эти элементы списка являются единственными значениями, которые пользователи могут выбрать с помощью кнопок параметров (переключателей).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этом случае строковое поле может действовать как значение перечисления для целей ввода пользователем.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Чтобы сохранить значение в базе данных в качестве перечисления, вручную сопоставьте строковому значению значение перечисления перед сохранением в базе данных, используя цепочку команд (см. раздел "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе, например).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство можно использовать для форматирования вещественных значений как валюты.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот подход применяется только в том случае, если параметр <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> имеет значение <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> — форматирование не применяется.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> — форматирование значения как валюты.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Когда форматирование валюты активно, поле <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> может использоваться для передачи кода валюты, который должен отображаться в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Значение является значением только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поле <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> содержит сумму денег, которая должна быть сохранена в базе данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство можно использовать, чтобы указать, где в приложении должно отображаться настраиваемое поле.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> — поле появится в разделе <bpt id="p2">**</bpt>Подробнее<ept id="p2">**</ept> приложения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Эти поля всегда предназначены только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> — поле будет отображаться после всех готовых полей строки в записях табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Эти поля могут быть как редактируемыми, так и только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Установите для этого свойства значение <bpt id="p1">**</bpt>Да<ept id="p1">**</ept>, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть редактируемым пользователями.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Установите для свойства значение <bpt id="p1">**</bpt>Нет<ept id="p1">**</ept>, чтобы поле было доступно только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Установите для этого свойства значение <bpt id="p1">**</bpt>Да<ept id="p1">**</ept>, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть обязательным.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство определяет метку, которая отображается рядом с полем в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions (список строк)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство применяется только тогда, когда для параметра <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> задано значение <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если задано значение <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>, строковые значения, доступные для выбора с помощью кнопок параметров (переключателей), определяются строками в списке.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если строки не указаны, запись свободного текста в поле строки разрешена (пример см. в пункте "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство определяет максимальную длину строкового поля.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Оно применяется только тогда, когда для параметра <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> задано значение <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="0" state="translated">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство определяет число десятичных разрядов, отображаемых в вещественных полях.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Оно применяется только тогда, когда для параметра <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> задано значение <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="0" state="translated">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Это свойство управляет порядком отображения настраиваемых полей в приложении, когда указано более одного настраиваемого поля.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поля, имеющие меньшие номера, отображаются первыми.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Для полей типа <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> это свойство передает логическое значение поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> это свойство передает значение глобально уникального идентификатора (GUID) поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> это свойство передает значение Int64 поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="0" state="translated">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> это свойство передает целое значение поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> это свойство передает вещественное значение поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="0" state="translated">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>String<ept id="p1">**</ept> это свойство передает строковое значение поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Оно также используется для полей типа <bpt id="p1">**</bpt>Real<ept id="p1">**</ept>, отформатированных как валюта.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Для этих полей свойство используется для передачи кода валюты в приложение.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Для полей типа <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> это свойство передает значение даты поля между сервером и приложением.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Отображение и сохранение настраиваемого поля в разделе записи табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Далее представлен снимок экрана мобильного приложения для создания записи табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">На нем отображаются готовые поля и настраиваемое поле в разделе "Запись времени", называемое "Тестовая строка" с уже установленным значением перечислимого типа "Второй параметр".</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Настраиваемое поле тестовой строки в приложении</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ниже представлен снимок экрана мобильного приложения, на котором пользователь выбирает один из вариантов перечисления, доступных для настраиваемого поля "Тестовая строка".</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Двумя вариантами являются "Первый параметр" и "Второй параметр", которые отображаются в виде переключателей.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В данный момент выбран второй вариант.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Кнопки параметров (переключатели) для настраиваемого поля "Тестовая строка"</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Расширение таблицы TSTimesheetLine таким образом, чтобы она содержала настраиваемое поле</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В обычных сценариях существует вероятность того, что данные для настраиваемого поля в разделе записи табеля учета рабочего времени будут сохранены в таблице TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTrans, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Они могут создаваться динамически в соответствии с логикой X++.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот подход может быть полезен в сценариях только для чтения (пример динамически создаваемых значений настраиваемого поля см. в разделе "Использование цепочки команд класса TSTimesheetDetails, метод buildCustomFieldListForHeader для заполнения подробных сведений табеля учета рабочего времени").</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Далее представлен снимок экрана репозитария прикладных объектов из Visual Studio.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Он показывает расширение таблицы TSTimesheetLine с полем TestLineString, добавленным в качестве настраиваемого поля.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Строка строки</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе записи табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Этот код управляет параметрами отображения для поля в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В следующем примере показано строковое поле для записей времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В этом поле имеются два параметра, <bpt id="p1">**</bpt>Первый вариант<ept id="p1">**</ept> и <bpt id="p2">**</bpt>Второй вариант<ept id="p2">**</ept>, которые доступны через кнопки параметров(переключатели).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поле в приложении связано с полем <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept>, которое добавляется в таблицу TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Обратите внимание на использование метода <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept>, чтобы упростить инициализацию свойств настраиваемого поля: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> и <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">При желании эти параметры также можно настроить вручную.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Использование цепочки команд метода buildCustomFieldListForEntry класса TSTimesheetEntry для ввода значений в запись табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Метод <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> используется для ввода значений в сохраненных строках табеля учета рабочего времени в мобильном приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Он принимает в качестве параметра запись TSTimesheetTrans.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Используйте цепочку команд класса TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Чтобы сохранить настраиваемое поле обратно в базу данных в обычном режиме использования, необходимо расширить несколько методов:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Метод <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> используется для определения того, была ли запись строки изменена пользователем в приложении и должна ли она быть сохранена в базе данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если производительность не критична, этот метод может быть упрощен, чтобы он всегда возвращал значение <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Методы <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> и <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> могут быть расширены таким образом, чтобы они могли вводить значения в запись базы данных TSTimesheetLine из представленной записи контракта данных TSTimesheetEntry.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В приведенном ниже примере обратите внимание на то, как сопоставление между полем базы данных и полем ввода выполняется вручную с помощью кода X++.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Метод <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> также может быть расширен, если настраиваемое поле, сопоставленное с объектом <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept>, должно быть записано обратно в таблицу базы данных TSTimesheetLineweek.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В следующем примере сохраняется значение <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> или <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept>, которое пользователь выбирает, в базу данных в качестве необработанного строкового значения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если поле базы данных является полем типа <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept>, эти значения можно вручную сопоставить значению перечисления, а затем сохранить в поле перечисления таблицы базы данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Отображение настраиваемого поля в разделе заголовка табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Далее представлен снимок экрана мобильного приложения при просмотре табеля учета рабочего времени пользователем.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Кнопка "Дополнительно" была выбрана в верхнем правом углу для отображения параметра "Подробнее".</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Команда "Подробнее"</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Далее представлен снимок экрана мобильного приложения, в котором отображается раздел "Дополнительно" табеля учета рабочего времени.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В раздел заголовка табеля учета рабочего времени добавлено настраиваемое поле, называемое "Коэффициент использования этого табеля учета рабочего времени (вычисляемое настраиваемое поле)"</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Для настраиваемого поля задается значение "0,667", доступное только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Раздел "Дополнительно"</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Расширение таблицы TSTimesheetTable таким образом, чтобы она содержала настраиваемое поле</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">В обычных сценариях вероятно, что данные для настраиваемого поля в разделе заголовка будут извлекаться из таблицы TSTimesheetHeader.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTable, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Они могут создаваться динамически в соответствии с логикой X++.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В следующем примере показан такой подход.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Поля в разделе заголовка в приложении всегда доступны только для чтения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе заголовка</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Этот код управляет параметрами отображения для поля в приложении.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В следующем примере показано вычисленное значение в разделе заголовка в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для заполнения сведений табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Метод <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> используется для ввода сведений заголовка табеля учета рабочего времени в мобильном приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Он принимает в качестве параметра запись TSTimesheetTable.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">В следующем примере не считываются никакие значения из базы данных.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Вместо этого используется логика X++ для создания вычисляемого значения, которое затем отображается в приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Другие возможности настройки/расширяемости</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Добавление дополнительной проверки для приложения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Существующая логика для функций табеля учета рабочего времени на уровне базы данных будет продолжать работать, как ожидается.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Чтобы прервать выполнение операции сохранения или отправки и показать определенное сообщение об ошибке, можно добавить <bpt id="p1">**</bpt>throw error("сообщение пользователю")<ept id="p1">**</ept> в код, используя цепочку расширения команд.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ниже приведены три примера полезных расширяемых методов:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> в таблице TSTimesheetLine возвращает значение <bpt id="p2">**</bpt>false<ept id="p2">**</ept> во время операции сохранения для строки табеля учета рабочего времени, в мобильном приложении отображается сообщение об ошибке.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Если <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> в таблице TSTimesheetTable возвращает значение <bpt id="p2">**</bpt>false<ept id="p2">**</ept> во время операции отправки табеля учета рабочего времени, в приложении, пользователю отображается сообщение об ошибке.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Логика, которая заполняет поля (например, <bpt id="p1">**</bpt>Свойство строки<ept id="p1">**</ept>), когда метод <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> в таблице TSTimesheetLine будет по-прежнему выполняться.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Скрытие и отметка готовых полей как доступных только для чтения через конфигурацию</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Из параметров проекта можно сделать так, чтобы готовые поля были доступны только для чтения или были скрыты в мобильном приложении.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Задайте параметры в разделе <bpt id="p1">**</bpt>Мобильные табели учета рабочего времени<ept id="p1">**</ept> на вкладке <bpt id="p2">**</bpt>Табель учета рабочего времени<ept id="p2">**</ept> на странице <bpt id="p3">**</bpt>Параметры модуля "Управление и учет по проектам"<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Параметры проекта</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Изменение доступных для выбора действий с помощью расширений</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Действия, доступные для выбора для проекта, заполняются с помощью методов <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> и <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> в классе <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Можно использовать цепочку команд для изменения этого поведения в соответствии с бизнес-ситуацией для мероприятий, доступных для выбора для конкретного проекта.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ввод категории проекта по умолчанию в записи табеля учета рабочего времени</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ввод категории проекта по умолчанию в записи табеля учета рабочего времени происходит на трех уровнях.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Можно использовать цепочку команд для расширения поведения на любом из этих уровней или на всех уровнях, чтобы добиться желаемого поведения.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Используется следующая иерархия:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Приложение пытается поместить категорию по умолчанию из ресурса проекта.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Эта категория по умолчанию задается в методах <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> и <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> в классе <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Если категория по умолчанию не указана на уровне ресурсов проекта, приложение пытается извлечь ее из проектной деятельности.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Эта категория по умолчанию задается в методе <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> в классе <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Если категория по умолчанию не указана на уровне действий проекта, категория по умолчанию берется из параметров проекта.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Эта категория по умолчанию задается в методе <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> в классе <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>