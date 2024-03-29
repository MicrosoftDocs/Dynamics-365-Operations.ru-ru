---
title: Финансовая отчетность (Россия)
description: В этой статье содержится информация о финансовой отчетности для России.
author: AdamTrukawka
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2d6f32f08dec7f2352f2bc6ddbce27985c9bbccb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275867"
---
# <a name="financial-reporting-russia"></a>Финансовая отчетность (Россия)

[!include [banner](../includes/banner.md)]

Можно настроить финансовые отчеты, такие как балансовый отчет или любой другой отчет, в котором отчетные суммы представляются в ячейках. 

Следует определить список отчетов и ячейки отчетов. Для каждой ячейки отчета следует определить правила сбора данных на основе проводок главной книги, бюджетных проводок и регистров налога на прибыль. 

В электронной отчетности (ER) необходимо настроить выходные данные отчета, чтобы конфигурация ER использовала данные, рассчитанные для настроенного финансового отчета и создавала выходной файл согласно конфигурации формата (например, Microsoft Excel или XML).

Необходимо также настроить обработку электронных сообщений, чтобы один шаг позволял авторизованным пользователем выполнять конфигурацию ER для финансового отчета, создавать отчет и сохранять данных созданного отчета.

## <a name="set-up-financial-reports"></a>Настройка финансовых отчетов

Для настройки финансовых отчетов выполните следующие задачи:

1. Настройте имена отчетов.
2. Настройте ячейки отчета.
3. Настройте правила расчета для ячеек отчета.

### <a name="set-up-report-names"></a>Настройка имен отчетов
1. Выберите **Главная книга \> Настройка финансовых отчетов \> Финансовые отчеты**, чтобы открыть страницу **Отчеты**. На вкладке **Обзор** отображается список всех отчетов, настроенных в системе.
2. Создайте отчет и введите имя и описание для него.
3. Выберите вкладку **Общие**, которая отображает общие параметры для создания отчетов. 
4. В поле **Валюта** выберите **Базовая валюта**, если данные в отчете должны быть представлены в валюте компании по умолчанию. Если данные должны быть представлены в валюте отчетности, выберите **Валюта отчетности**. Также можно указать валюту для каждой ячейки отдельно.
5. В поле **Период** выберите период по умолчанию, для которого должны рассчитываться проводки. Данные в отчете будут рассчитываться для выбранного периода на основе даты, указанной при выполнении отчета.
6. В поле **Тип строки** выберите источник данных по умолчанию для отчета. Доступны следующие значения.

    | Tип строки | описание |
    |-----------|-------------|
    | Транзакции | В отчете отображаются данные из разнесенных проводок для счетов ГК. Если выбрано это значение, выберите значение в поле **Учитывать проводки**, чтобы определить, как отмена операций должна использоваться для расчетов. Доступны варианты: **Все**, **Только сторно** и **Без учета сторно**. |
    | Бюджет | В отчете отображаются данные из записей бюджета для счетов ГК. Если выбрано это значение, выберите бюджетную модель по умолчанию в поле **Бюджетная модель**. |
    | Зарегистрировать | В отчете отображаются данные из рассчитанных регистров налога на прибыль. |
    | Константа | В отчете отображаются значения определенных констант для ячеек. |
    | Подрядчик | В отчете отображаются данные из активных/пассивных сальдо подрядчиков. |
    | Сальдо набора аналитик | В отчете отображаются сальдо для выбранного набора аналитик. Если выбрано это значение, выберите набор финансовых аналитик по умолчанию в поле **Набор аналитик**. |

7. В поле **Коэффициент** введите значение, на которое необходимо разделить данные отчета. 

    Например, если данные в отчете должны быть представлена в тысячах рублей, введите **1000**. Если данные должны быть представлена в полных рублях, введите **1**.

