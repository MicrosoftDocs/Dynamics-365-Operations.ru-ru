---
title: Подавлять элементы управления содержимым Word в сформированных отчетах
description: В этой статье объясняется, как настроить формат электронной отчетности (ER) для создания отчетов в виде файлов Microsoft Word, в которых подавлены элементы управления содержимым.
author: kfend
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.search.form:
- ERWorkspace, ERSolutionTable, EROperationDesigner
- LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: 8787d43a0c453d49dd1d0efcbb7b5d276721be9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267325"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Подавлять элементы управления содержимым Word в сформированных отчетах

[!include [banner](../includes/banner.md)]

Чтобы создавать отчеты как документы Microsoft Word, необходимо разработать шаблон для отчетов в качестве документа Word. Этот шаблон должен содержать элементы управления содержимым Word в качестве заполнителей для данных, которые будут заполнены во время выполнения. Чтобы использовать документ Word, созданный в качестве шаблона для ваших отчетов, можно [настроить](er-design-configuration-word.md) новое [решение](er-quick-start1-new-solution.md) [электронной отчетности (ER)](general-electronic-reporting.md). Решение должно включать [конфигурацию](general-electronic-reporting.md#Configuration) электронной отчетности, которая содержит компонент формата электронной отчетности. Этот формат электронной отчетности должен быть настроен на использование шаблона, разработанного для создания отчетов.

В версии Dynamics 365 Finance 10.0.6 или более поздней можно настроить формулы в формате электронной отчетности, чтобы подавить некоторые элементы управления содержимым Word в создаваемых документах.

Следующие шаги описывают, как пользователь, назначенный для роли "системный администратор" или "Консультант по функциональным возможностям электронной отчетности", может настроить формат ER, который создает отчеты как файлы Word, и подавляет некоторые элементы управления содержимым в созданных отчетах, которые были настроены с помощью шаблона Word.

Эти шаги можно выполнить в компании GBSI.

## <a name="prerequisites"></a>Необходимые условия

Для выполнения этих действий необходимо сначала выполнить шаги из следующих проводников по задачам:

- [Разработка конфигурации для создания отчетов в формате OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word](./tasks/er-design-configuration-word-2016-11.md)

После выполнения шагов этих проводников по задачам подготавливаются следующие номенклатуры:

- Формат ER **Пример отчета о листе**, настроенный для создания документа в формате Microsoft Word
- Черновая версия **Примера отчета о листе** в формате ER с пометкой **Исполняемая**
- **Электронный** метод платежей, настроенный на использование формата ER **Пример отчета о листе** для обработки платежей поставщикам

Необходимо также загрузить и сохранить следующий шаблон для примера отчета:

- [Связанный шаблон 2 отчета о платежах (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Проверка загруженного шаблона Word

1. В классическом приложении Word откройте файл шаблона **SampleVendPaymDocReportBounded2.docx**, который был загружен ранее.
2. Убедитесь, что файл шаблона содержит раздел "Сводка", в котором показаны итоговые суммы платежа для каждого кода валюты, который был удовлетворен в обработанных платежах.

    - Раздел "Сводка" располагается в отдельной таблице документа Word.
    - Первая строка этой таблицы содержит заголовки столбцов таблицы в качестве заголовка раздела.
    - Во второй строке этой таблицы содержится повторяющийся элемент управления содержимым в качестве сведений о разделе.
    - Этот элемент управления содержимым отображается в поле **SummaryLines** пользовательской XML-части **отчета**.
    - На основе этого сопоставления элемент управления содержимым связывается с элементом **SummaryLines** для редактируемого формата ER.

    > [!NOTE]
    > Повторяющийся элемент управления содержимым помечается ключом **SummaryLines**, совпадающим с полем пользовательской XML-части, которой он сопоставлен.

    ![Макет шаблона Word.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Выбор существующей конфигурации отчета электронной отчетности

Для следующих шагов вы будете повторно использовать существующую конфигурацию ER, которая была настроена при выполнении шагов, описанных ранее в разделе проводников по задачам.

1. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
2. Выберите **Конфигурации отчетности**.
3. На странице **Конфигурации** в дереве конфигураций разверните **Модель платежа**, затем выберите **Пример отчета о листе**.
4. Выберите **конструктор**, чтобы изменить черновую версию выбранного формата ER.

## <a name="replace-the-current-template-with-the-new-template"></a>Замена текущего шаблона на новый шаблон

В настоящее время файл SampleVendPaymDocReportBounded.docx используется как шаблон для создания выходных данных в формате Word. На следующих шагах вы замените этот шаблон Word новым шаблоном Word, SampleVendPaymDocReportBounded2.docx, который загрузили ранее.

1. На странице **Конструктор форматов** выберите **Вложения**.
2. На странице **Вложения** выберите **Удалить**, чтобы удалить существующий шаблон.
3. Выберите **Да**, чтобы подтвердить удаление.
4. Выберите **Создать** \> **Файл**.
5. Выберите **Обзор**, найдите и выберите файл **SampleVendPaymDocReportBounded2.docx**, загруженный ранее.
6. Нажмите **ОК**.
7. Закройте страницу **Вложения**.
8. На странице **Конструктор форматов** в поле **Шаблон** введите или выберите файл **SampleVendPaymDocReportBounded2.docx**.

## <a name="run-the-format-to-create-word-output"></a>Выполните формат для создания выходных данных Word

1. Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.
2. На странице **Платежи поставщикам** на вкладке **Список** выберите все платежи.
3. Выберите **Статус платежа** \> **Нет**.
4. Выберите **Создать платежи**.
5. В поле **Способ оплаты** выберите **Электронный**.
6. В поле **Банковский счет** выберите **GBSI OPER**.
7. Нажмите **ОК**.
8. В диалоговом окне **параметров электронной отчетности** нажмите кнопку **ОК** и проанализируйте созданные выходные данные.

    ![Платежи для обработки на странице платежей поставщикам.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Выходные данные представлены в формате Word и содержат раздел "Сводка".

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Настройка редактируемого формата для подавления раздела сводки

Если необходимо подавлять раздел сводки в созданном документе на основе запроса пользователя, запустившего данный формат ER, необходимо изменить формат файла ER.

1. Перейдите в раздел **Администрирование организации** \> **Рабочие области** \> **Электронная отчетность** и откройте черновую версию формата ER для редактирования.
2. Выберите **Конфигурации отчетности**. 
3. На странице **Конфигурации** в дереве конфигураций разверните **Модель платежа** \> **Пример отчета о листе**.
4. Выберите **Конструктор**.
5. На странице **конструктор форматов** разверните **Word** и выберите **SummaryLines**.
6. На вкладке **Сопоставление** добавьте новый источник данных для запроса пользователю во время выполнения, следует ли подавлять раздел сводки:

    1. Выберите **Добавить корень**.
    2. В диалоговом окне **Добавить источник данных** выберите **Общее\Параметр ввода пользователя**, чтобы открыть диалоговое окно **Свойства источника данных параметра пользовательского ввода**.
    3. В поле **Имя** введите **uipSuppress**.
    4. В поле **Метка** введите **подавление раздела сводки**.
    5. В поле **имя типа данных операций** выберите или введите **NoYes**.
    6. Нажмите **ОК**.

7. Добавить новый источник данных типа перечисления приложения **NoYes**:

    1. Выберите **Добавить корень**.
    2. В диалоговом окне **Добавить источник данных** выберите **Dynamics 365 for Operations\Перечисление**, чтобы открыть диалоговое окно **Свойства источника данных "перечисление"**.
    3. В поле **Имя** введите **enumNoYes**.
    4. В поле **Метка** введите **Параметры подавления**.
    5. В поле **имя типа данных операций** выберите или введите **NoYes**.
    6. Нажмите **ОК**.

8. Для выбранного элемента формата **SummaryLines** настройте формулу, чтобы указать, когда следует подавлять элемент управления содержимым Word, связанный с выбранным элементом форматирования:

    1. На вкладке **Сопоставление** в разделе **Удаленный** выберите **Изменить**, чтобы открыть страницу **[конструктор формул](general-electronic-reporting-formula-designer.md)**.
    2. В поле **Формула** введите формулу `uipSuppress = enumNoYes.Yes`.
    3. Выберите **Сохранить**, затем закройте страницу **Конструктор формул**.

        > [!NOTE]
        > Эта формула будет применена к созданному документу **после запуска всех остальных элементов форматирования**. Чтобы применить эту формулу, в созданном документе найден элемент управления содержимым Word, помеченный как элемент формата, для которого настроена формула (в данном случае **SummaryLines**). Затем этот элемент управления содержимым полностью удаляется вместе со строкой в таблице Word, в которой он содержится. Строка сведений из раздела сводки удаляется из созданного документа.
        >
        > Во время разработки можно настроить формулу **Удаленный** для элемента форматирования, даже если в шаблоне Word нет элемента управления, который используется в качестве тега, совпадающего с именем элемента формата, для которого настроено свойство **Удаленный**. При проверке формата во время разработки появляется [предупреждение](er-components-inspections.md#i14) об этой несогласованности.
        >
        > Во время выполнения создается исключение, если ни один из элементов управления в шаблоне Word не используется в теге, совпадающем с именем элемента формата, для которого настроено свойство **Удаленный**.

    4. На вкладке **Сопоставление** в области **Удаленный** установите для параметра **С родительским** значение **Да**.

        > [!NOTE]
        > Необходимо установить для этого параметра значение **Да**, чтобы удалить всю таблицу слов в качестве родительского объекта строки, содержащей сведения о разделе сводки. Если для этого параметра установить значение **нет**, строка заголовка раздела останется в созданном документе.

9. Для сохранения изменений в изменяемом формате выберите **Сохранить**.

    ![Созданные выходные данные в формате Word.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Выполните измененный формат для создания выходных данных Word

1. Перейдите в раздел **Расчеты с поставщиками** \> **Платежи** \> **Журнал платежей**.
2. Выберите журнал платежей, который был создан, а затем выберите **Строки**.
3. На странице **Платежи поставщикам** выберите все строки, а затем выберите **статус оплаты** \> **нет**.
4. Выберите **Создать платежи**.
5. В поле **Способ оплаты** выберите **Электронный**.
6. В поле **Банковский счет** выберите **GBSI OPER**.
7. Нажмите **ОК**.
8. В диалоговом окне **Параметры электронной отчетности** в поле **подавление раздела сводки** выберите **Да**.
9. Нажмите кнопку **ОК** и проанализируйте созданные выходные данные.

    ![Созданные выходные данные в формате Word.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Обратите внимание, что выходные данные не содержат раздел "Сводка", так как он был подавлен.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Разработка конфигурации для создания отчетов в формате OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [Разработка конфигураций электронной отчетности для создания отчетов в формате Word](er-design-configuration-word.md)
- [Повторное использование конфигураций электронной отчетности с шаблонами Excel для формирования отчетов в формате Word](./tasks/er-design-configuration-word-2016-11.md)
- [Проверка настроенного компонента электронной отчетности для предотвращения неполадок среды выполнения](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
