---
title: Две валюты
description: В этой статье содержатся сведения об учете в двух валютах, когда валюта отчетности используется как вторая валюта учета для Microsoft Dynamics 365 Finance.
author: kweekley
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 19337b2651830d79543361d525bf24c4f794e825
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065757"
---
# <a name="dual-currency"></a>Две валюты

[!include [banner](../includes/banner.md)]

Функциональность, которая была введена в Microsoft Dynamics 365 Finance версии 8.1 (октябрь 2018), позволяет валюту отчетности переназначить и использовать в качестве второй валюты учета. Эта функция называется *две валюты*. Изменения для двух валют не могут быть отключены через конфигурационный ключ или параметр. Так как валюта отчетности используется как вторая валюта учета, изменился способ, которым валюта отчетности вычисляется в логике разноски.

Кроме того улучшены несколько модулей для отслеживания, отчетности и использования валюты отчетности в различных процессах. К этим модулям относятся:

- Главная книга 
- Финансовая отчетность 
- Расчеты с поставщиками
- Расчеты с клиентами 
- Управление банком и кассовыми операциями 
- Основные средства 
- Консолидации

После обновления необходимо выполнить определенные шаги для управления банком и кассовыми операциями и основными средствами. Таким образом, обязательно внимательно прочитайте и изучите соответствующие разделы в этой статье.

## <a name="posting-process"></a>Процесс разноски

Была изменена логика разноски для всех проводок, которые создают запись учета в главной книге. Ниже приведено, как ранее рассчитывалась валюта отчетности:

Сумма в валюте проводки \> Сумма в валюте учета \> Сумма в валюте отчетности

Например, проводка вводится в валюте "канадский доллар" (CAD). Сумма в канадских долларах преобразуется в валюту учета, которой является доллар США (USD). Сумма в долларах США затем преобразуется в валюту учета, которой является Евро (EUR). Таким образом, должны иметься валютные курсы между CAD и USD, а также между USD и EUR.

Новый расчет производится следующим образом:

Суммы в валюте проводки \> Сумма в валюте учета

Суммы в валюте проводки \> Сумма в валюте отчетности

В связи с этим изменением теперь должны иметься валютные курсы между CAD и USD, а также между CAD и EUR.

## <a name="reports-and-inquiries"></a>Отчеты и запросы

В разных отчетах и запросах теперь отображаются как суммы в валюте отчетности, так и суммы в валюте учета. Не все отчеты и запросы были обновлены. Например, отчеты, отображающие суммы только в валюте проводки, не были изменены.

Изменения следуют одной из двух схем:

- Если отчет или запрос имеет достаточно места для отображения сумм как в валюте учета, так и в валюте отчетности, были добавлены суммы в валюте отчетности.
- Если отчет или запрос не имеет достаточного места для отображения сумм в обеих валютах, вариант был добавлен, чтобы пользователи могли выбирать валюту, которая отображается.

Для разных отчетов и запросов логика также была добавлена для подавления сумм в валюте отчетности, если валюта отчетности совпадает с валютой учета или если валюта отчетности не была определена в книге учета для юридического лица.

## <a name="financial-journals"></a>Финансовые журналы

Финансовые журналы, такие как общий журнал и журнал накладных поставщиков, были обновлены, чтобы они содержали дополнительные сведения о валюте отчетности. Итоговые суммы по ваучера и журнала теперь отображаются в валюте отчетности. Кроме того, отображается информация о валютном курсе для валюты отчетности на вкладке **Общие** строк журнала. Таким образом, при вводе транзакций можно переопределить валютный курс для валюты отчетности.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Накладные поставщиков, заказы на продажу и договора на продажу
Накладные поставщиков, заказы на продажу и соглашения на продажу были обновлены, чтобы включить фиксированный валютный курс для валюты отчетности. Фиксированный валютный курс может быть определен как для валюты учета, так и для валюты отчетности, когда валюта проводки отличается. Если валюта учета и валюта отчетности одинаковы, то синхронизация фиксированного валютного курса будет обеспечиваться путем использования фиксированного обменного курса валюты учета в качестве фиксированного обменного курса валюты отчетности. Фиксированный валютный курс валюты отчетности не может быть изменен для этой конфигурации. Если валюта учета и валюта отчетности различаются, фиксированный валютный курс может быть определен как для валюты учета, так и для валюты отчетности при вводе проводки. Если валюта отчетности не была определена в книге учета, поле **Фиксированный валютный курс валюты отчетности** не включается, и сумма в валюте отчетности не рассчитывается.