8. Выберите вкладку **Тип проводки**, на которой отображается список типов проводок, которые будут учитываться в расчетах. 
9. Создайте строку. В поле **Тип проводки** выберите тип проводки, который должен включать отчет. Проводки из соответствующего модуля будет использоваться для создания отчета. Создайте строку для каждого типа проводки, который требуется.

    Например, если выбрать **Банк** как тип проводки, в отчет будут включены проводки, которые созданы из модуля **Банковские операции**. Если не создать никакие строки, не будет использоваться фильтр. 

10. Выберите вкладку **Слой разноски**, на которой отображается список слоев проводок, которые будут учитываться в расчетах. Если не создать никакие строки, не будет использоваться фильтр.
11. Выберите вкладку **Финансовые аналитики**, которая показывает фильтры аналитик, если отчет должен быть создан только для определенных значений финансовой аналитики, но не для всех значений.
12. Создайте строку. В поле **Ссылка** выберите имя аналитики.
13. В полях **От** и **До** задайте диапазон аналитик, которые необходимо учитывать в расчетах. Создайте строку для каждого диапазона аналитик, который требуется. Если не создать никакие строки, не будет использоваться фильтр.

### <a name="set-up-report-cells"></a>Настройка ячеек отчета

Можно настроить ячейки отчета вручную или путем копирования их из другого отчета. 

#### <a name="copy-financial-reports-settings"></a>Копирование параметров финансовых отчетов

1. На странице **Отчеты** выберите **Копировать**, чтобы открыть диалоговое окно **Копирование настроек отчета в новый отчет**.
2. В разделе **Исходный отчет** в поле **Организация** выберите организацию для копирования. В поле **Код отчета** выберите код отчета для копирования.
3. В разделе **Целевой отчет** в поле **Код отчета** выберите код отчета для копирования в него настроек или введите новый код отчета. Если параметры уже указаны для целевого отчета, они будут перезаписаны.

#### <a name="manually-create-report-cells"></a>Создание ячеек отчета вручную
1. На странице **Отчеты** выберите **Настройка**, чтобы открыть страницу **Настройка реквизитов**. В верхней области отображается список ячеек отчета и их основные параметры.

    ![Настройка ячеек отчета.](media/cells-setup.jpg)

2. В верхней области создайте строку. В поле **Код** введите уникальный код для ячейки отчета.

    Можно настроить любое требуемое соглашение об именах для идентификаторов, но имя каждой ячейки в одном отчете должно быть уникальным. Конфигурации электронной отчетности, настроенная для вывода отчета, должна фильтровать список значений отчета по кодам ячеек в привязке между значениями отчета и элементов форматирования.

    > [!TIP]
    > Например, можно использовать объединение имен тегов XML из официального электронного формата отчета. 

3. Введите описание строки.

Вкладки в верхней области, а также поля на каждой вкладке совпадают с вкладками и полями на странице **Отчеты**. Значения, введенные для ячейки отчета на странице **Настройка реквизитов**, заменяют значения, введенные для отчета на странице **Отчеты**.

### <a name="set-up-calculation-rules-for-report-cells"></a>Настройка правил расчета для ячеек отчета

Используйте следующую процедуру, чтобы создать операции для ячеек отчета.

1. На странице **Отчеты** выберите **Настройка**, чтобы открыть страницу **Настройка реквизитов**.
2. В верхней области выберите строку для ячейки отчета или создайте строку. Затем на нижней панели выберите **Добавить**, чтобы создать новую строку.

    Для каждой ячейки отчета можно настроить одну или несколько строк, которые содержат параметры для расчета сумм. Эти строки связаны математическими операторами.

    ![Настройка операций для ячеек отчета.](media/cells-setup-operations.jpg)

3. В поле **Оператор** выберите математический оператор, который должен применяться к значению ячейки.

    > [!NOTE] 
    > Поле **Оператор** указывает математический знак для суммы, которая рассчитывается для ячейки. Математический знак также используется при настройке многострочных операций. Обычно ваучеры типов **Сальдо по кредиту**, **Обороты по кредиту** или **Оборот в корреспонденции кредит** должны использовать знак "минус" (–).

