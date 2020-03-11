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
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080780"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="3b93e-103">Реализация настраиваемых полей для мобильного приложения Microsoft Dynamics 365 Project Timesheet на iOS и Android</span><span class="sxs-lookup"><span data-stu-id="3b93e-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b93e-104">В этом разделе приводятся общие шаблоны для использования расширений для реализации настраиваемых полей.</span><span class="sxs-lookup"><span data-stu-id="3b93e-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="3b93e-105">Рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="3b93e-105">The following topics are covered:</span></span>

- <span data-ttu-id="3b93e-106">Различные типы данных, поддерживаемые платформой настраиваемых полей</span><span class="sxs-lookup"><span data-stu-id="3b93e-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="3b93e-107">Порядок отображения доступных только для чтения или редактируемых полей в записях табеля учета рабочего времени, а также сохранения предоставленных пользователем значений обратно в базу данных</span><span class="sxs-lookup"><span data-stu-id="3b93e-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="3b93e-108">Порядок отображения полей только для чтения в заголовке табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="3b93e-109">Порядок интеграции другой пользовательской бизнес-логики для ввода значений по умолчанию в поля и выполнения дополнительной проверки</span><span class="sxs-lookup"><span data-stu-id="3b93e-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="3b93e-110">Аудитория</span><span class="sxs-lookup"><span data-stu-id="3b93e-110">Audience</span></span>

<span data-ttu-id="3b93e-111">Этот раздел предназначен для разработчиков, которые интегрируют свои настраиваемые поля в мобильное приложение Microsoft Dynamics 365 Project Timesheet, доступное для Apple iOS и Google Android.</span><span class="sxs-lookup"><span data-stu-id="3b93e-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="3b93e-112">Предполагается, что читатели знакомы с разработкой на языке X++ и функциональностью табеля учета рабочего времени проекта.</span><span class="sxs-lookup"><span data-stu-id="3b93e-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="3b93e-113">Контракт данных — класс TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="3b93e-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="3b93e-114">Класс **TSTimesheetCustomField** — это класс контракта данных X++, который представляет информацию о настраиваемом поле для функциональности табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="3b93e-115">Списки объектов настраиваемых полей передаются как в контракте данных TSTimesheetDetails, так и в контракте данных TSTimesheetEntry для отображения пользовательских полей в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="3b93e-116">**TSTimesheetDetails** — контракт заголовка табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="3b93e-117">**TSTimesheetEntry** — контракт проводки табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="3b93e-118">Группы этих объектов с одинаковыми данными проекта и значением **timesheetLineRecId** составляют строку.</span><span class="sxs-lookup"><span data-stu-id="3b93e-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="3b93e-119">fieldBaseType (Типы)</span><span class="sxs-lookup"><span data-stu-id="3b93e-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="3b93e-120">Свойство **FieldBaseType** объекта **TsTimesheetCustom** определяет тип поля, которое отображается в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="3b93e-121">Поддерживаются следующие типы значений **Types**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="3b93e-122">Значение типов</span><span class="sxs-lookup"><span data-stu-id="3b93e-122">Types value</span></span> | <span data-ttu-id="3b93e-123">Вид</span><span class="sxs-lookup"><span data-stu-id="3b93e-123">Type</span></span>              | <span data-ttu-id="3b93e-124">Основание</span><span class="sxs-lookup"><span data-stu-id="3b93e-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="3b93e-125">0</span><span class="sxs-lookup"><span data-stu-id="3b93e-125">0</span></span>           | <span data-ttu-id="3b93e-126">String (и Enum)</span><span class="sxs-lookup"><span data-stu-id="3b93e-126">String (and Enum)</span></span> | <span data-ttu-id="3b93e-127">Поле отображается как текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="3b93e-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="3b93e-128">1</span><span class="sxs-lookup"><span data-stu-id="3b93e-128">1</span></span>           | <span data-ttu-id="3b93e-129">Целочисленный</span><span class="sxs-lookup"><span data-stu-id="3b93e-129">Integer</span></span>           | <span data-ttu-id="3b93e-130">Значение отображается как число без десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="3b93e-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="3b93e-131">2</span><span class="sxs-lookup"><span data-stu-id="3b93e-131">2</span></span>           | <span data-ttu-id="3b93e-132">Действующий</span><span class="sxs-lookup"><span data-stu-id="3b93e-132">Real</span></span>              | <span data-ttu-id="3b93e-133">Значение отображается как число, имеющее десятичные знаки.</span><span class="sxs-lookup"><span data-stu-id="3b93e-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="3b93e-134">Чтобы показать реальное значение как валюту в приложении, используйте свойство **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="3b93e-135">Для задания числа отображаемых десятичных знаков можно использовать свойство **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="3b93e-136">3</span><span class="sxs-lookup"><span data-stu-id="3b93e-136">3</span></span>           | <span data-ttu-id="3b93e-137">Дата</span><span class="sxs-lookup"><span data-stu-id="3b93e-137">Date</span></span>              | <span data-ttu-id="3b93e-138">Форматы дат определяются параметром пользователя **Формат даты, времени и чисел**, указанным в параметрах **Настройки языка и страны/региона** в разделе **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="3b93e-139">4</span><span class="sxs-lookup"><span data-stu-id="3b93e-139">4</span></span>           | <span data-ttu-id="3b93e-140">Логический</span><span class="sxs-lookup"><span data-stu-id="3b93e-140">Boolean</span></span>           | |
| <span data-ttu-id="3b93e-141">15</span><span class="sxs-lookup"><span data-stu-id="3b93e-141">15</span></span>          | <span data-ttu-id="3b93e-142">GUID</span><span class="sxs-lookup"><span data-stu-id="3b93e-142">GUID</span></span>              | |
| <span data-ttu-id="3b93e-143">16</span><span class="sxs-lookup"><span data-stu-id="3b93e-143">16</span></span>          | <span data-ttu-id="3b93e-144">Int64</span><span class="sxs-lookup"><span data-stu-id="3b93e-144">Int64</span></span>             | |

