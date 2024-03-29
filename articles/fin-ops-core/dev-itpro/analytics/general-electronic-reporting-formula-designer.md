---
title: Конструктор формул в электронной отчетности (ER)
description: В этой статье содержится информация о том, как использовать конструктор формул в электронной отчетности (ER).
author: kfend
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 283c882300ece460c18ffebe572238e7629f8dee
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476819"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Конструктор формул в электронной отчетности (ER)

[!include [banner](../includes/banner.md)]

В этой статье описывается, как использовать конструктор формул в электронной отчетности (ER). При проектировании формата для определенного электронного документа в ER можно использовать формулы для преобразования данных, чтобы они отвечали требованиям для выполнения и форматирования этого документа. Эти формулы напоминают формулы в Microsoft Excel. В формулах поддерживаются различные типы функций: текст, дата и время, математические логические, информация, преобразование типа данных и другое (характерные для конкретных бизнес-доменов функции).

## <a name="formula-designer-overview"></a>Обзор конструктора формул

Электронная отчетность (ER) поддерживает конструктор формул. Поэтому во время разработки имеется возможность задать выражения, которые можно использовать для выполнения следующих задач во время выполнения:

- Преобразование данных, полученных из базы данных приложения, которые должны вводить в модель данных ER, играющую роль источника данных для форматов ER. (Например, эти преобразования могут содержать фильтрацию, группирование и преобразование типов данных.)
- Форматирование данных, которые должны быть отправлены в генерирующий электронный документ в соответствии с макетом и условиями определенного формата электронной отчетности. (Например, форматирование может быть выполнено в соответствии с затребованным языком, культурой или кодировкой.)
- Управление процессом создания электронных документов. (Например, выражения могут включать или отключать вывод конкретных элементов формата, в зависимости от обрабатываемых данных. Они также могут прерывать процесс создания документа или выдавать сообщения пользователям.)

Страницу **Конструктор формул** можно открыть при выполнении любого из следующих действий:

- Связывание элементов источника данных с компонентами модели данных.
- Связывание элементов источника данных с компонентами формата.
- Завершение обслуживания вычисляемых полей, которые являются частью источников данных.
- Определение условий видимости и редактируемости для параметров пользовательского ввода.
- Определение значений по умолчанию для параметров пользовательского ввода.
- Разработка преобразований формата.
- Определение условий включения для компонентов формата.
- Определение имен файлов для компонентов FILE формата.
- Определение условий для проверок управления процессом.
- Определение текста сообщения для проверок управления процессом.

## <a name="data-binding"></a><a name="Binding"></a>Привязка данных

Конструктор формул ER можно использовать для определения выражения, которое конвертирует данные, полученные от источников данных, таким образом, чтобы эти данные можно было ввести в потребителе данных следующим образом во время выполнения:

- Из источников данных приложения и параметров времени выполнения в модель данных ER
- Из модели данных ER в формат ER
- Из источников данных приложения и параметров времени выполнения в формат ER

На следующем рисунке показана разработка выражения этого типа. В этом примере выражение округляет значение поля **Intrastat.AmountMST** таблицы Интрастат до двух десятичных знаков, и затем возвращает округленное значение.

