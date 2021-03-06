---
title: Разработка конфигурации для создания документов в формате Excel
description: В этой теме описывается, как создавать формат электронной отчетности (ER) для заполнения шаблона Excel, а затем создание исходящих документов в формате Excel.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893916"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Разработка конфигурации для создания документов в формате Excel

[!include[banner](../includes/banner.md)]

Можно разработать конфигурацию формата [электронной отчетности (ER)](general-electronic-reporting.md), имеющую [компонент формата](general-electronic-reporting.md#FormatComponentOutbound) ER, который можно настроить для создания исходящего документа в формате книги Microsoft Excel. Для этой цели необходимо использовать специальный компонент формата ER.

Для получения дополнительных сведений об этой возможности следуйте указаниям в разделе [Создание конфигурации для создания отчетов в формате OPENXML](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Добавление нового формата ER

При добавлении новой конфигурации формата ER для создания исходящего документа в формате книги Excel необходимо либо выбрать значение **Excel** для атрибута **типа формата** для формата, либо оставить атрибут **тип формата** пустым.

- При выборе **Excel** можно настроить формат для создания исходящего документа только в формате Excel.
- Если оставить этот атрибут пустым, можно настроить формат для создания исходящего документа в любом формате, поддерживаемом структурой ER.

Чтобы настроить компонент "формат ER" конфигурации, выберите **конструктор** на панели операций и откройте компонент формата ER для редактирования в конструкторе операций ER.

![Страница конфигураций](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Компонент файла Excel

### <a name="manual-entry"></a>Ручной ввод

Для создания исходящего документа в формате Excel необходимо добавить компонент **файла\\Excel** в настроенный формат ER.

![Компонент Excel\файл](./media/er-excel-format-add-file-component.png)

Чтобы указать макет для исходящего документа, вложите в компонент **файл\\Excel** книгу Excel с расширением .xlsx в качестве шаблона для исходящих документов.

> [!NOTE]
> При присоединении шаблона вручную необходимо использовать [тип документа](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), который был настроен для этой цели в [параметрах ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Добавление вложения в компонент Excel\файл](./media/er-excel-format-add-file-component2.png)

Чтобы указать, как будет заполняться заданный шаблон при выполнении настроенного формата ER, необходимо добавить вложенные компоненты **Лист**, **Диапазон**, и **Ячейка** к компоненту **Excel\\файл**. Каждый вложенный компонент должен быть связан с именованной номенклатурой Excel.

### <a name="template-import"></a>Импорт шаблона

Можно выбрать **Импорт из Excel** на вкладке **Импорт** панели операций для импорта нового шаблона в пустой формат ER. В этом примере компонент **Excel\\файл** будет создан автоматически, и к нему будет присоединяться импортированный шаблон. Все необходимые компоненты ER также будут созданы автоматически на основе списка обнаруженных именованных номенклатур Excel.

![Выберите Импорт из Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> Если требуется создать необязательный элемент **Лист** в редактируемом формате ER, установите для параметра **Создать элемент формата листа Excel** значение **Да**.

## <a name="sheet-component"></a>Компонент листа

Компонент **Лист** указывает лист прилагаемой книги Excel, который должен быть заполнен. Имя листа в шаблоне Excel определяется в свойстве **Лист** этого компонента.

> [!NOTE]
> Этот компонент не является обязательным для книг Excel, содержащих один лист.

На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **листа**, чтобы указать, должен ли компонент быть помещен в созданный документ:

- Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий лист.
- Если выражение свойства **Включено** настроено на возврат значения **Ложь** во время выполнения, созданный документ не будет содержать лист.

![Пример компонента листа](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Компонент Диапазон

Компонент **диапазон** указывает диапазон Excel, который должен управляться этим компонентом ER. Имя диапазона определяется в свойстве **Диапазон Excel** этого компонента.

Свойство **Направление репликации** определяет, будет ли и каким образом повторяться диапазон в созданном документе:

- Если для свойства **Направление репликации** установлено значение **Без репликации** , соответствующий диапазон Excel не будет повторяться в созданном документе.
- Если для свойства **Направление репликации** установлено значение **Вертикально** , соответствующий диапазон Excel будет повторяться в созданном документе. Каждый реплицируемый диапазон помещается под исходным диапазоном шаблона Excel. Число повторов определяется числом записей в источнике данных типа **списка записей**, привязанного к этому компоненту ER.
- Если для свойства **Направление репликации** установлено значение **Горизонтально** , соответствующий диапазон Excel будет повторяться в созданном документе. Каждый реплицируемый диапазон помещается справа от исходным диапазоном шаблона Excel. Число повторов определяется числом записей в источнике данных типа **списка записей**, привязанного к этому компоненту ER.

Для получения дополнительных сведений о горизонтальной репликации выполните шаги разделе [Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel](tasks/er-horizontal-1.md).

Компонент **диапазон** может иметь другие вложенные компоненты ER, которые используются для ввода значений в соответствующие именованные диапазоны Excel.

- Если какой-либо компонент группы **Текст** используется для ввода значений, значение вводится в диапазон Excel в виде текстового значения.

    > [!NOTE]
    > Этот шаблон используется для форматирования введенных значений на основе языкового стандарта, определенного в приложении.

- Если для ввода значений используется компонент **ячейка** группы **Excel**, значение вводится в диапазон Excel как значение типа данных, которое определяется привязкой этого компонента **ячейка** (например, **Строка**, **Вещественный** или **Целочисленный**).

    > [!NOTE]
    > Этот шаблон используется для того, чтобы приложение Excel могло форматировать введенные значения на основе языкового стандарта локального компьютера, открывающего исходящий документ.

На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **Диапазон**, чтобы указать, должен ли компонент быть помещен в созданный документ:

- Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий диапазон.
- Если выражение свойства **Включено** настроено так, что оно возвращает значение **Ложь** во время выполнения, и если этот диапазон не представляет все строки или столбцы, в созданный документ не будет помещен соответствующий диапазон.
- Если выражение свойства **Включено** настроено так, что оно возвращает значение **Ложь** во время выполнения, и этот диапазон представляет все строки или столбцы, созданный документ будет содержать эти строки и столбцы в виде скрытых строк и столбцов.

## <a name="cell-component"></a>Компонент ячейка

Компонент **ячейка** используется для заполнения именованных ячеек, фигур и изображений Excel. Чтобы указать имя объекта Excel, которое должно быть заполнено компонентом ER **ячейка**, необходимо указать название этого объекта в свойстве **диапазон Excel** для компонента **ячейка**.

На вкладке **Сопоставление** в конструкторе операций ER можно настроить свойство **Включено** для компонента **Ячейка**, чтобы указать, должен ли объект быть помещен в созданный документ:

- Если выражение свойства **Включено** настроено так, что оно возвращает значение **истина** во время выполнения, или если какое-либо выражение не настроено, в созданный документ будет помещен соответствующий объект. Привязка этого компонента **ячейка** указывает значение, помещаемое в соответствующий объект.
- Если выражение свойства **Включено** настроено на возврат значения **Ложь** во время выполнения, соответствующий объект не будет помещен в созданном документе.

Когда компонент **ячейка** настраивается на ввод значения в ячейку, она может быть привязана к источнику данных, который возвращает значение примитивного типа данных (например, **Строка**, **Вещественный** или **Целочисленный**). В этом случае значение вводится в ячейку как значение того же типа данных.

Когда компонент **ячейка** настраивается на ввод значения в форму Excel, она может быть привязана к источнику данных, который возвращает значение примитивного типа данных (например, **Строка**, **Вещественный** или **Целочисленный**). В этом случае значение вводится в форму Excel как текст этой формы. Для значений типов данных, не являющихся **строками**, преобразование в текст выполняется автоматически.

> [!NOTE]
> Можно настроить компонент **ячейка** для заполнения формы только в тех случаях, когда поддерживается свойство текста формы.

Когда компонент **ячейка** настраивается на ввод значения в изображение Excel, она может быть привязана к источнику данных, который возвращает значение типа данных **Контейнер**, который представляет изображение в двоичном формате. В этом случае значение вводится в изображение Excel в виде изображения.

> [!NOTE]
> Все изображения и формы Excel перекрепляются по верхнему левому углу в конкретную ячейку или диапазон Excel. Если требуется копировать изображение или форму Excel, необходимо настроить ячейку или диапазон, для которых она была привязана, в качестве копируемой ячейки или диапазона.

Дополнительные сведения о внедрении изображений и форм см. в разделе [Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Компонент Разрыв страницы

Компонент **Разрыв страниц** заставляет Excel начать новую страницу. Этот компонент не требуется, если необходимо использовать разбиение по страницам Excel по умолчанию, но его следует использовать, если требуется, чтобы Excel использовал формат ER для структурирования разбиения.

## <a name="footer-component"></a>Компонент нижнего колонтитула

**Компонент нижнего колонтитула** используется для заполнения нижних колонтитулов в нижней части созданного листа в книге Excel.

> [!NOTE]
> Этот компонент можно добавить для каждого компонента **листа** для указания других нижних колонтитулов для других листов в созданной книге Excel.

При настройке отдельного компонента **нижнего колонтитула** для указания страниц, для которых используется компонент, можно использовать свойство **Внешний вид верхнего или нижнего колонтитула**. Доступны следующие значения:

- **Любой** — запускает настроенный компонент **нижнего колонтитула** для любой страницы родительского листа Excel.
- **Первый** — запускает настроенный компонент **нижнего колонтитула** только для первой страницы родительского листа Excel.
- **Четный** — запускает настроенный компонент **нижнего колонтитула** только для четных страниц родительского листа Excel.
- **Нечетный** — запускает настроенный компонент **нижнего колонтитула** только для нечетных страниц родительского листа Excel.

Для одного компонента **листа** можно добавить несколько компонентов **нижних колонтитулов**, каждое из которых имеет различное значение свойства **Внешний вид верхнего или нижнего колонтитула**. Таким образом можно создавать различающиеся нижние колонтитулы для страниц других типов в листе Excel.

> [!NOTE]
> Убедитесь, что каждый компонент **Нижний колонтитул** который вы добавляете к одному компоненту **Лист**, имеет другое значение для свойства **Внешний вид верхнего или нижнего колонтитула**. В противном случае возникнет [ошибка проверки](er-components-inspections.md#i16). Полученное сообщение об ошибке уведомляет пользователя о несогласованности.

В добавленный компонент **нижнего колонтитула** добавьте необходимые вложенные компоненты **Текст\\Строка**, **Текст\\DateTime** или другого типа. Настройте привязки для этих компонентов, чтобы указать, как заполняются нижние колонтитулы страницы.

Можно также использовать специальные [коды форматирования](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers), чтобы правильно отформатировать содержимое созданного нижнего колонтитула. Чтобы узнать, как использовать этот подход, выполните шаги, указанные в [примере 1](#example-1) далее в этом разделе.

> [!NOTE]
> При настройке форматов ER убедитесь, что установлен [предел](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) Excel и максимальное число символов для одного верхнего или нижнего колонтитула.

## <a name="header-component"></a>Компонент заголовка

Компонент **Заголовок** используется для заполнения заголовков в верхней части созданного листа в книге Excel. Он используется как и компонент **нижнего колонтитула**.

## <a name="edit-an-added-er-format"></a>Редактирование добавленного формата ER

### <a name="update-a-template"></a>Обновление шаблона

Можно выбрать **Обновление из Excel** на вкладке **Импорт** панели операций для импорта обновленного шаблона в редактируемый формат ER. В ходе этого процесса шаблон выбранного компонента **Excel\\Файл** будет заменен новым шаблоном. Содержимое редактируемого формата ER будет синхронизировано с содержимым обновленного шаблона ER.

- Новый компонент формата ER будет создан автоматически для каждого имени Excel, если компонент формата ER не найден в редактируемом формате.
- Если соответствующее имя Excel не найдено, все компоненты формата ER будут удалены из редактируемого формата ER.

> [!NOTE]
> Задайте для параметра **Создать элемент формата листа Excel** значение **Да**, если требуется создать необязательный элемент **Лист** в редактируемом формате ER.
>
> Если редактируемый формат ER первоначально содержал элементы **лист**, рекомендуется настроить для параметра **Создать элемент формата листа Excel** значение **Да**, если импортируется обновленный шаблон. В противном случае все вложенные элементы исходного элемента **лист** будут создаваться "с нуля". Таким образом, все привязки повторно созданных элементов формата будут потеряны в обновленном формате ER.

![Параметр "Создать элемент формата листа Excel" в диалоговом окне Обновление из Excel](./media/er-excel-format-update-template.png)

Чтобы получить дополнительные сведения об этой функции, выполните действия, описанные в разделе [Изменение форматов электронной отчетности путем повторного применения шаблонов Excel](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Проверяет формат ER

При проверке формата ER, который может быть изменен, выполняется проверка согласованности, чтобы убедиться в том, что в используемом в данный момент шаблоне Excel присутствует имя Excel. Будет выведено уведомление о любых несоответствиях. Для некоторых несоответствий будет предложено автоматическое исправление вопросов.

![Сообщения об ошибка проверки](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Управление вычислением формул Excel

При создании исходящего документа в формате книги Microsoft Excel некоторые ячейки данного документа могут содержать формулы Excel. Когда функция **Включить использование библиотеки EPPlus в платформе электронной отчетности** включена, можно управлять моментом вычисления формул путем изменения значения [параметра](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Параметры расчета** в используемом шаблоне Excel:

- Выберите **Автоматически**, чтобы пересчитать все зависимые формулы каждый раз, когда сформированный документ дополняется новыми диапазонами, ячейками и т. д.
    >[!NOTE]
    > Это может привести к снижению производительности для шаблонов Excel, которые содержат несколько связанных формул.
- Выберите **Вручную**, чтобы избежать пересчета формулы при создании документа.
    >[!NOTE]
    > Пересчет формул вручную выполняется принудительно при открытии созданного документа для предварительного просмотра с помощью Excel.
    > Не используйте этот параметр, если вы настраиваете место назначение электронной отчетности, которое предполагает использование созданного документа без предварительного просмотра в Excel (преобразование в PDF, электронная почта и т. д.), так как созданный документ может не содержать значений в ячейках, содержащих формулы.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Пример 1: форматирование содержимого нижнего колонтитула

1. Используйте предоставленные конфигурации ER для [создания](er-generate-printable-fti-forms.md) печатаемого документа накладной с произвольным текстом (FTI).
2. Просмотр нижнего колонтитула созданного документа. Обратите внимание, что в нем содержится информация о номере текущей страницы и общее число страниц в документе.

    ![Просмотр нижнего колонтитула созданного документа в формате Excel](./media/er-fillable-excel-footer-1.gif)

3. В конструкторе формата ER [откройте](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) образец формата ER для просмотра.

    Нижний колонтитул листа **Накладная** создается на основе параметров двух компонентов **Строка**, расположенных в компоненте **нижнего колонтитула**:

    - Первый компонент **Строка** заполняется следующими кодами форматирования, чтобы в Excel применялось определенное форматирование:

        - **&C** — выравнивание текста нижнего колонтитула по центру.
        - **&"Segoe UI,Regular"&8** — представляет текст нижнего колонтитула в шрифте "Segoe UI Regular" размером 8 пунктов.

    - Второй компонент **Строка** заполняет текст, содержащий номер текущей страницы и общее число страниц в текущем документе.

    ![Просмотр компонента формата электронной отчетности нижнего колонтитула на странице конструктора форматов](./media/er-fillable-excel-footer-2.png)

4. Настройка образца формата ER для изменения нижнего колонтитула текущей страницы:

    1. [Создайте](er-quick-start2-customize-report.md#DeriveProvidedFormat) производный настраиваемый формат ER для **накладной с произвольным текстом (Excel)** на основе образца формата ER.
    2. Добавьте первую новую пару компонентов **Строка** для **нижнего колонтитула** для листа **накладной**:

        1. Добавьте компонент **Строка**, который выравнивает название компании по левому краю и представляет его в шрифте "Segoe UI Regular" размера 8 пунктов (**"&L&"Segoe UIRegular"&8"**).
        2. Добавьте компонент **Строка**, который заполняет название компании (**model.InvoiceBase.CompanyInfo.Name**).

    3. Добавьте вторую новую пару компонентов **Строка** для **нижнего колонтитула** для листа **накладной**:

        1. Добавьте компонент **Строка**, который выравнивает дату обработки по правому краю и представляет его в шрифте "Segoe UI Regular" размера 8 пунктов (**"&R&"Segoe UIRegular"&8"**).
        2. Добавьте компонент **Строка**, который заполняет дату обработки в пользовательском формате (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Просмотр компонента формата электронной отчетности нижнего колонтитула на странице конструктора форматов](./media/er-fillable-excel-footer-3.png)

    4. [Заполните](er-quick-start2-customize-report.md#CompleteDerivedFormat) черновую версию производного пользовательского формата ER **для накладной с произвольным текстом (Excel)**.

5. [Настройте](er-generate-printable-fti-forms.md#configure-print-management) Управление печатью для использования производного пользовательского формата ER для **накладной с произвольным текстом (Excel)** вместо образца формата ER.
6. Создание печатаемого документа FTI и просмотр нижнего колонтитула созданного документа.

    ![Просмотр нижнего колонтитула созданного документа в формате Excel](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Разработка конфигурации для создания отчетов в формате OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Изменение форматов электронной отчетности путем повторного применения шаблонов Excel](modify-electronic-reporting-format-reapply-excel-template.md)

[Использование горизонтально разворачивающихся диапазонов для динамического добавления столбцов в отчеты Excel](tasks/er-horizontal-1.md)

[Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md)

[Настройка электронной отчетности (ER) для загрузки данных в Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]