---
title: Разноска косвенных затрат
description: В этой статье описывается, как разносить косвенные затраты, создавать группы затрат и добавлять узлы к листу калькуляции затрат для косвенных затрат.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868441"
---
# <a name="indirect-cost-posting"></a>Разноска косвенных затрат

Косвенные затраты представляют собой затраты, не имеющие непосредственного отношения к отдельному мероприятию в производственном процессе. Примерами являются административные затраты, такие как зарплата сотрудников, затраты бухгалтерского отдела и накладные расходы, например, арендная плата, оплата коммунальных услуг и затраты на оборудование.

## <a name="calculating-indirect-costs"></a>Расчет косвенных затрат

В Microsoft Dynamics 365 Finance отсутствует автоматический способ расчета ставки косвенных затрат. Необходимо определить косвенные затраты, создать коды косвенных затрат и установить ставку для каждого вида косвенных затрат в листе калькуляции затрат.

Точный процесс, используемый для расчета косвенных затрат, может слегка отличаться в зависимости от компании. Однако, как правило, процесс состоит из следующих основных шагов:

1. Создание списка косвенных затрат, которые должны быть определены в производстве. Этот список может включать расходы на аренду, администрирование расходы, расходы на учет и расходы на юридические услуги. Он не должен включать затраты на сырье или затраты на трудовые ресурсы, которые определены в маршрутах производства.
2. Суммирование всех косвенных затрат. Можно сгруппировать похожие типы косвенных затрат или отделить их друг от друга. Каждый вид настраиваемых косвенных затрат может иметь разные счета ГК, используемые для разноски в главную книгу.
3. Сравнение косвенных затрат с коэффициентом, который также называется базой распределения. Можно выбрать любой коэффициент. Далее приводятся несколько распространенных примеров:

    - Реализация
    - Общее количество, которое производится
    - Время настройки
    - Время выполнения

    Можно выбрать период, для которого необходимо рассчитать косвенные затраты, например, ежемесячно, ежеквартально или ежегодно. Сумма косвенных затрат и сумма коэффициента должны охватывать один и тот же период времени. Для расчета ставки косвенных затрат используется следующая формула:

    *Ставка косвенных затрат* = *Общие расходы косвенных затрат* &divide; *Общий коэффициент*

4. Создание групп косвенных затрат.
5. Настройте таблицу калькуляции затрат с учетом ваших ставок.
6. Настройка затрат для косвенных затрат в версии учета затрат.