[![Выражение связывания данных.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

На следующем рисунке показано, как может использоваться выражение этого типа. В этом примере результат сконструированного выражения вводится в компоненте **Transaction.InvoicedAmount** модели данных **Модель налоговой отчетности**.

[![Используемое выражение привязки данных.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Во время выполнения созданная формула `ROUND (Intrastat.AmountMST, 2)` округляет значение поля **AmountMST** для каждой записи в таблице Интрастат до двух десятичных разрядов. Затем она вводит округленное значение в компонент **Transaction.InvoicedAmount** модели данных **Налоговая отчетность**.

## <a name="data-formatting"></a><a name="Transformation"></a>Формат данных

Конструктор формул ER можно использовать для определения выражения, которое форматирует данные, полученные от источников данных, таким образом, чтобы эти данные можно было отправить как часть создания электронного документа. Может иметься форматирование, которое должно применяться как типовое правило, которое должно быть повторно использовано для формата. В этом случае можно ввести это форматирование один раз в конфигурации формата как именованное преобразование, имеющее выражение форматирования. Позднее это именованное преобразование можно связывать с многими компонентами формата, выходные данные в которых должны форматироваться в соответствии с созданным выражением форматирования.

На следующем рисунке показана разработка преобразования этого типа. В этом примере преобразование **TrimmedString** усекает входящие данные типа данных *String*, удаляя ведущие и конечные пробелы. Затем оно возвращает значение усеченной строки.

[![Преобразование.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

На следующем рисунке показано, как может использоваться преобразование этого типа. В данном примере несколько компонентов формата отправляют текст как выходные данные для создания электронного документа во время выполнения. Все эти компоненты формата ссылаются на преобразование **TrimmedString** по имени.

[![Используемое преобразование.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Когда компоненты формата, такие как компонент **partyName** на предыдущем рисунке, ссылаются на преобразование **TrimmedString**, это преобразование отправляет текст как выходные данные в создающий электронный документ. Этот текст не включает начальные и конечные пробелы.

Если у вас есть форматирование, которое должно применяться индивидуально, его можно внедрить как отдельное выражение привязки определенного компонента "формат". На следующем рисунке показано выражение этого типа. В этом примере компонент формата **partyType** привязан к источнику данных через выражение, преобразующее входящие данные из поля **Model.Company.RegistrationType** в источнике данных в текст в верхнем регистре. Выражение затем отправляет этот текст как выходные данные в электронный документ.

[![Применение форматирования к отдельному компоненту.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Управление процессом

Конструктор формул ER может использоваться для определения выражений для управления процессом формирования электронных документов. Можно выполнить следующие задачи.

- определения условий, определяющий, когда процесс создания документа должен быть остановлен.
- задания выражений, которые либо будут создавать сообщения для пользователя об остановленных процессах, либо записывать сообщения в журнал выполнения о продолжении процесса формирования отчетности;
- Определение имен файлов генерируемых электронных документов и управление условиями их создания.

Каждое из правил управления процессом конструируется в виде отдельной валидации. На следующем рисунке показана проверка этого типа. Здесь объяснение конфигурации в этом примере:

- Проверка производится, когда узел **INSTAT** создан во время создания XML-файла.
- Если список транзакций пуст, проверка останавливает процесс выполнения и возвращает значение **FALSE**.
- Проверка возвращает сообщение об ошибке, которое включает текст метки SYS70894 на языке, предпочитаемом пользователем.

[![Проверка.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Конструктор формул ER используется также для создания имени файла для формируемого электронного документа и управления процессом создания файла. На следующем рисунке показана разработка управления процессом этого типа. Здесь объяснение конфигурации в этом примере:

- Список записей из источника данных **model.Intrastat** разделен на пакеты. Каждый пакет содержит до 1000 записей.
- Выпуск создает ZIP-файл, который содержит один файл в формате XML для каждой партии, который была создана.
- Выражение возвращает имя файла для генерации электронных документов путем объединения имени файла и расширения имени файла. Для второй партии и всех последующих партий имя файла содержит код партии в качестве суффикса.
- Выражение включает (возвратом значения **TRUE**) процесс создания файла для тех пакетов, которые содержат хотя бы одну запись.

[![Управление процессом.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Управление содержимым документов

Конструктор формул электронной отчетности можно использовать для настройки выражений, определяющих, какие данные будут помещены в создаваемые электронные документы во время выполнения. Выражения могут включать или отключать вывод конкретных элементов формата, в зависимости от обрабатываемых данных и настроенной логики. Эти выражения могут быть введены для одного элемента формата в поле **Включено** на вкладке **Сопоставление** на странице **Конструктор операций**. Вы можете ввести выражения как логическое условие, которое возвращает *логическое* значение:

- Если условие возвращает **True**, текущий элемент формата выполняется.
- Если условие возвращает **False**, текущий элемент формата пропускается.

На следующем рисунке показаны выражения этого типа. (В качестве примера используется версия 11.12.11 конфигурации формата **Перенос кредита ISO20022 (NO)**, предоставляемой корпорацией Майкрософт.) Компонент формата **XMLHeader** настроен для описания структуры сообщения о переносе кредита в соответствии со стандартами сообщений ISO 20022 XML. Компонент формата **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** сконфигурирован для добавления к созданному сообщению, элементу XML **Ustrd**, и размещения информации о предъявлении к оплате в неструктурированный формат в виде текста следующих элементов XML:

- Компонент **PaymentNotes** используется для создания текста платежных примечаний.
- Компонент **DelimitedSequence** создает номера накладных с разделителями-запятыми, которые используются для сопоставления текущего переноса кредита.

[![Компоненты PaymentNotes и DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Компоненты **PaymentNotes** и **DelimitedSequence** обозначены с использованием вопросительного знака. Вопросительный знак указывает на то, что использование компонента является условным. В этом случае использование компонентов основано на следующих критериях:
>
> - Выражение `@.PaymentsNotes <> ""`, определенное для компонента **PaymentNotes**, разрешает (возвращая **TRUE**) заполнение XML-элемента **Ustrd**, тестом примечаний платежа, если этот текст для текущего переноса кредита не пуст.
>
>    [![Выражение для компонента PaymentNotes.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Выражение `@.PaymentsNotes = ""`, определенное для компонента **DelimitedSequence**, выражение разрешает (возвращая **TRUE**) заполнение XML-элемента **Ustrd** разделенными запятыми номерами накладных, которые используются для сопоставления текущего переноса кредита, когда текст примечаний платежа для этого переноса кредита пуст.
>
>    [![Выражение для компонента DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> На основе этой настройки созданное сообщение для каждого платежа должника, XML-элемент **Ustrd**, будет содержать либо текст примечаний по платежу, либо, если такой текст пуст, текст с разделенными запятыми номерами накладных, использованных для сопоставления данного платежа.

## <a name="assistance-in-formulas-writing"></a>Помощь в написании формул

### <a name="data-sources-navigator"></a>Навигатор по источникам данных

Формулу, представляющую элемент структурированного источника данных, можно изменять. При настройке параметров ER для представления пути к элементу структурированного источника данных в виде [относительного пути](relative-path-data-bindings-er-models-format.md) знак "собачки" (@) [отображается](er-formula-language.md#relative-path) в формуле вместо оставшейся части абсолютного пути в используемой иерархической древовидной структуре. Эта оставшаяся часть абсолютного пути указывает на родительский элемент редактируемого элемента. В версии Finance **10.0.30 и более поздних версиях** на странице **Конструктор формул** в области **Источники данных** можно выбрать пункт **Переход к @**, чтобы поместить курсор дерева источников данных на элемент, который является родительским элементом для редактируемого элемента. Структура всех свернутых элементов по возрастанию будет автоматически и рекурсивно развернута при необходимости. Это развертывание может помочь быстро визуализировать базовый элемент редактируемого элемента, увидеть одноуровневые элементы редактируемого элемента в дереве источников данных и использовать каждый из них в изменяемой формуле, если это необходимо.

![Используйте пункт "Перейти к @", чтобы поместить курсор дерева источников данных на элемент, который является родительским по отношению к редактируемому элементу на странице Конструктор формул.](./media/er_formula-designer-data-sources-navigator.gif)

### <a name="data-sources-picker"></a>Средство выбора источников данных

На странице **Конструктор формул** на панели **Источники данных** слева выберите элемент источника данных, который необходимо перенести в изменяемую формулу. Затем выберите **Добавить источник данных**. Обратите внимание, что выбранный элемент добавляется в текст редактируемой формулы.

> [!TIP]
> При использовании параметра **Добавить источник данных** в редакторе формул по умолчанию выбранный элемент всегда добавляется в конец текста формулы. При выполнении той же задачи в [Расширенном редакторе формул](er-advanced-formula-editor.md) выбранный элемент вставляется в текст формулы в текущей позиции курсора.

### <a name="built-in-functions-picker"></a>Средство выбора встроенных функций

На странице **Конструктор формул** на панели **Функции** справа выберите встроенную функцию ER, которую необходимо перенести в изменяемую формулу. Затем выберите **Добавить функцию**. Обратите внимание, что выбранная функция добавляется в текст редактируемой формулы.

> [!TIP]
> При использовании параметра **Добавить функцию** в редакторе формул по умолчанию выбранная функция всегда добавляется в конец текста формулы. При выполнении той же задачи в [Расширенном редакторе формул](er-advanced-formula-editor.md) выбранная функция вставляется в текст формулы в текущей позиции курсора.

### <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Проверка настроенных формул

На странице **конструктора формул** выберите **Тест**, чтобы проверить, как работает настроенная формула.

[![Выбор теста для проверки формулы.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

При необходимости значений аргументов формулы можно открыть диалоговое окно **Тест выражения** на странице **Конструктор формул**. В большинстве случаев эти аргументы должны быть определены вручную, так как настроенные привязки не запускались во время разработки. На вкладке **Результаты проверки** на странице **Конструктор формулы** показан результат выполнения настроенной формулы.

В следующем примере показано, как можно протестировать формулу, настроенную для домена внешней торговли, чтобы убедиться, что товарный код Интрастат содержит только цифры.

При тестировании этой формулы можно использовать диалоговое окно **Тест выражения** для указания значения товарного кода Интрастат для тестирования.

[![Определение товарного кода Интрастат для тестирования.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

После указания товарного кода Интрастат и выбора **OK** на вкладке **Результат проверки** на странице конструктора **Конструктор формул** отображается результат выполнения настроенной формулы. Затем можно оценить, является ли результат приемлемым. Если результат неприемлем, можно обновить формулу и протестировать ее снова.

[![Результаты проверки.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Некоторые формулы не могут быть протестированы во время разработки. Например, формула может вернуть результат типа данных, который не может быть отображен на вкладке **Результат проверки**. В этом случае вы получаете сообщение об ошибке, в котором говорится, что формула не может быть протестирована.

[![Сообщение об ошибке.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор электронной отчетности](general-electronic-reporting.md)
- [Язык формул электронной отчетности](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