- <span data-ttu-id="3b93e-145">Если свойство **stringOptions** не предусмотрено у объекта **TSTimesheetCustomField**, пользователю предоставляется текстовое поле свободного формата.</span><span class="sxs-lookup"><span data-stu-id="3b93e-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="3b93e-146">Свойство **stringLength** может использоваться для установки максимальной длины строки, которую пользователи могут вводить.</span><span class="sxs-lookup"><span data-stu-id="3b93e-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="3b93e-147">Если свойство **stringOptions** предоставляется в объекте **TSTimesheetCustomField**, эти элементы списка являются единственными значениями, которые пользователи могут выбрать с помощью кнопок параметров (переключателей).</span><span class="sxs-lookup"><span data-stu-id="3b93e-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="3b93e-148">В этом случае строковое поле может действовать как значение перечисления для целей ввода пользователем.</span><span class="sxs-lookup"><span data-stu-id="3b93e-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="3b93e-149">Чтобы сохранить значение в базе данных в качестве перечисления, вручную сопоставьте строковому значению значение перечисления перед сохранением в базе данных, используя цепочку команд (см. раздел "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе, например).</span><span class="sxs-lookup"><span data-stu-id="3b93e-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="3b93e-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="3b93e-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="3b93e-151">Это свойство можно использовать для форматирования вещественных значений как валюты.</span><span class="sxs-lookup"><span data-stu-id="3b93e-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="3b93e-152">Этот подход применяется только в том случае, если параметр **fieldBaseType** имеет значение **Real**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="3b93e-153">**TSCustomFieldExtendedType:None** — форматирование не применяется.</span><span class="sxs-lookup"><span data-stu-id="3b93e-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="3b93e-154">**TSCustomFieldExtendedType::Currency** — форматирование значения как валюты.</span><span class="sxs-lookup"><span data-stu-id="3b93e-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="3b93e-155">Когда форматирование валюты активно, поле **stringValue** может использоваться для передачи кода валюты, который должен отображаться в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="3b93e-156">Значение является значением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-156">The value is a read-only value.</span></span>

    <span data-ttu-id="3b93e-157">Поле **realValue** содержит сумму денег, которая должна быть сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="3b93e-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="3b93e-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="3b93e-159">Это свойство можно использовать, чтобы указать, где в приложении должно отображаться настраиваемое поле.</span><span class="sxs-lookup"><span data-stu-id="3b93e-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="3b93e-160">**TSCustomFieldSection::Header** — поле появится в разделе **Подробнее** приложения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="3b93e-161">Эти поля всегда предназначены только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-161">These fields are always read-only.</span></span>
- <span data-ttu-id="3b93e-162">**TSCustomFieldSection::Line** — поле будет отображаться после всех готовых полей строки в записях табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="3b93e-163">Эти поля могут быть как редактируемыми, так и только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="3b93e-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="3b93e-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="3b93e-165">Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="3b93e-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="3b93e-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="3b93e-167">Это свойство определяет поле, когда значения, предоставляемые приложением, сохраняются обратно в базу данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="3b93e-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="3b93e-168">isEditable (NoYes)</span></span>

<span data-ttu-id="3b93e-169">Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть редактируемым пользователями.</span><span class="sxs-lookup"><span data-stu-id="3b93e-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="3b93e-170">Установите для свойства значение **Нет**, чтобы поле было доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="3b93e-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="3b93e-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="3b93e-172">Установите для этого свойства значение **Да**, чтобы указать, что поле в разделе записи табеля учета рабочего времени должно быть обязательным.</span><span class="sxs-lookup"><span data-stu-id="3b93e-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="3b93e-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="3b93e-173">label (str)</span></span>

<span data-ttu-id="3b93e-174">Это свойство определяет метку, которая отображается рядом с полем в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="3b93e-175">stringOptions (список строк)</span><span class="sxs-lookup"><span data-stu-id="3b93e-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="3b93e-176">Это свойство применяется только тогда, когда для параметра **fieldBaseType** задано значение **String**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="3b93e-177">Если задано значение **stringOptions**, строковые значения, доступные для выбора с помощью кнопок параметров (переключателей), определяются строками в списке.</span><span class="sxs-lookup"><span data-stu-id="3b93e-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="3b93e-178">Если строки не указаны, запись свободного текста в поле строки разрешена (пример см. в пункте "Использование цепочки команд в классе TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных" далее в этом разделе).</span><span class="sxs-lookup"><span data-stu-id="3b93e-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="3b93e-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="3b93e-179">stringLength (int)</span></span>

<span data-ttu-id="3b93e-180">Это свойство определяет максимальную длину строкового поля.</span><span class="sxs-lookup"><span data-stu-id="3b93e-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="3b93e-181">Оно применяется только тогда, когда для параметра **fieldBaseType** задано значение **String**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="3b93e-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="3b93e-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="3b93e-183">Это свойство определяет число десятичных разрядов, отображаемых в вещественных полях.</span><span class="sxs-lookup"><span data-stu-id="3b93e-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="3b93e-184">Оно применяется только тогда, когда для параметра **fieldBaseType** задано значение **Real**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="3b93e-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="3b93e-185">orderSequence (int)</span></span>

<span data-ttu-id="3b93e-186">Это свойство управляет порядком отображения настраиваемых полей в приложении, когда указано более одного настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="3b93e-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="3b93e-187">Поля, имеющие меньшие номера, отображаются первыми.</span><span class="sxs-lookup"><span data-stu-id="3b93e-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="3b93e-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="3b93e-188">booleanValue (boolean)</span></span>

<span data-ttu-id="3b93e-189">Для полей типа **Boolean** это свойство передает логическое значение поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="3b93e-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="3b93e-190">guidValue (guid)</span></span>

<span data-ttu-id="3b93e-191">Для полей типа **GUID** это свойство передает значение глобально уникального идентификатора (GUID) поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="3b93e-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="3b93e-192">int64Value (int64)</span></span>

<span data-ttu-id="3b93e-193">Для полей типа **Int64** это свойство передает значение Int64 поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="3b93e-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="3b93e-194">intValue (int)</span></span>

<span data-ttu-id="3b93e-195">Для полей типа **Int** это свойство передает целое значение поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="3b93e-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="3b93e-196">realValue (real)</span></span>

<span data-ttu-id="3b93e-197">Для полей типа **Real** это свойство передает вещественное значение поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="3b93e-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="3b93e-198">stringValue (str)</span></span>

<span data-ttu-id="3b93e-199">Для полей типа **String** это свойство передает строковое значение поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="3b93e-200">Оно также используется для полей типа **Real**, отформатированных как валюта.</span><span class="sxs-lookup"><span data-stu-id="3b93e-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="3b93e-201">Для этих полей свойство используется для передачи кода валюты в приложение.</span><span class="sxs-lookup"><span data-stu-id="3b93e-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="3b93e-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="3b93e-202">dateValue (date)</span></span>

<span data-ttu-id="3b93e-203">Для полей типа **Date** это свойство передает значение даты поля между сервером и приложением.</span><span class="sxs-lookup"><span data-stu-id="3b93e-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="3b93e-204">Отображение и сохранение настраиваемого поля в разделе записи табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="3b93e-205">Далее представлен снимок экрана мобильного приложения для создания записи табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="3b93e-206">На нем отображаются готовые поля и настраиваемое поле в разделе "Запись времени", называемое "Тестовая строка" с уже установленным значением перечислимого типа "Второй параметр".</span><span class="sxs-lookup"><span data-stu-id="3b93e-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Настраиваемое поле тестовой строки в приложении](media/timesheet-entry.jpg)