4. В поле **Тип строки** выберите источник данных, используемый для расчета выбранной строки. По умолчанию используется значение из настройки ячейки. Однако это значение можно изменить. Доступны следующие типы строк.

    | Tип строки | Иcточник данных | Доступный тип операции |
    |-----------|-------------|-----------------------------|
    | Транзакции | Проводки ГК | Сальдо, Сальдо кредит, Сальдо дебет, Оборот, Обороты по кредиту, Обороты по дебету, Оборот в корреспонденции, Оборот в корреспонденции кредит, Оборот в корреспонденции дебет, Активное сальдо (дебет) и Пассивное сальдо (кредит) |
    | Бюджет | Бюджетные проводки | Сальдо, Сальдо кредит, Сальдо дебет, Оборот, Обороты по кредиту и Обороты по дебету |
    | Зарегистрировать | Значение, указанное в поле **Поле регистра** на вкладке **Регистры налогового учета** |
    | Константа | Значение, указанное в поле **Постоянное значение** операций ячейки | |
    | Подрядчик | Проводки ГК, связанные с подрядчиками | Активное сальдо (дебет) и пассивное сальдо (кредит). Значения сальдо рассчитываются для аналитического уровня (**Документ**, **Соглашение** или **Подрядчик**), который указан в поле **Детализация сальдо** на вкладке **Общие**. |
    | Сальдо набора аналитик | | |

5. Если выбрано значение **Проводки**, **Бюджет** или **Подрядчик** в поле **Тип строки**, выберите тип операции в поле **Тип операции**. Доступны следующие значения.

    <table>
    <thead>
    <tr>
    <th>Тип операции</th>
    <th>Алгоритм расчета</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Баланс</td>
    <td>Сумма по проводке для счета ГК на дату</td>
    </tr>
    <tr>
    <td>Сальдо кредит</td>
    <td>Сумма проводки по кредиту для счета ГК на дату</td>
    </tr>
    <tr>
    <td>Сальдо дебет</td>
    <td>Сумма проводки по дебету для счета ГК на дату</td>
    </tr>
    <tr>
    <td>Товарооборот</td>
    <td>Сумма проводки для счета ГК за период</td>
    </tr>
    <tr>
    <td>Обороты по кредиту</td>
    <td>Сумма проводки по кредиту для счета ГК за период</td>
    </tr>
    <tr>
    <td>Обороты по дебету</td>
    <td>Сумма проводки по дебету для счета ГК за период</td>
    </tr>
    <tr>
    <td>Оборот в корреспонденции (только для типа строки <strong>Проводки</strong>)</td>
    <td>Сумма проводки для счета ГК в корреспонденции с другими счетами ГК за период</td>
    </tr>
    <tr>
    <td>Оборот в корреспонденции кредит (только для типа строки <strong>Проводки</strong>)</td>
    <td>Сумма проводки по кредиту для счета ГК в корреспонденции с другими счетами ГК за период</td>
    </tr>
    <tr>
    <td>Оборот в корреспонденции дебет (только для типа строки <strong>Проводки</strong>)</td>
    <td>Сумма проводки по дебету для счета ГК в корреспонденции с другими счетами ГК за период</td>
    </tr>
    <tr>
    <td>Активное сальдо (дебет) (только для типов строки <strong>Проводки</strong> и <strong>Подрядчик</strong>)</td>
    <td>Алгоритм расчета зависит от типа строки: <ul>
    <li><strong>Проводки:</strong> во-первых, сальдо для счета главной книги рассчитываются для всех комбинаций финансовых аналитик. Во-вторых, дебетовые сальдо для каждой комбинации аналитик суммируются. Полученное значение является значением ячейки.</li>
    <li><strong>Подрядчик:</strong> активное сальдо для счета ГК рассчитывается по клиенту, контракту или документу.</li>
    </ul></td>
    </tr>
    <tr>
    <td>Пассивное сальдо (кредит) (только для типов строки <strong>Проводки</strong> и <strong>Подрядчик</strong>)</td>
    <td>Алгоритм расчета зависит от типа строки: <ul>
    <li><strong>Проводки:</strong> во-первых, сальдо для счета главной книги рассчитываются для всех комбинаций финансовых аналитик. Во-вторых, кредитные сальдо для каждой комбинации аналитик суммируются. Полученное значение является значением ячейки.</li>
    <li><strong>Подрядчик:</strong> пассивное сальдо для счета ГК рассчитывается по контрагенту, контракту или документу.</td>
    </tr>
    </tbody>
    </table>

