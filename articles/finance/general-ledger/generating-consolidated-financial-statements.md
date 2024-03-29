---
title: Формирование консолидированных финансовых отчетов
description: В этой статье описываются различные сценарии, в которых возможно формирование консолидированных финансовых отчетов.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: c6a132b742414a3dab635634c7bb5ba0dbea527d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846809"
---
# <a name="generate-consolidated-financial-statements"></a>Формирование консолидированных финансовых отчетов

[!include [banner](../includes/banner.md)]

В этой статье описываются различные сценарии, в которых возможно формирование консолидированных финансовых отчетов.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Одноуровневые и многоуровневые консолидации между юридическими лицами
Самый простой способ консолидации при использовании модуля "Финансовая отчетность" — это использование аналитических структур для агрегирования данных по компаниям, имеющим одинаковый план счетов и одинаковые финансовые периоды. Ниже приведены базовые инструкции по консолидации отчетности с помощью аналитической структуры.

1. Создайте определение строк и убедитесь, что все необходимые счета во всех компаниях включены в строки.
2. Создайте определение столбцов, которое включает в себя все столбцы, необходимые в создаваемом отчете.
3. Создайте аналитическую структуру, которая включает в себя по аналитическому узлу для каждой компании, которую вы планируете включать в консолидированные отчеты.