<span data-ttu-id="3b93e-208">Ниже представлен снимок экрана мобильного приложения, на котором пользователь выбирает один из вариантов перечисления, доступных для настраиваемого поля "Тестовая строка".</span><span class="sxs-lookup"><span data-stu-id="3b93e-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="3b93e-209">Двумя вариантами являются "Первый параметр" и "Второй параметр", которые отображаются в виде переключателей.</span><span class="sxs-lookup"><span data-stu-id="3b93e-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="3b93e-210">В данный момент выбран второй вариант.</span><span class="sxs-lookup"><span data-stu-id="3b93e-210">The second option is currently selected.</span></span>

![Кнопки параметров (переключатели) для настраиваемого поля "Тестовая строка"](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="3b93e-212">Расширение таблицы TSTimesheetLine таким образом, чтобы она содержала настраиваемое поле</span><span class="sxs-lookup"><span data-stu-id="3b93e-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="3b93e-213">В обычных сценариях существует вероятность того, что данные для настраиваемого поля в разделе записи табеля учета рабочего времени будут сохранены в таблице TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="3b93e-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="3b93e-214">Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTrans, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).</span><span class="sxs-lookup"><span data-stu-id="3b93e-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="3b93e-215">Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="3b93e-216">Они могут создаваться динамически в соответствии с логикой X++.</span><span class="sxs-lookup"><span data-stu-id="3b93e-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="3b93e-217">Этот подход может быть полезен в сценариях только для чтения (пример динамически создаваемых значений настраиваемого поля см. в разделе "Использование цепочки команд класса TSTimesheetDetails, метод buildCustomFieldListForHeader для заполнения подробных сведений табеля учета рабочего времени").</span><span class="sxs-lookup"><span data-stu-id="3b93e-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="3b93e-218">Далее представлен снимок экрана репозитария прикладных объектов из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3b93e-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="3b93e-219">Он показывает расширение таблицы TSTimesheetLine с полем TestLineString, добавленным в качестве настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="3b93e-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Строка строки](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="3b93e-221">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе записи табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="3b93e-222">Этот код управляет параметрами отображения для поля в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="3b93e-223">Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.</span><span class="sxs-lookup"><span data-stu-id="3b93e-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="3b93e-224">В следующем примере показано строковое поле для записей времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="3b93e-225">В этом поле имеются два параметра, **Первый вариант** и **Второй вариант**, которые доступны через кнопки параметров(переключатели).</span><span class="sxs-lookup"><span data-stu-id="3b93e-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="3b93e-226">Поле в приложении связано с полем **TestLineString**, которое добавляется в таблицу TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="3b93e-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="3b93e-227">Обратите внимание на использование метода **TSTimesheetCustomField::newFromMetatdata()**, чтобы упростить инициализацию свойств настраиваемого поля: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** и **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="3b93e-228">При желании эти параметры также можно настроить вручную.</span><span class="sxs-lookup"><span data-stu-id="3b93e-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="3b93e-229">Использование цепочки команд метода buildCustomFieldListForEntry класса TSTimesheetEntry для ввода значений в запись табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="3b93e-230">Метод **buildCustomFieldListForEntry** используется для ввода значений в сохраненных строках табеля учета рабочего времени в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="3b93e-231">Он принимает в качестве параметра запись TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="3b93e-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="3b93e-232">Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="3b93e-233">Используйте цепочку команд класса TSTimesheetEntryService, чтобы сохранить запись табеля учета рабочего времени из приложения обратно в базу данных</span><span class="sxs-lookup"><span data-stu-id="3b93e-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="3b93e-234">Чтобы сохранить настраиваемое поле обратно в базу данных в обычном режиме использования, необходимо расширить несколько методов:</span><span class="sxs-lookup"><span data-stu-id="3b93e-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="3b93e-235">Метод **timesheetLineNeedsUpdating** используется для определения того, была ли запись строки изменена пользователем в приложении и должна ли она быть сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="3b93e-236">Если производительность не критична, этот метод может быть упрощен, чтобы он всегда возвращал значение **true**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="3b93e-237">Методы **populateTimesheetLineFromEntryDuringCreate** и **populateTimesheetLineFromEntryDuringUpdate** могут быть расширены таким образом, чтобы они могли вводить значения в запись базы данных TSTimesheetLine из представленной записи контракта данных TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="3b93e-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="3b93e-238">В приведенном ниже примере обратите внимание на то, как сопоставление между полем базы данных и полем ввода выполняется вручную с помощью кода X++.</span><span class="sxs-lookup"><span data-stu-id="3b93e-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="3b93e-239">Метод **populateTimesheetWeekFromEntry** также может быть расширен, если настраиваемое поле, сопоставленное с объектом **TSTimesheetEntry**, должно быть записано обратно в таблицу базы данных TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="3b93e-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="3b93e-240">В следующем примере сохраняется значение **firstOption** или **secondOption**, которое пользователь выбирает, в базу данных в качестве необработанного строкового значения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="3b93e-241">Если поле базы данных является полем типа **Enum**, эти значения можно вручную сопоставить значению перечисления, а затем сохранить в поле перечисления таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="3b93e-242">Отображение настраиваемого поля в разделе заголовка табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="3b93e-243">Далее представлен снимок экрана мобильного приложения при просмотре табеля учета рабочего времени пользователем.</span><span class="sxs-lookup"><span data-stu-id="3b93e-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="3b93e-244">Кнопка "Дополнительно" была выбрана в верхнем правом углу для отображения параметра "Подробнее".</span><span class="sxs-lookup"><span data-stu-id="3b93e-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Команда "Подробнее"](media/show-more.png)

