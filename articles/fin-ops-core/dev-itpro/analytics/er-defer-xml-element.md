---
title: Отложить выполнение элементов XML в форматах ER
description: В этой теме объясняется, как отложить выполнение элемента XML в формате электронной отчетности (ER).
author: NickSelin
manager: kfend
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: e9f6161186d04b690ee560dac7ee12974d070506
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015365"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>Отложить выполнение элементов XML в форматах ER

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a>Обзор

Можно использовать конструктор Operations структуры [Электронная отчетность (ER)](general-electronic-reporting.md), чтобы [настроить](./tasks/er-format-configuration-2016-11.md) [компонент форматирования](general-electronic-reporting.md#FormatComponentOutbound) решения ER, используемого для создания исходящих документов в формате XML. Иерархическая структура сконфигурированного компонента форматирования состоит из элементов форматирования различных типов. Эти элементы форматирования используются для заполнения созданных документов необходимой информацией во время выполнения. По умолчанию при выполнении формата ER элементы форматирования выполняются в том же порядке, в котором они представлены в иерархии форматов: один за одним, начиная с верхнего и до нижнего. Однако во время разработки можно изменить порядок выполнения для всех элементов XML сконфигурированного компонента форматирования.

При включении параметра <a name="DeferredXmlElementExecution"></a>**Отложенное выполнение** для элемента XML в настроенном формате можно отложить выполнение этого элемента. В этом случае элемент не выполняется, пока не будут запущены все остальные элементы его родительского элемента.

Чтобы получить дополнительные сведения об этой функции, выполните пример в этой теме.

## <a name="limitations"></a>Ограничения

Параметр **Отложенное выполнение** поддерживается только для элементов XML, настроенных для формата ER, который используется для создания **исходящих** документов в формате XML.

Параметр **Отложенное выполнение** поддерживается только для XML-элементов, которые находятся только в одном другом XML-элементе. Таким образом, он не применяется к XML-элементам, расположенным в других типах элементов форматирования (например, в элементе **XML-последовательности**).

Параметр **Отложенное выполнение** не поддерживается для XML-элементов, которые находятся в элементе формата **Общий\\Файл**, когда для параметра **Файла разбиения** установлено значение **Да**. Дополнительные сведения о разбиении файлов XML см. [Разбиение созданных XML-файлов по их размеру и количеству содержимого](er-split-files.md).

## <a name="Example"></a>Пример: отложить выполнение элемента XML в формате ER

Следующие шаги описывают, как пользователь [с ролью](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) системного администратора или консультанта по функциональным возможностям электронной отчетности может настроить формат ER, содержащий элемент XML, отличающийся от порядка в иерархии форматов.

Эти шаги можно выполнить в компании **USMF** в Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Необходимые условия

Чтобы выполнить пример в этом разделе, необходимо иметь доступ к компании **USMF** в Finance для одной из следующих ролей:

- Консультант по функциональным возможностям электронной отчетности
- Системный администратор

Если вы еще не завершили пример в теме [Отложить выполнение элементов XML в форматах ER](er-defer-sequence-element.md#Example), загрузите следующие [конфигурации](general-electronic-reporting.md#Configuration) примера решения ER.

| Описание содержания            | Имя файла |
|--------------------------------|-----------|
| Конфигурации модели данных электронной отчетности    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Конфигурация сопоставления модели ER | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Прежде чем начать, необходимо загрузить и сохранить следующую конфигурацию примера решения ER на свой локальный компьютер.

| Описание содержания     | Имя файла |
|-------------------------|-----------|
| Конфигурация формата электронной отчетности | [Format to learn deferred XML elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>Импорт примера конфигураций электронной отчетности

1. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
2. Выберите **Конфигурации отчетности**.
3. На странице **Конфигурации**, если конфигурация **Модель для изучения отложенных элементов** недоступна в дереве конфигурации, импортируйте конфигурацию модели данных ER:

    1. Выберите **Обмен**, а затем выберите **Загрузить из XML-файла**.
    2. Выберите **Обзор**, найдите и выберите файл **Model to learn deferred elements.1.xml**, а затем нажмите **ОК**.

4. Если конфигурация **Сопоставление для изучения отложенных элементов** недоступна в дереве конфигурации, импортируйте конфигурацию сопоставления модели ER:

    1. Выберите **Обмен**, а затем выберите **Загрузить из XML-файла**.
    2. Выберите **Обзор**, найдите и выберите файл **Mapping to learn deferred elements.1.1.xml**, а затем нажмите **ОК**.

5. Импорт конфигурации формата ER:

    1. Выберите **Обмен**, а затем выберите **Загрузить из XML-файла**.
    2. Выберите **Обзор**, найдите и выберите файл **Format to learn deferred XML elements.1.1.xml**, а затем нажмите **ОК**.

6. В дереве конфигурации раскройте **Модель для изучения отложенных элементов**.
7. Просмотрите список импортированных конфигураций ER в дереве конфигурации.

    ![Импортированные конфигурации ER на странице конфигурации](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Активация поставщика конфигураций

1. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
2. На странице **Конфигурации локализации** в разделе **Поставщики конфигурации** убедитесь, что [поставщик конфигурации](general-electronic-reporting.md#Provider) для демонстрационной компании Litware, Inc. (`http://www.litware.com`) и помечен как "Активный". Если этого поставщика конфигурации нет в списке или он не помечен как активный, следуйте указаниям в теме [Создание поставщика конфигурации и пометка его как активного](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Демонстрационная компания Litware, Inc. на странице конфигураций локализации](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Просмотр импортированного сопоставления модели

Просмотрите настройки компонента сопоставления модели ER, настроенного для доступа к налоговым проводкам, и предоставьте доступ к данным по запросу.

1. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
2. Выберите **Конфигурации отчетности**.
3. На странице **Конфигурации** в дереве конфигураций разверните **Модель для изучения отложенных элементов**.
4. Выберите конфигурацию **Сопоставление для изучения отложенных элементов**.
5. Выберите **конструктор**, чтобы открыть список сопоставлений.
6. Выберите **конструктор**, чтобы просмотреть сведения о сопоставлении.
7. Выберите **Показать сведения**.
8. Просмотрите источники данных, которые настроены для доступа к налоговым проводкам:

    - Источник данных **Проводки** типа *Табличная запись* настроен на доступ к записям таблицы приложений **TaxTrans**.
    - Источник данных **Ваучеры** типа *Вычисляемое поле* настраивается так, чтобы в качестве списка записей возвращались требуемые коды ваучеров (**INV-10000349** и **INV-10000350**).
    - В источнике данных **Отфильтровано** для типа *Вычисляемое поле* настраивается выбор из источника данных **Проводки** только налоговых проводок по необходимым ваучерам.
    - Поле **\$TaxAmount** типа *Вычисляемое поле* добавляется для источника данных **Отфильтровано**, чтобы предоставить значение налога с противоположным знаком.
    - Источник данных **Сгруппировано** типа *Группа по* настроен для группирования отфильтрованных налоговых проводок по источнику данных **Отфильтровано**.
    - Поле агрегирования **TotalSum** для источника данных **Сгруппировано** настраивается для суммирования значений поля **\$TaxAmount** источника данных **Отфильтровано** для всех фильтруемых налоговых проводок этого источника данных.

        ![Поле агрегирования TotalSum на странице изменение параметров изменения "GroupBy"](./media/ER-DeferredXml-GroupByParameters.png)

9. Проверьте, как настроенные источники данных привязаны к модели данных и как они предоставляют доступ к данным, чтобы сделать их доступными в формате ER:

    - Источник данных **Отфильтровано** связан с полем **Data.List** модели данных.
    - Поле **\$TaxAmount** источника данных **Отфильтровано** связан с полем **Data.List.Value** модели данных.
    - Поле **TotalSum** источника данных **Сгруппировано** связано с полем **Data.Summary.Total** модели данных.

    ![Страница конструктора сопоставления модели](./media/ER-DeferredXml-ModelMapping.png)

10. Закройте страницы **Конструктор сопоставления моделей** и **Сопоставления моделей**.

### <a name="review-the-imported-format"></a>Просмотр импортированного формата

1. На странице **Конфигурации** в дереве конфигурации выберите конфигурацию **Формат для изучения отложенных элементов XML**.
2. Выберите **конструктор**, чтобы просмотреть сведения о формате.
3. Выберите **Показать сведения**.
4. Проверьте настройки компонентов формата ER, настроенные для создания исходящего документа в формате XML, который включает в себя подробные сведения о налоговых проводках:

    - Элемент XML **Отчет\\Сообщение** настроен для заполнения исходящего документа одним узлом,содержащим вложенные XML-элементы (**Заголовок**, **Запись** и **Сводка**).
    - Элемент формата XML **Отчет\\Сообщение\\Заголовок** настроен для заполнения исходящего документа одним узлом заголовка, в котором отображаются дата и время начала обработки.
    - Элемент формата XML **Отчет \\Сообщение\\Запись** настроен для заполнения исходящего документа одним узлом записи, отображающей сведения об отдельных налоговых проводках.
    - Элемент XML **Отчет\\Сообщение\\Сводка** настроен для заполнения исходящего документа одним узлом сводки, который включает сумму налоговых значений из обработанных налоговых проводок.

    ![Элемент XML сообщения и вложенные элементы XML на странице конструктора формата](./media/ER-DeferredXml-Format.png)

5. На вкладке **Сопоставление** изучите следующие сведения.

    - Элемент **Отчет\\Сообщение\\Заголовок** необязательно должен быть привязан к источнику для создания отдельного узла исходящего документа.
    - Атрибут **ExecutionDateTime** генерирует дату и время (включая миллисекунды) при добавлении узла заголовка.
    - Элемент **Отчет\\Сообщение\\Запись** привязан к **model.Data.List** для создания отдельного узла записи для каждой записи из связанного списка.
    - Атрибут **TaxAmount** привязан к **model.Data.List.Value** (который отображается как **\@.Value** в представлении относительного пути) для создания значения налога текущей налоговой проводки.
    - Атрибут **RunningTotal** является заполнителем для итоговых значений налога. В данный момент этот атрибут не имеет выходных данных, так как для него не настроена ни привязка, ни значение по умолчанию.
    - Атрибут **ExecutionDateTime** генерирует дату и время (включая миллисекунды), когда текущая транзакция обрабатывается в этом отчете.
    - Элемент **Отчет\\Сообщение\\Сводка** необязательно должен быть привязан к источнику данных для создания отдельного узла исходящего документа.
    - Атрибут **TotalTaxAmount** привязан к **model.Data.Summary.Total** для создания суммы налоговых значений обработанных налоговых проводок.
    - Атрибут **ExecutionDateTime** генерирует дату и время (включая миллисекунды) при добавлении узла сводки.

    ![Вкладка сопоставления на странице конструктора формата](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Запуск импортированного формата

1. На странице **Конструктор формата** выберите **Выполнить**.
2. Загрузите файл, предлагаемый веб-браузером, и откройте его для просмотра.

    ![Загруженный файл](./media/ER-DeferredXml-Run.png)

Обратите внимание, что в узле сводки указана сумма значений налога для обработанных проводок. Так как формат настроен на использование привязки **model.Data.Summary.Total** для возврата этой суммы, сумма вычисляется путем вызова агрегирования **TotalSum** источника данных **Сгруппировано** типа *GroupBy*, который использует сопоставление модели. Чтобы рассчитать это агрегирование, сопоставление модели выполняет итерации по всем проводкам, выбранным в источнике данных **Отфильтровано**. Сравнивая время выполнения узла сводки и последнего узла записи, можно определить, что расчет суммы занял 12 миллисекунд (мс). Сравнивая время выполнения первого и последнего узлов записи, можно определить, что создание всех узлов записи заняло 9 мс. Таким образом, потребовалось всего 21 мс.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Измените формат так, чтобы расчет основывался на созданных выходных данных

Если объем проводки значительно превышает объем в текущем примере, время расчета может увеличиться и вызвать снижение производительности. Изменяя настройку формата, можно помочь предотвратить эти проблемы в производительности системы. Так как для их включения в создаваемый отчет необходимо получить доступ к налоговым значениям, эти сведения можно повторно использовать для расчета значений налога. Дополнительные сведения см. в разделе [Настройка формата для инвентаризации и суммирования](./tasks/er-format-counting-summing-1.md).

1. На странице **Конструктор форматов** на вкладке **Формат** выберите элемент файла **Отчет** в дереве форматов.
2. Установите для параметра **Сбор сведений о результате** значение **Да**. Теперь можно настроить этот формат с помощью содержимого созданного отчета в качестве источника данных, к которому можно получить доступ с помощью встроенных функций ER в категории [Сбор данных](er-functions-category-data-collection.md).
3. На вкладке **Сопоставление** выберите элемент XML **Отчет\\Сообщение\\Запись**.
4. Настройте выражение **Имя ключа собранных данных** как `WsColumn`.
5. Настройте выражение **Значение ключа собранных данных** как `WsRow`.

    ![Элемент XML "Запись" на странице конструктора формата](./media/ER-DeferredXml-Format3.png)

6. Выберите атрибут **Отчет\\Сообщение\\Запись\\TaxAmount**.
7. Настройте выражение **Имя ключа собранных данных** как `SummingAmountKey`.

    ![Атрибут TaxAmount на странице конструктора формата](./media/ER-DeferredXml-Format4.png)

    Можно рассмотреть этот параметр, чтобы задать выполнение виртуального листа, где значение ячейки A1 добавляется к значению суммы налога из каждой обработанной налоговой проводки.

8. Выберите атрибут **Отчет\\Сообщение\\Запись\\RunningTotal**, а затем выберите **Изменить формулу**.
9. Настройте выражение `SUMIF(SummingAmountKey, WsColumn, WsRow)` с помощью встроенной функции [ER SUMIF](er-functions-datacollection-sumif.md) и выберите **Сохранить**.

    ![Выражение SUMIF](./media/ER-DeferredXml-FormulaDesigner.png)

10. Закройте страницу **Конструктор формул**.
11. Выберите **Сохранить**, затем выберите **Выполнить**.
12. Загрузите и просмотрите файл, предлагаемый веб-браузером.

    ![Загруженный файл](./media/ER-DeferredXml-Run1.png)

    Последний узел записи содержит нарастающую сумму значений налогов, которая рассчитывается для всех обработанных проводок, используя созданные выходные данные в качестве источника данных. Этот источник данных начинается с начала отчета и продолжается до последней налоговой проводки. Узел сводки содержит сумму налоговых значений для всех обработанных проводок, которые рассчитываются в сопоставлении моделей, используя источник данных типа *GroupBy*. Обратите внимание, что эти значения равны. Таким образом, вместо **GroupBy** можно использовать суммирование на основе выходных данных. Сравнивая время выполнения первого узла записи и узла сводки, можно определить, что создание всех узлов записи и суммирование заняло 11 мс. Таким образом, после создания узлов записей и суммирования значений налога измененный формат будет примерно в два раза быстрее, чем исходный формат.

13. Выберите атрибут **Отчет\\Сообщение\\Сводка\\TotalTaxAmount**, а затем выберите **Изменить формулу**.
14. Введите выражение `SUMIF(SummingAmountKey, WsColumn, WsRow)` вместо существующего выражения.
15. Выберите **Сохранить**, затем выберите **Выполнить**.
16. Загрузите и просмотрите файл, предлагаемый веб-браузером.

    ![Загруженный файл](./media/ER-DeferredXml-Run2.png)

    Обратите внимание, что нарастающее итоговое значение налога в последнем узле записи теперь равно сумме в узле сводки.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Помещайте в заголовок отчета значения суммирования, основанные на выходных данных

Если, например, необходимо представить сумму значений налога в заголовке отчета, можно изменить формат.

1. На странице **Конструктор форматов** на вкладке **Формат** выберите элемент последовательности **Отчет\\Сообщение\\Элемент XML**.
2. Выберите **Переместить вверх**.
3. Выберите **Сохранить**, затем выберите **Выполнить**.
4. Загрузите и просмотрите файл, предлагаемый веб-браузером.

    ![Загруженный файл](./media/ER-DeferredXml-Run3.png)

    Обратите внимание на то, что сумма налоговых значений в узле сводки в данном случае равняется 0 (нулю), поскольку эта сумма будет вычисляться на основе созданных выходных данных. Когда создается первый узел записи, созданные выходные данные еще не содержат узлы записи со сведениями о проводке. Этот формат можно настроить, чтобы отложить выполнение элемента последовательности **Отчет\\Сообщение\\Сводка**, пока не будет выполнен элемент **Отчет\\Сообщение\\Запись** для всех налоговых проводок.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Отсрочка выполнения элемента XML сводки для использования рассчитанного итогового значения

1. На странице **Конструктор форматов** на вкладке **Формат** выберите элемент последовательности **Отчет\\Сообщение\\Элемент XML**.
2. Для параметра **Отложенное выполнение** выберите значение **Да**.

    ![Параметр отложенного выполнения элемента XML сводки на странице конструктора формата](./media/ER-DeferredXml-Format5.png)

3. Выберите **Сохранить**, затем выберите **Выполнить**.
4. Загрузите и просмотрите файл, предлагаемый веб-браузером.

    ![Загруженный файл](./media/ER-DeferredXml-Run4.png)

    Элемент **Отчет\\Сообщение\\Сводка** выполняется только после того, как все остальные элементы, вложенные в родительский элемент, **Отчет\\Сообщение**, были выполнены. Поэтому он выполняется после того, как элемент **Отчет\\Сообщение\\Запись** был выполнен для всех налоговых проводок источника данных **model.Data.List**. Значения времени выполнения первого и последнего узлов записей и узлов заголовка и сводки подтверждают этот факт.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Настройка формата для инвентаризации и суммирования](./tasks/er-format-counting-summing-1.md)
- [Трассировка выполнения формата электронной отчетности для устранения проблем с производительностью](trace-execution-er-troubleshoot-perf.md)
- [Отложить выполнение элементов последовательности в форматах ER](er-defer-sequence-element.md#Example)