> [!TIP]
> Дополнительные сведения о создании и настройке определений строк, столбцов и аналитических структур см. в разделе [Компоненты финансового отчета](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

На следующем рисунке показано, как использовать определение аналитической структуры в модуле "Финансовая отчетность" для указания каждой компании, которая будет консолидироваться.

![Определение аналитической структуры.](./media/reporting-tree-definition.png "Определение аналитической структуры")

Как видно из консолидированного отчета на следующем рисунке, при использовании аналитической структуры в сочетании с определением отчета можно просматривать каждую компанию по отдельности. Консолидированный суммы отображаются на сводном уровне.

![Сводный уровень с консолидированными суммами.](./media/consolidate-amount-summary-level.png "Сводный уровень с консолидированными суммами")

Также можно создать многоуровневую аналитическую структуру, которая включает в себя столько уровней, сколько необходимо. На следующем рисунке показано определение многоуровневой аналитической структуры со свертками по регионам мира.

![Определение многоуровневой аналитической структуры со свертками по регионам.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Определение многоуровневой аналитической структуры со свертками по регионам")

На следующем рисунке показано определение многоуровневой аналитической структуры со свертками по функциональным подразделениям.

![Определение многоуровневой аналитической структуры со свертками по функциональным подразделениям.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Определение многоуровневой аналитической структуры со свертками по функциональным подразделениям")

### <a name="viewing-companies-side-by-side"></a>Просмотр компаний друг рядом с другом
Многие клиенты предпочитают отчеты, где компании отображаются друг рядом с другом и в столбце приведен консолидированный итог. Этот формат легко можно реализовать после создания аналитической структуры. Ниже приведены основные шаги, которые необходимо выполнить для просмотра компаний друг рядом с другом в консолидированных финансовых отчетах.

1. Создайте определение столбцов, которое включает в себя столбец **Финансовая аналитика** для каждой компании.
2. Используйте поле **Элемент аналитической структуры**, чтобы выбрать структуру и элемент структуры для каждого столбца.
3. (Необязательно.) Добавьте заголовки и столбцы итогов.

На следующем рисунке показано определение столбцов в формате "друг рядом с другом".

![Определение столбцов в формате "друг рядом с другом".](./media/column-definition-side-by-side-format.png "Определение столбцов в формате &quot;друг рядом с другом&quot;")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Консолидации на основе организационных структур, созданных из юридических лиц
Организационные иерархии, содержащие аналитики или юридические лица, динамически создают аналитические структуры в модуле "Финансовая отчетность". Простой способ оптимизировать консолидацию — это добавить в отчет в модуле "Финансовая отчетность" организационную иерархию. На основании даты отчета модуль Financial Reporting выберет организационную иерархию на дату вступления силу или перед ней, как показано на следующем рисунке.

![Динамическое создание определения аналитической структуры.](./media/dynamically-create-reporting-tree-definitions.png "Динамическое создание определения аналитической структуры")

## <a name="consolidations-that-involve-eliminations"></a>Консолидации, в которых используются элиминирования
Проводки элиминирования — часто используемый элемент процесса консолидации. В этом примере в ходе консолидации исключается пять счетов: 142600, 211400, 401420, 401180 и 510820. Компании могут по-разному настраивать свои внутрихолдинговые счета. Например, некоторые компании используют в качестве последней цифры 9, если счет используется во внутрихолдинговых проводках. Вне зависимости от используемого способа, если вы знаете внутрихолдинговые счета, вы можете отразить элиминирования в своих консолидированных финансовых отчетах.

На следующем рисунке показано определение столбцов для консолидированного отчета о прибылях и убытках. Для каждой компании с помощью фильтра по аналитике определено три внутрихолдинговых счета прибылей и убытков. Столбцы "F", "G" и "H" включают счета элиминирования только для компаний USMF, USRT и DEMF. Эти столбцы настроены так, что они **не** печатаются в финансовом отчете.

![Определение столбцов консолидированного отчета о прибылях и убытках.](./media/column-definition-consolidated-income-statement.png "Определение столбцов консолидированного отчета о прибылях и убытках")

При формировании отчета суммы элиминирования рассчитываются в столбцах F, G и H и суммируются в столбце I. В столбце J отображаются консолидированные суммы. Эти консолидированные суммы не включают в себя элиминирования для компаний USMF, USRT и DEMF.

> [!TIP]
> Создайте второй отчет, содержащий только исключаемые записи, и используйте его в группе отчетов, в которую входит ваш консолидированный отчет. Таким образом у вас будет вся необходимая информация для создания всех требуемых записей журнала.

На следующем рисунке показан консолидированный отчет.

![Консолидированный отчет о прибылях и убытках.](./media/consolidated-report-income-statement.png "Консолидированный отчет о прибылях и убытках")

Вне зависимости от того, что вы используете — счета, аналитики или и то и другое, модуль "Финансовая отчетность" позволяет отфильтровывать исключаемые записи с помощью фильтрации по аналитикам.

## <a name="minority-interest"></a>Миноритарная доля
Компания может быть владельцем только некоторой доли другой компании. В этой ситуации при подготовке консолидированного отчета важно учитывать только ту долю, которая принадлежит вашей компании. В модуле "Финансовая отчетность" предусмотрено несколько способов отражения миноритарных долей в зависимости от предпочтений пользователя. Одним из способов является использование процента свертки в определении аналитической структуры. Другой способ — отражение миноритарной доли в виде отдельной строки в отчете.

### <a name="using-the-reporting-tree-definition"></a>Использование определения аналитической структуры
В определении аналитической структуры введите процент владения в столбце **Процент свертки** (столбце H), как показано на следующем рисунке. При формировании отчета этот процент будет использоваться для расчета консолидированной суммы. В этом примере компании Contoso принадлежит только 80% компании Contoso Germany. Можно ввести **80** или **0,8** в столбце **Процент свертки**, и 80 процентов будет свертываться на консолидированный уровень.

> [!NOTE]
> Этот процент владения можно применять к любому элементу аналитической структуры, а не только на уровне компании. 

![Использование процента в определении аналитической структуры.](./media/Using-reporting-tree-definition-percentage.png "Использование процента в определении аналитической структуры")

При формировании отчета в отчете по Contoso Germany будет отображаться 100 процентов суммы выручки, а 80 процентов этой суммы будет свернуто в выручку на консолидированном уровне.

Если вашей компании принадлежит менее 1 процента другой компании, вы можете установить флажок **Разрешить сведение менее 1%** на вкладке **Дополнительные параметры** страницы **Настройки отчета**, как показано на следующем рисунке. В этом случае значения в столбце **Процент свертки** в аналитической структуре будет рассматриваться как значения меньше 1 процента. Например, если ввести **0,8**, 0,8 процента суммы будет свернуто на консолидированный уровень, а не 80 процентов. Того же результата можно добиться, если оставить флажок **Разрешить сведение менее 1%** снятым и ввести **0,008** в столбце **Процент свертки**.

![Параметры настроек отчетности.](./media/reporting-setting-options.png "Параметры настроек отчетности")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Отражение владения в виде отдельной строки в консолидированном отчете
Другой вариант отражения миноритарных долей — показывать 100 процентов дочерней компании для каждой строки в отчете, однако вычитать неконтролирующую долю из чистого дохода.

Как показано на следующем рисунке, для расчета миноритарной доли в финансовых отчетах можно использовать инструкцию **IF THEN ELSE** и ограничение столбца в определении строк.

![Отражение владения в виде отдельной строки в консолидированном отчете.](./media/Showing-ownership-separate-row-consolidated-report.png "Отражение владения в виде отдельной строки в консолидированном отчете")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Разные планы счетов у разных юридических лиц
Нередко разные юридические лица используют разные планы счетов, однако им все равно нужно составлять консолидированные финансовые отчеты. В этом случае можно использовать модуль "Финансовая отчетность" для консолидации данных, чтобы можно было формировать консолидированные финансовые отчеты. Ниже приведены базовые инструкции по консолидации отчетности при использовании в разных юридических лицах разных планов счетов.

1. Создайте определение строк, содержащее несколько ссылок на финансовые аналитики. Для каждого плана счетов должно быть по одной ссылке.
2. Используйте ограничение элемента аналитической структуры в определении столбцов, чтобы назначить каждую компанию соответствующему столбцу.


В каждую строку в определении строк можно добавить по несколько связей с финансовыми аналитиками для плана счетов каждой компании. На следующем рисунке компания USMF использует набор счетов в первом столбце **Связь с финансовой аналитикой** (столбце J), а компания DEMF использует счета во втором столбце **Связь с финансовой аналитикой** (столбце K).

> [!TIP]
> Дополнительные сведения о ячейке **Связь с финансовой аналитикой** см. в разделе "Указание ячейки «Связь с финансовой аналитикой»".

![Задание первой связи счетов с финансовой аналитикой.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Задание первой связи счетов с финансовой аналитикой")

Можно использовать аналитическую структуру для определения того, какая связь с финансовыми аналитиками из определения строк используется с каждой из компаний. Выберите определение строк в столбце E, а затем выберите соответствующую связь со строкой в столбце F, как показано на следующем рисунке.

![Связь с финансовыми аналитиками в определении строк.](./media/link-financial-dimensions-row-definition-used.png "Связь с финансовыми аналитиками в определении строк")

> [!TIP]
> При создании связей с финансовыми аналитиками используйте описание для указания компаний, к которым относится каждая из связей. Так вам будет легче выбрать нужную компанию при создании аналитической структуры. В определении столбцов поле **Элемент аналитической структуры** позволяет ограничить каждый столбец одним элементом аналитической структуры, чтобы можно было просматривать данные компаний друг рядом с другом. Если не указать конкретную компанию для столбца, будут отображаться консолидированные данные по всем компаниям.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Разные финансовые календари у разных юридических лиц
У разных юридических лиц могут быть разные финансовые календари, но от них все равно могут требоваться консолидированные финансовые отчеты. Существует два способа консолидации данных при наличии разных финансовых периодов в разных юридических лицах:

- Создайте определение столбцов и используйте период и год для сопоставления соответствующих периодов для каждой компании.
- Выбрав **Настройки** \> **Прочие** \> **Дополнительные параметры**, выберите, как должны консолидироваться данные — по дате окончания периода или по номеру периода.

При разработке определения столбцов для нескольких компаний с разными финансовыми периодами важно подумать о том, какая из компаний будет назначена полю **Название компании** в определении отчета. Финансовый календарь этой компании будет использоваться в качестве базового финансового календаря для определения отчета. Например, в следующей таблице показаны финансовые периоды, которые настроены для компаний USMF и INMF. Для консолидированных отчетов необходимо использовать тот финансовый календарь, который используется в компании USMF. В столбце "Сопоставление" показан эквивалентный период и год для каждой компании, если отчет формируется на 30 июня 2018 г.

| Организация   | Финансовый год                                  | Сопоставление                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Финансовый год, с 1 июля по 30 июня          | Период 12, финансовый год 2018 | 
| INMF      | Календарный год, с 1 января по 31 декабря | Период 6, финансовый год 2018  |

На следующем рисунке компания USMF указана в поле **Название компании** в определении отчета. Следовательно, финансовый календарь компании USMF будет использоваться в качестве базового финансового календаря. В этом примере при формировании отчета на 30 июня 2018 г. для компании USMF будет использоваться период BASE, который в определении отчета указан как период 12. Для компании INMF будет использоваться BASE–6, т. е. период 6. Оба столбца будут включать данные за июнь 2018 года.

![Базовый период отчета.](./media/report-base-period.png "Базовый период отчета")

На следующем рисунке показаны параметры в определении отчета, позволяющие выбрать, что используется для консолидации — номер периода или дата окончания периода.

![Параметры для выбора номера периода в определении отчета.](./media/options-report-definition-period-number.png "Параметры для выбора номера периода в определении отчета")

## <a name="business-unit-consolidations"></a>Консолидация по бизнес-единицам
Эта статья посвящена использованию определений и организационных иерархий аналитических структур в Financial Reporting для целей консолидации. Можно также использовать аналитическую структуру для создания консолидированных отчетов по бизнес-единицам, например отчетов о продажах или производственной деятельности по всему миру. Создание таких отчетов — распространенное требование. Чтобы создать их, выберите для каждой единицы компанию и аналитику, по которой нужно консолидировать данные. Например, на следующем рисунке свертка по бизнес-единицам достигается путем повтора каждой компании в столбце **Компания** (столбце A) и указания группы значений аналитики "Подразделение" для компании в столбце **Аналитики** (столбце D).

![Консолидированные отчеты по бизнес-единицам.](./media/business-unit-consolidation-reports.png "Консолидированные отчеты по бизнес-единицам")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Консолидации, в которых фигурирует несколько валют отчетности
Модуль "Финансовая отчетность" обеспечивает дополнительную гибкость при просмотре фактических данных, бюджетных данных, данных бюджетного контроля и данных бюджетного планирования в нескольких валютах. За счет использования данных настройки ключа просмотр любого отчета в любой валюте в любой момент и для любого пользователя не требует никакой дополнительной настройки в модуле "Финансовая отчетность".

### <a name="prerequisites"></a>Необходимые условия
Для правильного расчета пересчитанных сальдо модулю "Финансовая отчетность" требуется,чтобы счету "Нераспределенная прибыль" в списке **Счет ГК** была назначена категория **Счет нераспределенной прибыли**. Модуль "Финансовая отчетность" не поддерживает разноску на счет "Нераспределенная прибыль". При разноске проводок на счет "Нераспределенная прибыль" пересчитанные сальдо не будет рассчитываться правильно. Мы рекомендуем пользователям настроить дополнительный счет "Нераспределенная прибыль" для разноски корректировок по счету "Нераспределенная прибыль".

В счете ГК поля **Тип валютного курса для финансовой отчетности** и **Тип пересчета валюты** на экспресс-вкладке **Финансовая отчетность** должны быть заданы для каждого счета, как показано на следующем рисунке. Эту задачу можно выполнять отдельно для каждого счета или использовать шаблоны счетов для распространения изменений на нижестоящие счета.

- В поле **Тип валютного курса для финансовой отчетности** выберите тип валютного курса, содержащий валюты и валютные курсы, применяемые к счету. Эта таблица валют и валютных курсов будет применяться к фактическим данным в модуле "Финансовая отчетность".
- В поле **Тип пересчета валюты** выберите способ, используемый для расчета валютного курса для счета. Этот способ пересчета валюты используется и для фактических, и для бюджетных данных в модуле "Финансовая отчетность".

![Счета ГК финансовой отчетности.](./media/Financial-reporting-main-accounts.png "Счета ГК финансовой отчетности")

Для бюджетных данных, данных бюджетного контроля и данных бюджетного планирования тип валютного курса определяется на странице **Книга учета**. Эта таблица будет использоваться для извлечения валютных курсов; при этом будет использоваться тип пересчета валюты, назначенный счету.

### <a name="currency-translation-methods"></a>Методы пересчета валюты
Существует четыре варианта расчета валютных курсов в модуле "Финансовая отчетность":

- **Средневзвешенное** — этот метод чаще всего используется для счетов прибылей и убытков. Он предполагает использование следующей формулы:

    (валютный курс × количество дней действия) ÷ количество дней в периоде

- **Среднее** — этот метод представляет собой альтернативный метод для счетов прибылей и убытков. Он предполагает использование следующей формулы:

    общая сумма валютных курсов ÷ количество валютных курсов

- **Текущий** — этот метод чаще всего используется для балансовых счетов. Используемый валютный курс — это курс на дату отчета или столбца в модуле "Финансовая отчетность" или перед этой датой.
- **Дата проводки** — этот метод используется для счетов основных средств. Используемый валютный курс — это курс на дату приобретения основного средства. Если курс на эту дату не введен, используется предыдущий курс, введенный как можно ближе к дате приобретения основного средства.

### <a name="report-designer-options-for-currency-translation"></a>Параметры конструктора отчетов для пересчета валюты
В модуле "Финансовая отчетность" любой отчет может отображаться в любом количестве валют отчетности. Следующие поля в определении отчета поддерживают эту возможность:

- Раздел **Информация о валюте** на странице **Определение отчета**. В этом разделе отображается валюта, в которой отображаются значения при формировании отчета.
- Новый флажок **Включить все валюты отчетности**. Если этот флажок установлен, после формирования отчета, в котором используется функциональная валюта компании, в очередь отчетов будет добавлено по отчету для каждой валюты отчетности. Если этот флажок снят, вы по-прежнему можете выбрать валюту отчетности в веб-средстве просмотра. В этом случае валюта отчетности будет обрабатываться только в случае, если вы ее выберете.

Параметры в определении отчета позволяют легко пересчитать отчет во всех ваши валюты отчетности. Следовательно, вы можете обойтись без одинаковых определений отчетов, которые отличаются только используемой валютой. Если вам требуется отчет, в котором параллельно отображается несколько валют, вы можете продолжать использовать поле **Отображение валюты** на странице **Определение столбцов** для пересчета только данного столбца отчета в альтернативную валюту отчетности.

### <a name="currency-translation-adjustment"></a>Корректировка пересчета валюты
Корректировка пересчета валюты — это разница между курсами, которые используются для расчета балансовых счетов, и курсом, используемым для счетов в отчете о прибылях и убытках. Из-за этой разницы балансовый отчет будет несбалансированным. С помощью модуля "Финансовая отчетность" рассчитывать корректировку пересчета валюты можно двумя способами:

- Использовать страницу **Корректировка округлений** в определении строк, как показано на рисунке ниже.

    ![Корректировка пересчета валюты с помощью корректировки округлений.](./media/Currency-translation-adjustment-rounding-adjustments.png "Корректировка пересчета валюты с помощью корректировки округлений")

    При указании строки, в которой должна отображаться корректировка округления (корректировка пересчета валюты), итоговой строки активов, итоговой строки обязательств и акционерного капитала, а также необходимого порога модуль "Финансовая отчетность" рассчитывает разницу и помещает ее в требуемую строку. Будет создана строка **Корректировка округлений**, которая отображается при детализации, как показано на следующем рисунке.

    ![Детализация до корректировки округлений.](./media/rounding-adjustment-drill-down.png "Детализация до корректировки округлений")

- Поместить все счета в диапазон, от активов до расходов. Как показано на следующем рисунке, разница будет совпадать с суммой корректировки округлений (корректировки пересчета валюты). Таким образом, ее можно использовать в качестве контрольной суммы, чтобы убедиться, что на странице корректировки округлений нет пропущенных сальдо по счетам.

    ![Проверка корректировки округлений.](./media/rounding-adjustment-form-check.png "Проверка корректировки округлений")

### <a name="balance-calculation-approach"></a>Подход к расчету сальдо
Для получения правильно пересчитанных сумм при использовании валют в модуле "Финансовая отчетность" используются следующие методы расчета сальдо:

- **Средневзвешенное и среднее** — каждый период рассчитывается по своему средневзвешенному значению и суммируется для таких столбцов, как поквартальная сумма и сумма с начала года.
- **Исторический** — любой счет, для которого используется исторический метод пересчета, всегда возвращается к дате проводки. Если с проводкой связана дата приобретения, эта дата используется для получения валютного курса. Каждый период затем суммируется и сохраняется для уменьшения времени расчета.
- **Текущий** — рассчитываемые и итоговые столбцы, такие как столбцы поквартальных сумм и сумм с начала года, рассчитываются по спот-курсу, определенному в столбце или в отчете. Например, для столбца **Квартал 1** будет использоваться курс на 31 марта, если используется календарный год.

## <a name="additional-resources"></a>Дополнительные ресурсы

Дополнительные сведения о консолидации и пересчете валют см. в родительской статье этой статьи: [Обзор финансовых консолидаций и пересчета валют](./financial-consolidations-currency-translation.md).

Дополнительные сведения о том, как вводить информацию для интерактивной консолидации, см. в разделе [Интерактивные финансовые консолидации](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