6. Если выбрано значение **Сальдо**, **Сальдо кредит**, **Сальдо дебет**, **Активное сальдо (дебет)** или **Пассивное сальдо (кредит)** в поле **Тип операции**, выберите тип сальдо в поле **Тип сальдо**: **Входящее** или **Исходящее**.
7. В поле **Счет/интервал** выберите **Счет** для настройки одного счета главной книги для операции. Чтобы настроить диапазон счетов ГК, выберите **Интервал**.
8. Выполните одно из следующих действий в зависимости от значения, выбранного в поле **Счет/интервал**.

    - Если вы выбрали **Счет**, укажите счет ГК в поле **Счет**.
    - Если вы выбрали **Интервал**, выберите **Настройка \> Диапазон счетов**. Создайте строку, затем на вкладке **Диапазон счетов** в полях **От** и **До** выберите первый и последний номера счетов ГК, которые должны использоваться в расчете.

9. В поле **Корр. счет/интервал** выберите **Счет** для настройки одного счета главной книги для операции. Чтобы настроить диапазон счетов ГК, выберите **Интервал**.
10. Выполните одно из следующих действий в зависимости от значения, выбранного в поле **Корр. счет/интервал**.

    - Если вы выбрали **Счет**, укажите счет ГК в поле **Корр. счет**.
    - Если вы выбрали **Интервал**, выберите **Настройка \> Диапазон счетов**. Создайте строку, затем на вкладке **Диапазон корр. счетов** в полях **От** и **До** выберите первый и последний номера счетов ГК, которые должны использоваться в расчете.

11. Если на шаге 4 выбрано значение **Подрядчик** в поле **Тип строки**, на вкладке **Общие** в поле **Детализация сальдо** выберите аналитический уровень, для которого должно рассчитываться активное или пассивное сальдо для подрядчика: **Документ**, **Соглашение** или **Подрядчик**.
12. Если выбрано значение **Регистр** в поле **Тип строки**, выполните следующие действия:

    1. На вкладке **Налоговые регистры** в поле **Код регистра** выберите код регистра налога на прибыль. Затем в поле **Поле регистра** выберите имя поля регистра. Данные из выбранного поля регистра будут учитываться в расчете.
    2. Необязательно: в поле **Счет/интервал** выберите **Счет** для настройки расчета налогового регистра для одного кода расходов. Затем в поле **Счет** выберите код расхода. Можно также выбрать значение **Интервал**, чтобы настроить расчет для диапазона кодов расходов. Затем выберите **Настройка \> Диапазон счетов** и укажите интервал кодов расходов.

13. Необязательно: вкладки **Общие**, **Слой разноски** и **Финансовые аналитики** содержат те же поля, что и соответствующие вкладки в верхней области страниц **Настройка реквизитов** и **Отчеты**. На каждой вкладке задайте значения для строк операций. Значения, введенные для операции, заменяют значения по умолчанию, введенные для ячейки и/или отчета.
14. После завершения создания строк операций можно упорядочить их в нужной последовательности. Выберите строку, затем выберите кнопку **Вверх** или **Вниз**, чтобы переместить ее на одну позицию вверх или вниз.

## <a name="run-the-report"></a>Выполнение отчета
Перед запуском отчета создайте формат электронной отчетности, который будет экспортировать данные, рассчитанные для финансового отчета. Дополнительные сведения о создании формата электронных отчетов в Excel см. в разделе [Настройка финансовых отчетов в Excel](rus-excel-financial-report.md)