<span data-ttu-id="3b93e-246">Далее представлен снимок экрана мобильного приложения, в котором отображается раздел "Дополнительно" табеля учета рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="3b93e-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="3b93e-247">В раздел заголовка табеля учета рабочего времени добавлено настраиваемое поле, называемое "Коэффициент использования этого табеля учета рабочего времени (вычисляемое настраиваемое поле)"</span><span class="sxs-lookup"><span data-stu-id="3b93e-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="3b93e-248">Для настраиваемого поля задается значение "0,667", доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Раздел "Дополнительно"](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="3b93e-250">Расширение таблицы TSTimesheetTable таким образом, чтобы она содержала настраиваемое поле</span><span class="sxs-lookup"><span data-stu-id="3b93e-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="3b93e-251">В обычных сценариях вероятно, что данные для настраиваемого поля в разделе заголовка будут извлекаться из таблицы TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="3b93e-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="3b93e-252">Однако можно использовать другие таблицы, если данные могут быть извлечены на основе предоставленной записи TSTimesheetTable, или если у нее нет определенного контекста записи (например, если поле в параметрах проекта задано только для чтения).</span><span class="sxs-lookup"><span data-stu-id="3b93e-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="3b93e-253">Обратите внимание, что настраиваемые поля не обязательно должны иметь в своей основе записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="3b93e-254">Они могут создаваться динамически в соответствии с логикой X++.</span><span class="sxs-lookup"><span data-stu-id="3b93e-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="3b93e-255">В следующем примере показан такой подход.</span><span class="sxs-lookup"><span data-stu-id="3b93e-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="3b93e-256">Поля в разделе заголовка в приложении всегда доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="3b93e-257">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для отображения поля в разделе заголовка</span><span class="sxs-lookup"><span data-stu-id="3b93e-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="3b93e-258">Этот код управляет параметрами отображения для поля в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="3b93e-259">Например, он определяет тип поля, метку, является ли поле обязательным и в каком разделе отображается поле.</span><span class="sxs-lookup"><span data-stu-id="3b93e-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="3b93e-260">В следующем примере показано вычисленное значение в разделе заголовка в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="3b93e-261">Использование цепочки команд метода buildCustomFieldListForHeader класса TSTimesheetDetails для заполнения сведений табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="3b93e-262">Метод **buildCustomFieldListForHeader** используется для ввода сведений заголовка табеля учета рабочего времени в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="3b93e-263">Он принимает в качестве параметра запись TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="3b93e-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="3b93e-264">Поля из этой записи могут использоваться для заполнения значения настраиваемого поля в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="3b93e-265">В следующем примере не считываются никакие значения из базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b93e-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="3b93e-266">Вместо этого используется логика X++ для создания вычисляемого значения, которое затем отображается в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="3b93e-267">Другие возможности настройки/расширяемости</span><span class="sxs-lookup"><span data-stu-id="3b93e-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="3b93e-268">Добавление дополнительной проверки для приложения</span><span class="sxs-lookup"><span data-stu-id="3b93e-268">Adding additional validation for the app</span></span>

<span data-ttu-id="3b93e-269">Существующая логика для функций табеля учета рабочего времени на уровне базы данных будет продолжать работать, как ожидается.</span><span class="sxs-lookup"><span data-stu-id="3b93e-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="3b93e-270">Чтобы прервать выполнение операции сохранения или отправки и показать определенное сообщение об ошибке, можно добавить **throw error("сообщение пользователю")** в код, используя цепочку расширения команд.</span><span class="sxs-lookup"><span data-stu-id="3b93e-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="3b93e-271">Ниже приведены три примера полезных расширяемых методов:</span><span class="sxs-lookup"><span data-stu-id="3b93e-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="3b93e-272">Если **validateWrite** в таблице TSTimesheetLine возвращает значение **false** во время операции сохранения для строки табеля учета рабочего времени, в мобильном приложении отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3b93e-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="3b93e-273">Если **validateSubmit** в таблице TSTimesheetTable возвращает значение **false** во время операции отправки табеля учета рабочего времени, в приложении, пользователю отображается сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3b93e-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="3b93e-274">Логика, которая заполняет поля (например, **Свойство строки**), когда метод **insert** в таблице TSTimesheetLine будет по-прежнему выполняться.</span><span class="sxs-lookup"><span data-stu-id="3b93e-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="3b93e-275">Скрытие и отметка готовых полей как доступных только для чтения через конфигурацию</span><span class="sxs-lookup"><span data-stu-id="3b93e-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="3b93e-276">Из параметров проекта можно сделать так, чтобы готовые поля были доступны только для чтения или были скрыты в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="3b93e-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="3b93e-277">Задайте параметры в разделе **Мобильные табели учета рабочего времени** на вкладке **Табель учета рабочего времени** на странице **Параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Параметры проекта](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="3b93e-279">Изменение доступных для выбора действий с помощью расширений</span><span class="sxs-lookup"><span data-stu-id="3b93e-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="3b93e-280">Действия, доступные для выбора для проекта, заполняются с помощью методов **getActivitiesForProject()** и **getActivityQuery()** в классе **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="3b93e-281">Можно использовать цепочку команд для изменения этого поведения в соответствии с бизнес-ситуацией для мероприятий, доступных для выбора для конкретного проекта.</span><span class="sxs-lookup"><span data-stu-id="3b93e-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="3b93e-282">Ввод категории проекта по умолчанию в записи табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="3b93e-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="3b93e-283">Ввод категории проекта по умолчанию в записи табеля учета рабочего времени происходит на трех уровнях.</span><span class="sxs-lookup"><span data-stu-id="3b93e-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="3b93e-284">Можно использовать цепочку команд для расширения поведения на любом из этих уровней или на всех уровнях, чтобы добиться желаемого поведения.</span><span class="sxs-lookup"><span data-stu-id="3b93e-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="3b93e-285">Используется следующая иерархия:</span><span class="sxs-lookup"><span data-stu-id="3b93e-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="3b93e-286">Приложение пытается поместить категорию по умолчанию из ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="3b93e-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="3b93e-287">Эта категория по умолчанию задается в методах **getCurrentUserResource** и **getDelegatedResourcesForCurrentUser** в классе **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="3b93e-288">Если категория по умолчанию не указана на уровне ресурсов проекта, приложение пытается извлечь ее из проектной деятельности.</span><span class="sxs-lookup"><span data-stu-id="3b93e-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="3b93e-289">Эта категория по умолчанию задается в методе **getActivitiesForProject** в классе **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="3b93e-290">Если категория по умолчанию не указана на уровне действий проекта, категория по умолчанию берется из параметров проекта.</span><span class="sxs-lookup"><span data-stu-id="3b93e-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="3b93e-291">Эта категория по умолчанию задается в методе **getProjectDetailsbyRule** в классе **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="3b93e-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