> [!NOTE]
> Можно использовать модуль **Учет затрат** для накопления затрат и определения накладных расходов из других источников, таких как производство, проекты и главная книга. Дополнительные сведения см. в разделе [Учет затрат](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Различные регулирующие учреждения опубликовали руководство по типам затрат, которые могут быть включены в качестве косвенных затрат или накладных расходов в затраты на готовую продукцию. Прежде чем приступить к настройке косвенных затрат, рекомендуется проконсультироваться с бухгалтерами и ознакомиться с местными нормативными правилами, чтобы убедиться в соответствии требованиям.

## <a name="create-cost-groups-for-indirect-costs"></a>Создание групп затрат для косвенных расходов.

Необходимо создать хотя бы одну группу затрат, которая будет использоваться для косвенных затрат. Количество групп затрат, которые можно использовать, не ограничено. Обдумайте способ расчета затрат и определите наличие различных ставок для различных типов затрат. Например, ваша организация производит продукты питания. Некоторые виды сырья и готовых товаров являются сухой продукцией и имеют одинаковые косвенные затраты для складских операций. Прочие виды сырья и готовых продуктов являются охлажденной продукцией и имеют более высокие косвенные затраты. В этом случае может возникнуть необходимость создать две группы затрат: **Накладные расходы для сухой продукции** и **Накладные расходы для охлажденной продукции**

Чтобы создать группу затрат для непрямых затрат, выполните следующие действия.

1. Перейдите в раздел **Управление производством &gt; Настройка &gt; Маршруты &gt; Маршрутные группы**.
2. Выберите **Создать** для создания группы.
3. В поле **Группа затрат** введите уникальное имя группы затрат, например **НРМАТ**.
4. В поле **Имя** введите описание группы затрат, например **Накладные расходы на материал**.
5. В поле **Тип группы затрат** выберите **Косвенные**.
6. Необязательно: в поле **Поведение** выберите **Постоянные затраты** или **Переменные затраты**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Настройка листа калькуляции затрат для косвенных затрат

После создания одной или нескольких групп затрат можно настроить лист калькуляции затрат с косвенными затратами и определить порядок расчета. Возможно, потребуется сгруппировать косвенные затраты в листе калькуляции затрат. Для группировки косвенных затрат можно создать дополнительный заголовок на листе калькуляции затрат. Необходимо создать хотя бы один узел для каждой группы затрат в листе калькуляции затрат. Для каждой группы затрат по косвенным затратам можно добавить еще несколько расчетов косвенных затрат.

### <a name="indirect-cost-node-types"></a>Типы узлов косвенных затрат

В этом разделе описаны различные типы узлов косвенных затрат.

#### <a name="surcharge"></a>Доплата

**Доплата** является одним из наиболее распространенных типов косвенных затрат. В этом случае процент затрат рассчитывается на основе базы распределения затрат по производственному заказу. Можно определить базу распределения, выбрав группы затрат, связанные с компонентами материалов или времени в листе калькуляции затрат.

Например, к затратам на производство для всех видов сырья в производственном заказе может быть добавлена 3-процентная доплата.

#### <a name="rate"></a>Ставка

Косвенные затраты типа **Ставка** используются для добавления фиксированной суммы затрат в производственный заказ на основе базы распределения затрат по производственному заказу. Ставка может основываться на одном из трех подтипов:

- **Процесс** — ставка зависит от времени выполнения в маршруте.
- **Настройка** — ставка зависит от времени настройки в маршруте.
- **Количество** — ставка зависит от произведенного количества.

Можно определить базу распределения, выбрав группы затрат, связанные с компонентами материалов или времени в листе калькуляции затрат.

Например, фиксированная сумма в размере 2,00 долларов США добавляется к каждому производственному заказу в зависимости от времени выполнения в маршруте для группы затрат на труд в листе калькуляции затрат.

#### <a name="output-unit-based"></a>На основе исходящих единиц измерения

Косвенные затраты типа **На основе исходящих единиц измерения** рассчитываются путем умножения суммы, указанной на экспресс-вкладке **Ставка** листа калькуляции затрат, на выбранный подтип. В качестве множителя для косвенных затрат можно выбрать количество, вес или объем готовой продукции.

Например, в данном случае используется количество для расчета амортизации оборудования в размере 1,50 долларов США для каждого производимого количества. В другом примере используется объем для расчета затрат в размере 2,00 долларов США на охлаждение объема пространства, которое занимает готовая продукция в холодильниках.

#### <a name="input-unit-based"></a>На основе входящих единиц измерения

Косвенные затраты типа **На основе входящих единиц измерения** рассчитывается путем умножения количества сырья, которое потребляется в производственном заказе, на сумму. Для расчета итогового значения можно использовать вес или объем входных данных в производственном заказе. Можно ограничить расчет подмножеством материалов, выбрав одну или несколько групп затрат на экспресс-вкладке **База распределения** листа калькуляции затрат.

Например, можно использовать объем входных данных для конкретной группы затрат, связанной с охлажденной продукцией, чтобы добавить 1,00 доллар США в производственный заказ.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Создание итогового узла для косвенных затрат на листе калькуляции затрат

Чтобы создать итоговый узел для косвенных затрат на листе калькуляции затрат, выполните следующие действия.

1. Перейдите в раздел **Управление затратами &gt; Настройка учетных политик косвенных затрат &gt; Лист калькуляции**.
2. В дереве выберите узел, который представляет стоимость произведенных товаров.
3. Выберите **Создать** для создания узла.
4. В поле **Выбрать тип узла** выберите **Итого**.
5. В поле **Код** введите уникальный код узла, например, **Производственные накладные расходы**.
6. Выберите флажок **Заголовок**.
7. Выберите флажок **Итого**.
8. Нажмите **ОК**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Создание узла группы косвенных затрат на листе калькуляции затрат

Чтобы создать узел группы косвенных затрат на листе калькуляции затрат, выполните следующие действия.

1. Перейдите в раздел **Управление затратами &gt; Настройка учетных политик косвенных затрат &gt; Лист калькуляции**.
2. В дереве выберите узел, для которого необходимо создать косвенные затраты. Например, выберите итоговый узел для параметра **Производственные накладные расходы**.
3. Выберите **Создать** для создания узла.
4. В поле **Выбрать тип узла** выберите **Группа затрат**.
5. В поле **Код** введите уникальный код узла, например, **ТРАНСП**.
6. В поле **Описание** введите краткое описание, например **Транспортные накладные расходы**.
7. Нажмите **ОК**.
8. В поле **Группа затрат** выберите группу затрат, например, **OVH1: транспортные накладные расходы**.

### <a name="create-a-surcharge-indirect-cost"></a>Создание косвенных затрат для доплаты

Чтобы создать косвенные затраты для доплаты на листе калькуляции затрат, выполните следующие действия.

1. Перейдите в раздел **Управление затратами &gt; Настройка учетных политик косвенных затрат &gt; Лист калькуляции**.
2. В дереве выберите узел группы косвенных затрат, для которого необходимо создать косвенные затраты. Например, выберите итоговый узел для параметра **ТРАНСП — транспортные накладные расходы**.
3. Выберите **Создать** для создания узла.
4. В поле **Выбрать тип узла** выберите **Доплата**.
5. В поле **Код** введите уникальный код узла, например, **Доплата за транспортировку**.
6. Нажмите **ОК**.
7. В поле **Подтип** выберите **Итого**.
8. На экспресс-вкладке **База распределения** выберите **Создать**, чтобы создать код затрат.
9. В поле **Код** выберите группу затрат, которая будет использоваться для расчета доплаты.
10. Необязательно: повторите шаги с 8 по 9 для каждой дополнительной группы затрат, которую необходимо использовать для расчета.
11. На экспресс-вкладке **Доплата** выберите **Создать**, чтобы создать новую ставку.
12. В поле **Версия** выберите версию учета затрат, в которую требуется добавить доплату.
13. Необязательно: в поле **Место** введите место, к которому применяется доплата.
14. В поле **Процент** введите процентное значение для расчета по производственным заказам из групп затрат, которые определены на экспресс-вкладке **База распределения**.
15. На экспресс-вкладке **Разноски главной книги** выберите счет ГК, который будет использоваться для полей **Распределенные оценочные косвенные затраты**, **Оценочная стоимость понесенных косвенных затрат, НЗП**, **Распределенные косвенные затраты** и **Стоимость понесенных косвенных затрат, НЗП**.
16. Необязательно: на экспресс-вкладке **Финансовые аналитики** укажите финансовые аналитики для ввода по умолчанию в проводках при разнесении в главную книгу.

В предыдущей процедуре показано, как создать косвенные затраты для типа **Доплаты**. Аналогичные шаги используются для создания других типов косвенных затрат. В следующих разделах описаны различия для каждого типа.

#### <a name="rate"></a>Ставка

- На шаге 4 выберите **Ставка** вместо **Доплаты**.
- На шаге 7 выберите **Процесс**, **Настройка** или **Количество** вместо **Итого**.
- На шаге 11 используйте экспресс-вкладку **Ставка** вместо экспресс-вкладки **Доплата**.
- На шаге 14 введите сумму в поле **Сумма** вместо процента в поле **Процент**.

#### <a name="output-unit-based"></a>На основе исходящих единиц измерения

- На шаге 4 выберите **На основе исходящих единиц измерения** вместо **Доплата**.
- На шаге 7 выберите **Количество**, **Вес** или **Объем** вместо **Итого**.
- Пропустите шаги 8–10.
- На шаге 11 используйте экспресс-вкладку **Ставка** вместо экспресс-вкладки **Доплата**.

#### <a name="input-unit-based"></a>На основе входящих единиц измерения

- На шаге 4 выберите **На основе входящих единиц измерения** вместо **Доплата**.
- На шаге 7 выберите **Количество** или **Объем** вместо **Итого**.
- На шаге 11 используйте экспресс-вкладку **Ставка** вместо экспресс-вкладки **Доплата**.