1. Выберите **Главная книга > Запросы и отчеты > Финансовые отчеты (Россия)**. 
2. В поле **Сопоставление форматов** выберите созданный формат электронного отчета и затем выберите **ОК**. 
3. В диалоговом окне **Параметры электронной отчетности** заполните необходимые параметры для выполнения отчета: 

      - В поле **Конечная дата** укажите период для выполнения отчета.
      - В поле **Отчет** определите финансовый отчет.
 
  > [!NOTE]
  > Один из параметров — **Дата отчетности**. Это поле используется только в том случае, если выполняется разноска проводок ГК, которые корректируют закрытый финансовый период. Ввод даты отчетности позволяет сообщить о корректирующих проводках в корректирующих отчетах для закрытого периода и исключить корректирующие проводки из текущего отчетного периода.
  >
  > - Если вы создаете корректирующий отчет для закрытых периодов, и настроили поле **Дата отчета**, расчет ячеек в финансовых отчетах учитывает проводки базового периода и более поздние проводки вплоть до даты отчета, которые исправляют базовый период. Дата отчетности в учтенной проводке входит в базовый период.
  > 
  > - Если вы создаете отчет для недавнего периода, и задали поле **Дата отчета**, расчет ячеек в финансовых отчетах учитывает проводки базового (недавнего) периода, но исключает проводки, которые корректируют предыдущие (закрытые) периоды. Дата отчета в учтенной проводке входит в предыдущий закрытый период.

## <a name="run-the-report-from-electronic-messages"></a>Выполнение отчета из электронных сообщений
Дополнительные сведения см. в разделе [Обмен электронными сообщениями](../general-ledger/electronic-messaging.md). Приведенный ниже пример показывает, как настроить электронные сообщения для выполнения конфигурации электронной отчетности для финансовых отчетов.

1. На странице **Статусы сообщения** создайте статусы сообщений, которые применимы к отчету (например, **Создано** и **Сформировано**).
2. На странице **Действие обработки сообщения** создайте следующие действия:

    1. Действие, которое называется **Создать сообщение**, и которое имеет тип **Создать сообщение** и статус результата **Создано**.
    2. Действие, которое называется **Готово к формированию** и имеет тип действия **Пользовательская обработка на уровне сообщения** и статусом результата **Готово к формированию**.
    3. Действие, которое называется **Создать отчет** и имеет тип действия **Сообщение экспорта электронной отчетности**, исходный статус **Создано** и статус результата **Сформировано**. Для этого действия задайте следующие дополнительные значения:

        - Задайте для параметра **Показать диалоговое окно** значение **Да**.
        - В поле **Сопоставление формата** выберите формат электронной отчетности, созданный ранее. 
        - В поле **Имя файла** определите имя по умолчанию для созданного файла.

    ![Действия обработки сообщения.](media/message-processing-action.jpg)

4. На странице **Обработка электронного сообщения** определите поток обработки для отчета.

    Например, определить обработку, которая состоит из трех ранее созданных действий: Создать сообщение, Готово для формирования и Создать отчет.

5. На странице **Электронные сообщения** выберите обработку, которую вы создали на предыдущем шаге.
6. Выберите **Создать**, чтобы создать сообщение. 
7. В полях **Дата начала** и **Дата окончания** укажите даты периода отчетности.
8. Обновите статус до **Готово к формированию**.

    ![Электронные сообщения.](media/electronic-messages.jpg)

9. Выберите **Создать отчет** для выполнения формата электронной отчетности для финансового отчета.
10. Если появится запрос, введите параметры пользователя в диалоговом окне.
11. Просмотрите созданный файл в области **Вложения**.

Дополнительные сведения о том, как выполнять отчет из электронных сообщений с помощью бухгалтерской отчетности см. в разделе [Бухгалтерская отчетность в электронном формате](rus-accounting-reporting.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