## <a name="module-changes"></a>Изменения модулей

Следующие модули используют валюту отчетности в качестве второй валюты отчетности:

- [Главная книга](#general-ledger)
- [Финансовая отчетность](#financial-reporting)
- [Расчеты с поставщиками](#accounts-payable-and-accounts-receivable)
- [Расчеты с клиентами](#accounts-payable-and-accounts-receivable)
- [Управление банком и кассовыми операциями](#cash-and-bank-management)
- [Основные средства](#fixed-assets)
- [Консолидации](#consolidations)

### <a name="general-ledger"></a>Главная книга

Если валюта отчетности была определена в книге учета, главная книга уже отслеживает суммы в валюте отчетности для каждой записи учета. Однако эти суммы теперь преобразуются из сумм в валюте проводки.

Следующие дополнительные изменения были выполнены в модуле **Главная книга**:

- Можно определить отдельный тип валютного курса для валюты отчетности в книге учета. Если организация не хочет использовать другой тип валютного курса, поле для типа валютного курса для валюты отчетности можно оставить пустым. Кроме того, можно выбрать тот же тип валютного курса, что и используемый для валюты учета. Если оставить это поле пустым, система использует тип валютного курса для валюты учета.
- Новый журнал, журнал корректировок валюты отчетности, позволяет разносить корректировки на счета учета только в валюте отчетности. Этот журнал позволяет выполнять разноску только на счета ГК. Он не поддерживает внутрихолдинговые разноски, и валюта должна быть валютой отчетности юридического лица, когда выполняется разноска журнала. При разноске журнала суммы в валюте проводки и суммы в валюте учета равны 0 (нолю), а сумма в валюте отчетности разносится с суммой, введенной в проводку. Поскольку способ, которым валюта отчетности используется в модулях **Расчеты с поставщиками**, **Расчеты с клиентами** и **Основные средства**, изменился, этот журнал может использоваться для корректировки после обновления. Примеры, которые показывают, как можно использовать этот журнал, см. в разделах для этих модулей.
- Процесс распределения периодов был обновлен таким образом, чтобы он выделял суммы в валютах проводки, учета и отчетности. Ранее суммы выделялись в валютах проводки и учета, затем сумма в валюте учета преобразовывалась в валюту отчетности. Это поведение может привести к тому, что сальдо остается на счете учета в валюте отчетности. Теперь, когда суммы рассчитываются и используется в записи учета, преобразование не производится.
- Процесс переоценки в иностранной валюте уже переоценил суммы в валюте отчетности. Тем не менее, сумма в валюте отчетности теперь вычисляется с использованием суммы в валюте проводки, как было описано в разделе [Процесс разноски](#posting-process) ранее в этой статье.
- Многие отчеты и запросы в главной книге уже имели валюту отчетности, но несколько не имели. Одним из примеров является страница списка **Оборотно-сальдовая ведомость**. Эта страница списка теперь включает столбцы для валюты учета и валюты отчетности. Обратите внимание, что столбцы для валюты отчетности скрыты, если валюта учета и валюта отчетности одинаковы, или если валюта отчетности не была определена в главной книге.

### <a name="financial-reporting"></a>Финансовая отчетность

Улучшения в модуле **Финансовая отчетность** позволяют включить суммы в валюте отчетности в финансовом отчете двумя способами. В определении столбца можно создать отчет непосредственно по суммам в валюте отчетности, которые разносятся в главную книгу (новые функциональные возможности). Кроме того, можно продолжить переводить суммы из валюты учета в валюту отчетности (существующая функция).

Это изменение доступно через параметр **Отображения валюты** в определении столбца. При выборе **Валюта отчетности из книги** суммы в столбце не преобразуются. Вместо этого они включаются в отчет непосредственно из главной книги. Если требуется, чтобы в столбце отображались преобразованные суммы, выберите пункт **Пересчет в XXXX**, где *XXXX* является валютой отчетности, которая должна отображаться в столбце. В этом случае суммы в валюте учета преобразуются в выбранную валюту, используя существующую функцию преобразования.

### <a name="accounts-payable-and-accounts-receivable"></a>Расчеты с клиентами и расчеты с поставщиками

Модули **Расчеты с поставщиками** и **Расчеты с клиентами** уже контролировали суммы в валюте отчетности. Тем не менее суммы не отображались и не использовались для различных процессов. Сделаны следующие изменения:

- Суммы в валюте отчетности теперь отображаются в проводках как для клиентов, так и для поставщиков. Суммы в валюте отчетности также отображаются для открытого сальдо каждой проводки.
- Процесс распределения по срокам был обновлен, чтобы организация могла просмотреть классификации по срокам оплаты в валюте учета или валюте отчетности.
- Различные запросы и отчеты были обновлены таким образом, чтобы отображать суммы в валюте отчетности. Примерами могут служить отчеты **Выверка клиентов и ГК** и **Выверка ГК и поставщика**.
- Процесс переоценки в иностранной валюте уже переоценил суммы в валюте отчетности. Тем не менее, сумма в валюте отчетности теперь вычисляется с использованием суммы в валюте проводки, как описано в разделе [Процессе разноски](#posting-process).
- **Соображения в связи с обновлением:** перед обновлением рассчитываются суммы в валюте отчетности для документов (накладные, платежи и т. д.) через валюту учета. Например, накладная разнесена до обновления организации, и эта накладная не оплачена. При обновлении учетная запись накладной остается без изменений. Однако после обновления изменения для двух валют вступают в силу. Таким образом, при выполнении платежа по накладной сумма платежа в валюте отчетности теперь вычисляется через сумму в валюте проводки. При сопоставлении платежа и накладной незначительное различие может быть рассчитано в сумме реализованной прибыли/убытка, так как теперь суммы в валюте отчетности вычисляются по-другому. Если расхождение, которое рассчитывается, считается значительным, новый журнал корректировки в новой валюте отчетности может использоваться для корректировки сальдо реализованной прибыли/убытка и счетов учета расчетов с поставщиками и расчетов с клиентами только в валюте отчетности.

### <a name="cash-and-bank-management"></a>Управление банком и кассовыми операциями

Ранее модуль **Управление банком и кассовыми операциями** не отслеживал никакие суммы в валюте отчетности для проводок, которые были разнесены для каждого банковского счета. После обновления для любой новых проводок, которые разносятся, автоматически отслеживаются суммы в валюте отчетности. Тем не менее, суммы в валюте отчетности необходимо добавить к ранее разнесенным проводкам во вспомогательной книге.

- **Соображения в связи с обновлением:** поскольку проводки по банковскому счету ранее не отслеживали суммы в валюте отчетности во вспомогательной книге, мастер был добавлен, чтобы можно было добавить суммы в валюте отчетности к проводкам по банковским счетам. Этот мастер **не** выполняет снова разноску в главную книгу. Вместо этого он принимает суммы в валюте отчетности из главной книги и обновляет их в таблицах вспомогательной книги.

    - Чтобы запустить мастер, выберите **Управление банком и кассовыми операциями** \> **Настройка** \> **Добавление сумм в валюте отчетности в проводки банковского счета**.
    - В мастере отображаются проводки для всех банковских счетов в текущей компании, в которых сумма в валюте отчетности равна 0 (нулю). Включаются только те проводки, которые были учтены до обновления.
    - Для каждой проводки по банковскому счету мастер производит поиск соответствующих операций учета в главной книге и вводит сумму в валюте отчетности по умолчанию. Несмотря на то, что эти суммы могут редактироваться, рекомендуется, чтобы вы **не** изменяли их. В противном случае может оказаться невозможно выполнить выверку сальдо банковского счета в главной книге. Единственный случай, когда необходимо изменить сумму, — это если не удается найти сумму в валюте отчетности в ГК. В этом случае мастер отображает сумму со значением 0 (ноль) для валюты отчетности.
    - При выборе **Отменить** в мастере проводки по банковскому счету и любые изменения сумм в валюте отчетности сохраняются до следующего запуска мастера. Однако суммы в валюте отчетности для проводок банковского счета не обновляются. Обновление происходит только при выборе **Готово** в мастере. Можно запустить мастер несколько раз. Таким образом, при обнаружении ошибки можно исправить любые неправильные суммы в валюте отчетности.

- Никакие процессы модуля управления банком и кассовыми операциями не были изменены, но разные отчеты и запросы были обновлены таким образом, чтобы отображать суммы в валюте отчетности. Отчеты прогнозов движения денежных средств являются исключением из этого правила. Они не были обновлены, чтобы включить суммы в валюте отчетности.

### <a name="fixed-assets"></a>Основные средства

Ранее модуль **Основные средства** не отслеживал никакие суммы в валюте отчетности для проводок, которые были разнесены для каждого журнала основных средств. После обновления для любой новых проводок, которые разносятся, автоматически отслеживаются суммы в валюте отчетности. Тем не менее, суммы в валюте отчетности необходимо добавить к ранее разнесенным проводкам во вспомогательной книге.

Кроме того, в процесс амортизации внесены значительные изменения. Эти изменения требуют участия пользователя после обновления. Важно прочитать и понять следующие изменения, даже если ОС еще не используются.

- Изменился способ, которым процесс амортизации определяет сумму в валюте отчетности. Следующий сценарий сравнивает, как амортизация ранее определяла сумму в валюте отчетности, и как теперь она определяет сумма в валюте отчетности.



    **Сценарий амортизации**

    ОС приобретено и разнесено со следующими суммами. Обратите внимание, что сумма в валюте отчетности разносится в главную книгу, но она не хранится в таблицах вспомогательной книги основных средств.

    | Тип проводки | Сумма проводки | Валютный курс | Сумма в валюте учета | Валютный курс | Сумма в валюте отчетности |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Ввод в эксплуатацию      | 1 000 000 DKK      | 2.0           | 500 000 USD                | 2,5           | 200 000 EUR               |

    **Предыдущая амортизации для валюты отчетности**

    В конце года предложение по амортизации выполняется и рассчитывает следующие суммы.

    | Тип проводки | Сумма проводки | Валютный курс | Сумма в валюте учета | Валютный курс | Сумма в валюте отчетности |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Амортизация     | 50 000 USD         | 1,0           | 50 000 USD                 | 2,6           | 19 230,77 EUR             |

    При выполнении предложения по амортизации программа рассчитывает сумму в валюте учета, используя метод амортизации. Затем она преобразует эту сумму в валюту отчетности с использованием текущего валютного курса между долларами США и Евро. Это преобразование вызывает проблемы, так как основное средство не может быть амортизировано в полном объеме в валюте отчетности при использовании спот-курса.

    **Новая амортизации для валюты отчетности**

    Процесс амортизации был изменен, чтобы сумма в валюте отчетности также вычислялась с помощью метода амортизации. Ниже приведены результаты при выполнении амортизации основного средства.

    | Тип проводки | Сумма проводки | Валютный курс | Сумма в валюте учета | Валютный курс                                                       | Сумма в валюте отчетности |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Амортизация     | 50 000 USD         | 1,0           | 50 000 USD                 | 2,5<blockquote>[!NOTE] Несмотря на то, что отображается этот валютный курс, он не используются для перевода в валюту отчетности.</blockquote> | 20 000 EUR                |

    При выполнении предложения по амортизации рассчитывается как сумма в валюте учета, так и сумма в валюте отчетности с помощью метода амортизации. Эти суммы затем используются в учетной записи в главной книге. Никакое преобразование, чтобы определить сумму в валюте отчетности, не выполняется.

- **Соображения в связи с обновлением:** поскольку проводки по журналу основных средств ранее не отслеживали валюту отчетности, мастер был добавлен, чтобы можно было добавить суммы в валюте отчетности к проводкам журнала основных средств. Этот мастер **не** выполняет снова разноску в главную книгу. Из-за того, что был изменен способ, которым предложение по амортизации рассчитывает суммы в валюте отчетности, мастер **необходимо** выполнить и завершить для каждой компании, прежде чем организация сможет ввести любые проводки амортизации.

    - Чтобы запустить мастер, выберите **Основные средства** \> **Настройка** \> **Добавить суммы в валюте отчетности в книги основных средств**.
    - В мастере отображаются проводки для всех журналов основных средств в текущей компании, в которых сумма в валюте отчетности равна 0 (нулю). Включаются только те проводки, которые были учтены до обновления.
    - Мастер **не** извлекает суммы в валюте отчетности из главной книги. Как было описано в предыдущем сценарии, суммы в валюте отчетности, которые были первоначально разнесены в главную книгу, неправильно использовали спот-курс. Эти суммы не должны отображаться во вспомогательной книге ОС, так как в следующем расчете амортизации будут использоваться неправильные суммы. Вместо этого мастер находит валютные курсы на дату первого приобретения. Затем используется этот валютный курс для рекомендации суммы в валюте отчетности, которая должна быть разнесена во вспомогательной книге. Например, вот что может отображаться в мастере для предыдущего сценария.

        | Основные средства | Резервирование      | Тип проводки | Дата проводки | Денежный | Сумма в валюте проводки | Сумма, руб.  | Валютный курс | Сумма в валюте отчетности |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Ввод в эксплуатацию      | 03.06.2016         | датская крона      | 1000000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Амортизация     | 03.06.2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Амортизация     | 03.06.2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Амортизация     | 03.06.2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Многие клиенты отслеживали сведения о проводках основных средств в книгах. Эти сведения включают валютные курсы и суммы. Если эти данные в книге, можно создать тип настраиваемый тип валютного курса и обновить его с использованием валютных курсов из книги. Этот тип валютного курса затем будет использоваться для ввода валютного курса по умолчанию на дату приобретения и расчета суммы в валюте отчетности. Если тип валютного курса не выбран, мастер использует тип валютного курса, который был определен в главной книге.
    - Валютный курс и суммы в валюте отчетности можно изменить. Если валютный курс изменяется, сумма в валюте отчетности пересчитывается с использованием нового курса.
    - При выборе **Отменить** в мастере проводки журнала основных средств и любые изменения валютного курса или сумм в валюте отчетности сохраняются до следующего запуска мастера. Однако суммы в валюте отчетности для проводок журнала основных средств не обновляются. Обновление происходит только при выборе **Готово** в мастере. Можно запустить мастер несколько раз. Таким образом, при обнаружении ошибки можно исправить любые неправильные суммы в валюте отчетности.
    - Когда суммы в валюте отчетности полностью обновляются во вспомогательной книге, вы **должны** установить для параметра **Вы обновили все суммы в валюте отчетности в проводках журнала основных средств?** значение **Да**, а затем выбрать **Готово**. Расчеты амортизации не могут быть завершена, пока для параметра **Вы обновили все суммы в валюте отчетности в проводках журнала основных средств?** не будет задано значение **Да**. После того как для параметра задано значение **Да**, мастер больше не будет доступен.
    - После обновления проводок с основными средствами во вспомогательной книге с суммами в валюте отчетности, эти суммы не будут соответствовать суммам, которые были первоначально разнесены в главную книгу. Тем не менее журнал корректировки валюты отчетности может использоваться для обновления сальдо счетов книги учета амортизации в главной книге, чтобы они соответствовали суммам, которые были первоначально разнесены.
    - Новая сущность **Суммы проводок основных средств в валюте отчетности**, добавленная в рабочую область **Управление данными**, позволяет экспортировать данные из мастера. Затем данные можно использовать для определения сальдо во вспомогательной книге основных средств для проводок амортизации. Это сальдо затем может использоваться для определения суммы корректировки в валюте отчетности в главной книге.

- **Соображения в связи с обновлением:** новые поля настройки были добавлены к основным средствам и используются при расчете амортизации. Возможно, потребуется обновить эти поля до следующего расчета амортизации.

    - В журнале основных средств (**Основные средства** \> **Книги**) экспресс-вкладка **Общие** имеет новое поле **Цена приобретения в валюте отчетности**.
    - В журнале основных средств (**Основные средства** \> **Книги**) экспресс-вкладка **Амортизация** имеет новое поле **Ожидаемая ликвидационная стоимость в валюте отчетности**.
    - В параметрах основных средств (**Основные средства** \> **Настройка** \> **Параметры основных средств**) на экспресс-вкладке **Общие** имеется новое поле **Минимальная сумма амортизации в валюте отчетности**.
    - В книгах (**Основные средства** \> **Настройка** \> **Книги**) на экспресс-вкладке **Общие** имеются два новых поля: **Округлить амортизацию в валюте отчетности** и **Сохранить остаточную стоимость в валюте отчетности**.

- Так как предложение по амортизации теперь рассчитывает суммы как в валюте учета, так и в валюте отчетности, журнал основных средств был обновлен, чтобы в нем отображались суммы амортизации в валюте отчетности. Для проводок по амортизации валюта проводки всегда является валютой учета. Таким образом, эти суммы будут продолжать отображаться в столбцах **Дебет** и **Кредит**. Два новых столбца **Дебет в валюте отчетности** и **Кредит в валюте отчетности** были добавлены к сетке.

    - Новые поля будут доступны только в том случае, если тип проводки — один из четырех типов амортизации: **Амортизация**, **Корректировка амортизации**, **Дополнительная амортизация** или **Особая амортизационная премия**.
    - Если тип проводки амортизации вводится в журнал основных средств, суммы в валюте отчетности отображаются в новых столбцах. Эти суммы могут быть изменены.
    - Если валюта учета и валюта отчетности в книге учета совпадают, суммы будут поддерживаться синхронизированными. При изменении суммы **Кредит** сумма **Кредит в валюте отчетности** автоматически изменяется, чтобы она соответствовала ей.
    - Если любой другой тип проводки вводится в журнал основных средств, суммы **Дебет в валюте отчетности** и **Кредит в валюте отчетности** никогда не отображаются, ни до, ни после разноски. Суммы в валюте учета и в валюте отчетности по-прежнему доступны в ваучере, который разносится в главную книгу.
    
### <a name="consolidations"></a>Консолидации
    
Функциональные возможности, введенные в Dynamics 365 Finance версии 10.0.5 (Октябрь 2019), обеспечивают функции через управление функциями для расширенной гибкости при консолидации и учете в двух валютах. Чтобы включить эту функцию, перейдите в рабочую область **Управление функциями** и выберите **Включить функцию учета в двух валютах в консолидации главной книги**.

В консолидации главной книги был добавлен новый параметр для консолидации сумм в валюте учета или валюте отчетности из исходных компаний. Если валюта учета или отчетности совпадает с валютой учета или валютой отчетности в консолидированной компании, суммы будут скопированы непосредственно, а не переведены.

-  Теперь можно выбрать, следует ли использовать валюту учета или валюту отчетности из исходной компании в качестве валюты проводки в консолидированной компании.

- Суммы в валюте учета или отчетности их исходной компании будут скопированы напрямую в суммы в валюте учета или валюте отчетности в консолидированной компании, если какая-то из валют совпадает. Суммы в валюте учета и в валюте отчетности в консолидированной компании рассчитываются с использованием валютного курса, если ни одна из валют не совпадает.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

